---
title: 電子申告の数式言語
description: このトピックでは、電子申告 (ER) の数式言語の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 846a9373fc15065513e634b15d9dac1eccc46a99
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561808"
---
# <a name="electronic-reporting-formula-language"></a>電子申告の数式言語

[!include [banner](../includes/banner.md)]

電子申告 (ER) では、強力なデータ変換経験を提供します。 [ER フォーミュラ デザイナー](general-electronic-reporting-formula-designer.md) で必要なデータ操作を表すために使用される言語は、Microsoft Excel の数式言語と共通しています。

## <a name="basic-syntax"></a>基本構文

ER の式は、次のいずれかまたはすべての要素を含めることができます。

- [定数](#Constants)
- [演算子](#Operators)
- [参照](#References)
- [パス](#Paths)
- [関数](#Functions)

## <a name=""></a><a name="Constants">定数</a>

式の設計時に、テキストおよび数値定数 (つまり、計算されない定数) を使用できます。 たとえば、`VALUE ("100") + 20` の式では、数値定数 **20** および文字列定数 **"100"** を使用し、**120** という数値を返します。

ER フォーミュラ デザイナーはエスケープ シーケンスをサポートします。 したがって、別の方法で処理されるべき式文字列を指定することができます。 たとえば、`"Leo Tolstoy ""War and Peace"" Volume 1"` の式は、**レフ トルストイ "戦争と平和" ボリューム 1** というテキスト文字列を返します。

## <a name=""></a><a name="Operators">演算子</a>

次の表に、加算、減算、乗算、除算などの基本的な数学演算の実行に使用できる算術演算子を示します。

| オペレーター | 意味               | 例     |
|----------|-----------------------|-------------|
| +        | 追加              | `1+2`       |
| -        | 減算、否定 | `5-2`、`-1` |
| \*       | 乗算        | `7\*8`      |
| /        | 区分              | `9/3`       |

次の表に、サポートされる比較演算子を示します。 これらの演算子を使用して、2 つの値を比較することができます。

| オペレーター | 意味                  | 例      |
|----------|--------------------------|--------------|
| =        | 等しい                    | `X=Y`        |
| &gt;     | より大きい             | `X>Y`        |
| &lt;     | より小さい                | `X<Y`        |
| &gt;=    | 以上 | `X>=Y`       |
| &lt;=    | 以下    | `X<=Y`       |
| &lt;&gt; | 次の値に等しくない             | `X<>Y`       |

また、テキスト連結演算子としてアンパサンド (&) を使用することができます。 これにより、1 つ以上の文字列を 1 つのテキストに結合または連結することができます。

| オペレーター | 意味     | 例                                               |
|----------|-------------|-------------------------------------------------------|
| &        | 連結 | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>演算子の優先順位

複合式のパーツを評価する順番は重要です。 たとえば、`1 + 4 / 2` の式の結果は、加算または除算のどちらを先に実行するかによって異なります。 明示的に式の評価方法を定義するためにかっこを使用できます。 たとえば、加算を最初に実行する必要があることを示すには、前の式を `(1 + 4) / 2` に変更できます。 式で工程の順序を明確に定義しない場合、順序はサポートされる演算子に割り当てられている既定の優先順位に基づきます。 次の表に、各演算子に割り当てられている優先順位を示します。 高い優先順位 (たとえば、7) がある演算子は、低い優先順位 (たとえば、1) がある演算子より前に評価されます。

| 優先順位 | 演算子      | 構文                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | グループ化       | ( … )                                                                   |
| 6          | メンバーのアクセス  | … します。 …                                                                   |
| 5          | 関数の呼び出し  | … ( … )                                                                 |
| 4          | 乗算 | … \* …<br>… / …                                                         |
| 3          | 付加       | … + …<br>… - …                                                          |
| 2          | 比較     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | 区切り     | … , …                                                                   |

式に同じ優先順位を持つ複数の連続した演算子が含まれている場合は、これらの操作は左から右に評価されます。 たとえば、`1 + 6 / 2 \* 3 > 5` の式は **true** を返します。 式の閲覧や管理を簡単にするよう、式で操作する希望の順序を明示的に示すために、かっこを使用することをお勧めします。

## <a name=""></a><a name="References">参照</a>

式の設計中に使用できる現在の ER コンポーネントのすべてのデータ ソースは名前付き参照を使用できます。 現在の ER コンポーネントは、モデル マッピングまたは形式のいずれかです。 たとえば、現在の ER モデル マッピングには **ReportingDate** データ ソースが含まれ、*DateTime* データ型の値を返します。 生成ドキュメントでその値を正しく書式設定するために、`DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")` の式のデータ ソースを参照できます。

アルファベットの文字で表されない参照元のデータ ソースの名前のすべての文字は、単一引用符 (') の後に続く必要があります。 参照データ ソースの名前がアルファベットの文字を表さない記号を少なくとも 1 つ含む場合、名前を単一引用符で囲む必要があります。 たとえば、これらアルファベットでない記号は、句読点またはそのほかの書面記号です。 次にいくつか例を挙げます。

- **今日の日付 & 時間** データ ソースは、`'Today''s date & time'` のように ER の式で参照する必要があります。
- **顧客** データ ソースの **name()** メソッドは、ER 式で `Customers.'name()'` のように参照する必要があります。

アプリケーション データ ソースのメソッドにパラメーターがある場合は、次の構文を使用して、これらのメソッドを呼び出します。

- **システム** データ ソースの **isLanguageRTL** メソッドが、*文字列* データ型の **EN-US** パラメーターを含む場合、このメソッドは ER 式で `System.isLanguageRTL("EN-US")` として参照する必要があります。
- メソッド名に英数字シンボルのみが含まれている場合、引用符は必須ではありません。 ただし、名前にかっこが含まれている場合、テーブルのメソッドに対しては必須です。

**システム** データ ソースが、**グローバル** アプリケーション クラスを参照する ER マッピングに追加されると、式 `System.isLanguageRTL("EN-US ")` は *ブール* 値の **FALSE** を返します。 変更された式 `System.isLanguageRTL("AR")` は *ブール* 値の **TRUE** を返します。

値がこのメソッドのタイプのパラメータに渡される方法を制限することができます。

- このタイプのメソッドに、定数だけを渡すことができます。 定数の値は、デザイン時に定義されます。
- このタイプのパラメーターで、プリミティブ (基本) データ型のみがサポートされています。 プリミティブ データ型には、*整数*、*実数*、*ブール値*、および *文字列* が含まれます。

## <a name=""></a><a name="Paths">パス</a>

式が構成されたデータ ソースを参照する場合、そのデータ ソースの特定のプリミティブ要素の選択にパス定義を使用できます。 ドット (.) は、構成されたデータ ソースの個別要素を区切るために使用します。 たとえば、現在の ER モデル マッピングには **InvoiceTransactions** データ ソースが含まれ、このデータ ソースはレコード一覧を返します。 **InvoiceTransactions** レコード構造には、**AmountDebit** および **AmountCredit** フィールドが含まれており、どちらのフィールドも数値を返します。 したがって、請求金額 `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit` を計算するための次の式をデザインできます。 この式の `InvoiceTransactions.AmountDebit` 構造は、*レコード リスト* タイプの **InvoiceTransactions** データ ソースの **AmountDebit** フィールドにアクセスするために使用されるパスです。

### <a name="relative-path"></a>相対パス

構成されたデータ ソースのパスが "at" 記号 (@) で始まる場合は、相対パスとなります。 使用される階層ツリー構造の絶対パスの残り部分の代わりに、"at" 記号が表示されます。 次の図は、例を示します。 ここでは、絶対パス `Ledger.'accountingCurrency()'` は、**元帳** データ ソースからの会計通貨値がデータ モデルの **会計通貨** フィールドに入力されることを示します。

![ER モデル マッピング デザイナー ページでの絶対パスの例](./media/ER-FormulaLanguage-AbsolutePath.png)

次の図の例では、相対パスがどのように使用されるかを示します。 相対パス `@.AccountNum` は、**Intrastat** データ ソースの **AccountNum** フィールド (データモデルの階層ツリーの **AccountNum** フィールドの 1 レベル上に表示される) が、データモデルの **AccountNum** フィールドに顧客または仕入先勘定番号を入力して使用されることを示します。

![ER モデル マッピング デザイナー ページでの相対パスの例](./media/ER-FormulaLanguage-RelativePath1.png)

絶対パスの残りの部分は、[ER フォーミュラ エディター](general-electronic-reporting-formula-designer.md) でも表示されます。

![ER フォーミュラ デザイナー ページの絶対パスの残りの部分](./media/ER-FormulaLanguage-RelativePath2.png)

詳細については、[ER モデルと ER 形式のデータ バインディングに相対パスを使用する](relative-path-data-bindings-er-models-format.md) を参照してください。

## <a name=""></a><a name="Functions">関数</a>

ER 組み込み関数は、ER 式で使用できます。 式のコンテキストのすべてのデータ ソース (つまり、現在の ER モデル マッピングまたは ER フォーマット) は、呼び出し元関数の引数に従って呼び出し元関数のパラメータとして使用できます。 定数は、呼び出し関数のパラメータとしても使用できます。 たとえば、現在の ER モデル マッピングには **InvoiceTransactions** データ ソースが含まれ、このデータ ソースはレコード一覧を返します。 **InvoiceTransactions** レコード構造には、**AmountDebit** および **AmountCredit** フィールドが含まれており、どちらのフィールドも数値を返します。 したがって、請求額を計算するには、ER 丸め関数を使用する次の式をデザインできます: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`。

ER モデル マッピングと ER レポートをデザインする場合は、次のカテゴリから ER 関数を使用できます。

- [日時の関数](er-functions-category-datetime.md)
- [リスト機能](er-functions-category-list.md)
- [論理機能](er-functions-category-logical.md)
- [算術関数](er-functions-category-mathematical.md)
- [レコード機能](er-functions-category-record.md)
- [テキスト関数](er-functions-category-text.md)
- [データ収集機能](er-functions-category-data-collection.md)
- [その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)
- [型変換関数](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>関数の一覧の拡張

ER では ER の式で使用される関数の一覧を拡張できます。 これにはエンジニアリングの実績が要求されます。 詳細については、[電子申告 (ER) 関数の一覧の拡張](general-electronic-reporting-formulas-list-extension.md) を参照してください。

## <a name="compound-expressions"></a>複合式

データ型が一致する場合、異なるカテゴリの関数を使用する複合式を作成できます。 関数を一緒に使用する場合は、1 つの関数からの出力のデータ型を別の関数が必要とする入力データ型に一致させます。 たとえば、フィールドの ER 形式要素へのバインディングで発生する "リストが空である" エラーを回避するには、次の例に示すように、[リスト](er-functions-category-list.md) カテゴリの関数を [論理](er-functions-category-logical.md) カテゴリの関数と組み合わせます。 ここでは、数式は [IF](er-functions-logical-if.md) 関数を使用して **IntrastatTotals** リストが空であるかどうかをテストしてから、必要な集計の値をリストから返します。 **IntrastatTotals** リストが空の場合、数式は **0** (ゼロ) を返します。

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>複数のソリューション

多くの場合、異なるカテゴリからの関数または同じカテゴリからの異なる機能を使用して、同じデータ変換結果を複数の方法で取得できます。 たとえば、前の式は [リスト](er-functions-category-list.md) カテゴリからの [COUNT](er-functions-list-count.md) 関数を使用してコンフィギュレーションすることもできます。

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子申告機能の一覧の拡張](general-electronic-reporting-formulas-list-extension.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]