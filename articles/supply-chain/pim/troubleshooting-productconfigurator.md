---
title: 製品コンフィギュレーターのトラブルシューティング
description: このトピックでは、製品コンフィギュレーターを操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e6cfeb6a2b4166dfa9a5a5cc1b7d3d913b865ce2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999609"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="99952-103">製品コンフィギュレーターのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="99952-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="99952-104">このトピックでは、製品コンフィギュレーターを操作する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="99952-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="99952-105">販売注文明細行で製品を構成すると、品目テキストが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="99952-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="99952-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="99952-106">Issue description</span></span>

<span data-ttu-id="99952-107">この問題は、構成可能品目の販売注文明細行を作成し、品目テキストを変更した場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="99952-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="99952-108">品目を構成してから **OK** をクリックすると、テキストは標準テキストで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="99952-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="99952-109">問題の解決</span><span class="sxs-lookup"><span data-stu-id="99952-109">Issue resolution</span></span>

<span data-ttu-id="99952-110">この動作は予期されています。</span><span class="sxs-lookup"><span data-stu-id="99952-110">This behavior is expected.</span></span> <span data-ttu-id="99952-111">テキスト フィールドには、バリアント名が含まれており、行を構成した後にのみ入力されます。</span><span class="sxs-lookup"><span data-stu-id="99952-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="99952-112">したがって、行を構成した後でなくても、テキストを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99952-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="99952-113">製品構成モデルが計算されると、整数属性が誤って丸められます。</span><span class="sxs-lookup"><span data-stu-id="99952-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="99952-114">問題の説明</span><span class="sxs-lookup"><span data-stu-id="99952-114">Issue description</span></span>

<span data-ttu-id="99952-115">この問題は、次の一連のアクションを実行した場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="99952-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="99952-116">生産構成モデルで次の属性を設定します。</span><span class="sxs-lookup"><span data-stu-id="99952-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="99952-117">入力 (整数)</span><span class="sxs-lookup"><span data-stu-id="99952-117">Input (integer)</span></span>
    - <span data-ttu-id="99952-118">パーセント(10 進数)</span><span class="sxs-lookup"><span data-stu-id="99952-118">Percent (decimal)</span></span>
    - <span data-ttu-id="99952-119">結果 (整数)</span><span class="sxs-lookup"><span data-stu-id="99952-119">Result (integer)</span></span>

2. <span data-ttu-id="99952-120">以下の式を持つ計算を作成します。</span><span class="sxs-lookup"><span data-stu-id="99952-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="99952-121">*結果* = *入力* × *パーセント* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="99952-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="99952-122">この場合、整数の結果は常に正しく丸められるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="99952-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="99952-123">たとえば、入力が 1000 で、パーセントが 2.40 であるとします。</span><span class="sxs-lookup"><span data-stu-id="99952-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="99952-124">したがって、1000 の 2.40 パーセントが 24 (10 進数では 24.00) であるため、整数の結果は 24 であると想定されます。</span><span class="sxs-lookup"><span data-stu-id="99952-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="99952-125">代わりに、23 という結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="99952-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="99952-126">しかし、パーセントが 2.39 の場合、計算は 23 ではなく 24 に丸められます。</span><span class="sxs-lookup"><span data-stu-id="99952-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="99952-127">パーセントが 2.50 の場合、計算は予想どおり 25 に丸められます。</span><span class="sxs-lookup"><span data-stu-id="99952-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="99952-128">問題の解決</span><span class="sxs-lookup"><span data-stu-id="99952-128">Issue resolution</span></span>

<span data-ttu-id="99952-129">この問題は、Microsoft Solver Foundation の内部で端数を使用して数値を表す方法が原因で発生します。</span><span class="sxs-lookup"><span data-stu-id="99952-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="99952-130">前の例では、パーセントが 2.40 である計算の結果は、27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375 として表されます。</span><span class="sxs-lookup"><span data-stu-id="99952-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="99952-131">.NET がこの値を整数としてキャストする場合、23 を返します。</span><span class="sxs-lookup"><span data-stu-id="99952-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="99952-132">他のシナリオがこれに依存しているため、この動作は変更されません。</span><span class="sxs-lookup"><span data-stu-id="99952-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="99952-133">前の例では、追加の小数点属性と計算を導入することにより、この問題を修正できます。</span><span class="sxs-lookup"><span data-stu-id="99952-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="99952-134">たとえば、生産構成モデルで次の属性を設定できます。</span><span class="sxs-lookup"><span data-stu-id="99952-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="99952-135">入力 (整数)</span><span class="sxs-lookup"><span data-stu-id="99952-135">Input (integer)</span></span>
- <span data-ttu-id="99952-136">パーセント (10 進数)</span><span class="sxs-lookup"><span data-stu-id="99952-136">Percent (decimal)</span></span>
- <span data-ttu-id="99952-137">ResultDecimal (10 進数)</span><span class="sxs-lookup"><span data-stu-id="99952-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="99952-138">ResultInteger (整数)</span><span class="sxs-lookup"><span data-stu-id="99952-138">ResultInteger (integer)</span></span>

<span data-ttu-id="99952-139">この場合、次の計算を追加できます。</span><span class="sxs-lookup"><span data-stu-id="99952-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="99952-140">*ResultDecimal* = *入力* × *パーセント* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="99952-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="99952-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="99952-141">*ResultInteger* = *ResultDecimal*</span></span>
