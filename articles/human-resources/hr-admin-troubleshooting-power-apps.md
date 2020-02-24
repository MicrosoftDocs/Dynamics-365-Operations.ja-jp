---
title: Power Apps 管理センターで環境を作成できない
description: この記事では、管理者が Microsoft Power Apps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: f4c75706183a3d6c961852395e464d46ba3ec1f2
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009642"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a><span data-ttu-id="eb929-103">Power Apps 管理センターで環境を作成できない</span><span class="sxs-lookup"><span data-stu-id="eb929-103">Can't create an environment in the Power Apps Admin center</span></span>

<span data-ttu-id="eb929-104">**問題点**</span><span class="sxs-lookup"><span data-stu-id="eb929-104">**Issue**</span></span>

- <span data-ttu-id="eb929-105">テナント/環境の管理者が Microsoft Power Apps 管理者センターで環境を作成することができません。</span><span class="sxs-lookup"><span data-stu-id="eb929-105">The tenant/environment admin can't create an environment in the Microsoft Power Apps Admin center.</span></span>
- <span data-ttu-id="eb929-106">環境の作成手順を実行する権限をユーザーに提供するライセンスは、その手順を実行しているユーザーに直接割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="eb929-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="eb929-107">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="eb929-107">**Solution**</span></span>

<span data-ttu-id="eb929-108">テナント管理者が、環境の作成手順を実行するユーザーに、有効な Power Apps P2 ライセンスを直接割り当てていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eb929-108">Make sure that the tenant admin has assigned a valid Power Apps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="eb929-109">その権限を提供する Microsoft Dynamics サービス プランは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="eb929-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="eb929-110">全体の最小在庫管理単位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="eb929-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="eb929-111">Power Apps P2 サービス計画</span><span class="sxs-lookup"><span data-stu-id="eb929-111">Power Apps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="eb929-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="eb929-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="eb929-113">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="eb929-113">Power Apps for Dynamics 365</span></span> |
| <span data-ttu-id="eb929-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="eb929-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="eb929-115">Power Apps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="eb929-115">Power Apps for Dynamics 365</span></span> |

<span data-ttu-id="eb929-116">さまざまな Microsoft Office SKU も、スタンドアロンの Power Apps プラン 2 SKU と一緒にこの権利を提供することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eb929-116">Note that various Microsoft Office SKUs also provide the right, together with standalone Power Apps Plan 2 SKUs.</span></span> <span data-ttu-id="eb929-117">重要な点は、これらの SKU のいずれかが必要であることです。</span><span class="sxs-lookup"><span data-stu-id="eb929-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="eb929-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) に移動します。</span><span class="sxs-lookup"><span data-stu-id="eb929-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="eb929-119">次の手順に従って、環境を作成します [人事管理のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。</span><span class="sxs-lookup"><span data-stu-id="eb929-119">Create the environments by following the instructions in [Provision Human Resources](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
