---
title: 仕訳帳の税金計算遅延の有効化
description: このトピックでは、仕訳帳明細行の量が膨大な場合に、**仕訳帳の税金計算遅延の有効化**機能を使用して、税額計算のパフォーマンスを向上させる方法について説明します。
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
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178619"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="60655-103">仕訳帳の税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="60655-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="60655-104">このトピックでは、仕訳帳明細行の量が膨大な場合に、**仕訳帳の税金計算遅延の有効化**機能を使用して、税額計算のパフォーマンスを向上させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="60655-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="60655-105">仕訳帳の現在の売上税計算の動作は、ユーザーが売上税グループ/品目売上税グループなどの税関連フィールドを更新したときにリアルタイムで発生します。</span><span class="sxs-lookup"><span data-stu-id="60655-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="60655-106">仕訳帳明細行レベルで更新すると、すべての仕訳帳明細行の税額が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="60655-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="60655-107">この方法では、ユーザーはリアルタイムに計算された税額を確認できますが、仕訳帳明細行の量が膨大な場合はパフォーマンスの問題が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="60655-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="60655-108">この機能は、パフォーマンスの問題を解決するために税金計算を遅延させるオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="60655-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="60655-109">この機能が有効になっている場合、ユーザーが "売上税" コマンドをクリックするか、仕訳帳を転記するときにのみ、税額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="60655-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="60655-110">ユーザーは、次の 3 つのレベルでパラメーターをオンまたはオフにできます。</span><span class="sxs-lookup"><span data-stu-id="60655-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="60655-111">法人ごと</span><span class="sxs-lookup"><span data-stu-id="60655-111">By legal entity</span></span>
- <span data-ttu-id="60655-112">仕訳帳名ごと</span><span class="sxs-lookup"><span data-stu-id="60655-112">By journal name</span></span>
- <span data-ttu-id="60655-113">仕訳帳ヘッダーごと</span><span class="sxs-lookup"><span data-stu-id="60655-113">By journal header</span></span>

<span data-ttu-id="60655-114">システムは、仕訳帳ヘッダーのパラメーター値を最終値として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="60655-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="60655-115">仕訳帳ヘッダーのパラメーター値は、既定で仕訳帳名から取得されます。</span><span class="sxs-lookup"><span data-stu-id="60655-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="60655-116">仕訳帳名のパラメーター値は、仕訳帳名の作成時に総勘定元帳パラメーターの既定値になります。</span><span class="sxs-lookup"><span data-stu-id="60655-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="60655-117">このパラメーターをオンにすると、仕訳帳の "実際の売上税額" フィールドと "計算済売上税額" のフィールドが除外されます。</span><span class="sxs-lookup"><span data-stu-id="60655-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="60655-118">そうすることにより、ユーザーが税計算を開始する前にこれら 2 つのフィールドの値は常に 0 を示すことになり、ユーザーを混乱させません。</span><span class="sxs-lookup"><span data-stu-id="60655-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="60655-119">法人ごとの税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="60655-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="60655-120">**総勘定元帳 > 元帳の設定 > 総勘定元帳のパラメーター**の順に移動する</span><span class="sxs-lookup"><span data-stu-id="60655-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="60655-121">**売上税**タブをクリックする</span><span class="sxs-lookup"><span data-stu-id="60655-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="60655-122">**一般**クイック タブで、パラメーター**税金計算の遅延**を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="60655-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="60655-123">仕訳帳ごとの税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="60655-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="60655-124">**総勘定元帳 > 仕訳帳の設定 > 仕訳帳名**に移動する</span><span class="sxs-lookup"><span data-stu-id="60655-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="60655-125">**一般**クイック タブで、パラメーター**税金計算の遅延**を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="60655-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="60655-126">仕訳帳ごとの税金計算遅延の有効化</span><span class="sxs-lookup"><span data-stu-id="60655-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="60655-127">**総勘定元帳 > 仕訳入力 > 一般仕訳帳**の順に移動する</span><span class="sxs-lookup"><span data-stu-id="60655-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="60655-128">**新規**をクリックする</span><span class="sxs-lookup"><span data-stu-id="60655-128">Click **New**</span></span>
3. <span data-ttu-id="60655-129">仕訳帳名を選択する</span><span class="sxs-lookup"><span data-stu-id="60655-129">Select a journal name</span></span>
4. <span data-ttu-id="60655-130">**設定**をクリックする</span><span class="sxs-lookup"><span data-stu-id="60655-130">Click **Setup**</span></span>
5. <span data-ttu-id="60655-131">パラメーター**税金計算の遅延**を有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="60655-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
