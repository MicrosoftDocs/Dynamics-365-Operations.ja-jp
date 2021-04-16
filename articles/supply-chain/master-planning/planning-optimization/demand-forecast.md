---
title: 需要予測を伴うマスター プラン
description: このトピックでは、計画の最適化を使用したマスター プラン中の需要予測を含める方法について説明します。
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup, ReqReduceKey, ForecastModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 88e93e7a363bf5db3d25d7fe6a0ab390f79912b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833308"
---
# <a name="master-planning-with-demand-forecasts"></a><span data-ttu-id="11a3b-103">需要予測を伴うマスター プラン</span><span class="sxs-lookup"><span data-stu-id="11a3b-103">Master planning with demand forecasts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11a3b-104">需要予測を計画の最適化と組み合わせて使用することにより、マスター プランで予測される需要を考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-104">You can use a demand forecast together with Planning Optimization to account for expected demand in your master planning.</span></span> <span data-ttu-id="11a3b-105">需要予測を手動で作成するか、インポートするか、または Microsoft Dynamics 365 Supply Chain Management の需要予測機能を使用して生成することができます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-105">You can manually create a demand forecast, import it, or generate it by using the demand forecasting functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="11a3b-106">需要予測の詳細については、[需要予測の概要](../introduction-demand-forecasting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="11a3b-106">For more information about demand forecasting, see [Demand forecasting overview](../introduction-demand-forecasting.md).</span></span>

> [!NOTE]
> <span data-ttu-id="11a3b-107">個別の予測計画は、計画の最適化ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-107">Separate forecast planning isn't supported with Planning Optimization.</span></span> <span data-ttu-id="11a3b-108">したがって、計画の最適化を使用している場合は、**マスター プラン パラメータ** ページの **現在の予測計画** の設定が無効になります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-108">Therefore, the **Current forecast plan** setting on the **Master planning parameters** page has no effect when you use Planning Optimization.</span></span>

## <a name="set-up-a-master-plan-to-include-a-demand-forecast"></a><span data-ttu-id="11a3b-109">需要予測を含めるためのマスター プランの設定</span><span class="sxs-lookup"><span data-stu-id="11a3b-109">Set up a master plan to include a demand forecast</span></span>

<span data-ttu-id="11a3b-110">計画された需要予測が含まれるようにマスター プランを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11a3b-110">To configure a master plan so that it includes a demand forecast, follow these steps.</span></span>

1. <span data-ttu-id="11a3b-111">**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-111">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="11a3b-112">既存の計画を選択するか、新しい計画を作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-112">Select an existing plan, or create a new plan.</span></span>
1. <span data-ttu-id="11a3b-113">**一般** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-113">On the **General** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="11a3b-114">**予測モデル** - 適用する予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-114">**Forecast model** – Select the forecast model to apply.</span></span> <span data-ttu-id="11a3b-115">このモデルは、現在のマスター プランに対して供給提案が生成されるときに考慮されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-115">This model will be considered when a supply suggestion is generated for the current master plan.</span></span>
    - <span data-ttu-id="11a3b-116">**需要予測を含める** – このオプションを *はい* に設定すると、現在のマスター プランに需要予測を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-116">**Include demand forecast** – Set this option to *Yes* to include the demand forecast in the current master plan.</span></span> <span data-ttu-id="11a3b-117">これを *いいえ* に設定すると、需要予測トランザクションはマスター プランに含まれません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-117">If you set it to *No*, demand forecast transactions won't be included in the master plan.</span></span>
    - <span data-ttu-id="11a3b-118">**予測要件を減らすために使用するメソッド** - 予測要求を減らすために使用するメソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-118">**Method used to reduce forecast requirements** – Select the method that should be used to reduce forecast requirements.</span></span> <span data-ttu-id="11a3b-119">詳細については、このトピックの後半の [予測の下方修正キー](#reduction-keys) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="11a3b-119">For more information, see the [Forecast reduction keys](#reduction-keys) section later in this topic.</span></span>

1. <span data-ttu-id="11a3b-120">**タイムフェンス (日数)** クイックタブで、次のフィールドを設定して、需要予測が発生する期間を指定できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-120">On the **Time fence in days** FastTab, you can set the following fields to specify the period that the demand forecast is included during:</span></span>

    - <span data-ttu-id="11a3b-121">**予測計画** - 個々の補充グループから発生した予測計画タイムフェンスを上書きする場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-121">**Forecast plan** – Set this option to *Yes* to override the forecast plan time fence that originates from the individual coverage groups.</span></span> <span data-ttu-id="11a3b-122">現在のマスター プランの個々の補充グループの値を使用しない場合は、*いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-122">Set it to *No* to use the values from the individual coverage groups for the current master plan.</span></span>
    - <span data-ttu-id="11a3b-123">**予測期間** - **予測計画** オプションを *はい* に設定した場合は、需要予測を適用すべき日数 (今日からの日付) を指定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-123">**Forecast time period** – If you set the **Forecast plan** option to *Yes*, specify the number of days (from today's date) that the demand forecast should be applied.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="11a3b-124">**予測計画** 設定は、計画の最適化ではまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-124">The **Forecast plan** setting isn't yet supported with Planning Optimization.</span></span>

## <a name="set-up-a-coverage-group-to-include-a-demand-forecast"></a><span data-ttu-id="11a3b-125">需要予測を含めるための補充グループの設定</span><span class="sxs-lookup"><span data-stu-id="11a3b-125">Set up a coverage group to include a demand forecast</span></span>

<span data-ttu-id="11a3b-126">需要予測が含まれるように補充グループを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11a3b-126">To configure a coverage group so that it includes a demand forecast, follow these steps.</span></span>

1. <span data-ttu-id="11a3b-127">**マスター プラン \> 設定 \> プラン \> 補充グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-127">Go to **Master planning \> Setup \> Plans \> Coverage groups**.</span></span>
1. <span data-ttu-id="11a3b-128">既存の補充グループを選択するか、新しいグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-128">Select an existing coverage group, or create a new group.</span></span>
1. <span data-ttu-id="11a3b-129">**その他** クイック タブで、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-129">On the **Other** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="11a3b-130">**予測計画タイム フェンス** - 需要予測を適用する日数 (今日の日付から) を入力します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-130">**Forecast plan time fence** – Enter the number of days (from today's date) that the demand forecast should be applied for.</span></span> <span data-ttu-id="11a3b-131">この値は、前のセクションで説明したように、マスター プランの **予測計画** オプションを使用して上書きできます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-131">This value can be overridden by using the **Forecast plan** option on the master plan, as described in the previous section.</span></span>
    - <span data-ttu-id="11a3b-132">**下方修正キー** - 適用する下方修正キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-132">**Reduction key** – Select the reduction key to apply.</span></span> <span data-ttu-id="11a3b-133">詳細については、[予測の下方修正キーを作成および設定](#create-reduction-key) して [このトピックの後の下方修正キーセクションを使用](#use-reduction-key) します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-133">For more information, see the [Create and set up a forecast reduction key](#create-reduction-key) and [Use a reduction key](#use-reduction-key) sections later in this topic.</span></span>
    - <span data-ttu-id="11a3b-134">**予測の下方修正** - **予測要求の削減に使用する方法** フィールドが *トランザクション-下方修正キー* または *トランザクション - 動的期間* に設定されているマスター プランの場合、予測を下方修正するトランザクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-134">**Reduce forecast by** – For master plans where the **Method used to reduce forecast requirements** field is set to *Transactions - reduction key* or *Transactions - dynamic period*, specify which transactions should reduce the forecast.</span></span> <span data-ttu-id="11a3b-135">次の値からいずれか 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-135">Select one of the following values:</span></span>

        - <span data-ttu-id="11a3b-136">**すべてのトランザクション** - すべてのトランザクションで予測を下方修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-136">**All transactions** – All transactions should reduce the forecast.</span></span>
        - <span data-ttu-id="11a3b-137">**注文** - 販売注文の場合のみ、予測を下方修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-137">**Orders** – Only sales orders should reduce the forecast.</span></span>

        > [!NOTE]
        > <span data-ttu-id="11a3b-138">*すべてのトランザクション* を選択した場合、同じ在庫分析コードで需要と供給の両方を持つトランザクションはニュートラルと見なされ、予測下方修正では無視されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-138">If you select *All transactions*, transactions that have both demand and supply in the same inventory dimensions are considered neutral and are ignored during the forecast reduction.</span></span> <span data-ttu-id="11a3b-139">たとえば、計画分析コードが [サイトのみ] に設定されており、倉庫ではない場合、サイト 1、倉庫 11、サイト 1 (倉庫 13) の移動オーダーは無視され、残りの需要予測が下方修正されません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-139">For example, if the planning dimension is set to site only, not warehouse, a transfer order between site 1, warehouse 11, and site 1, warehouse 13, will be ignored and won't reduce the remaining demand forecast.</span></span>

    - <span data-ttu-id="11a3b-140">**会社間注文を含める** - 予測を下方出するときに会社間注文を含める必要がある場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-140">**Include intercompany orders** – Set this option to *Yes* if intercompany orders should be included when the forecast is reduced.</span></span> <span data-ttu-id="11a3b-141">それ以外の場合、*いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-141">Otherwise, set it to *No*.</span></span>
    - <span data-ttu-id="11a3b-142">**需要予測に顧客予測を含める** - 顧客予測を全体的な予測に含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-142">**Include customer forecast in the demand forecast** – Specify whether a customer forecast should be included in the overall forecast.</span></span> <span data-ttu-id="11a3b-143">このオプションにより、実需がどのように需要予測を減少させるか決定されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-143">This option determines how actual demand reduces the forecasted demand.</span></span> <span data-ttu-id="11a3b-144">特定の顧客が購入した品目の供給をマスター プランでカバーするために、この設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-144">You can use it to ensure that master planning covers the supply of items that are purchased by specific customers.</span></span>

        - <span data-ttu-id="11a3b-145">このオプションを *はい* に設定すると、予測全体に顧客予測が含まれます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-145">Set this option to *Yes* to include a customer forecast in the overall forecast.</span></span> <span data-ttu-id="11a3b-146">この場合、実際の顧客要求では、顧客予測と全体的な予測の両方が減少します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-146">In this case, actual customer demand reduces both the customer forecast and the overall forecast.</span></span> <span data-ttu-id="11a3b-147">マスター プランは、全体的な予測数量のみに対応する計画オーダーを生成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-147">Master planning generates planned orders to cover only the overall forecast quantity.</span></span>
        - <span data-ttu-id="11a3b-148">予測全体に顧客予測が含めない場合は、このオプションを *いいえ* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-148">Set this option to *No* if you don't want to include a customer forecast in the overall forecast.</span></span> <span data-ttu-id="11a3b-149">この場合、実際の顧客の需要では顧客の予測のみが減少します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-149">In this case, actual customer demand reduces only the customer forecast.</span></span> <span data-ttu-id="11a3b-150">マスター プランは、全体的な予測数量および各顧客の数量に対する予測の両方をカバーする、計画オーダーを生成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-150">Master planning generates planned orders to cover both the overall forecast quantity and the forecast for each customer quantity.</span></span>

## <a name="forecast-reduction-keys"></a><a name="reduction-keys"></a><span data-ttu-id="11a3b-151">予測下方修正キー</span><span class="sxs-lookup"><span data-stu-id="11a3b-151">Forecast reduction keys</span></span>

<span data-ttu-id="11a3b-152">このセクションでは、予測要求を減らすために使用されるさまざまな方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-152">This section provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="11a3b-153">これには、各メソッドの結果の例が含まれます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-153">It includes examples of the results of each method.</span></span> <span data-ttu-id="11a3b-154">予測下方修正キーの作成、設定、および使用方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-154">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="11a3b-155">予測要求を減らすため予測下方修正キーを使用するいくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-155">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

### <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="11a3b-156">予測要求の削減に使用する方法</span><span class="sxs-lookup"><span data-stu-id="11a3b-156">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="11a3b-157">マスター プランに予測を含める場合、実際の需要が含まれるときに予測要求を削減する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-157">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span> <span data-ttu-id="11a3b-158">マスター プランでは、過去から予測要求が除外されます。つまり、今日の日付より前のすべての予測要求が除外されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-158">Note that master planning excludes forecast requirements from the past, which means all forecast requirements before today's date.</span></span>

<span data-ttu-id="11a3b-159">マスター プランに予測を含め、予測要求を減らすために使用される方法を選択するには、**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-159">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="11a3b-160">**予測モデル** フィールドで、予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-160">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="11a3b-161">**予測要求の削減に使用する方法** フィールドで、方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-161">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="11a3b-162">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-162">The following options are available:</span></span>

- <span data-ttu-id="11a3b-163">None</span><span class="sxs-lookup"><span data-stu-id="11a3b-163">None</span></span>
- <span data-ttu-id="11a3b-164">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="11a3b-164">Percent – reduction key</span></span>
- <span data-ttu-id="11a3b-165">トランザクション - 下方修正キー (計画の最適化ではまだサポートされていません)</span><span class="sxs-lookup"><span data-stu-id="11a3b-165">Transactions – reduction key (not yet supported with Planning Optimization)</span></span>
- <span data-ttu-id="11a3b-166">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="11a3b-166">Transactions – dynamic period</span></span>

<span data-ttu-id="11a3b-167">次のセクションでは、各オプションの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-167">The following sections provide more information about each option.</span></span>

#### <a name="none"></a><span data-ttu-id="11a3b-168">なし</span><span class="sxs-lookup"><span data-stu-id="11a3b-168">None</span></span>

<span data-ttu-id="11a3b-169">**なし** を選択すると、予測要求はマスター スケジューリング時に削減されません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-169">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="11a3b-170">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-170">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="11a3b-171">これらの計画オーダーは、他のタイプの需要に関係なく、推奨数量を管理します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-171">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="11a3b-172">たとえば、販売注文が出された場合、マスター プランは販売注文を供給する追加の計画オーダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-172">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="11a3b-173">予測要求の数量は削減されません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-173">The quantity of the forecast requirements isn't reduced.</span></span>

#### <a name="percent--reduction-key"></a><span data-ttu-id="11a3b-174">率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="11a3b-174">Percent – reduction key</span></span>

<span data-ttu-id="11a3b-175">**率 - 下方修正キー** を選択すると、予測要求は下方修正キーで定義された割合および期間に従って削減されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-175">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="11a3b-176">この場合、マスター プランでは各期間の予測数量 × 下方修正キーとして数量が計算される計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-176">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="11a3b-177">他のタイプの需要がある場合、マスター プランではその要求を供給する計画オーダーも作成されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-177">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

##### <a name="example-percent--reduction-key"></a><span data-ttu-id="11a3b-178">例: 率 – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="11a3b-178">Example: Percent – reduction key</span></span>

<span data-ttu-id="11a3b-179">この例は、下方修正キーによって定義されたパーセンテージおよび期間に従って、下方修正キーが需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-179">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="11a3b-180">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-180">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="11a3b-181">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-181">Month</span></span>    | <span data-ttu-id="11a3b-182">需要予測</span><span class="sxs-lookup"><span data-stu-id="11a3b-182">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="11a3b-183">1 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-183">January</span></span>  | <span data-ttu-id="11a3b-184">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-184">1,000</span></span>           |
| <span data-ttu-id="11a3b-185">2 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-185">February</span></span> | <span data-ttu-id="11a3b-186">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-186">1,000</span></span>           |
| <span data-ttu-id="11a3b-187">3 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-187">March</span></span>    | <span data-ttu-id="11a3b-188">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-188">1,000</span></span>           |
| <span data-ttu-id="11a3b-189">4 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-189">April</span></span>    | <span data-ttu-id="11a3b-190">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-190">1,000</span></span>           |

<span data-ttu-id="11a3b-191">**下方修正キー** ページで、次の行を設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-191">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="11a3b-192">計上額</span><span class="sxs-lookup"><span data-stu-id="11a3b-192">Change</span></span> | <span data-ttu-id="11a3b-193">単位</span><span class="sxs-lookup"><span data-stu-id="11a3b-193">Unit</span></span>  | <span data-ttu-id="11a3b-194">パーセンテージ</span><span class="sxs-lookup"><span data-stu-id="11a3b-194">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="11a3b-195">1</span><span class="sxs-lookup"><span data-stu-id="11a3b-195">1</span></span>      | <span data-ttu-id="11a3b-196">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-196">Month</span></span> | <span data-ttu-id="11a3b-197">100</span><span class="sxs-lookup"><span data-stu-id="11a3b-197">100</span></span>     |
| <span data-ttu-id="11a3b-198">2</span><span class="sxs-lookup"><span data-stu-id="11a3b-198">2</span></span>      | <span data-ttu-id="11a3b-199">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-199">Month</span></span> | <span data-ttu-id="11a3b-200">75</span><span class="sxs-lookup"><span data-stu-id="11a3b-200">75</span></span>      |
| <span data-ttu-id="11a3b-201">3</span><span class="sxs-lookup"><span data-stu-id="11a3b-201">3</span></span>      | <span data-ttu-id="11a3b-202">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-202">Month</span></span> | <span data-ttu-id="11a3b-203">50</span><span class="sxs-lookup"><span data-stu-id="11a3b-203">50</span></span>      |
| <span data-ttu-id="11a3b-204">4</span><span class="sxs-lookup"><span data-stu-id="11a3b-204">4</span></span>      | <span data-ttu-id="11a3b-205">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-205">Month</span></span> | <span data-ttu-id="11a3b-206">25</span><span class="sxs-lookup"><span data-stu-id="11a3b-206">25</span></span>      |

<span data-ttu-id="11a3b-207">品目の補充グループに下方修正キーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-207">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="11a3b-208">その後、**マスター プラン** ページの **予測要求の削減に使用する方法** フィールドで、**率 - 下方修正キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-208">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="11a3b-209">この場合、1 月 1 日に予測のスケジューリングを実行する場合、需要予測要求は、**下方修正キー** ページで設定した率に従って消費されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-209">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="11a3b-210">次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-210">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="11a3b-211">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-211">Month</span></span>                | <span data-ttu-id="11a3b-212">計画オーダーの数量</span><span class="sxs-lookup"><span data-stu-id="11a3b-212">Planned order quantity</span></span> | <span data-ttu-id="11a3b-213">計算</span><span class="sxs-lookup"><span data-stu-id="11a3b-213">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="11a3b-214">1 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-214">January</span></span>              | <span data-ttu-id="11a3b-215">0</span><span class="sxs-lookup"><span data-stu-id="11a3b-215">0</span></span>                      | <span data-ttu-id="11a3b-216">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="11a3b-216">= 0% × 1,000</span></span>   |
| <span data-ttu-id="11a3b-217">2 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-217">February</span></span>             | <span data-ttu-id="11a3b-218">250</span><span class="sxs-lookup"><span data-stu-id="11a3b-218">250</span></span>                    | <span data-ttu-id="11a3b-219">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="11a3b-219">= 25% × 1,000</span></span>  |
| <span data-ttu-id="11a3b-220">3 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-220">March</span></span>                | <span data-ttu-id="11a3b-221">500</span><span class="sxs-lookup"><span data-stu-id="11a3b-221">500</span></span>                    | <span data-ttu-id="11a3b-222">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="11a3b-222">= 50% × 1,000</span></span>  |
| <span data-ttu-id="11a3b-223">4 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-223">April</span></span>                | <span data-ttu-id="11a3b-224">750</span><span class="sxs-lookup"><span data-stu-id="11a3b-224">750</span></span>                    | <span data-ttu-id="11a3b-225">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="11a3b-225">= 75% × 1,000</span></span>  |
| <span data-ttu-id="11a3b-226">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-226">May through December</span></span> | <span data-ttu-id="11a3b-227">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-227">1,000</span></span>                  | <span data-ttu-id="11a3b-228">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="11a3b-228">= 100% × 1,000</span></span> |

#### <a name="transactions--reduction-key"></a><span data-ttu-id="11a3b-229">トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="11a3b-229">Transactions – reduction key</span></span>

<span data-ttu-id="11a3b-230">**トランザクション - 下方修正キー** を選択すると、予測要求は下方修正キーで定義された期間に発生するトランザクションによって削減されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-230">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

##### <a name="example-transactions--reduction-key"></a><span data-ttu-id="11a3b-231">例: トランザクション – 下方修正キー</span><span class="sxs-lookup"><span data-stu-id="11a3b-231">Example: Transactions – reduction key</span></span>

<span data-ttu-id="11a3b-232">この例は、下方修正キーによって定義された期間中に実行される実際の注文が、需要予測要求を減少させる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-232">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="11a3b-233">この例では、**マスター プラン** ページの **予測要求の削減に使用する方法** フィールドで、**トランザクション – 下方修正キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-233">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="11a3b-234">1 月 1 日の時点で次の販売注文が存在します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-234">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="11a3b-235">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-235">Month</span></span>    | <span data-ttu-id="11a3b-236">注文数</span><span class="sxs-lookup"><span data-stu-id="11a3b-236">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="11a3b-237">1 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-237">January</span></span>  | <span data-ttu-id="11a3b-238">956</span><span class="sxs-lookup"><span data-stu-id="11a3b-238">956</span></span>                      |
| <span data-ttu-id="11a3b-239">2 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-239">February</span></span> | <span data-ttu-id="11a3b-240">1,176</span><span class="sxs-lookup"><span data-stu-id="11a3b-240">1,176</span></span>                    |
| <span data-ttu-id="11a3b-241">3 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-241">March</span></span>    | <span data-ttu-id="11a3b-242">451</span><span class="sxs-lookup"><span data-stu-id="11a3b-242">451</span></span>                      |
| <span data-ttu-id="11a3b-243">4 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-243">April</span></span>    | <span data-ttu-id="11a3b-244">119</span><span class="sxs-lookup"><span data-stu-id="11a3b-244">119</span></span>                      |

<span data-ttu-id="11a3b-245">前の例で使用した毎月 1,000 個の同じ需要予測を使用する場合、次の要求数量がマスター プランに転送されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-245">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="11a3b-246">月</span><span class="sxs-lookup"><span data-stu-id="11a3b-246">Month</span></span>                | <span data-ttu-id="11a3b-247">必要な個数</span><span class="sxs-lookup"><span data-stu-id="11a3b-247">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="11a3b-248">1 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-248">January</span></span>              | <span data-ttu-id="11a3b-249">44</span><span class="sxs-lookup"><span data-stu-id="11a3b-249">44</span></span>                        |
| <span data-ttu-id="11a3b-250">2 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-250">February</span></span>             | <span data-ttu-id="11a3b-251">0</span><span class="sxs-lookup"><span data-stu-id="11a3b-251">0</span></span>                         |
| <span data-ttu-id="11a3b-252">3 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-252">March</span></span>                | <span data-ttu-id="11a3b-253">549</span><span class="sxs-lookup"><span data-stu-id="11a3b-253">549</span></span>                       |
| <span data-ttu-id="11a3b-254">4 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-254">April</span></span>                | <span data-ttu-id="11a3b-255">881</span><span class="sxs-lookup"><span data-stu-id="11a3b-255">881</span></span>                       |
| <span data-ttu-id="11a3b-256">5 ～ 12 月</span><span class="sxs-lookup"><span data-stu-id="11a3b-256">May through December</span></span> | <span data-ttu-id="11a3b-257">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-257">1,000</span></span>                     |

#### <a name="transactions--dynamic-period"></a><span data-ttu-id="11a3b-258">トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="11a3b-258">Transactions – dynamic period</span></span>

<span data-ttu-id="11a3b-259">**トランザクション - 動的期間** を選択する場合、予測要求が動的期間中に発生する実際の注文トランザクションから削減されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-259">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="11a3b-260">動的期間は、現在の予測日を含み、次の予測の開始時点で終了します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-260">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="11a3b-261">この場合、マスター プランでは需要予測 (予測要求) を供給する計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-261">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="11a3b-262">ただし、実際の注文トランザクションが出されると、予測要求が削減されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-262">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="11a3b-263">実際のトランザクションは、予測要求の一部を使用します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-263">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="11a3b-264">このオプションを使用すると、次の動作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-264">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="11a3b-265">下方修正キーは必要でないまたは使用されません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-265">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="11a3b-266">予測が完全に減少すると、現在の予測の予測要求は 0 (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-266">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="11a3b-267">将来の予測がない場合、入力された最後の予測からの予測要求は減少します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-267">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="11a3b-268">タイム フェンスは予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-268">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="11a3b-269">プラス在庫日数は予測下方修正の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-269">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="11a3b-270">実際の注文トランザクションが予測要求を超える場合、残りのトランザクションは次の予測の期間には繰り越されません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-270">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

##### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="11a3b-271">例 1: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="11a3b-271">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="11a3b-272">ここでは、**トランザクション - 動的期間** メソッドの使用方法を示す簡単な例を上げます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-272">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="11a3b-273">この例では、次の需要予測がマスター プランに含まれます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-273">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="11a3b-274">日</span><span class="sxs-lookup"><span data-stu-id="11a3b-274">Date</span></span>       | <span data-ttu-id="11a3b-275">需要予測</span><span class="sxs-lookup"><span data-stu-id="11a3b-275">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="11a3b-276">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-276">January 1</span></span>  | <span data-ttu-id="11a3b-277">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-277">1,000</span></span>           |
| <span data-ttu-id="11a3b-278">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-278">February 1</span></span> | <span data-ttu-id="11a3b-279">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-279">1,000</span></span>             |

<span data-ttu-id="11a3b-280">次の販売注文も作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-280">You also create the following sales orders.</span></span>

| <span data-ttu-id="11a3b-281">日</span><span class="sxs-lookup"><span data-stu-id="11a3b-281">Date</span></span>        | <span data-ttu-id="11a3b-282">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="11a3b-282">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="11a3b-283">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-283">January 15</span></span>  | <span data-ttu-id="11a3b-284">200</span><span class="sxs-lookup"><span data-stu-id="11a3b-284">200</span></span>                  |
| <span data-ttu-id="11a3b-285">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="11a3b-285">February 15</span></span> | <span data-ttu-id="11a3b-286">400</span><span class="sxs-lookup"><span data-stu-id="11a3b-286">400</span></span>                  |

<span data-ttu-id="11a3b-287">この場合、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-287">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="11a3b-288">需要予測日</span><span class="sxs-lookup"><span data-stu-id="11a3b-288">Demand forecast date</span></span> | <span data-ttu-id="11a3b-289">件数</span><span class="sxs-lookup"><span data-stu-id="11a3b-289">Quantity</span></span> | <span data-ttu-id="11a3b-290">説明</span><span class="sxs-lookup"><span data-stu-id="11a3b-290">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="11a3b-291">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-291">January 1</span></span>            | <span data-ttu-id="11a3b-292">800</span><span class="sxs-lookup"><span data-stu-id="11a3b-292">800</span></span>      | <span data-ttu-id="11a3b-293">予測要求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="11a3b-293">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="11a3b-294">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-294">January 15</span></span>           | <span data-ttu-id="11a3b-295">200</span><span class="sxs-lookup"><span data-stu-id="11a3b-295">200</span></span>      | <span data-ttu-id="11a3b-296">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="11a3b-296">Sales orders requirements</span></span>             |
| <span data-ttu-id="11a3b-297">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-297">February 1</span></span>           | <span data-ttu-id="11a3b-298">600</span><span class="sxs-lookup"><span data-stu-id="11a3b-298">600</span></span>      | <span data-ttu-id="11a3b-299">予測要求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="11a3b-299">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="11a3b-300">15 年 2月</span><span class="sxs-lookup"><span data-stu-id="11a3b-300">February 15</span></span>          | <span data-ttu-id="11a3b-301">400</span><span class="sxs-lookup"><span data-stu-id="11a3b-301">400</span></span>      | <span data-ttu-id="11a3b-302">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="11a3b-302">Sales orders requirements</span></span>             |

##### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="11a3b-303">例 2: トランザクション – 動的期間</span><span class="sxs-lookup"><span data-stu-id="11a3b-303">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="11a3b-304">ほとんどの場合、トランザクションが特定の予測期間内の需要予測を下方修正するようにシステムが設定されています: 週、月など。</span><span class="sxs-lookup"><span data-stu-id="11a3b-304">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="11a3b-305">これらの期間は下方修正キーで定義されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-305">These periods are defined in the reduction key.</span></span> <span data-ttu-id="11a3b-306">ただし、2 つの需要予測行の間の時間も、*暗黙に* 期間ととらえることもできます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-306">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="11a3b-307">この例では、次の日付および数量について需要予測を作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-307">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="11a3b-308">日</span><span class="sxs-lookup"><span data-stu-id="11a3b-308">Date</span></span>       | <span data-ttu-id="11a3b-309">需要予測</span><span class="sxs-lookup"><span data-stu-id="11a3b-309">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="11a3b-310">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-310">January 1</span></span>  | <span data-ttu-id="11a3b-311">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-311">1,000</span></span>           |
| <span data-ttu-id="11a3b-312">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-312">January 5</span></span>  | <span data-ttu-id="11a3b-313">500</span><span class="sxs-lookup"><span data-stu-id="11a3b-313">500</span></span>             |
| <span data-ttu-id="11a3b-314">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-314">January 12</span></span> | <span data-ttu-id="11a3b-315">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-315">1,000</span></span>           |

<span data-ttu-id="11a3b-316">この予測では、予測日の間にクリア期間がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="11a3b-316">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="11a3b-317">日付 1 と日付 2 と間には 4 日間の期間があり、日付 2 と日付 3 の間には 7 日間の期間があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-317">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="11a3b-318">このような周期が変動するものを、動的期間といいます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-318">These spans are the dynamic periods.</span></span>

<span data-ttu-id="11a3b-319">次の販売注文明細行も作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-319">You also create the following sales order lines.</span></span>

| <span data-ttu-id="11a3b-320">日</span><span class="sxs-lookup"><span data-stu-id="11a3b-320">Date</span></span>                             | <span data-ttu-id="11a3b-321">販売注文数量</span><span class="sxs-lookup"><span data-stu-id="11a3b-321">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="11a3b-322">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-322">December 15 in the previous year</span></span> | <span data-ttu-id="11a3b-323">500</span><span class="sxs-lookup"><span data-stu-id="11a3b-323">500</span></span>                  |
| <span data-ttu-id="11a3b-324">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-324">January 3</span></span>                        | <span data-ttu-id="11a3b-325">100</span><span class="sxs-lookup"><span data-stu-id="11a3b-325">100</span></span>                  |
| <span data-ttu-id="11a3b-326">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-326">January 10</span></span>                       | <span data-ttu-id="11a3b-327">200</span><span class="sxs-lookup"><span data-stu-id="11a3b-327">200</span></span>                  |

<span data-ttu-id="11a3b-328">この場合、次のように予測が削減されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-328">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="11a3b-329">最初の販売注文は、いずれの期間内でもないため、予測を下方修正することはありません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-329">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="11a3b-330">2 番目の販売注文は 1 月 1 日から 1 月 5 日の間に行われるため、1 月 1 日の予測は 100 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-330">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="11a3b-331">3 番目の販売注文は 1 月 5 日から 1 月 12 日の間に行われるため、1 月 5 日の予測は 200 だけ下方修正されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-331">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="11a3b-332">したがって、次の計画オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-332">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="11a3b-333">需要予測日</span><span class="sxs-lookup"><span data-stu-id="11a3b-333">Demand forecast date</span></span>             | <span data-ttu-id="11a3b-334">件数</span><span class="sxs-lookup"><span data-stu-id="11a3b-334">Quantity</span></span> | <span data-ttu-id="11a3b-335">説明</span><span class="sxs-lookup"><span data-stu-id="11a3b-335">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="11a3b-336">前年度の 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-336">December 15 in the previous year</span></span> | <span data-ttu-id="11a3b-337">500</span><span class="sxs-lookup"><span data-stu-id="11a3b-337">500</span></span>      | <span data-ttu-id="11a3b-338">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="11a3b-338">Sales order requirements</span></span>                                            |
| <span data-ttu-id="11a3b-339">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-339">January 1</span></span>                        | <span data-ttu-id="11a3b-340">900</span><span class="sxs-lookup"><span data-stu-id="11a3b-340">900</span></span>      | <span data-ttu-id="11a3b-341">1 月 1 日から 1 月 5 日の期間の予測要求 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="11a3b-341">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="11a3b-342">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-342">January 3</span></span>                        | <span data-ttu-id="11a3b-343">100</span><span class="sxs-lookup"><span data-stu-id="11a3b-343">100</span></span>      | <span data-ttu-id="11a3b-344">販売注文の要件</span><span class="sxs-lookup"><span data-stu-id="11a3b-344">Sales order requirements</span></span>                                            |
| <span data-ttu-id="11a3b-345">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-345">January 5</span></span>                        | <span data-ttu-id="11a3b-346">300</span><span class="sxs-lookup"><span data-stu-id="11a3b-346">300</span></span>      | <span data-ttu-id="11a3b-347">1 月 5 日から 1 月 10 日の期間の予測要求 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="11a3b-347">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="11a3b-348">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="11a3b-348">January 12</span></span>                       | <span data-ttu-id="11a3b-349">1.000</span><span class="sxs-lookup"><span data-stu-id="11a3b-349">1,000</span></span>    | <span data-ttu-id="11a3b-350">1 月 12 日から終了日の期間の予測要求</span><span class="sxs-lookup"><span data-stu-id="11a3b-350">Forecast requirements period January 12 to end</span></span>                      |

### <a name="create-and-set-up-a-forecast-reduction-key"></a><a name="create-reduction-key"></a><span data-ttu-id="11a3b-351">予測下方修正キーの作成および設定</span><span class="sxs-lookup"><span data-stu-id="11a3b-351">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="11a3b-352">予測下方修正キーは、予測要求を削減するため **トランザクション - 下方修正キー** および **率 - 下方修正キー** の方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-352">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="11a3b-353">下方修正キーを作成および設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11a3b-353">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="11a3b-354">**マスター プラン \> 設定 \> 補充 \> 下方修正キー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-354">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="11a3b-355">**新規** を選択して、下方修正キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-355">Select **New** to create a reduction key.</span></span>
3. <span data-ttu-id="11a3b-356">**下方修正キー** フィールドで、予測下方修正キーの固有識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-356">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="11a3b-357">その後、**名前** フィールドで、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-357">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="11a3b-358">各期間の期間および下方修正キーの割合を定義します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-358">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="11a3b-359">**有効日** フィールドは、期間の作成が開始する日付を示します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-359">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="11a3b-360">**有効日を使用** オプションを **はい** に設定すると、有効日の期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-360">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="11a3b-361">**いいえ** に設定すると、マスター プランが実行される日付で期間が開始します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-361">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="11a3b-362">予測下方修正が発生する期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-362">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="11a3b-363">特定の期間の、予測要求を削減する必要がある割合を指定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-363">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="11a3b-364">要件を削減するには正の値、または要件を増加するには負の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-364">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

### <a name="use-a-reduction-key"></a><a name="use-reduction-key"></a><span data-ttu-id="11a3b-365">下方修正キーの使用</span><span class="sxs-lookup"><span data-stu-id="11a3b-365">Use a reduction key</span></span>

<span data-ttu-id="11a3b-366">予測下方修正キーは、品目の補充グループに割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-366">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="11a3b-367">これらの手順に従い、下方修正キーを品目の補充グループに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-367">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="11a3b-368">**マスター プラン \> 設定 \> 補充 \> 補充グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-368">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="11a3b-369">**その他** クイック タブの、**下方修正キー** フィールドで、補充グループに割り当てる下方修正キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-369">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="11a3b-370">その後、下方修正キーは、補充グループに属する品目すべてに適用されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-370">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="11a3b-371">マスター スケジューリング時に予測下方修正の計算に下方修正キーを使用するには、予測計画またはマスター プランの設定でこの設定を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-371">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="11a3b-372">次の場所のいずれかに移動します:</span><span class="sxs-lookup"><span data-stu-id="11a3b-372">Go to one of the following locations:</span></span>

    - <span data-ttu-id="11a3b-373">**マスター プラン \> 設定 \> 計画 \> 予測計画**</span><span class="sxs-lookup"><span data-stu-id="11a3b-373">**Master planning \> Setup \> Plans \> Forecast plans**</span></span>
    - <span data-ttu-id="11a3b-374">**マスター プラン \> 設定 \> 計画 \> マスター プラン**</span><span class="sxs-lookup"><span data-stu-id="11a3b-374">**Master planning \> Setup \> Plans \> Master plans**</span></span>

4. <span data-ttu-id="11a3b-375">**予測計画** または **マスター プラン** ページの、**一般** クイック タブの、**予測要求の削減に使用する方法** フィールドで、**率 - 下方修正キー** または **トランザクション - 下方修正キー** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-375">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

### <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="11a3b-376">トランザクションによる予測の削減</span><span class="sxs-lookup"><span data-stu-id="11a3b-376">Reduce a forecast by transactions</span></span>

<span data-ttu-id="11a3b-377">予測要求の削減のメソッドとして **トランザクション - 下方修正キー** または **トランザクション - 動的期間** を選択すると、予測を削減するトランザクションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-377">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="11a3b-378">**補充グループ** ページの、**その他** クイック タブにある、**予測の削減方法** フィールドで、すべてのトランザクションで予測を削減する必要がある場合は **すべてのトランザクション** を、または販売注文のみで予測を削減する必要がある場合は **販売注文** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-378">On the **Coverage groups** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="forecast-models-and-submodels"></a><span data-ttu-id="11a3b-379">予測モデルおよび下位モデル</span><span class="sxs-lookup"><span data-stu-id="11a3b-379">Forecast models and submodels</span></span>

<span data-ttu-id="11a3b-380">このセクションでは、予測モデルの作成方法と、下位モデルを設定して複数の予測モデルを結合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-380">This section describes how to create forecast models and how to combine multiple forecast models by setting up submodels.</span></span>

<span data-ttu-id="11a3b-381">*予測モデル* により、特定の予測に名前を付け、識別します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-381">A *forecast model* names and identifies a specific forecast.</span></span> <span data-ttu-id="11a3b-382">予測モデルを作成したら、予測明細行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-382">After you've created the forecast model, you can add forecast lines to it.</span></span> <span data-ttu-id="11a3b-383">複数の品目の予測明細行を追加するには、**需要予測明細行** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-383">To add forecast lines for multiple items, use the **Demand forecast lines** page.</span></span> <span data-ttu-id="11a3b-384">選択した特定の品目の予測明細行を追加するには、**リリース済製品** ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-384">To add forecast lines for a specific selected item, use the **Released products** page.</span></span>

<span data-ttu-id="11a3b-385">予測モデルには、他の予測モデルからの予測を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-385">A forecast model can include forecasts from other forecast models.</span></span> <span data-ttu-id="11a3b-386">この結果を実現するには、他の予測モデルを親予測モデルの *下位モデル* として追加します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-386">To achieve this result, you add other forecast models as *submodels* of a parent forecast model.</span></span> <span data-ttu-id="11a3b-387">親予測モデルの下位モデルとして追加する前に、各関連モデルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-387">You must create each relevant model before you can add it as a submodel of a parent forecast model.</span></span>

<span data-ttu-id="11a3b-388">作成された構造により、複数の個々の予測からの入力を結合 (集計) することができるので、予測を制御するための強力な方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-388">The resulting structure gives you a powerful way to control forecasts, because it lets you combine (aggregate) the input from multiple individual forecasts.</span></span> <span data-ttu-id="11a3b-389">したがって、計画の観点から見て、シミュレーションの予測を結合させることは容易です。</span><span class="sxs-lookup"><span data-stu-id="11a3b-389">Therefore, from a planning point of view, it's easy to combine forecasts for simulations.</span></span> <span data-ttu-id="11a3b-390">たとえば、通常の予測と春のプロモーションの予測の組み合わせに基づくシミュレーションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-390">For example, you might set up a simulation that is based on the combination of a regular forecast with the forecast for a spring promotion.</span></span>

### <a name="submodel-levels"></a><span data-ttu-id="11a3b-391">下位モデル レベル</span><span class="sxs-lookup"><span data-stu-id="11a3b-391">Submodel levels</span></span>

<span data-ttu-id="11a3b-392">親予測モデルに追加できる下位モデルの数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-392">There is no limit on the number of submodels that can be added to a parent forecast model.</span></span> <span data-ttu-id="11a3b-393">ただし、構造の深さはレベル 1 のみです。</span><span class="sxs-lookup"><span data-stu-id="11a3b-393">However, the structure can be only one level deep.</span></span> <span data-ttu-id="11a3b-394">つまり、別の予測モデルの下位モデルである予測モデルには、独自の下位モデルを設定することができません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-394">In other words, a forecast model that is a submodel of another forecast model can't have its own submodels.</span></span> <span data-ttu-id="11a3b-395">予測モデルに下位モデルを追加すると、その予測モデルが既に別の予測モデルの下位モデルかどうかがシステムによって確認されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-395">When you add submodels to a forecast model, the system checks whether that forecast model is already a submodel of another forecast model.</span></span>

<span data-ttu-id="11a3b-396">マスター プランが独自の下位モデルを持つ下位モデルを検出した場合、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-396">If master planning encounters a submodel that has its own submodels, you receive an error message.</span></span>

#### <a name="submodel-levels-example"></a><span data-ttu-id="11a3b-397">下位モデル レベルの例</span><span class="sxs-lookup"><span data-stu-id="11a3b-397">Submodel levels example</span></span>

<span data-ttu-id="11a3b-398">予測モデル A には、予測モデル B が下位モデルとして設定されています。</span><span class="sxs-lookup"><span data-stu-id="11a3b-398">Forecast model A has forecast model B as a submodel.</span></span> <span data-ttu-id="11a3b-399">したがって、予測モデル B には独自の下位モデルを設定できません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-399">Therefore, forecast model B can't have its own submodels.</span></span> <span data-ttu-id="11a3b-400">予測モデル B に下位モデルを追加しようとする場合、「予測モデル B はモデル A の下位モデルです」というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-400">If you try to add a submodel to forecast model B, you receive the following error message: "Forecast model B is a submodel for model A."</span></span>

### <a name="aggregating-forecasts-across-forecast-models"></a><span data-ttu-id="11a3b-401">予測モデル間での予測の集計</span><span class="sxs-lookup"><span data-stu-id="11a3b-401">Aggregating forecasts across forecast models</span></span>

<span data-ttu-id="11a3b-402">同じ日に発生した予測明細行は、予測モデルとその下位モデル全体で集計されます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-402">Forecast lines that occur on the same day will be aggregated across their forecast model and its submodels.</span></span>

#### <a name="aggregation-example"></a><span data-ttu-id="11a3b-403">集計の例</span><span class="sxs-lookup"><span data-stu-id="11a3b-403">Aggregation example</span></span>

<span data-ttu-id="11a3b-404">予測モデル A には、予測モデル B および C が下位モデルとして設定されています。</span><span class="sxs-lookup"><span data-stu-id="11a3b-404">Forecast model A has forecast models B and C as submodels.</span></span>

- <span data-ttu-id="11a3b-405">予測モデル A には、6 月 15 日に 2 個の需要予測が含まれています。</span><span class="sxs-lookup"><span data-stu-id="11a3b-405">Forecast model A includes a demand forecast for 2 pieces (pcs) on June 15.</span></span>
- <span data-ttu-id="11a3b-406">予測モデル B には、6 月 15 日に 3 個の需要予測が含まれています。</span><span class="sxs-lookup"><span data-stu-id="11a3b-406">Forecast model B includes a demand forecast for 3 pcs on June 15.</span></span>
- <span data-ttu-id="11a3b-407">予測モデル C には、6 月 15 日に 4 個の需要予測が含まれています。</span><span class="sxs-lookup"><span data-stu-id="11a3b-407">Forecast model C includes a demand forecast for 4 pcs on June 15.</span></span>

<span data-ttu-id="11a3b-408">作成される需要予測は、6 月 15 日に 9 個 (2 + 3 + 4) の単一の需要となります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-408">The resulting demand forecast will be a single demand for 9 pcs (2 + 3 + 4) on June 15.</span></span>

> [!NOTE]
> <span data-ttu-id="11a3b-409">各下位モデルでは独自のパラメーターが使用され、親予測モデルのパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-409">Each submodel uses its own parameters, not the parameters of the parent forecast model.</span></span>

### <a name="create-a-forecast-model"></a><span data-ttu-id="11a3b-410">予測モデルの作成</span><span class="sxs-lookup"><span data-stu-id="11a3b-410">Create a forecast model</span></span>

<span data-ttu-id="11a3b-411">予測モデルを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11a3b-411">To create a forecast model, follow these steps.</span></span>

1. <span data-ttu-id="11a3b-412">**マスター プラン \> 設定 \> 需要予測 \> 予測モデル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-412">Go to **Master planning \> Setup \> Demand forecasting \> Forecast models**.</span></span>
1. <span data-ttu-id="11a3b-413">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-413">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="11a3b-414">新しい予測モデルについて、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-414">Set the following fields for the new forecast model:</span></span>

    - <span data-ttu-id="11a3b-415">**モデル** – モデルの一意識別子を入力します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-415">**Model** – Enter a unique identifier for the model.</span></span>
    - <span data-ttu-id="11a3b-416">**名前** - モデルに、内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-416">**Name** – Enter a descriptive name for the model.</span></span>
    - <span data-ttu-id="11a3b-417">**停止済** – 通常、このオプションは *いいえ* に設定する必要があります 。</span><span class="sxs-lookup"><span data-stu-id="11a3b-417">**Stopped** – Usually, you should set this option to *No*.</span></span> <span data-ttu-id="11a3b-418">モデルに割り当てられているすべての予測明細行の編集を回避する場合は、このオプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-418">Set it to *Yes* only if you want to prevent editing of all forecast lines that are assigned to the model.</span></span>

    > [!NOTE]
    > <span data-ttu-id="11a3b-419">**キャッシュ フロー予測に含める** フィールドと **プロジェクト** クイック タブのフィールドはマスター プランに関連付けることができません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-419">The **Include in cash flow forecasts** field and the fields on the **Project** FastTab aren't related to master planning.</span></span> <span data-ttu-id="11a3b-420">したがって、このコンテキストでは無視して使用できます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-420">Therefore, you can ignore them in this context.</span></span> <span data-ttu-id="11a3b-421">これらの情報は、**プロジェクト管理および会計** モジュールで予測を使用する場合にのみ考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="11a3b-421">You must consider them only when you work with forecasts for the **Project management and accounting** module.</span></span>

### <a name="assign-submodels-to-a-forecast-model"></a><span data-ttu-id="11a3b-422">下位モデルを予測モデルに割り当てる</span><span class="sxs-lookup"><span data-stu-id="11a3b-422">Assign submodels to a forecast model</span></span>

<span data-ttu-id="11a3b-423">予測モデルに下位モデルを割り当てるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="11a3b-423">To assign submodels to a forecast model, follow these steps.</span></span>

1. <span data-ttu-id="11a3b-424">**在庫管理 \> 設定 \> 予測 \> 予測モデル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-424">Go to **Inventory management \> Setup \> Forecast \> Forecast models**.</span></span>
1. <span data-ttu-id="11a3b-425">リスト ペインで、下位モデルを設定する予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-425">In the list pane, select the forecast model to set up a submodel for.</span></span>
1. <span data-ttu-id="11a3b-426">**下位モデル** クイック タブで、**追加** を選択してグリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-426">On the **Submodel** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="11a3b-427">新しい行で、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-427">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="11a3b-428">**下位モデル** – 下位モデルとして追加する予測モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-428">**Submodel** – Select the forecast model to add as a submodel.</span></span> <span data-ttu-id="11a3b-429">この予測モデルは既に存在している必要があります。また、独自の下位モデルを持たせることはできません。</span><span class="sxs-lookup"><span data-stu-id="11a3b-429">This forecast model must already exist, and it must not have any submodels of its own.</span></span>
    - <span data-ttu-id="11a3b-430">**名前** - 下位モデルに、内容を示す名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="11a3b-430">**Name** – Enter a descriptive name for the submodel.</span></span> <span data-ttu-id="11a3b-431">たとえば、親予測モデルに対する下位モデルの関係を示す名前にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="11a3b-431">For example, this name might indicate the submodel's relation to the parent forecast model.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

