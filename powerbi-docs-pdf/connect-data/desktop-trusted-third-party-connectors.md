---
title: ตัวเชื่อมต่อบุคคลที่สามที่เชื่อถือได้ใน Power BI
description: วิธีการเชื่อถือตัวเชื่อมต่อบุคคลที่สามที่ลงนามแล้วใน Power BI
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 04/3/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: aa135853119615c8be626699daffca88c03633fb
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96410884"
---
# <a name="trusted-third-party-connectors"></a><span data-ttu-id="afc3b-103">ตัวเชื่อมต่อจากบุคคลที่สามที่เชื่อถือได้</span><span class="sxs-lookup"><span data-stu-id="afc3b-103">Trusted third-party connectors</span></span>

## <a name="why-do-you-need-trusted-third-party-connectors"></a><span data-ttu-id="afc3b-104">เพราะเหตุใดคุณจึงต้องการตัวเชื่อมต่อบุคคลที่สามที่เชื่อถือได้?</span><span class="sxs-lookup"><span data-stu-id="afc3b-104">Why do you need trusted third-party connectors?</span></span>

<span data-ttu-id="afc3b-105">ใน Power BI โดยทั่วไปเราขอแนะนำให้รักษาระดับ 'การรักษาความปลอดภัยของส่วนขยายข้อมูล' ของคุณให้อยู่ในระดับที่สูงขึ้น ซึ่งจะช่วยป้องกันการโหลดรหัสที่ไม่ผ่านการรับรองจาก Microsoft</span><span class="sxs-lookup"><span data-stu-id="afc3b-105">In Power BI, we generally recommend keeping your 'Data extension security' level at the higher level, which prevents loading of code not certified by Microsoft.</span></span> <span data-ttu-id="afc3b-106">อย่างไรก็ตามอาจมีหลายกรณีที่คุณต้องการโหลดตัวเชื่อมต่อเฉพาะ - ตัวเชื่อมต่อที่คุณเขียนขึ้น หรือที่ให้ไว้กับคุณโดยที่ปรึกษาหรือผู้จำหน่ายนอกเหนือจากเส้นทางการรับรองของ Microsoft</span><span class="sxs-lookup"><span data-stu-id="afc3b-106">However, there may be many cases in which you want to load specific connectors--ones you've written, or ones provided to you by a consultant or vendor outside the Microsoft certification path.</span></span>

<span data-ttu-id="afc3b-107">นักพัฒนาตัวเชื่อมต่อที่กำหนดสามารถลงนามด้วยใบรับรอง และให้ข้อมูลที่คุณต้องการเพื่อโหลดตัวเชื่อมต่ออย่างปลอดภัยโดยไม่ลดระดับการตั้งค่าความปลอดภัยของคุณ</span><span class="sxs-lookup"><span data-stu-id="afc3b-107">The developer of a given connector can sign it with a certificate and provide you with the information you need to securely load it without lowering your security settings.</span></span>

<span data-ttu-id="afc3b-108">ถ้าคุณต้องการทราบข้อมูลเพิ่มเติมเกี่ยวกับการตั้งค่าความปลอดภัย คุณสามารถอ่านข้อมูลเพิ่มเติมได้ [ที่นี่](./desktop-connector-extensibility.md)</span><span class="sxs-lookup"><span data-stu-id="afc3b-108">If you want to know more about the security settings, you can read about them [here](./desktop-connector-extensibility.md).</span></span>

## <a name="using-the-registry-to-trust-third-party-connectors"></a><span data-ttu-id="afc3b-109">ใช้รีจิสตรีเพื่อเชื่อถือตัวเชื่อมต่อบุคคลที่สาม</span><span class="sxs-lookup"><span data-stu-id="afc3b-109">Using the registry to trust third-party connectors</span></span>

<span data-ttu-id="afc3b-110">การเชื่อถือตัวเชื่อมต่อบุคคลที่สามใน Power BI ทำได้โดยการระบุรหัสประจำตัวของใบรับรองที่คุณต้องการเชื่อถือในค่ารีจิสตรีที่ระบุ</span><span class="sxs-lookup"><span data-stu-id="afc3b-110">Trusting third-party connectors in Power BI is done by listing the thumbprint of the certificate you want to trust in a specified registry value.</span></span> <span data-ttu-id="afc3b-111">หากรหัสประจำตัวนี้ตรงกับรหัสประจำตัวของใบรับรองในตัวเชื่อมต่อที่คุณต้องการโหลด คุณจะสามารถโหลดตัวเชื่อมต่อได้ในระดับความปลอดภัย 'แนะนำ' ของ Power BI</span><span class="sxs-lookup"><span data-stu-id="afc3b-111">If this thumbprint matches the thumbprint of the certificate on the connector you want to load, you will be able to load it in the ‘Recommended’ security level of Power BI.</span></span> 

<span data-ttu-id="afc3b-112">เส้นทางรีจิสทรีคือ HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="afc3b-112">The registry path is HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Power BI Desktop.</span></span> <span data-ttu-id="afc3b-113">ตรวจสอบให้แน่ใจว่ามีเส้นทางอยู่แล้ว หรือสร้างเส้นทางขึ้นมา</span><span class="sxs-lookup"><span data-stu-id="afc3b-113">Make sure the path exists, or create it.</span></span> <span data-ttu-id="afc3b-114">เราเลือกตำแหน่งที่ตั้งนี้เนื่องจากมีการควบคุมจากนโยบายด้าน IT เป็นหลัก รวมถึงต้องมีการเข้าถึงการจัดการเครื่องภายในเพื่อแก้ไขด้วย</span><span class="sxs-lookup"><span data-stu-id="afc3b-114">We chose this location due to it being primarily controlled by IT policy, as well as requiring local machine administration access to edit.</span></span> 

![รีจิสทรีของ Power BI Desktop ที่ไม่มีการตั้งค่าคีย์ของบุคคลที่สามที่เชื่อถือได้](media/desktop-trusted-third-party-connectors/desktoptrustedthird1.png)

<span data-ttu-id="afc3b-116">เพิ่มค่าใหม่ภายใต้เส้นทางที่ระบุไว้ด้านบน</span><span class="sxs-lookup"><span data-stu-id="afc3b-116">Add a new value under the path specified above.</span></span> <span data-ttu-id="afc3b-117">ชนิดควรเป็น “ค่าหลายสตริง” (REG_MULTI_SZ) และควรเรียกว่า “TrustedCertificateThumbprints”</span><span class="sxs-lookup"><span data-stu-id="afc3b-117">The type should be “Multi-String Value” (REG_MULTI_SZ), and it should be called “TrustedCertificateThumbprints”</span></span> 

![รีจิสทรีของ Power BI Desktop ที่มีรายการสำหรับตัวเชื่อมต่อบุคคลที่สามที่เชื่อถือได้ แต่ไม่มีคีย์](media/desktop-trusted-third-party-connectors/desktoptrustedthird2.png)

<span data-ttu-id="afc3b-119">เพิ่มรหัสประจำตัวของใบรับรองที่คุณต้องการเชื่อถือ</span><span class="sxs-lookup"><span data-stu-id="afc3b-119">Add the thumbprints of the certificates you want to trust.</span></span> <span data-ttu-id="afc3b-120">คุณสามารถเพิ่มใบรับรองหลายใบโดยใช้ “\0” เป็นตัวคั่น หรือในตัวแก้ไขรีจิสทรีให้คลิกขวา -> แก้ไขและใส่รหัสประจำตัวแต่ละรายการในบรรทัดใหม่</span><span class="sxs-lookup"><span data-stu-id="afc3b-120">You can add multiple certificates by using “\0” as a delimiter, or in the registry editor, right click -> modify and put each thumbprint on a new line.</span></span> <span data-ttu-id="afc3b-121">ตัวอย่างรหัสประจำตัวนำมาจากใบรับรองแบบลงนามด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="afc3b-121">Example thumbprint is taken from a self-signed certificate.</span></span> 

 ![รีจิสทรีของ Power BI Desktop ที่มีการตั้งค่าคีย์ของบุคคลที่สามที่เชื่อถือได้](media/desktop-trusted-third-party-connectors/desktoptrustedthird3.png)

<span data-ttu-id="afc3b-123">ถ้าคุณทำตามคำแนะนำอย่างถูกต้องและได้รับรหัสประจำตัวที่เหมาะสมโดยนักพัฒนาของคุณ ตอนนี้คุณควรจะสามารถเชื่อมั่นในตัวเชื่อมต่อที่ลงนามด้วยใบรับรองที่เกี่ยวข้องได้อย่างปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="afc3b-123">If you’ve followed the instructions properly, and have been given the proper thumbprint by your developer, you should now be able to securely trust connectors signed with the associated certificate.</span></span>

## <a name="how-to-sign-connectors"></a><span data-ttu-id="afc3b-124">วิธีการลงนามตัวเชื่อมต่อ</span><span class="sxs-lookup"><span data-stu-id="afc3b-124">How to Sign Connectors</span></span>

<span data-ttu-id="afc3b-125">ถ้าคุณมีตัวเชื่อมต่อที่คุณหรือนักพัฒนาจำเป็นต้องลงนาม คุณสามารถอ่านได้ในเอกสาร Power Query [ที่นี่](/power-query/handlingconnectorsigning)</span><span class="sxs-lookup"><span data-stu-id="afc3b-125">If you have a connector you or a developer need to sign, you can read about it in the Power Query docs [here](/power-query/handlingconnectorsigning).</span></span>