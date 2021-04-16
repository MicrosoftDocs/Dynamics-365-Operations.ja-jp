---
title: NULLCONTAINER ER 関数
description: このトピックでは、NULLCONTAINER 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746510"
---
# <a name="nullcontainer-er-function"></a>NULLCONTAINER ER 関数

[!include [banner](../includes/banner.md)]

`NULLCONTAINER` 関数は、指定されたリストまたはレコードと同じ構造を持つ *コンテナー (レコード)* 値を返します。

## <a name="syntax"></a>構文

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a>引数

`list`: *レコード リスト* または *コンテナー (レコード)*

*レコード リスト* または *コンテナー (レコード)* タイプのデータ ソースの有効なパス。

## <a name="return-values"></a>戻り値

*コンテナー (レコード)*

結果レコード値。

## <a name="usage-notes"></a>使用上の注意

> [!NOTE] 
> この関数は廃止されています。 代わりに `EMPTYRECORD` 関数を使用してください。 詳細については、[EMPTYRECORD](er-functions-record-emptyrecord.md) をご覧ください。

## <a name="example"></a>例

`NULLCONTAINER (SPLIT ("abc", 1))` は、`SPLIT` 関数で返ってきたリストと同じ構造を持つ新しい空のレコードを返します。 詳細については、[SPLIT](er-functions-list-split.md) をご覧ください。

## <a name="additional-resources"></a>追加リソース

[レコード機能](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]