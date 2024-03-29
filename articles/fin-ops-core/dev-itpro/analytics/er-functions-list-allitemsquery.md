---
title: ALLITEMSQUERY ER 関数
description: この記事では、ALLITEMSQUERY 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e350dfbe800ddc3e7b1f388fb951d091a283f4e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285308"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER 関数

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY` 関数は、結合された SQL クエリとして実行されます。 これは、指定したパスに一致するすべての品目を表すレコードの一覧を構成する、新しいフラット化された *レコード リスト* の値を返します。

## <a name="syntax"></a>構文

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>引数

`path`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。 少なくとも 1 つの関係が含まれている必要があります。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

指定されたパスは、*レコード リスト* データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があります。 また、少なくとも 1 つの関係が含まれている必要があります。 パス *文字列* や *日付* などのデータ要素は、デザイン時に電子申告 (ER) 式ビルダーでエラーを生成する必要があります。

この関数は、 SQL を使用して直接呼び出すことができるアプリケーション オブジェクト (テーブル、エンティティ、クエリなど) を参照する *レコード リスト* データ型のデータ ソースに適用されると、結合された SQL クエリとして実行されます。 それ以外の場合は、[ALLITEMS](er-functions-list-allitems.md) 関数としてメモリ上で実行されます。

## <a name="example"></a>例

モデル マッピングでは、次のデータ ソースを定義します。

- CustInvoiceTable テーブルを参照する *テーブル レコード* タイプの **CustInv** データ ソース
- `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` 式を含む *計算済フィールド* タイプの **FilteredInv** データ ソース
- `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` 式を含む *計算済フィールド* タイプの **JourLines**

**JourLines** データ ソースを呼び出すモデル マッピングを実行すると、次の SQL ステートメントが実行されます。

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
