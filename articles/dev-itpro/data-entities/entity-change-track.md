---
title: エンティティへの変更追跡の有効化
description: Microsoft Dynamics 365 for Finance and Operations からのデータの差分エクスポートを有効にする追跡の変更を使用します。
author: Milindav2
manager: AnnBe
ms.date: 02/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 265974
ms.assetid: 434b5d9f-9877-4769-ad96-d4e8d460a7fa
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22bd043c6a21b8fae2f4f76ba21e3556ce3f06a3
ms.sourcegitcommit: 916c969a89bc436f7ea7ddcc6f3370e4f1eef632
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/11/2019
ms.locfileid: "378100"
---
# <a name="enable-change-tracking-for-entities"></a><span data-ttu-id="f8d37-103">エンティティの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="f8d37-103">Enable change tracking for entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8d37-104">変更追跡は、データ管理を使用して Microsoft Dynamics 365 for Finance and Operations からのデータの差分エクスポートを有効化します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-104">Change tracking enables incremental export of data from Microsoft Dynamics 365 for Finance and Operations by using Data management.</span></span> <span data-ttu-id="f8d37-105">増分エクスポートでは、変更されたレコードのみがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-105">In an incremental export, only records that have changed are exported.</span></span> <span data-ttu-id="f8d37-106">差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8d37-106">To enable incremental export, you must enable change tracking on entities.</span></span> <span data-ttu-id="f8d37-107">エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。</span><span class="sxs-lookup"><span data-stu-id="f8d37-107">If you don't enable change tracking on an entity, you can only enable a full export each time.</span></span> <span data-ttu-id="f8d37-108">BYOD と BYOD 以外のシナリオで変更の追跡を有効にすることができますが、必要があることのみを表示、自分のデータベースの持ち込み (BYOD) ユース ケースでのみ、エンティティでこれがサポートされている場合は変更の追跡が削除を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-108">Although, change tracking can be enabled for BYOD and non-BYOD scenarios, it must be noted that only for bring your own database (BYOD) use cases, change tracking also tracks deletes if the entity supports this.</span></span>

## <a name="enable-change-tracking-for-byod"></a><span data-ttu-id="f8d37-109">BYOD の変更追跡を有効する</span><span class="sxs-lookup"><span data-stu-id="f8d37-109">Enable change tracking for BYOD</span></span>
<span data-ttu-id="f8d37-110">データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-110">You can enable change tracking when you publish one or more entities to a data store (BYOD).</span></span>

1. <span data-ttu-id="f8d37-111">**データ管理**ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-111">In the **Data management** workspace, select **Configure entity export to database**.</span></span>
2. <span data-ttu-id="f8d37-112">データのエクスポート先のデータベースを選択し、**発行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-112">Select the database to export data to, and then select **Publish**.</span></span>

    <span data-ttu-id="f8d37-113">1 つまたは複数のエンティティをデータベースに公開することができます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-113">You can publish one or more entities to your database.</span></span> <span data-ttu-id="f8d37-114">**公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-114">Select **Show published only** to see a list of entities that have previously been published.</span></span>

3. <span data-ttu-id="f8d37-115">公開されているエンティティを選択し、**変更の追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-115">Select an entity that is published, and then select **Change tracking**.</span></span>
4. <span data-ttu-id="f8d37-116">環境内の変更追跡の適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-116">Select the appropriate option for change tracking for your environment.</span></span>

    <span data-ttu-id="f8d37-117">複数のテーブルを使用してエンティティをモデル化できます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-117">An entity can be modeled by using more than one table.</span></span> <span data-ttu-id="f8d37-118">このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-118">The options let you specify the granularity at which changes can be tracked in an entity.</span></span>

    | <span data-ttu-id="f8d37-119">オプション</span><span class="sxs-lookup"><span data-stu-id="f8d37-119">Option</span></span>               | <span data-ttu-id="f8d37-120">変更の追跡方法</span><span class="sxs-lookup"><span data-stu-id="f8d37-120">How changes are tracked</span></span> |
    |----------------------|-------------------------|
    | <span data-ttu-id="f8d37-121">プライマリ テーブルの有効化</span><span class="sxs-lookup"><span data-stu-id="f8d37-121">Enable primary table</span></span> | <span data-ttu-id="f8d37-122">プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="f8d37-122">Changes that are made to any fields in the primary table trigger a change in entity.</span></span> <span data-ttu-id="f8d37-123">セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。</span><span class="sxs-lookup"><span data-stu-id="f8d37-123">Changes that are made to fields in secondary tables don't trigger a change in entity.</span></span> |
    | <span data-ttu-id="f8d37-124">エンティティ全体の有効化</span><span class="sxs-lookup"><span data-stu-id="f8d37-124">Enable entire entity</span></span> | <span data-ttu-id="f8d37-125">エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。</span><span class="sxs-lookup"><span data-stu-id="f8d37-125">Changes that are made to any fields in any table in the entity trigger a change in entity.</span></span> |
    | <span data-ttu-id="f8d37-126">カスタム クエリの有効化</span><span class="sxs-lookup"><span data-stu-id="f8d37-126">Enable Custom query</span></span>  | <span data-ttu-id="f8d37-127">エンティティでの変更をトリガーする必要がある一連のカスタム フィールドを任意のテーブルから選択します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-127">Select a set of custom fields from any tables that must trigger a change in entity.</span></span> |

    > [!NOTE]
    > <span data-ttu-id="f8d37-128">変更がトリガーされた場合、変更はフィールド レベルではなくレコード全体で追跡されます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-128">If a change is triggered, the change is tracked on the entire record and not at the field level.</span></span> <span data-ttu-id="f8d37-129">エンティティ レコード全体がエクスポート先にエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-129">The entire entity record is exported to the destination.</span></span> <span data-ttu-id="f8d37-130">選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。</span><span class="sxs-lookup"><span data-stu-id="f8d37-130">Regardless of the option that you select, the number of fields in the entity is the number that is exported to the destination.</span></span>

## <a name="enable-change-tracking-for-non-byod-scenarios"></a><span data-ttu-id="f8d37-131">非 BYOD シナリオでの変更追跡の有効化</span><span class="sxs-lookup"><span data-stu-id="f8d37-131">Enable change tracking for non-BYOD scenarios</span></span>
<span data-ttu-id="f8d37-132">非 BYOD シナリオでは、変更追跡は、エンティティを選択して **変更追跡**をクリックすることによって、データ管理のデータ エンティティ リスト ページから有効にできます。</span><span class="sxs-lookup"><span data-stu-id="f8d37-132">For non-BYOD scenarios, change tracking can be enabled from the data entities list page in data management by selecting the entities and clicking **Change tracking**.</span></span>

## <a name="custom-query-for-change-tracking"></a><span data-ttu-id="f8d37-133">変更追跡用のカスタム クエリ</span><span class="sxs-lookup"><span data-stu-id="f8d37-133">Custom query for change tracking</span></span>
<span data-ttu-id="f8d37-134">次の例は、エンティティに静的メソッドを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f8d37-134">The following example shows how to add a static method to an entity.</span></span> <span data-ttu-id="f8d37-135">メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8d37-135">You must make sure that the method returns a query, and that the root node is the same as the entity.</span></span> <span data-ttu-id="f8d37-136">たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。</span><span class="sxs-lookup"><span data-stu-id="f8d37-136">For example, for the Customer entity, the root node is custTable, and the change tracking query for it is also custtable.</span></span>

- <span data-ttu-id="f8d37-137">クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8d37-137">You must enable change tracking on the tables that are part of the query.</span></span>
- <span data-ttu-id="f8d37-138">エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。</span><span class="sxs-lookup"><span data-stu-id="f8d37-138">Create a join between the entity and the change tracking query (on the root table) to determine which records have changed in the entity.</span></span>

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
