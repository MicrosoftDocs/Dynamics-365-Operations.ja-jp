---
title: 財務分析コードを公開する読み取り専用エンティティの作成
description: このトピックでは、登録済のトランザクションのエンティティを作成する方法について説明します。
author: robinarh
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 273653
ms.assetid: 119610df-3975-43ce-830b-84fe58266321
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c2151b1e3c15b3076e6eaca4f037366320dc8c9c
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923173"
---
# <a name="create-read-only-entities-that-expose-financial-dimensions"></a>財務分析コードを公開する読み取り専用エンティティの作成
[!include [banner](../includes/banner.md)]


このトピックでは、登録されている登録済のトランザクションのエンティティを作成する方法について説明します。 

> [!NOTE] 
> このトピックは、ソリューション アーキテクチャ チームの Per Baarsoe Jorgensen から得たものです。 顧客と作業時に発生した実際のシナリオを説明します。 

配分を使用して適用された財務分析コードと共にすべての仕入先請求明細行のトランザクションを公開しなければならないシナリオを考えてみましょう。 サード パーティのツールによる簡単な消費が不可欠なので、このシナリオ用のエンティティを作成します。 結果として、エンティティは他の関連するエンティティと結合する必要はなく、単独で値を提供できるべきです。

これらの要件を満たすために、サンプル エンティティを作成するプロセスについて説明します。 (これらの手順はすでに文書化されているため、Microsoft Azure DevOps との統合の手順は省略します。)

## <a name="create-a-basic-entity"></a>基本エンティティの作成
最初のステップは、**新しい品目** を選択して、プロジェクト内に新しい要素を作成することです。. 

[![新しい項目](./media/fd-basic.png)](./media/fd-basic.png)

開いているフォームで、データ モデルの **データ エンティティ** 要素のタイプを選択します。

[![データ要素](./media/fd-element.png)](./media/fd-element.png)

> [!NOTE] 
> 後で名前を変更できないためエンティティに名前を付けるときは注意が必要です。

次に、データ エンティティ ウィザードで、適切なプライマリ データ ソースを選択します。 シナリオでは、このデータ ソースは VendInvoiceTrans です。

[![データ エンティティ ウィザード](./media/fd-wizard.png)](./media/fd-wizard.png)

VendInvoiceTrans の場合のように、ウィザードは自然キーを持たないテーブルを受け入れません。 したがって、次のエラー メッセージが表示される場合があります。

[![ナチュラル キーのエラー](./media/fd-error.png)](./media/fd-error.png)

この問題を回避するには、VendGroup などの自然なキーが関連付けられている他のプライマリ データ ソースを選択します。

このデータ ソースは実際には必要ないので、フィールドも必要ありません。 したがって、**すべて選択** チェック ボックスをオフにします。

[![すべての選択を解除](./media/fd-wizard2.png)](./media/fd-wizard2.png)

最後に、**完了** をクリックして、エンティティのテンプレートを作成します。

## <a name="customize-the-basic-entity"></a>基本的なエンティティをカスタマイズします。
エンティティ、ステージング テーブル、およびセキュリティ資産が作成され、カスタム エンティティを作成できるようになりました。 プロジェクトでは、デザイナーで VendorInvoiceTransactionDetailsEntity エンティティを開きます。 

[![デザイナーの VendorInvoiceTransactionDetailsEntity](./media/fd-designer.png)](./media/fd-designer.png)

デザイナーで、ウィザードに適用したダミー テーブル (VendGroup) を、トランザクション テーブル VendInvoiceTrans に変えます。 フィールドの追加を選択しなかったため、エンティティのフィールドを削除する必要はありません。

[![データ エンティティのタイプ](./media/fd-menu.png)](./media/fd-menu.png)

> [!NOTE] 
> このエンティティを使用してトランザクション データを公開するため、エンティティを読み取り専用としてマークすることが重要です。 そのため、トップ ノードで **Is read only** プロパティを **Yes** に設定します。 勘定配布はバージョン管理されているため、クエリを実行するときに現在のバージョンのみが返されることが重要です。 したがって、この部分を複数のエンティティ間で簡単に再利用できるようにするビューを作成します。 

[![VendInvoiceTrans と置き換え](./media/fd-menu2.png)](./media/fd-menu2.png)

プロパティで、**ReferenceDistribution** に **0** の範囲フィルター値、**ReferenceRole** に **1** の範囲フィルター値を代入します。 AccountDistributionReverse データ ソースの結合モード プロパティは、**NoExistsJoin** である必要があります。 新しいビューを配置した後、現在作成している VendorInvoiceTransactionDetailsEntity エンティティに追加できます。 

[![VendorInvoiceTransactionDetailsEntity の追加](./media/fd-menu3.png)](./media/fd-menu3.png)

## <a name="expose-financial-dimensions-as-fields"></a>財務分析コードをフィールドとして公開
次の重要なステップは、財務分析コードをエンティティ上の異なるフィールドとして公開することです。 シナリオは転記済トランザクションの上に構築されるため、フィールドを DimensionCombinationentity エンティティに追加する必要があります。 拡張機能による方法を使用して復元力のある方法で調整を行います。これにより、コード ベースを新しいバージョンに今後アップグレードするとき、必要なメンテナンスは最小限になります。

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-version-1611"></a>Microsoft Dynamics 365 for Finance and Operations Enterprise Edition バージョン 1611

バージョン 1611 以降については、Microsoft Visual Studio (**Dynamics 365** &gt; **アドイン** &gt; **Odata の財務分析コードの追加**) で利用できるウィザードを使用する必要があります。 手順については、[Excel テンプレートに分析コードを追加する](dimensions-overview.md) を参照してください。

### <a name="earlier-versions"></a>以前のバージョン

以前のバージョンで作業している場合、ここで説明されている手順を完了する必要があります。 最初に、エンティティ拡張機能自体を追加します。 コンテキスト メニュー (ショートカット メニュー) で **拡張機能を作成** を選択します。 次に、データを取得するコードを作成します。 エンティティ拡張子が既に確立されているため、新しいクラスを作成する必要があります。 次の例では、**ProductLine** という名前の任意の分析コードを追加します。.
    
```xpp    
[ExtensionOf(dataentityviewstr(DimensionCombinationentity))]
  public final class DimensionCombinationentity_Extension
  {
    private static server str getEmptyOrDimensionValueSqlString(str _attributeName)
    {
        str sqlStatement;

        DimensionAttribute dimensionAttribute = DimensionAttribute::findByName(_attributeName);

        if (!dimensionAttribute)
        {
            sqlStatement = SysComputedColumn::returnLiteral('');
        }
        else
        {
            sqlStatement = strFmt('SELECT TOP 1 T1.%1 ', dimensionAttribute.DimensionValueColumnName);
        }

        return sqlStatement;
    }

    /// Generates the sql to populate the FOTA view field.
    public static server str ProductLineValue()
    {
        return DimensionCombinationentity::getEmptyOrDimensionValueSqlString('ProductLine');
    }
  }
```

これらのメソッドを参照するカスタム フィールドを使用して、新たに作成されたエンティティ拡張機能にフィールドを追加しました。 

[![フィールドの追加](./media/fd-menu4.png)](./media/fd-menu4.png)

次に、フィールドがマップされておらず、拡張機能クラスに対して作成したコードを通じて取得する必要があることを反映するためにプロパティ値を設定します。 リレーションを作成するとき、次の値も設定します。

-   カーディナリティ: **ZeroMore**
-   関連データ エンティティ: **DimensionCombinationentity**
-   関連データ エンティティ カーディナリティ: **ZeroOne**
-   関係タイプ: **関連**

[![関係の作成](./media/fd-menu5.png)](./media/fd-menu5.png)

> [!Note]
> クラス名でデータ メソッドを完全に修飾する必要があります。 

新しい VendInvoiceTransactionentity エンティティに DimensionCombinationentity エンティティを追加する準備が整いました。 

[![DimensionCombinationentity の追加](./media/fd-menu6.png)](./media/fd-menu6.png)

AccountingDistributionCurrent と DimensionCombinationentity エンティティの両方が外部結合であることに注意します。 

[![外部結合](./media/fd-menu7.png)](./media/fd-menu7.png)

ここで、新しいエンティティで必須フィールドをさまざまなデータ ソースから **フィールド** ノード (つまり、新たに作成された ProductLine) にドラッグする必要があります。 

[![ProductLine にドラッグ](./media/fd-menu8.png)](./media/fd-menu8.png)

エクスポートの構成時に差分更新機能を有効にするために、エンティティにキーを追加する必要があります。 したがって、VendInvoiceTrans データ ソースの RecId が、たとえば VendInvoiceTransRecId と名付けられたフィールドの一部であることを確認する必要があります。 フィールドがフィールドリストに入った後、フィールドを **EntityKey** ノードにドラッグできます。 

[![EntityKey にドラッグ](./media/fd-menu9.png)](./media/fd-menu9.png)

ステージング テーブルが完全に構成されたエンティティに関連付けられていることを確認するには、ステージング テーブルを更新する必要があります。 エンティティのコンテキスト メニューで、**ステージング テーブルの更新** を選択します。 

[![ステージング テーブルの更新](./media/fd-menu10.png)](./media/fd-menu10.png)

エンティティの作業が完了したら、それを構築することができます。 

> [!NOTE]
> このシナリオでは、LedgerDimension が DimensionCombinationentity エンティティに関連付けられました。 DefaultDimension があるシナリオでは、DimensionSetentity エンティティに関連付ける必要があります。 必要な強化と拡張は、DimensionCombinationentity エンティティに対して行った強化と拡張と同じです。

## <a name="additional-resources"></a>追加リソース

[Dynamics AX 7 のエンティティを自分の Azure SQL データベースにエクスポートする](/archive/blogs/dynamicsaxbi/export-dynamics-ax7-entities-to-your-own-azure-sql-database)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]