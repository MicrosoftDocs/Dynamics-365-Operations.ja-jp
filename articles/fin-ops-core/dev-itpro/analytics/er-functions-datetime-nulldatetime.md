---
title: NULLDATETIME ER 関数
description: このトピックでは、NULLDATETIME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 159abe09f158565fa9c38da530498329ff183fba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563441"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER 関数

[!include [banner](../includes/banner.md)]

`NULLDATETIME` 関数は、**null** の日時値 (1900 年 1 月 1 日) を表す *DateTime* 値を協定世界時 (グリニッジ標準時 \[GMT\]) で返します。

## <a name="syntax"></a>構文

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>戻り値

*日時*

結果日時値。

## <a name="example"></a>例

`DATETIMEFORMAT( NULLDATETIME(), "O")` は、**言語と国/地域の基本設定** セクションにタイムゾーン値 **(GMT) 協定世界時** を持つアプリケーション ユーザーによって開始されたプロセス中に呼び出されると、文字列値 **1900-01-01T00:00:00.0000000+00:00** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]