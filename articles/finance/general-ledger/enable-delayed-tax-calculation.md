---
title: 仕訳帳の税金計算遅延の有効化
description: このトピックでは、仕訳帳明細行の数が非常に大きい場合に、税金計算遅延の機能をオンにして、税額計算のパフォーマンスを向上させる方法について説明します。
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 4ea79747e8e7c078baa6e270ecebf88c4832e079
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968807"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="e3e9e-103">仕訳帳の税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="e3e9e-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="e3e9e-104">このトピックでは、仕訳帳の消費税計算を遅らせる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="e3e9e-105">この機能により、多数の仕訳帳明細行がある場合に、税額計算のパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="e3e9e-106">既定では、仕訳帳明細行の消費税金額は、税金に関連するフィールドが更新されるたびに計算されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="e3e9e-107">これらのフィールドには、消費税グループと品目消費税グループのフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="e3e9e-108">仕訳帳明細行を更新すると、すべての仕訳帳明細行の税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="e3e9e-109">この動作は、ユーザーに対してリアルタイムで計算された税額を表示しますが、仕訳帳明細行の数が非常に大きい場合はパフォーマンスにも影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="e3e9e-110">税金計算遅延の機能を使用すると、仕訳帳の税額計算を遅らせるため、パフォーマンス問題を修正できます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="e3e9e-111">この機能が有効になっている場合、**消費税** を選択するか、仕訳帳を転記するときにのみ、税額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="e3e9e-112">消費税の計算は、次の 3 つのレベルで遅らせることができます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="e3e9e-113">法人エンティティ</span><span class="sxs-lookup"><span data-stu-id="e3e9e-113">Legal entity</span></span>
- <span data-ttu-id="e3e9e-114">仕訳帳名</span><span class="sxs-lookup"><span data-stu-id="e3e9e-114">Journal name</span></span>
- <span data-ttu-id="e3e9e-115">仕訳帳ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e3e9e-115">Journal header</span></span>

<span data-ttu-id="e3e9e-116">システムによって、仕訳帳ヘッダーの設定が優先されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="e3e9e-117">既定では、この設定は仕訳帳名から取得されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="e3e9e-118">既定では、仕訳帳名の設定は、仕訳帳名の作成時に **一般会計パラメーター** ページの設定から取得されます。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="e3e9e-119">次のセクションでは、法人、仕訳帳名、および仕訳帳ヘッダーの税金計算遅延を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="e3e9e-120">法人レベルでの税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="e3e9e-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="e3e9e-121">**一般会計 \> 元帳の設定 \> 一般会計パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="e3e9e-122">**消費税** タブの **全般** クイック タブで、**税金計算遅延** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![一般会計パラメーターの画像](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="e3e9e-124">仕訳帳名レベルでの税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="e3e9e-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="e3e9e-125">**一般会計 \> 仕訳帳の設定 \> 仕訳帳名** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="e3e9e-126">**消費税** セクションの **全般** クイック タブで、**税金計算遅延** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![仕訳帳名の画像](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="e3e9e-128">仕訳帳ヘッダー レベルでの税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="e3e9e-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="e3e9e-129">**一般会計 \> 仕訳入力 \> 一般仕訳帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="e3e9e-130">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-130">Select **New**.</span></span>
3. <span data-ttu-id="e3e9e-131">仕訳帳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-131">Select a journal name.</span></span>
4. <span data-ttu-id="e3e9e-132">**設定** タブで、**税金計算遅延** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e3e9e-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![一般仕訳帳ページの画像](media/delayed-tax-calculation-journal-header.png)
