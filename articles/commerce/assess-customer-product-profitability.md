---
title: 顧客と製品の収益性の評価
description: この記事では、アクセスしたり、参照したり、Dynamics 365 Commerce データから顧客と製品の収益性についての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3770832cb8eee96931d8f8e68c726d5e09d3fceb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980057"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="e8c2d-103">顧客と製品の収益性の評価</span><span class="sxs-lookup"><span data-stu-id="e8c2d-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8c2d-104">この記事では、アクセスしたり、参照したり、Dynamics 365 Commerce データから顧客と製品の収益性についての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e8c2d-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="e8c2d-105">Commerce の一部として、ユーザーは、次の基準の 1 つに基づいて、組織階層のさまざまなレベルで上位顧客 (10 ～ 100) の収益性を調査できます。</span><span class="sxs-lookup"><span data-stu-id="e8c2d-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e8c2d-106">売上金額</span><span class="sxs-lookup"><span data-stu-id="e8c2d-106">Sales amount</span></span>
- <span data-ttu-id="e8c2d-107">件数</span><span class="sxs-lookup"><span data-stu-id="e8c2d-107">Quantity</span></span>
- <span data-ttu-id="e8c2d-108">売上総利益率</span><span class="sxs-lookup"><span data-stu-id="e8c2d-108">Gross profit margin</span></span>
- <span data-ttu-id="e8c2d-109">利益幅の割合</span><span class="sxs-lookup"><span data-stu-id="e8c2d-109">Margin percentage</span></span>

<span data-ttu-id="e8c2d-110">この評価に関しては、次の場所のいずれかから開くことができる、**上位の顧客** レポートをすぐに使用できます:</span><span class="sxs-lookup"><span data-stu-id="e8c2d-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e8c2d-111">**店舗管理** ワークスペース &gt; **Retail と Commerce** &gt; **チャネル** &gt; **店舗管理** &gt; **レポート** &gt; **上位の顧客レポート**</span><span class="sxs-lookup"><span data-stu-id="e8c2d-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="e8c2d-112">**照会およびレポート** セクション &gt; **Retail と Commerce** &gt; **照会およびレポート** &gt; **売上レポート** &gt; **上位の顧客レポート**</span><span class="sxs-lookup"><span data-stu-id="e8c2d-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="e8c2d-113">同様に、ユーザーは次の基準の一つに基づいて、組織階層のさまざまなレベルで上位製品 (10 ~ 100) の収益性を調査できます:</span><span class="sxs-lookup"><span data-stu-id="e8c2d-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e8c2d-114">売上金額</span><span class="sxs-lookup"><span data-stu-id="e8c2d-114">Sales amount</span></span>
- <span data-ttu-id="e8c2d-115">件数</span><span class="sxs-lookup"><span data-stu-id="e8c2d-115">Quantity</span></span>
- <span data-ttu-id="e8c2d-116">売上総利益率</span><span class="sxs-lookup"><span data-stu-id="e8c2d-116">Gross profit margin</span></span>
- <span data-ttu-id="e8c2d-117">利益幅の割合</span><span class="sxs-lookup"><span data-stu-id="e8c2d-117">Margin percentage</span></span>

<span data-ttu-id="e8c2d-118">この評価に関しては、次の場所のいずれかから開くことができる、**上位製品** レポートをすぐに使用できます:</span><span class="sxs-lookup"><span data-stu-id="e8c2d-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e8c2d-119">**店舗管理** ワークスペース &gt; **Retail と Commerce** &gt; **チャネル** &gt; **店舗管理** &gt; **レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="e8c2d-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e8c2d-120">**カテゴリと製品の管理** ワークスペース &gt; **Retail と Commerce** &gt; **製品とカテゴリ** &gt; **店舗管理** &gt; **レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="e8c2d-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e8c2d-121">**照会およびレポート** セクション &gt; **Retail と Commerce** &gt; **照会およびレポート** &gt; **売上レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="e8c2d-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
