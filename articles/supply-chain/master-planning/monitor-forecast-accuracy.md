---
title: 予測精度を監視する
description: この記事では、Microsoft Dynamics 365 for Finance and Operations によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7070c15f9ee23cfdba871af68d1fc5954735651
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556809"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="b26a1-103">予測精度を監視する</span><span class="sxs-lookup"><span data-stu-id="b26a1-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b26a1-104">この記事では、Microsoft Dynamics 365 for Finance and Operations によって計算される予測精度のタイプおよび精度の値の表示方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="b26a1-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="b26a1-105">Finance and Operations では、次のタイプの予測の正確性を計算します。</span><span class="sxs-lookup"><span data-stu-id="b26a1-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="b26a1-106">マスター プランによって使用されている履歴予測と履歴需要を比較することによる履歴予測精度。</span><span class="sxs-lookup"><span data-stu-id="b26a1-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="b26a1-107">履歴予測精度の値 (絶対値とパーセント値の両方) を表示するには、**需要予測の詳細** ページの **正確性の表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b26a1-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="b26a1-108">予想を生成するのに使用される予測モデルの見積精度。</span><span class="sxs-lookup"><span data-stu-id="b26a1-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="b26a1-109">精度の割合を **需要予測の詳細** ページの **モデルの詳細 - MAPE** で表示できます。</span><span class="sxs-lookup"><span data-stu-id="b26a1-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="b26a1-110">**Note:** Finance and Operations Demand forecasting Microsoft Azure Machine Learning サービスを使用している場合、内部モデル制度の計算はテスト データ セットに基づきます。</span><span class="sxs-lookup"><span data-stu-id="b26a1-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="b26a1-111">テスト データ セットのサイズを指定するには、**需要予測のパラメータ** ページで **TEST\_SET\_SIZE\_PERCENT** パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="b26a1-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="b26a1-112">たとえば、値を **20** に設定する場合、履歴データの最後の 20 パーセントは内部モデル精度の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b26a1-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="b26a1-113">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="b26a1-113">Additional resources</span></span>
--------

[<span data-ttu-id="b26a1-114">調整された予測の承認</span><span class="sxs-lookup"><span data-stu-id="b26a1-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b26a1-115">需要予測を計算するときに、トランザクション履歴データから異常値を削除</span><span class="sxs-lookup"><span data-stu-id="b26a1-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



