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
ms.openlocfilehash: da200460c66cb4d69f119c69bf9c1f786b7542098c23d4567538186790b3e10e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766371"
---
# <a name="enable-change-tracking-for-entities"></a>エンティティの変更追跡の有効化

[!include [banner](../includes/banner.md)]

変更追跡は、データ管理を使用して Finance and Operations アプリからのデータの増分エクスポートを有効化します。 増分エクスポートでは、変更されたレコードのみがエクスポートされます。 差分エクスポートを有効にするには、エンティティの変更追跡を有効にする必要があります。 エンティティで追跡を有効にしない場合は、毎回完全なエクスポートしか有効にできません。 

変更追跡は、自分のデータベース (BYOD) シナリオと非 BYOD シナリオの両方に対して有効にできます。 これには、Dataverse 仮想エンティティを介したレコードの変更の取得が含まれます。

> [!NOTE]
> 変更の追跡では、エンティティがサポートしている場合、独自のデータベース (BYOD) および Dataverse 仮想エンティティのユース ケースに対してのみレコードの削除を追跡します。 他の非 BYOD シナリオでは、追跡レコードの削除は含まれません。 削除処理は エンティティ内 の ルート データ ソース に対してのみ追跡されます。

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
変更追跡は、非 BYOD シナリオに対して有効にできます。 これには、Finance and Operations アプリの Dataverse 仮想エンティティを介したレコードの変更の取得が含まれます。 エンティティで変更追跡が有効になっている場合、優先設定ヘッダーとして `odata.track-changes` を追加することで、エンティティの OData エンドポイントから変更点を取得することができます。

エンティティに対する変更追跡の使用の詳細については、「[変更追跡を使用したデータと外部システムとの同期](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)」を参照してください。

非 BYOD シナリオで変更追跡を有効化する方法 :

1. **データ管理** ワークスペースから、**データ エンティティ** リスト ページを選択します。
2. 変更追跡を有効にするエンティティを選択します。 
3. アクション リボンで、**変更追跡** アクションを選択し、エンティティの変更を追跡する方法について必要なオプションを選択します。 使用可能なオプションの詳細については、前述の「[BYOD に対して変更追跡を有効にする](#enable-change-tracking-for-byod)」セクションのテーブルを参照してください。

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
