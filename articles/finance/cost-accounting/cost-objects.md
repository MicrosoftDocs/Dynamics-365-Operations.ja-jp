---
title: 原価オブジェクト分析コード
description: 原価を分析する際、原価要素分析コードを使用して、原価がどこに流れるかを決定します。 原価オブジェクト分析コードを使用して、原価を割り当てる場所を決定します。 このトピックでは、原価オブジェクト分析コードについて説明します。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimensionMember, CAMCostObject
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a090ecae2aadf1d0e08dd6127f831abdbf4a6b0a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976430"
---
# <a name="cost-object-dimensions"></a><span data-ttu-id="7e271-105">原価オブジェクト分析コード</span><span class="sxs-lookup"><span data-stu-id="7e271-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e271-106">原価を分析する際、原価要素分析コードを使用して、原価がどこに流れるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="7e271-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="7e271-107">原価オブジェクト分析コードを使用して、原価を割り当てる場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="7e271-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="7e271-108">このトピックでは、原価オブジェクト分析コードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7e271-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="7e271-109">原価オブジェクトは、見積、原価の割り当て、または直接測定するオブジェクトのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="7e271-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="7e271-110">標準的な原価のオブジェクトには、製品、プロジェクト、リソース、部門、原価部門、および地理的領域が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7e271-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="7e271-111">管理は、原価を定量化するのに原価オブジェクトを使用し、収益性分析を推進します。</span><span class="sxs-lookup"><span data-stu-id="7e271-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="7e271-112">原価オブジェクト分析コードと原価オブジェクト分析コード メンバー</span><span class="sxs-lookup"><span data-stu-id="7e271-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="7e271-113">原価オブジェクトは、*原価オブジェクト分析コード*として知られています。</span><span class="sxs-lookup"><span data-stu-id="7e271-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="7e271-114">原価オブジェクト分析コードが参照するエンティティを決定した後、個々の分析コード値を指定するか、またはそれらを他のソース システムから原価オブジェクトにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e271-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="7e271-115">これらの個別の分析コード値は*原価オブジェクト分析コード メンバ*と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="7e271-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="7e271-116">たとえば、原価オブジェクト分析コードとして原価部門として知られる財務分析コードを使用するとします。</span><span class="sxs-lookup"><span data-stu-id="7e271-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="7e271-117">個々の原価部門にどのように原価が流れるかを確認するには、原価オブジェクト分析コード メンバをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e271-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="7e271-118">この場合、原価オブジェクト分析コード メンバは、販売、生産、管理、地理的な場所などの実際の原価部門です。</span><span class="sxs-lookup"><span data-stu-id="7e271-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="7e271-119">次のスクリーン ショットは、原価オブジェクト分析コード メンバーとしての実際の原価部門である原価オブジェクト分析コードとしての原価部門の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="7e271-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="7e271-120">[![原価オブジェクト分析コードとして原価部門を表示するスクリーンショット](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="7e271-120">[![Screenshot showing Cost Centers as cost object dimension](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="7e271-121">データ コネクタを使用して原価オブジェクト分析コード メンバーをインポートする</span><span class="sxs-lookup"><span data-stu-id="7e271-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="7e271-122">原価オブジェクト分析コードメンバーのインポートを容易にするために、データ コネクタを使用して、原価オブジェクト分析コードとして使用するエンティティから値を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e271-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="7e271-123">ビルド済のデータ コネクタ、または構築するカスタム データ コネクタを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e271-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>



