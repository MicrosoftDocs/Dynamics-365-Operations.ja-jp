---
title: LIST ER 関数
description: このトピックでは、LIST 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917284"
---
# <a name="LIST">LIST ER 関数</a>

[!include [banner](../includes/banner.md)]

`LIST` 関数は、指定された引数から作成されたレコードの新しいリストで構成される*レコード リスト*値を返します。

## <a name="syntax"></a>構文

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>引数

`record 1`: *コンテナー (レコード)*

*レコード*データ タイプのデータ ソースの参照。 この引数は必須です。

`record N`: *コンテナー (レコード)*

*レコード*データ タイプのデータ ソースの参照。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

作成されたリストの構造には、引数で指定されているすべてのレコードの構造で表示されるフィールドのみが含まれます。

## <a name="example"></a>例

*コンテナー* タイプのデータ ソース **レコード 1** を入力します。 このデータ ソースには、*計算済フィールド* タイプの次の入れ子になったフィールドが含まれています。

- **コード:** このフィールドには、*文字列*タイプの値を返す式が含まれています。
- **金額:** このフィールドには、*実数*タイプの値を返す式が含まれています。

次に、*コンテナー* タイプのデータ ソース **レコード 2** を入力します。 このデータ ソースには、*計算済フィールド* タイプの次の入れ子になったフィールドが含まれています。

- **金額:** このフィールドには、*実数*タイプの値を返す式が含まれています。
- **IsValid:** このフィールドには、*ブール値*タイプの値を返す式が含まれています。

この場合、式 `LIST('Record 1', 'Record 2')` は 2 つのレコードを含む新しいリストを返します。 このフィールドは、呼び出された関数のすべての引数に対して表示される唯一のフィールドであるため、このリストの構造は*実数*タイプの 1 つの**金額**フィールドで構成されます。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)
