--- 
title: "月次締め請求書のパラメーターのコンフィギュレーションと買掛金勘定の設定 (日本)"
description: "日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。"
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
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
ms.sourcegitcommit: 66f10523fe3fb104550a88f735a9644613ec861b
ms.openlocfilehash: 23f312f2ad075b773c334c0d8c807ec0f6577a28
ms.contentlocale: ja-jp
ms.lasthandoff: 10/30/2017

---
# <a name="configure-consolidated-invoice-parameters-and-setup-for-accounts-payable-japan"></a><span data-ttu-id="bef29-103">月次締め請求書のパラメーターのコンフィギュレーションと買掛金勘定の設定 (日本)</span><span class="sxs-lookup"><span data-stu-id="bef29-103">Configure consolidated invoice parameters and setup for accounts payable (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bef29-104">日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="bef29-104">In Japan, consolidated invoices can be enabled to fit the Japanese business practices.</span></span>



<span data-ttu-id="bef29-105">この手順では、月次締め請求書の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="bef29-105">This procedure walks you through setting up consolidated invoice functionality.</span></span>



<span data-ttu-id="bef29-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="bef29-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="configure-accounts-payable-parameters-for-consolidated-invoices"></a><span data-ttu-id="bef29-107">月次締め請求書に対する [買掛金勘定パラメーター] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bef29-107">Configure Accounts payable parameters for consolidated invoices</span></span>
1. <span data-ttu-id="bef29-108">[買掛金勘定] > [設定] > [買掛金勘定パラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bef29-108">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="bef29-109">[仕入先] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="bef29-109">Expand the Vendor section.</span></span>
3. <span data-ttu-id="bef29-110">[仕入先に対する月次締め請求書] チェック ボックスをチェックします。</span><span class="sxs-lookup"><span data-stu-id="bef29-110">Check the Consolidated invoice for vendor check box.</span></span>
4. <span data-ttu-id="bef29-111">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bef29-111">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="bef29-112">締め ID に使用される番号順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="bef29-112">Specify the number sequence to use for the Consolidation ID.</span></span>  

## <a name="configure-payment-days"></a><span data-ttu-id="bef29-113">[支払期日] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bef29-113">Configure Payment days</span></span>
1. <span data-ttu-id="bef29-114">[買掛金勘定] > [支払の設定] > [支払期日] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bef29-114">Go to Accounts payable > Payment setup > Payment days.</span></span>
    * <span data-ttu-id="bef29-115">支払期日のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bef29-115">Configure a Payment day</span></span>  

## <a name="configure-terms-of-payment"></a><span data-ttu-id="bef29-116">[支払条件] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bef29-116">Configure Terms of payment</span></span>
1. <span data-ttu-id="bef29-117">[買掛金勘定] > [支払設定] > [支払条件] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bef29-117">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="bef29-118">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="bef29-118">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bef29-119">たとえば、[支払い条件] フィールドで「代金引換払い」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="bef29-119">For example, filter on the Terms of payment field with a value of 'COD'.</span></span>
3. <span data-ttu-id="bef29-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bef29-120">Click Edit.</span></span>
    * <span data-ttu-id="bef29-121">[支払方法] として [締日] を選択</span><span class="sxs-lookup"><span data-stu-id="bef29-121">Select Cutoff day as the Payment Method</span></span>  
    * <span data-ttu-id="bef29-122">[締日] は R1 リリースでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="bef29-122">The Cutoff day is not available at R1 release.</span></span> <span data-ttu-id="bef29-123">代わりに [当月] を選択できます。</span><span class="sxs-lookup"><span data-stu-id="bef29-123">You can choose Current month as an alternative.</span></span> <span data-ttu-id="bef29-124">この結果、手動での調整を必要とするわずかな差が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bef29-124">This may result in slight difference, which needs to be adjusted manually.</span></span>   
4. <span data-ttu-id="bef29-125">[支払期日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="bef29-125">In the Payment day field, type a value.</span></span>


