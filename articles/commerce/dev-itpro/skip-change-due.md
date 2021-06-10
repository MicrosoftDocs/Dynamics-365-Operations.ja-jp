---
title: POS の「お釣りの支払い」ダイアログ ボックスをスキップする
description: このトピックでは、トランザクションが完全に支払われていてお釣りが必要ない場合に、販売時点管理 (POS) で「お釣りの支払い」ダイアログ ボックスをスキップする方法について説明します。
author: rubendel
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 9d66937f2b2d13c9473bfb31db39d36bb5944bde
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022095"
---
# <a name="skip-change-due-dialog-box-in-pos"></a><span data-ttu-id="bad00-103">POS の「お釣りの支払い」ダイアログ ボックスをスキップする</span><span class="sxs-lookup"><span data-stu-id="bad00-103">Skip "change due" dialog box in POS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bad00-104">このトピックでは、トランザクションが完全に支払われていてお釣りを支払う必要がない場合に、販売時点管理 (POS) で **お釣りの支払い** ダイアログ ボックスをスキップする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bad00-104">This topic describes how to skip the **Change due** dialog box in the point of sale (POS) when a transaction is paid in full and there's no change due.</span></span>

<span data-ttu-id="bad00-105">POS での支払いでは、クレジットの使用率が高まっているため、ほとんどのトランザクションで顧客にお釣りを支払う必要がなくなっています。</span><span class="sxs-lookup"><span data-stu-id="bad00-105">For payments at the POS, there is now a greater prevalence of credit usage, as most transactions don't require change to be provided to the customer.</span></span> <span data-ttu-id="bad00-106">Dynamics 365 Commerce では、実際に顧客に対してお釣りを支払う必要がない限り、**お釣りの支払い** ダイアログをスキップするように POS を構成できます。</span><span class="sxs-lookup"><span data-stu-id="bad00-106">In Dynamics 365 Commerce, you can configure POS so that the  **Change due** dialog is skipped unless there's actually change due back to the customer.</span></span> <span data-ttu-id="bad00-107">**お釣りの支払い** ダイアログ ボックスは、ギフト レシートのレシート形式が、**必要時** に印刷するように構成されている場合にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="bad00-107">The **Change due** dialog box will also be shown if the receipt format for gift receipts is configured to print **As required**.</span></span> <span data-ttu-id="bad00-108">ギフト レシートが **必要時** に印刷するように構成されている場合 は、ギフト レシートを印刷するためのオプションが **お釣りの支払い** ダイアログ ボックスに含まれ、**お釣りの支払いをスキップ** の構成が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="bad00-108">When gift receipts are configured to print **As required**, the option to print a gift receipt is included in the **Change due** dialog box, overriding the **Skip change due** configuration.</span></span>

## <a name="configure-property-to-skip-change-due-dialog-box"></a><span data-ttu-id="bad00-109">プロパティを構成して **お釣りの支払い** ダイアログ ボックスをスキップする</span><span class="sxs-lookup"><span data-stu-id="bad00-109">Configure property to skip **Change due** dialog box</span></span>

<span data-ttu-id="bad00-110">**お釣りの支払い** ダイアログ ボックスをスキップするように構成するプロパティは、店舗レベルの設定の **機能プロファイル** レベルにあります。</span><span class="sxs-lookup"><span data-stu-id="bad00-110">The property you need to configure to skip the **Change due** dialog box is found in the **Functionality profile** level, which is a store-level setting.</span></span> 

<span data-ttu-id="bad00-111">プロパティを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="bad00-111">To configure the property, follow these steps.</span></span>

1. <span data-ttu-id="bad00-112">ダイアログ ボックスをスキップする店舗の **機能プロファイル** を検索します。</span><span class="sxs-lookup"><span data-stu-id="bad00-112">Search for the **Functionality profile** for the store where the dialog box should be skipped.</span></span>
1. <span data-ttu-id="bad00-113">目的の店舗の機能プロファイルを開き、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bad00-113">Open the functionality profile for the target store and select **Edit**.</span></span> 
1. <span data-ttu-id="bad00-114">**機能** クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="bad00-114">Expand the **Functions** FastTab.</span></span> <span data-ttu-id="bad00-115">**端末** 小見出しの下の、**お釣りの支払い** フィールドで、**ゼロのときにスキップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bad00-115">Under the **Terminal** subheading, in the **Change due** field, select **Skip when zero**.</span></span> 
1. <span data-ttu-id="bad00-116">**保存** を選択してから、**1070** チャネル構成配布スケジュールを実行します。</span><span class="sxs-lookup"><span data-stu-id="bad00-116">Select **Save**, and then run the **1070** channel configuration distribution schedule.</span></span>
1. <span data-ttu-id="bad00-117">変更が同期されたら、POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="bad00-117">After the changes are synchronized, sign out of the POS and then sign back in.</span></span> <span data-ttu-id="bad00-118">**お釣りの支払い** ダイアログ ボックスが表示されないことを確認するために、顧客にお釣りを支払う必要のないトランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="bad00-118">Make a transaction that has no change due to the customer to verify that the **Change due** dialog box isn't displayed.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="bad00-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bad00-119">Additional resources</span></span>

[<span data-ttu-id="bad00-120">支払方法</span><span class="sxs-lookup"><span data-stu-id="bad00-120">Payment methods</span></span>](../payment-methods.md)

[<span data-ttu-id="bad00-121">クレジット カードの設定、認証、および取得</span><span class="sxs-lookup"><span data-stu-id="bad00-121">Credit card setup, authorization, and capture</span></span>](../../finance/accounts-receivable/credit-card-authorizations.md)

[<span data-ttu-id="bad00-122">販売時点管理 (POS) 用の現金貨幣単位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bad00-122">Configure cash denominations for the point of sale (POS)</span></span>](../cash-denominations.md)

[<span data-ttu-id="bad00-123">クレジット カード処理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bad00-123">Configure credit card processing</span></span>](../tasks/configure-credit-card-processing.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]