---
title: "予測精度を監視する"
description: "この記事では、Microsoft Dynamics 365 for Operations によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 580b45263b45e6ef730b0fac32575fcdd9c358b6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="monitor-forecast-accuracy"></a>予測精度を監視する

[!include[banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Operations によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。

Dynamics 365 for Operations では、次のタイプの予測の正確性を計算します:

-   マスター プランによって使用されている履歴予測と履歴需要を比較することによる履歴予測精度。 履歴予測精度の値 (絶対値とパーセント値の両方) を表示するには、[**需要予測の詳細**] ページの [**正確性の表示**] をクリックします。
-   予想を生成するのに使用される予測モデルの見積精度。 精度の割合を [**需要予測の詳細**] ページの [**モデルの詳細 - MAPE**] で表示できます。 

[**注記:**] Dynamics 365 for Operations Demand forecasting Microsoft Azure Machine Learning サービスを使用している場合、内部モデル精度の計算はテスト データ セットに基づきます。 テスト データ セットのサイズを指定するには、[**需要予測のパラメータ**] ページで [**TEST\_SET\_SIZE\_PERCENT**] パラメーターを設定します。 たとえば、値を **20** に設定する場合、履歴データの最後の 20 パーセントは内部モデル精度の計算に使用されます。


<a name="see-also"></a>参照
--------

[調整された予測の承認](authorize-adjusted-forecast.md)

[需要予測を計算するときにトランザクション履歴データから異常値を削除する](remove-historical-outliers-calculating-demand-forecast.md)




