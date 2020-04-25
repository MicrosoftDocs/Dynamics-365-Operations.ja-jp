---
title: LISTJOIN ER 関数
description: このトピックでは、LISTJOIN 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249038"
---
# <a name=""></a><a name="LISTJOIN">LISTJOIN ER 関数</a>

[!include [banner](../includes/banner.md)]

この `LISTJOIN` 関数は、指定された引数から作成された新しい結合リストを表す *レコード リスト* 値を返します。

## <a name="syntax"></a>構文

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>引数

`list 1`: *レコード リスト*

*レコード リスト* データ タイプのデータ ソースの参照。 この引数は必須です。

`list N`: *レコード リスト*

*レコード リスト* データ タイプのデータ ソースの参照。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

作成されたリストの構造には、引数で参照されるすべてのレコード リストの構造に存在するフィールドのみが含まれます。

## <a name="example"></a>例

`Container` タイプのデータ ソース **レコード 1** を入力します。 このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:

- **コード**: このフィールドには、`String` タイプの値を返す式が含まれています。
- **量**: このフィールドには、`Real` タイプの値を返す式が含まれています。

次に、`Container` タイプのデータ ソース **レコード 2** を入力します。 このデータ ソースには、`Calculated field` タイプの次の入れ子になったフィールドが含まれています:

- **量**: このフィールドには、`Real` タイプの値を返す式が含まれています。
- **IsValid**: このフィールドには、`Boolean` タイプの値を返す式が含まれています。

この場合、式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` は 2 つのレコードを含む新しいリストを返します。 このフィールドは、呼び出された関数のすべての引数に表示される唯一のフィールドであるため、`Real` タイプの 1 つの **量** フィールドで構成されます。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)
