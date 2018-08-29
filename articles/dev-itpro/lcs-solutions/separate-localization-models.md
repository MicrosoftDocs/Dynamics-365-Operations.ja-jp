---
title: "ローカライズ モデルの分離"
description: "ローカライズおよび翻訳向け LCS ソリューションの要件の一部として、以前のバージョンの Microsoft Dynamics 365 for Finance and Operations のローカライズ ソリューションに、規制と競合の両方の機能が含まれている場合、ローカライズ ISV ソリューション プロバイダーはソリューションを各機能タイプごとに別々のモデルに分割する必要があります。 この記事では、この要件に関する情報を提供します。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: shylaw
ms.search.scope: Operations
ms.custom: 27561
ms.assetid: 49b634ab-d7f7-4e34-a7e9-7350548bf1a0
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b94a8eb9ee319286dc203201611b3f5151f24f53
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="separation-of-localization-models"></a><span data-ttu-id="55641-104">ローカライズ モデルの分離</span><span class="sxs-lookup"><span data-stu-id="55641-104">Separation of localization models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="55641-105">ローカライズおよび翻訳向け LCS ソリューションの要件の一部として、以前のバージョンの Microsoft Dynamics 365 for Finance and Operations のローカライズ ソリューションに、規制と競合の両方の機能が含まれている場合、ローカライズ ISV ソリューション プロバイダーはソリューションを各機能タイプごとに別々のモデルに分割する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55641-105">As part of the requirements for LCS solutions for localization and translation, if a localization solution for previous versions of Microsoft Dynamics 365 for Finance and Operations contains both regulatory and competitive features, localization ISV solution providers must split the solution into separate models for each feature type.</span></span> <span data-ttu-id="55641-106">この記事では、この要件に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="55641-106">This article provides information about this requirement.</span></span>

<span data-ttu-id="55641-107">多国籍の顧客は、Finance and Operations を配置するすべての国/地域で法的な要求事項を遵守する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55641-107">Multinational customers must comply with regulatory requirements in all countries/regions where they deploy Finance and Operations.</span></span> <span data-ttu-id="55641-108">同時に顧客はコード メンテナンスのコストを最小限に抑えたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="55641-108">At the same time, these customers want to minimize the cost of code maintenance.</span></span> <span data-ttu-id="55641-109">したがって、以前のバージョンの Finance and Operations のローカリゼーション ソリューションに規制機能と競合機能の両方が含まれている場合、顧客が必要とする機能を採用して展開できるように、ソリューションを別々のモデルに分割する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55641-109">Therefore, if a localization solution for previous versions of Finance and Operations contains both regulatory and competitive features, the solution must be split into separate models, so that customers can adopt and deploy the features that they require.</span></span> <span data-ttu-id="55641-110">アプリケーション ファンデーションおよび Finance and Operations スタックのアプリケーション スイートを複数のモデルに分割する努力がなされています。</span><span class="sxs-lookup"><span data-stu-id="55641-110">An effort has been made to split the Application foundation and Application suite of the Finance and Operations stack into multiple models.</span></span> 

<span data-ttu-id="55641-111">時間の経過とともにモデルの数は増加すると予想されます。</span><span class="sxs-lookup"><span data-stu-id="55641-111">The number of models is expected to grow over time.</span></span> <span data-ttu-id="55641-112">モノシリック コード ベースを分割すると、スケーラビリティ、管理性、および保守性の向上など、多くの利点が提供されます。</span><span class="sxs-lookup"><span data-stu-id="55641-112">Splitting a monolithic code base provides many benefits, such as better scalability, manageability, and serviceability.</span></span> <span data-ttu-id="55641-113">ローカライズ ソリューションをより詳細なモデルに分割するためのローカライズ要件は、この作業に基づいています。</span><span class="sxs-lookup"><span data-stu-id="55641-113">The localization requirement to split a localization solution into more granular models builds on this effort.</span></span> <span data-ttu-id="55641-114">目標は、Finance and Operations の多国籍の顧客に同じ利益を提供することです。</span><span class="sxs-lookup"><span data-stu-id="55641-114">The goal is to provide the same benefits to multinational customers of Finance and Operations.</span></span> 

<span data-ttu-id="55641-115">機能を規制または競争のいずれかに分類した後、[ローカライズ機能の分類](classify-localization-features.md) で説明せれているように、これらの機能のコードを少なくとも 2 つのモデルに分割し、1 つのモデルは規制機能のため、また少なくとも 1 つのモデルは競合機能となります。</span><span class="sxs-lookup"><span data-stu-id="55641-115">After you've classified features as either regulatory or competitive, as described in [Classify localization features](classify-localization-features.md), split the code for these features into at least two models, one model for the regulatory features and at least one model for the competitive features.</span></span> <span data-ttu-id="55641-116">競合機能をさらに分割することができる場合 (たとえば、小売に関連する機能や固定資産に関連する機能など)、分割することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="55641-116">If the competitive features can be split further (for example, into features that are related to Retail and features that are related to Fixed assets), it's a good idea to split them.</span></span> <span data-ttu-id="55641-117">ただし、さらに分割する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="55641-117">However, further splitting isn't mandatory.</span></span> <span data-ttu-id="55641-118">Finance and Operations のスタックを複数のモデルに分割する方法の詳細については、[モデルの分割を理解する](../dev-tools/model-split.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="55641-118">For more information about how to split the Finance and Operations stack into multiple models, see [Understanding the model split](../dev-tools/model-split.md).</span></span>




