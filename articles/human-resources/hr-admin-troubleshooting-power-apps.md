---
title: Power Apps 管理センターで環境を作成できない
description: この記事では、管理者が Microsoft Power Apps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f1a086f1b710de9bad898abc740286c174ae3be7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797988"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="68357-103">Power Apps 管理センターで環境を作成できない</span><span class="sxs-lookup"><span data-stu-id="68357-103">Can't create an environment in the Power Apps Admin center</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="68357-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="68357-104">**Issue**</span></span>

- <span data-ttu-id="68357-105">テナント/環境の管理者が Microsoft Power Apps 管理者センターで環境を作成することができません。</span><span class="sxs-lookup"><span data-stu-id="68357-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="68357-106">ユーザーは、環境を作る権限を付与するライセンスを持っていません。</span><span class="sxs-lookup"><span data-stu-id="68357-106">The user doesn't have a license that gives the right to create environments.</span></span>

<span data-ttu-id="68357-107">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="68357-107">**Solution**</span></span>

<span data-ttu-id="68357-108">テナント管理者が、環境を作成するユーザーに有効な Power Apps P2 ライセンスを割り当てている必要があります。</span><span class="sxs-lookup"><span data-stu-id="68357-108">Make sure the tenant admin has assigned a valid Power Apps P2 license to the user creating the environment.</span></span> <span data-ttu-id="68357-109">次の Microsoft Dynamics サービス 計画では、環境を作成するアクセス許可が提供されます。</span><span class="sxs-lookup"><span data-stu-id="68357-109">The following Microsoft Dynamics service plans provide permissions to create environments:</span></span>

| <span data-ttu-id="68357-110">全体の製品の最小管理単位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="68357-110">Overall product stockkeeping unit (SKU)</span></span>       | <span data-ttu-id="68357-111">Power Apps P2 サービス計画</span><span class="sxs-lookup"><span data-stu-id="68357-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="68357-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="68357-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="68357-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="68357-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="68357-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="68357-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="68357-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="68357-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="68357-116">さまざまな Microsoft Office SKU も、スタンドアロンの Power Apps プラン 2 SKU と一緒にこの権利を提供することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="68357-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="68357-117">重要な点は、これらの SKU のいずれかが必要であることです。</span><span class="sxs-lookup"><span data-stu-id="68357-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="68357-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) に移動します。</span><span class="sxs-lookup"><span data-stu-id="68357-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="68357-119">次の手順に従って、環境を作成します [人事管理のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。</span><span class="sxs-lookup"><span data-stu-id="68357-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]