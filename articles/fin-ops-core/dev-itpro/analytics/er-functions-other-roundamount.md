---
title: ROUNDAMOUNT ER 機能
description: このトピックでは、ROUNDAMOUNT 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 15a84b086b324ec390d88e8b2617022ad4773977
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683066"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT ER 機能

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT` 関数は、指定された丸めルールに従って、指定された数値を最も近い別の数値の倍数に丸めた結果の *実際* 値を返します。

## <a name="syntax"></a>構文

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>引数

`number`: *Int* または *Real*

丸める必要のある数値。

`decimals`: *Int* または *Real*

`number` パラメーターの値を倍数に丸める必要がある数。

`round rule`: *列挙値*

丸めルールを定義する **RoundOffType** 列挙型の列挙値。 この列挙型は、次の値を提供します。

- 標準 (通常)
- 下方向 (RoundDown)
- 切り上げ (RoundUp)

## <a name="return-values"></a>戻り値

*実績*

結果数値は、`decimals` パラメーターで指定された値の倍数で、`number` パラメーターで指定された値に近いです。

## <a name="usage-notes"></a>使用上の注意

`number` パラメーターがゼロの場合、この関数は常にゼロを返します。

`decimals` パラメーターがゼロのとき、この関数が既定の丸め値に丸めます `round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、既定の丸め値は **0.01** です。 それ以外の場合、既定の丸め値 **1.0** です。

`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、この関数は最も近い丸め金額を丸めます。

`round rule` パラメーターが **RoundOffType.RoundDown** に設定されると、この関数は最も近い丸め金額をゼロに向かって丸めます。

`round rule` パラメーターが **RoundOffType.RoundUp** に設定されると、この関数はゼロから最も近い丸め金額に丸めます。

`round rule` パラメーターが **RoundOffType.Ordinary** に設定されると、この機能は [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel 機能および [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ 機能のように動作します。

## <a name="remarks"></a>備考

指定した小数点以下の桁数に数値を丸めるには、[ROUND](er-functions-mathematical-round.md) 機能を使用します。

## <a name="example"></a>例

**model.RoundOff** パラメーターが **RoundOffType.Ordinary** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 7.35 を返します。 

**model.RoundOff** パラメーターが **RoundOffType.RoundDown** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 7.35 を返します。 

**model.RoundOff** パラメーターが **RoundOffType.RoundUp** に設定されると、`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` は 8.4 を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)

[算術関数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]