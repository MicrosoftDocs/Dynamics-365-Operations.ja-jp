---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
manager: AnnBe
ms.date: 06/02/2020
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
ms.openlocfilehash: ebeb9584904cc749f5b5a2f3891f851a72d76591
ms.sourcegitcommit: 3fa1e8583003a90ba486f757c3826b139e1b3f73
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/02/2020
ms.locfileid: "3421567"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="c9591-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="c9591-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="c9591-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="c9591-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="c9591-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c9591-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="c9591-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="c9591-106">Features not intended to be implemented</span></span>
<span data-ttu-id="c9591-107">次の LCS 機能は廃止されており、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="c9591-107">The following LCS features are deprecated and will not be implemented in self-service deployment.</span></span>

| <span data-ttu-id="c9591-108">**機能**</span><span class="sxs-lookup"><span data-stu-id="c9591-108">**Feature**</span></span>        | <span data-ttu-id="c9591-109">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9591-109">**Description**</span></span>   |
|--------------------|--------|
| <span data-ttu-id="c9591-110">システム診断</span><span class="sxs-lookup"><span data-stu-id="c9591-110">System diagnostics</span></span> | <span data-ttu-id="c9591-111">システム診断は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="c9591-111">System diagnostics has been deprecated.</span></span> <span data-ttu-id="c9591-112">現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c9591-112">All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> |
| <span data-ttu-id="c9591-113">サービス要求</span><span class="sxs-lookup"><span data-stu-id="c9591-113">Service requests</span></span>   | <span data-ttu-id="c9591-114">サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="c9591-114">Service requests are being replaced with self-service actions.</span></span> |

### <a name="known-issues-in-this-release"></a><span data-ttu-id="c9591-115">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="c9591-115">Known issues in this release</span></span>
<span data-ttu-id="c9591-116">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="c9591-116">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="c9591-117">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="c9591-117">Every 2 weeks there is a new release of LCS.</span></span>

## <a name="finance-and-operations-apps"></a><span data-ttu-id="c9591-118">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="c9591-118">Finance and Operations apps</span></span> 

> [!NOTE]
> <span data-ttu-id="c9591-119">Dynamics 365 Commerce は、10.0.10 リリースを使用した最新の配置エクスペリエンスに実装されています。</span><span class="sxs-lookup"><span data-stu-id="c9591-119">Dynamics 365 Commerce is implemented in the modern deployment experience with the 10.0.10 release.</span></span> <span data-ttu-id="c9591-120">詳細については、[セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9591-120">For more information, see [Create payment packaging for Application Explorer for self-service deployment](../../../commerce/dev-itpro/payment-connector-package.md).</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="c9591-121">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="c9591-121">Features not intended to be implemented</span></span>
<span data-ttu-id="c9591-122">次の機能は廃止されており、最新の配置エクスペリエンスでは実装されません。</span><span class="sxs-lookup"><span data-stu-id="c9591-122">The following features are deprecated and will not be implemented in the modern deployment experience.</span></span>

| <span data-ttu-id="c9591-123">**機能**</span><span class="sxs-lookup"><span data-stu-id="c9591-123">**Feature**</span></span>  | <span data-ttu-id="c9591-124">**説明**</span><span class="sxs-lookup"><span data-stu-id="c9591-124">**Description**</span></span>                     |
|--------------|-------------------------------------|
| <span data-ttu-id="c9591-125">カスタム フォント</span><span class="sxs-lookup"><span data-stu-id="c9591-125">Custom fonts</span></span> | <span data-ttu-id="c9591-126">カスタム フォントはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c9591-126">Custom fonts are not supported.</span></span> <span data-ttu-id="c9591-127">詳細については、[Dynamics 365 アプリケーションのドキュメント レポート サービス](../analytics/reporting-experience-iias-environments.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9591-127">For more information, see [Document Reporting Service in Dynamics 365 applications](../analytics/reporting-experience-iias-environments.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c9591-128">非推奨の機能の詳細については、[削除済みまたは非推奨のプラットフォーム機能](../get-started/removed-deprecated-features-platform-updates.md)、[以前のリリースからの削除済みおよび非推奨の機能](../migration-upgrade/deprecated-features.md)、[以前のリリースの削除済みおよび非推奨の機能](../get-started/removed-deprecated-features-platform-updates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9591-128">For more information about deprecated features, see [Removed or deprecated platform features](../get-started/removed-deprecated-features-platform-updates.md) and [Removed or deprecated features from previous releases](../migration-upgrade/deprecated-features.md) and [Removed or deprecated features in previous releases](../get-started/removed-deprecated-features-platform-updates.md).</span></span>
