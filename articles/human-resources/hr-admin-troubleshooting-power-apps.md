---
title: Power Apps 管理センターで環境を作成できない
description: この記事では、管理者が Microsoft Power Apps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113261"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="703b3-103">Power Apps 管理センターで環境を作成できない</span><span class="sxs-lookup"><span data-stu-id="703b3-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="703b3-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="703b3-104">**Issue**</span></span>

- <span data-ttu-id="703b3-105">テナント/環境の管理者が Microsoft Power Apps 管理者センターで環境を作成することができません。</span><span class="sxs-lookup"><span data-stu-id="703b3-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="703b3-106">ユーザーは、環境を作る権限を付与するライセンスを持っていません。</span><span class="sxs-lookup"><span data-stu-id="703b3-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="703b3-107">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="703b3-107">**Solution**</span></span>

<span data-ttu-id="703b3-108">テナント管理者が、環境を作成するユーザーに有効な Power Apps P2 ライセンスを割り当てている必要があります。</span><span class="sxs-lookup"><span data-stu-id="703b3-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="703b3-109">次の Microsoft Dynamics サービス 計画では、環境を作成するアクセス許可が提供されます。</span><span class="sxs-lookup"><span data-stu-id="703b3-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="703b3-110">全体の製品の最小管理単位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="703b3-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="703b3-111">Power Apps P2 サービス計画</span><span class="sxs-lookup"><span data-stu-id="703b3-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="703b3-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="703b3-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="703b3-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="703b3-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="703b3-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="703b3-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="703b3-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="703b3-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="703b3-116">さまざまな Microsoft Office SKU も、スタンドアロンの Power Apps プラン 2 SKU と一緒にこの権利を提供することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="703b3-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="703b3-117">重要な点は、これらの SKU のいずれかが必要であることです。</span><span class="sxs-lookup"><span data-stu-id="703b3-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="703b3-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) に移動します。</span><span class="sxs-lookup"><span data-stu-id="703b3-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="703b3-119">次の手順に従って、環境を作成します [人事管理のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。</span><span class="sxs-lookup"><span data-stu-id="703b3-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
