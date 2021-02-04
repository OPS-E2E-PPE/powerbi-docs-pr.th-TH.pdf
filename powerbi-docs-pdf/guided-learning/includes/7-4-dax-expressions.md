---
ms.openlocfilehash: f22c12ec0ad5bd413f3658704132143c878df1aa
ms.sourcegitcommit: 7aa0136f93f88516f97ddd8031ccac5d07863b92
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/05/2020
ms.locfileid: "73800174"
---
<span data-ttu-id="8e31e-101">การใช้**ตัวแปร**คือจุดที่มีประสิทธิภาพของนิพจน์ DAX</span><span class="sxs-lookup"><span data-stu-id="8e31e-101">Using **variables** are an extremely powerful part of a DAX expression.</span></span>

![](media/7-4-dax-expressions/dax-variables_1.png)

<span data-ttu-id="8e31e-102">คุณสามารถกำหนดตัวแปรได้ทุกที่ในนิพจน์ DAX โดยใช้ไวยากรณ์ต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="8e31e-102">You can define a variable anywhere in a DAX expression, using the following syntax:</span></span>

    VARNAME = RETURNEDVALUE

<span data-ttu-id="8e31e-103">ตัวแปรสามารถเป็นชนิดข้อมูลใดก็ได้ รวมถึงเป็นได้ทั้งตาราง</span><span class="sxs-lookup"><span data-stu-id="8e31e-103">Variables can be any data type, including entire tables.</span></span>

<span data-ttu-id="8e31e-104">โปรดจำไว้ว่าเมื่อคุณอ้างอิงตัวแปรในนิพจน์ DAX ทุกครั้ง Power BI จะต้องคำนวณค่าของตัวเองใหม่ให้ตรงตามข้อกำหนดของคุณ</span><span class="sxs-lookup"><span data-stu-id="8e31e-104">Keep in mind that each time you reference a variable in your DAX expression, Power BI must recalculate its value according to your definition.</span></span> <span data-ttu-id="8e31e-105">เนื่องด้วยเหตุนี้ การหลีกเลี่ยงตัวแปรที่ซ้ำกันในฟังก์ชันของคุณจึงเป็นสิ่งที่ดี</span><span class="sxs-lookup"><span data-stu-id="8e31e-105">For this reason, it's good practice to avoid repeating variables in your function.</span></span>

> <span data-ttu-id="8e31e-106">เนื้อหาวิดีโอโดย [Alberto Ferrari, SQBI](https://www.sqlbi.com/learning-dax)</span><span class="sxs-lookup"><span data-stu-id="8e31e-106">Video content courtesy of [Alberto Ferrari, SQLBI](https://www.sqlbi.com/learning-dax)</span></span>
> 
> 

