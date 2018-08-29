---
title: "Lifecycle Services (LCS) のシステム診断"
description: "このトピックでは、Lifecycle Services (LCS) のシステム診断に関する詳細情報を提供します。"
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 19061
ms.assetid: 9a217373-f72b-4a28-adef-79900e40c872
ms.search.region: Global
ms.author: murtazac
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 597e24d95dd182db0df46c5deb0f76e7e4e44e3b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="system-diagnostics-in-lifecycle-services-lcs"></a><span data-ttu-id="8c2d4-103">Lifecycle Services (LCS) のシステム診断</span><span class="sxs-lookup"><span data-stu-id="8c2d4-103">System diagnostics in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c2d4-104">Microsoft Dynamics Lifecycle Services で、システム診断は管理者が 1 つまたは複数の Microsoft Dynamics AX 環境の正常性を監視および把握するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-104">In Microsoft Dynamics Lifecycle Services, the System diagnostics helps administrators monitor and understand the health of one or more Microsoft Dynamics AX environments.</span></span> <span data-ttu-id="8c2d4-105">次のタスクを実行するように構成できるローカルにインストールされたコンポーネントがあるクラウド ベースのツールです。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-105">It is a cloud-based tool that has a locally-installed component that can be configured to perform the following tasks:</span></span>
-   <span data-ttu-id="8c2d4-106">オンプレミスの Microsoft Dynamics AX 環境を検出 (データベースのインスタンスおよび Microsoft Dynamics AX Application Object Server (AOS) インスタンス)。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-106">Discover on-premises Microsoft Dynamics AX environments (database instances and Microsoft Dynamics AX Application Object Server (AOS) instances).</span></span>
-   <span data-ttu-id="8c2d4-107">検出された環境からデータを収集します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-107">Collect data from the environments that were discovered.</span></span>
-   <span data-ttu-id="8c2d4-108">収集したデータでルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-108">Run rules on the collected data.</span></span>
-   <span data-ttu-id="8c2d4-109">ダッシュボードの規則違反を報告します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-109">Report rule violations on a dashboard.</span></span>
-   <span data-ttu-id="8c2d4-110">レポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-110">Provide reports.</span></span>

<span data-ttu-id="8c2d4-111">データは、事前定義されたスケジュールで実行されるジョブを使用して収集されます。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-111">Data is collected by using jobs that run on predefined schedules.</span></span> <span data-ttu-id="8c2d4-112">次の図は、システム診断プログラムとローカルにインストールされたコンポーネントがどのようにやり取りするかを示しています。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-112">The following diagram describes how System diagnostics and the locally-installed components interact.</span></span>
<span data-ttu-id="8c2d4-113">システム診断サービス</span><span class="sxs-lookup"><span data-stu-id="8c2d4-113">System diagnostic service</span></span>

![システム診断サービス (Lifecycle Services)](./media/systemdiagnosticservicelifecycleservices.png) <span data-ttu-id="8c2d4-115">システム診断では、Microsoft Dynamics AX の次のバージョンがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-115">System diagnostics supports the following versions of Microsoft Dynamics AX:</span></span>
-   <span data-ttu-id="8c2d4-116">Microsoft Dynamics AX 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8c2d4-116">Microsoft Dynamics AX 2012 R2</span></span>
-   <span data-ttu-id="8c2d4-117">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="8c2d4-117">Microsoft Dynamics AX 2012 Feature Pack</span></span>
-   <span data-ttu-id="8c2d4-118">Microsoft Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="8c2d4-118">Microsoft Dynamics AX 2012</span></span>
-   <span data-ttu-id="8c2d4-119">Microsoft Dynamics AX 2012 R3</span><span class="sxs-lookup"><span data-stu-id="8c2d4-119">Microsoft Dynamics AX 2012 R3</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8c2d4-120">前提条件</span><span class="sxs-lookup"><span data-stu-id="8c2d4-120">Prerequisites</span></span>
<span data-ttu-id="8c2d4-121">システム診断を使用する前に、次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-121">Before you can use the System diagnostics, you must complete the following tasks:</span></span>
-   <span data-ttu-id="8c2d4-122">Diagnostic サービスのインストーラーをダウンロードして実行します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-122">Download and run the installer for the Diagnostic service.</span></span>
-   <span data-ttu-id="8c2d4-123">検出ウィザードを実行します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-123">Run the Discovery wizard.</span></span>
-   <span data-ttu-id="8c2d4-124">データの収集をスケジュールまたは実行します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-124">Schedule or run data collection.</span></span>

## <a name="getting-started"></a><span data-ttu-id="8c2d4-125">はじめに</span><span class="sxs-lookup"><span data-stu-id="8c2d4-125">Getting started</span></span>
<span data-ttu-id="8c2d4-126">次のトピックでは、システム診断をインストールして使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8c2d4-126">The following topics explain how to install and use System diagnostics.</span></span>
-   [<span data-ttu-id="8c2d4-127">システム診断のインストールと実行 (Lifecycle Services)</span><span class="sxs-lookup"><span data-stu-id="8c2d4-127">Install and run System diagnostics (Lifecycle Services)</span></span>](install-run-system-diagnostics-lcs.md)
-   [<span data-ttu-id="8c2d4-128">システム診断を使用する (Lifecycle Services)</span><span class="sxs-lookup"><span data-stu-id="8c2d4-128">Use System diagnostics (Lifecycle Services)</span></span>](system-diagnostics-lcs.md)






