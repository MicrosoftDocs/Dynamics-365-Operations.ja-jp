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
ms.openlocfilehash: e0589748247cf9195116687cf70228b4ef36e29b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211549"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="e14ad-103">顧客と製品の収益性の評価</span><span class="sxs-lookup"><span data-stu-id="e14ad-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e14ad-104">この記事では、アクセスしたり、参照したり、Dynamics 365 Commerce データから顧客と製品の収益性についての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e14ad-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="e14ad-105">Commerce の一部として、ユーザーは、次の基準の 1 つに基づいて、組織階層のさまざまなレベルで上位顧客 (10 ～ 100) の収益性を調査できます。</span><span class="sxs-lookup"><span data-stu-id="e14ad-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e14ad-106">売上金額</span><span class="sxs-lookup"><span data-stu-id="e14ad-106">Sales amount</span></span>
- <span data-ttu-id="e14ad-107">件数</span><span class="sxs-lookup"><span data-stu-id="e14ad-107">Quantity</span></span>
- <span data-ttu-id="e14ad-108">売上総利益率</span><span class="sxs-lookup"><span data-stu-id="e14ad-108">Gross profit margin</span></span>
- <span data-ttu-id="e14ad-109">利益幅の割合</span><span class="sxs-lookup"><span data-stu-id="e14ad-109">Margin percentage</span></span>

<span data-ttu-id="e14ad-110">この評価に関しては、次の場所のいずれかから開くことができる、**上位の顧客** レポートをすぐに使用できます:</span><span class="sxs-lookup"><span data-stu-id="e14ad-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e14ad-111">**店舗管理** ワークスペース &gt; **Retail と Commerce** &gt; **チャネル** &gt; **店舗管理** &gt; **レポート** &gt; **上位の顧客レポート**</span><span class="sxs-lookup"><span data-stu-id="e14ad-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="e14ad-112">**照会およびレポート** セクション &gt; **Retail と Commerce** &gt; **照会およびレポート** &gt; **売上レポート** &gt; **上位の顧客レポート**</span><span class="sxs-lookup"><span data-stu-id="e14ad-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="e14ad-113">同様に、ユーザーは次の基準の一つに基づいて、組織階層のさまざまなレベルで上位製品 (10 ~ 100) の収益性を調査できます:</span><span class="sxs-lookup"><span data-stu-id="e14ad-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e14ad-114">売上金額</span><span class="sxs-lookup"><span data-stu-id="e14ad-114">Sales amount</span></span>
- <span data-ttu-id="e14ad-115">件数</span><span class="sxs-lookup"><span data-stu-id="e14ad-115">Quantity</span></span>
- <span data-ttu-id="e14ad-116">売上総利益率</span><span class="sxs-lookup"><span data-stu-id="e14ad-116">Gross profit margin</span></span>
- <span data-ttu-id="e14ad-117">利益幅の割合</span><span class="sxs-lookup"><span data-stu-id="e14ad-117">Margin percentage</span></span>

<span data-ttu-id="e14ad-118">この評価に関しては、次の場所のいずれかから開くことができる、**上位製品** レポートをすぐに使用できます:</span><span class="sxs-lookup"><span data-stu-id="e14ad-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e14ad-119">**店舗管理** ワークスペース &gt; **Retail と Commerce** &gt; **チャネル** &gt; **店舗管理** &gt; **レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="e14ad-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e14ad-120">**カテゴリと製品の管理** ワークスペース &gt; **Retail と Commerce** &gt; **製品とカテゴリ** &gt; **店舗管理** &gt; **レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="e14ad-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e14ad-121">**照会およびレポート** セクション &gt; **Retail と Commerce** &gt; **照会およびレポート** &gt; **売上レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="e14ad-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]