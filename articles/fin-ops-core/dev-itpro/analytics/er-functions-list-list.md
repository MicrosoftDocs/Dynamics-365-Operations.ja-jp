---
title: LIST ER 関数
description: この記事では、LIST 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
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
ms.openlocfilehash: 7a5f27baa248ec84c75725cf32a1f482841424c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277635"
---
# <a name="list-er-function"></a>LIST ER 関数

[!include [banner](../includes/banner.md)]

`LIST` 関数は、指定された引数から作成されたレコードの新しいリストで構成される *レコード リスト* 値を返します。

## <a name="syntax"></a>構文

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>引数

`record 1`: *コンテナー (レコード)*

*レコード* データ タイプのデータ ソースの参照。 この引数は必須です。

`record N`: *コンテナー (レコード)*

*レコード* データ タイプのデータ ソースの参照。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

作成されたリストの構造には、引数で指定されているすべてのレコードの構造で表示されるフィールドのみが含まれます。

## <a name="example"></a>例

*コンテナー* タイプのデータ ソース **レコード 1** を入力します。 このデータ ソースには、*計算済フィールド* タイプの次の入れ子になったフィールドが含まれています。

- **コード:** このフィールドには、*文字列* タイプの値を返す式が含まれています。
- **金額:** このフィールドには、*実数* タイプの値を返す式が含まれています。

次に、*コンテナー* タイプのデータ ソース **レコード 2** を入力します。 このデータ ソースには、*計算済フィールド* タイプの次の入れ子になったフィールドが含まれています。

- **金額:** このフィールドには、*実数* タイプの値を返す式が含まれています。
- **IsValid:** このフィールドには、*ブール値* タイプの値を返す式が含まれています。

この場合、式 `LIST('Record 1', 'Record 2')` は 2 つのレコードを含む新しいリストを返します。 このフィールドは、呼び出された関数のすべての引数に対して表示される唯一のフィールドであるため、このリストの構造は *実数* タイプの 1 つの **金額** フィールドで構成されます。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
