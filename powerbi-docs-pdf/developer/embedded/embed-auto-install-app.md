---
title: ติดตั้งแอป Power BI อัตโนมัติเมื่อทำการฝังสำหรับองค์กรของคุณโดยใช้การวิเคราะห์แบบฝังของ Power BI เพื่อสร้างข้อมูลเชิงลึก BI แบบฝัง
description: เรียนรู้วิธีการติดตั้งแอป Power BI อัตโนมัติเมื่อทำการฝังสำหรับองค์กรของคุณโดยใช้การวิเคราะห์แบบฝังของ Power BI เพื่อสร้างข้อมูลเชิงลึก BI แบบฝัง
author: KesemSharabi
ms.author: kesharab
ms.topic: how-to
ms.service: powerbi
ms.subservice: powerbi-developer
ms.custom: ''
ms.date: 04/16/2019
ms.openlocfilehash: 66ba3b7d573c86b32a91bc0a98cd5ec0775fec75
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565834"
---
# <a name="auto-install-power-bi-apps-when-embedding-for-your-organization"></a><span data-ttu-id="ae502-103">ติดตั้งแอป Power BI อัตโนมัติเมื่อมีการฝังสำหรับองค์กรของคุณ</span><span class="sxs-lookup"><span data-stu-id="ae502-103">Auto-install Power BI apps when embedding for your organization</span></span>

<span data-ttu-id="ae502-104">หากต้องการฝังเนื้อหาจากแอป ผู้ใช้ที่เป็นผู้ฝังจะต้องมี[สิทธิ์การเข้าถึงแอป](../../collaborate-share/service-create-distribute-apps.md)</span><span class="sxs-lookup"><span data-stu-id="ae502-104">To embed content from an app, the user that is embedding must have [access to the app](../../collaborate-share/service-create-distribute-apps.md).</span></span> <span data-ttu-id="ae502-105">ถ้าติดตั้งแอปสำหรับผู้ใช้แล้ว การฝังจะทำงานได้อย่างราบรื่น</span><span class="sxs-lookup"><span data-stu-id="ae502-105">If the app is installed for the user, then embedding works smoothly.</span></span> <span data-ttu-id="ae502-106">สำหรับข้อมูลเพิ่มเติม โปรดดูที่[ฝังรายงานหรือแดชบอร์ดจากแอป](./index.yml)</span><span class="sxs-lookup"><span data-stu-id="ae502-106">For more information, see [Embed reports or dashboards from app](./index.yml).</span></span> <span data-ttu-id="ae502-107">คุณสามารถกำหนดใน PowerBI.com ที่ทุกแอปสามารถ[ติดตั้งได้โดยอัตโนมัติ](https://powerbi.microsoft.com/blog/automatically-install-apps/)</span><span class="sxs-lookup"><span data-stu-id="ae502-107">It's possible to define in PowerBI.com that all apps can be [installed automatically](https://powerbi.microsoft.com/blog/automatically-install-apps/).</span></span> <span data-ttu-id="ae502-108">อย่างไรก็ตาม การดำเนินการนี้จะต้องทำในระดับผู้เช่า และใช้กับทุกแอป</span><span class="sxs-lookup"><span data-stu-id="ae502-108">However, this action is done at the tenant level and applies to all apps.</span></span>

## <a name="auto-install-app-on-embedding"></a><span data-ttu-id="ae502-109">ติดตั้งแอปโดยอัตโนมัติเมื่อมีการฝัง</span><span class="sxs-lookup"><span data-stu-id="ae502-109">Auto-install app on embedding</span></span>

<span data-ttu-id="ae502-110">ถ้าผู้ใช้มีสิทธิ์เข้าถึงแอป แต่ยังไม่ได้ติดตั้งแอป การฝังจะล้มเหลว</span><span class="sxs-lookup"><span data-stu-id="ae502-110">If a user has access to an app, but the app isn't installed, then embedding fails.</span></span> <span data-ttu-id="ae502-111">เพื่อหลีกเลี่ยงความล้มเหลวเหล่านี้เมื่อมีการฝังจากแอป คุณสามารถอนุญาตให้ติดตั้งแอปโดยอัตโนมัติ เมื่อมีการฝังได้</span><span class="sxs-lookup"><span data-stu-id="ae502-111">So you can avoid these failures when embedding from an app, you can allow auto installation of the app upon embedding.</span></span> <span data-ttu-id="ae502-112">การดำเนินการนี้หมายความว่า ถ้าไม่ได้ติดตั้งแอปที่ผู้ใช้พยายามที่จะฝัง ระบบจะติดตั้งให้คุณโดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="ae502-112">This action means if the app the user tries to embed isn't installed, it's automatically installed for you.</span></span> <span data-ttu-id="ae502-113">ดังนั้น เนื้อหาคุณที่ต้องการจะถูกฝังทันที ซึ่งเป็นประสบการณ์การใช้งานที่ราบรื่นสำหรับผู้ใช้</span><span class="sxs-lookup"><span data-stu-id="ae502-113">So the content you want gets embedded immediately, resulting in a smooth experience for the user.</span></span>

## <a name="embed-for-power-bi-users-user-owns-data"></a><span data-ttu-id="ae502-114">การฝังสำหรับผู้ใช้ Power BI (ผู้ใช้เป็นเจ้าของข้อมูล)</span><span class="sxs-lookup"><span data-stu-id="ae502-114">Embed for Power BI users (User owns data)</span></span>

<span data-ttu-id="ae502-115">หากต้องการอนุญาตให้ติดตั้งแอปโดยอัตโนมัติสำหรับผู้ใช้ของคุณ คุณจะต้องให้สิทธิ์ 'สร้างเนื้อหา' แก่แอปพลิเคชันของคุณเมื่อ[ลงทะเบียนแอปพลิเคชัน](register-app.md#register-an-azure-ad-app) หรือเพิ่ม ถ้าคุณลงทะเบียนแอปไว้อยู่แล้ว</span><span class="sxs-lookup"><span data-stu-id="ae502-115">To allow auto install of apps for your users, you need to give your application the 'Content Create' permission when [registering your application](register-app.md#register-an-azure-ad-app), or add it if you already registered your app.</span></span>

![ลงทะเบียนแอปสร้างเนื้อหา](media/embed-auto-install-app/register-app-create-content.png)

<span data-ttu-id="ae502-117">ถัดไป คุณจะต้องระบุ ID แอปใน URL ที่ฝังไว้</span><span class="sxs-lookup"><span data-stu-id="ae502-117">Next, you need to provide the app ID in the embed URL.</span></span> <span data-ttu-id="ae502-118">ในการให้ข้อมูล ID แอป ผู้สร้างแอปจะต้องติดตั้งแอปก่อน จากนั้นใช้การเรียกใช้ [Power BI Rest API](/rest/api/power-bi/) รายการใดรายการหนึ่งที่รองรับ - [รับรายงาน](/rest/api/power-bi/reports/getreports)หรือ[รับแดชบอร์ด](/rest/api/power-bi/dashboards/getdashboards)</span><span class="sxs-lookup"><span data-stu-id="ae502-118">To provide the app ID, the app creator first needs to install the app then use one of the supported [Power BI Rest API](/rest/api/power-bi/) calls - [Get Reports](/rest/api/power-bi/reports/getreports) or [Get Dashboards](/rest/api/power-bi/dashboards/getdashboards).</span></span> <span data-ttu-id="ae502-119">จากนั้น ผู้สร้างแอปจะต้องใช้ Url ที่ฝังไว้จากการตอบสนอง REST API</span><span class="sxs-lookup"><span data-stu-id="ae502-119">Then the app creator needs to take the embed Url from the REST API response.</span></span> <span data-ttu-id="ae502-120">ID แอปจะปรากฏใน URL ถ้าเนื้อหามาจากแอป</span><span class="sxs-lookup"><span data-stu-id="ae502-120">The app ID appears in the URL if the content is from an app.</span></span>  <span data-ttu-id="ae502-121">หลังจากที่คุณฝัง URL แล้ว คุณจะสามารถใช้เพื่อฝังได้อย่างสม่ำเสมอ</span><span class="sxs-lookup"><span data-stu-id="ae502-121">After you have the embed URL, you can use it to embed regularly.</span></span>

## <a name="secure-embed"></a><span data-ttu-id="ae502-122">การฝังที่ปลอดภัย</span><span class="sxs-lookup"><span data-stu-id="ae502-122">Secure Embed</span></span>

<span data-ttu-id="ae502-123">หากต้องการใช้ติดตั้งแอปโดยอัตโนมัติ ผู้สร้างแอปจะต้องติดตั้งแอปก่อน จากนั้นไปที่แอปบน PowerBI.com นำทางไปยังรายงาน และรับลิงก์ตามปกติ</span><span class="sxs-lookup"><span data-stu-id="ae502-123">To use auto install of apps, the app creator first needs to install the app then go to the app on PowerBI.com, navigate to the report, and get the link in a usual fashion.</span></span> <span data-ttu-id="ae502-124">ผู้ใช้อื่น ๆ ทั้งหมดที่มีสิทธิ์การเข้าถึงแอปที่สามารถใช้ลิงก์จะสามารถฝังรายงานได้</span><span class="sxs-lookup"><span data-stu-id="ae502-124">All other users with access to the app that can use the link can embed the report.</span></span>

## <a name="considerations-and-limitations"></a><span data-ttu-id="ae502-125">ข้อควรพิจารณาและข้อจำกัด</span><span class="sxs-lookup"><span data-stu-id="ae502-125">Considerations and limitations</span></span>

* <span data-ttu-id="ae502-126">คุณสามารถฝังรายงานและแดชบอร์ดสำหรับสถานการณ์นี้ได้เท่านั้น</span><span class="sxs-lookup"><span data-stu-id="ae502-126">You can only embed reports and dashboards for this scenario.</span></span>

* <span data-ttu-id="ae502-127">ในขณะน้ี ระบบไม่รองรับคุณลักษณะนี้สำหรับแอปที่เป็นเจ้าของข้อมูล และสถานการณ์ที่ฝังใน SharePoint</span><span class="sxs-lookup"><span data-stu-id="ae502-127">This feature is currently not supported for app owns data and SharePoint embed scenarios.</span></span>