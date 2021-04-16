---
title: 予測精度の監視
description: このトピックでは、Dynamics 365 Supply Chain Management によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。
author: roxanadiaconu
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
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db8b9fdaf05f58d1386513348c11fcc54887d9c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826470"
---
# <a name="monitor-forecast-accuracy"></a>予測精度の監視

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。

Supply Chain Management では、次のタイプの予測の正確性を計算します。

-   マスター プランによって使用されている履歴予測と履歴需要を比較することによる履歴予測精度。 履歴予測精度の値 (絶対値とパーセント値の両方) を表示するには、**需要予測の詳細** ページの **正確性の表示** をクリックします。
-   予想を生成するのに使用される予測モデルの見積精度。 精度の割合を **需要予測の詳細** ページの **モデルの詳細 - MAPE** で表示できます。 

> [!NOTE]
> 需要予測 Microsoft Azure Machine Learning を使用する場合、内部モデル精度の計算はテスト データ セットに基づきます。 テスト データ セットのサイズを指定するには、**需要予測のパラメータ** ページで **TEST\_SET\_SIZE\_PERCENT** パラメーターを設定します。 たとえば、値を **20** に設定する場合、履歴データの最後の 20 パーセントは内部モデル精度の計算に使用されます。


<a name="additional-resources"></a>追加リソース
--------

[調整された需要予測の承認](authorize-adjusted-forecast.md)

[需要予測を計算するときに、トランザクション履歴データから異常値を削除](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]