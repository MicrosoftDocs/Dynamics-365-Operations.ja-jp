---
title: 半期の減価償却方法
description: このトピックでは、資産の事業供用年度時に 6 か月間の減価償却を計算する半年簡便法を使用して、固定資産の減価償却を計算する方法について説明します。
author: moaamer
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: fb15a293bb8cec1b4faba7bcbd29eb4df7916786
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720395"
---
# <a name="half-year-depreciation-convention-methodology"></a>半期の減価償却方法

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックでは、半年簡便法を使用して減価償却を計算するために固定資産で使用される方法について説明します。 半年簡便法では、資産の事業供用年度時に 6 か月間の減価償却を計算します。 減価償却方法の詳細については、[減価償却方法](Fixed-asset-depreciation-conventions.md) を参照してください。 

6 か月間の減価償却方法を使用する場合、システムは取得年度または資産の事業供用開始年度を使用して、その年度から 5 年の減価償却を計算してから、6 か月を追加します。 このプロセスを示すために、価格 50,000 円で取得され、2020 年 4 月に事業供用が開始された資産を考えてみます。 また、資産の耐用年数を 5 年間と仮定します。

事業供用の初年度は 2020 年 12 月に終了し、資産の 5 年の耐用年数の終了は 2024 年 12 月となります。 半期の減価償却方法では、資産の耐用年数に 6 か月が追加され、耐用年数の終了は 2025 年 6 月となります。 

> 年次減価償却 50,000/5 = 10,000 月次減価償却 10,000/12 = 833.33 <br>
> 初年度減価償却 10,000/2 = 5,000、それ以降の月次減価償却 5,000/9 = 555.56

   [![半期減価償却方法の減価償却スケジュール。](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)

半年簡便法によって追加された減価償却期間の延長は、減価償却のより正確な配賦を提供します。 半年簡便法では、減価償却がより均等になるため、損益計算書の報告に役立ちます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
