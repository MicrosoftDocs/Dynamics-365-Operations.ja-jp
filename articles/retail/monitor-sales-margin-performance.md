---
title: 販売と利益幅のパフォーマンスの監視
description: Dynamics 365 Retail を使用してリアルタイムに販売と利益幅のパフォーマンスを監視できます。
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 46ecefdd15a3a208588aaf630571764047464cdb
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018067"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="aa7e8-103">販売と利益幅のパフォーマンスの監視</span><span class="sxs-lookup"><span data-stu-id="aa7e8-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aa7e8-104">Dynamics 365 Retail を使用してリアルタイムに販売と利益幅のパフォーマンスを監視できます。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-104">You can monitor sales and margin performance in real time using Dynamics 365 Retail.</span></span>

<span data-ttu-id="aa7e8-105">小売の一部として、販売と利益幅のパフォーマンスを次の分析コードの組織階層のさまざまなレベルでリアルタイムに監視できます。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-105">As part of Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="aa7e8-106">製品</span><span class="sxs-lookup"><span data-stu-id="aa7e8-106">Products</span></span>
- <span data-ttu-id="aa7e8-107">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="aa7e8-107">Categories</span></span>
- <span data-ttu-id="aa7e8-108">割引</span><span class="sxs-lookup"><span data-stu-id="aa7e8-108">Discounts</span></span>
- <span data-ttu-id="aa7e8-109">期間を年とする</span><span class="sxs-lookup"><span data-stu-id="aa7e8-109">Years as time period</span></span>
- <span data-ttu-id="aa7e8-110">登録/ターミナル</span><span class="sxs-lookup"><span data-stu-id="aa7e8-110">Registers/terminals</span></span>
- <span data-ttu-id="aa7e8-111">スタッフ/従業員</span><span class="sxs-lookup"><span data-stu-id="aa7e8-111">Staff/employees</span></span>
- <span data-ttu-id="aa7e8-112">顧客</span><span class="sxs-lookup"><span data-stu-id="aa7e8-112">Customers</span></span>
- <span data-ttu-id="aa7e8-113">作業単位</span><span class="sxs-lookup"><span data-stu-id="aa7e8-113">Operating units</span></span>

<span data-ttu-id="aa7e8-114">また、階層グリッド構造を活用する 2 つの固有のレポートにより、ユーザーは既定の小売製品カテゴリ階層でトップ カテゴリ ノードからカテゴリの個々のリーフ ノードへドリルダウンして、販売と利益幅のパフォーマンスを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="aa7e8-115">ユーザーは、小売レポート階層のために既定の組織階層として定義された組織階層で、上位の作業単位から個々のチャンネルにドリルダウンすることもできます。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="aa7e8-116">次の場所のいずれかからレポートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="aa7e8-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="aa7e8-117">**小売店舗管理** ワークスペース &gt; **小売** &gt; **チャンネル** &gt; **小売店舗管理** &gt; **レポート**</span><span class="sxs-lookup"><span data-stu-id="aa7e8-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="aa7e8-118">**カテゴリと製品の管理** ワークスペース &gt; **小売** &gt; **製品とカテゴリ** &gt; **小売店舗の管理** &gt; **レポート**</span><span class="sxs-lookup"><span data-stu-id="aa7e8-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="aa7e8-119">**価格設定および割引に管理** ワークスペース &gt; **小売** &gt; **価格決定と割引** &gt; **小売店舗の管理** &gt; **レポート**</span><span class="sxs-lookup"><span data-stu-id="aa7e8-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
- <span data-ttu-id="aa7e8-120">**照会とレポート** セクション &gt; **小売** &gt; **照会とレポート** &gt; **売上レポート**</span><span class="sxs-lookup"><span data-stu-id="aa7e8-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
