---
title: "エンティティの変更追跡を有効化"
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
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: c2238521ad8a62d494425159ad19eb77740ac1f2
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---
# <a name="enable-change-tracking-for-an-entity-by-using-a-custom-query"></a>カスタム クエリを使用してエンティティの変更追跡を有効化

[!include [banner](../includes/banner.md)]

変更追跡は、Microsoft Dynamics 365 for Finance and Operations のデータを、データ管理を使用して差分エクスポートする機能です。 増分エクスポートでは、変更されたレコードのみがエクスポートされます。 差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。 エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。

## <a name="enable-change-tracking"></a>変更追跡の有効化
データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。

1. **データ管理**ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション**を選択します。
2. データのエクスポート先のデータベースを選択し、**発行** を選択します。

    1 つまたは複数のエンティティをデータベースに公開することができます。 **公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。

3. 公開されているエンティティを選択し、**変更の追跡** を選択します。
4. 環境内の変更追跡の適切なオプションを選択します。

    複数のテーブルを使用してエンティティをモデル化できます。 このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。

    | オプション               | 変更の追跡方法 |
    |----------------------|-------------------------|
    | プライマリ テーブルの有効化 | プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。 セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。 |
    | エンティティ全体の有効化 | エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。 |
    | カスタム クエリの有効化  | エンティティでの変更をトリガーする必要がある一連のカスタム フィールドを任意のテーブルから選択します。 |

    > [!NOTE]
    > 変更が発生した場合、エンティティ レコードが出力先をエクスポートされます。 選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。

## <a name="custom-query-for-change-tracking"></a>変更追跡用のカスタム クエリ
次の例は、エンティティに静的メソッドを追加する方法を示しています。 メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。 たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。

- クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。
- エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。

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

