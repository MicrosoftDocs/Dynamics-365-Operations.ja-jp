---
title: FA_SUM ER 関数
description: この記事では、FA_SUM 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: bcedbc3df835b219b8df6d05f1db6b331f1e9254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278920"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER 関数

[!include [banner](../includes/banner.md)]

`FA_SUM` 関数は、指定された固定資産品目、価値モデル コード、およびの固定資産額のデータで構成される *コンテナー (レコード)* 値を返します。

## <a name="syntax"></a>構文

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>引数

`fixed asset code`: *文字列*

残高が計算される固定資産品目のコードを表す *文字列* 値。

`value model code`: *文字列*

残高が計算される値モデルのコードを表す *文字列* 値。

`start date`: *日付*

固定資産額が計算された期間の開始日を表す *日付* 値。

`end date`: *日付*

固定資産額が計算された期間の終了日を表す *日付* 値。

## <a name="return-values"></a>戻り値

*コンテナー (レコード)*

結果レコード値。

## <a name="example"></a>例

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` は、**現在** 値モデルと **Date1** から **Date2** の期間のために準備された固定資産 **COMP-000001** の日付コンテナーを返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
