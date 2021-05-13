---
title: データ管理
description: このトピックでは、環境のデータの不整合を見つけて修正する単純なスケジューリング プロセスの使用方法について説明します。
author: RyanCCarlson2
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataMaintenance
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2021-03-31
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 9e4b75f260376ad9801ec8ec03f98e7187fed3ad
ms.sourcegitcommit: 05868764acd3d77970724a30c49c5ae5ffb6ca5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906635"
---
# <a name="data-maintenance"></a><span data-ttu-id="36111-103">データ管理</span><span class="sxs-lookup"><span data-stu-id="36111-103">Data maintenance</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="36111-104">データ管理によって、単純なスケジューリング プロセスを実行して、環境内のデータの不整合を検出または修正できます。</span><span class="sxs-lookup"><span data-stu-id="36111-104">Data maintenance enables simple scheduling processes that you can run to find or correct data inconsistencies in your environment.</span></span>

<span data-ttu-id="36111-105">誤ったデータを使用すると、毎日、毎月、および年間の運用が悪影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="36111-105">Incorrect data can adversely affect your day-to-day, monthly, and yearly operations.</span></span> <span data-ttu-id="36111-106">誤ったデータによって発生する不整合とエラーは、年度末の活動などの主要なイベントを停止し、日々の収益ストリームを停止し、組織の意思決定能力に影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="36111-106">Inconsistencies and errors that come from incorrect data has the potential to halt major events like year-end activities and can even halt your daily revenue streams and affect your organization's decision-making capabilities.</span></span>

<span data-ttu-id="36111-107">*Data Maintenance Portal* は、システム管理者がデータまたはシステムに直接影響を与えるさまざまなアクションをスケジュールして実行できるツールです。</span><span class="sxs-lookup"><span data-stu-id="36111-107">The *Data Maintenance Portal* is a tool that lets system administrators schedule and run various actions that will have a direct effect on the data or the system.</span></span> <span data-ttu-id="36111-108">一部のアクションは問題を修正する機会を継続的に探しスケジュールすることができ、他のアクションはオン デマンドで実行してシステムに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="36111-108">Some actions can be scheduled to continuously look for opportunities to fix issues, and others can be run on demand to enact some change on the system.</span></span> <span data-ttu-id="36111-109">現在、3 つの基本的なアクション タイプがあります: 直接、スキャン、および固定。</span><span class="sxs-lookup"><span data-stu-id="36111-109">Currently there are three basic types of actions: direct, scanning, and fixing.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="36111-110">アクションのタイプ</span><span class="sxs-lookup"><span data-stu-id="36111-110">Types of actions</span></span>

- <span data-ttu-id="36111-111">*直接アクション* は、オンデマンドでのみ実行され、タスクを直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="36111-111">*Direct actions* can be run on-demand only, and can run tasks directly.</span></span> <span data-ttu-id="36111-112">Microsoft サポートでは直接アクションを使用する場合がありますが、これはダウンタイムを必要とせずにキャッシュをクリアするのと同じくらい簡単か、またはサポート プロセスを支援するために参照スキャナーを実行するのと同じくらい複雑です。</span><span class="sxs-lookup"><span data-stu-id="36111-112">Microsoft Support may use direct actions, which could be as simple as clearing a cache without the need for downtime or as complicated as running a reference scanner to aid the support process.</span></span>

- <span data-ttu-id="36111-113">*スキャン アクション* では、1 日に数回、データの問題を検索してデータを検索します。</span><span class="sxs-lookup"><span data-stu-id="36111-113">*Scanning actions* will search your data, a few times a day, looking for problems in the data.</span></span> <span data-ttu-id="36111-114">見つかった問題は、Microsoft に報告されます。</span><span class="sxs-lookup"><span data-stu-id="36111-114">The problems found will be reported to Microsoft.</span></span> <span data-ttu-id="36111-115">自動修正がまだされていない可能性がありますが、データの正常性を改善するために Microsoft に貴重なデータを提供するシステム アクションが多数存在します。</span><span class="sxs-lookup"><span data-stu-id="36111-115">There are a number of system actions that may not yet have an automated fix, but will provide valuable data to Microsoft to improve the health of your data.</span></span> <span data-ttu-id="36111-116">Microsoft は、この方法で見つかった問題についてお客様に連絡する場合があります。</span><span class="sxs-lookup"><span data-stu-id="36111-116">Microsoft may reach out to you regarding problems found through this method.</span></span>

- <span data-ttu-id="36111-117">*アクションの修正* はスキャン アクションと同じ頻度で実行されますが、営業案件が見つかった場合は、データへの修正がスケジュールされます。</span><span class="sxs-lookup"><span data-stu-id="36111-117">*Fixing actions* runs on the same cadence as a scanning action, but when an opportunity is found, it will schedule a fix to the data.</span></span> <span data-ttu-id="36111-118">アクションの修正はデータのべき等を意味し、最初の実行時にすべてのデータを修正できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="36111-118">Fixing actions are meant to be data idempotent and may not fix all of the data on the first run.</span></span> <span data-ttu-id="36111-119">修正アクションでは、データの実行の度にサブセットのみが修正することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="36111-119">We recommend that a fixing action only fixes a subset of data each time it runs.</span></span> <span data-ttu-id="36111-120">時間をかけて、システムに大きな負荷が与えることなく、データはクリーンアップされた状態に到達します。</span><span class="sxs-lookup"><span data-stu-id="36111-120">Over time, the data will reach a clean state without exposing a significant load on the system.</span></span> <span data-ttu-id="36111-121">このタイプのアクションは、システムの一括アップグレードの支援を助ける場合があります。</span><span class="sxs-lookup"><span data-stu-id="36111-121">This type of action may help facilitate an in-place upgrade of your system.</span></span>

## <a name="control-of-actions"></a><span data-ttu-id="36111-122">アクションの管理</span><span class="sxs-lookup"><span data-stu-id="36111-122">Control of actions</span></span>
<span data-ttu-id="36111-123">Data Maintenance Portal にアクセスするには、**システム管理 > 定期処理タスク > データ メンテナンス** に移動します。</span><span class="sxs-lookup"><span data-stu-id="36111-123">To access the Data Maintenance Portal, administrators can go to **System administration > Periodic tasks > Data maintenance**.</span></span> <span data-ttu-id="36111-124">このページでは、管理者が利用可能なアクションの一覧と、各アクションの最新の状態を確認できます。</span><span class="sxs-lookup"><span data-stu-id="36111-124">On this page, administrators can see the list of actions that are available, and the latest status of each action.</span></span> <span data-ttu-id="36111-125">アクションに関する重要情報は、右側のパネルで確認できます。</span><span class="sxs-lookup"><span data-stu-id="36111-125">Important information about the action can be found in the right panel.</span></span> <span data-ttu-id="36111-126">アクションをスケジュールできる場合は、ページの下部に **スケジュール** というラベルの付いたボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="36111-126">If the action can be scheduled, there will be a button labeled **Schedule** available at the bottom of the page.</span></span> <span data-ttu-id="36111-127">**今すぐ実行** ボタンを選択することにより、自動スケジュールによって実行される前に、すべてのアクションがオン デマンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="36111-127">All actions can be run on demand, prior to being run by the automated schedule, by selecting the **Run now** button.</span></span> <span data-ttu-id="36111-128">Microsoft によって定義されたシステム アクションを無効にしたり有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="36111-128">System actions, defined by Microsoft, cannot be disabled or enabled.</span></span> 

> [!NOTE]
> <span data-ttu-id="36111-129">データ メンテナンス 管理プロセスの繰り返しは、プロセス自動化フレームワークによってバックグラウンド プロセスとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="36111-129">The recurrence of data maintenance processes are handled by the process automation framework as background processes.</span></span> <span data-ttu-id="36111-130">バックグラウンド プロセスには 2 つの主要タイプがあります: 機会用スキャンと実行タスクです。</span><span class="sxs-lookup"><span data-stu-id="36111-130">There are two main types of background processes: one for scanning for opportunities and one for running tasks.</span></span> <span data-ttu-id="36111-131">詳細については、[プロセス オートメーション フレームワークの開発](../process-automation/process-automation-framework.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="36111-131">For more information, see [Process automation framework development](../process-automation/process-automation-framework.md).</span></span>
