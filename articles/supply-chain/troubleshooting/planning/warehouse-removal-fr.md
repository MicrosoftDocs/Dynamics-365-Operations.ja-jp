---
title: 予測明細行から倉庫需要予測分析コードを削除できない
description: 予測明細行から倉庫需要予測分析コードを削除できません。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026680"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="909ea-103">予測明細行から倉庫需要予測分析コードを削除できない</span><span class="sxs-lookup"><span data-stu-id="909ea-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="909ea-104">KB 番号: 4614408</span><span class="sxs-lookup"><span data-stu-id="909ea-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="909ea-105">現象</span><span class="sxs-lookup"><span data-stu-id="909ea-105">Symptoms</span></span>

<span data-ttu-id="909ea-106">この問題は、**需要予測パラメータ** ページの **予測分析コード** タブで **倉庫** 分析コードが割り当てられていない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="909ea-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="909ea-107">しかし、**倉庫** 列は **需要予測** ページ (**マスター プラン \> 予測 \> 手動予測エンティティ \> 需要予測明細行**) に表示されます 。</span><span class="sxs-lookup"><span data-stu-id="909ea-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="909ea-108">解像度</span><span class="sxs-lookup"><span data-stu-id="909ea-108">Resolution</span></span>

<span data-ttu-id="909ea-109">**需要予測パラメータ** ページの **予測分析コード** タブの設定は、**需要予測** ページ には影響しません。</span><span class="sxs-lookup"><span data-stu-id="909ea-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="909ea-110">予測コードは、調整済み需要予測で生成および表示されるベースライン予測を制御します。</span><span class="sxs-lookup"><span data-stu-id="909ea-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="909ea-111">ただし、「実際の」需要予測に必要な分析コードは制御しません。</span><span class="sxs-lookup"><span data-stu-id="909ea-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="909ea-112">**調整済需要予測** ページに表示されるレコードを承認することで、予測モデルの「実際の」予測エントリに変換できます。</span><span class="sxs-lookup"><span data-stu-id="909ea-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="909ea-113">その後、そのモデルをマスター プランに使用できます。</span><span class="sxs-lookup"><span data-stu-id="909ea-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="909ea-114">**需要予測** ページでは、需要予測明細行に表示される「実際の」予測の分析コードが在庫分析コードの一部になります。</span><span class="sxs-lookup"><span data-stu-id="909ea-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="909ea-115">(この動作は、販売注文明細行の動作と似ています。) **倉庫** を必須の在庫分析コードとして使用するようシステムを設定していない場合は、ページをカスタマイズして列を非表示にできます。</span><span class="sxs-lookup"><span data-stu-id="909ea-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
