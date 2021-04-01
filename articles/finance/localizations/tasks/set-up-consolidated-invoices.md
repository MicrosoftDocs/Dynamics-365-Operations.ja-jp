---
title: 月次締め請求書の設定
description: 日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, PaymDay, PaymTerm
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c59e4df4552c139731dd93dacb20bd7a47326af
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256584"
---
# <a name="set-up-consolidated-invoices"></a><span data-ttu-id="dce89-103">月次締め請求書の設定</span><span class="sxs-lookup"><span data-stu-id="dce89-103">Set up consolidated invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dce89-104">日本では、日本の商習慣に合わせて月次締め請求書を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="dce89-104">In Japan, consolidated invoices can be enabled to fit the Japanese business practices.</span></span>



<span data-ttu-id="dce89-105">この手順では、月次締め請求書の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="dce89-105">This procedure walks you through setting up consolidated invoice functionality.</span></span>



<span data-ttu-id="dce89-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="dce89-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="configure-accounts-receivable-parameters-for-consolidated-invoices"></a><span data-ttu-id="dce89-107">月次締め請求書に対する [売掛金勘定パラメーター] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dce89-107">Configure Accounts receivable parameters for consolidated invoices</span></span>
1. <span data-ttu-id="dce89-108">[売掛金勘定] > [設定] > [売掛金勘定パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="dce89-108">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="dce89-109">[顧客] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="dce89-109">Expand the Customer section.</span></span>
    * <span data-ttu-id="dce89-110">[顧客の月次締め請求書] の有効化</span><span class="sxs-lookup"><span data-stu-id="dce89-110">Enable Consolidated invoice for customers</span></span>  
3. <span data-ttu-id="dce89-111">[番号順序] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce89-111">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="dce89-112">締め ID に使用される番号順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="dce89-112">Specify the number sequence to use for the Consolidation ID.</span></span>  

## <a name="configure-payment-days"></a><span data-ttu-id="dce89-113">[支払期日] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dce89-113">Configure Payment days</span></span>
1. <span data-ttu-id="dce89-114">[売掛金勘定] > [支払設定] > [支払期日] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dce89-114">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="dce89-115">支払期日のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dce89-115">Configure a Payment day</span></span>  

## <a name="configure-terms-of-payment"></a><span data-ttu-id="dce89-116">[支払条件] のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dce89-116">Configure Terms of payment</span></span>
1. <span data-ttu-id="dce89-117">[売掛金勘定] > [支払設定] > [支払条件] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dce89-117">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
2. <span data-ttu-id="dce89-118">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="dce89-118">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dce89-119">たとえば、[支払い条件] フィールドで「代金引換払い」という値を指定してフィルターを実行します。</span><span class="sxs-lookup"><span data-stu-id="dce89-119">For example, filter on the Terms of payment field with a value of 'COD'.</span></span>
3. <span data-ttu-id="dce89-120">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce89-120">Click Edit.</span></span>
    * <span data-ttu-id="dce89-121">[支払方法] として [締日] を選択</span><span class="sxs-lookup"><span data-stu-id="dce89-121">Select Cutoff day as the Payment Method</span></span>  
    * <span data-ttu-id="dce89-122">[締日] は R1 リリースでは表示されません。</span><span class="sxs-lookup"><span data-stu-id="dce89-122">The Cutoff day is not available at R1 release.</span></span> <span data-ttu-id="dce89-123">代わりに [当月] を選択できます。</span><span class="sxs-lookup"><span data-stu-id="dce89-123">You can choose Current month as an alternative.</span></span> <span data-ttu-id="dce89-124">この結果、手動での調整を必要とするわずかな差が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="dce89-124">This may result in slight difference, which needs to adjusted manually.</span></span>  
4. <span data-ttu-id="dce89-125">[支払期日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="dce89-125">In the Payment day field, type a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]