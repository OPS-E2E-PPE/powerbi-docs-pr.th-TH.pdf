---
title: ฝังเนื้อหา Power BI ในแอปพลิเคชันการวิเคราะห์แบบฝังตัวไว้พร้อมด้วยโครงร่างสำคัญของบริการและความลับของแอปพลิเคชันที่เปิดใช้งานข้อมูลเชิงลึก BI ที่ฝังตัวได้ดีขึ้น
description: เรียนรู้วิธีการรับรองความถูกต้องสำหรับการวิเคราะห์แบบฝังตัวโดยใช้บริการแอปพลิเคชัน Azure Active Directory หลักและข้อมูลลับของแอปพลิเคชัน เปิดใช้งานข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.custom: ''
ms.date: 11/23/2020
ms.openlocfilehash: 35bdaa8af06187767975126daa1f2445908fed9f
ms.sourcegitcommit: eeaf607e7c1d89ef7312421731e1729ddce5a5cc
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/05/2021
ms.locfileid: "97886798"
---
# <a name="embed-power-bi-content-with-service-principal-and-an-application-secret"></a>การฝังเนื้อหา Power BI ด้วยบริการหลักและความลับของแอปพลิเคชัน

บริการหลักคือวิธีการรับรองความถูกต้องที่สามารถใช้เพื่ออนุญาตให้แอปพลิเคชัน  Azure AD เข้าถึงเนื้อหาบริการของ Power BI และ API

เมื่อคุณสร้างแอป Azure Active Directory (Azure AD)  [วัตถุบริการหลัก](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object) จะถูกสร้างขึ้น วัตถุบริการหลัก ซึ่งเป็นที่รู้จักกันว่า *บริการหลัก* จะช่วยให้ Azure AD รับรองความถูกต้องของแอปของคุณ เมื่อรับรองความถูกต้องแล้ว แอปจะสามารถเข้าถึงแหล่งข้อมูลผู้เช่า Azure AD

ในการรับรองความถูกต้อง บริการหลักจะใช้ *รหัส แอปพลิเคชัน* ของแอป Azure AD และหนึ่งในรายการต่อไปนี้:

* ใบรับรอง
* ข้อมูลลับของแอปพลิเคชัน

บทความนี้อธิบายการรับรองความถูกต้องของบริการหลักโดยใช้ *รหัสแอปพลิเคชัน* และ *ความลับของแอปพลิเคชัน*

>[!NOTE]
>Azure AD ขอแนะนำให้คุณรักษาความปลอดภัยบริการหลังบ้านของคุณโดยใช้ใบรับรอง แทนที่จะเป็นคีย์ลับ
>* [เรียนรู้เพิ่มเติมเกี่ยวกับการรับโทเค็นการเข้าถึงจาก Azure AD โดยใช้คีย์ลับหรือใบรับรอง](/azure/architecture/multitenant-identity/client-assertion)
>* เมื่อต้องการรักษาความปลอดภัยโซลูชันของคุณโดยใช้ใบรับรอง ให้ทำตามคำแนะนำในบทความนี้จากนั้นทำตามขั้นตอนที่อธิบายไว้ใน[ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการและใบรับรอง](embed-service-principal-certificate.md)

## <a name="method"></a>วิธีการ

เมื่อต้องการใช้องค์ประกอบหลักและการวิเคราะห์แบบฝัง ID แอปพลิเคชัน ให้ทำตามขั้นตอนเหล่านี้:

1. สร้าง [แอป Azure AD](/azure/active-directory/manage-apps/what-is-application-management)

    1. สร้างความลับของแอป Azure AD
    
    2. รับ *รหัสแอปพลิเคชัน* และ *ความลับของแอปพลิเคชัน* ของแอป

    >[!NOTE]
    >ขั้นตอนเหล่านี้จะอธิบายไว้ใน **ขั้นตอนที่ 1** สำหรับข้อมูลเพิ่มเติมเกี่ยวกับการสร้างแอป Azure AD โปรดดูบทความ [สร้างแอป Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal)

2. สร้างกลุ่มความปลอดภัย Azure AD

3. เปิดใช้งานการตั้งค่าการจัดการบริการของ Power BI

4. เพิ่มบริการหลักไปยังพื้นที่ทำงานของคุณ

5. ฝังเนื้อหาของคุณ

> [!IMPORTANT]
> เมื่อคุณเปิดใช้งานบริการหลักที่จะใช้กับ Power BI สิทธิ์ AD ของแอปพลิเคชันไม่มีผลบังคับใช้อีกต่อไป มีจัดการสิทธิ์ของแอปพลิเคชันแล้วผ่านทางพอร์ทัลผู้ดูแลระบบ Power BI

## <a name="step-1---create-an-azure-ad-app"></a>ขั้นตอนที่ 1 - สร้าง แอป Azure AD

สร้างแอป Azure AD โดยใช้วิธีใดวิธีหนึ่งต่อไปนี้:

* [สร้างแอปในพอร์ทัล Microsoft Azure](embed-service-principal.md#creating-an-azure-ad-app-in-the-microsoft-azure-portal)

* [สร้างแอปโดยใช้ PowerShell](embed-service-principal.md#creating-an-azure-ad-app-using-powershell)

### <a name="creating-an-azure-ad-app-in-the-microsoft-azure-portal"></a>การสร้างแอป Azure AD ในพอร์ทัล Microsoft Azure

1. ลงชื่อเข้าใช้ใน [Microsoft Azure](https://ms.portal.azure.com/#allservices)

2. ค้นหา **การลงทะเบียนแอป** และคลิกลิงก์ **การลงทะเบียนแอป**

    ![ลงทะเบียนแอป azure](media/embed-service-principal/azure-app-registration.png)

3. คลิก **การลงทะเบียนใหม่**

    ![การลงทะเบียนใหม่](media/embed-service-principal/new-registration.png)

4. ระบุข้อมูลที่จำเป็น:
    * **ชื่อ** - กรอกชื่อสำหรับแอปพลิเคชันของคุณ
    * **ชนิดบัญชีที่ได้รับการสนับสนุน** - เลือกประเภทบัญชีที่ได้รับการสนับสนุน
    * (ไม่บังคับ) **เปลี่ยนเส้นทาง URI** - กรอก URI ถ้าจำเป็น

5. คลิก **ลงทะเบียน**

6. หลังจากลงทะเบียนแล้ว *รหัสแอปพลิเคชัน* จะพร้อมใช้งานจากแท็บ **ภาพรวม** คัดลอกและบันทึก *รหัสแอปพลิเคชัน* สำหรับใช้งานในภายหลัง

    ![สกรีนช็อตแสดงตำแหน่งที่จะขอรับ ID แอปพลิเคชันในแท็บภาพรวม](media/embed-service-principal/application-id.png)

7. คลิกแท็บ **ใบรับรองและความลับ**

     ![สกรีนช็อตที่แสดงใบรับรองและบานหน้าต่างความลับสำหรับแอปในพอร์ทัล Azure](media/embed-service-principal/certificates-and-secrets.png)

8. คลิก **ความลับของไคลเอ็นต์ใหม่**

    ![สกรีนช็อตที่แสดงปุ่มความลับของไคลเอ็นต์ใหม่ในบานหน้าต่างใบรับรองและความลับ](media/embed-service-principal/new-client-secret.png)

9. ในหน้าต่าง *เพิ่มความลับของไคลเอ็นต์* กรอกคำอธิบาย ระบุเวลาที่คุณต้องการให้ความลับของไคลเอ็นต์หมดอายุ จากนั้นคลิก **เพิ่ม**

10. คัดลอกและบันทึกค่า *ความลับของไคลเอ็นต์*

    ![สกรีนช็อตที่แสดงค่าลับในบานหน้าต่างใบรับรองและความลับ](media/embed-service-principal/client-secret-value.png)

    >[!NOTE]
    >หลังจากที่คุณออกจากหน้าต่างนี้ ค่าความลับของไคลเอ็นต์จะถูกซ่อนอยู่และคุณจะไม่สามารถดูหรือคัดลอกอีกครั้งได้

### <a name="creating-an-azure-ad-app-using-powershell"></a>การสร้างแอป Azure AD โดยใช้ PowerShell

ส่วนนี้จะประกอบด้วยสคริปต์ตัวอย่างในการสร้างแอป Azure AD ใหม่โดยใช้ [PowerShell](/powershell/azure/create-azure-service-principal-azureps)

```powershell
# The app ID - $app.appid
# The service principal object ID - $sp.objectId
# The app key - $key.value

# Sign in as a user that's allowed to create an app
Connect-AzureAD

# Create a new Azure AD web application
$app = New-AzureADApplication -DisplayName "testApp1" -Homepage "https://localhost:44322" -ReplyUrls "https://localhost:44322"

# Creates a service principal
$sp = New-AzureADServicePrincipal -AppId $app.AppId

# Get the service principal key
$key = New-AzureADServicePrincipalPasswordCredential -ObjectId $sp.ObjectId
```

## <a name="step-2---create-an-azure-ad-security-group"></a>ขั้นตอนที่ 2 - สร้างกลุ่มความปลอดภัย Azure AD

บริการหลักของคุณไม่มีสิทธิ์ในการเข้าถึงเนื้อหา Power BI และ API ของคุณ ในการให้สิทธิ์การเข้าถึงบริการหลัก ให้สร้างกลุ่มความปลอดภัยใน Azure AD และเพิ่มบริการหลักที่คุณสร้างไว้ในกลุ่มความปลอดภัยนั้น

มีสองวิธีในการสร้างกลุ่มความปลอดภัยใน Azure AD:
* [ด้วยตนเอง (ใน Azure)](embed-service-principal.md#create-a-security-group-manually)
* [การใช้ PowerShell](embed-service-principal.md#create-a-security-group-using-powershell)

### <a name="create-a-security-group-manually"></a>สร้างกลุ่มความปลอดภัยด้วยตนเอง

หากต้องการสร้างกลุ่มความปลอดภัยใน Azure ด้วยตนเอง ให้ทำตามคำแนะนำในบทความ [สร้างกลุ่มพื้นฐานและเพิ่มสมาชิกโดยใช้ Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) 

### <a name="create-a-security-group-using-powershell"></a>สร้างกลุ่มความปลอดภัยโดยใช้ PowerShell

ในด้านล่างจะแสดงสคริปต์ตัวอย่างในการสร้างกลุ่มความปลอดภัยใหม่ และการเพิ่มแอปไปยังกลุ่มความปลอดภัยนั้น

>[!NOTE]
>หากคุณต้องการเปิดใช้สิทธิ์การเข้าถึงบริการหลักสำหรับทั้งองค์กร โปรดข้ามขั้นตอนนี้

```powershell
# Required to sign in as admin
Connect-AzureAD

# Create an Azure AD security group
$group = New-AzureADGroup -DisplayName <Group display name> -SecurityEnabled $true -MailEnabled $false -MailNickName notSet

# Add the service principal to the group
Add-AzureADGroupMember -ObjectId $($group.ObjectId) -RefObjectId $($sp.ObjectId)
```

## <a name="step-3---enable-the-power-bi-service-admin-settings"></a>ขั้นตอนที่ 3 - เปิดใช้งานการตั้งค่าการจัดการบริการของ Power BI

เพื่อให้แอป Azure AD สามารถเข้าถึงเนื้อหา Power BI และ API ได้ ผู้ดูแลระบบ Power BI จำเป็นต้องเปิดใช้งานการเข้าถึงบริการหลักในพอร์ทัลผู้ดูแลระบบของ Power BI

เพิ่มกลุ่มความปลอดภัยที่คุณสร้างใน Azure AD สำหรับส่วนกลุ่มความปลอดภัยเฉพาะใน **การตั้งค่านักพัฒนา**

>[!IMPORTANT]
>บริการหลักมีสิทธิ์เข้าถึงการตั้งค่าผู้เช่าใดๆ ที่เปิดใช้งานอยู่ โดยจะรวมถึงกลุ่มความปลอดภัยเฉพาะหรือทั้งองค์กร ขึ้นอยู่กับการตั้งค่าผู้ดูแลระบบของคุณ
>
>เพื่อจำกัดการเข้าถึงบริการหลักของการตั้งค่าผู้เช่าเฉพาะ จะมีการอนุญาตให้เข้าถึงเพียงกลุ่มความปลอดภัยเฉพาะเท่านั้น อีกวิธีหนึ่งคือคุณสามารถสร้างกลุ่มความปลอดภัยเฉพาะสำหรับบริการหลัก และแยกออกไปจากการตั้งค่าผู้เช่าที่ต้องการได้

>[!div class="mx-imgBorder"]
>:::image type="content" source="media/embed-service-principal/admin-portal.png" alt-text="สกรีนช็อตแสดงการตั้งค่าของนักพัฒนาในตัวเลือกผู้ดูแลระบบในบริการ Power BI":::

## <a name="step-4---add-the-service-principal-to-your-workspace"></a>ขั้นตอนที่ 4 - เพิ่มบริการหลักไปยังพื้นที่ทำงานของคุณ

เมื่อต้องการเปิดใช้งานอาร์ติแฟกต์การเข้าถึงของแอป Azure AD ของคุณ เช่น รายงาน แดชบอร์ด และชุดข้อมูลในบริการ Power BI ให้เพิ่มเอนทิตีองค์ประกอบหลักของบริการ หรือกลุ่มความปลอดภัยที่มีองค์ประกอบหลักของบริการของคุณในฐานะสมาชิกหรือผู้ดูแลระบบในพื้นที่ทำงานของคุณ

>[!NOTE]
>ส่วนนี้แสดงคำแนะนำของ UI คุณยังสามารถเพิ่มองค์ประกอบหลักของบริการหรือกลุ่มความปลอดภัยให้กับพื้นที่ทำงานโดยใช้[กลุ่ม - เพิ่ม API ของผู้ใช้กลุ่ม](/rest/api/power-bi/groups/addgroupuser)ได้อีกด้วย

1. เลื่อนไปยังพื้นที่ทำงานที่คุณต้องการเปิดใช้งานการเข้าถึง และจากเมนู **เพิ่มเติม** เลือก **การเข้าถึงพื้นที่ทำงาน**

    :::image type="content" source="media/embed-service-principal/workspace-access.png" alt-text="สกรีนช็อตแสดงปุ่มการเข้าถึงพื้นที่ทำงานในเมนูเพิ่มเติมของพื้นที่ทำงาน Power BI":::

2. ในบานหน้าต่าง **การเข้าถึง** กล่องข้อความ ให้เพิ่มรายการใดรายการหนึ่งต่อไปนี้:

    * **องค์ประกอบหลักของบริการ** ของคุณ ชื่อองค์ประกอบหลักของบริการของคุณคือ *ชื่อที่แสดง* ของแอป Azure AD ของคุณตามที่ปรากฏในแท็บภาพรวมของแอป Azure AD ของคุณ

    * **กลุ่มความปลอดภัย** ที่รวมองค์ประกอบหลักของบริการของคุณ

3. เลือก **สมาชิก** หรือ **ผู้ดูแล** จากเมนูดรอปดาวน์

4. เลือก **เพิ่ม**

### <a name="add-a-service-principal-as-a-workspace-member-using-powershell"></a>เพิ่มหลักบริการเป็นสมาชิกพื้นที่ทำงานโดยใช้ PowerShell

ส่วนนี้ประกอบด้วยสคริปต์ตัวอย่างเพื่อเพิ่มหลักบริการเป็นสมาชิกพื้นที่ทำงานโดยใช้ [PowerShell](/powershell/azure/create-azure-service-principal-azureps)

```powershell
Login-PowerBI

# Service Principal Object ID for the created Service Principal
$SPObjectId = 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX'

$pbiWorkspace = Get-PowerBIWorkspace -Name "YourWorkspaceName"

Add-PowerBIWorkspaceUser -Id $pbiWorkspace.Id -AccessRight Member -PrincipalType App -Identifier $SPObjectId 

```

### <a name="add-a-security-group-as-a-workspace-member-using-powershell"></a>เพิ่มกลุ่มความปลอดภัยเป็นสมาชิกพื้นที่ทำงานโดยใช้ PowerShell

ส่วนนี้ประกอบด้วยสคริปต์ตัวอย่างเพื่อเพิ่มกลุ่มความปลอดภัยเป็นสมาชิกพื้นที่ทำงานโดยใช้ [PowerShell](/powershell/azure/create-azure-service-principal-azureps)

```powershell
Login-PowerBI

# Security Group Object ID for the created Security Group
$SGObjectId = 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX'

$pbiWorkspace = Get-PowerBIWorkspace -Name "YourWorkspaceName"

Add-PowerBIWorkspaceUser -Id $pbiWorkspace.Id -AccessRight Member -PrincipalType Group -Identifier $SGObjectId 

```

## <a name="step-5---embed-your-content"></a>ขั้นตอนที่ 5 - ฝังเนื้อหาของคุณ

คุณสามารถ[ฝังเนื้อหาของคุณภายในแอปพลิเคชันตัวอย่าง](embed-sample-for-customers.md) หรือภายในแอปพลิเคชันของคุณเอง

หลังจากที่มีการฝังเนื้อหาของคุณแล้ว คุณก็พร้อมที่จะ [ย้ายไปยังการผลิต](move-to-production.md)

>[!NOTE]
>เมื่อต้องการรักษาความปลอดภัยเนื้อหาของคุณโดยใช้ใบรับรอง ให้ทำตามขั้นตอนที่อธิบายไว้ใน[ฝังเนื้อหา Power BI ด้วยองค์ประกอบหลักของบริการและใบรับรอง](embed-service-principal-certificate.md)

## <a name="considerations-and-limitations"></a>ข้อควรพิจารณาและข้อจำกัด

* บริการหลักจะทำงานร่วมกับ[พื้นที่ทำงานใหม่](../../collaborate-share/service-create-the-new-workspaces.md)เท่านั้น
* **ความจุเฉพาะของฉัน** ไม่ได้รับการสนับสนุนเมื่อใช้บริการหลัก
* ต้องใช้ความจุเมื่อย้ายไปยังการผลิต
* คุณไม่สามารถลงชื่อเข้าใช้พอร์ทัล Power BI ด้วยบริการหลัก
* คุณจำเป็นต้องมีสิทธิ์ของผู้ดูแลระบบ Power BI เพื่อเปิดใช้งานบริการหลักในการตั้งค่านักพัฒนาภายในพอร์ทัลผู้ดูแลระบบของ Power BI
* แอปพลิเคชัน [แบบฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md) ไม่สามารถใช้บริการหลักได้
* [Dataflows](../../transform-model/dataflows/dataflows-introduction-self-service.md) การจัดการไม่ได้รับการสนับสนุน
* ปัจจุบัน โครงร่างสำคัญของบริการไม่สนับสนุนผู้ดูแลระบบ APIs
* เมื่อใช้โครงร่างสำคัญของบริการด้วยแหล่งข้อมูล [Azure Analysis Services](/azure/analysis-services/analysis-services-overview) โครงร่างสำคัญของบริการจะต้องมีสิทธิ์อินสแตนซ์ Azure Analysis Services การใช้กลุ่มความปลอดภัยที่ประกอบด้วยโครงร่างสำคัญของบริการสำหรับวัตถุประสงค์นี้ไม่ได้ผล

## <a name="next-steps"></a>ขั้นตอนถัดไป

>[!div class="nextstepaction"]
>[ลงทะเบียนแอป](register-app.md)

> [!div class="nextstepaction"]
>[Power BI Embedded สำหรับลูกค้าของคุณ](embed-sample-for-customers.md)

>[!div class="nextstepaction"]
>[ฝังโดยใช้องค์ประกอบหลักของบริการและใบรับรอง](embed-service-principal-certificate.md)

>[!div class="nextstepaction"]
>[แอปพลิเคชันและออบเจ็กต์บริการหลักใน Azure Active Directory](/azure/active-directory/develop/app-objects-and-service-principals)

>[!div class="nextstepaction"]
>[ความปลอดภัยระดับแถวโดยใช้เกตเวย์ข้อมูลภายในองค์กรที่มีโครงร่างสำคัญของบริการ](embedded-row-level-security.md#on-premises-data-gateway-with-service-principal)