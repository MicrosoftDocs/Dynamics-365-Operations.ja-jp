---
title: DATETODATETIME ER 関数
description: このトピックでは、DATETODATETIME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 8c5ad1d304f0914a9ddbca951cdb7419dbcc1f46
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682442"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER 関数

[!include [banner](../includes/banner.md)]

`DATETODATETIME` 関数は、特定の日付値から協定世界時 (グリニッジ標準時\[GMT\]) に変換された *DateTime* 値を返します。

## <a name="syntax"></a>構文

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>引数

`date`: *日付*

変換する日付を表す日付値。

## <a name="return-values"></a>戻り値

*日時*

結果日時値。

## <a name="example-1"></a>例 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` は、現在の Microsoft Dynamics 365 Finance セッションの日付 2015年12月24日を **12/24/2015 12:00:00 AM** として返します。 この例では、**CompInfo** は、**Finance and Operations/Table** タイプの電子申告 (ER) データ ソースで、CompanyInfo テーブルを参照します。

## <a name="example-2"></a>例 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` は、日時値 **2019 12:00:00 11/12 AM** を返します。

## <a name="additional-resources"></a>追加リソース

[日時の関数](er-functions-category-datetime.md)
