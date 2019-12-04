---
title: Common Data Service 統合のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Talent と Common Data Service 間の統合を有効または無効にする方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: 1b98a498fa0c026d16fa1317b2a463057c8f8c68
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832804"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="fadb0-103">Common Data Service 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="fadb0-103">Configure Common Data Service integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fadb0-104">Common Data Service と Microsoft Dynamics 365 Talent のインスタンス間の統合を、有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-104">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Talent on or off.</span></span> <span data-ttu-id="fadb0-105">また、同期の詳細を表示したり、追跡データをクリアしたり、エンティティを再同期して、2 つの環境間のデータ問題をトラブルシューティングすることもできます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-105">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="fadb0-106">統合をオフにすると、ユーザーは人材または Common Data Service に変更を加えることができますが、これらの変更は 2 つの環境間で同期されません。</span><span class="sxs-lookup"><span data-stu-id="fadb0-106">When you turn off integration, users can make changes in Talent or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="fadb0-107">既定では、環境のデモ データの有無に応じて、人材と Common Data Service 間の統合は有効または無効になります。</span><span class="sxs-lookup"><span data-stu-id="fadb0-107">By default, integration between Talent and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="fadb0-108">デモ データを含まない新しい環境において、**無効**</span><span class="sxs-lookup"><span data-stu-id="fadb0-108">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="fadb0-109">デモ データを含む新しい環境において、**有効**</span><span class="sxs-lookup"><span data-stu-id="fadb0-109">**On** for new environments that include demo data</span></span>

<span data-ttu-id="fadb0-110">デモ データが含まれる新しい環境では、データの準備時にデータの同期が開始されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-110">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="fadb0-111">次のような場合は、統合を無効にすることもできます:</span><span class="sxs-lookup"><span data-stu-id="fadb0-111">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="fadb0-112">Data Management Framework を介したデータに入力し正しい状態にするには、データを複数回インポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fadb0-112">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="fadb0-113">人材または Common Data Service のいずれかのデータに問題があります。</span><span class="sxs-lookup"><span data-stu-id="fadb0-113">There are issues with data in either Talent or Common Data Service.</span></span> <span data-ttu-id="fadb0-114">統合を無効にする場合、他では削除せず、もう一方の環境でレコードを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-114">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="fadb0-115">統合を有効に戻すと、削除されていない環境のレコードは、削除された環境に同期されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-115">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="fadb0-116">同期は次に、 **同期リクエストを失敗した Common Data Service 統合** バッチ ジョブが実行するときに開始されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-116">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="fadb0-117">データ統合を無効する場合、両方の環境で同じレコードを編集しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="fadb0-117">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="fadb0-118">統合を有効に戻すと、最後に編集したレコードが同期されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-118">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="fadb0-119">したがって、両方の環境でレコードに同じ変更を加えていない場合は、データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fadb0-119">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="fadb0-120">Common Data Service 統合のページにアクセス</span><span class="sxs-lookup"><span data-stu-id="fadb0-120">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="fadb0-121">Common Data Service による統合の設定を表示または構成を希望する人材インスタンスで、**システム管理**のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-121">In the Talent instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="fadb0-122">[![システム管理のタイル](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-122">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="fadb0-123">**リンク**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-123">Select the **Links** tab.</span></span>

    <span data-ttu-id="fadb0-124">[![リンク タブ](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-124">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="fadb0-125">**統合**で、**Common Data Service 統合**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-125">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="fadb0-126">[![Common Data Service コンフィギュレーション リンク](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-126">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-talent-and-common-data-service-on-or-off"></a><span data-ttu-id="fadb0-127">人材とCommon Data Service 間でのデータ統合を有効化また無効化</span><span class="sxs-lookup"><span data-stu-id="fadb0-127">Turn data integration between Talent and Common Data Service on or off</span></span>

- <span data-ttu-id="fadb0-128">統合を有効にするには、 **Common Data Service に統合を有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-128">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fadb0-129">統合を有効にすると、データは次に **同期リクエストを失敗した Common Data Service 統合** バッチ ジョブを実行する時に同期されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-129">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="fadb0-130">バッチ ジョブが完了すると、すべてのデータを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="fadb0-130">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="fadb0-131">統合を無効にするには、オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-131">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="fadb0-132">[![Common Data Service 統合を有効化または無効化](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-132">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="fadb0-133">データ統合の詳細を表示</span><span class="sxs-lookup"><span data-stu-id="fadb0-133">View data integration details</span></span>

<span data-ttu-id="fadb0-134">**Common Data Service 統合**ページの**管理**クイックタブで、レコードが人材と Common Data Service 間でどのようにリンクされているか確認できます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-134">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Talent and Common Data Service.</span></span>

- <span data-ttu-id="fadb0-135">エンティティのレコードを表示するには、**CDS エンティティ名**フィールドでエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-135">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="fadb0-136">グリッドには、選択したエンティティにリンクされているすべてのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-136">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="fadb0-137">[![エンティティのレコードを表示](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-137">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="fadb0-138">すべての Common Data Service エンティティが、現在リストにあるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="fadb0-138">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="fadb0-139">カスタム フィールドの使用をサポートしているエンティティだけが、グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-139">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="fadb0-140">新しいエンティティは、人材の継続的リリースによって利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="fadb0-140">New entities become available through continuous releases of Talent.</span></span>

<span data-ttu-id="fadb0-141">グリッドには、次のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fadb0-141">The grid includes the following fields:</span></span>

- <span data-ttu-id="fadb0-142">**CDS エンティティ名** – Common Data Service のエンティティ名。</span><span class="sxs-lookup"><span data-stu-id="fadb0-142">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="fadb0-143">**CDS エンティティ参照** – レコードを識別するために Common Data Service を使う識別子。</span><span class="sxs-lookup"><span data-stu-id="fadb0-143">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="fadb0-144">この値は、人材 **RecId** 値と同じです。</span><span class="sxs-lookup"><span data-stu-id="fadb0-144">This value is equivalent to a Talent **RecId** value.</span></span> <span data-ttu-id="fadb0-145">Microsoft Excel で Common Data Service エンティティうぃ開くと、識別子を確認できます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-145">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="fadb0-146">**人材エンティティ名** - 最後にデータを Common Data Service に同期したエンティティ。</span><span class="sxs-lookup"><span data-stu-id="fadb0-146">**Talent entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="fadb0-147">エンティティは、Common Data Service の接頭語または別の接頭語を持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="fadb0-147">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="fadb0-148">**人材参照** - 人材のレコードに関連付けられる **Recld** 値。</span><span class="sxs-lookup"><span data-stu-id="fadb0-148">**Talent reference** – The **RecId** value that is associated with the record in Talent.</span></span>
- <span data-ttu-id="fadb0-149">**CDS から削除されました** - Common Data Service から削除されたレコードかどうか示す値。</span><span class="sxs-lookup"><span data-stu-id="fadb0-149">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-talent-from-common-data-service"></a><span data-ttu-id="fadb0-150">Common Data Service から人材のレコードのアソシエーションを削除</span><span class="sxs-lookup"><span data-stu-id="fadb0-150">Remove the association of a record in Talent from Common Data Service</span></span>

<span data-ttu-id="fadb0-151">人材と Common Data Service 間のデータ同期中に問題が発生した場合、追跡をクリアにして追跡テーブルを再同期させることで、問題を解決できるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="fadb0-151">If you experience issues during data synchronization between Talent and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="fadb0-152">アソシエーションを削除し、Common Data Service のレコードを変更または削除する場合、その変更は人材に同期されません。</span><span class="sxs-lookup"><span data-stu-id="fadb0-152">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Talent.</span></span> <span data-ttu-id="fadb0-153">人材に変更を加える場合、新しい追跡レコードが作成され、レコードは Common Data Service に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fadb0-153">If you make changes in Talent, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="fadb0-154">人材と Common Data Service 間でレコードのアソシエーションを削除するには、**CDS エンティティ名**フィールドでエンティティを選び、**追跡情報をクリアにする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-154">To remove the association of a record between Talent and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="fadb0-155">[![追跡情報をクリア](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-155">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="fadb0-156">追跡をクリアにした後、エンティティの完全同期を実行するには、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fadb0-156">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-talent-and-common-data-service"></a><span data-ttu-id="fadb0-157">人材と Common Data Service 間のエンティティを同期</span><span class="sxs-lookup"><span data-stu-id="fadb0-157">Sync an entity between Talent and Common Data Service</span></span>

<span data-ttu-id="fadb0-158">Common Data Service からの変更が人材に表示するにはあまりにも長い場合、または追跡をクリアした後に追跡テーブルを更新する必要がある場合は、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-158">Use this procedure if changes from Common Data Service are taking too long to appear in Talent, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="fadb0-159">人材と Common Data Service 間のエンティティで完全同期を実行するには、**CDS エンティテ名**フィールドでエンティティを選び、**今すぐ同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fadb0-159">To run a full synchronization on an entity between Talent and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="fadb0-160">[![完全同期の実行](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="fadb0-160">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>
