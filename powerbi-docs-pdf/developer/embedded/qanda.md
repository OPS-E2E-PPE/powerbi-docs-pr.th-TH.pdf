---
title: Q&A ในการวิเคราะห์แบบฝังของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: การวิเคราะห์แบบฝังของ Power BI ให้คุณสามารถรวม ถามตอบ เข้าไปในแอปพลิเคชัน และอนุญาตให้ผู้ใช้ของคุณถามคำถามด้วยภาษาธรรมชาติ เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 11/20/2017
ms.openlocfilehash: 43e886e6472c6d95b900ccdb5c2e73b8dca3d4a0
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886614"
---
# <a name="qa-in-power-bi-embedded-analytics"></a><span data-ttu-id="504e7-104">Q&A ในการวิเคราะห์แบบฝังตัวของ Power BI</span><span class="sxs-lookup"><span data-stu-id="504e7-104">Q&A in Power BI embedded analytics</span></span>

<span data-ttu-id="504e7-105">การวิเคราะห์แบบฝังตัวของ Power BI ให้คุณสามารถรวม ถามตอบ เข้าไปในแอปพลิเคชัน และอนุญาตให้ผู้ใช้ของคุณถามคำถามด้วยภาษาธรรมชาติ และได้รับคำตอบทันทีในรูปวิชวล เช่น แผนภูมิ หรือกราฟ</span><span class="sxs-lookup"><span data-stu-id="504e7-105">Power BI embedded analytics offers you a way to incorporate Q&A into an application and allow your users to ask questions using natural language and receive immediate answers in the form of visuals like charts or graphs.</span></span>

![การโต้ตอบกับถามตอบ ในเฟรมฝังตัว](media/qanda/embedded-qanda.gif)

<span data-ttu-id="504e7-107">มีสองโหมดสำหรับการฝังตัวถามตอบ ในแอปพลิเคชันของคุณ: **โต้ตอบ** และ **เฉพาะผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="504e7-107">There are two modes for embedding Q&A within your application: **interactive** and **result only**.</span></span> <span data-ttu-id="504e7-108">โหมด **โต้ตอบ** ช่วยให้คุณสามารถพิมพ์คำถาม และแสดงคำถามอยู่ภายในวิชวล</span><span class="sxs-lookup"><span data-stu-id="504e7-108">**Interactive** mode allows you to type in questions and have them displayed within the visual.</span></span> <span data-ttu-id="504e7-109">ถ้าคุณมีคำถามที่บันทึกไว้ หรือตั้งค่าคำถามที่คุณต้องการแสดง คุณสามารถใช้โหมด **เฉพาะผลลัพธ์** โดยการใส่คำถามของคุณในการกำหนดค่าการฝังตัวได้</span><span class="sxs-lookup"><span data-stu-id="504e7-109">If you have a saved question, or a set question you want to display, you can use the **result only** mode by populating the question in your embed config.</span></span>

<span data-ttu-id="504e7-110">ลองมาดูรหัส JavaScript ว่ามีลักษณะเป็นอย่างไร</span><span class="sxs-lookup"><span data-stu-id="504e7-110">Here is a look at what the JavaScript code will look like.</span></span>

```javascript
// Embed configuration used to describe the what and how to embed.
// This object is used when calling powerbi.embed within the JavaScript API.
// You can find more information at https://github.com/Microsoft/PowerBI-JavaScript/wiki/Embed-Configuration-Details.
var config= {
    type: 'qna',
    tokenType:   models.TokenType.Embed | models.TokenType.Aad,
    accessToken: access token value,
    embedUrl:    https://app.powerbi.com/qnaEmbed (groupId to be appended as query parameter if required),
    datasetIds:  array of requested data set ids (at the moment we support only one dataset),
    viewMode:    models.QnaMode.Interactive | models.QnaMode.ResultOnly,
    question:    optional parameter for Explore mode (QnaMode.Interactive) and mandatory for Render Result mode (QnaMode.ResultOnly)
};

// Get a reference to the embedded QNA HTML element
var qnaContainer = $('#qnaContainer')[0];

// Embed the QNA and display it within the div container.
var qna = powerbi.embed(qnaContainer, config);
```

## <a name="set-question"></a><span data-ttu-id="504e7-111">ตั้งค่าคำถาม</span><span class="sxs-lookup"><span data-stu-id="504e7-111">Set question</span></span>

<span data-ttu-id="504e7-112">ถ้าคุณใช้ **โหมดผลลัพธ์** ด้วยคำถามที่ตั้งค่าไว้ คุณสามารถเพิ่มเติมคำถามลงในเฟรม และให้ตอบทันทีแทนที่ผลลัพธ์เดิม</span><span class="sxs-lookup"><span data-stu-id="504e7-112">If you used **result mode** with a set question, you can inject additional questions into the frame and have them immediately answered replacing the previous result.</span></span> <span data-ttu-id="504e7-113">วิชวลที่ตรงกับคำถามใหม่จะถูกแสดงแทน</span><span class="sxs-lookup"><span data-stu-id="504e7-113">A new visual is rendered matching the new question.</span></span>

<span data-ttu-id="504e7-114">ตัวอย่างหนึ่งของการใช้งานนี้ คือรายการคำถามที่ถามบ่อย</span><span class="sxs-lookup"><span data-stu-id="504e7-114">One example of this usage would be a frequently asked question list.</span></span> <span data-ttu-id="504e7-115">ผู้ใช้สามารถไปตามคำถามต่าง ๆ และได้รับคำตอบภายในส่วนฝังตัวเดียวกัน</span><span class="sxs-lookup"><span data-stu-id="504e7-115">The user could go through the questions and have them answered within the same embedded part.</span></span>

<span data-ttu-id="504e7-116">**โค้ดส่วนย่อสำหรับใช้ใน JS SDK:**</span><span class="sxs-lookup"><span data-stu-id="504e7-116">**Code snippet for JS SDK usage:**</span></span>  

```javascript
// Get a reference to the embedded Q&A HTML element
var qnaContainer = $('#qnaContainer')[0];

// Get a reference to the embedded Q&A.
qna = powerbi.get(qnaContainer);

qna.setQuestion("This year sales")
    .then(function (result) {
        …….
    })
    .catch(function (errors) {
        …….
    });
```

## <a name="visual-rendered-event"></a><span data-ttu-id="504e7-117">เหตุการณ์การแสดงผลวิชวล</span><span class="sxs-lookup"><span data-stu-id="504e7-117">Visual rendered event</span></span>

<span data-ttu-id="504e7-118">สำหรับโหมด **โต้ตอบ** แอปพลิเคชันสามารถรับการแจ้งเตือน เหตุการณ์ข้อมูลถูกเปลี่ยนแปลง ทุกครั้งที่วิชวลเปลี่ยนแปลงตามคำถามที่กำลังพิมพ์เข้าไป</span><span class="sxs-lookup"><span data-stu-id="504e7-118">For **interactive** mode, the application can be notified with a data changed event each time the rendered visual changes to target the updated input query as it is being typed.</span></span>

<span data-ttu-id="504e7-119">การฟังเหตุการณ์ *visualRendered* ให้คุณสามารถบันทึกคำถามไว้ใช้ภายหลัง</span><span class="sxs-lookup"><span data-stu-id="504e7-119">Listening to the *visualRendered* event allows you to save questions for use later.</span></span> 

<span data-ttu-id="504e7-120">**โค้ดส่วนย่อสำหรับใช้ใน JS SDK:**</span><span class="sxs-lookup"><span data-stu-id="504e7-120">**Code snippet for JS SDK usage:**</span></span>  

```javascript
// Get a reference to the embedded Q&A HTML element
var qnaContainer = $('#qnaContainer')[0];

// Get a reference to the embedded Q&A.
qna = powerbi.get(qnaContainer);

// qna.off removes a given event listener if it exists.
qna.off("visualRendered");

// qna.on will add an event listener.
qna.on("visualRendered", function(event) {
     …….
});
```

## <a name="embed-token"></a><span data-ttu-id="504e7-121">โทเค็นสำหรับฝังตัว</span><span class="sxs-lookup"><span data-stu-id="504e7-121">Embed token</span></span>

<span data-ttu-id="504e7-122">สร้างโทเค็นฝังตัวจากชุดข้อมูล เพื่อเริ่มส่วนถามตอบ</span><span class="sxs-lookup"><span data-stu-id="504e7-122">Create an embed token off of a dataset to start a Q&A part.</span></span> <span data-ttu-id="504e7-123">สำหรับข้อมูลเพิ่มเติม ดูที่[สร้างโทเค็น](/rest/api/power-bi/embedtoken)</span><span class="sxs-lookup"><span data-stu-id="504e7-123">For more information, see [Generate token](/rest/api/power-bi/embedtoken).</span></span>

## <a name="next-steps"></a><span data-ttu-id="504e7-124">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="504e7-124">Next steps</span></span>

<span data-ttu-id="504e7-125">ถ้าต้องการทดลองการฝังตัวถามตอบ ดู[ตัวอย่างการฝังตัวด้วย JavaScript](https://microsoft.github.io/PowerBI-JavaScript/demo/)</span><span class="sxs-lookup"><span data-stu-id="504e7-125">To give Q&A embedding a try, check out the [JavaScript embed sample](https://microsoft.github.io/PowerBI-JavaScript/demo/).</span></span>

<span data-ttu-id="504e7-126">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="504e7-126">More questions?</span></span> [<span data-ttu-id="504e7-127">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="504e7-127">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)