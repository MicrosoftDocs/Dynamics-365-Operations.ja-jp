---
title: RCS/グローバル レポジトリの強化されたフィルター処理
description: このトピックでは、追加フィルターを含むように改善された RCS グローバル レポジトリの拡張フィルター処理機能について説明します。
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 1913b661c46af5e34da1a2939cb2a5d5b4e46411
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445062"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="42661-103">RCS では、RCS/グローバル リポジトリで構成を見つけるフィルタリング オプションを強化しました</span><span class="sxs-lookup"><span data-stu-id="42661-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42661-104">このトピックでは、次のフィルターを含むように改善された、Regulatory Configuration Services (RCS) グローバル レポジトリの拡張フィルター処理機能について説明します：</span><span class="sxs-lookup"><span data-stu-id="42661-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="42661-105">**国/地域** ― ISO 国コードに基づく</span><span class="sxs-lookup"><span data-stu-id="42661-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="42661-106">**タグ** 次のタイプ：</span><span class="sxs-lookup"><span data-stu-id="42661-106">**Tags** types for:</span></span>
  - <span data-ttu-id="42661-107">職務分野</span><span class="sxs-lookup"><span data-stu-id="42661-107">Functional area</span></span>
  - <span data-ttu-id="42661-108">機能領域</span><span class="sxs-lookup"><span data-stu-id="42661-108">Feature area</span></span>
  - <span data-ttu-id="42661-109">業界</span><span class="sxs-lookup"><span data-stu-id="42661-109">Industry</span></span> 
  - <span data-ttu-id="42661-110">ビジネス ドキュメント</span><span class="sxs-lookup"><span data-stu-id="42661-110">Business document</span></span> 

<span data-ttu-id="42661-111">特定の構成や関連する構成を見つけやすくするために、個別に、またはグループとしてフィルタを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="42661-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="42661-112">例えば、「仕入先請求書に関連する構成可能なビジネス文書」という単一のタイプの文書を検索するには、**ビジネス ドキュメント タイプ** のフィルタを適用することで、そのタイプの文書を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="42661-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="42661-113">[![グローバル レポジトリのフィルター セクション](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="42661-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="42661-114">[仕入先請求書] などのドキュメントタイプを選択し、**フィルターの適用** をクリックすることで、検索をさらに絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="42661-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="42661-115">次の例では、**ビジネス ドキュメント タイプ** でフィルター処理した場合の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="42661-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="42661-116">[![フィルターを適用してビジネス ドキュメント タイプをインポートする](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="42661-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="42661-117">フィルタ処理された結果は、個別に、またはセットとして、ユーザーの RCS リポジトリまたは Dynamics 365 Finance 環境にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="42661-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="42661-118">これを行うには、構成のグループを選択し、**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42661-118">To do this, select the group of configurations, and click **Import**.</span></span>
