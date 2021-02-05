---
title: ลงทะเบียนแอปเพื่อฝังเนื้อหา Power BI ในแอปพลิเคชันการวิเคราะห์แบบฝังตัวของ Power BI สำหรับข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้น
description: เรียนรู้วิธีการลงทะเบียนแอปพลิเคชันภายใน Azure Active Directory สำหรับการใช้งานด้วยการฝังเนื้อหา Power BI เพื่อให้ได้ข้อมูลเชิงลึก BI แบบฝังที่ดีขึ้นโดยใช้การวิเคราะห์แบบฝังตัวของ Power BI
author: KesemSharabi
ms.author: kesharab
ms.reviewer: nishalit
ms.service: powerbi
ms.subservice: powerbi-developer
ms.topic: how-to
ms.date: 04/02/2019
ms.openlocfilehash: 624e0a2838a08d1cf68ae58223fe979a56312b48
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98565926"
---
# <a name="register-an-azure-ad-application-to-use-with-power-bi"></a>ลงทะเบียนแอปพลิเคชัน Azure AD เพื่อใช้กับ Power BI

เมื่อต้องการใช้การวิเคราะห์แบบฝังตัวของ Power BI คุณต้องลงทะเบียนแอปพลิเคชัน Azure Active Directory (Azure AD) ใน Azure แอป Azure AD สร้างสิทธิ์สำหรับทรัพยากร Power BI REST และอนุญาตให้เข้าถึง [Power BI REST APIs](/rest/api/power-bi/)

## <a name="determine-your-embedding-solution"></a>กำหนดโซลูชันการฝังตัวของคุณ

ก่อนลงทะเบียนแอปของคุณ ให้ตัดสินใจว่าโซลูชันใดต่อไปนี้เหมาะสมที่สุดสำหรับคุณ:

* ฝังตัวสำหรับลูกค้าของคุณ
* ฝังตัวสำหรับองค์กรของคุณ

### <a name="embed-for-your-customers"></a>ฝังตัวสำหรับลูกค้าของคุณ

ใช้โซลูชัน [ฝังตัวสำหรับลูกค้าของคุณ](embed-sample-for-customers.md) หรือที่เรียกว่า *แอปเป็นเจ้าของข้อมูล* หากคุณกำลังวางแผนที่จะสร้างแอปพลิเคชันที่ออกแบบมาสำหรับลูกค้าของคุณ ผู้ใช้จะไม่จำเป็นต้องลงชื่อเข้าใช้ Power BI หรือไม่จำเป็นต้องมีสิทธิการใช้งาน Power BI เพื่อใช้แอปพลิเคชันของคุณ แอปพลิเคชันของคุณจะใช้วิธีใดวิธีหนึ่งต่อไปนี้เพื่อรับรองความถูกต้องกับ Power BI:

* บัญชี **ผู้ใช้หลัก** (สิทธิการใช้งาน Power BI Pro ใช้สำหรับการลงชื่อเข้าใช้ Power BI)

* [โครงร่างสำคัญของบริการ](embed-service-principal.md)

โซลูชันฝังตัวสำหรับลูกค้าของคุณมักจะถูกใช้โดยผู้จำหน่ายซอฟต์แวร์อิสระ (ISVs) และนักพัฒนาที่กำลังสร้างแอปพลิเคชันสำหรับบุคคลที่สาม

### <a name="embed-for-your-organization"></a>ฝังตัวสำหรับองค์กรของคุณ

ใช้โซลูชัน [ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md) หรือที่เรียกว่า *ผู้ใช้เป็นเจ้าของข้อมูล* ถ้าคุณกำลังวางแผนที่จะสร้างแอปพลิเคชันที่ต้องการให้ผู้ใช้ใช้ข้อมูลประจำตัวของพวกเขาเพื่อรับรองความถูกต้องกับ Power BI

โซลูชันฝังตัวสำหรับองค์กรของคุณมักจะใช้โดยวิสาหกิจและองค์กรขนาดใหญ่ และมีไว้สำหรับผู้ใช้ภายใน

## <a name="register-an-azure-ad-app"></a>ลงทะเบียนแอป Azure AD

วิธีที่ง่ายที่สุดในการลงทะเบียนแอป Azure AD คือการใช้[เครื่องมือตั้งค่าการฝัง Power BI](https://app.powerbi.com/embedsetup) เครื่องมือนี้มีกระบวนการลงทะเบียนที่รวดเร็วสำหรับโซลูชันการฝังทั้งสองโดยใช้อินเทอร์เฟซแบบกราฟิกที่เรียบง่าย

ถ้าคุณกำลังสร้างแอปพลิเคชันแบบ *ฝังตัวสำหรับองค์กรของคุณ* และต้องการควบคุมแอป Azure AD ของคุณมากขึ้น คุณสามารถลงทะเบียนได้ด้วยตนเองในพอร์ทัล Azure

> [!IMPORTANT]
> ก่อนที่คุณลงทะเบียนแอป Power BI คุณต้องการ[ผู้เช่า Azure Active Directory และผู้ใช้ขององค์กร](create-an-azure-active-directory-tenant.md)

# <a name="embed-for-your-customers"></a>[ฝังสำหรับลูกค้าของคุณ](#tab/customers)

ขั้นตอนเหล่านี้จะอธิบายวิธีการลงทะเบียนแอปพลิเคชัน Azure AD สำหรับโซลูชัน[ฝังตัวสำหรับลูกค้าของคุณ](embed-sample-for-customers.md)ใน Power BI

[!INCLUDE[registration tool step 1](../../includes/register-tool-step-1.md)]

2. ในส่วน *เลือกโซลูชันการฝังตัว* ให้เลือก **ฝังตัวสำหรับลูกค้าของคุณ**

[!INCLUDE[registration tool step 3](../../includes/register-tool-step-3.md)]

4. ใน *ขั้นตอนที่ 2 - ลงทะเบียนแอปพลิเคชันของคุณ* ให้กรอกเขตข้อมูลต่อไปนี้:

    * **ชื่อแอปพลิเคชัน** - ตั้งชื่อให้แอปพลิเคชันของคุณ

    * **การเข้าถึง API** - เลือก Power BI APIs (หรือที่เรียกว่าขอบเขต) ที่แอปพลิเคชันของคุณต้องการ คุณสามารถใช้ *เลือกทั้งหมด* เพื่อเลือก APIs ทั้งหมด สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์การเข้าถึง Power BI ให้ดู [สิทธิ์และการยินยอมในจุดสิ้นสุดของแพลตฟอร์มข้อมูลประจำตัวของ Microsoft](/azure/active-directory/develop/v2-permissions-and-consent)

5. เลือก **ลงทะเบียน**

    **ID แอปพลิเคชัน** สำหรับแอป Azure AD ของคุณจะแสดงอยู่ในกล่อง *สรุป* คัดลอกค่านี้เพื่อใช้งานในภายหลัง

[!INCLUDE[registration tool steps 6-7](../../includes/register-tool-steps-6-7.md)]

8. ใน *ขั้นตอนที่ 5 - ให้สิทธิ์* ให้เลือก **ให้สิทธิ์** และเลือก **ยอมรับ** ในหน้าต่างป็อปอัพ ซึ่งจะช่วยให้แอป Azure AD ของคุณสามารถเข้าถึง APIs ที่คุณเลือก (หรือที่เรียกว่าขอบเขต) ด้วยผู้ใช้ที่ลงชื่อเข้าใช้ของคุณ ผู้ใช้รายนี้ถุกเรียกอีกอย่างว่า **ผู้ใช้หลัก**

9. (ไม่บังคับ) ถ้าคุณสร้างพื้นที่ทำงาน Power BI และอัปโหลดเนื้อหาโดยใช้เครื่องมือ ตอนนี้คุณสามารถเลือก **ดาวน์โหลดแอปพลิเคชันตัวอย่าง** ได้ อย่าลืมคัดลอกข้อมูลทั้งหมดในช่อง *สรุป*

[!INCLUDE[registration tool note](../../includes/register-tool-note.md)]

# <a name="embed-for-your-organization"></a>[ฝังตัวสำหรับองค์กรของคุณ](#tab/organization)

ขั้นตอนเหล่านี้จะอธิบายวิธีการลงทะเบียนแอปพลิเคชัน Azure AD สำหรับโซลูชัน[ฝังตัวสำหรับองค์กรของคุณ](embed-sample-for-your-organization.md)ใน Power BI

[!INCLUDE[registration tool step 1](../../includes/register-tool-step-1.md)]

2. ในส่วน *เลือกโซลูชันการฝังตัว* ให้เลือก **ฝังตัวสำหรับองค์กรของคุณ**

[!INCLUDE[registration tool step 3](../../includes/register-tool-step-3.md)]

4. ใน *ขั้นตอนที่ 2 - ลงทะเบียนแอปพลิเคชันของคุณ* ให้กรอกเขตข้อมูลต่อไปนี้:

    * **ชื่อแอปพลิเคชัน** - ตั้งชื่อให้แอปพลิเคชันของคุณ

    * **URL ของโฮมเพจ** - ป้อน URL สำหรับโฮมเพจของคุณ

    * **URL เปลี่ยนเส้นทาง** - เมื่อลงชื่อเข้าใช้ ผู้ใช้แอปพลิเคชันของคุณจะถูกเปลี่ยนเส้นทางไปยังที่อยู่นี้ในขณะที่แอปพลิเคชันของคุณได้รับรหัสรับรองความถูกต้องจาก Azure เลือกหนึ่งในตัวเลือกเหล่านี้:

        * **ใช้ URL ค่าเริ่มต้น** - ตัวเลือกนี้จะสร้างและดาวน์โหลดตัวอย่างแอปพลิเคชันการวิเคราะห์แบบฝังตัวโดยอัตโนมัติ URL ค่าเริ่มต้นคือ http://localhost:13526/

        * **ใช้ URL ที่กำหนดเอง** - เลือกตัวเลือกนี้หากคุณมีแอปพลิเคชันการวิเคราะห์แบบฝังตัวอยู่แล้ว และทราบว่าคุณต้องการใช้อะไรเป็น URL เปลี่ยนเส้นทาง

    * **การเข้าถึง API** - เลือก Power BI APIs (หรือที่เรียกว่าขอบเขต) ที่แอปพลิเคชันของคุณต้องการ คุณสามารถใช้ *เลือกทั้งหมด* เพื่อเลือก APIs ทั้งหมด สำหรับข้อมูลเพิ่มเติมเกี่ยวกับสิทธิ์การเข้าถึง Power BI ให้ดู [สิทธิ์และการยินยอมในจุดสิ้นสุดของแพลตฟอร์มข้อมูลประจำตัวของ Microsoft](/azure/active-directory/develop/v2-permissions-and-consent)

5. เลือก **ลงทะเบียน**

    **ID แอปพลิเคชัน** และค่า **รหัสลับแอปพลิเคชัน** ของแอป Azure AD ของคุณจะแสดงในกล่อง *สรุป* คัดลอกค่าเหล่านี้เพื่อใช้งานในภายหลัง

[!INCLUDE[registration tool steps 6-7](../../includes/register-tool-steps-6-7.md)]

8. (ไม่บังคับ) ถ้าคุณสร้างพื้นที่ทำงาน Power BI และอัปโหลดเนื้อหาโดยใช้เครื่องมือ ตอนนี้คุณสามารถเลือก **ดาวน์โหลดแอปพลิเคชันตัวอย่าง** ได้ อย่าลืมคัดลอกข้อมูลทั้งหมดในช่อง *สรุป*

[!INCLUDE[registration tool note](../../includes/register-tool-note.md)]

# <a name="manual-registration"></a>[การลงทะเบียนด้วยตนเอง](#tab/manual)

ใช้การลงทะเบียนแอป Azure AD ด้วยตนเองเฉพาะในกรณีที่คุณกำลังสร้างหนึ่งในโซลูชันต่อไปนี้:

* แอปพลิเคชัน *การฝังตัวสำหรับองค์กรของคุณ*

* แอปพลิเคชัน *การฝังตัวสำหรับลูกค้าของคุณ* ด้วย *โครงร่างสำคัญของบริการ*

    >[!NOTE]
    >ถ้าคุณเลือกตัวเลือกนี้ หลังจากที่คุณลงทะเบียนแอป Azure AD ของคุณ คุณจะต้อง[เพิ่มสิทธิ์ Power BI](#change-your-azure-ad-apps-permissions)

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับวิธีการลงทะเบียนแอปพลิเคชันใน Azure Active Directory ดู[กาลงทะเบียนใช้แอปพลิเคชันด้วย Azure Active Directory](/azure/active-directory/develop/quickstart-v2-register-an-app)

1. ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com)

2. เลือกผู้เช่า Azure AD ของคุณ โดยการเลือกบัญชีของคุณในมุมบนขวาของหน้า

3. เลือก **การลงทะเบียนแอป** หากคุณไม่เห็นตัวเลือกนี้ ให้ค้นหา
 
4. ใน *การลงทะเบียนแอป* ให้เลือก **การลงทะเบียนใหม่**

5. กรอกข้อมูลในเขตข้อมูลต่อไปนี้:

    * **ชื่อ** - ตั้งชื่อให้แอปพลิเคชันของคุณ

    * **ชนิดบัญชีที่รองรับ** - เลือกผู้ที่สามารถใช้แอปพลิเคชันได้

6. (ไม่บังคับ) ใน **URI เปลี่ยนเส้นทาง** ให้เพิ่ม URL เปลี่ยนเส้นทาง

7. เลือก **ลงทะเบียน** หลังจากลงทะเบียนแอปแล้ว คุณจะเข้าสู่หน้าภาพรวมของแอปซึ่งคุณสามารถรับ *ID แอปพลิเคชัน*

---

## <a name="change-your-azure-ad-apps-permissions"></a>เปลี่ยนสิทธิ์ของแอป Azure AD ของคุณ

หลังจากที่คุณลงทะเบียนแอปพลิเคชันของคุณแล้ว คุณสามารถทำการเปลี่ยนแปลงสิทธิ์ของคุณได้ การเปลี่ยนแปลงสิทธิ์สามารถทำได้ผ่านการกำหนดด้วยโปรแกรมหรือในพอร์ทัล Azure

>[!NOTE]
>สิทธิ์ของแอป Azure AD ใช้ได้กับโซลูชัน *การฝังตัวสำหรับลูกค้าของคุณ* ด้วยวิธีการรับรองความถูกต้อง *ผู้ใช้หลัก* เท่านั้น

# <a name="azure"></a>[Azure](#tab/Azure)

ในพอร์ทัล Azure คุณสามารถดูแอปของคุณและทำการเปลี่ยนแปลงสิทธิ์ของคุณได้

1. ลงชื่อเข้าใช้[พอร์ทัล Azure](https://portal.azure.com)

2. เลือกผู้เช่า Azure AD ของคุณ โดยการเลือกบัญชีของคุณในมุมบนขวาของหน้า

3. เลือก **การลงทะเบียนแอป** หากคุณไม่เห็นตัวเลือกนี้ ให้ค้นหา

4. จากแท็บ **แอปพลิเคชันที่เป็นเจ้า** ให้เลือกแอปของคุณ แอปพลิเคชันจะเปิดขึ้นในแท็บ *ภาพรวม* ซึ่งคุณสามารถตรวจสอบ *ID แอปพลิเคชัน* ได้

5. เลือกแท็บ **สิทธิ์ API**

6. เมื่อต้องเพิ่มสิทธิ์ ให้ทำตามขั้นตอนเหล่านี้:

    1. เลือก **เพิ่มสิทธิ์** จากนั้นเลือก **บริการ Power BI**

    2. เลือก **สิทธิ์ที่ได้รับมอบหมาย** และเพิ่มหรือลบสิทธิ์เฉพาะที่คุณต้องการ

    3. เมื่อคุณทำเสร็จแล้ว ให้เลือก **เพิ่มสิทธิ์** เพื่อบันทึกการเปลี่ยนแปลงของคุณ

7. เมื่อต้องการเอาสิทธิ์ออก ให้ทำตามขั้นตอนเหล่านี้:

    1. เลือกจุดไข่ปลา (...) ทางด้านขวาของสิทธิ์
    
    2. เลือก **เอาสิทธิ์ออก**
    
    3. ในหน้าต่างป็อปอัพ *เอาสิทธิ์ออก* ให้เลือก **ใช่ เอาออก**

# <a name="http"></a>[HTTP](#tab/HTTP)

เมื่อต้องการเปลี่ยนสิทธิ์แอป Azure AD ของคุณผ่านการกำหนดด้วยโปรแกรม คุณจะต้องได้รับชื่อบัญชีผู้ใช้บริการ (ผู้ใช้) ที่มีอยู่ภายในผู้เช่าของคุณ สำหรับข้อมูลเกี่ยวกับวิธีการดังกล่าว ดู[servicePrincipal](/graph/api/resources/serviceprincipal)

1. หากต้องการรับชื่อบัญชีผู้ใช้บริการทั้งหมดภายในผู้เช่าของคุณ ให้เรียกใช้ API `Get servicePrincipal` โดยไม่ต้องใช้ `{ID}`

2. ตรวจสอบชื่อบัญชีผู้ใช้บริการโดยใช้ *ID แอปพลิเคชัน* ของแอปของคุณเป็นคุณสมบัติ `appId`

    ```json
    Post https://graph.microsoft.com/v1.0/servicePrincipals HTTP/1.1
    Authorization: Bearer ey..qw
    Content-Type: application/json
    {
    "accountEnabled" : true,
    "appId" : "{App_Client_ID}",
    "displayName" : "{App_DisplayName}"
    }
    ```

    >[!NOTE]
    >`displayName` เป็นแบบทางเลือก

3. ให้สิทธิ์ Power BI แก่แอปของคุณโดยกำหนดค่าใดค่าหนึ่งเป็น `consentType`:

    * `AllPrincipals` - สามารถใช้ได้โดยผู้ดูแลระบบ Power BI เท่านั้นเพื่อให้สิทธิ์ในนามของผู้ใช้ทั้งหมดในผู้เช่า

    * `Principal` - ใช้เพื่อให้สิทธิ์ในนามของผู้ใช้ที่ระบุ ถ้าคุณกำลังใช้ตัวเลือกนี้ ให้เพิ่มคุณสมบัติ `principalId={User_ObjectId}` ลงในเนื้อหาคำขอ

     ```json
     Post https://graph.microsoft.com/v1.0/OAuth2PermissionGrants HTTP/1.1
     Authorization: Bearer ey..qw
     Content-Type: application/json
     {
     "clientId":"{Service_Plan_ID}",
     "consentType":"AllPrincipals",
     "resourceId":"c78a3685-1ce7-52cd-95f7-dc5aea8ec98e",
     "scope":"Dataset.ReadWrite.All Dashboard.Read.All Report.Read.All Group.Read Group.Read.All Content.Create Metadata.View_Any Dataset.Read.All Data.Alter_Any",
     "expiryTime":"2018-03-29T14:35:32.4943409+03:00",
     "startTime":"2017-03-29T14:35:32.4933413+03:00"
     }
     ```

    >[!NOTE]
    >* หากคุณใช้ **ผู้ใช้หลัก** เพื่อหลีกเลี่ยงไม่ให้ Azure AD พร้อมต์แจ้งขอรับคำยินยอม คุณจะต้องให้สิทธิ์แก่บัญชีหลัก
    >* `resourceId` *c78a3685-1ce7-52cd-95f7-dc5aea8ec98e* ขึ้นอยู่กับผู้เช่าและไม่เป็นสากล ค่านี้เป็น *objectId* ของแอปพลิเคชัน *Power BI Service* ใน Azure AD หากต้องการรับค่านี้จากพอร์ทัล Azure ให้ไปที่ [Enterprise applications> All applications](https://portal.azure.com/#blade/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/AllApps) และค้นหา *Power BI Service*

4. ให้สิทธิ์แอปแก่ Azure AD โดยกำหนดค่าเป็น `consentType`

    ```json
    Post https://graph.microsoft.com/v1.0/OAuth2PermissionGrants HTTP/1.1
    Authorization: Bearer ey..qw
    Content-Type: application/json
    {
    "clientId":"{Service_Plan_ID}",
    "consentType":"AllPrincipals",
    "resourceId":"61e57743-d5cf-41ba-bd1a-2b381390a3f1",
    "scope":"User.Read Directory.AccessAsUser.All",
    "expiryTime":"2018-03-29T14:35:32.4943409+03:00",
    "startTime":"2017-03-29T14:35:32.4933413+03:00"
    }
    ```

# <a name="c"></a>[C#](#tab/CSharp)

คุณยังสามารถเปลี่ยนสิทธิ์แอป Azure AD ของคุณโดยใช้ C# สำหรับข้อมูลเพิ่มเติม โปรดดู API สำหรับ [oAuth2PermissionGrant](/graph/api/oauth2permissiongrant-get) วิธีนี้มีประโยชน์หากคุณกำลังพิจารณาที่จะทำให้กระบวนการบางอย่างเป็นไปโดยอัตโนมัติ

สำหรับข้อมูลเพิ่มเติมเกี่ยวกับคำขอ HTTP โปรดดูที่[แท็บ HTTP](register-app.md?tabs=customers%2CHTTP#change-your-azure-ad-apps-permissions)

```csharp
var graphClient = GetGraphClient();

currentState.createdApp = await graphClient.Applications
    .Request()
    .AddAsync(application);

System.Threading.Thread.Sleep(2000);

var passwordCredential = new PasswordCredential
{
    DisplayName = "Client Secret Created in C#"
};

currentState.createdSecret = await graphClient.Applications[currentState.createdApp.Id]
    .AddPassword(passwordCredential)
    .Request()
    .PostAsync();

var servicePrincipal = new ServicePrincipal
{
    AppId = currentState.createdApp.AppId
};

currentState.createdServicePrincipal = await graphClient.ServicePrincipals
    .Request()
    .AddAsync(servicePrincipal);

GraphServiceClient graphClient = new GraphServiceClient(authProvider);

// Use oAuth2PermissionGrant to change permissions
var oAuth2PermissionGrant = await graphClient.Oauth2PermissionGrants["{id}"]
               .Request()
               .GetAsync();
```

---

## <a name="next-steps"></a>ขั้นตอนถัดไป

>[!div class="nextstepaction"]
>[รับโทเค็นการเข้าถึง Azure AD สำหรับแอปพลิเคชัน Power BI ของคุณ](get-azuread-access-token.md)

มีคำถามเพิ่มเติมหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)