---
title: เปิดใช้งานการตรวจสอบโครงร่างสำคัญของบริการสำหรับ API ของผู้ดูแลระบบแบบอ่านอย่างเดียว (แสดงตัวอย่าง)
description: เรียนรู้วิธีการตรวจสอบหลักการบริการเพื่ออนุญาตให้ใช้ Api ของผู้ดูแลระบบแบบอ่านอย่างเดียวได้
author: paulinbar
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: how-to
ms.date: 12/01/2020
ms.author: painbar
ms.custom: ''
LocalizationGroup: Administration
ms.openlocfilehash: 48e1a82b7a88bf4535acea49ea6770cedfdbf304
ms.sourcegitcommit: 1cad78595cca1175b82c04458803764ac36e5e37
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 01/19/2021
ms.locfileid: "98564876"
---
# <a name="enable-service-principal-authentication-for-read-only-admin-apis-preview"></a>เปิดใช้งานการตรวจสอบโครงร่างสำคัญของบริการสำหรับ API ของผู้ดูแลระบบแบบอ่านอย่างเดียว (แสดงตัวอย่าง)

หลักการบริการคือวิธีการรับรองความถูกต้องที่สามารถใช้เพื่ออนุญาตให้มีการเข้าถึงแอปพลิเคชัน Azure Active Directory (Azure AD) เนื้อหาแบริการของ Power BI และ Api ได้
เมื่อคุณสร้างแอป Azure AD  [วัตถุหลักการบริการ](/azure/active-directory/develop/app-objects-and-service-principals#service-principal-object) จะถูกสร้างขึ้น หลักการบริการ ซึ่งเป็นที่รู้จักกันว่าหลักการบริการ จะช่วยให้ Azure AD รับรองความถูกต้องของแอปของคุณ เมื่อรับรองความถูกต้องแล้ว แอปจะสามารถเข้าถึงแหล่งข้อมูลผู้เช่า Azure AD

## <a name="method"></a>วิธีการ

เมื่อต้องการเปิดใช้การตรวจสอบหลักการบริการสำหรับ Api แบบอ่านอย่างเดียวของ Power BI ให้ทำตามขั้นตอนเหล่านี้:

1. [สร้างแอป Azure AD](/azure/active-directory/develop/howto-create-service-principal-portal) คุณสามารถข้ามขั้นตอนนี้ได้ถ้าคุณมีแอป Azure AD ที่คุณต้องการใช้อยู่แล้ว จด App-Id สำหรับขั้นตอนต่อไป 
2. สร้าง **กลุ่มความปลอดภัย** ใหม่ใน Azure Active Directory [อ่านเพิ่มเติมเกี่ยวกับวิธีการสร้างกลุ่มพื้นฐานและเพิ่มสมาชิกโดยใช้ Azure Active Directory](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) คุณสามารถข้ามขั้นตอนนี้ได้ถ้าคุณมีกลุ่มความปลอดภัยที่คุณต้องการใช้งานอยู่แล้ว
    ตรวจสอบให้แน่ใจว่าได้เลือก **ความปลอดภัย** เป็นประเภทกลุ่ม

    ![สกรีนช็อตกล่องโต้ตอบการสร้างกลุ่มใหม่ในพอร์ทัล Azure](media/read-only-apis-service-principal-auth/azure-portal-new-group-dialog.png)

3. เพิ่มApp-Id ของคุณเป็นสมาชิกของกลุ่มความปลอดภัยที่คุณสร้างขึ้น โดยดำเนินการดังนี้:
    1. นำทางไปยัง **พอร์ทัล Azure > Azure Active Directory >  กลุ่ม** และเลือกกลุ่มความปลอดภัยที่คุณสร้างในขั้นตอนที่ 2
    1. เลือก **เพิ่มสมาชิก**
    หมายเหตุ: ตรวจสอบให้แน่ใจว่าแอปที่คุณใช้ไม่มีบทบาทผู้ดูแลระบบ Power BI ใดๆ ที่ตั้งค่าไว้ในพอร์ทัล Azure เมื่อต้องการตรวจสอบ ให้ทำดังนี้: 
       * ลงชื่อเข้าใช้ **พอร์ทัล Azure** เป็นผู้ดูแลระบบส่วนกลาง ผู้ดูแลระบบแอปพลิเคชัน หรือผู้ดูแลระบบแอปพลิเคชันระบบคลาวด์ 
        * เลือก **Azure Active Directory** จากนั้น **แอปพลิเคชันขององค์กร** 
        * เลือกแอปพลิเคชันที่คุณต้องการอนุญาตให้เข้าถึง Power BI 
        * เลือก **การอนุญาต** ตรวจสอบให้แน่ใจว่าไม่มีการอนุญาตที่จำเป็นสำหรับผู้ดูแลระบบ Power BI ที่ตั้งค่าไว้ในแอปพลิเคชันนี้ ดู[การจัดการความยินยอมให้กับแอปพลิเคชันและประเมินคำขอการยินยอม](/azure/active-directory/manage-apps/manage-consent-requests)สำหรับข้อมูลเพิ่มเติม 
4. เปิดใช้งานการตั้งค่าการจัดการบริการของ Power BI ในการทำขั้นตอนนี้:
    1. เข้าสู่ระบบพอร์ทัลผู้ดูแลระบบของ Power BI คุณจำเป็นต้องเป็นผู้ดูแลระบบ Power BI เพื่อดูหน้าการตั้งค่าผู้เช่า
    1. ที่ด้านล่าง **การตั้งค่า API ผู้ดูแลระบบ** คุณจะเห็น **อนุญาตให้บริการหลักใช้ API ผู้ดูแลระบบ Power BI แบบอ่านได้เท่านั้น (ตัวอย่าง)** ตั้งค่าการสลับเป็นเปิดใช้งานจากนั้นเลือกปุ่มตัวเลือก **กลุ่มความปลอดภัยเฉพาะ** และเพิ่มกลุ่มความปลอดภัยที่คุณสร้างไว้ในขั้นตอนที่ 2 ในช่องข้อความที่ปรากฏด้านล่างดังแสดงในรูปด้านล่าง

        ![สกรีนช็อตการตั้งค่าผู้เช่าที่อนุญาตให้ใช้หลักการบริการ](media/read-only-apis-service-principal-auth/allow-service-principals-tenant-setting.png)

 5. เริ่มต้นใช้งาน API ผู้ดูแลแบบอ่านอย่างเดียว ดูรายการของ API ที่รองรับด้านล่าง

    >[!IMPORTANT]
    >เมื่อคุณเปิดใช้งานหลักการบริการเพื่อใช้กับ Power BI แล้ว สิทธิ์ Azure AD ของแอปพลิเคชันจะไม่มีผลอีกต่อไป มีจัดการสิทธิ์ของแอปพลิเคชันแล้วผ่านทางพอร์ทัลผู้ดูแลระบบ Power BI

## <a name="considerations-and-limitations"></a>ข้อควรพิจารณาและข้อจำกัด
* คุณไม่สามารถลงชื่อเข้าใช้พอร์ทัล Power BI ด้วยบริการหลัก
* คุณจำเป็นต้องมีสิทธิ์ของผู้ดูแลระบบ Power BI เพื่อเปิดใช้งานบริการหลักในการตั้งค่า API ผู้ดูแลระบบภายในพอร์ทัลผู้ดูแลระบบของ Power BI
* หลักการบริการในขณะนี้สนับสนุน API ต่อไปนี้:
    * [GetGroupsAsAdmin](/rest/api/power-bi/admin/groups_getgroupsasadmin) ที่มี $expand สำหรับแดชบอร์ด ชุดข้อมูล รายงาน และกระแสข้อมูล 
    * [GetDashboardsAsAdmin](/rest/api/power-bi/admin/dashboards_getdashboardsasadmin) ที่มีไทล์ $expand
    * [GetDatasourcesAsAdmin](/rest/api/power-bi/admin/datasets_getdatasourcesasadmin) 
    * [GetDatasetToDataflowsLinksAsAdmin](/rest/api/power-bi/admin/datasets_getdatasettodataflowslinksingroupasadmin)
    * [GetDatasourcesAsAdmin](/rest/api/power-bi/admin/dataflows_getdataflowdatasourcesasadmin) 
    * [GetDataflowUpstreamDataflowsAsAdmin](/rest/api/power-bi/admin/dataflows_getupstreamdataflowsingroupasadmin) 
    * [GetCapacitiesAsAdmin](/rest/api/power-bi/admin/getcapacitiesasadmin)
    * [GetActivityLog](/rest/api/power-bi/admin/getactivityevents)
    * [GetModifiedWorkspaces](/rest/api/power-bi/admin/workspaceinfo_getmodifiedworkspaces)
    * [WorkspaceGetInfo](/rest/api/power-bi/admin/workspaceinfo_postworkspaceinfo)
    * [WorkspaceScanStatus](/rest/api/power-bi/admin/workspaceinfo_getscanstatus)
    * [WorkspaceScanResult](/rest/api/power-bi/admin/workspaceinfo_getscanresult)