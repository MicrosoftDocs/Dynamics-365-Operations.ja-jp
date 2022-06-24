---
title: ORDERBY ER 関数
description: この記事では、ORDERBY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1a922405ea23d2b1ff5ac062785e68626edbc8f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883762"
---
# <a name="orderby-er-function"></a>ORDERBY ER 関数

[!include [banner](../includes/banner.md)]

`ORDERBY` 関数は、指定されたリストを、指定された引数に基づいて並べ替えられた後に *レコード リスト* 値として返します。 これらの引数は、式として定義することができます。

## <a name="syntax-1"></a><a name="syntax-1"></a>構文 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>構文 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> この構文は、Microsoft Dynamics 365 Finance バージョン 10.0.25 以降でサポートされます。

## <a name="arguments"></a>引数

`location`: *[文字列](er-formula-supported-data-types-primitive.md#string)*

並べ替えを実行する場所。 次のオプションが有効です:

- "Query"
- "InMemory"

`list`: *[レコード リスト](er-formula-supported-data-types-composite.md#record-list)*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`expression 1`: *フィールド*

呼び出された関数の `list` 引数によって参照されるデータ ソースのフィールドの有効なパス。 参照フィールドは、プリミティブ データ型のフィールドである必要があります。 この引数は必須です。

`expression N`: *フィールド*

呼び出された関数の `list` 引数によって参照されるデータ ソースのフィールドの有効なパス。 参照フィールドは、プリミティブ データ型のフィールドである必要があります。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

### <a name="syntax-1"></a>構文 1

データの並べ替えは、常にアプリケーション サーバーのメモリ内で行われます。 詳細については、[例 1](#example-1) を参照してください。

### <a name="syntax-2"></a>構文 2

### <a name="sorting-in-memory"></a>メモリ内での並べ替え

`location` 引数が **InMemory** として指定されている場合、データの並べ替えはアプリケーション サーバーのメモリ内で行われます。 詳細については、[例 2](#example-2) を参照してください。

### <a name="sorting-in-database"></a>データベースでの並べ替え

`location` 引数が **Query** として指定されている場合、データの並べ替えはデータベース レベルで行われます。 この場合、`list` 引数は、直接データベース クエリを作成できるアプリケーション ソースを指定する、次の [電子申告 (ER)](general-electronic-reporting.md) データ ソースのいずれかをポイントする必要があります。

- *テーブル レコード* 型のデータ ソース
- *テーブル レコード* 型のデータ ソースの関係
- *計算フィールド* 型のデータ ソース

`expression 1` と`expression N` の引数は、直接データベース クエリも作成できるアプリケーション ソースの関連フィールドを指定する、ER データ ソースのフィールドをポイントする必要があります。

直接データベース クエリを作成できない場合、ER モデル マッピング デザイナーで検証 [エラー](er-components-inspections.md#i18) が発生します。 受信するメッセージは、`ORDERBY` 関数を含む ER 式を実行時に実行できないことを示しています。

パフォーマンスを向上させるため、多数のレコード (例えば、トランザクション アプリケーション テーブルなど) を含むアプリケーション データ ソースに対して並べ替えを構成する場合は、**Query** オプションを使用することをお勧めします。

> [!NOTE]
> `ORDEBY` 関数自体は、直接データベース クエリに変換できません。 したがって、この関数を含む ER データ ソースはクエリ可能ではありません。 また、クエリ可能なデータ ソースのみを使用できる ER 関数 ([FILTER](er-functions-list-filter.md) や [ALLITEMSQUERY](er-functions-list-allitemsquery.md) など) の範囲でも使用できません。

詳細については、[例 3](#example-3) と [例 4](#example-4) を参照してください。

### <a name="comparability"></a>比較可能性

SQLデータベース エンジンと Finance アプリケーション サーバーでは、1 つの文字に対して異なるランキング値を使用できるため、[文字列](er-formula-supported-data-types-primitive.md#string) フィールドを並べ替えに使用した場合、同じレコード リストの並べ替え結果が異なる場合があります。 詳細については、[例 5](#example-5) を参照してください。

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>例 1: メモリ内の既定の実行

*計算済フィールド* タイプのデータ ソース **DS** を入力し、式 `SPLIT ("C|B|A", "|")` が含まれている場合、式 `FIRST( ORDERBY( DS, DS. Value)).Value` はテキスト値 **"A"** を返します。

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>例 2: メモリ内の明示的実行

**Vendor** が、**VendTable** テーブルを参照する *テーブル レコード* のER データ ソースとして構成されている場合、式 `ORDERBY (Vendor, Vendor.'name()')` と 式 `ORDERBY ("InMemory", Vendor, Vendor.'name()')` の両方とも、名前で昇順に並べ替えられた仕入先のリストを返します。

ER モデル マッピング デザイナーで式 `ORDERBY ("Query", Vendor, Vendor.'name()')` を構成すると、直接データベース クエリに変換できないロジックを持つアプリケーション メソッドを `Vendor.'name()'` パスが参照のため、デザイン時に検証 [エラー](er-components-inspections.md#i8) が発生します。

## <a name="example-3-database-query"></a><a name="example-3"></a>例 3: データベース クエリ

**TaxTransaction** が、**TaxTrans** テーブルを参照する *テーブル レコード* 型の ER データ ソースとして構成されている場合、式 `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` はアプリケーション データベース レベルでレコードを並べ替え、税コード別に昇順に並べ替えられた税トランザクションの一覧を返します。

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>例 4: クエリ可能なデータ ソース

**TaxTransaction** が、**TaxTrans** テーブルを参照する *テーブル レコード* 型の ER データ ソースとして構成されている場合、**TaxTransactionFiltered** ER データ ソースは、指定の税コードのトランザクションをフェッチする式 `FILTER(TaxTransaction, TaxCode="VAT19")` を含むように構成することができます。 構成済の **TaxTransactionFiltered** ER データ ソースはクエリ可能なので、式 `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` を構成して、トランザクション日付で昇順に並べ替えられた、フィルター処理された税トランザクションの一覧を返することができます。

式 `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` を含む *計算フィールド* 型の ER データ ソース、および式 `FILTER(TaxTransactionOrdered, TaxCode="VAT19")` を含む *計算フィールド* 型の ER データ ソースとして **TaxTransactionOrdered** を構成する場合、ER モデル マッピング デザイナーで設計時に検証 [エラー](er-components-inspections.md#i18) が発生します。 このエラーは、[FILTER](er-functions-list-filter.md#usage-notes) 関数の最初の引数がクエリ可能な ER データ ソースを参照する必要があるのに、`ORDERBY` 関数を含む **TaxTransactionOrdered** データ ソースがクエリ可能ではないために発生します。

## <a name="example-5-comparability"></a><a name="example-5"></a>例 5: 比較可能性

### <a name="prerequisites"></a>必要条件

1. 式 `SPLIT ("D1|_D2|D3", "|")` を含む *計算フィールド* 型のデータ ソース **DS1** を入力します。
2. **[財務分析コード値](../../../finance/general-ledger/financial-dimensions.md)** ページを開き、**CostCenter** 分析コードを選択します。
3. 次の分析コード値を入力します: **D1**、**\_D2**、**D3**。

### <a name="sorting-in-memory"></a>メモリ内での並べ替え

1. 式 `ORDERBY("InMemory", DS1, DS1.Value)` を含む *計算フィールド* 型のデータ ソース **DS2** を構成します。
2. 式 `FIRST(DS2).Value` がテキスト値 **"D1"** を返し、式 `INDEX(DS2, COUNT(DS2)).Value` がテキスト値 **"\_D2"** を返し、式 `STRINGJOIN(DS2, DS2.Value, "|")` がテキスト値 **"D1\|D3\|\_D2"** を返す点に注意してください。

### <a name="sorting-in-database"></a>データベースでの並べ替え

1. **FinancialDimensionValueEntity** エンティティを参照する *テーブル レコード* タイプのデータ ソース **DS3** を入力します。
2. 式 `FILTER(DS3, DS3.FinancialDimension="CostCenter")` を含む *計算フィールド* 型のデータ ソース **DS4** を構成します。
3. 式 `ORDERBY(DS4, DS4.DimensionValue)` を含む *計算フィールド* 型のデータ ソース **DS5** を構成します。
4. 式 `FIRST(DS5).Value` がテキスト値 **"\_D2"** を返し、式 `INDEX(DS5, COUNT(DS5)).Value` がテキスト値 **"D3"** を返し、式 `STRINGJOIN(DS5, DS5.Value, "|")` がテキスト値 **"\_D2\|D1\|D3"** を返す点に注意してください。

## <a name="additional-resources"></a>追加リソース

[リスト関数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
