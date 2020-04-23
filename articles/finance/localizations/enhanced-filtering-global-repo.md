---
title: RCS/グローバル レポジトリの拡張フィルター処理
description: このトピックでは、追加フィルターを含むように改善された RCS グローバル レポジトリの拡張フィルター処理機能について説明します。
author: JaneA07
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: 1adbd690795139778dc77a574e9d5f91a4bdeb3c
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249168"
---
# <a name="enhanced-filtering-options-for-finding-configurations-in-the-global-repository"></a><span data-ttu-id="51e53-103">グローバル レポジトリのコンフィギュレーション検索のための拡張フィルター処理オプション</span><span class="sxs-lookup"><span data-stu-id="51e53-103">Enhanced filtering options for finding configurations in the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51e53-104">このトピックでは、次のフィルターを含むように改善された、Regulatory Configuration Services (RCS) グローバル レポジトリの拡張フィルター処理機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="51e53-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the following filters:</span></span> 
- <span data-ttu-id="51e53-105">**国/地域** - ISO 国コードに基づく</span><span class="sxs-lookup"><span data-stu-id="51e53-105">**Country/region** - based on ISO country codes</span></span>  
- <span data-ttu-id="51e53-106">**タグ** - 機能/機能領域 ; 業種 ; ビジネス ドキュメント タイプ用</span><span class="sxs-lookup"><span data-stu-id="51e53-106">**Tags** - for functional/feature area; Industry; Business document type</span></span> 

<span data-ttu-id="51e53-107">個別にまたはグループ別のいずれかでフィルターを適用して、特定または関連するコンフィギュレーションを検索できます。</span><span class="sxs-lookup"><span data-stu-id="51e53-107">You can apply filters, either individually or in groups, to find specific or related configurations.</span></span> <span data-ttu-id="51e53-108">たとえば、仕入先請求書に関連したすべてのコンフィギュレーション可能なビジネス ドキュメントを検索するには、**ビジネス ドキュメント タイプ** フィルターを適用できます。</span><span class="sxs-lookup"><span data-stu-id="51e53-108">For example, to find all configurable business documents related to vendor invoices, you can apply the **Business document type** filter.</span></span> 

<span data-ttu-id="51e53-109">国コードを選択して、**フィルターを適用する**をクリックすることによってさらに絞り込んだ検索ができます。</span><span class="sxs-lookup"><span data-stu-id="51e53-109">You can further refine a search by selecting the country code and clicking **Apply filter**.</span></span>  

<span data-ttu-id="51e53-110">[![グローバル レポジトリのフィルター セクション](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="51e53-110">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="51e53-111">次の例では、**ビジネス ドキュメント タイプ**でフィルター処理した場合の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="51e53-111">The following example shows the results when filtering on **Business document type**.</span></span> 

<span data-ttu-id="51e53-112">[![フィルターを適用してビジネス ドキュメント タイプをインポートする](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="51e53-112">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="51e53-113">フィルター処理された結果は、ユーザー RCS または Dynamics 365 Finance 環境に、個別にまたは (コンフィギュレーションのグループを選択することによって) セットとして**インポート**をクリックしてインポートできます。</span><span class="sxs-lookup"><span data-stu-id="51e53-113">Filtered results can be imported into users RCS or Dynamics 365 Finance environment, either individually or as a set (by selecting the group of configurations) and clicking **Import**.</span></span>






