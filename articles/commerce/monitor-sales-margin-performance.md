---
title: 販売と利益幅のパフォーマンスの監視
description: Dynamics 365 Commerce を使用してリアルタイムに販売と利益幅のパフォーマンスを監視できます。
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
ms.openlocfilehash: a7b2b6ba8115b43ef2e52e934bf8364e6f4044e7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413686"
---
# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="8c8b8-103">販売と利益幅のパフォーマンスの監視</span><span class="sxs-lookup"><span data-stu-id="8c8b8-103">Monitor sales and margin performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c8b8-104">Dynamics 365 Commerce を使用してリアルタイムに販売と利益幅のパフォーマンスを監視できます。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-104">You can monitor sales and margin performance in real time using Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8c8b8-105">Commerce の一部として、ユーザーは次の分析コードで販売と利益幅のパフォーマンスを組織階層のさまざまなレベルでリアル タイムに監視できます。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-105">As part of Commerce, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

- <span data-ttu-id="8c8b8-106">製品</span><span class="sxs-lookup"><span data-stu-id="8c8b8-106">Products</span></span>
- <span data-ttu-id="8c8b8-107">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="8c8b8-107">Categories</span></span>
- <span data-ttu-id="8c8b8-108">割引</span><span class="sxs-lookup"><span data-stu-id="8c8b8-108">Discounts</span></span>
- <span data-ttu-id="8c8b8-109">期間を年とする</span><span class="sxs-lookup"><span data-stu-id="8c8b8-109">Years as time period</span></span>
- <span data-ttu-id="8c8b8-110">登録/ターミナル</span><span class="sxs-lookup"><span data-stu-id="8c8b8-110">Registers/terminals</span></span>
- <span data-ttu-id="8c8b8-111">スタッフ/従業員</span><span class="sxs-lookup"><span data-stu-id="8c8b8-111">Staff/employees</span></span>
- <span data-ttu-id="8c8b8-112">顧客</span><span class="sxs-lookup"><span data-stu-id="8c8b8-112">Customers</span></span>
- <span data-ttu-id="8c8b8-113">作業単位</span><span class="sxs-lookup"><span data-stu-id="8c8b8-113">Operating units</span></span>

<span data-ttu-id="8c8b8-114">また、階層グリッド構造を活用する 2 つの固有のレポートにより、ユーザーは既定の製品カテゴリ階層でトップ カテゴリ ノードからカテゴリの個々のリーフ ノードへドリル ダウンして、販売と利益幅のパフォーマンスを監視することができます。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default product category hierarchy.</span></span> <span data-ttu-id="8c8b8-115">ユーザーは、レポート用に既定の組織階層として定義された組織階層で、上位の作業単位から個々のチャンネルにドリルダウンすることもできます。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for reporting.</span></span> <span data-ttu-id="8c8b8-116">次の場所のいずれかからレポートを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="8c8b8-116">You can open the reports from any of the following locations:</span></span>

- <span data-ttu-id="8c8b8-117">**店舗管理** ワークスペース &gt; **Retail および Commerce** &gt; **チャンネル** &gt; **店舗管理** &gt; **レポート**</span><span class="sxs-lookup"><span data-stu-id="8c8b8-117">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="8c8b8-118">**カテゴリと製品の管理** ワークスペース &gt; **Retail および Commerce** &gt; **製品とカテゴリ** &gt; **店舗管理** &gt; **レポート**</span><span class="sxs-lookup"><span data-stu-id="8c8b8-118">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Product and categories** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="8c8b8-119">**価格設定および割引の管理** ワークスペース &gt; **Retail および Commerce** &gt; **価格決定と割引** &gt; **店舗管理** &gt; **レポート**</span><span class="sxs-lookup"><span data-stu-id="8c8b8-119">**Pricing and discount management** workspace &gt; **Retail and Commerce** &gt; **Pricing and discounts** &gt; **Store management** &gt; **Reports**</span></span>
- <span data-ttu-id="8c8b8-120">**照会とレポート** セクション &gt; **Retail および Commerce** &gt; **照会とレポート** &gt; **売上レポート**</span><span class="sxs-lookup"><span data-stu-id="8c8b8-120">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>
