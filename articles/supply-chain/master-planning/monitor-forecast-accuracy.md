---
title: 予測精度の監視
description: このトピックでは、Dynamics 365 Supply Chain Management によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14d23ae800240ebb10ae085acf3ed981a22f1574
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470292"
---
# <a name="monitor-forecast-accuracy"></a>予測精度の監視

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。

Supply Chain Management では、次のタイプの予測の正確性を計算します。

-   マスター プランによって使用されている履歴予測と履歴需要を比較することによる履歴予測精度。 履歴予測精度の値 (絶対値とパーセント値の両方) を表示するには、**需要予測の詳細** ページの **正確性の表示** をクリックします。
-   予想を生成するのに使用される予測モデルの見積精度。 精度の割合を **需要予測の詳細** ページの **モデルの詳細 - MAPE** で表示できます。 

> [!NOTE]
> 需要予測 Microsoft Azure Machine Learning を使用する場合、内部モデル精度の計算はテスト データ セットに基づきます。 テスト データ セットのサイズを指定するには、**需要予測のパラメータ** ページで **TEST\_SET\_SIZE\_PERCENT** パラメーターを設定します。 たとえば、値を **20** に設定する場合、履歴データの最後の 20 パーセントは内部モデル精度の計算に使用されます。


## <a name="additional-resources"></a>追加リソース

[調整された需要予測の承認](authorize-adjusted-forecast.md)

[需要予測を計算するときに、トランザクション履歴データから異常値を削除](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]