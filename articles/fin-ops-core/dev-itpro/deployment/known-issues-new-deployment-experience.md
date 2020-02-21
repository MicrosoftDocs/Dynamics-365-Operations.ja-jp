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
ms.openlocfilehash: 7e8672a86841a0f905f006ad85d87e8f28c70ee2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003605"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="6ae78-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ae78-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="6ae78-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="6ae78-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="6ae78-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6ae78-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="6ae78-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="6ae78-106">Features not intended to be implemented</span></span>
<span data-ttu-id="6ae78-107">次の LCS 機能は廃止されており、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-107">The following LCS features are deprecated and will not be implemented in self-service deployment.</span></span>

| <span data-ttu-id="6ae78-108">**機能**</span><span class="sxs-lookup"><span data-stu-id="6ae78-108">**Feature**</span></span>        | <span data-ttu-id="6ae78-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ae78-109">**Description**</span></span>   |
|--------------------|--------|
| <span data-ttu-id="6ae78-110">システム診断</span><span class="sxs-lookup"><span data-stu-id="6ae78-110">System diagnostics</span></span> | <span data-ttu-id="6ae78-111">システム診断は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="6ae78-111">System diagnostics has been deprecated.</span></span> <span data-ttu-id="6ae78-112">現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="6ae78-112">All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> |
| <span data-ttu-id="6ae78-113">サービス要求</span><span class="sxs-lookup"><span data-stu-id="6ae78-113">Service requests</span></span>   | <span data-ttu-id="6ae78-114">サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="6ae78-114">Service requests are being replaced with self-service actions.</span></span> |

### <a name="known-issues-in-this-release"></a><span data-ttu-id="6ae78-115">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="6ae78-115">Known issues in this release</span></span>
<span data-ttu-id="6ae78-116">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="6ae78-116">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="6ae78-117">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="6ae78-117">Every 2 weeks there is a new release of LCS.</span></span>

-   <span data-ttu-id="6ae78-118">配置エラーを一覧表示するログ ファイルは、まだ LCS を通じて使用できません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-118">Log files listing deployment failures are not yet available through LCS.</span></span> <span data-ttu-id="6ae78-119">現時点では、ログ ファイルが必要な場合は、サポート チケットを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="6ae78-119">Currently, you can open a support ticket if you need the log files.</span></span>

-   <span data-ttu-id="6ae78-120">アプリケーション環境からの LCS の統合が機能しません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-120">LCS integration from the application environment does not work.</span></span> <span data-ttu-id="6ae78-121">この結果使用できない機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="6ae78-121">The features that are not available as a result of this include:</span></span>

    -   <span data-ttu-id="6ae78-122">はじめに</span><span class="sxs-lookup"><span data-stu-id="6ae78-122">Getting started</span></span>

    -   <span data-ttu-id="6ae78-123">BPM ライブラリを通じて有効なオンライン ヘルプ。</span><span class="sxs-lookup"><span data-stu-id="6ae78-123">Online Help enabled through BPM libraries.</span></span> <span data-ttu-id="6ae78-124">docs.microsoft.com のオンライン ヘルプは使用できます。</span><span class="sxs-lookup"><span data-stu-id="6ae78-124">Online Help from docs.microsoft.com is available.</span></span>

    -   <span data-ttu-id="6ae78-125">アプリケーション内からのサポート チケットを引き上げます。</span><span class="sxs-lookup"><span data-stu-id="6ae78-125">Raising support tickets from within the application.</span></span> <span data-ttu-id="6ae78-126">LCS からのクラウドを利用したサポートが有効です。</span><span class="sxs-lookup"><span data-stu-id="6ae78-126">Cloud-powered support from LCS is enabled.</span></span>

## <a name="finance-and-operations-apps"></a><span data-ttu-id="6ae78-127">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="6ae78-127">Finance and Operations apps</span></span> 

### <a name="features-not-yet-implemented"></a><span data-ttu-id="6ae78-128">まだ実装されていない機能</span><span class="sxs-lookup"><span data-stu-id="6ae78-128">Features not yet implemented</span></span>

<span data-ttu-id="6ae78-129">インフラストラクチャの依存関係がある次の機能は、最新の配置エクスペリエンスにはまだ実装されていません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-129">The following features that have infrastructure dependencies are not yet implemented in the modern deployment experience.</span></span> <span data-ttu-id="6ae78-130">これらの機能は推奨されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="6ae78-130">These features have not been deprecated.</span></span>

| <span data-ttu-id="6ae78-131">**機能**</span><span class="sxs-lookup"><span data-stu-id="6ae78-131">**Feature**</span></span>                 | <span data-ttu-id="6ae78-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ae78-132">**Description**</span></span>                                           |
|-----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="6ae78-133">Commerce</span><span class="sxs-lookup"><span data-stu-id="6ae78-133">Commerce</span></span>                      | <span data-ttu-id="6ae78-134">コマースのサポートがまだ有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-134">Commerce support is not yet enabled.</span></span>                        |
| <span data-ttu-id="6ae78-135">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="6ae78-135">Trace Parser</span></span>                | <span data-ttu-id="6ae78-136">実績ツールはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-136">Perf tools are not yet supported.</span></span>                         |

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="6ae78-137">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="6ae78-137">Features not intended to be implemented</span></span>
<span data-ttu-id="6ae78-138">次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-138">The following features are deprecated and will not be implemented in the modern deployment experience.</span></span>

| <span data-ttu-id="6ae78-139">**機能**</span><span class="sxs-lookup"><span data-stu-id="6ae78-139">**Feature**</span></span>  | <span data-ttu-id="6ae78-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="6ae78-140">**Description**</span></span>                     |
|--------------|-------------------------------------|
| <span data-ttu-id="6ae78-141">カスタム フォント</span><span class="sxs-lookup"><span data-stu-id="6ae78-141">Custom fonts</span></span> | <span data-ttu-id="6ae78-142">カスタム フォントはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6ae78-142">Custom fonts will not be supported.</span></span> |

