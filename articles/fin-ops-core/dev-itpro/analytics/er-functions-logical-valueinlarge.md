---
title: VALUEINLARGE ER 関数
description: このトピックでは、 VALUEINLARGE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705146"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER 関数

[!include [banner](../includes/banner.md)]

`VALUEINLARGE` 関数は、*Int64* あるいは *整数* タイプの指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。 この関数は、指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の*ブール*値が返されます。 `VALUEIN` 関数との違いを理解するには、このトピックで後述する [使用上の注意](#usage_note) セクションを参照してください。

## <a name="syntax"></a>構文

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>引数

`input`: *フィールド*

*レコード リスト* タイプのデータ ソースの項目の有効なパス。 この項目の値は一致します。

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

`list item expression`: *式*

照合に使用される指定されたリストの単一のフィールドを指し示すか、そのフィールドを含む有効な条件式。

## <a name="return-values"></a>戻り値

*ブール値*

結果*ブール*値。

## <a name=""></a><a name="usage_note">使用上の注意</a>

指定された入力が、データ ソース項目の *Int64* または *整数* タイプを表す場合、直接 SQL ステートメントに変換可能な呼び出しは、指定されたリストが一時的な SQL テーブルに変換され、単一の `EXISTS JOIN` クエリを実行することによってデータベース内で一致が実行されます。 それ以外の場合、この関数は [`VALUEIN`](er-functions-logical-valuein.md) 関数として機能します。

指定された入力が、*Int64* および *整数* タイプ以外の項目として設計されたデータ ソース項目を表している場合、設計時にエラーが発生し、`VALUEINLARGE` 関数が設定された ER 式に適用されないことが通知されます。

`VALUEINLARGE` 関数式が実行され、この実行のスコープで複数の一時テーブルが使用される場合、ランタイム エラーが発生します。

## <a name="example"></a>例

モデル マッピングでは、次のデータ ソースを定義します。

- *テーブル レコード* タイプの **In** データ ソース。
    - このデータ ソースは、**イントラスタット** テーブルを参照します。
    - **会社間** オプションは **いいえ** に設定されています。
- *計算フィールド* タイプの **InMemory** データ ソース。
    - このデータ ソースは、式 `WHERE (In, In.Port <> "")` が含まれています。
- *計算フィールド* タイプの **InFiltered** データ ソース。
    - このデータ ソースは、式 `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)` が含まれています。

データソース **InFiltered** が、会社 **DEMF** のコンテキストで呼び出されると、アプリケーション データベースに新しい一時テーブルが作成され、レコード ID コードの収集されたメモリ リストがこのテーブルに挿入され、**イントラスタット** テーブルのフィルター処理されたレコードを返す次の SQL ステートメントが生成されます。

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>追加リソース

[論理関数](er-functions-category-logical.md)

[VALUEIN 関数](er-functions-logical-valuein.md)
