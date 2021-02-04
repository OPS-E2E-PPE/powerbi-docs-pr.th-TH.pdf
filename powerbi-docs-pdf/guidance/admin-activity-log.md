---
title: เข้าถึงบันทึกกิจกรรม Power BI
description: คำแนะนำและรหัสสคริปต์ของตัวอย่าง PowerShell สำหรับการทำงานกับบันทึกกิจกรรม Power BI
author: peter-myers
ms.author: v-pemyer
ms.reviewer: asaxton
ms.service: powerbi
ms.subservice: powerbi-admin
ms.topic: sample
ms.date: 09/03/2020
ms.openlocfilehash: 18ce155419f712cce2c4973949cd02ffbd870724
ms.sourcegitcommit: 653e18d7041d3dd1cf7a38010372366975a98eae
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 12/01/2020
ms.locfileid: "96394669"
---
# <a name="access-the-power-bi-activity-log"></a><span data-ttu-id="23896-103">เข้าถึงบันทึกกิจกรรม Power BI</span><span class="sxs-lookup"><span data-stu-id="23896-103">Access the Power BI activity log</span></span>

<span data-ttu-id="23896-104">บทความนี้เหมาะสำหรับผู้ดูแลระบบ Power BI ซึ่งต้องการเข้าถึงบันทึกกิจกรรมของ Power BI</span><span class="sxs-lookup"><span data-stu-id="23896-104">This article targets Power BI administrators who need to access the Power BI activity log.</span></span> <span data-ttu-id="23896-105">เนื่องจากยังไม่มีอินเทอร์เฟซผู้ใช้ในการค้นหาบันทึกกิจกรรม คุณจึงต้องใช้ Power BI REST API และ cmdlet สำหรับการจัดการ</span><span class="sxs-lookup"><span data-stu-id="23896-105">Because there's no user interface to search the activity log yet, you'll need to use the Power BI REST API and management cmdlets.</span></span>

> [!NOTE]
> <span data-ttu-id="23896-106">บทความนี้ไม่ได้แนะนำหรืออธิบายเกี่ยวกับบันทึกกิจกรรม Power BI</span><span class="sxs-lookup"><span data-stu-id="23896-106">This article doesn't introduce or describe the Power BI activity log.</span></span> <span data-ttu-id="23896-107">สำหรับข้อมูลเพิ่มเติมดู [ติดตามกิจกรรมของผู้ใช้ใน Power BI](../admin/service-admin-auditing.md#use-the-activity-log)</span><span class="sxs-lookup"><span data-stu-id="23896-107">For more information, see [Track user activities in Power BI](../admin/service-admin-auditing.md#use-the-activity-log).</span></span>

## <a name="powershell-sample"></a><span data-ttu-id="23896-108">ตัวอย่าง PowerShell</span><span class="sxs-lookup"><span data-stu-id="23896-108">PowerShell sample</span></span>

<span data-ttu-id="23896-109">ตัวอย่าง PowerShell พร้อมใช้งาน เพื่อช่วยให้คุณสามารถเรียนรู้วิธีการกรองและเรียกคืนข้อมูลเกี่ยวกับเหตุการณ์การบันทึกกิจกรรม Power BI ได้</span><span class="sxs-lookup"><span data-stu-id="23896-109">A PowerShell sample is available to help you learn how to filter and retrieve Power BI activity log events.</span></span> <span data-ttu-id="23896-110">ส่วนย่อยของรหัสและสถานการณ์ทั้งหมดมีคำอธิบายประกอบพร้อมด้วยคำแนะนำเกี่ยวกับวิธีใช้ และข้อเสียหรือปัญหาทั่วไปที่ต้องระวัง</span><span class="sxs-lookup"><span data-stu-id="23896-110">All code fragments and scenarios are annotated with how-to instructions and common gaps or issues to watch out for.</span></span> <span data-ttu-id="23896-111">ซึ่งจะครอบคลุมสถานการณ์สองรูปแบบ:</span><span class="sxs-lookup"><span data-stu-id="23896-111">Two scenarios are covered:</span></span>

- <span data-ttu-id="23896-112">เรียกคืนรายการของผู้ใช้สำหรับแอปที่เฉพาะเจาะจง</span><span class="sxs-lookup"><span data-stu-id="23896-112">Retrieve a list of users for specific app.</span></span>
- <span data-ttu-id="23896-113">เรียกคืนรายการของผู้ใช้สำหรับการแชร์รายงานโดยตรง</span><span class="sxs-lookup"><span data-stu-id="23896-113">Retrieve a list of users for direct report sharing.</span></span>

> [!NOTE]
> <span data-ttu-id="23896-114">คุณจะต้องมีความคุ้นเคยกับ [Power BI Admin API](/rest/api/power-bi/admin) และ [มอดูล Power BI PowerShell](/powershell/power-bi/overview?view=powerbi-ps)</span><span class="sxs-lookup"><span data-stu-id="23896-114">You'll need to have some familiarity with the [Power BI Admin API](/rest/api/power-bi/admin) and [Power BI PowerShell modules](/powershell/power-bi/overview?view=powerbi-ps).</span></span> <span data-ttu-id="23896-115">คุณต้องติดตั้งมอดูล PowerShell ก่อนที่จะดำเนินการบล็อกสคริปต์เหล่านี้</span><span class="sxs-lookup"><span data-stu-id="23896-115">PowerShell modules must be installed prior to executing these script blocks.</span></span> <span data-ttu-id="23896-116">สำหรับข้อมูลเพิ่มเติมดู [ติดตามกิจกรรมของผู้ใช้ใน Power BI](../admin/service-admin-auditing.md#use-the-activity-log)</span><span class="sxs-lookup"><span data-stu-id="23896-116">For more information, see [Track user activities in Power BI](../admin/service-admin-auditing.md#use-the-activity-log).</span></span>
>
> <span data-ttu-id="23896-117">การเรียกคืนข้อมูลกิจกรรมของ Power BI อาจมีความล่าช้าได้ถึง 30 นาที</span><span class="sxs-lookup"><span data-stu-id="23896-117">There can be a lag of up to 30 minutes to retrieve Power BI events.</span></span>

<span data-ttu-id="23896-118">หากต้องการใช้ตัวอย่าง คุณต้องทำตามข้อกำหนดต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="23896-118">To use the sample, you must meet the following requirements:</span></span>

- <span data-ttu-id="23896-119">ติดตั้ง[มอดูล Power BI PowerShell](/powershell/power-bi/overview)</span><span class="sxs-lookup"><span data-stu-id="23896-119">Install the [Power BI PowerShell modules](/powershell/power-bi/overview).</span></span>
- <span data-ttu-id="23896-120">ผู้ใช้สคริปต์ PowerShell ต้องลงชื่อเข้าใช้ด้วย [Connect-PowerBIServiceAccount cmdlet](/powershell/module/microsoftpowerbimgmt.profile/connect-powerbiserviceaccount) และระบุข้อมูลประจำตัว Power BI เมื่อได้รับข้อความแจ้งเตือน</span><span class="sxs-lookup"><span data-stu-id="23896-120">The user of the PowerShell script must sign in using the [Connect-PowerBIServiceAccount cmdlet](/powershell/module/microsoftpowerbimgmt.profile/connect-powerbiserviceaccount) and enter Power BI admin credentials when prompted.</span></span> <span data-ttu-id="23896-121">จำเป็นต้องมีสิทธิ์ผู้ดูแลระบบเพื่อใช้ API บันทึกกิจกรรม</span><span class="sxs-lookup"><span data-stu-id="23896-121">Admin privileges are required to use the Activity Log API.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23896-122">ผู้ใช้ที่ไม่มีสิทธิ์ของผู้ดูแลระบบจะไม่สามารถดำเนินการกับส่วนย่อยของรหัสในสคริปต์ตัวอย่างได้</span><span class="sxs-lookup"><span data-stu-id="23896-122">Users without admin privileges won't be able to execute code fragments in the sample script.</span></span>

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

## <a name="next-steps"></a><span data-ttu-id="23896-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="23896-123">Next steps</span></span>

<span data-ttu-id="23896-124">สำหรับข้อมูลเพิ่มเติมที่เกี่ยวข้องกับบทความนี้ โปรดดูทรัพยากรต่อไปนี้:</span><span class="sxs-lookup"><span data-stu-id="23896-124">For more information related to this article, check out the following resources:</span></span>

- [<span data-ttu-id="23896-125">ติดตามกิจกรรมของผู้ใช้ใน Power BI</span><span class="sxs-lookup"><span data-stu-id="23896-125">Track user activities in Power BI</span></span>](../admin/service-admin-auditing.md#use-the-activity-log)
- <span data-ttu-id="23896-126">มีคำถามหรือไม่</span><span class="sxs-lookup"><span data-stu-id="23896-126">Questions?</span></span> [<span data-ttu-id="23896-127">ลองถามชุมชน Power BI</span><span class="sxs-lookup"><span data-stu-id="23896-127">Try asking the Power BI Community</span></span>](https://community.powerbi.com/)
- <span data-ttu-id="23896-128">มีข้อเสนอแนะไหม</span><span class="sxs-lookup"><span data-stu-id="23896-128">Suggestions?</span></span> [<span data-ttu-id="23896-129">สนับสนุนแนวคิดในการปรับปรุง Power BI</span><span class="sxs-lookup"><span data-stu-id="23896-129">Contribute ideas to improve Power BI</span></span>](https://ideas.powerbi.com/)
