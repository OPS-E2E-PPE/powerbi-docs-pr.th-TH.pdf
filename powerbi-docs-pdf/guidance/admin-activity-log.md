---
title: เข้าถึงบันทึกกิจกรรม Power BI
description: คำแนะนำและรหัสสคริปต์ของตัวอย่าง PowerShell สำหรับการทำงานกับบันทึกกิจกรรม Power BI
author: peter-myers
ms.author: kfollis
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: sample
ms.date: 09/03/2020
ms.openlocfilehash: 0e86966225060c24aa154c0b29ea533dad89908b
ms.sourcegitcommit: fb529c4532fbbdfde7ce28e2b4b35f990e8f21d9
ms.translationtype: MT
ms.contentlocale: th-TH
ms.lasthandoff: 01/30/2021
ms.locfileid: "99088706"
---
# <a name="access-the-power-bi-activity-log"></a>เข้าถึงบันทึกกิจกรรม Power BI

บทความนี้เหมาะสำหรับผู้ดูแลระบบ Power BI ซึ่งต้องการเข้าถึงบันทึกกิจกรรมของ Power BI เนื่องจากยังไม่มีอินเทอร์เฟซผู้ใช้ในการค้นหาบันทึกกิจกรรม คุณจึงต้องใช้ Power BI REST API และ cmdlet สำหรับการจัดการ

> [!NOTE]
> บทความนี้ไม่ได้แนะนำหรืออธิบายเกี่ยวกับบันทึกกิจกรรม Power BI สำหรับข้อมูลเพิ่มเติมดู [ติดตามกิจกรรมของผู้ใช้ใน Power BI](../admin/service-admin-auditing.md#use-the-activity-log)

## <a name="powershell-sample"></a>ตัวอย่าง PowerShell

ตัวอย่าง PowerShell พร้อมใช้งาน เพื่อช่วยให้คุณสามารถเรียนรู้วิธีการกรองและเรียกคืนข้อมูลเกี่ยวกับเหตุการณ์การบันทึกกิจกรรม Power BI ได้ ส่วนย่อยของรหัสและสถานการณ์ทั้งหมดมีคำอธิบายประกอบพร้อมด้วยคำแนะนำเกี่ยวกับวิธีใช้ และข้อเสียหรือปัญหาทั่วไปที่ต้องระวัง ซึ่งจะครอบคลุมสถานการณ์สองรูปแบบ:

- เรียกคืนรายการของผู้ใช้สำหรับแอปที่เฉพาะเจาะจง
- เรียกคืนรายการของผู้ใช้สำหรับการแชร์รายงานโดยตรง

> [!NOTE]
> คุณจะต้องมีความคุ้นเคยกับ [Power BI Admin API](/rest/api/power-bi/admin) และ [มอดูล Power BI PowerShell](/powershell/power-bi/overview?view=powerbi-ps&preserve-view=true) คุณต้องติดตั้งมอดูล PowerShell ก่อนที่จะดำเนินการบล็อกสคริปต์เหล่านี้ สำหรับข้อมูลเพิ่มเติมดู [ติดตามกิจกรรมของผู้ใช้ใน Power BI](../admin/service-admin-auditing.md#use-the-activity-log)
>
> การเรียกคืนข้อมูลกิจกรรมของ Power BI อาจมีความล่าช้าได้ถึง 30 นาที

หากต้องการใช้ตัวอย่าง คุณต้องทำตามข้อกำหนดต่อไปนี้:

- ติดตั้ง[มอดูล Power BI PowerShell](/powershell/power-bi/overview)
- ผู้ใช้สคริปต์ PowerShell ต้องลงชื่อเข้าใช้ด้วย [Connect-PowerBIServiceAccount cmdlet](/powershell/module/microsoftpowerbimgmt.profile/connect-powerbiserviceaccount) และระบุข้อมูลประจำตัว Power BI เมื่อได้รับข้อความแจ้งเตือน จำเป็นต้องมีสิทธิ์ผู้ดูแลระบบเพื่อใช้ API บันทึกกิจกรรม

> [!IMPORTANT]
> ผู้ใช้ที่ไม่มีสิทธิ์ของผู้ดูแลระบบจะไม่สามารถดำเนินการกับส่วนย่อยของรหัสในสคริปต์ตัวอย่างได้

```powershell
# Written by Sergei Gundorov; v1 development started on 07/08/2020
#
# Intent: 1. Address common friction points and usage issues and questions related to the
#            events generated by Power BI Service that are stored in the activity log.
#         2. Provide boiler plate code for capturing all 30 days of available data.
#         3. Power BI admin privileges are required to use the Activity Log API.
#
# Use:    Sign in to the Power BI service with admin privileges and execute specific segment one at a time.

# IMPORTANT: Use Connect-PowerBIServiceAccount to connect to the service before running individual code segments.

# IMPORTANT: $day value may need to be adjusted depending on where you're located in the world relative to UTC.
#            The Power BI activity log records events using UTC time; so add or subtract days according to your global location.

# SCENARIO: Sample code fragment to retrieve a limited number of attributes for specific events for specific user report viewing activity.
# You need to get user's Azure Active Directory (AAD) object ID. You can use this Azure AD cmdlet: https://docs.microsoft.com/powershell/module/azuread/get-azureaduser?view=azureadps-2.0

# Dates need to be entered using ISO 8601 format; adjust dates to span no more than 24 hours.
$a=Get-PowerBIActivityEvent -StartDateTime '2020-06-23T19:00:00.000' -EndDateTime '2020-06-23T20:59:59.999' -ActivityType 'ViewReport' -User [USER AAD ObjectId GUID] | ConvertFrom-Json

# You can use any attribute value to filter results further. For example, a specific event request Id can be used to analyze just one specific event.
$a | Select RequestId, ReportName, WorkspaceName |where {($_.RequestId -eq '[RequestId GUID of the event]')}

# SCENARIO: Retrieve a list of users for specific app.
# The user list can be partially derived (based on last 30 days of available activity) by combining data for two events: CreateApp and UpdateApp.
# Both events will contain OrgAppPermission property that contains app user access list.
# Actual app installation can be tracked using InstallApp activity.
# Run each code segment separately for each event.

# Iterate through 30 days of activity CreateApp.
$day=Get-date

for($s=0; $s -le 30; $s++)
{
    $periodStart=$day.AddDays(-$s)
    $base=$periodStart.ToString("yyyy-MM-dd")

    write-host $base

    $a=Get-PowerBIActivityEvent -StartDateTime ($base+'T00:00:00.000') -EndDateTime ($base+'T23:59:59.999') -ActivityType 'CreateApp' -ResultType JsonString | ConvertFrom-Json
    $c=$a.Count

    for($i=0 ; $i -lt $c; $i++)
    {
        $r=$a[$i]
        Write-Host "App Name `t: $($r.ItemName)"
                 ` "WS Name `t: $($r.WorkSpaceName)"
                 ` "WS ID `t`t: $($r.WorkspaceId)"
                 ` "Created `t: $($r.CreationTime)"
                 ` "Users `t`t: $($r.OrgAppPermission) `n"
    }
}

# Iterate through 30 days of activity UpdateApp.
$day=Get-date

for($s=0; $s -le 30; $s++)
{
    $periodStart=$day.AddDays(-$s)
    $base=$periodStart.ToString("yyyy-MM-dd")

    write-host $base

    $a=Get-PowerBIActivityEvent -StartDateTime ($base+'T00:00:00.000') -EndDateTime ($base+'T23:59:59.999') -ActivityType 'UpdateApp' -ResultType JsonString | ConvertFrom-Json
    $c=$a.Count

    for($i=0 ; $i -lt $c; $i++)
    {
        $r=$a[$i]
        Write-Host "App Name `t: $($r.ItemName)"
                 ` "WS Name `t: $($r.WorkSpaceName)"
                 ` "WS ID `t`t: $($r.WorkspaceId)"
                 ` "Updated `t: $($r.CreationTime)"
                 ` "Users `t`t: $($r.OrgAppPermission) `n"
    }
}

# Iterate through 30 days of activity InstallApp.
$day=Get-date

for($s=0; $s -le 30; $s++)
{
    $periodStart=$day.AddDays(-$s)
    $base=$periodStart.ToString("yyyy-MM-dd")

    write-host $base

    $a=Get-PowerBIActivityEvent -StartDateTime ($base+'T00:00:00.000') -EndDateTime ($base+'T23:59:59.999') -ActivityType 'InstallApp' -ResultType  JsonString | ConvertFrom-Json
    $c=$a.Count

    for($i=0 ; $i -lt $c; $i++)
    {
        $r=$a[$i]
        Write-Host "App Name `t: $($r.ItemName)"
                 ` "Installed `t: $($r.CreationTime)"
                 ` "User `t`t: $($r.UserId) `n"
    }
}

# SCENARIO: Retrieve a list of users for direct report sharing.
# This logic and flow can be used for tracing direct dashboard sharing by substituting activity type.
# Default output is formatted to return the list of users as a string. There is commented out code block to get multi-line user list.
# IMPORTANT: Removal of a user or group from direct sharing access list event is not tracked. For this reason, the list may be not accurate.
# IMPORTANT: If the user list contains a GUID instead of a UPN the report was shared to a group.
#            Group name and email can be obtained using Azure AD cmdlets using captured ObjectId GUID.

# Iterate through 30 days of activity ShareReport.
$day=Get-date

for($s=0; $s -le 30; $s++)
{
    $periodStart=$day.AddDays(-$s)
    $base=$periodStart.ToString("yyyy-MM-dd")

    #write-host $base

    $a=Get-PowerBIActivityEvent -StartDateTime ($base+'T00:00:00.000') -EndDateTime ($base+'T23:59:59.999') -ActivityType 'ShareReport' -ResultType JsonString | ConvertFrom-Json
    $c=$a.Count

    for($i=0 ; $i -lt $c; $i++)
    {
        $r=$a[$i]

        Write-Host "Rpt Name `t: $($r.ItemName)"
                 ` "Rpt Id  `t: $($r.ArtifactId)"
                 ` "WS Name  `t: $($r.WorkSpaceName)"
                 ` "WS ID  `t`t: $($r.WorkspaceId)"
                 ` "Capacity  `t: $($r.CapacityId)"
                 ` "SharedOn  `t: $($r.CreationTime.Replace('T',' ').Replace('Z',''))"
                 ` "User `t`t: $($r.UserId)"
                 #  NOTE:  $_.RecipientEmail + $_.RecipientName or +$_.ObjectId is the case for group sharing
                 #         can never happen both at the same time in the same JSON record
                 ` "Shared with`t: $(($r.SharingInformation)| % {$_.RecipientEmail + $_.ObjectId +'[' + $_.ResharePermission +']'})"


       #OPTIONAL: Formatted output for SharingInformation attribute
       #$sc= $r.SharingInformation.Count
       #Write-Host "Shared with`t:"
       #for($j=0;$j -lt $sc;$j++)
       #{
       #     Write-Host "`t`t`t  $($r.SharingInformation[$j].RecipientEmail)" -NoNewline
       #     Write-Host $r.SharingInformation[$j].ObjectId -NoNewline
       #     Write-Host ('[' + $r.SharingInformation[$j].ResharePermission +']')
       #}

       Write-host ""
    }
}
```

## <a name="next-steps"></a>ขั้นตอนถัดไป

สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:

- [ติดตามกิจกรรมของผู้ใช้ใน Power BI](../admin/service-admin-auditing.md#use-the-activity-log)
- มีคำถามหรือไม่ [ลองถามชุมชน Power BI](https://community.powerbi.com/)
- มีข้อเสนอแนะไหม [สนับสนุนแนวคิดในการปรับปรุง Power BI](https://ideas.powerbi.com/)
