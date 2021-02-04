---
title: 'บริการจากบุคคลที่สาม: ตัวเชื่อมต่อ Facebook สำหรับ Power BI Desktop'
description: 'บริการจากบุคคลที่สาม: ตัวเชื่อมต่อ Facebook สำหรับ Power BI Desktop'
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: how-to
ms.date: 02/20/2020
LocalizationGroup: Connect to data
ms.openlocfilehash: 4f1faf585643c593e194e965dff2bb29988e27d4
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96402581"
---
# <a name="use-the-facebook-connector-for-power-bi-desktop"></a><span data-ttu-id="d0f7b-103">ใช้ตัวเชื่อมต่อ Facebook สำหรับ Power BI Desktop </span><span class="sxs-lookup"><span data-stu-id="d0f7b-103">Use the Facebook connector for Power BI Desktop</span></span>
<span data-ttu-id="d0f7b-104">ตัวเชื่อมต่อ Facebook ใน **Power BI Desktop** อาศัย Facebook Graph API</span><span class="sxs-lookup"><span data-stu-id="d0f7b-104">The Facebook connector in **Power BI Desktop** relies on the Facebook Graph API.</span></span> <span data-ttu-id="d0f7b-105">ด้วยเหตุนี้ คุณลักษณะและความพร้อมใช้งานอาจแตกต่างกันเมื่อเวลาผ่านไป</span><span class="sxs-lookup"><span data-stu-id="d0f7b-105">As such, features and availability may vary over time.</span></span>

<span data-ttu-id="d0f7b-106">คุณสามารถดู[บทช่วยสอนเกี่ยวกับตัวเชื่อมต่อ Facebook สำหรับ Power BI Desktop](desktop-tutorial-facebook-analytics.md)ได้</span><span class="sxs-lookup"><span data-stu-id="d0f7b-106">You can see a [tutorial about the Facebook Connector for Power BI Desktop](desktop-tutorial-facebook-analytics.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0f7b-107">**การยกเลิกการสนับสนุนของประกาศตัวเชื่อมต่อข้อมูล Facebook:** การนำเข้าและรีเฟรชข้อมูลจาก Facebook ใน Excel จะไม่สามารถทำงานได้อย่างถูกต้องอีกต่อไปโดยเริ่มในเดือนเมษายน 2020</span><span class="sxs-lookup"><span data-stu-id="d0f7b-107">**Deprecation of Facebook data connector notice:** Import and refresh data from Facebook in Excel will no longer work properly beginning in April, 2020.</span></span> <span data-ttu-id="d0f7b-108">คุณสามารถใช้ตัวเชื่อมต่อ *Get & Transform (Power Query)* ของ Facebook ได้จนกว่าจะถึงเวลานั้น</span><span class="sxs-lookup"><span data-stu-id="d0f7b-108">You can use the Facebook *Get & Transform (Power Query)* connector until then.</span></span> <span data-ttu-id="d0f7b-109">หลังจากวันที่ดังกล่าว คุณจะไม่สามารถเชื่อมต่อกับ Facebook และจะได้รับข้อความข้อผิดพลาด</span><span class="sxs-lookup"><span data-stu-id="d0f7b-109">After that date, you will not be able to connect to Facebook, and will receive an error message.</span></span> <span data-ttu-id="d0f7b-110">เราขอแนะนำให้คุณปรับเปลี่ยนหรือลบคิวรี *Get & Transform (Power Query)* ที่มีอยู่ ที่ใช้ตัวเชื่อมต่อ Facebook โดยเร็วที่สุดเพื่อหลีกเลี่ยงผลลัพธ์ที่ไม่คาดคิด</span><span class="sxs-lookup"><span data-stu-id="d0f7b-110">We recommend revising or removing any existing *Get & Transform (Power Query)* queries that use the Facebook connector as soon as possible to avoid unexpected results.</span></span>


<span data-ttu-id="d0f7b-111">Facebook v1.0 ของ Graph API หมดอายุเมื่อวันที่ 30 เมษายน 2015</span><span class="sxs-lookup"><span data-stu-id="d0f7b-111">Facebook expired v1.0 of its Graph API on April 30 2015.</span></span> <span data-ttu-id="d0f7b-112">Power BI ใช้ API Graph เบื้องหลังสำหรับตัวเชื่อมต่อ Facebook ช่วยให้คุณสามารถเชื่อมต่อและวิเคราะห์ข้อมูลของคุณได้</span><span class="sxs-lookup"><span data-stu-id="d0f7b-112">Power BI uses the Graph API behind the scenes for the Facebook connector, allowing you to connect to your data and analyze it.</span></span>

<span data-ttu-id="d0f7b-113">การสอบถามที่สร้างขึ้นก่อนวันที่ 30 เมษายน 2015 อาจไม่สามารถใช้งานได้อีกต่อไปหรือส่งกลับข้อมูลน้อยลง</span><span class="sxs-lookup"><span data-stu-id="d0f7b-113">Queries that were built before April 30 2015 may no longer work or return less data.</span></span> <span data-ttu-id="d0f7b-114">หลังจากวันที่ 30 เมษายน 2015, Power BI ได้นำ v2.8 มาใช้งานในทุกการใช้งานไปยัง Facebook API</span><span class="sxs-lookup"><span data-stu-id="d0f7b-114">Subsequent to April 30 2015, Power BI leverages v2.8 in all calls to the Facebook API.</span></span> <span data-ttu-id="d0f7b-115">ถ้าการสอบถามของคุณสร้างขึ้นก่อนวันที่ 30 เมษายน 2015 และคุณยังไม่ได้ใช้มาตั้งแต่วันที่ดังกล่าว คุณอาจต้องรับรองความถูกต้องอีกครั้งเพื่ออนุมัติชุดสิทธิ์ที่เราจะขอใหม่</span><span class="sxs-lookup"><span data-stu-id="d0f7b-115">If your query was built prior to April 30, 2015 and you have not used it since, you’ll likely need to authenticate again, to approve the new set of permissions that we’ll ask for.</span></span>

<span data-ttu-id="d0f7b-116">แม้ว่าเราพยายามเผยแพร่อัปเดตที่สอดคล้องกับการเปลี่ยนแปลงใด ๆ API อาจเปลี่ยนแปลงในลักษณะที่ส่งผลกระทบต่อผลลัพธ์ของการสอบถามที่เราสร้างขึ้นได้</span><span class="sxs-lookup"><span data-stu-id="d0f7b-116">Although we attempt to release updates in accordance with any changes, the API may change in a way that affects the results of the queries we generate.</span></span> <span data-ttu-id="d0f7b-117">ในบางกรณี บางแบบสอบถามอาจไม่สนับสนุนอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="d0f7b-117">In some cases, certain queries may no longer be supported.</span></span> <span data-ttu-id="d0f7b-118">เนื่องจากการต้องพึ่งพาจากบุคคลที่สามนี้ เราไม่สามารถรับประกันผลลัพธ์การสอบถามของคุณเมื่อใช้ตัวเชื่อมต่อนี้ได้</span><span class="sxs-lookup"><span data-stu-id="d0f7b-118">Due to this dependency, we cannot guarantee the results of your queries when using this connector.</span></span>

<span data-ttu-id="d0f7b-119">รายละเอียดเพิ่มเติมเกี่ยวกับการเปลี่ยนแปลงใน Facebook API ที่พร้อมใช้งาน[ที่นี่](https://developers.facebook.com/docs/apps/changelog#v2_0)</span><span class="sxs-lookup"><span data-stu-id="d0f7b-119">More details on the change in the Facebook API are available [here](https://developers.facebook.com/docs/apps/changelog#v2_0).</span></span>

