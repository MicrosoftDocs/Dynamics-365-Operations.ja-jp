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
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 196163
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-05-15
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ad2a43d543ee84145b2bea7c43e29f33e82d6b72
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368433"
---
# <a name="loyalty-extension-sample"></a>ロイヤルティの拡張機能のサンプル

[!include [banner](../../../includes/banner.md)]

## <a name="scenario"></a>シナリオ 
小売業者は、顧客がロイヤルティ ポイントを取得し、1 つのトランザクションでロイヤルティ ポイントを使用して支払うことができるように求めています。 

## <a name="scenario-details"></a>シナリオの詳細
小売業者は、チャネルのロイヤルティ スキームを設定し、そのスキームをロイヤルティ プログラムと関連付けました。 ロイヤルティ スキーマには、収益と償還のルールが含まれています。 小売業者は、顧客がロイヤルティ ポイントを使用して、部分的に取引金額を支払うことができるようにしたいと考えています。 顧客は、他の支払い方法を使用して支払う残りのトランザクション金額に対してロイヤルティ ポイントを獲得することができます。

## <a name="assumptions"></a>前提
ロイヤルティの設定が提供する柔軟性のため、このシナリオはすばやく非常に複雑になります。 このサンプルの複雑さを軽減するためにいくつかの仮定をしました。 ただし、これらの前提条件は、現実の例から遠くかけ離れてはいません。 前提条件を次に示します。

+ ロイヤルティ プログラムに関連付けられている階層はありません。
+ 1 つのロイヤルティ スキームと 1 つのロイヤルティ報酬ポイント タイプがあります。
+ すべての商品カテゴリに適用される単一の収益ルールがあります。 たとえば、このルールは、顧客が消費する $1 ごとに、0.1 の報酬ポイントを獲得するよう指定する可能性があります。 
+ すべての商品カテゴリに適用される単一の引き換えルールがあります。 たとえば、このルールは、1 つの報酬ポイントが $1 と同じであるよう指定する可能性があります。

> [!NOTE] 
> ここで触れている収益と償還のルールは単なる例に過ぎません。 このサンプルでは、ハードコーディングされた値があります。 生産シナリオでは、値は代わりにデータベースから読み取られる必要があります。

## <a name="customization-approach"></a>カスタマイズ方法
このカスタマイズを 2 つの手順で実装します。 手順 1 では、ロイヤルティ ポイントがトランザクションに使用されなかったかのようにポイントを獲得します。 次に、ステップ 2 で獲得された余分なポイントは、償還されたポイントに基づいて減額されます。

ロイヤリティ機能には 6 つのサービス リクエストがあります。

+ GetLoyaltyCardStatusServiceRequest
+ CalculateLoyaltyRewardPointsServiceRequest
+ IssueLoyaltyCardServiceRequest
+ FillInLoyaltyRewardPointLinesForSalesServiceRequest
+ FillInLoyaltyRewardPointLinesForReturnServiceRequest
+ FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest

キャッシュ・アンド・キャリー取引の特典ポイントを計算するために、システムは販売取引行に対して  **FillInLoyaltyRewardPointLinesForSalesServiceRequest** を使用します。 この要求は、**FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** を使用して実際の報酬計算を行います。 同様に、システムは返品トランザクション ラインに **FillInLoyaltyRewardPointLinesForReturnServiceRequest** を使用し、この要求は **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** も使用して実際の報酬計算を行います。 ロイヤルティ機能の最初から用意されている実装内容では、顧客は同じトランザクションでロイヤルティ ポイントの引き換えと獲得を両方できません。 つまり、販売トランザクションに、ロイヤルティ カードの支払/入金明細行がある場合、**FillInLoyaltyRewardPointLinesForSalesServiceRequest** は特典ポイントを計算するために、**FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** を呼び出しません。 

ロイヤルティ ポイントを同じ取引で引き換えて獲得するには、1 つのサービス要求 **FillInLoyaltyRewardPointLinesForSalesServiceRequest** を使用します。

### <a name="step-1"></a>ステップ１ 

シナリオでは、報酬ポイントを計算するため **FillInLoyaltyRewardPointLinesForEarnOrDeductServiceRequest** を常に呼び出すように、**FillInLoyaltyRewardPointLinesForSalesServiceRequest** を実装する必要があります ただし、この変更により、ロイヤルティ ポイントを使用して顧客が支払う金額に基づいて、余分に獲得したポイントを計算するシステムとなります。 したがって、獲得ポイントを適切な額だけ減らすことができなければなりません。 この調整は、ステップ 2 で行われます。

### <a name="step-2"></a>ステップ２

拡張性フレームワークが **FillInLoyaltyRewardPointLinesForSalesServiceRequest** で提供する事後トリガー メカニズムを活用します。 転記トリガーでは、獲得および引き換えのルールを使用して、引き換えた各報酬ポイントに対して獲得した余分なポイント数を決定します。 次に、これらの余分なポイントを差し引いて、正確な金額を取得します。

#### <a name="implement-fillinloyaltyrewardpointlinesforsalesservicerequest"></a>FillInLoyaltyRewardPointLinesForSalesServiceRequest の実装 

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

#### <a name="implement-the-post-trigger-for-fillinloyaltyrewardpointlinesforsalesservicerequest"></a>FillInLoyaltyRewardPointLinesForSalesServiceRequest の転記トリガーの実装

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
