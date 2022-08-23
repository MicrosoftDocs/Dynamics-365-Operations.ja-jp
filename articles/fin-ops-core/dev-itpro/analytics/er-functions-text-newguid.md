---
title: NEWGUID ER 関数
description: この記事では、NEWGUID 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274775"
---
# <a name="newguid-er-function"></a>NEWGUID ER 関数

[!include [banner](../includes/banner.md)]

`NEWGUID` 関数は、新しいグローバルに一意な識別子 (GUID) を生成し、それを *[GUID](er-formula-supported-data-types-primitive.md#guid)* 値として返します。

## <a name="syntax"></a>構文

```vb
NEWGUID ()
```

## <a name="return-values"></a>戻り値

*GUID*

結果の GUID 値です。

## <a name="example"></a>例

`NEWGUID()` は、常に **3afcf7ff-af10-ec11-b6e6-000d3a13209e** などの新しい *GUID* 値を返します。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
