--- 
title: "月次締め請求書の設定 (日本)"
description: "日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 858cbf5f5beee4c02ebbb670f35386d26a0883f4
ms.openlocfilehash: 4858c2dd5f78d68546cb0c958cdb5ac9847fd4e3
ms.contentlocale: ja-jp
ms.lasthandoff: 10/31/2017

---
# <a name="set-up-consolidated-invoices-japan"></a><span data-ttu-id="7f2f1-103">月次締め請求書の設定 (日本)</span><span class="sxs-lookup"><span data-stu-id="7f2f1-103">Set up consolidated invoices (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f2f1-104">日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-104">In Japan, consolidated invoices can be enabled to fit the Japanese business practices.</span></span>



<span data-ttu-id="7f2f1-105">この手順では、月次締め請求書の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-105">This procedure walks you through setting up consolidated invoice functionality.</span></span>



<span data-ttu-id="7f2f1-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="configure-accounts-receivable-parameters-for-consolidated-invoices"></a><span data-ttu-id="7f2f1-107">月次締め請求書に対する [売掛金勘定パラメーター] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f2f1-107">Configure Accounts receivable parameters for consolidated invoices</span></span>
1. <span data-ttu-id="7f2f1-108">[売掛金勘定] > [設定] > [売掛金勘定パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-108">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="7f2f1-109">[顧客] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-109">Expand the Customer section.</span></span>
    * <span data-ttu-id="7f2f1-110">[顧客の月次締め請求書] の有効化</span><span class="sxs-lookup"><span data-stu-id="7f2f1-110">Enable Consolidated invoice for customers</span></span>  
3. <span data-ttu-id="7f2f1-111">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-111">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="7f2f1-112">締め ID に使用される番号順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-112">Specify the number sequence to use for the Consolidation ID.</span></span>  

## <a name="configure-payment-days"></a><span data-ttu-id="7f2f1-113">[支払期日] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f2f1-113">Configure Payment days</span></span>
1. <span data-ttu-id="7f2f1-114">[売掛金勘定] > [支払設定] > [支払期日] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-114">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="7f2f1-115">支払期日のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f2f1-115">Configure a Payment day</span></span>  

## <a name="configure-terms-of-payment"></a><span data-ttu-id="7f2f1-116">[支払条件] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="7f2f1-116">Configure Terms of payment</span></span>
1. <span data-ttu-id="7f2f1-117">[売掛金勘定] > [支払設定] > [支払条件] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-117">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
2. <span data-ttu-id="7f2f1-118">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-118">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7f2f1-119">たとえば、[支払い条件] フィールドで「代金引換払い」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-119">For example, filter on the Terms of payment field with a value of 'COD'.</span></span>
3. <span data-ttu-id="7f2f1-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-120">Click Edit.</span></span>
    * <span data-ttu-id="7f2f1-121">[支払方法] として [締日] を選択</span><span class="sxs-lookup"><span data-stu-id="7f2f1-121">Select Cutoff day as the Payment Method</span></span>  
    * <span data-ttu-id="7f2f1-122">[締日] は R1 リリースでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-122">The Cutoff day is not available at R1 release.</span></span> <span data-ttu-id="7f2f1-123">代わりに [当月] を選択できます。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-123">You can choose Current month as an alternative.</span></span> <span data-ttu-id="7f2f1-124">この結果、手動での調整を必要とするわずかな差が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-124">This may result in slight difference, which needs to be adjusted manually.</span></span>  
4. <span data-ttu-id="7f2f1-125">[支払期日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7f2f1-125">In the Payment day field, type a value.</span></span>


