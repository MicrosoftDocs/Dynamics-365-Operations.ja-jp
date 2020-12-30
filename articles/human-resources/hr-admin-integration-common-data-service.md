---
title: Common Data Service 統合のコンフィギュレーション
description: Common Data Service と Dynamics 365 Human Resources の統合を有効化また無効化にできます。 また、同期の詳細を表示し、追跡データをクリアし、エンティティを再同期して、2 つの環境間のデータ問題のトラブルシューティングに役立てることもできます。
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9ee4715526e18b33ae4b7e90b081ed5868bb19c
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527930"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="a1f93-104">Common Data Service 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a1f93-104">Configure Common Data Service integration</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a1f93-105">Common Data Service と Dynamics 365 Human Resources の統合を有効化また無効化にできます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="a1f93-106">また、同期の詳細を表示したり、追跡データをクリアしたり、エンティティを再同期して、2 つの環境間のデータ問題をトラブルシューティングすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="a1f93-107">統合をオフにすると、ユーザーは Human Resources または Common Data Service に変更を加えることができますが、これらの変更は 2 つの環境間で同期されません。</span><span class="sxs-lookup"><span data-stu-id="a1f93-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="a1f93-108">既定では、Human Resources とCommon Data Service 間の統合はオフになっています。</span><span class="sxs-lookup"><span data-stu-id="a1f93-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="a1f93-109">次のような場合は、統合を無効にすることもできます:</span><span class="sxs-lookup"><span data-stu-id="a1f93-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="a1f93-110">Data Management Framework を介したデータに入力し正しい状態にするには、データを複数回インポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="a1f93-111">Human Resources または Common Data Service のいずれかのデータに問題があります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="a1f93-112">統合を無効にする場合、他では削除せず、もう一方の環境でレコードを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="a1f93-113">統合をオンに戻すと、削除されなかった環境のレコードは、削除された環境に同期します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="a1f93-114">同期は次に、 **同期リクエストを失敗した Common Data Service 統合** バッチ ジョブが実行するときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="a1f93-115">データ統合を無効する場合、両方の環境で同じレコードを編集しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a1f93-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="a1f93-116">統合を有効に戻すと、最後に編集したレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="a1f93-117">したがって、両方の環境でレコードに同じ変更を加えていない場合は、データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="a1f93-118">Common Data Service 統合のページにアクセス</span><span class="sxs-lookup"><span data-stu-id="a1f93-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="a1f93-119">Common Data Service による統合の設定を表示または構成を希望する Human Resources インスタンスで、**システム管理** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="a1f93-120">[![システム管理のタイル](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="a1f93-121">**リンク** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="a1f93-122">[![リンク タブ](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="a1f93-123">**統合** で、**Common Data Service 統合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="a1f93-124">[![Common Data Service コンフィギュレーション リンク](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="a1f93-125">Human Resources とCommon Data Service 間でのデータ統合を有効化また無効化</span><span class="sxs-lookup"><span data-stu-id="a1f93-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="a1f93-126">統合を有効にするには、 **Common Data Service に統合を有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a1f93-127">統合を有効にすると、データは次に **同期リクエストを失敗した Common Data Service 統合** バッチ ジョブを実行する時に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="a1f93-128">バッチ ジョブが完了すると、すべてのデータを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="a1f93-129">統合を無効にするには、オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="a1f93-130">[![Common Data Service 統合を有効化または無効化](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="a1f93-131">データ移行タスクの実行中は、 Common Data Service 統合をオフにすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a1f93-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="a1f93-132">大規模なデータのアップロードはパフォーマンスに大きな影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="a1f93-133">たとえば、2000 件の作業者をアップロードすると、統合が有効になっている場合には数時間かかりますが、無効になっている場合は1時間もかかりません。</span><span class="sxs-lookup"><span data-stu-id="a1f93-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="a1f93-134">この例で示している数値は、デモンストレーションの目的でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="a1f93-135">レコードのインポートにかかる正確な時間は、さまざまな要因によって多くの影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="a1f93-136">データ統合の詳細を表示</span><span class="sxs-lookup"><span data-stu-id="a1f93-136">View data integration details</span></span>

<span data-ttu-id="a1f93-137">**Common Data Service 統合** ページの **管理** クイック タブで、レコードが Human Resources と Common Data Service 間でどのようにリンクされているか確認できます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="a1f93-138">エンティティのレコードを表示するには、**CDS エンティティ名** フィールドでエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="a1f93-139">グリッドには、選択したエンティティにリンクされているすべてのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="a1f93-140">[![エンティティのレコードを表示](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="a1f93-141">すべての Common Data Service エンティティが、現在リストにあるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="a1f93-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="a1f93-142">カスタム フィールドの使用をサポートしているエンティティだけが、グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="a1f93-143">新しいエンティティは、Human Resources の継続的リリースによって利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="a1f93-144">グリッドには、次のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1f93-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="a1f93-145">**CDS エンティティ名** – Common Data Service のエンティティ名。</span><span class="sxs-lookup"><span data-stu-id="a1f93-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="a1f93-146">**CDS エンティティ参照** – レコードを識別するために Common Data Service を使う識別子。</span><span class="sxs-lookup"><span data-stu-id="a1f93-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="a1f93-147">この値は、Human Resources **RecId** 値と同じです。</span><span class="sxs-lookup"><span data-stu-id="a1f93-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="a1f93-148">Microsoft Excel で Common Data Service エンティティうぃ開くと、識別子を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="a1f93-149">**Human Resources エンティティ名** – 最後にデータを Common Data Service に同期したエンティティ。</span><span class="sxs-lookup"><span data-stu-id="a1f93-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="a1f93-150">エンティティは、Common Data Service の接頭語または別の接頭語を持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="a1f93-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="a1f93-151">**Human Resources 参照** – Human Resources のレコードに関連付けられる **Recld** 値。</span><span class="sxs-lookup"><span data-stu-id="a1f93-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="a1f93-152">**CDS から削除されました** - Common Data Service から削除されたレコードかどうか示す値。</span><span class="sxs-lookup"><span data-stu-id="a1f93-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="a1f93-153">Common Data Service から Human Resources のレコードのアソシエーションを削除</span><span class="sxs-lookup"><span data-stu-id="a1f93-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="a1f93-154">Human Resources と Common Data Service 間のデータ同期中に問題が発生した場合、追跡をクリアにして追跡テーブルを再同期させることで、問題を解決できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="a1f93-155">アソシエーションを削除し、Common Data Service のレコードを変更または削除する場合、その変更は Human Resources に同期されません。</span><span class="sxs-lookup"><span data-stu-id="a1f93-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="a1f93-156">Human Resources に変更を加える場合、新しい追跡レコードが作成され、レコードは Common Data Service に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="a1f93-157">Human Resources と Common Data Service 間でレコードのアソシエーションを削除するには、**CDS エンティティ名** フィールドでエンティティを選び、**追跡情報をクリアにする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="a1f93-158">[![追跡情報をクリア](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="a1f93-159">追跡をクリアにした後、エンティティの完全同期を実行するには、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1f93-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="a1f93-160">Human Resources と Common Data Service 間のエンティティを同期</span><span class="sxs-lookup"><span data-stu-id="a1f93-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="a1f93-161">この手順は、次の場合に使用します:</span><span class="sxs-lookup"><span data-stu-id="a1f93-161">Use this procedure when:</span></span>

- <span data-ttu-id="a1f93-162">Common Data Service からの変更は、Human Resources に表示されるまでに時間がかかりすぎます。</span><span class="sxs-lookup"><span data-stu-id="a1f93-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="a1f93-163">追跡をクリアした後、追跡テーブルを最新の情報に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1f93-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="a1f93-164">Human Resources と Common Data Service の間のエンティティで完全同期を実行するには:</span><span class="sxs-lookup"><span data-stu-id="a1f93-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="a1f93-165">**CDS エンティティ名** フィールドで、エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="a1f93-166">**今すぐ同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a1f93-166">Select **Sync now**.</span></span>

<span data-ttu-id="a1f93-167">[![完全同期の実行](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="a1f93-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


