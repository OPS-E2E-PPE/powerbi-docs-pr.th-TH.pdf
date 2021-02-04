---
title: เชื่อมต่อกับ Microsoft Graph Security API ใน Power BI Desktop
description: เชื่อมต่อกับ Microsoft Graph Security API ใน Power BI Desktop ได้อย่างง่ายดาย
author: paulinbar
ms.author: painbar
ms.reviewer: ''
ms.custom: seojan19
ms.service: powerbi
ms.subservice: pbi-data-sources
ms.topic: conceptual
ms.date: 01/29/2019
LocalizationGroup: Connect to data
ms.openlocfilehash: b3aa9be7be6e2769367cd3337b78030d52bde0c7
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96411436"
---
# <a name="connect-to-the-microsoft-graph-security-api-in-power-bi-desktop"></a><span data-ttu-id="43ab0-103">เชื่อมต่อกับ Microsoft Graph Security API ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-103">Connect to the Microsoft Graph Security API in Power BI Desktop</span></span>

<span data-ttu-id="43ab0-104">ใช้ตัวเชื่อมต่อ Microsoft Graph Security ของ Power BI Desktop เพื่อเชื่อมต่อกับ [Microsoft Graph Security API](/graph/security-concept-overview)</span><span class="sxs-lookup"><span data-stu-id="43ab0-104">Use the Microsoft Graph Security connector of Power BI Desktop to connect to the [Microsoft Graph Security API](/graph/security-concept-overview).</span></span> <span data-ttu-id="43ab0-105">หลังจากนั้นคุณสามารถสร้างแดชบอร์ดและรายงานที่ช่วยให้คุณสามารถรับข้อมูลเชิงลึกให้กับการรักษาความปลอดภัยของคุณที่เกี่ยวข้อง [การแจ้งเตือน](/graph/api/resources/alert) และ [Secure Score](/graph/api/resources/securescores)</span><span class="sxs-lookup"><span data-stu-id="43ab0-105">You can then build dashboards and reports to gain insights into your security-related [alerts](/graph/api/resources/alert) and [secure scores](/graph/api/resources/securescores).</span></span>

<span data-ttu-id="43ab0-106">Microsoft Graph Security API เชื่อมต่อ [โซลูชันความปลอดภัยหลายรายการ](/graph/api/resources/security-api-overview#alerts) จาก Microsoft และคู่ค้าเพื่อให้การแจ้งเตือนสัมพันธ์กันง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="43ab0-106">The Microsoft Graph Security API connects [multiple security solutions](/graph/api/resources/security-api-overview#alerts) from Microsoft and its partners to make correlation of alerts easier.</span></span> <span data-ttu-id="43ab0-107">การผสานรวมนี้ให้การเข้าถึงข้อมูลบริบทที่หลากหลายและทำให้การทำงานอัตโนมัติเป็นเรื่องง่ายขึ้น</span><span class="sxs-lookup"><span data-stu-id="43ab0-107">This combination provides access to rich contextual information and simplifies automation.</span></span> <span data-ttu-id="43ab0-108">ซึ่งช่วยให้องค์กรต่างๆ สามารถรับข้อมูลเชิงลึกและดำเนินการกับผลิตภัณฑ์รักษาความปลอดภัยหลายรายการได้อย่างรวดเร็วในขณะที่ลดต้นทุนและความซับซ้อน</span><span class="sxs-lookup"><span data-stu-id="43ab0-108">It empowers organizations to quickly gain insights and act across multiple security products, while reducing cost and complexity.</span></span>

## <a name="prerequisites-to-use-the-microsoft-graph-security-connector"></a><span data-ttu-id="43ab0-109">ข้อกำหนดเบื้องต้นเพื่อใช้งานตัวเชื่อมต่อ Microsoft Graph Security</span><span class="sxs-lookup"><span data-stu-id="43ab0-109">Prerequisites to use the Microsoft Graph Security connector</span></span>

<span data-ttu-id="43ab0-110">หากต้องการใช้งานตัวเชื่อมต่อ Microsoft Graph Security คุณต้องได้รับความยินยอมจากผู้ดูแลระบบส่วนกลาง Azure Active Directory (Azure AD) *อย่างชัดเจน*</span><span class="sxs-lookup"><span data-stu-id="43ab0-110">To use the Microsoft Graph Security connector, you must *explicitly* get consent by the Azure Active Directory (Azure AD) global administrator.</span></span> <span data-ttu-id="43ab0-111">โปรดดู [ข้อกำหนดการยืนยันตัวตนของ Microsoft Graph](/graph/security-authorization)</span><span class="sxs-lookup"><span data-stu-id="43ab0-111">See [Microsoft Graph Security authentication requirements](/graph/security-authorization).</span></span>
<span data-ttu-id="43ab0-112">การยินยอมต้องการรหัสแอปพลิเคชันและชื่อของตัวเชื่อมต่อซึ่งอ้างถึงที่นี่และพร้อมใช้งานใน [พอร์ทัล Azure](https://portal.azure.com):</span><span class="sxs-lookup"><span data-stu-id="43ab0-112">Consent requires the connector's application ID and name, which is cited here and is available in the [Azure portal](https://portal.azure.com):</span></span>

| <span data-ttu-id="43ab0-113">คุณสมบัติ</span><span class="sxs-lookup"><span data-stu-id="43ab0-113">Property</span></span> | <span data-ttu-id="43ab0-114">Value</span><span class="sxs-lookup"><span data-stu-id="43ab0-114">Value</span></span> |
|----------|-------|
| <span data-ttu-id="43ab0-115">**ชื่อแอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="43ab0-115">**Application name**</span></span> | `MicrosoftGraphSecurityPowerBIConnector` |
| <span data-ttu-id="43ab0-116">**รหัสแอปพลิเคชัน**</span><span class="sxs-lookup"><span data-stu-id="43ab0-116">**Application ID**</span></span> | `cab163b7-247d-4cb9-be32-39b6056d4189` |
| <span data-ttu-id="43ab0-117">**เปลี่ยนเส้นทาง URI**</span><span class="sxs-lookup"><span data-stu-id="43ab0-117">**Redirect URI**</span></span> | `https://oauth.powerbi.com/views/oauthredirect.html` |
|||

<span data-ttu-id="43ab0-118">ในการให้ความยินยอมสำหรับตัวเชื่อมต่อ ผู้ดูแลระบบส่วนกลาง Azure AD ของคุณสามารถใช้วิธีใดวิธีหนึ่งต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43ab0-118">To grant consent for the connector, your Azure AD global administrator can use either of these methods:</span></span>

* [<span data-ttu-id="43ab0-119">ให้ความยินยอมสำหรับแอปพลิเคชัน Azure AD</span><span class="sxs-lookup"><span data-stu-id="43ab0-119">Grant consent for Azure AD applications</span></span>](/azure/active-directory/develop/v2-permissions-and-consent)

* <span data-ttu-id="43ab0-120">ตอบสนองต่อการร้องขอที่แอปลอจิกของคุณส่งในระหว่างการเรียกใช้ครั้งแรกผ่าน [ประสบการณ์ความยินยอมของแอปพลิเคชัน](/azure/active-directory/develop/application-consent-experience)</span><span class="sxs-lookup"><span data-stu-id="43ab0-120">Respond to a request that your logic app submits during its first run through the  [application-consent experience](/azure/active-directory/develop/application-consent-experience)</span></span>
   
<span data-ttu-id="43ab0-121">บัญชีผู้ใช้ที่ลงชื่อเข้าใช้ตัวเชื่อมต่อ Microsoft Graph Security ต้องได้รับการมอบหมายจากใน Azure AD **ถ้า** ตัวอ่านระบบความปลอดภัย หรือ *ผู้ดูแลระบบความปลอดภัย*</span><span class="sxs-lookup"><span data-stu-id="43ab0-121">The user account that signs in to the Microsoft Graph Security connector must be assigned the Azure AD Security Reader role, **if** the user is not a member of the *Security Administrator* role.</span></span> <span data-ttu-id="43ab0-122">โปรดดู [กำหนดบทบาท Azure AD ให้ผู้ใช้](/graph/security-authorization#assign-azure-ad-roles-to-users)</span><span class="sxs-lookup"><span data-stu-id="43ab0-122">See [Assign Azure AD roles to users](/graph/security-authorization#assign-azure-ad-roles-to-users).</span></span>

## <a name="using-the-microsoft-graph-security-connector"></a><span data-ttu-id="43ab0-123">ใช้ตัวเชื่อมต่อ Microsoft Graph Security</span><span class="sxs-lookup"><span data-stu-id="43ab0-123">Using the Microsoft Graph Security connector</span></span>

<span data-ttu-id="43ab0-124">ทำตามขั้นตอนเหล่านี้เพื่อใช้ตัวเชื่อมต่อ:</span><span class="sxs-lookup"><span data-stu-id="43ab0-124">Follow these steps to use the connector:</span></span>

1. <span data-ttu-id="43ab0-125">เลือก **รับข้อมูล** > **เพิ่มเติม** จากริบบอน **หน้าแรก** ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-125">Select **Get Data** > **More** from the **Home** ribbon in Power BI Desktop.</span></span>
2. <span data-ttu-id="43ab0-126">เลือก **บริการออนไลน์** จากรายการหมวดหมู่ทางด้านซ้ายของหน้าต่าง</span><span class="sxs-lookup"><span data-stu-id="43ab0-126">Select **Online Services** from the categories list on the left side of the window.</span></span>
3. <span data-ttu-id="43ab0-127">โปรดเลือก **การรักษาความปลอดภัยของ Microsoft Graph**</span><span class="sxs-lookup"><span data-stu-id="43ab0-127">Select **Microsoft Graph Security (Beta)**.</span></span>

    ![กล่องโต้ตอบรับข้อมูล](media/desktop-connect-graph-security/GetData.PNG)
    
4. <span data-ttu-id="43ab0-129">ในหน้าต่าง **Microsoft Graph Security** ให้เลือกเวอร์ชันของ Microsoft Graph API เพื่อทำการคิวรี : **v1.0** หรือ **beta**</span><span class="sxs-lookup"><span data-stu-id="43ab0-129">In the **Microsoft Graph Security** window, select the Microsoft Graph API version to query: **v1.0** or **beta**.</span></span>

    ![กล่องโต้ตอบเลือกเวอร์ชัน](media/desktop-connect-graph-security/selectVersion.PNG)
    
5. <span data-ttu-id="43ab0-131">ลงชื่อเข้าใช้บัญชี Azure Active Directory เมื่อคุณได้รับพร้อมต์แจ้ง</span><span class="sxs-lookup"><span data-stu-id="43ab0-131">Sign in to your Azure Active Directory account when you're prompted.</span></span> <span data-ttu-id="43ab0-132">บัญชีนี้ต้องมีบทบาท *ตัวอ่านระบบความปลอดภัย* หรือ *ผู้ดูแลระบบความปลอดภัย* ดังที่กล่าวไว้ในส่วนก่อนหน้า</span><span class="sxs-lookup"><span data-stu-id="43ab0-132">This account needs to have the *Security Reader* or *Security Administrator* role, as mentioned in the previous section.</span></span>

    ![ลงชื่อเข้าใช้](media/desktop-connect-graph-security/SignIn.PNG) 
    
6. <span data-ttu-id="43ab0-134">ถ้าคุณเป็นผู้ดูแลระบบ *และ* คุณยังไม่ได้ให้ความยินยอมกับตัวเชื่อมต่อ Microsoft Graph Security Power BI (แอปพลิเคชัน) คุณจะเห็นกล่องโต้ตอบต่อไปนี้</span><span class="sxs-lookup"><span data-stu-id="43ab0-134">If you're the admin *and* you don't yet have consent to the Microsoft Graph Security Power BI connector (application), you'll see the following dialog box.</span></span> <span data-ttu-id="43ab0-135">โปรดเลือก **ให้ความยินยอมในนามขององค์กรของคุณ**</span><span class="sxs-lookup"><span data-stu-id="43ab0-135">Select **Consent on behalf of your organization**.</span></span>

    ![กล่องโต้ตอบจัดการความยินยอม](media/desktop-connect-graph-security/AdminConsent.PNG)
    
7. <span data-ttu-id="43ab0-137">เมื่อคุณลงชื่อเข้าใช้แล้ว คุณจะเห็นกล่องโต้ตอบต่อไปนี้ที่ระบุว่าคุณได้รับการตรวจสอบสิทธิ์แล้ว</span><span class="sxs-lookup"><span data-stu-id="43ab0-137">When you're signed in, you'll see the following dialog box that indicates that you've been authenticated.</span></span> <span data-ttu-id="43ab0-138">เลือก **เชื่อมต่อ**</span><span class="sxs-lookup"><span data-stu-id="43ab0-138">Select **Connect**.</span></span>

    ![กล่องโต้ตอบ "คุณมีการลงชื่อเข้าใช้แล้วในขณะนี้"](media/desktop-connect-graph-security/SignedIn.PNG)
    
8. <span data-ttu-id="43ab0-140">หลังจากคุณเชื่อมต่อแล้ว หน้าต่าง **ตัวนำทาง** จะแสดงการแจ้งเตือน คะแนนความปลอดภัย และเอนทิตีอื่น ๆ ที่มีอยู่ใน [Microsoft Graph Security API](/graph/security-concept-overview) สำหรับเวอร์ชันที่คุณเลือกในขั้นตอนที่ 4</span><span class="sxs-lookup"><span data-stu-id="43ab0-140">After you connect, the **Navigator** window displays the alerts, secure scores, and other entities that are available in the [Microsoft Graph Security API](/graph/security-concept-overview) for the version that you selected in step 4.</span></span> <span data-ttu-id="43ab0-141">เลือกเอนทิตี้ตั้งแต่หนึ่งรายการขึ่นไปเพื่อนำเข้า และใช้ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-141">Select one or more entities to import and use in Power BI Desktop.</span></span> <span data-ttu-id="43ab0-142">จาดนั้น เลือก **โหลด** เพื่อดูผลลัพธ์ที่แสดงหลังจากขั้นตอนที่ 9</span><span class="sxs-lookup"><span data-stu-id="43ab0-142">Then, select **Load** to get the result view that's shown after step 9.</span></span>

    ![กล่องโต้ตอบการนำทาง](media/desktop-connect-graph-security/NavTable.PNG)
    
9. <span data-ttu-id="43ab0-144">ถ้าคุณต้องการใช้งานคิวรีขั้นสูงกับ Microsoft Graph Security API ให้เลือก **ระบุ URL ของ Microsoft Graph Security แบบกำหนดเองเพื่อกรองผลลัพธ์**</span><span class="sxs-lookup"><span data-stu-id="43ab0-144">If you want to use an advanced query with the Microsoft Graph Security API, select **Specify custom Microsoft Graph Security URL to filter results**.</span></span> <span data-ttu-id="43ab0-145">ใช้ฟังก์ชันนี้เพื่อส่งคิวรี [OData.Feed](./desktop-connect-odata.md) ไปยัง Microsoft Graph Security API ด้วยสิทธิ์ที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="43ab0-145">Use this function to issue an [OData.Feed](./desktop-connect-odata.md) query to the Microsoft Graph Security API with the required permissions.</span></span>

   <span data-ttu-id="43ab0-146">ตัวอย่างต่อไปนี้ใช้ `https://graph.microsoft.com/v1.0/security/alerts?$filter=Severity eq 'High'` *serviceUri*</span><span class="sxs-lookup"><span data-stu-id="43ab0-146">The following example uses the `https://graph.microsoft.com/v1.0/security/alerts?$filter=Severity eq 'High'` *serviceUri*.</span></span> <span data-ttu-id="43ab0-147">เมื่อต้องการดูวิธีสร้างคิวรีเพื่อกรอง เรียงลำดับ หรือดึงผลลัพธ์ล่าสุดให้ดูที่ [ตัวเลือกคิวรีระบบ OData](/graph/query-parameters)</span><span class="sxs-lookup"><span data-stu-id="43ab0-147">To see how to build queries to filter, order, or retrieve the most-recent results, refer to [OData system query options](/graph/query-parameters).</span></span>

   ![ตัวอย่าง OdataFeed](media/desktop-connect-graph-security/ODataFeed.PNG)
    
   <span data-ttu-id="43ab0-149">เมื่อคุณเลือกฟังก์ชัน **Invoke**, **OData.Feed** ทำให้เรียกใช้ API ซึ่งเปิดตัวแก้ไขคิวรี</span><span class="sxs-lookup"><span data-stu-id="43ab0-149">When you select **Invoke**, the **OData.Feed** function makes a call to the API, which opens Query Editor.</span></span> <span data-ttu-id="43ab0-150">คุณกรองและปรับแต่งชุดข้อมูลที่คุณต้องการใช้</span><span class="sxs-lookup"><span data-stu-id="43ab0-150">You filter and refine the set of data that you want to use.</span></span> <span data-ttu-id="43ab0-151">จากนั้นคุณโหลดข้อมูลนั้นลงใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-151">Then, you load that data into Power BI Desktop.</span></span>

<span data-ttu-id="43ab0-152">นี่คือหน้าต่างผลลัพธ์สำหรับเอนทิตี Microsoft Graph Security ที่เราคิวรีไป:</span><span class="sxs-lookup"><span data-stu-id="43ab0-152">Here's the results window for the Microsoft Graph Security entities that we queried for:</span></span>

   ![ตัวอย่างหน้าต่างผลลัพธ์](media/desktop-connect-graph-security/Result.PNG)
    

<span data-ttu-id="43ab0-154">ตอนนี้คุณพร้อมที่จะใช้ข้อมูลที่นำเข้าจากตัวเชื่อมต่อ Microsoft Graph Security ใน Power BI Desktop แล้ว</span><span class="sxs-lookup"><span data-stu-id="43ab0-154">Now you’re ready to use the imported data from the Microsoft Graph Security connector in Power BI Desktop.</span></span> <span data-ttu-id="43ab0-155">คุณสามารถสร้างกราฟิกหรือรายงานได้</span><span class="sxs-lookup"><span data-stu-id="43ab0-155">You can create graphics or reports.</span></span> <span data-ttu-id="43ab0-156">หรือคุณสามารถโต้ตอบกับข้อมูลอื่นที่คุณนำเข้าจากเวิร์กบุ๊ก Excel ฐานข้อมูล หรือแหล่งข้อมูลอื่นได้</span><span class="sxs-lookup"><span data-stu-id="43ab0-156">Or, you can interact with other data that you import from Excel workbooks, databases, or other data sources.</span></span>

## <a name="next-steps"></a><span data-ttu-id="43ab0-157">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="43ab0-157">Next steps</span></span>
* <span data-ttu-id="43ab0-158">ดูตัวอย่างและเทมเพลต Power BI ที่ใช้ตัวเชื่อมต่อนี้ที่ [ตัวอย่าง Microsoft Graph Security GitHub Power BI](https://aka.ms/graphsecuritypowerbiconnectorsamples)</span><span class="sxs-lookup"><span data-stu-id="43ab0-158">Check out Power BI samples and templates that use this connector at [Microsoft Graph Security GitHub Power BI samples](https://aka.ms/graphsecuritypowerbiconnectorsamples).</span></span>

* <span data-ttu-id="43ab0-159">สำหรับสถานการณ์ผู้ใช้และข้อมูลเพิ่มเติม โปรดดู [โพสต์บล็อกตัวเชื่อมต่อของ Microsoft Graph Security Power BI นี้](https://aka.ms/graphsecuritypowerbiconnectorblogpost)</span><span class="sxs-lookup"><span data-stu-id="43ab0-159">For user scenarios and additional information, see [this Microsoft Graph Security Power BI connector blog post](https://aka.ms/graphsecuritypowerbiconnectorblogpost).</span></span>

* <span data-ttu-id="43ab0-160">คุณสามารถเชื่อมต่อกับข้อมูลทุกประเภทได้โดยใช้ Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-160">You can connect to all sorts of data by using Power BI Desktop.</span></span> <span data-ttu-id="43ab0-161">สำหรับข้อมูลเพิ่มเติม โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="43ab0-161">For more information, check out the following resources:</span></span>

    * [<span data-ttu-id="43ab0-162">Power BI Desktop คืออะไร</span><span class="sxs-lookup"><span data-stu-id="43ab0-162">What is Power BI Desktop?</span></span>](../fundamentals/desktop-what-is-desktop.md)
    * [<span data-ttu-id="43ab0-163">แหล่งข้อมูลใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-163">Data sources in Power BI Desktop</span></span>](desktop-data-sources.md)
    * [<span data-ttu-id="43ab0-164">จัดรูปร่างและรวมข้อมูลด้วย Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-164">Shape and combine data with Power BI Desktop</span></span>](desktop-shape-and-combine-data.md)
    * [<span data-ttu-id="43ab0-165">เชื่อมต่อกับเวิร์กบุ๊ก Excel ใน Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="43ab0-165">Connect to Excel workbooks in Power BI Desktop</span></span>](desktop-connect-excel.md)
    * [<span data-ttu-id="43ab0-166">ป้อนข้อมูลลงใน Power BI Desktop โดยตรง</span><span class="sxs-lookup"><span data-stu-id="43ab0-166">Enter data directly into Power BI Desktop</span></span>](desktop-enter-data-directly-into-desktop.md)