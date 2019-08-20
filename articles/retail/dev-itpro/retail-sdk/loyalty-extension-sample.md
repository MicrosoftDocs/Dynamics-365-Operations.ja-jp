---
title: ロイヤルティの拡張機能のサンプル
description: このトピックでは、顧客がロイヤルティ ポイントを獲得し、同じトランザクションでロイヤルティ ポイントを使用して支払ができるようにシステムを設定する方法について説明します。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 196163
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-05-15
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 48b47559f8a349534fc3f70945d751ef376bfc40
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833117"
---
# <a name="loyalty-extension-sample"></a><span data-ttu-id="1fea2-103">ロイヤルティの拡張機能のサンプル</span><span class="sxs-lookup"><span data-stu-id="1fea2-103">Loyalty extension sample</span></span>

[!include [banner](../../../includes/banner.md)]

## <a name="scenario"></a><span data-ttu-id="1fea2-104">シナリオ</span><span class="sxs-lookup"><span data-stu-id="1fea2-104">Scenario</span></span>

<span data-ttu-id="1fea2-105">小売業者は、顧客がロイヤルティ ポイントを取得し、1 つのトランザクションでロイヤルティ ポイントを使用して支払うことができるように求めています。</span><span class="sxs-lookup"><span data-stu-id="1fea2-105">A retailer wants customers to be able to earn loyalty points and pay by using loyalty points in a single transaction.</span></span> 

## <a name="scenario-details"></a><span data-ttu-id="1fea2-106">シナリオの詳細</span><span class="sxs-lookup"><span data-stu-id="1fea2-106">Scenario details</span></span>

<span data-ttu-id="1fea2-107">小売業者は、チャネルのロイヤルティ スキームを設定し、そのスキームをロイヤルティ プログラムと関連付けました。</span><span class="sxs-lookup"><span data-stu-id="1fea2-107">The retailer has set up a loyalty scheme for the channel and associated that scheme with a loyalty program.</span></span> <span data-ttu-id="1fea2-108">ロイヤルティ スキーマには、収益と償還のルールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1fea2-108">The loyalty scheme includes some earning and redemption rules.</span></span> <span data-ttu-id="1fea2-109">小売業者は、顧客がロイヤルティ ポイントを使用して、部分的に取引金額を支払うことができるようにしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="1fea2-109">The retailer wants customers to be able to partially pay a transaction amount by using their loyalty points.</span></span> <span data-ttu-id="1fea2-110">顧客は、他の支払い方法を使用して支払う残りのトランザクション金額に対してロイヤルティ ポイントを獲得することができます。</span><span class="sxs-lookup"><span data-stu-id="1fea2-110">The customers should then be able to earn loyalty points for the remaining transaction amount that they pay by using other payment methods.</span></span>

## <a name="assumptions"></a><span data-ttu-id="1fea2-111">前提</span><span class="sxs-lookup"><span data-stu-id="1fea2-111">Assumptions</span></span>

<span data-ttu-id="1fea2-112">ロイヤルティの設定が提供する柔軟性のため、このシナリオはすばやく非常に複雑になります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-112">Because of the flexibility that the loyalty setup provides, this scenario can quickly become very complex.</span></span> <span data-ttu-id="1fea2-113">このサンプルの複雑さを軽減するためにいくつかの仮定をしました。</span><span class="sxs-lookup"><span data-stu-id="1fea2-113">We have made some assumptions to reduce the complexity of this sample.</span></span> <span data-ttu-id="1fea2-114">ただし、これらの前提条件は、現実の例から遠くかけ離れてはいません。</span><span class="sxs-lookup"><span data-stu-id="1fea2-114">However, these assumptions aren't far removed from the real-world examples.</span></span> <span data-ttu-id="1fea2-115">前提条件を次に示します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-115">Here are the assumptions:</span></span>

+ <span data-ttu-id="1fea2-116">ロイヤルティ プログラムに関連付けられている階層はありません。</span><span class="sxs-lookup"><span data-stu-id="1fea2-116">No tiers are associated with the loyalty program.</span></span>
+ <span data-ttu-id="1fea2-117">1 つのロイヤルティ スキームと 1 つのロイヤルティ報酬ポイント タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-117">There is a single loyalty scheme and a single loyalty reward point type.</span></span>
+ <span data-ttu-id="1fea2-118">すべての商品カテゴリに適用される単一の収益ルールがあります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-118">There is a single earning rule that applies to all product categories.</span></span> <span data-ttu-id="1fea2-119">たとえば、このルールは、顧客が消費する $1 ごとに、0.1 の報酬ポイントを獲得するよう指定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-119">For example, this rule might specify that, for every $1 that the customer spends, he or she earns 0.1 reward point.</span></span> 
+ <span data-ttu-id="1fea2-120">すべての商品カテゴリに適用される単一の引き換えルールがあります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-120">There is a single redemption rule that applies to all product categories.</span></span> <span data-ttu-id="1fea2-121">たとえば、このルールは、1 つの報酬ポイントが $1 と同じであるよう指定する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-121">For example, this rule might specify that one reward point is equivalent to $1.</span></span>

> [!NOTE] 
> <span data-ttu-id="1fea2-122">ここで触れている収益と償還のルールは単なる例に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="1fea2-122">The earning and redemption rules that are mentioned here are just examples.</span></span> <span data-ttu-id="1fea2-123">このサンプルでは、ハードコーディングされた値があります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-123">For this sample, we have hard-coded the values.</span></span> <span data-ttu-id="1fea2-124">生産シナリオでは、値は代わりにデータベースから読み取られる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-124">For a production scenario, the values should be read from the database instead.</span></span>

## <a name="customization-approach"></a><span data-ttu-id="1fea2-125">カスタマイズ方法</span><span class="sxs-lookup"><span data-stu-id="1fea2-125">Customization approach</span></span>

<span data-ttu-id="1fea2-126">このカスタマイズを 2 つの手順で実装します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-126">We implement this customization in two steps.</span></span> <span data-ttu-id="1fea2-127">手順 1 では、ロイヤルティ ポイントがトランザクションに使用されなかったかのようにポイントを獲得します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-127">In step 1, points will be earned as though loyalty points weren't used in the transaction.</span></span> <span data-ttu-id="1fea2-128">次に、ステップ 2 で獲得された余分なポイントは、償還されたポイントに基づいて減額されます。</span><span class="sxs-lookup"><span data-stu-id="1fea2-128">Then, in step 2, the extra points that were earned will be reduced, based on the points that were redeemed.</span></span>

<span data-ttu-id="1fea2-129">ロイヤリティ機能には 6 つのサービス リクエストがあります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-129">There are six service requests for the loyalty feature:</span></span>

+ <span data-ttu-id="1fea2-130">GetLoyaltyCardStatusServiceRequest</span><span class="sxs-lookup"><span data-stu-id="1fea2-130">GetLoyaltyCardStatusServiceRequest</span></span>
+ <span data-ttu-id="1fea2-131">CalculateLoyaltyRewardPointsServiceRequest</span><span class="sxs-lookup"><span data-stu-id="1fea2-131">CalculateLoyaltyRewardPointsServiceRequest</span></span>
+ <span data-ttu-id="1fea2-132">IssueLoyaltyCardServiceRequest</span><span class="sxs-lookup"><span data-stu-id="1fea2-132">IssueLoyaltyCardServiceRequest</span></span>
+ <span data-ttu-id="1fea2-133">FillInLoyaltyRewardPointLinesForSalesServiceRequest</span><span class="sxs-lookup"><span data-stu-id="1fea2-133">FillInLoyaltyRewardPointLinesForSalesServiceRequest</span></span>
+ <span data-ttu-id="1fea2-134">FillInLoyaltyRewardPointLinesForReturnServiceRequest</span><span class="sxs-lookup"><span data-stu-id="1fea2-134">FillInLoyaltyRewardPointLinesForReturnServiceRequest</span></span>
+ <span data-ttu-id="1fea2-135">FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest</span><span class="sxs-lookup"><span data-stu-id="1fea2-135">FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest</span></span>

<span data-ttu-id="1fea2-136">キャッシュ・アンド・キャリー取引の特典ポイントを計算するために、システムは販売取引行に対して  **FillInLoyaltyRewardPointLinesForSalesServiceRequest** を使用します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-136">To calculate the reward points for a cash-and-carry transaction, the system uses **FillInLoyaltyRewardPointLinesForSalesServiceRequest** for sales transaction lines.</span></span> <span data-ttu-id="1fea2-137">この要求は、**FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** を使用して実際の報酬計算を行います。</span><span class="sxs-lookup"><span data-stu-id="1fea2-137">This request, in turn, uses **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** to do the actual reward calculation.</span></span> <span data-ttu-id="1fea2-138">同様に、システムは返品トランザクション ラインに **FillInLoyaltyRewardPointLinesForReturnServiceRequest** を使用し、この要求は **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** も使用して実際の報酬計算を行います。</span><span class="sxs-lookup"><span data-stu-id="1fea2-138">Similarly, the system uses **FillInLoyaltyRewardPointLinesForReturnServiceRequest** for return transaction lines, and this request also uses **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** to do the actual reward calculation.</span></span> <span data-ttu-id="1fea2-139">ロイヤルティ機能の最初から用意されている実装内容では、顧客は同じトランザクションでロイヤルティ ポイントの引き換えと獲得を両方できません。</span><span class="sxs-lookup"><span data-stu-id="1fea2-139">In the out-of-box implementation of the loyalty feature, customers can't both redeem and earn loyalty points in the same transaction.</span></span> <span data-ttu-id="1fea2-140">つまり、販売トランザクションに、ロイヤルティ カードの支払/入金明細行がある場合、**FillInLoyaltyRewardPointLinesForSalesServiceRequest** は特典ポイントを計算するために、**FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** を呼び出しません。</span><span class="sxs-lookup"><span data-stu-id="1fea2-140">In other words, if the sales transaction has a tender line for the loyalty card, **FillInLoyaltyRewardPointLinesForSalesServiceRequest** doesn't call **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** to calculate the reward points.</span></span> 

<span data-ttu-id="1fea2-141">ロイヤルティ ポイントを同じ取引で引き換えて獲得するには、1 つのサービス要求 **FillInLoyaltyRewardPointLinesForSalesServiceRequest** を使用します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-141">To enable loyalty points to be redeemed and earned in the same transaction, we will work with one service request, **FillInLoyaltyRewardPointLinesForSalesServiceRequest**.</span></span>

### <a name="step-1"></a><span data-ttu-id="1fea2-142">ステップ１</span><span class="sxs-lookup"><span data-stu-id="1fea2-142">Step 1</span></span> 

<span data-ttu-id="1fea2-143">シナリオでは、報酬ポイントを計算するため **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** を常に呼び出すように、**FillInLoyaltyRewardPointLinesForSalesServiceRequest** を実装する必要があります</span><span class="sxs-lookup"><span data-stu-id="1fea2-143">For our scenario, we must implement **FillInLoyaltyRewardPointLinesForSalesServiceRequest** in such a way that it always calls **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** to calculate the reward points.</span></span> <span data-ttu-id="1fea2-144">ただし、この変更により、ロイヤルティ ポイントを使用して顧客が支払う金額に基づいて、余分に獲得したポイントを計算するシステムとなります。</span><span class="sxs-lookup"><span data-stu-id="1fea2-144">However, this change will cause the system to calculate extra earned points, based on the amount that the customer pays by using loyalty points.</span></span> <span data-ttu-id="1fea2-145">したがって、獲得ポイントを適切な額だけ減らすことができなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1fea2-145">Therefore, we must be able to reduce the earned points by an appropriate amount.</span></span> <span data-ttu-id="1fea2-146">この調整は、ステップ 2 で行われます。</span><span class="sxs-lookup"><span data-stu-id="1fea2-146">This adjustment is done in step 2.</span></span>

### <a name="step-2"></a><span data-ttu-id="1fea2-147">ステップ２</span><span class="sxs-lookup"><span data-stu-id="1fea2-147">Step 2</span></span>

<span data-ttu-id="1fea2-148">拡張性フレームワークが **FillInLoyaltyRewardPointLinesForSalesServiceRequest** で提供する事後トリガー メカニズムを活用します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-148">We take advantage of the post trigger mechanism that the extensibility framework provides on **FillInLoyaltyRewardPointLinesForSalesServiceRequest**.</span></span> <span data-ttu-id="1fea2-149">転記トリガーでは、獲得および引き換えのルールを使用して、引き換えた各報酬ポイントに対して獲得した余分なポイント数を決定します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-149">In the post trigger, we will use the earning and redemption rules to determine how many extra points were earned for each reward point that was redeemed.</span></span> <span data-ttu-id="1fea2-150">次に、これらの余分なポイントを差し引いて、正確な金額を取得します。</span><span class="sxs-lookup"><span data-stu-id="1fea2-150">We will then subtract those extra points to get the correct amount.</span></span>

#### <a name="implement-fillinloyaltyrewardpointlinesforsalesservicerequest"></a><span data-ttu-id="1fea2-151">FillInLoyaltyRewardPointLinesForSalesServiceRequest の実装</span><span class="sxs-lookup"><span data-stu-id="1fea2-151">Implement FillInLoyaltyRewardPointLinesForSalesServiceRequest</span></span> 

```cs
namespace Contoso
{
    namespace Commerce.Runtime.EarnRedeemLoyalty
    {
        using System;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        using Microsoft.Dynamics.Commerce.Runtime.DataServices.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
        using System.Collections.Generic;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        public class FillInLoyaltyRewardPointLinesForSalesHandler : IRequestHandler
        {
            /// <summary>
            /// Gets the collection of supported request types by this handler.
            /// </summary>
            public IEnumerable<Type> SupportedRequestTypes
            {
                get
                {
                    return new[]
                    {
                        typeof(FillInLoyaltyRewardPointLinesForSalesServiceRequest),
                    };
                }
            }
            /// <summary>
            /// Entry point to FillInLoyaltyRewardPointLinesForSalesServiceRequest service.
            /// </summary>
            /// <param name="request">The request to execute.</param>
            /// <returns>Returns the SalesTransaction object with the one or more LoyaltyRewardPointLines.</returns>
            public Response Execute(Request request)
            {
                ThrowIf.Null(request, "request");
                var LoyaltyRewardPointLinesForSalesServiceRequest = (FillInLoyaltyRewardPointLinesForSalesServiceRequest)request;
                SalesTransaction salesTransaction = LoyaltyRewardPointLinesForSalesServiceRequest.SalesTransaction;
                // Call the service to calculate the loyalty reward points.                
                var fillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest = new FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest(salesTransaction, LoyaltyRewardPointLinesForSalesServiceRequest.EarnSchemeLines, LoyaltyRewardPointEntryType.Earn);
                var fillInLoyaltyRewardPointLinesForEarnOrDeductServiceResponse = request.RequestContext.Execute<SingleEntityDataServiceResponse<SalesTransaction>>(fillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest);
                salesTransaction = fillInLoyaltyRewardPointLinesForEarnOrDeductServiceResponse.Entity;
                return new SingleEntityDataServiceResponse<SalesTransaction>(salesTransaction);
            }
        }
    }
}
```

#### <a name="implement-the-post-trigger-for-fillinloyaltyrewardpointlinesforsalesservicerequest"></a><span data-ttu-id="1fea2-152">FillInLoyaltyRewardPointLinesForSalesServiceRequest の転記トリガーの実装</span><span class="sxs-lookup"><span data-stu-id="1fea2-152">Implement the post trigger for FillInLoyaltyRewardPointLinesForSalesServiceRequest</span></span>

```cs
namespace Contoso
{
    namespace Commerce.Runtime.Sample.EarnRedeemLoyalty
    {
        using System;
        using System.Collections.Generic;
        using System.Linq;
        using Microsoft.Dynamics.Commerce.Runtime;
        using Microsoft.Dynamics.Commerce.Runtime.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
        using Microsoft.Dynamics.Commerce.Runtime.DataModel;
        class AdjustLoyatyRewardsTrigger : IRequestTrigger
        {
            public IEnumerable<Type> SupportedRequestTypes
            {
                get { return new[] { typeof(FillInLoyaltyRewardPointLinesForSalesServiceRequest) }; }
            }
            public void OnExecuted(Request request, Response response)
            {
                ThrowIf.Null(request, "request");
                var LoyaltyRewardPointSalesServiceRequest = (FillInLoyaltyRewardPointLinesForSalesServiceRequest)request;
                SalesTransaction salesTransaction = LoyaltyRewardPointSalesServiceRequest.SalesTransaction;

                if (salesTransaction.LoyaltyRewardPointLines != null)
                {
                    decimal totalReedeemedPoints = 0m;
                    decimal extraEarnedPoints = 0m;
                    
                    // Find the redeemed reward lines in the transaction and calculate the total redeemed reward points
                    IEnumerable<LoyaltyRewardPointLine> redeemLoyaltyRewardPointLines = salesTransaction.LoyaltyRewardPointLines.Where<LoyaltyRewardPointLine>(line => line.EntryType == LoyaltyRewardPointEntryType.Redeem);
                    if (redeemLoyaltyRewardPointLines.Count() > 0)
                    {
                        foreach (var rewardPointLine in redeemLoyaltyRewardPointLines)
                        {
                            totalReedeemedPoints += rewardPointLine.RewardPointAmountQuantity;
                        }
                        // Calculate the number of extra earned points for every redeemed point.
                        // If the earning rules stated that for every $1 spent, the user earns X points and redemption rule was that Y points equal $1 then, for every redemption point the user earns X/Y extra earn points.
                        // Based on the above logic, in this sample, for every redeemed point the user earns .1/1 = .1 extra earned points.
                        extraEarnedPoints = .1m * totalReedeemedPoints; 
                    }
                    // Reduce the amount of earned points by the extraEarnedPoints calculated above.
                    IEnumerable<LoyaltyRewardPointLine> earnLoyaltyRewardPointLines = salesTransaction.LoyaltyRewardPointLines.Where<LoyaltyRewardPointLine>(line => line.EntryType == LoyaltyRewardPointEntryType.Earn);
                    if (earnLoyaltyRewardPointLines.Count() > 0)
                    {
                        earnLoyaltyRewardPointLines.FirstOrDefault().RewardPointAmountQuantity -= extraEarnedPoints;
                    }
                }
            }
            public void OnExecuting(Request request)
            { }
        }
    }
}
```
