---
title: "予測の精度を監視します。"
description: "この記事では、Microsoft Dynamics 365を計算するついて、精度値の表示方法を説明します予測の精度のタイプを。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>予測の精度を監視します。

この記事では、Microsoft Dynamics 365を計算するついて、精度値の表示方法を説明します予測の精度のタイプを。

Dynamics 365 for Operationsで、予測の精度の次のタイプが計算されます:

-   マスター プランによって使用されている履歴予測と履歴需要を比較することによる履歴予測精度。 履歴予測精度の値 (絶対値とパーセント値の両方) を表示するには、[**需要予測の詳細**] ページの [**正確性の表示**] をクリックします。
-   予想を生成するのに使用される予測モデルの見積精度。 精度の割合を [**需要予測の詳細**] ページの [**モデルの詳細 - MAPE**] で表示できます。 

**注記: **工程の需要予測の、MicrosoftのAzureの機械学習サービスのDynamics 365を使用すると、内部モデルの精度の計算はテストデータ設定に基づいています。 テストデータ設定のサイズを指定するには、**需要予測パラメータ**ページの**テスト\_および\_のサイズを\_**パラメータを設定します。 たとえば、値を **20** に設定する場合、履歴データの最後の 20 パーセントは内部モデル精度の計算に使用されます。


<a name="see-also"></a>参照
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


