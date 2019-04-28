---
title: PowerApps と Microsoft Flow を使用した Talent の拡張 - シナリオ例
description: このトピックでは、Microsoft PowerApps および Microsoft Flow を使用する Microsoft Dynamics 365 for Talent の拡張性シナリオのいくつかの例を説明します。
author: negudava
manager: Annbe
ms.date: 03/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 0aa3578047b9397682a7039d0dbcc05cc1b167e4
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "949923"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="c2134-103">PowerApps と Microsoft Flow を使用した Talent の拡張 - シナリオ例</span><span class="sxs-lookup"><span data-stu-id="c2134-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="c2134-104">このトピックでは、Microsoft PowerApps および Microsoft Flow を使用する Microsoft Dynamics 365 for Talent の拡張性シナリオのいくつかの例を説明します。</span><span class="sxs-lookup"><span data-stu-id="c2134-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="c2134-105">各例に関連付けられているソリューション パッケージを PowerApps 環境にインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="c2134-106">次に、そのパッケージをガイダンスもしくは組織に適用できるシナリオを実装するための開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2134-107">このトピックで説明されているテンプレートおよびアプリを「そのまま」使用する場合は、それらをテストして、実装に固有のすべてのシナリオをカバーしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c2134-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="c2134-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="c2134-108">Prerequisites</span></span>

- <span data-ttu-id="c2134-109">パッケージをインポートするには、ユーザーは**環境メーカー**のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="c2134-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="c2134-110">アプリをエクスポートまたはインポートするには、PowerApps プラン 2 ライセンスもしくは PowerApps プラン 2 試用版ライセンスが必要です。</span><span class="sxs-lookup"><span data-stu-id="c2134-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="c2134-111">フロー – フォーム コネクト</span><span class="sxs-lookup"><span data-stu-id="c2134-111">Flow – Form Connect</span></span>

<span data-ttu-id="c2134-112">**フロー – フォーム コネクト** テンプレートは、Microsoft Forms からデータを読み込み、それを Common Data Service エンティティに格納することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="c2134-113">このテンプレートは、他のシナリオに使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="c2134-114">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="c2134-114">Here are some examples:</span></span>

- <span data-ttu-id="c2134-115">候補評価をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="c2134-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="c2134-116">コースのアンケート結果をキャプチャします。</span><span class="sxs-lookup"><span data-stu-id="c2134-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="c2134-117">人事管理 (HR) の管理者向けの面接質問のライブラリを作成します。</span><span class="sxs-lookup"><span data-stu-id="c2134-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="c2134-118">面接プロセスの候補者の評価をキャプチャします</span><span class="sxs-lookup"><span data-stu-id="c2134-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="c2134-119">Microsoft Dynamics 365: Attract では、フォームが候補者のポータルに表示され、候補者は詳細を記入することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="c2134-120">フォームは、職務テンプレートに活動としても埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="c2134-121">候補者がフォームを送信すると、Microsoft Flow はフォーム送信をキャプチャし、データを読み込み、Common Data Service エンティティに格納します。</span><span class="sxs-lookup"><span data-stu-id="c2134-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="c2134-122">**フロー – フォーム コネクト** テンプレートおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [フロー – フォーム コネクト](https://go.microsoft.com/fwlink/?linkid=2081988) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2134-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="c2134-123">Powerapps に渡されたパラメーターの開始と抽出</span><span class="sxs-lookup"><span data-stu-id="c2134-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="c2134-124">**Powerapps に渡されたパラメーターの開始と抽出**テンプレートは、Attract に固有のあらゆる PowerApps シナリオの開始点として使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="c2134-125">**求人応募**、**候補者 ID**、および**JobID** など、Attract によって渡されたすべての既定のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c2134-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="c2134-126">このテンプレートを使用して候補者評価フォームを取得し、候補者が記入した評価を採用マネージャーが表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c2134-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="c2134-127">PowerApps を使用して作成されたアプリケーションは、Attract の職務テンプレートに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="c2134-128">**Powerapps に渡されるパラメーターの開始および抽出**テンプレートおよびカスタム エンティティの構造をダウンロードするには、Microsoft ダウンロード センターの [Powerapps に渡されるパラメーターの開始および抽出](https://go.microsoft.com/fwlink/?linkid=2081991)に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2134-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="c2134-129">Office 365 との統合</span><span class="sxs-lookup"><span data-stu-id="c2134-129">Integration with Office 365</span></span>

<span data-ttu-id="c2134-130">**Office 365 との統合**アプリケーションを使用して、Microsoft Office 365 からサインイン ユーザーのチーム情報を抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="c2134-131">出勤、退勤の詳細および例外の記録を抽出するために、Talent の従業員を参照します。</span><span class="sxs-lookup"><span data-stu-id="c2134-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="c2134-132">出勤および退勤の詳細は、カスタム Common Data Service エンティティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c2134-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="c2134-133">これらの詳細は、統合によってサードパーティ製システムから入力されることを前提とします。</span><span class="sxs-lookup"><span data-stu-id="c2134-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="c2134-134">このアプリケーションは、他のシナリオに使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="c2134-135">たとえば、チームの休暇情報、カレンダーのイベント、およびそのチーム固有のイベントを表示するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="c2134-136">**Office 365 との統合**アプリケーションおよびカスタム エンティティ構造をダウンロードするには、Microsoft ダウンロード センターの [Office 365 との統合](https://go.microsoft.com/fwlink/?linkid=2081787)に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2134-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="c2134-137">フロー – 電子メール通知</span><span class="sxs-lookup"><span data-stu-id="c2134-137">Flow – Email Notification</span></span>

<span data-ttu-id="c2134-138">**フロー – 電子メール通知**テンプレートは電子メール通知のシナリオに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="c2134-139">採用プロセスのどの段階でも、採用チームが拒否した候補者への通知電子メールをトリガーするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="c2134-140">このテンプレートを拡張して、採用プロセス全体を通して候補者ステージの変更を追跡し、採用チームと候補者に通知を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="c2134-141">一般に、Common Data Service に格納されているエンティティの場合、Core HR、Attract、または Dynamics 365 Talent: Onboard で発生したイベントに関する通知を送信するようにフローを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="c2134-142">**フロー – 電子メール通知**テンプレートをダウンロードするには、Microsoft ダウンロード センターの [フロー – 電子メール通知](https://go.microsoft.com/fwlink/?linkid=2082103) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2134-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="c2134-143">フロー – SQL 接続と実行</span><span class="sxs-lookup"><span data-stu-id="c2134-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="c2134-144">**フロー – SQL 接続と実行**テンプレートを Microsoft SQL Server に接続し、SQL クエリを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c2134-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="c2134-145">このテンプレートは SQL テーブルの読み取りと更新のために設計されていますが、他のシナリオでも使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="c2134-146">たとえば、Common Data Service のステージング テーブルに SQL Server のレコードを入力したり、SQL Server からの増分プッシュを使用してステージング テーブルを定期的に同期するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="c2134-147">**フロー – SQL 接続と実行**テンプレートをダウンロードするには、Microsoft ダウンロード センターの [フロー – SQL 接続と実行](https://go.microsoft.com/fwlink/?linkid=2081789) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2134-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="c2134-148">フロー – SharePoint 統合</span><span class="sxs-lookup"><span data-stu-id="c2134-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="c2134-149">**フロー – SharePoint 統合** テンプレートを使用すると、Microsoft SharePoint リストからデータを読み取り、そのリストを Common Data Service エンティティのフィールド値と比較し、その比較結果を通知電子メールとして送信できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="c2134-150">組織では、一連のスキルが緊急に必要とされることがあるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="c2134-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="c2134-151">これらのスキルは、SharePoint に SharePoint リストとして格納できます。</span><span class="sxs-lookup"><span data-stu-id="c2134-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="c2134-152">候補者が一連の必要なスキルがリストされている仕事に応募するときに、候補者のスキルと SharePoint に格納されているスキルに顕著な一致が見られる場合は、通知電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="c2134-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="c2134-153">このように通知があることで、採用担当者は候補者と連絡を取ったり組織全体を通して採用することができるので、緊急に必要とされるポジションはより迅速に埋められます。</span><span class="sxs-lookup"><span data-stu-id="c2134-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="c2134-154">このテンプレートは、SharePoint 統合を含むあらゆるシナリオで使用できるように拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="c2134-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="c2134-155">**フロー – SharePoint 統合** テンプレートをダウンロードするには、Microsoft ダウンロード センターの [フロー – SharePoint 統合](https://go.microsoft.com/fwlink/?linkid=2082109) に移動します。</span><span class="sxs-lookup"><span data-stu-id="c2134-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="c2134-156">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c2134-156">Additional resources</span></span>

[<span data-ttu-id="c2134-157">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="c2134-157">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="c2134-158">テナントと環境間でのアプリケーションの移行</span><span class="sxs-lookup"><span data-stu-id="c2134-158">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
