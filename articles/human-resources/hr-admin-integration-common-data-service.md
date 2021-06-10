---
title: Dataverse 統合のコンフィギュレーション
description: Microsoft Dataverse と Dynamics 365 Human Resources の統合を有効化また無効化にできます。 また、同期の詳細を表示し、追跡データをクリアし、テーブルを再同期して、2 つの環境間のデータ問題のトラブルシューティングに役立てることもできます。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 721799c9a6fafe0a809f447189ce6814b30ca863
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052460"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="a7734-104">Dataverse 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a7734-104">Configure Dataverse integration</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a7734-105">Microsoft Dataverse と Dynamics 365 Human Resources の統合を有効化また無効化にできます。</span><span class="sxs-lookup"><span data-stu-id="a7734-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="a7734-106">また、同期の詳細を表示し、追跡データをクリアし、テーブルを再同期して、2 つの環境間のデータ問題のトラブルシューティングに役立てることもできます。</span><span class="sxs-lookup"><span data-stu-id="a7734-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="a7734-107">Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](/powerapps/maker/data-platform/data-platform-intro)を参照してください</span><span class="sxs-lookup"><span data-stu-id="a7734-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="a7734-108">統合をオフにすると、ユーザーは Human Resources または Dataverse に変更を加えることができますが、これらの変更は 2 つの環境間で同期されません。</span><span class="sxs-lookup"><span data-stu-id="a7734-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="a7734-109">既定では、Human Resources とDataverse 間の統合はオフになっています。</span><span class="sxs-lookup"><span data-stu-id="a7734-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="a7734-110">次のような場合は、統合を無効にすることもできます:</span><span class="sxs-lookup"><span data-stu-id="a7734-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="a7734-111">Data Management Framework を介したデータに入力し正しい状態にするには、データを複数回インポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7734-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="a7734-112">Human Resources または Dataverse のいずれかのデータに問題があります。</span><span class="sxs-lookup"><span data-stu-id="a7734-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="a7734-113">統合を無効にする場合、他では削除せず、もう一方の環境でレコードを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="a7734-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="a7734-114">統合をオンに戻すと、削除されなかった環境のレコードは、削除された環境に同期します。</span><span class="sxs-lookup"><span data-stu-id="a7734-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="a7734-115">同期は次に、 **同期リクエストを失敗した Dataverse 統合** バッチ ジョブが実行するときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="a7734-116">データ統合を無効する場合、両方の環境で同じレコードを編集しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a7734-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="a7734-117">統合を有効に戻すと、最後に編集したレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="a7734-118">したがって、両方の環境でレコードに同じ変更を加えていない場合は、データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a7734-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="a7734-119">Dataverse 統合のページにアクセス</span><span class="sxs-lookup"><span data-stu-id="a7734-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="a7734-120">Dataverse による統合の設定を表示または構成を希望する Human Resources インスタンスで、**システム管理** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="a7734-121">[![システム管理のタイル](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="a7734-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="a7734-122">**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="a7734-123">[![リンク タブ](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="a7734-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="a7734-124">**統合** で、**Dataverse 統合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="a7734-125">[![Dataverse コンフィギュレーション リンク](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="a7734-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="a7734-126">Human Resources とDataverse 間でのデータ統合を有効化また無効化</span><span class="sxs-lookup"><span data-stu-id="a7734-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="a7734-127">統合を有効にするには、**Microsoft Dataverse 統合** ページで、**Dataverse 統合を有効化する** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7734-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a7734-128">統合を有効にすると、データは次に **同期リクエストを失敗した Dataverse 統合** バッチ ジョブを実行する時に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="a7734-129">バッチ ジョブが完了すると、すべてのデータを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a7734-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="a7734-130">統合を無効にするには、オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a7734-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="a7734-131">[![Dataverse 統合を有効化または無効化](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="a7734-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="a7734-132">データ移行タスクの実行中は、 Dataverse 統合をオフにすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a7734-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="a7734-133">大規模なデータのアップロードはパフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a7734-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="a7734-134">たとえば、2000 件の作業者をアップロードすると、統合が有効になっている場合には数時間かかりますが、無効になっている場合は1時間もかかりません。</span><span class="sxs-lookup"><span data-stu-id="a7734-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="a7734-135">この例で示している数値は、デモンストレーションの目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="a7734-136">レコードのインポートにかかる正確な時間は、さまざまな要因によって多くの影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="a7734-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="a7734-137">データ統合の詳細を表示</span><span class="sxs-lookup"><span data-stu-id="a7734-137">View data integration details</span></span>

<span data-ttu-id="a7734-138">**Microsoft Dataverse 統合** ページの **管理** クイック タブで、行が Human Resources と Dataverse 間でどのようにリンクされているかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="a7734-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="a7734-139">テーブルの行を表示するには、**Dataverse テーブル** フィールドのテーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="a7734-140">グリッドには、選択したテーブルにリンクされているすべての行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="a7734-141">すべての Dataverse テーブルが、現在リストにあるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="a7734-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="a7734-142">カスタム フィールドの使用をサポートしているテーブルだけが、グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="a7734-143">Human Resources の継続的リリースにより、新しいテーブルが利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a7734-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="a7734-144">グリッドには、次のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a7734-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="a7734-145">**Dataverse テーブル** – Dataverse のテーブルの名称です。</span><span class="sxs-lookup"><span data-stu-id="a7734-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="a7734-146">**Dataverse エンティティ参照** – Dataverse がレコードの識別に使用する識別子です。</span><span class="sxs-lookup"><span data-stu-id="a7734-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="a7734-147">この値は、Human Resources **RecId** 値と同じです。</span><span class="sxs-lookup"><span data-stu-id="a7734-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="a7734-148">Microsoft Excel で Dataverse テーブルを開くと、識別子を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a7734-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="a7734-149">**Human Resources エンティティ名** – 最後にデータを Dataverse に同期させた Human Resources エンティティです。</span><span class="sxs-lookup"><span data-stu-id="a7734-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="a7734-150">エンティティは、Dataverse の接頭語または別の接頭語を持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="a7734-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="a7734-151">**Human Resources 参照** – Human Resources のレコードに関連付けられる **Recld** 値。</span><span class="sxs-lookup"><span data-stu-id="a7734-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="a7734-152">**Dataverse から削除** - Dataverse から行が削除されたかどうかを示す値です。</span><span class="sxs-lookup"><span data-stu-id="a7734-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="a7734-153">Human Resources のレコードは、Dataverse の行に対応します。</span><span class="sxs-lookup"><span data-stu-id="a7734-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="a7734-154">Dataverse の行から人事レコードの関連付けを削除します</span><span class="sxs-lookup"><span data-stu-id="a7734-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="a7734-155">Human Resources と Dataverse 間のデータ同期中に問題が発生した場合、追跡をクリアにして追跡テーブルを再同期させることで、問題を解決できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a7734-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="a7734-156">関連付けを削除してから Dataverse の行を変更または削除すると、変更内容は Human Resources に同期されません。</span><span class="sxs-lookup"><span data-stu-id="a7734-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="a7734-157">Human Resources で変更を加えると、新しい追跡レコードが作成され、Dataverse で行が更新されます。</span><span class="sxs-lookup"><span data-stu-id="a7734-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="a7734-158">Human Resources レコードと Dataverse の行関連付けを削除するには、**Dataverse テーブル** のフィールドでテーブルを選択し、**追跡情報の削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="a7734-159">[![追跡情報をクリア](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="a7734-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="a7734-160">追跡を削除した後、テーブルの完全同期を実行するには、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7734-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="a7734-161">Human Resources と Dataverse 間のテーブルを同期する</span><span class="sxs-lookup"><span data-stu-id="a7734-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="a7734-162">この手順は、次の場合に使用します:</span><span class="sxs-lookup"><span data-stu-id="a7734-162">Use this procedure when:</span></span>

- <span data-ttu-id="a7734-163">Dataverse からの変更は、Human Resources に表示されるまでに時間がかかりすぎます。</span><span class="sxs-lookup"><span data-stu-id="a7734-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="a7734-164">追跡をクリアした後、追跡テーブルを最新の情報に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7734-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="a7734-165">Human Resources と Dataverse の間のテーブルで完全同期を実行するには :</span><span class="sxs-lookup"><span data-stu-id="a7734-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="a7734-166">**Dataverse テーブル** フィールドで、テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="a7734-167">**今すぐ同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7734-167">Select **Sync now**.</span></span>

<span data-ttu-id="a7734-168">[![完全同期の実行](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="a7734-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="a7734-169">参照</span><span class="sxs-lookup"><span data-stu-id="a7734-169">See also</span></span>

[<span data-ttu-id="a7734-170">Dataverse テーブル</span><span class="sxs-lookup"><span data-stu-id="a7734-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="a7734-171">構成 Dataverse 仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="a7734-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="a7734-172">Human Resources 仮想テーブルに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a7734-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="a7734-173">Microsoft Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="a7734-173">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="a7734-174">用語の更新</span><span class="sxs-lookup"><span data-stu-id="a7734-174">Terminology updates</span></span>](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]