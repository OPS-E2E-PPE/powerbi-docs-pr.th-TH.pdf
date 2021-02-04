---
ms.openlocfilehash: ea958349988cade1045e80b073254ab1f29bbe9e
ms.sourcegitcommit: 60dad5aa0d85db790553e537bf8ac34ee3289ba3
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/29/2019
ms.locfileid: "61264074"
---
<span data-ttu-id="984ec-101">ในหัวข้อก่อนหน้า เราได้ดูเกี่ยวกับวิธีที่คุณสามารถใช้ Power BI ในการเชื่อมต่อแหล่งข้อมูล และวิธีรีเฟรชชุดข้อมูลด้วยตนเองในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="984ec-101">In previous topics we've looked at how you can use Power BI to connect to data sources, and how to manually refresh your datasets on the Power BI service.</span></span> <span data-ttu-id="984ec-102">อย่างไรก็ตาม คุณไม่จำเป็นต้องรีเฟรชด้วยตนเองทุกครั้งที่มีการเปลี่ยนแปลงข้อมูลของคุณ ดังนั้นคุณจึงสามารถใช้ Power BI ในการตั้งค่าการรีเฟรชตามกำหนดการซึ่งจะเชื่อมต่อกับแหล่งข้อมูลของคุณ และเผยแพร่ลงในบริการของ Power BI โดยอัตโนมัติ</span><span class="sxs-lookup"><span data-stu-id="984ec-102">However, you're not going to want to manually refresh things every time your data changes, so you can use Power BI to set up a scheduled refresh that will connect to your data sources and publish them into the Power BI Service automatically.</span></span> <span data-ttu-id="984ec-103">นอกจากนี้ยังช่วยให้คุณสามารถเชื่อมต่อบริการกับแหล่งข้อมูลในองค์กร รวมถึงไฟล์ Excel, ฐานข้อมูล Access, ฐานข้อมูล SQL และอื่นๆ</span><span class="sxs-lookup"><span data-stu-id="984ec-103">This also gives you a way to connect the service with any on-premises data sources, including Excel files, Access databases, SQL databases, and more.</span></span>

<span data-ttu-id="984ec-104">ระบบที่ช่วยให้คุณสามารถเชื่อมต่อแหล่งข้อมูลในองค์กรของคุณกับบริการของ Power BI ได้เรียกว่า **เกตเวย์ข้อมูล**</span><span class="sxs-lookup"><span data-stu-id="984ec-104">The system that lets you connect your on-premises data sources to the Power BI service is called the **data gateway**.</span></span> <span data-ttu-id="984ec-105">ซึ่งเป็นแอปพลิเคชันขนาดเล็กที่ทำงานบนคอมพิวเตอร์ของคุณ และใช้กำหนดการที่จัดเรียงไว้ล่วงหน้าในการเชื่อมต่อกับข้อมูลของคุณ รวบรวมการอัปเดต และนำไปไว้ในบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="984ec-105">It's a small application that runs on your computer, and uses a pre-arranged schedule to connect to your data, gather any updates, and push them up to the Power BI service.</span></span> <span data-ttu-id="984ec-106">**Personal Gateway** คือ**เกตเวย์ข้อมูล**เวอร์ชันที่สามารถใช้โดยไม่ต้องมีการกำหนดค่าของผู้ดูแล</span><span class="sxs-lookup"><span data-stu-id="984ec-106">The **personal gateway** is a version of the **data gateway** that can be used without any administrator configuration.</span></span>

>[!NOTE]
><span data-ttu-id="984ec-107">คอมพิวเตอร์ที่เรียกใช้ Power BI Personal Gateway *ต้อง*เปิดใช้งาน และเชื่อมต่อกับอินเทอร์เน็ตเพื่อให้ **Personal Gateway** ทำงานได้อย่างถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="984ec-107">The computer  that is running the Power BI personal gateway *must* be on and connected to the Internet for **personal gateway** to work properly.</span></span>
> 

<span data-ttu-id="984ec-108">เมื่อต้องการตั้งค่า**เกตเวย์ส่วนบุคคล** ก่อนอื่นให้ลงชื่อเข้าใช้บริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="984ec-108">To set up your **personal gateway**, first sign in to the Power BI service.</span></span> <span data-ttu-id="984ec-109">เลือกไอคอน **ดาวน์โหลด** ที่มุมบนขวาของหน้าจอ แล้วเลือก **เกตเวย์ข้อมูล** จากเมนู</span><span class="sxs-lookup"><span data-stu-id="984ec-109">Select the **Download** icon in the top right-hand corner of the screen, and then select **Data Gateways** from the menu.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_1b.png)

<span data-ttu-id="984ec-110">จากนั้นคุณจะถูกนำไปยังเว็บเพจที่คุณสามารถเลือก **Power BI Gateway - Personal** ได้ ตามที่แสดงอยู่ด้านล่าง</span><span class="sxs-lookup"><span data-stu-id="984ec-110">From there you'll be taken to a web page where you can select the **Power BI Gateway - Personal**, as shown below.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_2b.png)

<span data-ttu-id="984ec-111">เรียกใช้แอปพลิเคชันเมื่อเสร็จสิ้นการดาวน์โหลด และดำเนินตัวช่วยสร้างการติดตั้งให้แล้วเสร็จ</span><span class="sxs-lookup"><span data-stu-id="984ec-111">Run the application once it finishes downloading, and complete the installation wizard.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_3a.png)

<span data-ttu-id="984ec-112">จากนั้นคุณจะได้รับพร้อมท์ให้เปิดใช้งานตัวช่วยสร้างการกำหนดค่าเพื่อตั้งค่าเกตเวย์ของคุณ</span><span class="sxs-lookup"><span data-stu-id="984ec-112">You'll then be prompted to launch the configuration wizard to set up your gateway.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_3b.png)

<span data-ttu-id="984ec-113">ระบบจะขอให้คุณลงชื่อเข้าใช้บัญชีบริการของ Power BI ก่อน จากนั้นให้ลงชื่อเข้าใช้บัญชี Windows ของเครื่อง เนื่องจากบริการเกตเวย์จะทำงานภายใต้บัญชีของคุณ</span><span class="sxs-lookup"><span data-stu-id="984ec-113">You'll be asked first to sign in to your Power BI service account, and then to sign in to the machine's Windows account, since the gateway service runs under your account.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_3c.png)

<span data-ttu-id="984ec-114">กลับไปยังบริการของ Power BI</span><span class="sxs-lookup"><span data-stu-id="984ec-114">Return to the Power BI service.</span></span> <span data-ttu-id="984ec-115">เลือกเมนูจุดไข่ปลา (สามจุด) ถัดจากชุดข้อมูลที่คุณต้องการรีเฟรช จากนั้นเลือก **จัดกำหนดการรีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="984ec-115">Select the ellipsis (three dots) menu next to the dataset you want to refresh, and then select **Schedule Refresh**.</span></span> <span data-ttu-id="984ec-116">ซึ่งจะเปิดหน้า **การตั้งค่าการรีเฟรช**</span><span class="sxs-lookup"><span data-stu-id="984ec-116">This opens the **Refresh Settings** page.</span></span> <span data-ttu-id="984ec-117">Power BI ตรวจพบว่าคุณได้ติดตั้ง **Personal Gateway** และบอกสถานะให้คุณทราบ</span><span class="sxs-lookup"><span data-stu-id="984ec-117">Power BI detects that you've installed a **personal gateway**, and lets you know its status.</span></span>

<span data-ttu-id="984ec-118">เลือก **แก้ไขข้อมูลประจำตัว** ถัดจากแต่ละแหล่งข้อมูล และตั้งค่าการรับรองความถูกต้อง</span><span class="sxs-lookup"><span data-stu-id="984ec-118">Select **Edit credentials** next to each applicable data source and set up authentication.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_6.png)

<span data-ttu-id="984ec-119">สุดท้าย ให้ตั้งค่าตัวเลือกภายใต้ **กำหนดตารางเวลาการรีเฟรช** เพื่อเปิดการใช้งานการอัปเดตอัตโนมัติ และตั้งค่าเวลาและความถี่ในการอัปเดต</span><span class="sxs-lookup"><span data-stu-id="984ec-119">Finally, set the options under **Schedule Refresh** to activate automatic updates and set when and how frequently they occur.</span></span>

![](media/4-6-install-configure-personal-gateway/4-6_7.png)

<span data-ttu-id="984ec-120">เท่านี้ก็เรียบร้อย</span><span class="sxs-lookup"><span data-stu-id="984ec-120">And that's it.</span></span> <span data-ttu-id="984ec-121">ตามเวลาที่กำหนดไว้ Power BI จะไปยังแหล่งข้อมูลเหล่านั้น โดยใช้ข้อมูลประจำตัวที่คุณให้และการเชื่อมต่อกับคอมพิวเตอร์ที่เรียกใช้ **Personal Gateway** ของคุณ และอัปเดตรายงานและชุดข้อมูลตามกำหนดการของคุณ</span><span class="sxs-lookup"><span data-stu-id="984ec-121">On the scheduled times, Power BI will go out to those data sources, using the credentials you provided and the connection to the computer that has your **personal gateway** running, and update the reports and datasets according to your schedule.</span></span> <span data-ttu-id="984ec-122">ในครั้งถัดไปที่คุณไปที่ Power BI แดชบอร์ด รายงาน และชุดข้อมูลเหล่านั้นจะแสดงข้อมูลตามการรีเฟรชตามกำหนดการล่าสุด</span><span class="sxs-lookup"><span data-stu-id="984ec-122">The next time you go to Power BI, those dashboards, reports, and datasets will reflect data as of the most recent scheduled refresh.</span></span>

## <a name="next-steps"></a><span data-ttu-id="984ec-123">ขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="984ec-123">Next steps</span></span>
<span data-ttu-id="984ec-124">**ยินดีด้วย!**</span><span class="sxs-lookup"><span data-stu-id="984ec-124">**Congratulations!**</span></span> <span data-ttu-id="984ec-125">คุณได้ทำส่วน **การสำรวจข้อมูล** ของหลักสูตร **การเรียนรู้พร้อมคำแนะนำ** สำหรับ Power BI เสร็จเรียบร้อยแล้ว</span><span class="sxs-lookup"><span data-stu-id="984ec-125">You've completed this **Exploring Data** section of the **Guided Learning** course for Power BI.</span></span> <span data-ttu-id="984ec-126">บริการของ Power BI เต็มไปด้วยวิธีที่น่าสนใจในการสำรวจข้อมูล แชร์ข้อมูลเชิงลึก และโต้ตอบกับภาพ</span><span class="sxs-lookup"><span data-stu-id="984ec-126">The Power BI service is full of interesting ways to explore data, share insights, and interact with visuals.</span></span> <span data-ttu-id="984ec-127">และทั้งหมดนั้นสามารถเข้าถึงได้จากเบราว์เซอร์ จากบริการที่คุณเชื่อมต่อได้จากทุกที่ที่คุณไป</span><span class="sxs-lookup"><span data-stu-id="984ec-127">And it's all accessible from a browser, from a service that you can connect to wherever you are.</span></span>

<span data-ttu-id="984ec-128">คู่หูที่มีประสิทธิภาพและเป็นที่รู้จักของ Power BI คือ **Excel**</span><span class="sxs-lookup"><span data-stu-id="984ec-128">One powerful and well-known partner of Power BI is **Excel**.</span></span> <span data-ttu-id="984ec-129">Power BI และ Excel ได้รับการออกแบบให้ทำงานร่วมกันได้ดี เวิร์กบุ๊กของคุณจะมีลักษณะเหมือนเดิมใน Power BI และสามารถนำเวิร์กบุ๊กไปที่นั่นได้อย่างง่ายดาย</span><span class="sxs-lookup"><span data-stu-id="984ec-129">Power BI and Excel are designed to work well together; your workbooks will feel at home in Power BI, and it's easy to get them there.</span></span>

![](media/4-6-install-configure-personal-gateway/5-1_1.png)

<span data-ttu-id="984ec-130">ง่ายดายเพียงใดหรือ</span><span class="sxs-lookup"><span data-stu-id="984ec-130">How easy?</span></span> <span data-ttu-id="984ec-131">คุณจะได้คำตอบนั้นในส่วนถัดไป **Power BI และ Excel**</span><span class="sxs-lookup"><span data-stu-id="984ec-131">In the next section, **Power BI and Excel** you learn exactly that.</span></span>

<span data-ttu-id="984ec-132">เจอกันในส่วนถัดไป!</span><span class="sxs-lookup"><span data-stu-id="984ec-132">See you in the next section!</span></span>

