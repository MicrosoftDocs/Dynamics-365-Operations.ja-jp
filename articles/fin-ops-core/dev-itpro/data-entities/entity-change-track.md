---
title: エンティティへの変更追跡の有効化
description: Finance and Operations からのデータの差分エクスポートを有効にする追跡の変更を使用します。
author: Milindav2
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.custom: 265974
ms.assetid: 434b5d9f-9877-4769-ad96-d4e8d460a7fa
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ea630d0684d3f51e21150865364ab4144ca5771
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750580"
---
# <a name="enable-change-tracking-for-entities"></a><span data-ttu-id="17614-103">エンティティの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="17614-103">Enable change tracking for entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17614-104">変更追跡は、データ管理を使用して Finance and Operations アプリからのデータの増分エクスポートを有効化します。</span><span class="sxs-lookup"><span data-stu-id="17614-104">Change tracking enables incremental export of data from Finance and Operations apps by using Data management.</span></span> <span data-ttu-id="17614-105">増分エクスポートでは、変更されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="17614-105">In an incremental export, only records that have changed are exported.</span></span> <span data-ttu-id="17614-106">差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17614-106">To enable incremental export, you must enable change tracking on entities.</span></span> <span data-ttu-id="17614-107">エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。</span><span class="sxs-lookup"><span data-stu-id="17614-107">If you don't enable change tracking on an entity, you can only enable a full export each time.</span></span> 

<span data-ttu-id="17614-108">変更追跡は、自分のデータベース (BYOD) シナリオと非 BYOD シナリオの両方に対して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="17614-108">Change tracking can be enabled for both bring your own database (BYOD) and non-BYOD scenarios.</span></span> <span data-ttu-id="17614-109">これには、Dataverse 仮想エンティティを介したレコードの変更の取得が含まれます。</span><span class="sxs-lookup"><span data-stu-id="17614-109">This includes retrieving record changes through Dataverse virtual entities.</span></span>

    > [!NOTE]
    > Change tracking will track record deletion only for bring your own database (BYOD) and Dataverse virtual entity use cases, if the entity supports it. Other non-BYOD scenarios will not include tracking record deletion. Deletion is tracked only for the root data source in the entity.

## <a name="enable-change-tracking-for-byod"></a><span data-ttu-id="17614-110">BYOD の変更追跡を有効する</span><span class="sxs-lookup"><span data-stu-id="17614-110">Enable change tracking for BYOD</span></span>
<span data-ttu-id="17614-111">データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="17614-111">You can enable change tracking when you publish one or more entities to a data store (BYOD).</span></span>

1. <span data-ttu-id="17614-112">**データ管理** ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-112">In the **Data management** workspace, select **Configure entity export to database**.</span></span>
2. <span data-ttu-id="17614-113">データのエクスポート先のデータベースを選択し、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-113">Select the database to export data to, and then select **Publish**.</span></span>

    <span data-ttu-id="17614-114">1 つまたは複数のエンティティをデータベースに公開することができます。</span><span class="sxs-lookup"><span data-stu-id="17614-114">You can publish one or more entities to your database.</span></span> <span data-ttu-id="17614-115">**公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="17614-115">Select **Show published only** to see a list of entities that have previously been published.</span></span>

3. <span data-ttu-id="17614-116">公開されているエンティティを選択し、**変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-116">Select an entity that is published, and then select **Change tracking**.</span></span>
4. <span data-ttu-id="17614-117">環境内の変更追跡の適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-117">Select the appropriate option for change tracking for your environment.</span></span>

    <span data-ttu-id="17614-118">複数のテーブルを使用してエンティティをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="17614-118">An entity can be modeled by using more than one table.</span></span> <span data-ttu-id="17614-119">このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="17614-119">The options let you specify the granularity at which changes can be tracked in an entity.</span></span>

    | <span data-ttu-id="17614-120">オプション</span><span class="sxs-lookup"><span data-stu-id="17614-120">Option</span></span>               | <span data-ttu-id="17614-121">変更の追跡方法</span><span class="sxs-lookup"><span data-stu-id="17614-121">How changes are tracked</span></span> |
    |----------------------|-------------------------|
    | <span data-ttu-id="17614-122">プライマリ テーブルの有効化</span><span class="sxs-lookup"><span data-stu-id="17614-122">Enable primary table</span></span> | <span data-ttu-id="17614-123">プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="17614-123">Changes that are made to any fields in the primary table trigger a change in entity.</span></span> <span data-ttu-id="17614-124">セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。</span><span class="sxs-lookup"><span data-stu-id="17614-124">Changes that are made to fields in secondary tables don't trigger a change in entity.</span></span> |
    | <span data-ttu-id="17614-125">エンティティ全体の有効化</span><span class="sxs-lookup"><span data-stu-id="17614-125">Enable entire entity</span></span> | <span data-ttu-id="17614-126">エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="17614-126">Changes that are made to any fields in any table in the entity trigger a change in entity.</span></span> |
    | <span data-ttu-id="17614-127">カスタム クエリの有効化</span><span class="sxs-lookup"><span data-stu-id="17614-127">Enable custom query</span></span>  | <span data-ttu-id="17614-128">変更を追跡する必要があるテーブルを識別するカスタム クエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="17614-128">Uses a custom query that identifies the tables on which changes must be tracked.</span></span> <span data-ttu-id="17614-129">カスタム クエリはエンティティで定義されます。</span><span class="sxs-lookup"><span data-stu-id="17614-129">The custom query is defined in the entity.</span></span> |

    > [!NOTE]
    > <span data-ttu-id="17614-130">変更がトリガーされた場合、変更はフィールド レベルではなくレコード全体で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="17614-130">If a change is triggered, the change is tracked on the entire record and not at the field level.</span></span> <span data-ttu-id="17614-131">エンティティ レコード全体がエクスポート先にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="17614-131">The entire entity record is exported to the destination.</span></span> <span data-ttu-id="17614-132">選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。</span><span class="sxs-lookup"><span data-stu-id="17614-132">Regardless of the option that you select, the number of fields in the entity is the number that is exported to the destination.</span></span>

## <a name="enable-change-tracking-for-non-byod-scenarios"></a><span data-ttu-id="17614-133">非 BYOD シナリオでの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="17614-133">Enable change tracking for non-BYOD scenarios</span></span>
<span data-ttu-id="17614-134">変更追跡は、非 BYOD シナリオに対して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="17614-134">Change tracking can be enabled for non-BYOD scenarios.</span></span> <span data-ttu-id="17614-135">これには、Finance and Operations アプリの Dataverse 仮想エンティティを介したレコードの変更の取得が含まれます。</span><span class="sxs-lookup"><span data-stu-id="17614-135">This includes retrieving record changes through Dataverse virtual entities for Finance and Operations apps.</span></span> <span data-ttu-id="17614-136">エンティティで変更追跡が有効になっている場合、優先設定ヘッダーとして `odata.track-changes` を追加することで、エンティティの OData エンドポイントから変更点を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="17614-136">When change tracking is enabled for an entity, changes can be retrieved through the entity's OData endpoint by adding `odata.track-changes` as a preference header.</span></span>

<span data-ttu-id="17614-137">エンティティに対する変更追跡の使用の詳細については、「[変更追跡を使用したデータと外部システムとの同期](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="17614-137">For more information on using change tracking for an entity, see [Use change tracking to synchronize data with external systems](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems).</span></span>

<span data-ttu-id="17614-138">非 BYOD シナリオで変更追跡を有効化する方法 :</span><span class="sxs-lookup"><span data-stu-id="17614-138">To enable change tracking for non-BYOD scenarios:</span></span>

1. <span data-ttu-id="17614-139">**データ管理** ワークスペースから、**データ エンティティ** リスト ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-139">From the **Data management** workspace, select the **Data entities** list page.</span></span>
2. <span data-ttu-id="17614-140">変更追跡を有効にするエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-140">Select the entity for which you want to enable change tracking.</span></span> 
3. <span data-ttu-id="17614-141">アクション リボンで、**変更追跡** アクションを選択し、エンティティの変更を追跡する方法について必要なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="17614-141">Select the **Change tracking** action on the action ribbon, and select the desired option for how changes should be tracked for the entity.</span></span> <span data-ttu-id="17614-142">使用可能なオプションの詳細については、前述の「[BYOD に対して変更追跡を有効にする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track#enable-change-tracking-for-byod)」セクションのテーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="17614-142">See the table in the [Enable change tracking for BYOD](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/entity-change-track#enable-change-tracking-for-byod) section above for detail on the available options.</span></span>

## <a name="custom-query-for-change-tracking"></a><span data-ttu-id="17614-143">変更追跡用のカスタム クエリ</span><span class="sxs-lookup"><span data-stu-id="17614-143">Custom query for change tracking</span></span>
<span data-ttu-id="17614-144">次の例は、エンティティに静的メソッドを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="17614-144">The following example shows how to add a static method to an entity.</span></span> <span data-ttu-id="17614-145">メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17614-145">You must make sure that the method returns a query, and that the root node is the same as the entity.</span></span> <span data-ttu-id="17614-146">たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。</span><span class="sxs-lookup"><span data-stu-id="17614-146">For example, for the Customer entity, the root node is custTable, and the change tracking query for it is also custtable.</span></span>

- <span data-ttu-id="17614-147">クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="17614-147">You must enable change tracking on the tables that are part of the query.</span></span>
- <span data-ttu-id="17614-148">エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。</span><span class="sxs-lookup"><span data-stu-id="17614-148">Create a join between the entity and the change tracking query (on the root table) to determine which records have changed in the entity.</span></span>

```xpp
public static Query defaultCTQuery()
{
    Query q = new Query();    
    
    QueryBuildDataSource custDs = q.addDataSource(tableNum(CustTable));

    QueryBuildDataSource partyDs = custDs.addDataSource(tableNum(DirPartyTable));
    partyDs.relations(true);

    QueryBuildDataSource locationDs = partyDs.addDataSource(tableNum(DirPartyLocation));
    locationDs.addRange(fieldNum(DirPartyLocation, IsPrimary)).value(queryValue(NoYes::Yes));        
    locationDs.addLink(fieldNum(DirPartyTable, RecId), fieldNum(DirPartyLocation, Party));

    QueryBuildDataSource addressDs = locationDs.addDataSource(tableStr(LogisticsPostalAddress));        
    addressDs.addLink(fieldNum(DirPartyLocation, Location), fieldNum(LogisticsPostalAddress, Location));

    return q;
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
