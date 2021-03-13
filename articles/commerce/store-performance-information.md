---
title: 店舗パフォーマンスの分析
description: この記事では、アクセスしたり、参照したり、Dynamics 365 Commerce データに基づいて、店舗パフォーマンスについての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4688d3268986a9ae6fb2c9601396b56aacf87a93
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009621"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="002bb-103">店舗のパフォーマンスの分析</span><span class="sxs-lookup"><span data-stu-id="002bb-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="002bb-104">この記事では、アクセスしたり、参照したり、Dynamics 365 Commerce データに基づいて、店舗パフォーマンスについての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="002bb-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="002bb-105">Retail の一部として、次の場所のいずれかの最初から用意されている **チャンネル概要** レポートを開くことにより、選択した期間における組織階層のさまざまなレベルでリアルタイムに店舗パフォーマンスを調査できます。</span><span class="sxs-lookup"><span data-stu-id="002bb-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="002bb-106">**小売店舗管理** ワークスペース &gt; **小売** &gt; **チャンネル** &gt; **小売店舗管理** &gt; **レポート** &gt; **チャンネルの集計レポート**</span><span class="sxs-lookup"><span data-stu-id="002bb-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="002bb-107">**小売店舗の財務** ワークスペース &gt; **小売** &gt; **チャンネル** &gt; **小売店舗の財務** &gt; **レポート** &gt; **チャンネルの集計レポート**</span><span class="sxs-lookup"><span data-stu-id="002bb-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="002bb-108">**照会とレポート** セクション &gt; **小売** &gt; **照会とレポート** &gt; **売上レポート** &gt; **チャネル集計レポート**</span><span class="sxs-lookup"><span data-stu-id="002bb-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="002bb-109">このレポートは、店舗パフォーマンスの一部として次のスナップショットの概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="002bb-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="002bb-110">総売上集計</span><span class="sxs-lookup"><span data-stu-id="002bb-110">Gross sales summary</span></span>
- <span data-ttu-id="002bb-111">支払/入金タイプ集計</span><span class="sxs-lookup"><span data-stu-id="002bb-111">Tender type summary</span></span>
- <span data-ttu-id="002bb-112">税集計</span><span class="sxs-lookup"><span data-stu-id="002bb-112">Tax summary</span></span>
- <span data-ttu-id="002bb-113">価格変更の概要</span><span class="sxs-lookup"><span data-stu-id="002bb-113">Price overrides summary</span></span>
- <span data-ttu-id="002bb-114">割引概要</span><span class="sxs-lookup"><span data-stu-id="002bb-114">Discounts summary</span></span>
