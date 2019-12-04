---
title: Dynamics 365 Talent から Dynamics 365 Finance への統合に関する FAQ
description: このトピックでは、Talent および Finance の統合でどのデータが同期されるのかについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 10/14/2019
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
ms.openlocfilehash: 747922294eaf971795177beeb73839d453f6475a
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830189"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="546fa-103">Dynamics 365 Talent から Dynamics 365 Finance への統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="546fa-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="546fa-104">このトピックでは、Dynamics 365 Talent が Dynamics 365 Finance に統合される際にどのデータが同期されるかに関連した一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="546fa-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="546fa-105">すべてのデータが同期された、または一部のデータ エンティティだけが同期されましたか。</span><span class="sxs-lookup"><span data-stu-id="546fa-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="546fa-106">Core HR に関しては、データのサブセットが同期されます。</span><span class="sxs-lookup"><span data-stu-id="546fa-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="546fa-107">すべてのエンティティの一覧については、「[Dynamics 365 Talent から Dynamics 365 Finance への統合](talent-financeandoperations-integration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="546fa-108">Attract および Onboard に関しては、すべてのデータが Common Data Service にネイティブです。</span><span class="sxs-lookup"><span data-stu-id="546fa-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="546fa-109">Common Data Service に同期されたデータを表示できないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="546fa-109">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="546fa-110">既定では、Common Data Service の統合は、提供されているデモ データが含まれていない新しい環境ではオフになっています。</span><span class="sxs-lookup"><span data-stu-id="546fa-110">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="546fa-111">既定では、デモ データが含まれている新しい環境ではオンになっており、環境の準備時にデータの同期が開始されます。</span><span class="sxs-lookup"><span data-stu-id="546fa-111">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="546fa-112">データと同期する準備が整ったら、統合をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="546fa-112">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="546fa-113">詳細については、[Common Data Service 統合のコンフィギュレーション](hr-common-data-service-integration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-113">For more information, see [Configure Common Data Service integration](hr-common-data-service-integration.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="546fa-114">テンプレートを使用せずに新しいマップを作成できますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-114">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="546fa-115">テンプレートは、開始点です。</span><span class="sxs-lookup"><span data-stu-id="546fa-115">Templates are the starting point.</span></span> <span data-ttu-id="546fa-116">独自のテンプレートを作成できますが、テンプレートは統合プロジェクトを作成する際に常に必要です。</span><span class="sxs-lookup"><span data-stu-id="546fa-116">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="546fa-117">データ統合 (DI)、テンプレート、およびプロジェクトの詳細については、「[Common Data Service へデータを統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-117">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="546fa-118">Talent および Finance 間で転送する財務分析コードをマップできますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-118">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="546fa-119">財務分析コードは、現在 Common Data Service にはなく、結果として既定のテンプレートの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="546fa-119">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="546fa-120">このエンティティは計画されていますが、現在利用可能なリリース タイムラインはありません。</span><span class="sxs-lookup"><span data-stu-id="546fa-120">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="546fa-121">Finance で存在しますが、Talent では存在しないデータに関しては、Talent の**リンクの構成**を使用して 2 つのシステムを相互にリンクします。</span><span class="sxs-lookup"><span data-stu-id="546fa-121">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="546fa-122">Talent および Finance 間のリンクを構成する方法の詳細については、[Dynamics 365 Talent - Core HR (2018 年 10 月 31日) の新機能および変更された機能](whats-new-talent-october-31.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-122">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent - Core HR (October 31, 2018))](whats-new-talent-october-31.md).</span></span>

![財務分析コードのマップ](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="546fa-124">場合によっては、従業員をインポートする場合 Finance の無効な作業者に入ってしまいます。</span><span class="sxs-lookup"><span data-stu-id="546fa-124">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="546fa-125">なぜですか。</span><span class="sxs-lookup"><span data-stu-id="546fa-125">Why?</span></span>

<span data-ttu-id="546fa-126">従業員が Talent に有効な雇用詳細レコードがない場合、このエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-126">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="546fa-127">この問題を解決するには、**人事管理 \> 従業員 \> 雇用履歴 \> 日付マネージャー**に移動し、有効な雇用詳細レコードがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-127">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="546fa-128">フィールドのサブセットのみをマップする選択をする場合、非マップ フィールドに対して加えた変更は同期をトリガーしますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-128">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="546fa-129">データ同期は、実行スケジュールに従います。</span><span class="sxs-lookup"><span data-stu-id="546fa-129">Data sync follows the execution schedule.</span></span> <span data-ttu-id="546fa-130">このフィールドが統合マッピングの一部であるかどうかにかかわらず、レコードの任意のフィールドが変更されると、統合はレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="546fa-130">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="546fa-131">有効な作業者のみの変更を送信し、終了したレコードを送信しないためにはどうしますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-131">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="546fa-132">「高度なクエリ」を使用して、ソースデータを送信先に渡す前に、フィルター処理して再作成できます。</span><span class="sxs-lookup"><span data-stu-id="546fa-132">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![有効な作業者の高度なクエリ](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="546fa-134">特定のエンティティの Finance に送信するフィールドを指定できますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-134">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="546fa-135">フィールドは、統合タスクから追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="546fa-135">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="546fa-136">Common Data Service エンティティに存在するすべてのデータ フィールドが、Core HR から入力されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="546fa-136">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="546fa-137">追加のデータは、Power Apps 経由で入力されます。</span><span class="sxs-lookup"><span data-stu-id="546fa-137">Additional data can be populated via Power Apps.</span></span>

![統合タスクへ (から) フィールドを追加または削除します](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="546fa-139">バッチ ジョブとしての統合を設定しましたが、Talent は宛先システムへの接続を失いました。</span><span class="sxs-lookup"><span data-stu-id="546fa-139">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="546fa-140">宛先システムに同じ一連の変更をどのように送信しますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-140">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="546fa-141">例外処理の特別なセットアップは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="546fa-141">No special setup is required for exception handling.</span></span> <span data-ttu-id="546fa-142">データ統合は自動的にソースと宛先で発生したエラーを検出して報告し、手動での再試行を許可します。</span><span class="sxs-lookup"><span data-stu-id="546fa-142">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="546fa-143">ただし、手動でのデータ修正は許可しません。</span><span class="sxs-lookup"><span data-stu-id="546fa-143">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="546fa-144">データの更新が必要な場合、ソースまたは宛先のいずれかで発生します。</span><span class="sxs-lookup"><span data-stu-id="546fa-144">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="546fa-145">双方向の統合を設定できますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-145">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="546fa-146">いいえ、統合は現在一方向です (Talent から Finance and Operations)。</span><span class="sxs-lookup"><span data-stu-id="546fa-146">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="546fa-147">ただし、Talent から Finance にデータを送信可能な既定のテンプレートがあります。</span><span class="sxs-lookup"><span data-stu-id="546fa-147">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="546fa-148">自分の統合の一部として、レコードの削除を許可できますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-148">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="546fa-149">いいえ、データ統合は、データ転送の削除したレコードをキャプチャしません。</span><span class="sxs-lookup"><span data-stu-id="546fa-149">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="546fa-150">データ作成と更新 (UPSERT) のみが現在含まれます。</span><span class="sxs-lookup"><span data-stu-id="546fa-150">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="546fa-151">エラーの実行を再実行できますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-151">Can I rerun the errored execution?</span></span> <span data-ttu-id="546fa-152">その場合は、送信されるのは完全なファイルまたは変更のみですか。</span><span class="sxs-lookup"><span data-stu-id="546fa-152">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="546fa-153">データ統合の最初の実行は、常に完全な実行です。</span><span class="sxs-lookup"><span data-stu-id="546fa-153">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="546fa-154">その後の実行は、変更追跡に基づいています。</span><span class="sxs-lookup"><span data-stu-id="546fa-154">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="546fa-155">エラー実行が実行されると、実行のスコープのレコードを抽出し、Common Data Service から最新の変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="546fa-155">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="546fa-156">プロジェクトを保存すると、エラーが発生します:「プロジェクトにはマッピング エラーがあります。」</span><span class="sxs-lookup"><span data-stu-id="546fa-156">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="546fa-157">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="546fa-157">What do I do?</span></span>

<span data-ttu-id="546fa-158">統合キーの設定を確認し、設定に必要などんな変更も加えてから、プロジェクトでエンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="546fa-158">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="546fa-159">既定のテンプレートを使用すると、統合キーは自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="546fa-159">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="546fa-160">この問題は、新しいタスクが既存のテンプレートに追加されたときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-160">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="546fa-161">作業者の雇用がある法人の N 番号がある場合、それぞれに対するマップを作成する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-161">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="546fa-162">はい、Finance の各法人に対して、データ統合の統合プロジェクトを分ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-162">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="546fa-163">Microsoft により提供された既定のテンプレートの一部ではないデータを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-163">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="546fa-164">これを実行できますか ?</span><span class="sxs-lookup"><span data-stu-id="546fa-164">Can I do this?</span></span>

<span data-ttu-id="546fa-165">はい、フィールドは既存のテンプレートから追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="546fa-165">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="546fa-166">テンプレートを変更して、他の Common Data Service のエンティティからの追加データを含めます。</span><span class="sxs-lookup"><span data-stu-id="546fa-166">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="546fa-167">エンティティは、テンプレートに含まれる Common Data Service である必要があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-167">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="546fa-168">新しい Finance および Talent 環境を作成しましたが、エラーが発生しました。「データ値が、整合性制約に違反しています。」</span><span class="sxs-lookup"><span data-stu-id="546fa-168">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="546fa-169">なぜですか。</span><span class="sxs-lookup"><span data-stu-id="546fa-169">Why?</span></span>

<span data-ttu-id="546fa-170">このエラーが発生する理由には以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="546fa-170">Reasons for this error can include:</span></span>

- <span data-ttu-id="546fa-171">データ転送がなかったため、転送ソース (Common Data Service) で重複レコードの抽出となりました。</span><span class="sxs-lookup"><span data-stu-id="546fa-171">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="546fa-172">データ転送には、Finance and Operations で必要とされるフィールドの null 値があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-172">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="546fa-173">Common Data Service にあり、Finance and Operations の要件を満たすデータを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-173">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="546fa-174">実行エラーがあり従業員 ID が同期しなかった場合、失敗した従業員レコードがある履歴ジョブをどのように見つけますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-174">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="546fa-175">データ統合は、Finance で複数のプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="546fa-175">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="546fa-176">データ統合タスクと Finance プロジェクトとの関係は、1 対 1 です。</span><span class="sxs-lookup"><span data-stu-id="546fa-176">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="546fa-177">データ統合実行履歴からの時間を追跡し、Finance でインデックス -1 プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="546fa-177">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="546fa-178">データ統合でタスク番号が 9 の場合、Finance のインデックスは 8 です。</span><span class="sxs-lookup"><span data-stu-id="546fa-178">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="546fa-179">データ統合からタスク インデックスをキャプチャします (この例では「9」)。</span><span class="sxs-lookup"><span data-stu-id="546fa-179">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![データ統合からタスク インデックスをキャプチャします。](media/CaptureTaskIndex.png)

2. <span data-ttu-id="546fa-181">プロジェクトの実行時間を追跡します。</span><span class="sxs-lookup"><span data-stu-id="546fa-181">Track the execution time of the project.</span></span>

    ![プロジェクトの実行時間の追跡](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="546fa-183">Finance では、インデックス - 1 を識別します。</span><span class="sxs-lookup"><span data-stu-id="546fa-183">In Finance, identify index - 1.</span></span> <span data-ttu-id="546fa-184">この例では、接尾語「8」でインデックス「0」プロジェクトの実行時間を持つプロジェクトは、ステップ 2 の実行時間と一致します。</span><span class="sxs-lookup"><span data-stu-id="546fa-184">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![インデックスの識別](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="546fa-186">Talent および Finance を統合した後、Finance で Talent データが表示されません。</span><span class="sxs-lookup"><span data-stu-id="546fa-186">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="546fa-187">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="546fa-187">What do I do?</span></span>

<span data-ttu-id="546fa-188">Finance への統合には 2 つのステップがあります。</span><span class="sxs-lookup"><span data-stu-id="546fa-188">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="546fa-189">まず、Talent データが更新済で、Common Data Service で利用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-189">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="546fa-190">これはほぼリアルタイムの同期であり、データ エンティティ内のデータを参照して Power Apps で検証できます。</span><span class="sxs-lookup"><span data-stu-id="546fa-190">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data entities.</span></span>

![Common Data Service 内のデータ](media/DataInCDS.png)

<span data-ttu-id="546fa-192">Common Data Service で予定どおりにデータが表示されない場合は、エンティティが統合でサポートされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-192">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="546fa-193">Common Data Service に追加データを含めるには、Microsoft 側で変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="546fa-193">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="546fa-194">エンティティがサポートされデータが Common Data Service で使用できる場合は、データ統合でマッピングが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-194">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="546fa-195">インテグレーター マッピングが正常に見える場合、データ管理ジョブが正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-195">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="546fa-196">バッチ ジョブの実行中にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-196">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="546fa-197">データ管理の詳細については、「[データ管理](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-197">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="546fa-198">Finance にインポートした後、従業員の住所が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="546fa-198">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="546fa-199">何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-199">What should I do?</span></span>

<span data-ttu-id="546fa-200">**場所 ID** の番号順序は、Talent および Finance の両方で同じパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="546fa-200">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="546fa-201">Common Data Service から Finance and Operations にデータを統合する場合、アドレスの衝突がないように、番号順序は両側で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="546fa-201">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="546fa-202">Talent の実装中に、番号順序が Talent および Finance で同じではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-202">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="546fa-203">データが両方のシステムで維持される可能性がある場合は、すべての番号順序が同一でないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="546fa-203">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="546fa-204">接続設定を作成する際に、接続ドロップダウン リストで接続が確認できません。</span><span class="sxs-lookup"><span data-stu-id="546fa-204">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="546fa-205">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="546fa-205">What do I do?</span></span>

<span data-ttu-id="546fa-206">接続を作成するときは、Dynamics 365 Finance および Common Data Service を選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-206">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="546fa-207">雇用を同期する際、エラーが発生します。「CompanyInfo_FK が存在しません」または「フィールド '雇用終了日' の値 '12/31/2154 11:59:59 pm' が、関連するテーブル '雇用' で見つかりません。」何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-207">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="546fa-208">正しい法人にマッピングしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="546fa-208">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="546fa-209">法人の同期は既定のテンプレートの一部ではないため、Talent や Common Data Service に存在する各法人が Finance にも存在することが予想されます。</span><span class="sxs-lookup"><span data-stu-id="546fa-209">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="546fa-210">また、関連付けられている接続設定に対して正しい法人を選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="546fa-210">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="546fa-211">プロジェクトの設定後、Finance のフィールド マッピングは空のようです。</span><span class="sxs-lookup"><span data-stu-id="546fa-211">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="546fa-212">何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="546fa-212">What should I do?</span></span>

<span data-ttu-id="546fa-213">**データ管理 \> フレームワーク パラメーター \> エンティティ設定 \> エンティティ リストの更新**に移動して、Finance のデータ エンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="546fa-213">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="546fa-214">これは数分で完了し、それらのマッピングを表示できます。</span><span class="sxs-lookup"><span data-stu-id="546fa-214">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="546fa-215">新しいプロジェクトが作成されたときに、この問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="546fa-215">This issue occurs when new projects are created.</span></span>

![フィールド マッピングがありません](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="546fa-217">追加リソース</span><span class="sxs-lookup"><span data-stu-id="546fa-217">Additional resources</span></span>

- <span data-ttu-id="546fa-218">データ統合 (DI):</span><span class="sxs-lookup"><span data-stu-id="546fa-218">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="546fa-219">データを Common Data Service に統合</span><span class="sxs-lookup"><span data-stu-id="546fa-219">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="546fa-220">データ統合エラーの管理とトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="546fa-220">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="546fa-221">Power Apps、Microsoft Power Automate、および Common Data Service でシステムにより生成されたログの DSR 要求への応答</span><span class="sxs-lookup"><span data-stu-id="546fa-221">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="546fa-222">データ管理:</span><span class="sxs-lookup"><span data-stu-id="546fa-222">Data Management:</span></span>

  - [<span data-ttu-id="546fa-223">データ管理</span><span class="sxs-lookup"><span data-stu-id="546fa-223">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
