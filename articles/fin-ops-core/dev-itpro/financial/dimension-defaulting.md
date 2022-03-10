---
title: 既定の財務分析コード
description: このトピックでは、財務分析コードがどのように生成されるか、その結合に使用される API、および元帳分析コードの作成に使用する方法について説明します。
author: RyanCCarlson2
ms.date: 01/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2019-01-16
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7291a4824e71c42ec7e67f0680891130a6d1949
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781298"
---
# <a name="default-financial-dimensions"></a>既定の財務分析コード
[!include [banner](../includes/banner.md)]

このトピックでは、既定の財務分析コードについて開発者向けの説明を記載します。 ここでは、分析コードのがどのように生成されるか、その分析に使用される application programming interfaces (API)、および元帳分析コードの作成に使用する方法について説明します。 このトピックには、ユーザーインターフェイス (UI)、SQLテーブルクエリ、およびそれらのクエリの出力例が含まれています。 また、API とその使用例についても説明します。

このトピックでは、デモ データの会社として **USMF** を使用します。

財務分析コードのコンセプトおよび業務プロセスに対する影響について詳細は [財務分析コード](../../../finance/general-ledger/financial-dimensions.md) を参照してください。

### <a name="entering-default-dimensions"></a>既定の分析コードを入力する

250 以上のページによって、既定の財務分析コードを入力できます。 分析コードは、ファストタブに値および説明と共に一覧表示されています。 標準デモデータでは、30以上の分析コードを使用できます。 ただし、次の **財務分析コード** ファストタブには、次の5つの分析コード、BusinessUnit、課、部門、ItemGroup、プロジェクト のみを表示しています。 

![財務分析 ファストタブ。](./media/DefaultDimensionEntry.png "財務分析 ファストタブ")

### <a name="dimensions-list"></a>分析コード リスト

分析コードは、最初に勘定構造の一覧に基づいてフィルター処理されており、これらは現在の会社またはページで指定されている会社の元帳に関連付けられています。 次に、それらの構造に関連付けられている分析コードの一覧と、それらの構造に関連付けられている有効となっている高度なルールの一覧が結合されたリストが表示されます。 

![財務分析 ファストタブ リスト。](./media/FinancialDimensionList.png "財務分析 ファストタブ リスト")

### <a name="ledger-page"></a>元帳 ページ

**元帳** ページ (**一般会計 \> 設定 \> 元帳**) にて、会社の勘定構造を管理できます。 

![USMF 企業 の 台帳ページです。](./media/LedgerStructureConfiguration.png "USMF 企業 の 台帳ページです")

### <a name="account-structures-where-the-number-of-dimensions-varies"></a>分析コードの数が変動する勘定構造

勘定構造で使用する分析コードの数を決定するには **元帳** ページで グリッド上の **勘定構造の設定** を選択し、列の数を数えます。 以下の図は、3つの分析コードを使用しているの勘定構造と、5つの分析コードを使用する勘定構造を示しています。

**3つの分析コードを使っている勘定構造**

![USMF 企業の貸借対照表勘定の構造設定。](./media/BalanceSheetAccountStructureSetup.png "USMF 企業の貸借対照表勘定の構造設定")

**5つの分析コードを使っている勘定構造**

![USMF 企業の損益計算書勘定の構造設定。](./media/PandLAccountStructureSetup.png "USMF 企業の損益計算書勘定の構造設定")

上記の図に示した2つの勘定構造の間には、BusinessUnit、Department、CostCenter, ItemGroup、の4つの固有の分析コードがあります。 これら4つの分析コードは、既定の分析コードの一覧に表示されます。 さらに、高度なルールを介してアカウント構造に連係されている高度なルール構造からの分析コードが検証されます。 この例では、高度なルール構造から分析コードを検証した結果、5番目の分析コードがデフォルトの分析コードのリストに追加されています。

以下の図は、プロジェクト分析コードがデフォルト分析コードのリストに組み込むための高度なルールを示しています。

![損益計算書勘定の構造設定の複雑なルール。](./media/AdvancedRuleLinked.png "損益計算書勘定の構造設定の複雑なルール")

以下の図は、ルール構造を示しています。

![プロジェクトのルール構造。](./media/RuleStructure.png "プロジェクトのルール構造")

この MainAccount 分析コードは、多くの場合は既定の分析コードの一覧には表示されないことに注意してください。 ただし、予算作成は例外となります。 この場合、既定の分析コードの一覧にはMainAccount分析コードが明示的に含まれています。

### <a name="api-for-the-list-of-default-dimensions"></a>既定の分析コード一覧用API

既定のdimensionコントローラである **DimensionDefaultingController** は、会社に適切な分析コードを判断するために **DimensionCache::getDimensionAttributeSetForLedger()** APIを使用します。

## <a name="control-uptake-and-storage"></a>取込と保存の管理

### <a name="form-uptake-and-the-dimensions-data-model"></a>取込みフォームと分析コードデータのモデル

既定の分析コードを表示するすべてのページでは **DimensionDefaultingController** コントローラが使用されています。 このコントローラでは、分析コードが自動的に表示され、値を読み込んで保存するので、対話的な操作を行うことができます。 取込みパターンの詳細については、ホワイト ペーパー [Implementing the Account and Financial Dimensions Framework for Microsoft Dynamics AX 2012 Applications](https://go.microsoft.com/fwlink/?linkid=213133) を参照してください。

### <a name="storage-of-default-dimension-values"></a>既定の分析コード値の保存

分析コードに関連付けられている値は、これらの分析コード値を参照する主テーブルとは別のテーブルに格納されます。 たとえば、LedgerJournalTableテーブルには、DimensionAttributeValueSetテーブル内のレコードへの外部キー参照を保持する **dimensiondefault** 列があります。 このレコードは、表示される一連の値を意味する親レコードです。

![既定の分析コード値。](./media/Part2DefaultDimensionEntry.png "既定の分析コード値")

それぞれの値は、DimensionAttributeValueSetItem テーブルに独立した行として保存されますが、親レコードの外部キーは同じものとなります。

![すべての既定の分析コードを表す SQL 結果。](./media/SQLResultofAllDefaultDimensionValues.png "すべての既定の分析コードを表すSQL結果")

データは、これらのテーブルを介して直接照会できます。 また、以下の図に示すように **DimensionAttributeValueSetItemView** を使用してクエリを実行することもできます。

![DimensionAttributeValueSetItemView を使用したデータの問い合わせ。](./media/SQLofAllDefaultDimensionValues.png "DimensionAttributeValueSetItemView を使用したデータの問い合わせ")

### <a name="empty-values"></a>空の値

分析コードのフレームワークは、値が入力された分析コードについてのみ行を保存します。 空の行に対してはデータが保存されません。 したがって、データが保存された後、フレームワークは値を持たない分析コードについて、それがユーザーが削除したものなのか、そもそも値が入っていないものなのかを区別することができません。 空の値を保存するには、空白であることを意味する値を作成する必要があります。 例えば、**empty**、**n/a**、**\<cleared\>**、または **\*blank\*** などの名前を付けます。 ユーザーは、空白の値に対しては入力時にこの値を選択して、これは空白値入力の既定の動作とすることができます。

### <a name="immutable-data"></a>不変データ

ほとんどの分析コードと同様に、テーブルに挿入されたレコードは変更できません。 これらは最初に作成されますが、その後更新または削除されることがありません。 たとえば、ユーザーがプロジェクトIDを分析コードとして追加し、変更を保存したとします。

![既定の分析コードの入力と入力後の値。](./media/Part2-1DefaultDimensionEntry.png "既定の分析コードの入力と入力後の値")

この場合でも、新しい行が追加された場合でも、SQLクエリは以前と同様の3つの行を返します。 新しい値が追加されると、分析コードフレームワークは新しい値セットレコードと、前の分析コードセットを変更するのではなく、新しい値セットにリンクされている4つの追加の値セットアイテムレコードを作成します。

![新規セットにおけるすべての既定の分析コードを参照する SQL 問い合わせと出力結果 (列の調整済み)。](./media/Part2SQLResultsValueSet.png "新規セットにおけるすべての既定の分析コードを参照するSQL問い合わせと (列の調整がされた) 出力結果")

## <a name="copy-patterns"></a>パターンのコピー

このセクションでは、エンティティ間で既定の分析コードがどのようにコピーされるかについて説明します。

### <a name="copy-vs-merge"></a>コピーとマージ

通常、既定の分析コードは、勘定科目分析コードを作成するために他の分析コードの組み合わせとコピーまたはマージされます。 分析コードフレームワークは、既定の動作の優先順位を設定しません。 各ページまたはプロセスは、ビジネスロジックの要件に基づいて、優先順位を決定します。

以下の例を、"仮想注文" ドキュメントに基づいて進めていきます。 このドキュメントは、品目としてのサービスを含む顧客販売注文であると考えることができます。 または、在庫品目を品目として含む仕入先の発注書であると考えることもできます。 以下の図に示すように、処理内のさまざまな時点で既定の分析コードを入力または上書きすることができます。

![一般的なドキュメントにおける既定の分析コードのソース。](./media/DefaultDimensionSourcesGraph.png "一般的なドキュメントにおける既定の分析コードのソース")

注文ドキュメントの場合は、ビジネスロジックに相当する既定の分析コードが複数用意されています。 この例で使用される発注書のように、ドキュメントヘッダーには既定の分析コードのセットが含まれている場合があります。 この例では、顧客または仕入先のオーダーには一連の既定の分析コードが存在します。 注文のビジネスロジックによっては、これらのさまざまな既定の分析コードの組み合わせによって優先順位が異なる場合があります。 既定の分析コードの中で優先順位が高いものは、他の既定の分析コードを置き換えることがあります。 また、既定の分析コードがマージされる場合もあります。

### <a name="copying-default-dimensions"></a>既定の分析コードをコピーする

以下の図は、ある販売店の主勘定に入力された既定の分析コードを示しています。

![一般的なベンダーのアカウントに入力された既定の分析コード。](./media/DefaultDimensionVendor.png "一般的なベンダーのアカウントに入力された既定の分析コード")

以下の図は、仕入先レコードの既定の分析コード参照に対するSQLクエリを示しています。

![ベンダー レコードにおける既定の分析コードを参照する SQL 問い合わせ。](./media/DefaultDimensions3-SQLVendor.png "ベンダーのレコードにおける既定の分析コードを参照するSQL問い合わせ")

以下の図は、作成された既定の分析コードを示しています。

![既定の分析コードの結果。](./media/DefaultDimensions3-SQLResultVendor.png "既定の分析コードの結果")

以下の図は、この仕入先に対して作成された新しい発注書を示しています。 既定の分析コードがドキュメントヘッダーにコピーされます。

![ドキュメント ヘッダーにコピーされた既定の分析コード (注文書)。](./media/DefaultDimensions3-CopiedToDocHeader.png "ドキュメントヘッダーにコピーされた既定の分析コード (注文書)")

以下の図は、SQLクエリとヘッダレコードへの既定の分析コード参照を示しています。 

![注文書レコードにおける既定の分析コードを参照する SQL 問い合わせと出力結果。](./media/DefaultDimensions3-SQLCopiedToDocHeader.png "注文書レコードにおける既定の分析コードを表示するSQL問い合わせと出力結果")

以下の図にあるように、仕入先を選択するとただちに、発注書ヘッダーに既に存在する分析コードが仕入先の分析コードによって置き換えられます。

![仕入先からコピーされた既定の分析コード。](./media/DefaultDimensions3-SQLResultCopiedToDocHeader.png)

したがって、既定の分析コードの外部キーをコピーする必要があります。 以下の図は、仕入先から購買発注へ既定の分析コードをコピーするために使用されるコードを示しています。

![既定の分析コードをベンダーから注文書へコピーする際に使用するコード。](./media/DefaultDimensions3-6CodetoCopy.png "既定の分析コードをベンダーから注文書へとコピーする際に使用するコード")

次の図は、ユーザーがプロジェクト分析コード値を入力した後のヘッダー分析コードを示しています。 

![ユーザーが修正したドキュメント ヘッダー上の既定の分析コード (注文書)。](./media/DefaultDimensions3-7DocumentHeader.png "ユーザーが修正したドキュメントヘッダー上の既定の分析コード (注文書)")

以下のコードは、ヘッダー レコードの既定の分析コード参照に対する SQL クエリを示しています。

```sql
SELECT RecID, PURCHID, DEFAULTDIMENSION from PurchTable
WHERE PURCHID = '00000125' and DATAAREAID = 'usmf'

SELECT DA.NAME, DISPLAYVALUE, V.DIMENSIONATTRIBUTEVALUESET,
V.SETITEMRECID
FROM DIMENSIONATTRIBUTEVALUESETITEMVIEW V
JOIN DIMENSIONATTRIBUTE DA ON DA.RECID = V.DIMENSIONATTRIBUTE
WHERE V.DIMENSIONATTRIBUTEVALUESET = 52565466755
```

以下の図は、作成された既定の分析コードを示しています。

![注文書レコードにおける更新された既定の分析コードを表示した出力結果。](media/DefaultDimensions3-8SQLResultModifiedDocHearder.png)

ユーザーが **ライン** ビューに切り替えて明細行を入力すると、以下の図に示すように、発注書ヘッダーから既定の分析コードがコピーされます。

![ドキュメントの明細にコピーされた既定の分析コード (注文書明細)。](./media/DefaultDimensions3-9CopiedToLine.png "ドキュメントの明細にコピーされた既定の分析コード (注文書明細)")

以下の図は、外部キー参照を行にコピーするために使用されるコードを示しています。 この例では、明細行はまだ保存されていません。 そのため、既定の分析コードの外部キーは、メモリのテーブルバッファーのみに表示されます。

![既定の分析コードをヘッダーから明細へコピーする際に使用するコード。](./media/DefaultDimensions3-10CodeToCopyToLine.png "既定の分析コードをヘッダーから明細へとコピーする際に使用するコード")

## <a name="merging-patterns"></a>パターンのマージ

このセクションでは、エンティティ間で既定の分析コードがどのようにマージされるかを説明します。

### <a name="merging-default-dimensions"></a>既定の分析コードのマージ

次の図では、ユーザーが行の BusinessUnit 分析コードを手動で削除しました。 その結果、新しい既定の分析コード外部キーが作成され、発注書ヘッダーが更新されます。 

![ドキュメントの明細で修正された既定の分析コード (注文書明細)。](./media/DefaultDimension4-1DimOnLine.png "ドキュメントの明細で修正された既定の分析コード (注文書明細)")

この例ではヘッダーはまだ保存されていないため、更新された外部キーはメモリのテーブルバッファーにのみ表示されます。 ただし、以下の図に示すように、新しい既定の分析コードを照会して検索することができます。

![新たな既定の分析コードを検索する SQL クエリ。](./media/DefaultDimension4-1SQLDimOnLine.png "新たな既定の分析コードを検索するSQLクエリ")

![更新された既定の分析コード。](./media/DefaultDimension4-2SQLResultsOnLine.png "更新された既定の分析コード")

次に、ユーザーが購買注文の明細行に入力する品目を考えてみます。 以下の図は、製品タブでの既定の財務分析コードを示しています。

![品目の既定の分析コード。](./media/DefaultDimension4-3Item.png "品目の既定の分析コード")

以下のコードは、データベース内の既定の分析コードに対する SQL クエリを示しています。

```sql
SELECT ItemId, NAMEALIAS, DefaultDimension from InventTable where ItemId = '1000' AND DATAAREAID = 'USMF'

SELECT DA.NAME, DISPLAYVALUE, V.DIMENSIONATTRIBUTEVALUESET,
V.SETITEMRECID
FROM DIMENSIONATTRIBUTEVALUESETITEMVIEW V
JOIN DIMENSIONATTRIBUTE DA ON DA.RECID = V.DIMENSIONATTRIBUTE
WHERE V.DIMENSIONATTRIBUTEVALUESET = 68719490324
```

以下の図は、クエリの実行結果を示しています。

![品目レコードにおける既定の分析コードを表した出力結果。](./media/DefaultDimension4-4SQLResultsItem.png "品目レコードにおける既定の分析コードを表した出力結果")

続いて、購買注文の明細行に品目を入力します。 以下の図は、購買注文の明細行で選択された品目と、その結果の既定の分析コードを示しています。 この場合、既定の分析コード値は発注書ロジックによってマージされています。

![ドキュメント明細行 (購買注文の明細行) の既定の分析コード値のマージ。](./media/DefaultDimension4-5PurchLineResult.png)

以下のコードおよび図は、SQL クエリと購買注文明細行の品目レコードからの既定の分析コードの結果を示しています。

```sql
SELECT PURCHID, LINENUMBER, ITEMID, DEFAULTDIMENSION from PURCHLINE where PURCHID = '00000100' AND DATAAREAID = 'USMF'

SELECT DA.NAME, DISPLAYVALUE, V.DIMENSIONATTRIBUTEVALUESET,
V.SETITEMRECID
FROM DIMENSIONATTRIBUTEVALUESETITEMVIEW V
JOIN DIMENSIONATTRIBUTE DA ON DA.RECID = V.DIMENSIONATTRIBUTE
WHERE V.DIMENSIONATTRIBUTEVALUESET = 68719490325
```

[![ドキュメント明細行の品目レコードの既定の分析コードを示す出力 (購買注文明細行)。](./media/DefaultDimension4-6SQLResultOnItem.png)](./media/DefaultDimension4-6SQLResultOnItem.png)

品目が購買注文の明細行に対して指定されている場合、発注書のロジックが3つの異なる参照元の既定の分析コードをマージます。 以下の情報を参照してください

- 注文ヘッダーの既定の分析コードが、注文明細行の既定の分析コードとマージされて、"結合結果1" の既定の分析コードが生成されます。

    | 項目             | 注文明細行 | 注文ヘッダー | マージの結果 1 | 説明 |
    |------------------|------------|--------------|-----------------|-------------|
    | **BusinessUnit** |            |              |                 | この値は、両方のソースで空白です。 |
    | **CostCenter**   |            |              |                 | この値は、両方のソースで空白です。 |
    | **部門**   |            | 027          | 027             | 注文明細行の値は空白です。 結果として、この値は注文ヘッダーからコピーされます。 |
    | **ItemGroup**    |            |              |                 | この値は、両方のソースで空白です。 |
    | **プロジェクト**      | 000003     | 000003       | 000003          | この値は、両方のソースで空白です。 |
    | **外部キー**  | \*\*6190   | \*9574       | \*9574          | マージされた後は、注文ヘッダーと同じレコードが使用されます。 |

- 品目の既定の分析コードが、注文明細行の "結合結果1" とマージされて、"結合結果2" の既定の分析コードが生成されます。 以下の表では、マージ処理の際の論理ステップを示しています。 ただし、これらの手順は、実行時に、dimensionフレームワークによって提供されるAPIを使用してマージされます。

    | 項目             | マージの結果 1 | 項目     | マージの結果 2 | 説明 |
    |------------------|-----------------|----------|-----------------|-------------|
    | **BusinessUnit** |                 |          |                 | この値は、両方のソースで空白です。 |
    | **CostCenter**   |                 | 008      | 008             | ヘッダー行の結合結果の値が空白です。 結果として、この値は品目からコピーされます。 |
    | **部門**   | 027             | 023      | 027             | ヘッダー行の結合結果の値がセットされます。 したがって、その品目はスキップされます。 |
    | **ItemGroup**    |                 | AudioRM  | AudioRM         | ヘッダー行の結合結果の値が空白です。 結果として、この値は品目からコピーされます。 |
    | **プロジェクト**      | 000003          |          | 000003          | ヘッダー行の結合結果の値がセットされます。 |
    | **外部キー**  | \*6190          | \*\*0324 | \*\*0325        | マージ後の結果に対して新しいレコードIDが使用されます。 |

以下の図は、3つのソースからから既定の分析コードをマージするために使用されるコードを示しています。

[![注文ヘッダー、注文明細行、および品目から分析コードをマージするコード。](./media/DefaultDimension4-8CodeToMerge.png)](./media/DefaultDimension4-8CodeToMerge.png)

## <a name="creating-ledger-dimensions"></a>勘定分析コードの作成

このセクションでは、新しい勘定分析コードを作成するために既定の分析コードをマージするか方法について説明します。

既定の分析コードは、仕訳帳と勘定配布で使用される勘定科目の組み合わせを作成するために後のステップで使用される値を提供します。 勘定科目の組み合わせは、構造と順序が適用される MainAccount および分析コード値の組み合わせにすぎません。 詳細については、[第 5 部: 勘定分析コード](ledgeraccountcombinations.md#part-5-ledger-dimensions) を参照

既定の分析コードには、 MainAccount 以外の勘定科目の組み合わせに必要なすべての分析コードが用意されています。 既定の分析コードは既定の勘定と組み合わせることも、別の勘定分析コードを組み合わせて勘定分析コードを生成することもできます。

次の図は、購買注文明細行から勘定配布を実行する例を示しています。 注文明細行から **購買 \> 財務配分金額** を選択し **勘定配布** ページを開きます。 このページでは、既定の勘定科目の組み合わせである **618900--027-008audiorm**-が既に入力されています。

[![金額の配分を配布。](./media/DefaultDimension5-1AccountingDistributions.png)](./media/DefaultDimension5-1AccountingDistributions.png) 

[![勘定配布ページ。](./media/DefaultDimension5-1AcctDistForm.png)](./media/DefaultDimension5-1AcctDistForm.png)

勘定配賦に入力された、プロジェクト、コストセンター、品目グループ、部署の値。 また、次の図に示すように、転記品目グループの既定の MainAccount の値は、購買注文の経費勘定の購買経費として品目に入力されています。 プロジェクトは、ここに該当する勘定構造の一部ではないため、表示されません。

[![リリース済製品の詳細ページです。](./media/DefaultDimension5-1SourceofMainAccountOnPO.png)](./media/DefaultDimension5-1SourceofMainAccountOnPO.png) 

[![消費品目グループの詳細。](./media/DefaultDimension5-1SourceOfMAonPO2.png)](./media/DefaultDimension5-1SourceOfMAonPO2.png) 

以下の図は、クエリおよびその結果となる既定のアカウントのソースを示しています。

![SQL クエリ。](./media/DefaultDimension5-3SQLDefaultSource.png "SQL クエリ")

![結果は既定のアカウント ソースを表示します。](./media/DefaultDimension5-3SQLResultDefaultSource.png "結果は既定のアカウント ソースを表示します")

次の図は、品目グループの既定の勘定を含む購買注文明細行の既定の分析コードをマージするために必要なコードを示しています。 

![既定の分析コードと既定のアカウントを統合する際に使用するコード。](./media/DefaultDimension5-4CodeToMerge.png "既定の分析コードと既定のアカウントを統合する際に使用するコード")

マージが完了すると、以下の図に示すクエリのように、新しい勘定科目の組み合わせが作成されます。 この動作は、既定の分析コードが相互にマージされる際の挙動と共通しています。

![統合された既定のアカウントと既定の分析コードを表す SQL クエリと実行結果。](./media/DefaultDimension5-5SQLResultMerged.png "統合された既定のアカウントと既定の分析コードを表すSQLクエリと実行結果")

## <a name="common-pattern-apis"></a>一般的なAPIのパターン

このセクションでは、最も一般的な既定のパターンに使用されるAPIについて説明します。

### <a name="default-dimension-apis"></a>既定の分析コードAPI

**Dimensiondefaultfacade** と **LedgerDimensionDefaultFacade** クラスは、既定化を行うシナリオで必要なAPIを提供します。 **LedgerDimensionFacade** クラス" には、勘定分析コードで作業するためのメソッドが含まれています。 この方法は、パフォーマンスを優先し、高度に最適化されています。

### <a name="default-dimensions"></a>既定の分析コード

#### <a name="servicemergedefaultdimensions"></a>serviceMergeDefaultDimensions()

**ServiceMergeDefaultDimensions** APIは、既定の分析コードに対して最も頻繁に使用されるAPIです。 2つから4つの既定の分析コードから新たな既定の分析コードを作成する必要がある場合は、これを呼び出す必要があります。 4つ以上の既定の分析コードをマージする必要がある場合は、このAPIを複数回呼び出すことができます。 この場合、前回の呼び出しの結果を、後続の呼び出しの初期パラメータとして使用する必要があります。 この方法では、値が有効かどうかにかかわらず、すべての値が確実にマージされます。

**例: DimensionDefaultFacade::serviceMergeDefaultDimensions ()**

```xpp
public static DimensionDefault serviceMergeDefaultDimensions(
    DimensionDefault _value1,
    DimensionDefault _value2,
    DimensionDefault _value3 = 0,
    DimensionDefault _value4 = 0)
```

#### <a name="servicereplaceattributevalue"></a>serviceReplaceAttributeValue()

ServiceReplaceAttributeValue **()** APIは、1つの分析コード値をある既定のセットから別の既定セットへとコピーする必要がある場合に役立ちます。 指定された値は、ソースセットに既に存在する任意の値に置き換えられます。

**例: DimensionDefaultFacade::serviceReplaceAttributeValue ()** 

```xpp
public static DimensionDefault serviceReplaceAttributeValue(
    DimensionDefault _target,
    DimensionDefault _source,
    RecId _dimensionAttributeId)
```

#### <a name="servicemergevaliddefaultdimensions"></a>serviceMergeValidDefaultDimensions()

**ServiceMergeValidDefaultDimensions ()** APIは、現在の元帳に対して有効な値のみをマージしていく場合に便利です。 **ServiceMergeDefaultDimensions** と同じように動作しますが、有効な値の検証がされます。

**例: DimensionDefaultFacade::serviceMergeValidDefaultDimensions()** 

```xpp
public static DimensionDefault serviceMergeValidDefaultDimensions(
    DimensionDefault _defaultDimension1,
    DimensionDefault _defaultDimension2,
    DimensionDefault _defaultDimension3 = 0,
    DimensionDefault _defaultDimension4 = 0)
```

### <a name="ledger-dimensions"></a>勘定分析コード

#### <a name="servicecreateledgerdimension"></a>serviceCreateLedgerDimension()

**ServiceMergeDefaultDimensions** APIは、勘定分析コードに対して最も頻繁に使用されるAPIです。 このメソッドは、既定の勘定または既存の勘定科目の組み合わせと0 から3つの既定の分析コードから、新しい勘定科目の組み合わせを作成する必要がある場合に呼び出す必要があります。 3つ以上の既定の分析コードをマージする必要がある場合は、このAPIを複数回呼び出すことができます。 この場合、さまざまなソースが、後続の呼び出しの初期パラメーターとして前回の呼び出し結果を受け取ります。 MainAccount 分析コードは、指定された勘定分析コードからのみ取得されます。

**例: LedgerDimensionFacade.serviceCreateLedgerDimension()**

```xpp
public static LedgerDimensionAccount serviceCreateLedgerDimension(
    RecId            _ledgerDimensionId,
    DimensionDefault _dimensionDefault1 = 0,
    DimensionDefault _dimensionDefault2 = 0,
    DimensionDefault _dimensionDefault3 = 0)
    {
```

#### <a name="servicecreateledgerdimensionfortype"></a>serviceCreateLedgerDimensionForType()

**ServiceCreateLedgerDimensionForType ()** APIは、serviceCreateLedgerDimension **()** API と共通した特徴があります。 ただし、勘定科目の組み合わせを作成する代わりに、予算勘定や予算計画勘定など、他の勘定分析コードタイプを作成することもできます。 **LedgerDimensionType** パラメーター は、作成された勘定科目のタイプを指定する際に使用します。

**例: LedgerDimensionFacade.serviceCreateLedgerDimensionForType()**

```xpp
public static LedgerDimensionBase serviceCreateLedgerDimensionForType(
    LedgerDimensionType _ledgerDimensionType,
    LedgerDimensionBase _ledgerDimensionId,
    DimensionDefault    _dimensionDefault1 = 0,
    DimensionDefault    _dimensionDefault2 = 0,
    DimensionDefault    _dimensionDefault3 = 0)
```

#### <a name="servicecreateledgerdimfordefaultdim"></a>serviceCreateLedgerDimForDefaultDim()

**ServiceCreateLedgerDimForDefaultDim ()** APIは **serviceCreateLedgerDimension ()** および **serviceCreateLedgerDimensionForType ()** APIと共通した特徴を持っています。しかし、既定の分析コードの値は、新しい勘定分析コードに直接コピーされ、元帳分析コードの値は後でマージされます。 対照的に、前述の2つのAPIについては、勘定分析コード値がコピーされ、既定の分析コード値が結合されています。

**例: LedgerDimensionFacade::serviceCreateLedgerDimForDefaultDim()**

```xpp
public static LedgerDimensionBase serviceCreateLedgerDimForDefaultDim(
    DimensionDefault    _defaultDimension,
    LedgerDimensionBase _ledgerDimensionId)
```

#### <a name="serviceledgerdimensionfromledgerdims"></a>serviceLedgerDimensionFromLedgerDims()

**Serviceledgerdimensionfromledgerdims ()** API は前述のAPIと共通する特徴を持っていますがていますが、新しい勘定分析コードを作成するためには、ソースとして元帳分析コードのみを使用します。 主勘定には、勘定分析コードからの固定値のみが適用されます。

**例: LedgerDimensionFacade::serviceLedgerDimensionFromLedgerDims()**

```xpp
public static LedgerDimensionAccount serviceLedgerDimensionFromLedgerDims(
    LedgerDimensionBase _ledgerDimensionId1,
    LedgerDimensionBase _ledgerDimensionId2 = 0,
    LedgerDimensionBase _ledgerDimensionId3 = 0,
    LedgerDimensionBase _ledgerDimensionId4 = 0,
    LedgerDimensionBase _ledgerDimensionId5 = 0)
```

#### <a name="servicemergeledgerdimensions"></a>serviceMergeLedgerDimensions()

**ServiceMergeLedgerDimensions ()** APIは、 **serviceledgerdimensionfromledgerdims()** APIと共通とした特徴を持っていますが、2つの会計分析コードだけを組み合わせるように最適化されています。 

**例: LedgerDimensionFacade::serviceMergeLedgerDimensions()**

```xpp
public static LedgerDimensionBase serviceMergeLedgerDimensions(
    LedgerDimensionBase _ledgerDimension1,
    LedgerDimensionBase _ledgerDimension2,
    LedgerDimensionType _ledgerDimensionType = LedgerDimensionType::Account)
```

#### <a name="servicecreateledgerdimfromledgerdim"></a>serviceCreateLedgerDimFromLedgerDim()

**ServiceCreateLedgerDimFromLedgerDim ()** APIは、過去に転記されたドキュメントから新しい未転記のドキュメントに元帳分析コードをコピーする場合と、現在の勘定構造の設定を確実に使用すように設定したい場合に便利です。 これにより、転記時に新しい元帳分析コードを検証する際の検証エラーを防ぐことができます。

**例: LedgerDimensionFacade::serviceCreateLedgerDimFromLedgerDim()**

```xpp
public static LedgerDimensionAccount serviceCreateLedgerDimFromLedgerDim(LedgerDimensionAccount _ledgerDimension)
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]