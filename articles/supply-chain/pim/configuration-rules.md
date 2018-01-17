---
title: "コンフィギュレーション ルール"
description: "この記事は、コンフィギュレーション ルールに関する一般情報を示します。 コンフィギュレーション ルールは、分析コード ベースのコンフィギュレーション テクノロジを使用する製品の部品表 (BOM) の品目間の関係を定義します。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 6dff0abbcc9cf4138dec58c11b59cb9b19d81ce3
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="configuration-rules"></a><span data-ttu-id="605eb-104">コンフィギュレーション ルール</span><span class="sxs-lookup"><span data-stu-id="605eb-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="605eb-105">この記事は、コンフィギュレーション ルールに関する一般情報を示します。</span><span class="sxs-lookup"><span data-stu-id="605eb-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="605eb-106">コンフィギュレーション ルールは、分析コード ベースのコンフィギュレーション テクノロジを使用する製品の部品表 (BOM) の品目間の関係を定義します。</span><span class="sxs-lookup"><span data-stu-id="605eb-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="605eb-107">コンフィギュレーション ルールは、分析コード ベースのコンフィギュレーション モデルを定義する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="605eb-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="605eb-108">コンフィギュレーション ルールは、部品表 (BOM) で特定の品目の組み合わせを許可または禁止する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="605eb-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="605eb-109">BOM が作成され、関連する品目をそれぞれのコンフィギュレーション グループに割り当てた後、1 つ以上のコンフィギュレーション ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="605eb-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="605eb-110">2 つの品目が一緒に含まれる場合、**選択**オペレータを使用して、正しく含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="605eb-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="605eb-111">2 つの品目が相互に排他的な場合、**選択解除**オペレータを使用して排他されるようにします。</span><span class="sxs-lookup"><span data-stu-id="605eb-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="605eb-112">**注意:** この情報は、分析コード ベースのコンフィギュレーション テクノロジを使用する製品マスターにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="605eb-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="605eb-113">既存のコンフィギュレーションは、その後発生するコンフィギュレーション ルールに対する変更によって、影響を受けることはありません。</span><span class="sxs-lookup"><span data-stu-id="605eb-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="605eb-114">ただし、新しいコンフィギュレーションを定義する前にルールを設定し、ルールが変更されたと考えられる場合にルールを確認することは、重要なことです。</span><span class="sxs-lookup"><span data-stu-id="605eb-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="605eb-115">**注意:** **選択**メソッドでは、派生するコンフィギュレーション グループ、品目番号、およびコンフィギュレーションが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="605eb-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="605eb-116">**選択解除**メソッドでは、派生するコンフィギュレーション グループ、品目番号、およびコンフィギュレーションを選択できません。</span><span class="sxs-lookup"><span data-stu-id="605eb-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="605eb-117">参照</span><span class="sxs-lookup"><span data-stu-id="605eb-117">See also</span></span>
--------

[<span data-ttu-id="605eb-118">分析コード ベースの製品コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="605eb-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




