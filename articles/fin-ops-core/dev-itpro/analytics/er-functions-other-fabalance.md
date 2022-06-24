---
title: FA_BALANCE ER 機能
description: この記事では、FA_BALANCE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c3dd44f0d5ff143189b2c55c4df80847c2161231
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902686"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER 機能

[!include [banner](../includes/banner.md)]

`FA_BALANCE` 関数は、指定された固定資産品目、価値モデル コード、レポート年度、およびレポート日付の固定資産残高のデータで構成される *コンテナー (レコード)* 値を返します。

## <a name="syntax"></a>構文

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>引数

`fixed asset code`: *文字列*

残高が計算される固定資産品目のコードを表す *文字列* 値。

`value model code`: *文字列*

残高が計算される値モデルのコードを表す *文字列* 値。

`reporting year`: *列挙型*

残高計算の期間を定義する **AssetYear** 申請列挙型の列挙値。

`reporting date`: *日付*

残高計算の日付を定義する *日付* 値。

## <a name="return-values"></a>戻り値

*コンテナー (レコード)*

結果レコード値。

## <a name="example"></a>例

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` は、現在のアプリケーション セッションの日付で **現在** 値モデル用に準備された固定資産 **COMP-000001** の残高のデータ コンテナーを返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]