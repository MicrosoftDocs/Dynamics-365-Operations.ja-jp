---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
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
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 37626ca1f8a041ac7c2133735dffc1c4ea2bd6d3
ms.sourcegitcommit: 708b3966b1c2bd4999f528d4a03a89d9bb530616
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2020
ms.locfileid: "3100484"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="3f9d1-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="3f9d1-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="3f9d1-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="3f9d1-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="3f9d1-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="3f9d1-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="3f9d1-106">Features not intended to be implemented</span></span>
<span data-ttu-id="3f9d1-107">次の LCS 機能は廃止されており、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-107">The following LCS features are deprecated and will not be implemented in self-service deployment.</span></span>

| <span data-ttu-id="3f9d1-108">**機能**</span><span class="sxs-lookup"><span data-stu-id="3f9d1-108">**Feature**</span></span>        | <span data-ttu-id="3f9d1-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f9d1-109">**Description**</span></span>   |
|--------------------|--------|
| <span data-ttu-id="3f9d1-110">システム診断</span><span class="sxs-lookup"><span data-stu-id="3f9d1-110">System diagnostics</span></span> | <span data-ttu-id="3f9d1-111">システム診断は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-111">System diagnostics has been deprecated.</span></span> <span data-ttu-id="3f9d1-112">現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-112">All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> |
| <span data-ttu-id="3f9d1-113">サービス要求</span><span class="sxs-lookup"><span data-stu-id="3f9d1-113">Service requests</span></span>   | <span data-ttu-id="3f9d1-114">サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-114">Service requests are being replaced with self-service actions.</span></span> |

### <a name="known-issues-in-this-release"></a><span data-ttu-id="3f9d1-115">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="3f9d1-115">Known issues in this release</span></span>
<span data-ttu-id="3f9d1-116">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-116">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="3f9d1-117">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-117">Every 2 weeks there is a new release of LCS.</span></span>

-   <span data-ttu-id="3f9d1-118">配置エラーを一覧表示するログ ファイルは、まだ LCS を通じて使用できません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-118">Log files listing deployment failures are not yet available through LCS.</span></span> <span data-ttu-id="3f9d1-119">現時点では、ログ ファイルが必要な場合は、サポート チケットを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-119">Currently, you can open a support ticket if you need the log files.</span></span>

-   <span data-ttu-id="3f9d1-120">アプリケーション環境からの LCS の統合が機能しません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-120">LCS integration from the application environment does not work.</span></span> <span data-ttu-id="3f9d1-121">この結果使用できない機能は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-121">The features that are not available as a result of this include:</span></span>

    -   <span data-ttu-id="3f9d1-122">はじめに</span><span class="sxs-lookup"><span data-stu-id="3f9d1-122">Getting started</span></span>

    -   <span data-ttu-id="3f9d1-123">BPM ライブラリを通じて有効なオンライン ヘルプ。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-123">Online Help enabled through BPM libraries.</span></span> <span data-ttu-id="3f9d1-124">docs.microsoft.com のオンライン ヘルプは使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-124">Online Help from docs.microsoft.com is available.</span></span>

    -   <span data-ttu-id="3f9d1-125">アプリケーション内からのサポート チケットを引き上げます。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-125">Raising support tickets from within the application.</span></span> <span data-ttu-id="3f9d1-126">LCS からのクラウドを利用したサポートが有効です。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-126">Cloud-powered support from LCS is enabled.</span></span>

## <a name="finance-and-operations-apps"></a><span data-ttu-id="3f9d1-127">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="3f9d1-127">Finance and Operations apps</span></span> 

### <a name="features-not-yet-implemented"></a><span data-ttu-id="3f9d1-128">まだ実装されていない機能</span><span class="sxs-lookup"><span data-stu-id="3f9d1-128">Features not yet implemented</span></span>

<span data-ttu-id="3f9d1-129">インフラストラクチャの依存関係がある次の機能は、最新の配置エクスペリエンスにはまだ実装されていません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-129">The following features that have infrastructure dependencies are not yet implemented in the modern deployment experience.</span></span> <span data-ttu-id="3f9d1-130">これらの機能は推奨されていませんでした。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-130">These features have not been deprecated.</span></span>

| <span data-ttu-id="3f9d1-131">**機能**</span><span class="sxs-lookup"><span data-stu-id="3f9d1-131">**Feature**</span></span>                 | <span data-ttu-id="3f9d1-132">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f9d1-132">**Description**</span></span>                                           |
|-----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="3f9d1-133">Commerce</span><span class="sxs-lookup"><span data-stu-id="3f9d1-133">Commerce</span></span>                      | <span data-ttu-id="3f9d1-134">コマースのサポートがまだ有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-134">Commerce support is not yet enabled.</span></span>                        |
| <span data-ttu-id="3f9d1-135">Trace Parser</span><span class="sxs-lookup"><span data-stu-id="3f9d1-135">Trace Parser</span></span>                | <span data-ttu-id="3f9d1-136">実績ツールはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-136">Perf tools are not yet supported.</span></span>                         |

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="3f9d1-137">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="3f9d1-137">Features not intended to be implemented</span></span>
<span data-ttu-id="3f9d1-138">次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-138">The following features are deprecated and will not be implemented in the modern deployment experience.</span></span>

| <span data-ttu-id="3f9d1-139">**機能**</span><span class="sxs-lookup"><span data-stu-id="3f9d1-139">**Feature**</span></span>  | <span data-ttu-id="3f9d1-140">**説明**</span><span class="sxs-lookup"><span data-stu-id="3f9d1-140">**Description**</span></span>                     |
|--------------|-------------------------------------|
| <span data-ttu-id="3f9d1-141">カスタム フォント</span><span class="sxs-lookup"><span data-stu-id="3f9d1-141">Custom fonts</span></span> | <span data-ttu-id="3f9d1-142">カスタム フォントはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="3f9d1-142">Custom fonts will not be supported.</span></span> |

