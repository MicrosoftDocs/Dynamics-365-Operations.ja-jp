---
title: エンティティへの変更追跡の有効化
description: Finance and Operations からのデータの差分エクスポートを有効にする追跡の変更を使用します。
author: Milindav2
manager: AnnBe
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 265974
ms.assetid: 434b5d9f-9877-4769-ad96-d4e8d460a7fa
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30eb0a6ad9b9706e80a8470bee0e4c43c12100df
ms.sourcegitcommit: ac5c13f2c880aa5b3db3720ec93ae8dcccc1c214
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/08/2020
ms.locfileid: "3543070"
---
# <a name="enable-change-tracking-for-entities"></a><span data-ttu-id="f12bb-103">エンティティの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="f12bb-103">Enable change tracking for entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f12bb-104">変更追跡は、データ管理を使用して Finance and Operations からのデータの差分エクスポートを有効化します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-104">Change tracking enables incremental export of data from Finance and Operations by using Data management.</span></span> <span data-ttu-id="f12bb-105">増分エクスポートでは、変更されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-105">In an incremental export, only records that have changed are exported.</span></span> <span data-ttu-id="f12bb-106">差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12bb-106">To enable incremental export, you must enable change tracking on entities.</span></span> <span data-ttu-id="f12bb-107">エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。</span><span class="sxs-lookup"><span data-stu-id="f12bb-107">If you don't enable change tracking on an entity, you can only enable a full export each time.</span></span> <span data-ttu-id="f12bb-108">BYOD と BYOD 以外のシナリオで変更の追跡を有効にすることができますが、必要があることのみを表示、自分のデータベースの持ち込み (BYOD) ユース ケースでのみ、エンティティでこれがサポートされている場合は変更の追跡が削除を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-108">Although, change tracking can be enabled for BYOD and non-BYOD scenarios, it must be noted that only for bring your own database (BYOD) use cases, change tracking also tracks deletes if the entity supports this.</span></span> <span data-ttu-id="f12bb-109">削除処理は エンティティ内 の ルート データ ソース に対してのみ追跡されます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-109">Deletion is tracked only for the root data source in the entity.</span></span>

## <a name="enable-change-tracking-for-byod"></a><span data-ttu-id="f12bb-110">BYOD の変更追跡を有効する</span><span class="sxs-lookup"><span data-stu-id="f12bb-110">Enable change tracking for BYOD</span></span>
<span data-ttu-id="f12bb-111">データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-111">You can enable change tracking when you publish one or more entities to a data store (BYOD).</span></span>

1. <span data-ttu-id="f12bb-112">**データ管理**ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-112">In the **Data management** workspace, select **Configure entity export to database**.</span></span>
2. <span data-ttu-id="f12bb-113">データのエクスポート先のデータベースを選択し、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-113">Select the database to export data to, and then select **Publish**.</span></span>

    <span data-ttu-id="f12bb-114">1 つまたは複数のエンティティをデータベースに公開することができます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-114">You can publish one or more entities to your database.</span></span> <span data-ttu-id="f12bb-115">**公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-115">Select **Show published only** to see a list of entities that have previously been published.</span></span>

3. <span data-ttu-id="f12bb-116">公開されているエンティティを選択し、**変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-116">Select an entity that is published, and then select **Change tracking**.</span></span>
4. <span data-ttu-id="f12bb-117">環境内の変更追跡の適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-117">Select the appropriate option for change tracking for your environment.</span></span>

    <span data-ttu-id="f12bb-118">複数のテーブルを使用してエンティティをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-118">An entity can be modeled by using more than one table.</span></span> <span data-ttu-id="f12bb-119">このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-119">The options let you specify the granularity at which changes can be tracked in an entity.</span></span>

    | <span data-ttu-id="f12bb-120">オプション</span><span class="sxs-lookup"><span data-stu-id="f12bb-120">Option</span></span>               | <span data-ttu-id="f12bb-121">変更の追跡方法</span><span class="sxs-lookup"><span data-stu-id="f12bb-121">How changes are tracked</span></span> |
    |----------------------|-------------------------|
    | <span data-ttu-id="f12bb-122">プライマリ テーブルの有効化</span><span class="sxs-lookup"><span data-stu-id="f12bb-122">Enable primary table</span></span> | <span data-ttu-id="f12bb-123">プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="f12bb-123">Changes that are made to any fields in the primary table trigger a change in entity.</span></span> <span data-ttu-id="f12bb-124">セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。</span><span class="sxs-lookup"><span data-stu-id="f12bb-124">Changes that are made to fields in secondary tables don't trigger a change in entity.</span></span> |
    | <span data-ttu-id="f12bb-125">エンティティ全体の有効化</span><span class="sxs-lookup"><span data-stu-id="f12bb-125">Enable entire entity</span></span> | <span data-ttu-id="f12bb-126">エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="f12bb-126">Changes that are made to any fields in any table in the entity trigger a change in entity.</span></span> |
    | <span data-ttu-id="f12bb-127">カスタム クエリの有効化</span><span class="sxs-lookup"><span data-stu-id="f12bb-127">Enable Custom query</span></span>  | <span data-ttu-id="f12bb-128">変更を追跡する必要があるテーブルを識別するカスタム クエリを使用します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-128">Uses a custom query that identifies the tables on which changes must be tracked.</span></span> <span data-ttu-id="f12bb-129">カスタム クエリはエンティティで定義されます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-129">The custom query is defined in the entity.</span></span> |

    > [!NOTE]
    > <span data-ttu-id="f12bb-130">変更がトリガーされた場合、変更はフィールド レベルではなくレコード全体で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-130">If a change is triggered, the change is tracked on the entire record and not at the field level.</span></span> <span data-ttu-id="f12bb-131">エンティティ レコード全体がエクスポート先にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-131">The entire entity record is exported to the destination.</span></span> <span data-ttu-id="f12bb-132">選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。</span><span class="sxs-lookup"><span data-stu-id="f12bb-132">Regardless of the option that you select, the number of fields in the entity is the number that is exported to the destination.</span></span>

## <a name="enable-change-tracking-for-non-byod-scenarios"></a><span data-ttu-id="f12bb-133">非 BYOD シナリオでの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="f12bb-133">Enable change tracking for non-BYOD scenarios</span></span>
<span data-ttu-id="f12bb-134">非 BYOD シナリオでは、変更追跡は、エンティティを選択して **変更追跡**をクリックすることによって、データ管理のデータ エンティティ リスト ページから有効にできます。</span><span class="sxs-lookup"><span data-stu-id="f12bb-134">For non-BYOD scenarios, change tracking can be enabled from the data entities list page in data management by selecting the entities and clicking **Change tracking**.</span></span>

## <a name="custom-query-for-change-tracking"></a><span data-ttu-id="f12bb-135">変更追跡用のカスタム クエリ</span><span class="sxs-lookup"><span data-stu-id="f12bb-135">Custom query for change tracking</span></span>
<span data-ttu-id="f12bb-136">次の例は、エンティティに静的メソッドを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f12bb-136">The following example shows how to add a static method to an entity.</span></span> <span data-ttu-id="f12bb-137">メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12bb-137">You must make sure that the method returns a query, and that the root node is the same as the entity.</span></span> <span data-ttu-id="f12bb-138">たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。</span><span class="sxs-lookup"><span data-stu-id="f12bb-138">For example, for the Customer entity, the root node is custTable, and the change tracking query for it is also custtable.</span></span>

- <span data-ttu-id="f12bb-139">クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f12bb-139">You must enable change tracking on the tables that are part of the query.</span></span>
- <span data-ttu-id="f12bb-140">エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。</span><span class="sxs-lookup"><span data-stu-id="f12bb-140">Create a join between the entity and the change tracking query (on the root table) to determine which records have changed in the entity.</span></span>

```xpp
public static Query defaultCTQuery()
    {
        Query q;
        q = new Query();
        QueryBuildDataSource qbd = q.addDataSource(tablename2id('CustTable'));
        qbd = qbd.addDataSource(tablename2id('DirPartyTable'));
        qbd.relations(true);
        qbd = qbd.addDataSource(tablename2id('DirPartyLocation'));
        qbd.addRange(fieldname2id(tablename2id('DirPartyLocation'),'IsPrimary')).value("1");
        qbd.relations(false);
        qbd.addLink(fieldName2Id(tableName2Id('DirPartyTable'),'RecId'),fieldName2Id(tableName2Id('DirPartyLocation'),'Party'));
        qbd = qbd.addDataSource(tableName2Id('LogisticsPostalAddress'));
        qbd.relations(false);
        qbd.addLink(fieldName2Id(tableName2Id('DirPartyLocation'),'Location'),fieldName2Id(tableName2Id('LogisticsPostalAddress'),'Location'));
        return q;
    }
```
