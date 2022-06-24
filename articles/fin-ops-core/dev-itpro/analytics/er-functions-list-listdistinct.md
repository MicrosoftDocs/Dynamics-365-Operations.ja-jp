---
title: LISTDISTINCT ER 関数
description: この記事では、LISTDISTINCT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 7/30/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: d2f8e3a9d077493df3c3b7628608d31834f43f8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876808"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER 関数

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この `LISTDISTINCT` 関数は、指定されたリストのすべてのレコードに対して、指定された式をセレクターとして計算します。 固有のセレクター値ごとに 1 つのレコードを含む、新しい *レコード リスト* 値を返します。

## <a name="syntax"></a>構文

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`selector`: *プリミティブ データ型*

指定されたリスト内のすべてのレコードに対してセレクター値を計算するために使用される有効な式。

このパラメータでは、次のデータ型がサポートされています:

- ブール値
- 日
- DateTime
- GUID
- 整数
- Int64
- 実績
- 文字列

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

作成されたリストの構造は、指定されたリストの構造に一致します。

指定したリストの複数のレコードに対して同じセレクター値が計算される場合があります。 この場合、作成されたリスト内の対応するレコードのフィールド値は、セレクター値の計算対象となる指定されたリストの最初のレコードの値と等しくなります。

この関数の実行は、メモリ内に存在する *レコード リスト* タイプの [電子申告 (ER)](general-electronic-reporting.md) データ ソースで実行されます。

**GROUPBY** データ ソースを使用して、固有の値を持つセレクターが計算されるレコードの一覧を生成することもできます。 ただし、関数の実行はメモリ内で行われるため、パフォーマンスとメモリの消費の観点から、**GROUPBY** データ ソースより `LISTDISTINCT` 機能を使用することをお勧めします。

## <a name="example"></a>例

次の例は、特定の期間中に少なくとも 1 つの売上請求書またはプロジェクト請求書が発行された固有の顧客アカウント番号の一覧を取得する方法を示しています。

1. **CustInvoiceJour** アプリケーション テーブルを参照し、特定期間の売上請求書をフィルター処理する `Record list` タイプの **SalesInvoice** データ ソースを入力します。

    このデータ ソースの `InvoiceAccount` フィールドは、請求済顧客のアカウント番号を返します。

2. **ProjInvoiceJour** アプリケーション テーブルを参照し、特定期間のプロジェクト請求書をフィルター処理する `Record list` タイプの **ProjectInvoice** データ ソースを入力します。

    このデータ ソースの `InvoiceAccount` フィールドは、請求済顧客のアカウント番号を返します。

3. 式 `LISTJOIN(SalesInvoice, ProjectInvoice)` を含む `Calculated field` タイプの **AllInvoices** データ ソースを構成します。

    このデータ ソースは、売上請求書およびプロジェクト請求書の結合リストを返します。

4. 式 `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` を含む `Record list` タイプの **InvoicedCustomer** データ ソースを構成します。

    このデータ ソースは、定義された期間中に請求された固有の顧客ごとに 1 つのレコードを含む新しいリストを返します。 このリストの `InvoiceAccount` フィールドには、顧客アカウント番号が含まれています。

## <a name="additional-resources"></a>追加リソース

[リスト関数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]