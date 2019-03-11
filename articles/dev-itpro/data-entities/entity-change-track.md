---
title: エンティティへの変更追跡の有効化
description: Microsoft Dynamics 365 for Finance and Operations からのデータの差分エクスポートを有効にする追跡の変更を使用します。
author: Milindav2
manager: AnnBe
ms.date: 08/27/2018
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
ms.openlocfilehash: 1a79787266fb8eca27bde8376fcb7fbf3bc604c6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368952"
---
# <a name="enable-change-tracking-for-entities"></a>エンティティの変更追跡の有効化

[!include [banner](../includes/banner.md)]

変更追跡は、データ管理を使用して Microsoft Dynamics 365 for Finance and Operations からのデータの差分エクスポートを有効化します。 増分エクスポートでは、変更されたレコードのみがエクスポートされます。 差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。 エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。 自分のデータベースの持ち込み (BYOD) ユース ケースでは、データベースでサポートされている場合は変更履歴は削除も追跡できます。

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
    > 変更がトリガーされた場合、変更はフィールド レベルではなくレコード全体で追跡されます。 エンティティ レコード全体がエクスポート先にエクスポートされます。 選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。

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
