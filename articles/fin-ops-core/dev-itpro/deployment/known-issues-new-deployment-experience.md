---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: sarvanisathish
manager: AnnBe
ms.date: 09/18/2019
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
ms.openlocfilehash: f109c5d996aa31b1d71af85cdea7e8caa7e16edc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191584"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="9a252-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="9a252-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="9a252-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="9a252-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="9a252-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="9a252-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="9a252-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="9a252-106">Features not intended to be implemented</span></span>
<span data-ttu-id="9a252-107">次の LCS 機能は廃止されており、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="9a252-107">The following LCS features are deprecated and will not be implemented in self-service deployment.</span></span>

| <span data-ttu-id="9a252-108">**機能**</span><span class="sxs-lookup"><span data-stu-id="9a252-108">**Feature**</span></span>        | <span data-ttu-id="9a252-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a252-109">**Description**</span></span>   |
|--------------------|--------|
| <span data-ttu-id="9a252-110">システム診断</span><span class="sxs-lookup"><span data-stu-id="9a252-110">System diagnostics</span></span> | <span data-ttu-id="9a252-111">システム診断は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="9a252-111">System diagnostics has been deprecated.</span></span> <span data-ttu-id="9a252-112">現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="9a252-112">All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> |
| <span data-ttu-id="9a252-113">サービス要求</span><span class="sxs-lookup"><span data-stu-id="9a252-113">Service requests</span></span>   | <span data-ttu-id="9a252-114">サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="9a252-114">Service requests are being replaced with self-service actions.</span></span> |

### <a name="known-issues-in-this-release"></a><span data-ttu-id="9a252-115">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="9a252-115">Known issues in this release</span></span>
<span data-ttu-id="9a252-116">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="9a252-116">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="9a252-117">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="9a252-117">Every 2 weeks there is a new release of LCS.</span></span>

-   <span data-ttu-id="9a252-118">配置エラーを一覧表示するログ ファイルは、まだ LCS を通じて使用できません。</span><span class="sxs-lookup"><span data-stu-id="9a252-118">Log files listing deployment failures are not yet available through LCS.</span></span> <span data-ttu-id="9a252-119">現時点では、ログ ファイルが必要な場合は、サポート チケットを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="9a252-119">Currently, you can open a support ticket if you need the log files.</span></span>

-   <span data-ttu-id="9a252-120">アプリケーション環境からの LCS の統合が機能しません。</span><span class="sxs-lookup"><span data-stu-id="9a252-120">LCS integration from the application environment does not work.</span></span> <span data-ttu-id="9a252-121">この結果使用できない機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="9a252-121">The features that are not available as a result of this include:</span></span>

    -   <span data-ttu-id="9a252-122">はじめに</span><span class="sxs-lookup"><span data-stu-id="9a252-122">Getting started</span></span>

    -   <span data-ttu-id="9a252-123">BPM ライブラリを通じて有効なオンライン ヘルプ。</span><span class="sxs-lookup"><span data-stu-id="9a252-123">Online Help enabled through BPM libraries.</span></span> <span data-ttu-id="9a252-124">docs.microsoft.com のオンライン ヘルプは使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a252-124">Online Help from docs.microsoft.com is available.</span></span>

    -   <span data-ttu-id="9a252-125">アプリケーション内からのサポート チケットを引き上げます。</span><span class="sxs-lookup"><span data-stu-id="9a252-125">Raising support tickets from within the application.</span></span> <span data-ttu-id="9a252-126">LCS からのクラウドを利用したサポートが有効です。</span><span class="sxs-lookup"><span data-stu-id="9a252-126">Cloud-powered support from LCS is enabled.</span></span>

## <a name="finance-and-operations-apps"></a><span data-ttu-id="9a252-127">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="9a252-127">Finance and Operations apps</span></span> 

### <a name="features-not-yet-implemented"></a><span data-ttu-id="9a252-128">まだ実装されていない機能</span><span class="sxs-lookup"><span data-stu-id="9a252-128">Features not yet implemented</span></span>

<span data-ttu-id="9a252-129">インフラストラクチャの依存関係がある次の機能は、最新の配置エクスペリエンスにはまだ実装されていません。</span><span class="sxs-lookup"><span data-stu-id="9a252-129">The following features that have infrastructure dependencies are not yet implemented in the modern deployment experience.</span></span> <span data-ttu-id="9a252-130">これらの機能は推奨されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="9a252-130">These features have not been deprecated.</span></span>

| <span data-ttu-id="9a252-131">**機能**</span><span class="sxs-lookup"><span data-stu-id="9a252-131">**Feature**</span></span>                 | <span data-ttu-id="9a252-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a252-132">**Description**</span></span>                                           |
|-----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="9a252-133">小売</span><span class="sxs-lookup"><span data-stu-id="9a252-133">Retail</span></span>                      | <span data-ttu-id="9a252-134">Retail のサポートがまだ有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="9a252-134">Retail support is not yet enabled.</span></span>                        |
| <span data-ttu-id="9a252-135">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="9a252-135">Trace Parser</span></span>                | <span data-ttu-id="9a252-136">実績ツールはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="9a252-136">Perf tools are not yet supported.</span></span>                         |

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="9a252-137">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="9a252-137">Features not intended to be implemented</span></span>
<span data-ttu-id="9a252-138">次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。</span><span class="sxs-lookup"><span data-stu-id="9a252-138">The following features are deprecated and will not be implemented in the modern deployment experience.</span></span>

| <span data-ttu-id="9a252-139">**機能**</span><span class="sxs-lookup"><span data-stu-id="9a252-139">**Feature**</span></span>  | <span data-ttu-id="9a252-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="9a252-140">**Description**</span></span>                     |
|--------------|-------------------------------------|
| <span data-ttu-id="9a252-141">カスタム フォント</span><span class="sxs-lookup"><span data-stu-id="9a252-141">Custom fonts</span></span> | <span data-ttu-id="9a252-142">カスタム フォントはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="9a252-142">Custom fonts will not be supported.</span></span> |

