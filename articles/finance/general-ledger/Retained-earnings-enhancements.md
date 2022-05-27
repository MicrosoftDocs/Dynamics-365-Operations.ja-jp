---
title: 財務諸表での利益剰余金計算
description: このトピックでは、財務諸表 **利益剰余金計算** の拡張機能の使用方法について説明します。 この拡張機能は、為替換算を使用する組織に影響します。
author: jiwo
ms.date: 09/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: IT Pro, Developer
ms.reviewer: roschlom
ms.custom: 261824
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-01-09
ms.dyn365.ops.version: Version 10.0.8
ms.openlocfilehash: e3aefd4e3d2ba14021bcb88431abd5da3f980b42
ms.sourcegitcommit: f76fecbc28c9a6048366e8ead70060b1f5d21a97
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/08/2021
ms.locfileid: "7616068"
---
# <a name="retained-earnings-calculation-in-financial-reporting"></a>財務諸表での利益剰余金計算

[!include [banner](../includes/banner.md)]

このトピックでは、財務諸表 **利益剰余金計算** の拡張機能の使用方法について説明します。 この拡張機能は、為替換算を使用する組織に影響します。

> [!NOTE]
> 拡張機能のオン/オフを切り替えるには、サポート チケットを記録してください。
>
> 拡張機能をオンにすると、通貨換算タイプが **トランザクション日** に設定されている利益剰余金勘定は、今年度の変更と年末の為替レートを使用して会計通貨残高を計算します。 いずれかの年末の利益剰余金の合計は、計算された各年の合計になります。

### <a name="what-happens-when-you-turn-on-this-enhancement"></a>この拡張機能をオンにするとどうなりますか?

この例では、12 月 31 日に年度の決算を行います。 **利益剰余金計算** 拡張機能がオンになっている場合、今年度の変更は、その日付の通貨レートを使用して計算されます。 拡張機能がオフになっている場合、12 月 31 日の利益剰余金は USD250.00 です。 レポート通貨での金額は EUR312.50 です。 この金額は、USD250.00 に 1.25 を掛けたものに等しくなります。これは、2021 年 12 月 31 日現在の為替レートです。

拡張機能がオンになっている場合、2021 年 12 月 31 日現在のレポート通貨での利益剰余金は EUR288.75 です。 この数値は、(d) に示すように、計算された残高で構成されます。

| 利益剰余金                                                                                | 通貨 | 2018   | 2019   | 2020   | 2021   |
|--------------------------------------------------------------------------------------------------|:----------:|--------:|--------:|--------:|--------:|
| 拡張機能がオフになっている場合の 12/31/XXXX のバランス (a)。                                    | USD      | 100.00 | 150.00 | 225.00 | 250.00 |
| 拡張機能がオンで、通貨換算が使用されている場合の 12/31/XXXX の残高 (b)。    | USD      | 100.00 | 50.00  | 75.00  | 25.00  |
| 12/31/XXXX (c) の為替レート。                                                                 |          | 1.10   | 1.15   | 1.20   | 1.25   |
| 12/31/XXXX (d) の翻訳済為替レート。 計算は b × c です。                           | EUR      | 110.00 | 57.50  | 90.00  | 31.25  |
| 拡張機能がオンの場合の 2021 年 12 月 31 日の利益剰余金 (a)。                            | USD      | 100.00 | 150.00 | 225.00 | 250.00 |
| 拡張がオフの場合の 12/31/XXXX のレポート通貨での為替レート (a × c)。    | EUR      | 110.00 | 172.50 | 270.00 | 312.50 |
| 拡張機能がオンの場合の 12/31/XXXX のレポート通貨での合計為替 (d)。 | EUR      | 110.00 | 167.50 | 257.50 | 288.75 |

