---
title: Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合に関する FAQ
description: このトピックでは、Talent および Finance and Operations の統合でどのデータが同期されるのかについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 438c2b5689e450b9aae9c55168993f2ee84be4d5
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "950086"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a><span data-ttu-id="74f03-103">Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="74f03-103">Dynamics 365 for Talent to Dynamics 365 for Finance and Operations integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74f03-104">このトピックでは、Dynamics 365 for Talent が Dynamics 365 for Finance and Operations に統合される際にどのデータが同期されるかに関連した一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="74f03-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 for Talent is integrated with Dynamics 365 for Finance and Operations.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="74f03-105">すべてのデータが同期された、または一部のデータ エンティティだけが同期されましたか。</span><span class="sxs-lookup"><span data-stu-id="74f03-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="74f03-106">Core Human Resources (HR) で、データのサブセットが同期されます。</span><span class="sxs-lookup"><span data-stu-id="74f03-106">With Core Human Resources (HR), a subset of the data is synchronized.</span></span> <span data-ttu-id="74f03-107">すべてのエンティティの一覧については、「[Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合](talent-financeandoperations-integration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74f03-107">For a list of all the entities, see [Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="74f03-108">Attract および Onboard に関しては、すべてのデータが Common Data Service にネイティブです。</span><span class="sxs-lookup"><span data-stu-id="74f03-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="74f03-109">テンプレートを使用せずに新しいマップを作成できますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="74f03-110">テンプレートは、開始点です。</span><span class="sxs-lookup"><span data-stu-id="74f03-110">Templates are the starting point.</span></span> <span data-ttu-id="74f03-111">独自のテンプレートを作成できますが、テンプレートは統合プロジェクトを作成する際に常に必要です。</span><span class="sxs-lookup"><span data-stu-id="74f03-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="74f03-112">データ統合 (DI)、テンプレート、およびプロジェクトの詳細については、「[Common Data Service へデータを統合](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74f03-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a><span data-ttu-id="74f03-113">Talent および Finance and Operations 間で転送する財務分析コードをマップできますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-113">Can I map financial dimensions to transfer between Talent and Finance and Operations?</span></span>

<span data-ttu-id="74f03-114">財務分析コードは、現在 Common Data Service にはなく、結果として既定のテンプレートの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="74f03-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="74f03-115">このエンティティは計画されていますが、現在利用可能なリリース タイムラインはありません。</span><span class="sxs-lookup"><span data-stu-id="74f03-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="74f03-116">Finance and Operations で存在しますが、Talent では存在しないデータに関しては、Talent の**リンクの構成**を使用して 2 つのシステムを相互にリンクします。</span><span class="sxs-lookup"><span data-stu-id="74f03-116">For data that resides in Finance and Operations but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="74f03-117">Talent および Finance and Operations 間のリンクを構成する方法の詳細については、「[Dynamics 365 for Talent Core HR (2018 年 10月 31日) の新機能および変更された機能](whats-new-talent-october-31.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74f03-117">For more information about how to configure links between Talent and Finance and Operations, see [What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a><span data-ttu-id="74f03-118">場合によっては、従業員をインポートする場合 Finance and Operations の無効な作業者に入ってしまいます。</span><span class="sxs-lookup"><span data-stu-id="74f03-118">Sometimes when I import employees, they go into inactive workers in Finance and Operations.</span></span> <span data-ttu-id="74f03-119">なぜですか。</span><span class="sxs-lookup"><span data-stu-id="74f03-119">Why?</span></span>

<span data-ttu-id="74f03-120">従業員が Talent に有効な雇用詳細レコードがない場合、このエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-120">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="74f03-121">この問題を解決するには、**人事管理 \> 従業員 \> 雇用履歴 \> 日付マネージャー**に移動し、有効な雇用詳細レコードがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-121">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="74f03-122">フィールドのサブセットのみをマップする選択をする場合、非マップ フィールドに対して加えた変更は同期をトリガーしますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-122">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="74f03-123">データ同期は、実行スケジュールに従います。</span><span class="sxs-lookup"><span data-stu-id="74f03-123">Data sync follows the execution schedule.</span></span> <span data-ttu-id="74f03-124">このフィールドが統合マッピングの一部であるかどうかにかかわらず、レコードの任意のフィールドが変更されると、統合はレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="74f03-124">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="74f03-125">有効な作業者のみの変更を送信し、終了したレコードを送信しないためにはどうしますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-125">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="74f03-126">「高度なクエリ」を使用して、ソースデータを送信先に渡す前に、フィルター処理して再作成できます。</span><span class="sxs-lookup"><span data-stu-id="74f03-126">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a><span data-ttu-id="74f03-127">特定のエンティティの Finance and Operations に送信するフィールドを指定できますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-127">Can I specify which fields to send to Finance and Operations for a specific entity?</span></span>

<span data-ttu-id="74f03-128">フィールドは、統合タスクから追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="74f03-128">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="74f03-129">Common Data Service エンティティに存在するすべてのデータ フィールドが、Core HR から入力されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="74f03-129">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="74f03-130">追加のデータは、PowerApps 経由で入力されます。</span><span class="sxs-lookup"><span data-stu-id="74f03-130">Additional data can be populated via PowerApps.</span></span>

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="74f03-131">バッチ ジョブとしての統合を設定しましたが、Talent は宛先システムへの接続を失いました。</span><span class="sxs-lookup"><span data-stu-id="74f03-131">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="74f03-132">宛先システムに同じ一連の変更をどのように送信しますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-132">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="74f03-133">例外処理の特別なセットアップは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="74f03-133">No special setup is required for exception handling.</span></span> <span data-ttu-id="74f03-134">データ統合は自動的にソースと宛先で発生したエラーを検出して報告し、手動での再試行を許可します。</span><span class="sxs-lookup"><span data-stu-id="74f03-134">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="74f03-135">ただし、手動でのデータ修正は許可しません。</span><span class="sxs-lookup"><span data-stu-id="74f03-135">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="74f03-136">データの更新が必要な場合、ソースまたは宛先のいずれかで発生します。</span><span class="sxs-lookup"><span data-stu-id="74f03-136">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="74f03-137">双方向の統合を設定できますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-137">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="74f03-138">いいえ、統合は現在一方向です (Talent から Finance and Operations)。</span><span class="sxs-lookup"><span data-stu-id="74f03-138">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="74f03-139">ただし、Talent から Finance and Operations にデータを送信可能な既定のテンプレートがあります。</span><span class="sxs-lookup"><span data-stu-id="74f03-139">However, there is a default template available to send data from Talent to Finance and Operations.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="74f03-140">自分の統合の一部として、レコードの削除を許可できますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-140">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="74f03-141">いいえ、データ統合は、データ転送の削除したレコードをキャプチャしません。</span><span class="sxs-lookup"><span data-stu-id="74f03-141">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="74f03-142">データ作成と更新 (UPSERT) のみが現在含まれます。</span><span class="sxs-lookup"><span data-stu-id="74f03-142">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="74f03-143">エラーの実行を再実行できますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-143">Can I rerun the errored execution?</span></span> <span data-ttu-id="74f03-144">その場合は、送信されるのは完全なファイルまたは変更のみですか。</span><span class="sxs-lookup"><span data-stu-id="74f03-144">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="74f03-145">データ統合の最初の実行は、常に完全な実行です。</span><span class="sxs-lookup"><span data-stu-id="74f03-145">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="74f03-146">その後の実行は、変更追跡に基づいています。</span><span class="sxs-lookup"><span data-stu-id="74f03-146">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="74f03-147">エラー実行が実行されると、実行のスコープのレコードを抽出し、Common Data Service から最新の変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="74f03-147">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="74f03-148">プロジェクトを保存すると、エラーが発生します:「プロジェクトにはマッピング エラーがあります。」</span><span class="sxs-lookup"><span data-stu-id="74f03-148">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="74f03-149">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="74f03-149">What do I do?</span></span>

<span data-ttu-id="74f03-150">統合キーの設定を確認し、設定に必要などんな変更も加えてから、プロジェクトでエンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="74f03-150">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="74f03-151">既定のテンプレートを使用すると、統合キーは自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="74f03-151">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="74f03-152">この問題は、新しいタスクが既存のテンプレートに追加されたときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-152">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="74f03-153">作業者の雇用がある法人の N 番号がある場合、それぞれに対するマップを作成する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-153">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="74f03-154">はい、Finance and Operations の各法人に対して、データ統合の統合プロジェクトを分ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-154">Yes, for each legal entity in Finance and Operations, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="74f03-155">Microsoft により提供された既定のテンプレートの一部ではないデータを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-155">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="74f03-156">これを実行できますか ?</span><span class="sxs-lookup"><span data-stu-id="74f03-156">Can I do this?</span></span>

<span data-ttu-id="74f03-157">はい、フィールドは既存のテンプレートから追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="74f03-157">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="74f03-158">テンプレートを変更して、他の Common Data Service のエンティティからの追加データを含めます。</span><span class="sxs-lookup"><span data-stu-id="74f03-158">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="74f03-159">エンティティは、テンプレートに含まれる Common Data Service である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-159">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="74f03-160">新しい Finance and Operations、および Talent 環境を作成しましたが、エラーが発生しました。「データ値が、整合性制約に違反しています。」</span><span class="sxs-lookup"><span data-stu-id="74f03-160">I just created new Finance and Operations and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="74f03-161">なぜですか。</span><span class="sxs-lookup"><span data-stu-id="74f03-161">Why?</span></span>

<span data-ttu-id="74f03-162">このエラーが発生する理由には以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="74f03-162">Reasons for this error can include:</span></span>

- <span data-ttu-id="74f03-163">データ転送がなかったため、転送ソース (Common Data Service) で重複レコードの抽出となりました。</span><span class="sxs-lookup"><span data-stu-id="74f03-163">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="74f03-164">データ転送には、Finance and Operations で必要とされるフィールドの null 値があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-164">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="74f03-165">Common Data Service にあり、Finance and Operations の要件を満たすデータを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-165">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="74f03-166">実行エラーがあり従業員 ID が同期しなかった場合、失敗した従業員レコードがある履歴ジョブをどのように見つけますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-166">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="74f03-167">データ統合は、Finance and Operations で複数のプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="74f03-167">Data Integrator will create multiple projects in Finance and Operations.</span></span> <span data-ttu-id="74f03-168">データ統合タスクと Finance and Operations プロジェクトとの関係は、1 対 1 です。</span><span class="sxs-lookup"><span data-stu-id="74f03-168">The relationship between the Data Integrator task and the Finance and Operations project is one to one.</span></span>

<span data-ttu-id="74f03-169">データ統合実行履歴からの時間を追跡し、Finance and Operations でインデックス -1 プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="74f03-169">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance and Operations.</span></span> <span data-ttu-id="74f03-170">データ統合でタスク番号が 9 の場合、Finance and Operations のインデックスは 8 です。</span><span class="sxs-lookup"><span data-stu-id="74f03-170">If the task number is 9 in Data Integrator, the index in Finance and Operations is 8.</span></span>

1. <span data-ttu-id="74f03-171">データ統合からタスク インデックスをキャプチャします (この例では「9」)。</span><span class="sxs-lookup"><span data-stu-id="74f03-171">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![データ統合からタスク インデックスをキャプチャします。](media/CaptureTaskIndex.png)

2. <span data-ttu-id="74f03-173">プロジェクトの実行時間を追跡します。</span><span class="sxs-lookup"><span data-stu-id="74f03-173">Track the execution time of the project.</span></span>

![プロジェクトの実行時間の追跡](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="74f03-175">Finance and Operations で、インデックス - 1 を識別します。</span><span class="sxs-lookup"><span data-stu-id="74f03-175">In Finance and Operations, identify index - 1.</span></span> <span data-ttu-id="74f03-176">この例では、接尾語「8」でインデックス「0」プロジェクトの実行時間を持つプロジェクトは、ステップ 2 の実行時間と一致します。</span><span class="sxs-lookup"><span data-stu-id="74f03-176">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![インデックスの識別](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a><span data-ttu-id="74f03-178">Talent および Finance and Operations を統合した後、Finance and Operations で Talent データが表示されません。</span><span class="sxs-lookup"><span data-stu-id="74f03-178">After integrating Talent and Finance and Operations, I don’t see my Talent data in Finance and Operations.</span></span> <span data-ttu-id="74f03-179">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="74f03-179">What do I do?</span></span>

<span data-ttu-id="74f03-180">Finance and Operations への統合には 2 つのステップがあります。</span><span class="sxs-lookup"><span data-stu-id="74f03-180">The integration to Finance and Operations is a two-step process.</span></span> <span data-ttu-id="74f03-181">まず、Talent データが更新済で、Common Data Service で利用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-181">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="74f03-182">これはほぼリアルタイムの同期であり、データ エンティティ内のデータを参照して PowerApps で検証できます。</span><span class="sxs-lookup"><span data-stu-id="74f03-182">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Common Data Service 内のデータ](media/DataInCDS.png)

<span data-ttu-id="74f03-184">Common Data Service で予定どおりにデータが表示されない場合は、エンティティが統合でサポートされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-184">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="74f03-185">Common Data Service に追加データを含めるには、Microsoft 側で変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="74f03-185">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="74f03-186">エンティティがサポートされデータが Common Data Service で使用できる場合は、データ統合でマッピングが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-186">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="74f03-187">インテグレーター マッピングが正常に見える場合、データ管理ジョブが正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-187">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="74f03-188">バッチ ジョブの実行中にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-188">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="74f03-189">データ管理の詳細については、「[データ管理](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74f03-189">For more information about Data Management, see [Data management](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a><span data-ttu-id="74f03-190">Finance and Operations にインポートした後、従業員の住所が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="74f03-190">The addresses for my employees are incorrect after I import them into Finance and Operations.</span></span> <span data-ttu-id="74f03-191">何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-191">What should I do?</span></span>

<span data-ttu-id="74f03-192">**場所 ID** の番号順序は、Talent および Finance and Operations の両方で同じパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="74f03-192">The number sequence for **Location ID** uses the same pattern in both Talent and Finance and Operations.</span></span> <span data-ttu-id="74f03-193">Common Data Service から Finance and Operations にデータを統合する場合、アドレスの衝突がないように、番号順序は両側で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74f03-193">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="74f03-194">Talent の実装中に、番号順序が Talent および Finance and Operations で同じではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-194">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance and Operations.</span></span> <span data-ttu-id="74f03-195">データが両方のシステムで維持される可能性がある場合は、すべての番号順序が同一でないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="74f03-195">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="74f03-196">接続設定を作成する際に、接続ドロップダウン リストで接続が確認できません。</span><span class="sxs-lookup"><span data-stu-id="74f03-196">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="74f03-197">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="74f03-197">What do I do?</span></span>

<span data-ttu-id="74f03-198">接続を作成するときは、Dynamics 365 for Finance and Operations (現在のプレビュー) および Common Data Service を選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="74f03-198">Make sure when creating your connections, you choose Dynamics 365 for Finance and Operations (currently in preview) and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="74f03-199">雇用を同期する際、エラーが発生します。「CompanyInfo_FK が存在しません」または「フィールド '雇用終了日' の値 '12/31/2154 11:59:59 pm' が、関連するテーブル '雇用' で見つかりません。」何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-199">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="74f03-200">正しい法人にマッピングしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="74f03-200">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="74f03-201">法人の同期は既定のテンプレートの一部ではないため、Talent や Common Data Service に存在する各法人が Finance and Operations にも存在することが予想されます。</span><span class="sxs-lookup"><span data-stu-id="74f03-201">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance and Operations.</span></span>
<span data-ttu-id="74f03-202">また、関連付けられている接続設定に対して正しい法人を選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="74f03-202">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="74f03-203">プロジェクトの設定後、Finance and Operations のフィールド マッピングは空のようです。</span><span class="sxs-lookup"><span data-stu-id="74f03-203">After setting up my project, the field mapping for Finance and Operations appears to be empty.</span></span> <span data-ttu-id="74f03-204">何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="74f03-204">What should I do?</span></span>

<span data-ttu-id="74f03-205">**データ管理 \> フレームワーク パラメーター \> エンティティ設定 \> エンティティ リストの更新**に移動して、Finance and Operations のデータ エンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="74f03-205">Refresh the data entities in Finance and Operations by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="74f03-206">これは数分で完了し、それらのマッピングを表示できます。</span><span class="sxs-lookup"><span data-stu-id="74f03-206">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="74f03-207">新しいプロジェクトが作成されたときに、この問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="74f03-207">This issue occurs when new projects are created.</span></span>

![フィールド マッピングがありません](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="74f03-209">追加リソース</span><span class="sxs-lookup"><span data-stu-id="74f03-209">Additional resources</span></span>

- <span data-ttu-id="74f03-210">データ統合 (DI):</span><span class="sxs-lookup"><span data-stu-id="74f03-210">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="74f03-211">データを Common Data Service に統合</span><span class="sxs-lookup"><span data-stu-id="74f03-211">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="74f03-212">データ統合エラーの管理とトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="74f03-212">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="74f03-213">PowerApps、Microsoft Flow、および Common Data Service でシステムにより生成されたログの DSR 要求への応答</span><span class="sxs-lookup"><span data-stu-id="74f03-213">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="74f03-214">データ管理:</span><span class="sxs-lookup"><span data-stu-id="74f03-214">Data Management:</span></span>

  - [<span data-ttu-id="74f03-215">データ管理</span><span class="sxs-lookup"><span data-stu-id="74f03-215">Data management</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
