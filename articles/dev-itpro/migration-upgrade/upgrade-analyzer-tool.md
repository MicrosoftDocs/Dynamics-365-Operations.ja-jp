---
title: "AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画"
description: "このトピックでは、アップグレード アナライザー ツールを使用して、Dynamics AX 2012 から Dynamics 365 for Finance and Operations へのアップグレードを計画する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 01/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 106163
ms.assetid: 
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-05-31
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: fd3a58c887f68e15dbdd81edc0299866aa82c7c6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="upgrade-from-ax-2012---plan-by-using-the-upgrade-analyzer-tool"></a><span data-ttu-id="c43ec-103">AX 2012 からのアップグレード - アップグレード アナライザー ツールを使用した計画</span><span class="sxs-lookup"><span data-stu-id="c43ec-103">Upgrade from AX 2012 - Plan by using the Upgrade analyzer tool</span></span>

[!include [banner](../includes/banner.md)]

[!include [upgrade banner](../includes/upgrade-banner.md)]

<span data-ttu-id="c43ec-104">このトピックでは、アップグレード アナライザー ツールを使用して、Microsoft Dynamics AX 2012 から Microsoft Dynamics 365 for Finance and Operations へのアップグレードを計画する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c43ec-104">This topic explains how to use the Upgrade analyzer tool to plan your upgrade from Microsoft Dynamics AX 2012 to Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c43ec-105">このツールは、AX 2012 環境に対して実行され、 Finance and Operations サブスクリプション コストの削減を助けるために、AX 2012 内でクリーンアップする必要のあるデータを識別します。</span><span class="sxs-lookup"><span data-stu-id="c43ec-105">This tool is run against an AX 2012 environment and identifies data that you should clean up in AX 2012 to help reduce the subscription cost for Finance and Operations.</span></span> <span data-ttu-id="c43ec-106">このツールは、アップグレード プロセスのスピードアップに役立つ SQL 構成の最適化を提案します。</span><span class="sxs-lookup"><span data-stu-id="c43ec-106">The tool also suggests SQL configuration optimizations that can help speed up the upgrade processes.</span></span> <span data-ttu-id="c43ec-107">また、AX 2012 で使用する機能が Finance and Operations で廃止されている場合は、このツールが警告します。</span><span class="sxs-lookup"><span data-stu-id="c43ec-107">Additionally, the tool warns you if any features that you use in AX 2012 are obsolete in Finance and Operations.</span></span> <span data-ttu-id="c43ec-108">したがって、これらの機能を置き換える方法や回避する方法を計画できます。</span><span class="sxs-lookup"><span data-stu-id="c43ec-108">Therefore, you can plan ways to replace or work around those features.</span></span>

<span data-ttu-id="c43ec-109">アップグレード アナライザーは、Microsoft Dynamics Lifecycle Services (LCS) の通常のシステム診断サービスの一部として、AX 2012 環境からデータを収集します。</span><span class="sxs-lookup"><span data-stu-id="c43ec-109">Upgrade analyzer gathers data from your AX 2012 environment as part of the regular System diagnostic service in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c43ec-110">システム診断サービスの概要、および LCS を通じて使用できるようにデータを収集しクラウドに押し戻す方法に関する情報については、[システム診断 (AX 2012)](../lifecycle-services/ax-2012/system-diagnostics-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c43ec-110">For an overview of the System diagnostic service, and for information about how data is collected and pushed back into the cloud so that you can consume it through LCS, see [System diagnostics (AX 2012)](../lifecycle-services/ax-2012/system-diagnostics-lcs.md).</span></span>

<span data-ttu-id="c43ec-111">LCS の Microsoft Power BI レポートでは、システム診断サービスの結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c43ec-111">You can view the results of the System diagnostic service in a Microsoft Power BI report in LCS.</span></span> <span data-ttu-id="c43ec-112">レポートには、AX 2012 環境で完了する必要のあるタスクのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c43ec-112">The report presents a list of tasks that you should complete in the AX 2012 environment.</span></span>

<span data-ttu-id="c43ec-113">アップグレード分析レポートにアクセスするには、https://diag.lcs.dynamics.com/UpgradeAnalysisReport/Report/<ProjectID> に移動します (<ProjectID> を現在のプロジェクト ID で置き換えます。これは現在の LCS プロジェクトの URL にある整数です)。</span><span class="sxs-lookup"><span data-stu-id="c43ec-113">To access the Upgrade analyzer report, go to https://diag.lcs.dynamics.com/UpgradeAnalysisReport/Report/<ProjectID> (Replace <ProjectID> with your current project ID which is an integer that can be found in the URL of your current LCS project)</span></span>

<span data-ttu-id="c43ec-114">次の図は、アップグレード アナライザーを使用する手順の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="c43ec-114">The following illustration shows an overview of the procedure for using Upgrade analyzer.</span></span>

![アナライザー プロセスのアップグレード](media/upgradeAnalyzerProcess.png)

<span data-ttu-id="c43ec-116">AX 2012 環境内のシステム診断サービスを既に使用している場合は、既存のコンピューターとは異なるコンピューターで、サービスの新しいインスタンスをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c43ec-116">If you already use the System diagnostic service in your AX 2012 environment, you must configure a new instance of the service on a machine that differs from the existing machine.</span></span>

<span data-ttu-id="c43ec-117">AX 2012 環境内のシステム診断サービスをコンフィギュレーションする方法の詳細については、[システム診断のインストールと実行 (AX 2012)](../lifecycle-services/ax-2012/install-run-system-diagnostics-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c43ec-117">For information about how to configure the System diagnostic service in your AX 2012 environment, see [Install and run System diagnostics (AX 2012)](../lifecycle-services/ax-2012/install-run-system-diagnostics-lcs.md).</span></span>

<span data-ttu-id="c43ec-118">システム診断サービスを構成してから数分で、AX 2012 環境が LCS プロジェクトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c43ec-118">Within a few minutes after you configure the System diagnostic service, the AX 2012 environment will appear in your LCS project.</span></span>

