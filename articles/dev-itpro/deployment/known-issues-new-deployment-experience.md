---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: sarvanisathish
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 2afbf09176274777db9f63fcf6eaf9262c3faced
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368616"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="1551e-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="1551e-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="1551e-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="1551e-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="1551e-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="1551e-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="1551e-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="1551e-106">Features not intended to be implemented</span></span>
<span data-ttu-id="1551e-107">次の LCS 機能は廃止されており、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="1551e-107">The following LCS features are deprecated and will not be implemented in self-service deployment.</span></span>

| <span data-ttu-id="1551e-108">**機能**</span><span class="sxs-lookup"><span data-stu-id="1551e-108">**Feature**</span></span>        | <span data-ttu-id="1551e-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="1551e-109">**Description**</span></span>   |
|--------------------|--------|
| <span data-ttu-id="1551e-110">システム診断</span><span class="sxs-lookup"><span data-stu-id="1551e-110">System diagnostics</span></span> | <span data-ttu-id="1551e-111">システム診断は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="1551e-111">System diagnostics has been deprecated.</span></span> <span data-ttu-id="1551e-112">現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="1551e-112">All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> |
| <span data-ttu-id="1551e-113">サービス要求</span><span class="sxs-lookup"><span data-stu-id="1551e-113">Service requests</span></span>   | <span data-ttu-id="1551e-114">サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="1551e-114">Service requests are being replaced with self-service actions.</span></span> |

### <a name="known-issues-in-this-release"></a><span data-ttu-id="1551e-115">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="1551e-115">Known issues in this release</span></span>
<span data-ttu-id="1551e-116">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="1551e-116">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="1551e-117">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="1551e-117">Every 2 weeks there is a new release of LCS.</span></span>

-   <span data-ttu-id="1551e-118">配置エラーを一覧表示するログ ファイルは、まだ LCS を通じて使用できません。</span><span class="sxs-lookup"><span data-stu-id="1551e-118">Log files listing deployment failures are not yet available through LCS.</span></span> <span data-ttu-id="1551e-119">現時点では、ログ ファイルが必要な場合は、サポート チケットを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="1551e-119">Currently, you can open a support ticket if you need the log files.</span></span>

-   <span data-ttu-id="1551e-120">Finance and Operations 環境からの LCS 統合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="1551e-120">LCS integration from a Finance and Operations environment does not work.</span></span> <span data-ttu-id="1551e-121">この結果使用できない機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1551e-121">The features that are not available as a result of this include:</span></span>

    -   <span data-ttu-id="1551e-122">はじめに</span><span class="sxs-lookup"><span data-stu-id="1551e-122">Getting started</span></span>

    -   <span data-ttu-id="1551e-123">BPM ライブラリを通じて有効なオンライン ヘルプ。</span><span class="sxs-lookup"><span data-stu-id="1551e-123">Online Help enabled through BPM libraries.</span></span> <span data-ttu-id="1551e-124">docs.microsoft.com のオンライン ヘルプは使用できます。</span><span class="sxs-lookup"><span data-stu-id="1551e-124">Online Help from docs.microsoft.com is available.</span></span>

    -   <span data-ttu-id="1551e-125">Finance and Operations 内からサポート チケットを生成します。</span><span class="sxs-lookup"><span data-stu-id="1551e-125">Raising support tickets from within Finance and Operations.</span></span> <span data-ttu-id="1551e-126">LCS からのクラウドを利用したサポートが有効です。</span><span class="sxs-lookup"><span data-stu-id="1551e-126">Cloud-powered support from LCS is enabled.</span></span>

## <a name="finance-and-operations"></a><span data-ttu-id="1551e-127">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1551e-127">Finance and Operations</span></span> 

### <a name="features-not-yet-implemented"></a><span data-ttu-id="1551e-128">まだ実装されていない機能</span><span class="sxs-lookup"><span data-stu-id="1551e-128">Features not yet implemented</span></span>

<span data-ttu-id="1551e-129">インフラストラクチャの依存関係がある次の機能は、最新の配置エクスペリエンスにはまだ実装されていません。</span><span class="sxs-lookup"><span data-stu-id="1551e-129">The following features that have infrastructure dependencies are not yet implemented in the modern deployment experience.</span></span> <span data-ttu-id="1551e-130">これらの機能は推奨されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="1551e-130">These features have not been deprecated.</span></span>

| <span data-ttu-id="1551e-131">**機能**</span><span class="sxs-lookup"><span data-stu-id="1551e-131">**Feature**</span></span>                 | <span data-ttu-id="1551e-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="1551e-132">**Description**</span></span>                                           |
|-----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1551e-133">小売</span><span class="sxs-lookup"><span data-stu-id="1551e-133">Retail</span></span>                      | <span data-ttu-id="1551e-134">Retail のサポートがまだ有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="1551e-134">Retail support is not yet enabled.</span></span>                        |
| <span data-ttu-id="1551e-135">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="1551e-135">Trace Parser</span></span>                | <span data-ttu-id="1551e-136">実績ツールはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1551e-136">Perf tools are not yet supported.</span></span>                         |
| <span data-ttu-id="1551e-137">レポート: 画面に出力</span><span class="sxs-lookup"><span data-stu-id="1551e-137">Reporting – Print to Screen</span></span> | <span data-ttu-id="1551e-138">PDF への出力のみこの時点でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1551e-138">Only print to PDF is supported at this time.</span></span>              |
| <span data-ttu-id="1551e-139">Word にエクスポート</span><span class="sxs-lookup"><span data-stu-id="1551e-139">Export to Word</span></span>              | <span data-ttu-id="1551e-140">この時点で、Word へのエクスポート機能は有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="1551e-140">Export to Word functionality is not enabled at this time.</span></span> |

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="1551e-141">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="1551e-141">Features not intended to be implemented</span></span>
<span data-ttu-id="1551e-142">次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。</span><span class="sxs-lookup"><span data-stu-id="1551e-142">The following features are deprecated and will not be implemented in the modern deployment experience.</span></span>

| <span data-ttu-id="1551e-143">**機能**</span><span class="sxs-lookup"><span data-stu-id="1551e-143">**Feature**</span></span>  | <span data-ttu-id="1551e-144">**説明**</span><span class="sxs-lookup"><span data-stu-id="1551e-144">**Description**</span></span>                     |
|--------------|-------------------------------------|
| <span data-ttu-id="1551e-145">カスタム フォント</span><span class="sxs-lookup"><span data-stu-id="1551e-145">Custom fonts</span></span> | <span data-ttu-id="1551e-146">カスタム フォントはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="1551e-146">Custom fonts will not be supported.</span></span> |

### <a name="known-issues-in-this-release"></a><span data-ttu-id="1551e-147">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="1551e-147">Known issues in this release</span></span>
<span data-ttu-id="1551e-148">既知の問題は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1551e-148">Known issues are listed below.</span></span> <span data-ttu-id="1551e-149">これらは、アクティブにの作業されているバグです。</span><span class="sxs-lookup"><span data-stu-id="1551e-149">These are bugs that are being worked on actively.</span></span> <span data-ttu-id="1551e-150">修正プログラムは将来のリリースで提供されます。</span><span class="sxs-lookup"><span data-stu-id="1551e-150">Hotfixes will be provided in future releases.</span></span>

#### <a name="financial-reporting"></a><span data-ttu-id="1551e-151">財務報告</span><span class="sxs-lookup"><span data-stu-id="1551e-151">Financial reporting</span></span>

-   <span data-ttu-id="1551e-152">**既定のレポートは既定ではインポートされない:** 既定のレポートをインポートするには、以下を行います。</span><span class="sxs-lookup"><span data-stu-id="1551e-152">**Default reports are not imported by default:** To import the default reports, do the following:</span></span>

    1.  <span data-ttu-id="1551e-153">**総勘定元帳 \> 照会およびレポート\> 財務諸表** に移動して、レポート デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="1551e-153">Launch Report designer by going to **General Ledger \> Inquiries and reports \> Financial reports.**</span></span>
    2.  <span data-ttu-id="1551e-154">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1551e-154">Click **New**.</span></span>
    3.  <span data-ttu-id="1551e-155">**ツール \> 既定のレポートのインポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1551e-155">Go to **Tools \> Import Default Reports**.</span></span> 
    4.  <span data-ttu-id="1551e-156">レポートは、数分後に Web クライアントに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="1551e-156">Reports will load into the web client after a few minutes.</span></span>

-   <span data-ttu-id="1551e-157">**PDF に出力は、代わりに XPS に出力されます** (印刷ドライバーへのアクセスの問題のため)。</span><span class="sxs-lookup"><span data-stu-id="1551e-157">**Print to PDF is printing to XPS instead** (due to a print driver access issue).</span></span>
