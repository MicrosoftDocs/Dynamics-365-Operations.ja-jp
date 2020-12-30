---
title: Finance FAQ との統合
description: この記事では、人事管理および Finance 統合でどのデータが同期されるのかについて説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a94c1269cd81ecdcbdff018ec4a8f90be36f0f3
ms.sourcegitcommit: 6aa8d6aa8276611967fb6fab44715950de49f6af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4589066"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="3ebc1-103">Finance FAQ との統合</span><span class="sxs-lookup"><span data-stu-id="3ebc1-103">Integration with Finance FAQ</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3ebc1-104">このトピックでは、Dynamics 365 Human Resources が Dynamics 365 Finance に統合される際にどのデータが同期されるかに関連した一般的な質問に回答します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="3ebc1-105">Power Apps で Dynamics 365 Talent アプリケーションを編集することはできますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="3ebc1-106">No.</span><span class="sxs-lookup"><span data-stu-id="3ebc1-106">No.</span></span> <span data-ttu-id="3ebc1-107">Talent アプリケーション ユーザーを編集すると、Human Resources と Common Data Service の統合に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-107">If you edit the Talent application user, the integration between Human Resources and Common Data Service might fail.</span></span> <span data-ttu-id="3ebc1-108">次のテーブルでは、Talent アプリケーション ユーザーに対する既定の設定を表示しています。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="3ebc1-109">姓名</span><span class="sxs-lookup"><span data-stu-id="3ebc1-109">Full Name</span></span> | <span data-ttu-id="3ebc1-110">アプリケーション ID</span><span class="sxs-lookup"><span data-stu-id="3ebc1-110">Application ID</span></span> | <span data-ttu-id="3ebc1-111">Azure AD オブジェクト ID</span><span class="sxs-lookup"><span data-stu-id="3ebc1-111">Azure AD Object ID</span></span> | <span data-ttu-id="3ebc1-112">アプリケーション ID URI</span><span class="sxs-lookup"><span data-stu-id="3ebc1-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="3ebc1-113">Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="3ebc1-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="3ebc1-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="3ebc1-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="3ebc1-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="3ebc1-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="3ebc1-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="3ebc1-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![Talent アプリケーション ユーザーに対する既定の設定](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="3ebc1-118">すべてのデータが同期された、または一部のデータ エンティティだけが同期されましたか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="3ebc1-119">データのサブセットが同期されます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="3ebc1-120">すべてのエンティティの一覧については、[ Dynamics 365 Finance との統合](hr-admin-integration-finance.md) 参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="3ebc1-121">Common Data Service に同期されたデータを表示できないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="3ebc1-121">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="3ebc1-122">既定では、Common Data Service の統合は、提供されているデモ データが含まれていない新しい環境ではオフになっています。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-122">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="3ebc1-123">既定では、デモ データが含まれている新しい環境ではオンになっており、環境の準備時にデータの同期が開始されます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="3ebc1-124">データと同期する準備が整ったら、統合をオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="3ebc1-125">詳細については、[Common Data Service 統合のコンフィギュレーション](hr-admin-integration-common-data-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-125">For more information, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="3ebc1-126">テンプレートを使用せずに新しいマップを作成できますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="3ebc1-127">テンプレートは、開始点です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-127">Templates are the starting point.</span></span> <span data-ttu-id="3ebc1-128">独自のテンプレートを作成できますが、テンプレートは統合プロジェクトを作成する際に常に必要です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="3ebc1-129">データ統合 (DI)、テンプレート、およびプロジェクトの詳細については、「[Common Data Service へデータを統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="3ebc1-130">人事管理および Finance 間で転送する財務分析コードをマップできますか?</span><span class="sxs-lookup"><span data-stu-id="3ebc1-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="3ebc1-131">財務分析コードは、現在 Common Data Service にはなく、結果として既定のテンプレートの一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-131">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="3ebc1-132">このエンティティは計画されていますが、現在利用可能なリリース タイムラインはありません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="3ebc1-133">Finance and Operations で存在しますが、人事管理では存在しないデータに関しては、人事管理 **リンクの構成** を使用して 2 つのシステムを相互にリンクします。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![財務分析コードのマップ](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="3ebc1-135">場合によっては、従業員をインポートする場合 Finance の無効な作業者に入ってしまいます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="3ebc1-136">なぜですか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-136">Why?</span></span>

<span data-ttu-id="3ebc1-137">従業員が人事管理に有効な雇用詳細レコードがない場合、このエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="3ebc1-138">この問題を解決するには、**人事管理 \> 従業員 \> 雇用履歴 \> 日付マネージャー** に移動し、有効な雇用詳細レコードがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="3ebc1-139">フィールドのサブセットのみをマップする選択をする場合、非マップ フィールドに対して加えた変更は同期をトリガーしますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="3ebc1-140">データ同期は、実行スケジュールに従います。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="3ebc1-141">このフィールドが統合マッピングの一部であるかどうかにかかわらず、レコードの任意のフィールドが変更されると、統合はレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="3ebc1-142">有効な作業者のみの変更を送信し、終了したレコードを送信しないためにはどうしますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="3ebc1-143">「高度なクエリ」を使用して、ソースデータを送信先に渡す前に、フィルター処理して再作成できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![有効な作業者の高度なクエリ](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="3ebc1-145">特定のエンティティの Finance に送信するフィールドを指定できますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="3ebc1-146">フィールドは、統合タスクから追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="3ebc1-147">Common Data Service エンティティに存在するすべてのデータ フィールドが、人事管理から入力されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-147">Not all data fields that exist on the Common Data Service entity will be populated from Human Resources.</span></span>
<span data-ttu-id="3ebc1-148">追加のデータは、Power Apps 経由で入力されます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-148">Additional data can be populated via Power Apps.</span></span>

![統合タスクへ (から) フィールドを追加または削除します](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="3ebc1-150">バッチ ジョブとしての統合を設定しましたが、人事管理は宛先システムへの接続を失いました。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="3ebc1-151">宛先システムに同じ一連の変更をどのように送信しますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="3ebc1-152">例外処理の特別なセットアップは必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="3ebc1-153">データ統合は自動的にソースと宛先で発生したエラーを検出して報告し、手動での再試行を許可します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="3ebc1-154">ただし、手動でのデータ修正は許可しません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="3ebc1-155">データの更新が必要な場合、ソースまたは宛先のいずれかで発生します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="3ebc1-156">双方向の統合を設定できますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="3ebc1-157">いいえ、統合は現在一方向 (Finance and Operations への人事管理) です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="3ebc1-158">ただし、人事管理から Finance にデータを送信可能な既定のテンプレートがあります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="3ebc1-159">自分の統合の一部として、レコードの削除を許可できますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="3ebc1-160">いいえ、データ統合は、データ転送の削除したレコードをキャプチャしません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="3ebc1-161">データ作成と更新 (UPSERT) のみが現在含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="3ebc1-162">エラーの実行を再実行できますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="3ebc1-163">その場合は、送信されるのは完全なファイルまたは変更のみですか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="3ebc1-164">データ統合の最初の実行は、常に完全な実行です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="3ebc1-165">その後の実行は、変更追跡に基づいています。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="3ebc1-166">エラー実行が実行されると、実行のスコープのレコードを抽出し、Common Data Service から最新の変更を送信します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="3ebc1-167">プロジェクトを保存すると、エラーが発生します:「プロジェクトにはマッピング エラーがあります。」</span><span class="sxs-lookup"><span data-stu-id="3ebc1-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="3ebc1-168">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="3ebc1-168">What do I do?</span></span>

<span data-ttu-id="3ebc1-169">統合キーの設定を確認し、設定に必要などんな変更も加えてから、プロジェクトでエンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="3ebc1-170">既定のテンプレートを使用すると、統合キーは自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="3ebc1-171">この問題は、新しいタスクが既存のテンプレートに追加されたときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="3ebc1-172">作業者の雇用がある法人の N 番号がある場合、それぞれに対するマップを作成する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="3ebc1-173">はい、Finance の各法人に対して、データ統合の統合プロジェクトを分ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="3ebc1-174">Microsoft により提供された既定のテンプレートの一部ではないデータを転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="3ebc1-175">これを実行できますか ?</span><span class="sxs-lookup"><span data-stu-id="3ebc1-175">Can I do this?</span></span>

<span data-ttu-id="3ebc1-176">はい、フィールドは既存のテンプレートから追加または削除できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="3ebc1-177">テンプレートを変更して、他の Common Data Service のエンティティからの追加データを含めます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-177">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="3ebc1-178">エンティティは、テンプレートに含まれる Common Data Service である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-178">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="3ebc1-179">新しい Finance および人事管理環境を作成しましたが、「データ値が、整合性制約に違反しています」というエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="3ebc1-180">なぜですか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-180">Why?</span></span>

<span data-ttu-id="3ebc1-181">このエラーが発生する理由には以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="3ebc1-182">データ転送がなかったため、転送ソース (Common Data Service) で重複レコードの抽出となりました。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-182">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="3ebc1-183">データ転送には、Finance and Operations で必要とされるフィールドの Null 値があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="3ebc1-184">Common Data Service にあり、Finance and Operations の要件を満たすデータを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-184">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="3ebc1-185">実行エラーがあり従業員 ID が同期しなかった場合、失敗した従業員レコードがある履歴ジョブをどのように見つけますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="3ebc1-186">データ統合は、Finance で複数のプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="3ebc1-187">データ統合タスクと Finance プロジェクトとの関係は、1 対 1 です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="3ebc1-188">データ統合実行履歴からの時間を追跡し、Finance でインデックス -1 プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="3ebc1-189">データ統合でタスク番号が 9 の場合、Finance のインデックスは 8 です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="3ebc1-190">データ統合からタスク インデックスをキャプチャします (この例では「9」)。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![データ統合からタスク インデックスをキャプチャします。](media/CaptureTaskIndex.png)

2. <span data-ttu-id="3ebc1-192">プロジェクトの実行時間を追跡します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-192">Track the execution time of the project.</span></span>

    ![プロジェクトの実行時間の追跡](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="3ebc1-194">Finance では、インデックス - 1 を識別します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="3ebc1-195">この例では、接尾語「8」でインデックス「0」プロジェクトの実行時間を持つプロジェクトは、ステップ 2 の実行時間と一致します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![インデックスの識別](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="3ebc1-197">人事管理と Finance を統合した後、財務の人事管理データは表示されません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="3ebc1-198">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="3ebc1-198">What do I do?</span></span>

<span data-ttu-id="3ebc1-199">Finance への統合には 2 つのステップがあります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="3ebc1-200">まず、人事管理データが更新済で、Common Data Service で利用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-200">First, verify that the Human Resources data is updated and available in Common Data Service.</span></span> <span data-ttu-id="3ebc1-201">これはほぼリアルタイムの同期であり、データ エンティティ内のデータを参照して Power Apps で検証できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data entities.</span></span>

![Common Data Service 内のデータ](media/DataInCDS.png)

<span data-ttu-id="3ebc1-203">Common Data Service で予定どおりにデータが表示されない場合は、エンティティが統合でサポートされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-203">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="3ebc1-204">Common Data Service に追加データを含めるには、Microsoft 側で変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-204">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="3ebc1-205">エンティティがサポートされデータが Common Data Service で使用できる場合は、データ統合でマッピングが正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-205">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="3ebc1-206">インテグレーター マッピングが正常に見える場合、データ管理ジョブが正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="3ebc1-207">バッチ ジョブの実行中にエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="3ebc1-208">データ管理の詳細については、「[データ管理](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-208">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="3ebc1-209">Finance にインポートした後、従業員の住所が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="3ebc1-210">何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-210">What should I do?</span></span>

<span data-ttu-id="3ebc1-211">**場所 ID** の番号順序は、人事管理および Finance の両方で同じパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="3ebc1-212">Common Data Service から Finance and Operations にデータを統合する場合、アドレスの衝突がないように、番号順序は両側で一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="3ebc1-213">人事管理の実装中に、番号順序が人事管理および Finance and Operations で同じではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="3ebc1-214">データが両方のシステムで維持される可能性がある場合は、すべての番号順序が同一でないことを検証します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="3ebc1-215">接続設定を作成する際に、接続ドロップダウン リストで接続が確認できません。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="3ebc1-216">何をしたらいいですか ?</span><span class="sxs-lookup"><span data-stu-id="3ebc1-216">What do I do?</span></span>

<span data-ttu-id="3ebc1-217">接続を作成するときは、Dynamics 365 Finance および Common Data Service を選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="3ebc1-218">雇用を同期する際、エラーが発生します。「CompanyInfo_FK が存在しません」または「フィールド '雇用終了日' の値 '12/31/2154 11:59:59 pm' が、関連するテーブル '雇用' で見つかりません。」何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="3ebc1-219">正しい法人にマッピングしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="3ebc1-220">法人の同期は既定のテンプレートの一部ではないため、人事管理や Common Data Service に存在する各法人が Finance にも存在することが予想されます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="3ebc1-221">また、関連付けられている接続設定に対して正しい法人を選択していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="3ebc1-222">プロジェクトの設定後、Finance のフィールド マッピングは空のようです。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="3ebc1-223">何をする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-223">What should I do?</span></span>

<span data-ttu-id="3ebc1-224">**データ管理 \> フレームワーク パラメーター \> エンティティ設定 \> エンティティ リストの更新** に移動して、Finance のデータ エンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="3ebc1-225">これは数分で完了し、それらのマッピングを表示できます。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="3ebc1-226">新しいプロジェクトが作成されたときに、この問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="3ebc1-226">This issue occurs when new projects are created.</span></span>

![フィールド マッピングがありません](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="3ebc1-228">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3ebc1-228">Additional resources</span></span>

- <span data-ttu-id="3ebc1-229">データ統合 (DI):</span><span class="sxs-lookup"><span data-stu-id="3ebc1-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="3ebc1-230">データを Common Data Service に統合</span><span class="sxs-lookup"><span data-stu-id="3ebc1-230">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="3ebc1-231">データ統合エラーの管理とトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="3ebc1-231">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="3ebc1-232">Power Apps、Microsoft Power Automate、および Common Data Service でシステムにより生成されたログの DSR 要求への応答</span><span class="sxs-lookup"><span data-stu-id="3ebc1-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="3ebc1-233">データ管理:</span><span class="sxs-lookup"><span data-stu-id="3ebc1-233">Data Management:</span></span>

  - [<span data-ttu-id="3ebc1-234">データ管理</span><span class="sxs-lookup"><span data-stu-id="3ebc1-234">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
