---
title: "顧客と製品の収益性の評価"
description: "この記事では、アクセスしたり、参照したり、Microsoft Dynamics 365 for Retail データから顧客と製品の収益性についての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.contentlocale: ja-jp
ms.lasthandoff: 01/04/2019

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="528ca-103">顧客と製品の収益性の評価</span><span class="sxs-lookup"><span data-stu-id="528ca-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="528ca-104">この記事では、アクセスしたり、参照したり、Microsoft Dynamics 365 for Retail データから顧客と製品の収益性についての理解を深めるために、メモリ内およびリアルタイム分析を使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="528ca-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="528ca-105">Dynamics 365 for Retail の一部として、ユーザーは、次の基準の 1 つに基づいて、組織階層のさまざまなレベルで上位顧客 (10 ～ 100) の収益性を調査できます。</span><span class="sxs-lookup"><span data-stu-id="528ca-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="528ca-106">売上金額</span><span class="sxs-lookup"><span data-stu-id="528ca-106">Sales amount</span></span>
- <span data-ttu-id="528ca-107">件数</span><span class="sxs-lookup"><span data-stu-id="528ca-107">Quantity</span></span>
- <span data-ttu-id="528ca-108">売上総利益率</span><span class="sxs-lookup"><span data-stu-id="528ca-108">Gross profit margin</span></span>
- <span data-ttu-id="528ca-109">利益幅の割合</span><span class="sxs-lookup"><span data-stu-id="528ca-109">Margin percentage</span></span>

<span data-ttu-id="528ca-110">この評価に関しては、次の場所のいずれかから開くことができる、**上位の顧客**レポートをすぐに使用できます:</span><span class="sxs-lookup"><span data-stu-id="528ca-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="528ca-111">[小売店舗管理] ワークスペース &gt; [小売] &gt; [チャンネル] &gt; [小売店舗管理] &gt; [レポート] &gt; [上位の顧客レポート]</span><span class="sxs-lookup"><span data-stu-id="528ca-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="528ca-112">[照会とレポート] セクション &gt; [小売] &gt; [照会とレポート] &gt; [売上レポート] &gt; [上位の顧客レポート]</span><span class="sxs-lookup"><span data-stu-id="528ca-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="528ca-113">同様に、ユーザーは次の基準の一つに基づいて、組織階層のさまざまなレベルで上位製品 (10 ~ 100) の収益性を調査できます:</span><span class="sxs-lookup"><span data-stu-id="528ca-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="528ca-114">売上金額</span><span class="sxs-lookup"><span data-stu-id="528ca-114">Sales amount</span></span>
- <span data-ttu-id="528ca-115">件数</span><span class="sxs-lookup"><span data-stu-id="528ca-115">Quantity</span></span>
- <span data-ttu-id="528ca-116">売上総利益率</span><span class="sxs-lookup"><span data-stu-id="528ca-116">Gross profit margin</span></span>
- <span data-ttu-id="528ca-117">利益幅の割合</span><span class="sxs-lookup"><span data-stu-id="528ca-117">Margin percentage</span></span>

<span data-ttu-id="528ca-118">この評価に関しては、次の場所のいずれかから開くことができる、[上位製品] レポートをすぐに使用できます:</span><span class="sxs-lookup"><span data-stu-id="528ca-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="528ca-119">[小売店舗管理] ワークスペース &gt; [小売] &gt; [チャンネル] &gt; [小売店舗管理] &gt; [レポート] &gt; [上位製品レポート]</span><span class="sxs-lookup"><span data-stu-id="528ca-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="528ca-120">[カテゴリと製品の管理] ワークスペース &gt; **小売** &gt; **製品とカテゴリ** &gt; **小売店舗の管理** &gt; **レポート** &gt; **上位製品レポート**</span><span class="sxs-lookup"><span data-stu-id="528ca-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="528ca-121">[照会とレポート] セクション &gt; [小売] &gt; [照会とレポート] &gt; [売上レポート] &gt; [上位製品レポート]</span><span class="sxs-lookup"><span data-stu-id="528ca-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>

