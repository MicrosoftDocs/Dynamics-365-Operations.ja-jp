---
title: PowerApps 管理者センターで環境を作成することができない
description: このトピックでは、管理者が Microsoft PowerApps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305213"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a><span data-ttu-id="8deb8-103">PowerApps 管理センターで環境を作成できない</span><span class="sxs-lookup"><span data-stu-id="8deb8-103">Can't create an environment in the PowerApps Admin center</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8deb8-104">**払出**</span><span class="sxs-lookup"><span data-stu-id="8deb8-104">**Issue**</span></span>

- <span data-ttu-id="8deb8-105">テナント/環境の管理者が Microsoft PowerApps 管理者センターで環境を作成することができません。</span><span class="sxs-lookup"><span data-stu-id="8deb8-105">The tenant/environment admin can't create an environment in the Microsoft PowerApps Admin center.</span></span>
- <span data-ttu-id="8deb8-106">環境の作成手順を実行する権限をユーザーに提供するライセンスは、その手順を実行しているユーザーに直接割り当てられていません。</span><span class="sxs-lookup"><span data-stu-id="8deb8-106">A licence that gives users the right to perform the environment creation step hasn't been assigned directly to the user who is performing that step.</span></span>

<span data-ttu-id="8deb8-107">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="8deb8-107">**Solution**</span></span>

<span data-ttu-id="8deb8-108">テナント管理者が、環境の作成手順を実行するユーザーに、有効な PowerApps P2 ライセンスを直接割り当てていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8deb8-108">Make sure that the tenant admin has assigned a valid PowerApps P2 license directly to the user who will perform the environment creation step.</span></span> <span data-ttu-id="8deb8-109">その権限を提供する Microsoft Dynamics サービス プランは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="8deb8-109">Here are the Microsoft Dynamics service plans that provide that right.</span></span>

| <span data-ttu-id="8deb8-110">全体の最小在庫管理単位 (SKU)</span><span class="sxs-lookup"><span data-stu-id="8deb8-110">Overall product stock keeping unit (SKU)</span></span>       | <span data-ttu-id="8deb8-111">PowerApps P2 サービス計画</span><span class="sxs-lookup"><span data-stu-id="8deb8-111">PowerApps P2 service plan</span></span>  |
|------------------------------------------------|----------------------------|
| <span data-ttu-id="8deb8-112">Microsoft Dynamics 365 for Operations</span><span class="sxs-lookup"><span data-stu-id="8deb8-112">Microsoft Dynamics 365 for Operations</span></span>          | <span data-ttu-id="8deb8-113">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="8deb8-113">PowerApps for Dynamics 365</span></span> |
| <span data-ttu-id="8deb8-114">Microsoft Dynamics 365 Plan Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="8deb8-114">Microsoft Dynamics 365 Plan Enterprise Edition</span></span> | <span data-ttu-id="8deb8-115">PowerApps for Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="8deb8-115">PowerApps for Dynamics 365</span></span> |

<span data-ttu-id="8deb8-116">さまざまな Microsoft Office SKU も、スタンドアロンの PowerApps プラン 2 SKU と一緒にこの権利を提供することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8deb8-116">Note that various Microsoft Office SKUs also provide the right, together with standalone PowerApps Plan 2 SKUs.</span></span> <span data-ttu-id="8deb8-117">重要な点は、これらの SKU のいずれかが必要であることです。</span><span class="sxs-lookup"><span data-stu-id="8deb8-117">The important point is that one of these SKUs must be present.</span></span>

1. <span data-ttu-id="8deb8-118">[https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) に移動します。</span><span class="sxs-lookup"><span data-stu-id="8deb8-118">Go to [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).</span></span>
2. <span data-ttu-id="8deb8-119">次の手順に従って、環境を作成します [Talent のプロビジョニング](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)。</span><span class="sxs-lookup"><span data-stu-id="8deb8-119">Create the environments by following the instructions in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>
