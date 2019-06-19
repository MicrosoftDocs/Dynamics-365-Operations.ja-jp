---
title: PowerApps と Microsoft Flow を使用した Talent の拡張 - シナリオ例
description: このトピックでは、Microsoft PowerApps および Microsoft Flow を使用する Microsoft Dynamics 365 for Talent の拡張性シナリオのいくつかの例を説明します。
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: a9ebfd1f2621b8ad65d7623c37b6851cc0b5cb54
ms.sourcegitcommit: ffc37f7c2a63bada3055f37856a30424040bc9a3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/16/2019
ms.locfileid: "1577798"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="6dd3e-103">PowerApps と Microsoft Flow を使用した Talent の拡張 - シナリオ例</span><span class="sxs-lookup"><span data-stu-id="6dd3e-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="6dd3e-104">このトピックでは、Microsoft PowerApps および Microsoft Flow を使用する Microsoft Dynamics 365 for Talent の拡張性シナリオのいくつかの例を説明します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="6dd3e-105">各例に関連付けられているソリューション パッケージを PowerApps 環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="6dd3e-106">次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6dd3e-107">このトピックで説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="6dd3e-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="6dd3e-108">Prerequisites</span></span>

- <span data-ttu-id="6dd3e-109">パッケージをインポートするには、ユーザーは**環境メーカー**のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="6dd3e-110">アプリをエクスポートまたはインポートするには、PowerApps プラン 2 ライセンスもしくは PowerApps プラン 2 試用版ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="6dd3e-111">フロー – フォーム コネクト</span><span class="sxs-lookup"><span data-stu-id="6dd3e-111">Flow – Form Connect</span></span>

<span data-ttu-id="6dd3e-112">**フロー – フォーム コネクト** テンプレートは、Microsoft Forms からデータを読み込み、それを Common Data Service エンティティに格納することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="6dd3e-113">このテンプレートは、他のシナリオに使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="6dd3e-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-114">Here are some examples:</span></span>

- <span data-ttu-id="6dd3e-115">候補評価をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="6dd3e-116">コースのアンケート結果をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="6dd3e-117">人事管理 (HR) の管理者向けの面接質問のライブラリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="6dd3e-118">面接プロセスの候補者の評価をキャプチャします</span><span class="sxs-lookup"><span data-stu-id="6dd3e-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="6dd3e-119">Microsoft Dynamics 365: Attract では、フォームが候補者のポータルに表示され、候補者は詳細を記入することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="6dd3e-120">フォームは、職務テンプレートに活動としても埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="6dd3e-121">候補者がフォームを送信すると、Microsoft Flow はフォーム送信をキャプチャし、データを読み込み、Common Data Service エンティティに格納します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="6dd3e-122">**フロー – フォーム コネクト** テンプレートおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [フロー – フォーム コネクト](https://go.microsoft.com/fwlink/?linkid=2081988) に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="6dd3e-123">Powerapps に渡されたパラメーターの開始と抽出</span><span class="sxs-lookup"><span data-stu-id="6dd3e-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="6dd3e-124">**Powerapps に渡されたパラメーターの開始と抽出**テンプレートは、Attract に固有のあらゆる PowerApps シナリオの開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="6dd3e-125">**求人応募**、**候補者 ID**、および**JobID** など、Attract によって渡されたすべての既定のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="6dd3e-126">このテンプレートを使用して候補者評価フォームを取得し、候補者が記入した評価を採用マネージャーが表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="6dd3e-127">PowerApps を使用して作成されたアプリケーションは、Attract の職務テンプレートに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="6dd3e-128">**Powerapps に渡されるパラメーターの開始および抽出**テンプレートおよびカスタム エンティティの構造をダウンロードするには、Microsoft ダウンロード センターの [Powerapps に渡されるパラメーターの開始および抽出](https://go.microsoft.com/fwlink/?linkid=2081991)に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="6dd3e-129">Office 365 との統合</span><span class="sxs-lookup"><span data-stu-id="6dd3e-129">Integration with Office 365</span></span>

<span data-ttu-id="6dd3e-130">**Office 365 との統合**アプリケーションを使用して、Microsoft Office 365 からサインイン ユーザーのチーム情報を抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="6dd3e-131">出勤、退勤の詳細および例外の記録を抽出するために、Talent の従業員を参照します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="6dd3e-132">出勤および退勤の詳細は、カスタム Common Data Service エンティティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="6dd3e-133">これらの詳細は、統合によってサードパーティ製システムから入力されることを前提とします。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="6dd3e-134">このアプリケーションは、他のシナリオに使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="6dd3e-135">たとえば、チームの休暇情報、カレンダーのイベント、およびそのチーム固有のイベントを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="6dd3e-136">**Office 365 との統合**アプリケーションおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [Office 365 との統合](https://go.microsoft.com/fwlink/?linkid=2081787)に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="6dd3e-137">フロー – 電子メール通知</span><span class="sxs-lookup"><span data-stu-id="6dd3e-137">Flow – Email Notification</span></span>

<span data-ttu-id="6dd3e-138">**フロー – 電子メール通知**テンプレートは電子メール通知のシナリオに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="6dd3e-139">採用プロセスのどの段階でも、採用チームが拒否した候補者への通知電子メールをトリガーするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="6dd3e-140">このテンプレートを拡張して、採用プロセス全体を通して候補者ステージの変更を追跡し、採用チームと候補者に通知を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="6dd3e-141">一般に、Common Data Service に格納されているエンティティの場合、Core HR、Attract、または Dynamics 365 Talent: Onboard で発生したイベントに関する通知を送信するようにフローを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="6dd3e-142">**フロー – 電子メール通知**テンプレートをダウンロードするには、Microsoft ダウンロード センターの [フロー – 電子メール通知](https://go.microsoft.com/fwlink/?linkid=2082103) に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="6dd3e-143">フロー – SQL 接続と実行</span><span class="sxs-lookup"><span data-stu-id="6dd3e-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="6dd3e-144">**フロー – SQL 接続と実行**テンプレートを Microsoft SQL Server に接続し、SQL クエリを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="6dd3e-145">このテンプレートは SQL テーブルの読み取りと更新のために設計されていますが、他のシナリオでも使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="6dd3e-146">たとえば、Common Data Service のステージング テーブルに SQL Server のレコードを入力したり、SQL Server からの増分プッシュを使用してステージング テーブルを定期的に同期するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="6dd3e-147">**フロー – SQL 接続と実行**テンプレートをダウンロードするには、Microsoft ダウンロード センターの [フロー – SQL 接続と実行](https://go.microsoft.com/fwlink/?linkid=2081789) に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="6dd3e-148">フロー – SharePoint 統合</span><span class="sxs-lookup"><span data-stu-id="6dd3e-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="6dd3e-149">**フロー – SharePoint 統合** テンプレートを使用すると、Microsoft SharePoint リストからデータを読み取り、そのリストを Common Data Service エンティティのフィールド値と比較し、その比較結果を通知電子メールとして送信できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="6dd3e-150">組織では、一連のスキルが緊急に必要とされることがあるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="6dd3e-151">これらのスキルは、SharePoint に SharePoint リストとして格納できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="6dd3e-152">候補者が一連の必要なスキルがリストされている仕事に応募するときに、候補者のスキルと SharePoint に格納されているスキルに顕著な一致が見られる場合は、通知電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="6dd3e-153">このように通知があることで、採用担当者は候補者と連絡を取ったり組織全体を通して採用することができるので、緊急に必要とされるポジションはより迅速に埋められます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="6dd3e-154">このテンプレートは、SharePoint 統合を含むあらゆるシナリオで使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="6dd3e-155">**フロー – SharePoint 統合** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [フロー – SharePoint 統合](https://go.microsoft.com/fwlink/?linkid=2082109) に移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="6dd3e-156">人材プールの管理するための管理コンソール</span><span class="sxs-lookup"><span data-stu-id="6dd3e-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="6dd3e-157">LinkedIn との統合を有効にすると、自動的に LinkedIn の人材プールを作成します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="6dd3e-158">採用担当者は LinkedIn を介して InMail を新入社員と交換すると、新入社員にはプロファイルが作成され、Llinkedin 人材プールのメンバーとなります。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="6dd3e-159">この PowerApps アプリは、スキルに基づいて人材プールの候補者を再編成する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="6dd3e-160">次のタスクを実行するには、この PowerApps アプリを管理コンソールとして実行します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="6dd3e-161">人材プールに候補者をリスト</span><span class="sxs-lookup"><span data-stu-id="6dd3e-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="6dd3e-162">人材プールから候補者を追加および削除</span><span class="sxs-lookup"><span data-stu-id="6dd3e-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="6dd3e-163">候補者を別のプールへ移動</span><span class="sxs-lookup"><span data-stu-id="6dd3e-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="6dd3e-164">候補者を移動する前に、その候補者が人材プールの一部であるかどうかを判断</span><span class="sxs-lookup"><span data-stu-id="6dd3e-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="6dd3e-165">別の人材プールに移動する前に、その候補者のスキルを確認</span><span class="sxs-lookup"><span data-stu-id="6dd3e-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="6dd3e-166">この PowerApps アプリは多対多リレーションシップを使用するため、多対多リレーションシップを持つレコードを抽出する必要がある他のシナリオのテンプレートとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="6dd3e-167">**人材プールを扱う管理コンソール**テンプレートをダウンロードするには、Microsoft Download Center で[人材プールを扱う管理コンソール](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) へ移動します。</span><span class="sxs-lookup"><span data-stu-id="6dd3e-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](https://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6dd3e-168">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6dd3e-168">Additional resources</span></span>

[<span data-ttu-id="6dd3e-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="6dd3e-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="6dd3e-170">テナントと環境間でのアプリケーションの移行</span><span class="sxs-lookup"><span data-stu-id="6dd3e-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
