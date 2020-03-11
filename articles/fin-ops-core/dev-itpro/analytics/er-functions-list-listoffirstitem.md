---
title: LISTOFFIRSTITEM ER 関数
description: このトピックでは、LISTOFFIRSTITEM 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041978"
---
# <a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER 関数</a>

[!include [banner](../includes/banner.md)]

`LISTOFFIRSTITEM` 関数は、指定されたリストの最初のレコードのみで構成される*レコード リスト*値を返します。

## <a name="syntax"></a>構文

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="example"></a>例

式 `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` はテキスト値 **"A"** を返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)
