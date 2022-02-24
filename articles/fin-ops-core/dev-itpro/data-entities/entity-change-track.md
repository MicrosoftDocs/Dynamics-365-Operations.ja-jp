---
title: エンティティへの変更追跡の有効化
description: Finance and Operations からのデータの差分エクスポートを有効にする追跡の変更を使用します。
author: Milindav2
manager: AnnBe
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.custom: 265974
ms.assetid: 434b5d9f-9877-4769-ad96-d4e8d460a7fa
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 402fce89b2531a967435f7daabd40c78cd761978
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685469"
---
# <a name="enable-change-tracking-for-entities"></a>エンティティの変更追跡の有効化

[!include [banner](../includes/banner.md)]

変更追跡は、データ管理を使用して Finance and Operations からのデータの差分エクスポートを有効化します。 増分エクスポートでは、変更されたレコードのみがエクスポートされます。 差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。 エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。 BYOD と BYOD 以外のシナリオで変更の追跡を有効にすることができますが、必要があることのみを表示、自分のデータベースの持ち込み (BYOD) ユース ケースでのみ、エンティティでこれがサポートされている場合は変更の追跡が削除を追跡できます。 削除処理は エンティティ内 の ルート データ ソース に対してのみ追跡されます。

## <a name="enable-change-tracking-for-byod"></a>BYOD の変更追跡を有効する
データ ストア (BYOD) に 1 つまたは複数のエンティティを発行するとき、変更追跡を有効にすることができます。

1. **データ管理** ワークスペースで、**データベースへのエンティティのエクスポートのコンフィギュレーション** を選択します。
2. データのエクスポート先のデータベースを選択し、**発行** を選択します。

    1 つまたは複数のエンティティをデータベースに公開することができます。 **公開のみ表示** を選択し、既に公開されているエンティティの一覧を表示します。

3. 公開されているエンティティを選択し、**変更の追跡** を選択します。
4. 環境内の変更追跡の適切なオプションを選択します。

    複数のテーブルを使用してエンティティをモデル化できます。 このオプションを使用すると、エンティティ内で変更を追跡できる精度を指定できます。

    | オプション               | 変更の追跡方法 |
    |----------------------|-------------------------|
    | プライマリ テーブルの有効化 | プライマリ テーブルの任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。 セカンダリ テーブルのフィールドに加えられた変更は、エンティティの変更をトリガーしません。 |
    | エンティティ全体の有効化 | エンティティの任意のテーブルの、任意のフィールドに加えられた変更は、エンティティの変更をトリガーします。 |
    | カスタム クエリの有効化  | 変更を追跡する必要があるテーブルを識別するカスタム クエリを使用します。 カスタム クエリはエンティティで定義されます。 |

    > [!NOTE]
    > 変更がトリガーされた場合、変更はフィールド レベルではなくレコード全体で追跡されます。 エンティティ レコード全体がエクスポート先にエクスポートされます。 選択したオプションに関係なく、エンティティのフィールドの数はターゲットにエクスポートされた数になります。

## <a name="enable-change-tracking-for-non-byod-scenarios"></a>非 BYOD シナリオでの変更追跡の有効化
非 BYOD シナリオでは、変更追跡は、エンティティを選択して **変更追跡** をクリックすることによって、データ管理のデータ エンティティ リスト ページから有効にできます。

## <a name="custom-query-for-change-tracking"></a>変更追跡用のカスタム クエリ
次の例は、エンティティに静的メソッドを追加する方法を示しています。 メソッドがクエリを返し、ルート ノードがエンティティと同様であることを確認する必要があります。 たとえば、顧客エンティティについては、ルート ノードは custTable で、その変更追跡クエリも custTable です。

- クエリの一部であるテーブルの変更進捗管理を有効にする必要があります。
- エンティティと変更追跡クエリ (ルート テーブル上) との間に結合を作成し、エンティティ内で変更されたレコードを判断します。

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
