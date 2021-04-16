---
title: FA_SUM ER 関数
description: このトピックでは、FA_SUM 電子申告 (ER) 関数がどのように使用されるかについての情報を提供します。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744298"
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