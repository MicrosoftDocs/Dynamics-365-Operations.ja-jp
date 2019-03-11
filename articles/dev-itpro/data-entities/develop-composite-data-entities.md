---
title: 複合データ エンティティの開発
description: 複合エンティティは、相互に関連する複数のエンティティを利用して単一のエンティティを構築できる概念です。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 18411
ms.assetid: 1cb19868-cbfd-4f45-bc47-39b9f303583d
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fdfe2f472ae8b052446a1db48cdedd5f4855ebc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368540"
---
# <a name="develop-composite-data-entities"></a>複合データ エンティティの開発

[!include [banner](../includes/banner.md)]

複合エンティティは、相互に関連する複数のエンティティを利用して単一のエンティティを構築できる概念です。

## <a name="what-is-a-composite-entity"></a>複合エンティティとは何ですか ?

複合エンティティは、互いに関連する複数のエンティティを活用して単一のエンティティを構築できるコンセプトです。 この概念は、エンティティを販売ヘッダー/行、請求書ヘッダー/明細および仕入先カタログなどの単一の文書として表すことができるシナリオで頻繁に使用されます。 この概念は、同期 OData シナリオではなく非同期統合シナリオに適用され、データ管理プラットフォームからのみサポートされます。 X++ には複合エンティティ用のプログラム的なインターフェイスはありません。 XML ファイルに基づくインポート/エクスポートの一部であるデータ管理プラットフォームのみでサポートされます。

## <a name="example"></a>例
売上ヘッダーと販売明細行は、システムの 2 つの異なるエンティティです。 顧客の要求がそのヘッダーを示し、明細行が 1 つのドキュメントの一部である場合、これら 2 つのエンティティは複合エンティティとしてマージすることができます。 サンプル販売注文エンティティ: 複合エンティティ (MySalesTableCompositeEntity) は、販売注文ヘッダー エンティティ (MySalesTableEntity) と販売注文明細行エンティティ (MySalesTableLineEntity) から構成される販売注文ドキュメントを表します。

[![DevelopingCompositeEntities (17)](./media/developingcompositeentities-17-1024x290.png)](./media/developingcompositeentities-17.png)

リンクされたエンティティに基づいて、これらのエンティティは、エンティティの埋め込み要素タグを持つ XML ドキュメントとして公開されます。 XML はデータ管理で複合エンティティを公開する唯一の方法です。

```
<?xml version="1.0" encoding="utf-8"?>
<Document>

<MySalesTableEntity SalesID="SO1" CurrencyCode="USD" CustAccount="Acc001">
<MySalesLineEntity SalesPrice="2.00" QtyOrdered="10.00" LineAmount="20.00" ItemId="1000" LineNum="1.00" SalesID="SO1"/>
<MySalesLineEntity SalesPrice="2.00" QtyOrdered="10.00" LineAmount="20.00" ItemId="4401" LineNum="2.00" SalesID="SO1"/>
</MySalesTableEntity>

<MySalesTableEntity SalesID="SO2" CurrencyCode="USD" CustAccount="Acc002">
<MySalesLineEntity SalesPrice="2.00" QtyOrdered="10.00" LineAmount="20.00" ItemId="4402" LineNum="1.00" SalesID="SO2"/>
</MySalesTableEntity>

</Document>
```

XML 内の各ノードでは、個々のエンティティから属性を表します。 たとえば - &lt;MySalesTableEntity SalesID="SO1" CurrencyCode="USD" CustAccount="Acc001"&gt; SalesId、CurrencyCode および CustAccount は MySalesTableEntity からの属性です。

## <a name="building-the-composite-entity"></a>複合エンティティの作成
データ モデルの下に複合データ エンティティのノードがあります。 MySalesTableEntity の例を取り上げてみましょう。

### <a name="step-1-identify-and-create-the-individual-entities-for-the-composite-entity"></a>手順 1: 複合エンティティの個々のエンティティを識別して作成する

エンティティが相互に関連していることを確認します。 この例では、個々のエンティティは MySalesTableEntity および MySalesLineEntity です。

### <a name="step-2-add-relations-between-individual-entities"></a>手順 2: 個々のエンティティの間の関係を追加する

リレーション ノードの親エンティティへのリレーションを追加します。 例 – MySalesLineEntity は、MySalesTableEntity と関係性があります。

[![DevelopingCompositeEntities (18)](./media/developingcompositeentities-18.png)](./media/developingcompositeentities-18.png)

### <a name="step-3-create-a-new-composite-entity"></a>手順 3: 新しい複合エンティティを作成する

1. **Composite entity** タイプの新しい **Dynamics 365** コンポーネント品目をプロジェクトに追加します。
2. デザイナー モードで、エンティティを右クリックし、**新しいルート データ エンティティ参照**を選択します。

    [![DevelopingCompositeEntities (2)](./media/developingcompositeentities-2.png)](./media/developingcompositeentities-2.png)

3. 親データ エンティティにデータ エンティティを設定します。 ここでは、MySalesTableEntity です。
4. 親エンティティ ノードを右クリックし、**新しい埋め込みデータ エンティティ参照** を選択します。

    [![DevelopingCompositeEntities (3)](./media/developingcompositeentities-3.png)](./media/developingcompositeentities-3.png)

5. 子エンティティとして埋め込みデータ エンティティを設定します。 ここでは、MySalesLineEntity です。
6. 埋め込みデータ エンティティ プロパティのドロップダウン リストから **関係** プロパティを設定します。

    [![DevelopingCompositeEntities (4)](./media/developingcompositeentities-4.png)](./media/developingcompositeentities-4.png)

7. 複合エンティティには、複数レベルの子エンティティがサポートされています。

### <a name="step-4-create-relationships-between-staging-tables"></a>手順 4: ステージング テーブル間の関係を作成する

ナチュラル キーに基づいたエンティティ ステージング テーブルの親と子間の関係を作成する必要があります。 たとえば、MySalesTable および MySalesLine のステージング テーブルは、SalesID、DefinitionGroup、および ExecutionId によってリンクされます。

1. MySalesLineStaging テーブルの外部キー関係を追加します。

    [![DevelopingCompositeEntities (5)](./media/developingcompositeentities-5.png)](./media/developingcompositeentities-5.png)

2. 複合データ エンティティに関連付けられているすべてのステージング テーブルに、2 つの列、RowId と ParentRowId (int 型) を追加します。 列のプロパティについては、SysCompositeHeaderStaging テーブルを参照してください。

    [![DevelopingCompositeEntities (7)](./media/developingcompositeentities-7.png)](./media/developingcompositeentities-7.png)

これらの列は、ターゲット データのランタイム リレーションシップを定義するために使用されます。

- RowId、ParentRowid、DefinitionGroup、および ExecutionId を含むステージング テーブルにクラスター インデックスを作成します。 これは、パフォーマンス上の理由によります。
- コンポーネントをコンパイルして同期します。

### <a name="step-5-set-up-the-metadata-for-dmfentity"></a>手順 5: DMFEntity のメタデータを設定する

ローカル テストで、複合エンティティ メタデータは更新される必要があります。

1. **DIXF パラメータ &gt; エンティティ設定**に移動します。 **エンティティ リストの更新**をクリックします。

    [![DevelopingCompositeEntities (8)](./media/developingcompositeentities-8-1024x212.png)](./media/developingcompositeentities-8.png)

2. 別の方法として、複合エンティティ リストのメタデータを更新するために次のジョブを書き込むことができます。

    ```
    DMFDataPopulation::refreshCompositeEntityList();
    ```

3. ジョブを実行します。 エンティティ ルックアップに必要なメタデータが更新されます。

> [!NOTE]
> 現在これが回避方法です。 今後、コンパイル/同期時にリストを更新する機能が有効になります。

### <a name="step-6-test-the-entity-locally"></a>手順 6: ローカル エンティティをテストする

DIXF 標準プロセスからの通常のエンティティとして、データをインポートおよびエクスポートすることをお勧めします。 エンティティのインポートとエクスポートの以下の手順をご覧ください。

> [!NOTE]
> ソース タイプの XML-属性または XML-要素は、複合エンティティでサポートされています。

## <a name="import-a-composite-entity"></a>複合エンティティのインポート
1. **インポート** をクリックします。
2. **名前**、**ソース データ フォーマット**、および**エンティティ名**を入力します。
3. **ソース データ形式** は、xml-attribute または xml-element です。
4. **今すぐインポート**をクリックします。
5. 作成/更新/保留中のレコードの数が表示されます。

## <a name="export-a-composite-entity"></a>複合エンティティをエキスポート
1. **エクスポート** をクリックします。
2. **名前**、**ソース データ フォーマット**、**およびエンティティ名**を入力します。
3. **エンティティの追加**および**今すぐエクスポート**をクリックします。
4. **ダウンロード パッケージ**をクリックします。

## <a name="general-troubleshooting-guidelines"></a>トラブルシューティングの一般的なガイドライン
- 問題: エクスポートされた複合 XML ファイルがインポートされません。 これを生成するシナリオは次のとおりです。

    - 複合エンティティのファイルをエキスポートします。
    - 同じファイルをインポートします。
    - マッピングに失敗し、ファイルがインポートされません。

- 根本原因:

    - エクスポートされたファイルに行または関連する子エンティティ情報があるかどうかを確認します。
    - 明細行または関連する子エンティティについての情報がある場合、明細行はインポート中にマップされません。

- 解決策: 

    - すべての子のエンティティを含むサンプル ファイルを作成します。
    - このファイルは初期マッピングにのみ使用します。
    - マッピングに成功したら、明細行データがエンティティに含まれていない実際のファイルをインポートします。 再インポートを使用するか、新しいファイルをアップロードします。
    - レコードの有効性に応じて、部分データ (空の子レコード) を含むファイルをインポートする必要があります。
