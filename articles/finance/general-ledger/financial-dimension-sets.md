---
title: 財務分析コード セット
description: このトピックでは、財務分析コード セットについて説明し、その使用を最適化するためのヒントを提供します。
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021831"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="2fe5b-103">財務分析コード セット</span><span class="sxs-lookup"><span data-stu-id="2fe5b-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2fe5b-104">このトピックでは、財務分析コード セットについて説明し、その使用を最適化するためのヒントを提供します。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="2fe5b-105">分析コード セットは、一般会計データをユーザー定義の方法で集計するために使用できる財務分析コードの順序付きリストです。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="2fe5b-106">分析コード セットの主な用途は、試算表を定義することです。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="2fe5b-107">標準分析コード セットだけが、主勘定のみを含む分析コード セットになります。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="2fe5b-108">**財務分析コード セット** ページを使用して、財務分析コード セットの作成と管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="2fe5b-109">分析コード セットの残高</span><span class="sxs-lookup"><span data-stu-id="2fe5b-109">Dimension set balances</span></span>

<span data-ttu-id="2fe5b-110">分析コード セットには、財務分析コードに基づく残高があります。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="2fe5b-111">残高は、分析コード セットの定義に基づいて一般会計に存在します。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="2fe5b-112">残高は一般会計データから集計され、取得時のパフォーマンスを向上させることができます (試算表の生成時など)。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="2fe5b-113">残高の作成</span><span class="sxs-lookup"><span data-stu-id="2fe5b-113">Create balances</span></span>

<span data-ttu-id="2fe5b-114">**残高の作成** ボタンを使用して、現在残高が存在しない分析コード セットの残高を初期化します。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="2fe5b-115">残高の更新はすべての一般会計の転記活動に影響を与えるので、残高がある分析コード セットの数を制限することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="2fe5b-116">残高の更新</span><span class="sxs-lookup"><span data-stu-id="2fe5b-116">Update balances</span></span>

<span data-ttu-id="2fe5b-117">**残高の更新** ボタンを使用して、最新の一般会計の転記活動を残高に含めます。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="2fe5b-118">残高の更新は、軽い操作です。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-118">Balance updates are light operations.</span></span> <span data-ttu-id="2fe5b-119">最後の更新以降に発生した一般会計の転記活動のみを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="2fe5b-120">試算表の表示によって強制的に更新し、確実に現在の残高を表示します。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="2fe5b-121">定期バッチ ジョブの使用を検討すると、最も頻繁に使用する分析コード セットの更新を高速に行えます。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="2fe5b-122">このようにして、試算表のユーザーの待ち時間を最小限にすることができます。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="2fe5b-123">残高の再構築</span><span class="sxs-lookup"><span data-stu-id="2fe5b-123">Rebuild balances</span></span>

<span data-ttu-id="2fe5b-124">**残高の再構築** ボタンを使用して、最初から残高を再作成します。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="2fe5b-125">このようにして、確実に一般会計のデータと一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="2fe5b-126">残高の再構築には多くの処理が必要であり、通常は必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="2fe5b-127">定期的に残高の再構築が必要なシナリオがある場合は、カスタマー サポートに問い合わせることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="2fe5b-128">カスタマー サポートは、残高が一般会計のデータと一致しない理由を特定するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="2fe5b-129">残高のクリア</span><span class="sxs-lookup"><span data-stu-id="2fe5b-129">Clear balances</span></span>

<span data-ttu-id="2fe5b-130">**残高のクリア** ボタンを使用して残高を削除し、それ以上の更新を停止します。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="2fe5b-131">分析コード セットによる一般会計の転記活動への影響はなくなりました。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="2fe5b-132">詳細については、「[財務分析コード](financial-dimensions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2fe5b-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
