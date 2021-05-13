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
ms.openlocfilehash: 5b0aac56d60d67664a2ab92adbe68b3f579de306
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941069"
---
# <a name="enable-change-tracking-for-entities"></a><span data-ttu-id="df548-103">エンティティの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="df548-103">Enable change tracking for entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df548-104">変更追跡は、データ管理を使用して Finance and Operations アプリからのデータの増分エクスポートを有効化します。</span><span class="sxs-lookup"><span data-stu-id="df548-104">Change tracking enables incremental export of data from Finance and Operations apps by using Data management.</span></span> <span data-ttu-id="df548-105">増分エクスポートでは、変更されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="df548-105">In an incremental export, only records that have changed are exported.</span></span> <span data-ttu-id="df548-106">差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df548-106">To enable incremental export, you must enable change tracking on entities.</span></span> <span data-ttu-id="df548-107">エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。</span><span class="sxs-lookup"><span data-stu-id="df548-107">If you don't enable change tracking on an entity, you can only enable a full export each time.</span></span> 

<span data-ttu-id="df548-108">変更追跡は、自分のデータベース (BYOD) シナリオと非 BYOD シナリオの両方に対して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="df548-108">Change tracking can be enabled for both bring your own database (BYOD) and non-BYOD scenarios.</span></span> <span data-ttu-id="df548-109">これには、Dataverse 仮想エンティティを介したレコードの変更の取得が含まれます。</span><span class="sxs-lookup"><span data-stu-id="df548-109">This includes retrieving record changes through Dataverse virtual entities.</span></span>

> [!NOTE]
> <span data-ttu-id="df548-110">変更の追跡では、エンティティがサポートしている場合、独自のデータベース (BYOD) および Dataverse 仮想エンティティのユース ケースに対してのみレコードの削除を追跡します。</span><span class="sxs-lookup"><span data-stu-id="df548-110">Change tracking will track record deletion only for bring your own database (BYOD) and Dataverse virtual entity use cases, if the entity supports it.</span></span> <span data-ttu-id="df548-111">他の非 BYOD シナリオでは、追跡レコードの削除は含まれません。</span><span class="sxs-lookup"><span data-stu-id="df548-111">Other non-BYOD scenarios will not include tracking record deletion.</span></span> <span data-ttu-id="df548-112">削除処理は エンティティ内 の ルート データ ソース に対してのみ追跡されます。</span><span class="sxs-lookup"><span data-stu-id="df548-112">Deletion is tracked only for the root data source in the entity.</span></span>

## <a name="enable-change-tracking-for-byod"></a><span data-ttu-id="df548-113">BYOD の変更追跡を有効する</span><span class="sxs-lookup"><span data-stu-id="df548-113">Enable change tracking for BYOD</span></span>
<span data-ttu-id="df548-114">データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="df548-114">You can enable change tracking when you publish one or more entities to a data store (BYOD).</span></span>

1. <span data-ttu-id="df548-115">**データ管理** ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-115">In the **Data management** workspace, select **Configure entity export to database**.</span></span>
2. <span data-ttu-id="df548-116">データのエクスポート先のデータベースを選択し、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-116">Select the database to export data to, and then select **Publish**.</span></span>

    <span data-ttu-id="df548-117">1 つまたは複数のエンティティをデータベースに公開することができます。</span><span class="sxs-lookup"><span data-stu-id="df548-117">You can publish one or more entities to your database.</span></span> <span data-ttu-id="df548-118">**公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="df548-118">Select **Show published only** to see a list of entities that have previously been published.</span></span>

3. <span data-ttu-id="df548-119">公開されているエンティティを選択し、**変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-119">Select an entity that is published, and then select **Change tracking**.</span></span>
4. <span data-ttu-id="df548-120">環境内の変更追跡の適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-120">Select the appropriate option for change tracking for your environment.</span></span>

    <span data-ttu-id="df548-121">複数のテーブルを使用してエンティティをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="df548-121">An entity can be modeled by using more than one table.</span></span> <span data-ttu-id="df548-122">このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="df548-122">The options let you specify the granularity at which changes can be tracked in an entity.</span></span>

    | <span data-ttu-id="df548-123">オプション</span><span class="sxs-lookup"><span data-stu-id="df548-123">Option</span></span>               | <span data-ttu-id="df548-124">変更の追跡方法</span><span class="sxs-lookup"><span data-stu-id="df548-124">How changes are tracked</span></span> |
    |----------------------|-------------------------|
    | <span data-ttu-id="df548-125">プライマリ テーブルの有効化</span><span class="sxs-lookup"><span data-stu-id="df548-125">Enable primary table</span></span> | <span data-ttu-id="df548-126">プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="df548-126">Changes that are made to any fields in the primary table trigger a change in entity.</span></span> <span data-ttu-id="df548-127">セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。</span><span class="sxs-lookup"><span data-stu-id="df548-127">Changes that are made to fields in secondary tables don't trigger a change in entity.</span></span> |
    | <span data-ttu-id="df548-128">エンティティ全体の有効化</span><span class="sxs-lookup"><span data-stu-id="df548-128">Enable entire entity</span></span> | <span data-ttu-id="df548-129">エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="df548-129">Changes that are made to any fields in any table in the entity trigger a change in entity.</span></span> |
    | <span data-ttu-id="df548-130">カスタム クエリの有効化</span><span class="sxs-lookup"><span data-stu-id="df548-130">Enable custom query</span></span>  | <span data-ttu-id="df548-131">変更を追跡する必要があるテーブルを識別するカスタム クエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="df548-131">Uses a custom query that identifies the tables on which changes must be tracked.</span></span> <span data-ttu-id="df548-132">カスタム クエリはエンティティで定義されます。</span><span class="sxs-lookup"><span data-stu-id="df548-132">The custom query is defined in the entity.</span></span> |

    > [!NOTE]
    > <span data-ttu-id="df548-133">変更がトリガーされた場合、変更はフィールド レベルではなくレコード全体で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="df548-133">If a change is triggered, the change is tracked on the entire record and not at the field level.</span></span> <span data-ttu-id="df548-134">エンティティ レコード全体がエクスポート先にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="df548-134">The entire entity record is exported to the destination.</span></span> <span data-ttu-id="df548-135">選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。</span><span class="sxs-lookup"><span data-stu-id="df548-135">Regardless of the option that you select, the number of fields in the entity is the number that is exported to the destination.</span></span>

## <a name="enable-change-tracking-for-non-byod-scenarios"></a><span data-ttu-id="df548-136">非 BYOD シナリオでの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="df548-136">Enable change tracking for non-BYOD scenarios</span></span>
<span data-ttu-id="df548-137">変更追跡は、非 BYOD シナリオに対して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="df548-137">Change tracking can be enabled for non-BYOD scenarios.</span></span> <span data-ttu-id="df548-138">これには、Finance and Operations アプリの Dataverse 仮想エンティティを介したレコードの変更の取得が含まれます。</span><span class="sxs-lookup"><span data-stu-id="df548-138">This includes retrieving record changes through Dataverse virtual entities for Finance and Operations apps.</span></span> <span data-ttu-id="df548-139">エンティティで変更追跡が有効になっている場合、優先設定ヘッダーとして `odata.track-changes` を追加することで、エンティティの OData エンドポイントから変更点を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="df548-139">When change tracking is enabled for an entity, changes can be retrieved through the entity's OData endpoint by adding `odata.track-changes` as a preference header.</span></span>

<span data-ttu-id="df548-140">エンティティに対する変更追跡の使用の詳細については、「[変更追跡を使用したデータと外部システムとの同期](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df548-140">For more information on using change tracking for an entity, see [Use change tracking to synchronize data with external systems](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems).</span></span>

<span data-ttu-id="df548-141">非 BYOD シナリオで変更追跡を有効化する方法 :</span><span class="sxs-lookup"><span data-stu-id="df548-141">To enable change tracking for non-BYOD scenarios:</span></span>

1. <span data-ttu-id="df548-142">**データ管理** ワークスペースから、**データ エンティティ** リスト ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-142">From the **Data management** workspace, select the **Data entities** list page.</span></span>
2. <span data-ttu-id="df548-143">変更追跡を有効にするエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-143">Select the entity for which you want to enable change tracking.</span></span> 
3. <span data-ttu-id="df548-144">アクション リボンで、**変更追跡** アクションを選択し、エンティティの変更を追跡する方法について必要なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="df548-144">Select the **Change tracking** action on the action ribbon, and select the desired option for how changes should be tracked for the entity.</span></span> <span data-ttu-id="df548-145">使用可能なオプションの詳細については、前述の「[BYOD に対して変更追跡を有効にする](#enable-change-tracking-for-byod)」セクションのテーブルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="df548-145">See the table in the [Enable change tracking for BYOD](#enable-change-tracking-for-byod) section above for detail on the available options.</span></span>

## <a name="custom-query-for-change-tracking"></a><span data-ttu-id="df548-146">変更追跡用のカスタム クエリ</span><span class="sxs-lookup"><span data-stu-id="df548-146">Custom query for change tracking</span></span>
<span data-ttu-id="df548-147">次の例は、エンティティに静的メソッドを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="df548-147">The following example shows how to add a static method to an entity.</span></span> <span data-ttu-id="df548-148">メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df548-148">You must make sure that the method returns a query, and that the root node is the same as the entity.</span></span> <span data-ttu-id="df548-149">たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。</span><span class="sxs-lookup"><span data-stu-id="df548-149">For example, for the Customer entity, the root node is custTable, and the change tracking query for it is also custtable.</span></span>

- <span data-ttu-id="df548-150">クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df548-150">You must enable change tracking on the tables that are part of the query.</span></span>
- <span data-ttu-id="df548-151">エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。</span><span class="sxs-lookup"><span data-stu-id="df548-151">Create a join between the entity and the change tracking query (on the root table) to determine which records have changed in the entity.</span></span>

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
