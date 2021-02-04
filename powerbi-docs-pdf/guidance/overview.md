---
title: คำแนะนำสำหรับ Power BI
description: เอกสารคำแนะนำมีแนวทางปฏิบัติที่แนะนำให้ดำเนินการเมื่อใช้ Power BI
author: maggiesMSFT
ms.author: maggies
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi
ms.topic: conceptual
ms.date: 09/27/2019
ms.openlocfilehash: 20144222b1c2f05b48d018e352985b80ba1fa06e
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96419348"
---
# <a name="guidance-for-power-bi"></a><span data-ttu-id="7b19e-103">คำแนะนำสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b19e-103">Guidance for Power BI</span></span>

<span data-ttu-id="7b19e-104">ในส่วนนี้คุณจะพบคำแนะนำและแนวทางปฏิบัติที่แนะนำสำหรับ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b19e-104">Here you will find the guidance and recommended practices for Power BI.</span></span> <span data-ttu-id="7b19e-105">จะมีการอัปเดตและเพิ่มคำแนะนำเป็นประจำ</span><span class="sxs-lookup"><span data-stu-id="7b19e-105">Guidance will continue to be updated and added to.</span></span>

## <a name="data-modeling"></a><span data-ttu-id="7b19e-106">การสร้างแบบจำลองข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7b19e-106">Data modeling</span></span>

| <span data-ttu-id="7b19e-107">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="7b19e-107">Guidance</span></span> | <span data-ttu-id="7b19e-108">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7b19e-108">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="7b19e-109">ทำความเข้าใจแบบจำลองมิติที่มีลักษณะคล้ายดาวและความสำคัญที่มีต่อ Power BI</span><span class="sxs-lookup"><span data-stu-id="7b19e-109">Understand star schema and the importance for Power BI</span></span>](star-schema.md) | <span data-ttu-id="7b19e-110">อธิบายการออกแบบแบบจำลองมิติที่มีลักษณะคล้ายดาวและความสัมพันธ์ของการออกแบบนั้นเพื่อพัฒนาแบบจำลองข้อมูล Power BI ที่ปรับให้เหมาะสมเพื่อประสิทธิภาพการทำงานและความสามารถในการใช้งาน</span><span class="sxs-lookup"><span data-stu-id="7b19e-110">Describes star schema design and its relevance to developing Power BI data models optimized for performance and usability.</span></span> |
| [<span data-ttu-id="7b19e-111">เทคนิคการลดข้อมูลเพื่อการนำเข้าการสร้างแบบจำลอง</span><span class="sxs-lookup"><span data-stu-id="7b19e-111">Data reduction techniques for Import modeling</span></span>](import-modeling-data-reduction.md) | <span data-ttu-id="7b19e-112">อธิบายเทคนิคที่แตกต่างกันเพื่อช่วยลดข้อมูลที่โหลดลงในแบบจำลองการนำเข้า</span><span class="sxs-lookup"><span data-stu-id="7b19e-112">Describes different techniques to help reduce the data loaded into Import models.</span></span> |

## <a name="dax"></a><span data-ttu-id="7b19e-113">DAX</span><span class="sxs-lookup"><span data-stu-id="7b19e-113">DAX</span></span>

| <span data-ttu-id="7b19e-114">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="7b19e-114">Guidance</span></span> | <span data-ttu-id="7b19e-115">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7b19e-115">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="7b19e-116">DAX: ฟังก์ชันการแบ่งเทียบกับตัวดำเนินการหาร (/)</span><span class="sxs-lookup"><span data-stu-id="7b19e-116">DAX: DIVIDE function vs divide operator (/)</span></span>](dax-divide-function-operator.md) | <span data-ttu-id="7b19e-117">อธิบายเกี่ยวกับการใช้ฟังก์ชันการแบ่งที่เหมาะสมภายใน DAX</span><span class="sxs-lookup"><span data-stu-id="7b19e-117">Describes proper use of the DIVIDE function within DAX.</span></span> |

## <a name="dataflows"></a><span data-ttu-id="7b19e-118">กระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7b19e-118">Dataflows</span></span>

| <span data-ttu-id="7b19e-119">คำแนะนำ</span><span class="sxs-lookup"><span data-stu-id="7b19e-119">Guidance</span></span> | <span data-ttu-id="7b19e-120">คำอธิบาย</span><span class="sxs-lookup"><span data-stu-id="7b19e-120">Description</span></span> |
| --- | --- |
| [<span data-ttu-id="7b19e-121">แนวทางปฏิบัติที่ดีที่สุดสำหรับกระแสข้อมูล</span><span class="sxs-lookup"><span data-stu-id="7b19e-121">Dataflows best practice</span></span>](../transform-model/dataflows/dataflows-introduction-self-service.md) | <span data-ttu-id="7b19e-122">อธิบายเกี่ยวกับแนวทางปฏิบัติที่ดีที่สุดสำหรับการออกแบบกระแสข้อมูลใน Power BI</span><span class="sxs-lookup"><span data-stu-id="7b19e-122">Describes best practices for designing dataflows in Power BI.</span></span> |

<span data-ttu-id="7b19e-123">มีคำถามเพิ่มเติมหรือไม่</span><span class="sxs-lookup"><span data-stu-id="7b19e-123">More questions?</span></span> [<span data-ttu-id="7b19e-124">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="7b19e-124">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)