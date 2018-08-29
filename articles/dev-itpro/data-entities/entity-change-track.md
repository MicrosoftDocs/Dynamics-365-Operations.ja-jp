---
title: "エンティティへの変更追跡の有効化"
description: "変更追跡を使用して、Microsoft Dynamics 365 for Finance and Operations のデータを差分エクスポートできます。"
author: Milindav2
manager: AnnBe
ms.date: 09/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro, Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 265974
ms.assetid: 434b5d9f-9877-4769-ad96-d4e8d460a7fa
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 72fbe371ccf1bbfd50aed19065c333b54d216b75
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="enable-change-tracking-for-entities"></a><span data-ttu-id="eed30-103">エンティティへの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="eed30-103">Enable change tracking for entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eed30-104">変更追跡は、Microsoft Dynamics 365 for Finance and Operations のデータを、データ管理を使用して差分エクスポートする機能です。</span><span class="sxs-lookup"><span data-stu-id="eed30-104">Change tracking is a feature that enables incremental export of data from Microsoft Dynamics 365 for Finance and Operations, by using Data management.</span></span> <span data-ttu-id="eed30-105">増分エクスポートでは、変更されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="eed30-105">In an incremental export, only records that have changed are exported.</span></span> <span data-ttu-id="eed30-106">差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eed30-106">To enable incremental export, you must enable change tracking on entities.</span></span> <span data-ttu-id="eed30-107">エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。</span><span class="sxs-lookup"><span data-stu-id="eed30-107">If you don't enable change tracking on an entity, you can enable only full export each time.</span></span>

## <a name="enable-change-tracking"></a><span data-ttu-id="eed30-108">変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="eed30-108">Enable change tracking</span></span>
<span data-ttu-id="eed30-109">データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="eed30-109">You can enable change tracking when you publish one or more entities to a data store (BYOD).</span></span>

1. <span data-ttu-id="eed30-110">**データ管理**ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="eed30-110">In the **Data management** workspace, select **Configure entity export to database**.</span></span>
2. <span data-ttu-id="eed30-111">データのエクスポート先のデータベースを選択し、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eed30-111">Select the database to export data to, and then select **Publish**.</span></span>

    <span data-ttu-id="eed30-112">1 つまたは複数のエンティティをデータベースに公開することができます。</span><span class="sxs-lookup"><span data-stu-id="eed30-112">You can publish one or more entities to your database.</span></span> <span data-ttu-id="eed30-113">**公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="eed30-113">Select **Show published only** to see a list of entities that have previously been published.</span></span>

3. <span data-ttu-id="eed30-114">公開されているエンティティを選択し、**変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="eed30-114">Select an entity that is published, and then select **Change tracking**.</span></span>
4. <span data-ttu-id="eed30-115">環境内の変更追跡の適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="eed30-115">Select the appropriate option for change tracking for your environment.</span></span>

    <span data-ttu-id="eed30-116">複数のテーブルを使用してエンティティをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="eed30-116">An entity can be modeled by using more than one table.</span></span> <span data-ttu-id="eed30-117">このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="eed30-117">The options let you specify the granularity at which changes can be tracked in an entity.</span></span>

    | <span data-ttu-id="eed30-118">オプション</span><span class="sxs-lookup"><span data-stu-id="eed30-118">Option</span></span>               | <span data-ttu-id="eed30-119">変更の追跡方法</span><span class="sxs-lookup"><span data-stu-id="eed30-119">How changes are tracked</span></span> |
    |----------------------|-------------------------|
    | <span data-ttu-id="eed30-120">プライマリ テーブルの有効化</span><span class="sxs-lookup"><span data-stu-id="eed30-120">Enable primary table</span></span> | <span data-ttu-id="eed30-121">プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="eed30-121">Changes that are made to any fields in the primary table trigger a change in entity.</span></span> <span data-ttu-id="eed30-122">セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。</span><span class="sxs-lookup"><span data-stu-id="eed30-122">Changes that are made to fields in secondary tables don't trigger a change in entity.</span></span> |
    | <span data-ttu-id="eed30-123">エンティティ全体の有効化</span><span class="sxs-lookup"><span data-stu-id="eed30-123">Enable entire entity</span></span> | <span data-ttu-id="eed30-124">エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="eed30-124">Changes that are made to any fields in any table in the entity trigger a change in entity.</span></span> |
    | <span data-ttu-id="eed30-125">カスタム クエリの有効化</span><span class="sxs-lookup"><span data-stu-id="eed30-125">Enable Custom query</span></span>  | <span data-ttu-id="eed30-126">エンティティでの変更をトリガーする必要がある一連のカスタム フィールドを任意のテーブルから選択します。</span><span class="sxs-lookup"><span data-stu-id="eed30-126">Select a set of custom fields from any tables that must trigger a change in entity.</span></span> |

    > [!NOTE]
    > <span data-ttu-id="eed30-127">変更が発生した場合、エンティティ レコードが出力先をエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="eed30-127">If a change is triggered, the entity record is exported to the destination.</span></span> <span data-ttu-id="eed30-128">選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。</span><span class="sxs-lookup"><span data-stu-id="eed30-128">Regardless of the option that you select, the number of fields in the entity is the number that is exported to the destination.</span></span>

## <a name="custom-query-for-change-tracking"></a><span data-ttu-id="eed30-129">変更追跡用のカスタム クエリ</span><span class="sxs-lookup"><span data-stu-id="eed30-129">Custom query for change tracking</span></span>
<span data-ttu-id="eed30-130">次の例は、エンティティに静的メソッドを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="eed30-130">The following example shows how to add a static method to an entity.</span></span> <span data-ttu-id="eed30-131">メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eed30-131">You must make sure that the method returns a query, and that the root node is the same as the entity.</span></span> <span data-ttu-id="eed30-132">たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。</span><span class="sxs-lookup"><span data-stu-id="eed30-132">For example, for the Customer entity, the root node is custTable, and the change tracking query for it is also custtable.</span></span>

- <span data-ttu-id="eed30-133">クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eed30-133">You must enable change tracking on the tables that are part of the query.</span></span>
- <span data-ttu-id="eed30-134">エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。</span><span class="sxs-lookup"><span data-stu-id="eed30-134">Create a join between the entity and the change tracking query (on the root table) to determine which records have changed in the entity.</span></span>

```
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

