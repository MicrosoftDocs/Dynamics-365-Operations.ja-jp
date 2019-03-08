---
title: プロセスの活動
description: このトピックでは、採用プロセスで使用できるさまざまなタイプの活動に関する情報を提供します。
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2019
ms.locfileid: "374760"
---
# <a name="activities-in-the-hiring-processes"></a><span data-ttu-id="c3fa0-103">採用プロセスの活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-103">Activities in the hiring processes</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c3fa0-104">Microsoft Dynamics 365 for Talent: Attract の採用プロセスの一部として活動を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-104">Activities can be added as a part of the hiring process in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="c3fa0-105">活動はプロセス テンプレートに追加することも、ジョブ内の採用プロセスに直接追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-105">Activities can be added to a process template, or they can be added directly to the hiring process in the job.</span></span> <span data-ttu-id="c3fa0-106">ジョブが定義されると、プロセス テンプレートが選択され、テンプレートに含まれている活動がジョブに適用されます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-106">When a job is defined, a process template is selected, and the activities that are included in the template are applied to the job.</span></span> <span data-ttu-id="c3fa0-107">テンプレートが選択されていない場合は、既定のテンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-107">If a template isn't selected, the default template is used.</span></span> <span data-ttu-id="c3fa0-108">採用プロセスは、テンプレートが適用された後にジョブに変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-108">The hiring process can also be modified on the job after the template is applied.</span></span>

> [!NOTE] 
> <span data-ttu-id="c3fa0-109">プロセス テンプレートは、包括採用アドオンで利用できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-109">Process templates are available with the Comprehensive hiring add-on.</span></span>

## <a name="prospect-activity"></a><span data-ttu-id="c3fa0-110">候補者活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-110">Prospect activity</span></span>

<span data-ttu-id="c3fa0-111">候補者活動は、見込顧客をジョブに追加できるかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-111">The Prospect activity controls whether prospects can be added to a job.</span></span> <span data-ttu-id="c3fa0-112">既定値では、見込顧客をジョブに追加できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-112">By default, prospects can be added to a job.</span></span> <span data-ttu-id="c3fa0-113">候補者活動をオフにするには、**候補者の有効化**オプションを**オフ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-113">To turn off the Prospect activity, set the **Enable prospects** option to **Off**.</span></span> <span data-ttu-id="c3fa0-114">候補者活動をオンにすると、採用マネージャーは見込顧客を追加して表示することができ、**候補者**タブがジョブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-114">When the Prospect activity is turned on, hiring managers can add and view prospects, and the **Prospect** tab is shown on the job.</span></span>

## <a name="application-activity"></a><span data-ttu-id="c3fa0-115">アプリケーションの活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-115">Application activity</span></span>

<span data-ttu-id="c3fa0-116">採用プロセス テンプレートにアプリケーションの活動が必要です。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-116">The Application activity is required in the hiring process template.</span></span> <span data-ttu-id="c3fa0-117">申請の提出または申請のステージに追加する際に、候補者に電子メールを送信するには、**候補者に電子メールを送信**オプションを**オン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-117">To send email to candidates when they submit their application or are added to the Application stage, set the **Send mail to candidate** option to **On**.</span></span>

## <a name="interview-schedule-and-feedback-activity"></a><span data-ttu-id="c3fa0-118">面接のスケジュールおよびフィードバック活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-118">Interview schedule and feedback activity</span></span>

<span data-ttu-id="c3fa0-119">この活動には 3 つのコンポーネントがあります: 候補者の面接可能日の要求、スケジュール、およびフィードバックです。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-119">This activity has three components: Candidate availability request, Schedule, and Feedback.</span></span> <span data-ttu-id="c3fa0-120">採用プロセスの一部として個別に使用する代わりに、プロセスの一部として、候補者の面接可能日の要求、スケジュール、およびフィードバックを対象とする場合は、職務テンプレートの面接の活動を使用します。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-120">Use the interview activity in the job template if you want to include the candidate’s availability request, schedule, and feedback as part of the process instead of using them individually as part of the hiring process.</span></span> <span data-ttu-id="c3fa0-121">詳細については、[面接のスケジューリングおよびフィードバック](interview-scheduling-feedback.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-121">For more information, see [Interview scheduling and feedback](interview-scheduling-feedback.md).</span></span>

## <a name="powerapps-activity"></a><span data-ttu-id="c3fa0-122">PowerApps 活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-122">PowerApps activity</span></span>

<span data-ttu-id="c3fa0-123">PowerApps 活動では、Microsoft PowerApps アプリを採用プロセスに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-123">The PowerApps activity lets you embed a Microsoft PowerApps app in your hiring process.</span></span> <span data-ttu-id="c3fa0-124">アプリは、すべての申請者、内部申請者、外部申請者、または申請者には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-124">The app can be required for all applicants, internal applicants only, external applicants only, or no applicants.</span></span> <span data-ttu-id="c3fa0-125">アプリが必要とマークされている場合、ステージを進める前に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-125">If the app is marked as required, it must be completed before the stage can be advanced.</span></span> <span data-ttu-id="c3fa0-126">アプリが必要とマークされていない場合、活動はオプションのステップであり、アプリが完了していなくてもステージを進めることができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-126">If the app isn't marked as required, the activity is an optional step, and the stage can be advanced even if the app isn't completed.</span></span>

<span data-ttu-id="c3fa0-127">PowerApps 活動を採用プロセスに保存するには、PowerApps ID を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-127">To save the PowerApps activity to the hiring process, you must enter a PowerApps ID.</span></span> <span data-ttu-id="c3fa0-128">PowerApps ID を検索するには [PowerApps](https://web.powerapps.com) に移動して、**アプリ**を選択し、**詳細**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-128">To find the PowerApps ID, go to [PowerApps](https://web.powerapps.com), select **Apps**, and then select **Details**.</span></span>

<span data-ttu-id="c3fa0-129">**この活動の参加者の追加を許可**オプションを選択した場合は、PowerApps 活動を使用するアプリケーションの他の要因を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-129">If you select the **Allow adding participants for this activity** option, additional contributors can be added for an application that uses the PowerApps activity.</span></span> <span data-ttu-id="c3fa0-130">たとえば、組織では、技術上の役割に対する面接の質問のライブラリである PowerApps アプリを作成しました。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-130">For example, an organization has created a PowerApps app that is a library of interview questions for technical roles.</span></span> <span data-ttu-id="c3fa0-131">組織では、現在新しいソフトウェア開発者を採用しており、ソフトウェア開発者のロールの採用プロセスに PowerApps 活動が追加されました。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-131">The organization is now hiring a new software developer and has added the PowerApps activity to the hiring process for the Software Developer role.</span></span> <span data-ttu-id="c3fa0-132">**この活動の参加者の追加を許可**オプションが選択されている場合、ソフトウェア開発者のロールの申請者を表示している採用担当者または採用マネージャーが PowerApps 活動に人を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-132">If the **Allow adding participants for this activity** option is selected, a recruiter or hiring manager who is viewing an applicant for the Software Developer role can add people to the PowerApps activity.</span></span> <span data-ttu-id="c3fa0-133">ユーザーは、面接の質問を記載したアプリを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-133">Those people can then view the app that has the interview questions.</span></span>

> [!NOTE]
> <span data-ttu-id="c3fa0-134">PowerApps 活動は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-134">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="youtube-activity"></a><span data-ttu-id="c3fa0-135">YouTube 活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-135">YouTube activity</span></span>

<span data-ttu-id="c3fa0-136">YouTube 活動では、採用プロセスの一環として YouTube ビデオを共有できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-136">The YouTube activity lets you share a YouTube video as part of your hiring process.</span></span> <span data-ttu-id="c3fa0-137">YouTube 活動を採用プロセスに保存するには、YouTube ビデオの URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-137">To save the YouTube activity to the hiring process, you must specify the URL of the YouTube video.</span></span> <span data-ttu-id="c3fa0-138">PowerApps 活動については、参加者が活動に追加するのを許可することができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-138">As for the PowerApps activity, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="c3fa0-139">**候補のみに表示**オプションを選択した場合、ビデオは候補者エクスペリエンスの一部としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-139">If you select the **Show only to candidate** option, the video is shown only as part of the candidate experience.</span></span> <span data-ttu-id="c3fa0-140">これは、Attract の採用プロセスには表示されません。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-140">It isn't shown in the hiring process in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="c3fa0-141">YouTube 活動は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-141">The YouTube activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="web-content-activity"></a><span data-ttu-id="c3fa0-142">Web コンテンツ活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-142">Web content activity</span></span>

<span data-ttu-id="c3fa0-143">Web コンテンツ活動では、オンライン コンテンツを採用プロセスに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-143">The Web content activity lets you embed online content in your hiring process.</span></span> <span data-ttu-id="c3fa0-144">YouTube 活動を採用プロセスに保存するには、コンテンツの URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-144">To save the Web content activity to the hiring process, you must specify the URL of the content.</span></span> <span data-ttu-id="c3fa0-145">PowerApps および YouTube 活動については、参加者が活動に追加するのを許可することができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-145">As for the PowerApps and YouTube activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="c3fa0-146">**候補のみに表示**オプションを選択する場合、コンテンツは候補者エクスペリエンスの一部としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-146">If you select the **Show only to candidate** option, the content is shown only as part of the candidate experience.</span></span> <span data-ttu-id="c3fa0-147">これは、Attract の採用プロセスには表示されません。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-147">It isn't shown in the hiring process in Attract.</span></span> <span data-ttu-id="c3fa0-148">表示されるコンテンツのサイズを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-148">You can select the size of the content that is shown.</span></span>

> [!NOTE]
> <span data-ttu-id="c3fa0-149">Web コンテンツ活動は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-149">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="microsoft-forms-activity"></a><span data-ttu-id="c3fa0-150">Microsoft Forms 活動</span><span class="sxs-lookup"><span data-stu-id="c3fa0-150">Microsoft Forms activity</span></span>

<span data-ttu-id="c3fa0-151">Microsoft Forms 活動では、Microsoft Forms フォームを採用プロセスに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-151">The Microsoft Forms activity lets you embed a Microsoft Forms form in your hiring process.</span></span> <span data-ttu-id="c3fa0-152">Microsoft Forms では、クイズ、アンケート、およびポーリングを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-152">Microsoft Forms lets you create quizzes, surveys, and polls.</span></span> <span data-ttu-id="c3fa0-153">Microsoft Forms 活動を採用プロセスに保存するには、フォームの URL を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-153">To save the Microsoft Forms activity to the hiring process, you must specify of the URL of the form.</span></span> <span data-ttu-id="c3fa0-154">PowerApps、YouTube、および Web コンテンツ活動については、参加者が活動に追加するのを許可することができます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-154">As for the PowerApps, YouTube, and Web content activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="c3fa0-155">**候補のみに表示**オプションを選択する場合、フォームは候補者エクスペリエンスの一部としてのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-155">If you select the **Show only to candidate** option, the form is shown only as part of the candidate experience.</span></span> <span data-ttu-id="c3fa0-156">これは、Attract の採用プロセスには表示されません。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-156">It isn't shown in the hiring process in Attract.</span></span>

<span data-ttu-id="c3fa0-157">Microsoft Forms では、組織外のユーザーがアンケートやクイズに応答できるように設定を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-157">In Microsoft Forms, authors can change their settings to let users outside their organization respond to their survey or quiz.</span></span> <span data-ttu-id="c3fa0-158">この場合、ユーザーは応答を匿名で送信します。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-158">In this case, users submit responses anonymously.</span></span> <span data-ttu-id="c3fa0-159">アンケートやクイズに誰が記入したのかを見たい場合は、アンケートやクイズの一部として回答者に名前を入力することを要求できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-159">If you want to see who has filled out your survey or quiz, you can require that respondents enter their names as part of the survey or quiz.</span></span>

> [!NOTE]
> <span data-ttu-id="c3fa0-160">Microsoft Forms 活動は、包括採用アドオンでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c3fa0-160">The Microsoft Forms activity is available only with the Comprehensive hiring add-on.</span></span>
