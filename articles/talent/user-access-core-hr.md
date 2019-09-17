---
title: ユーザーは Core HR にアクセスできるが、Onboard または Attract アプリにはアクセスできない
description: このトピックでは、ユーザーが Microsoft Dynamics 365 for Talent Core HR にはアクセスできるが、Attract または Onboard アプリにはアクセスできない問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741723"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="6c288-103">ユーザーが Core HR にアクセスできるが、Onboard または Attract アプリにアクセスできない</span><span class="sxs-lookup"><span data-stu-id="6c288-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6c288-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="6c288-104">**Environment details**</span></span>

- <span data-ttu-id="6c288-105">Microsoft Dynamics Lifecycle Services (LCS) の配置がユーザー A によって実行されました。</span><span class="sxs-lookup"><span data-stu-id="6c288-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="6c288-106">ユーザー A は、Microsoft Dynamics 365 for Talent Core HR にユーザーとしてユーザー B を追加します。</span><span class="sxs-lookup"><span data-stu-id="6c288-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="6c288-107">**払出**</span><span class="sxs-lookup"><span data-stu-id="6c288-107">**Issue**</span></span>

<span data-ttu-id="6c288-108">ユーザー B は、Core HR にアクセスできますが、Talent に: Attract または Talent に: Onboard アプリにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="6c288-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="6c288-109">ユーザーが**エクスペリエンス アプリ**に移動しようとすると、代わりに試用環境に移動してしまいます。</span><span class="sxs-lookup"><span data-stu-id="6c288-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="6c288-110">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="6c288-110">**Solution**</span></span>

<span data-ttu-id="6c288-111">ユーザー B は、プロビジョニング プロセス中にユーザー A が作成した Microsoft PowerApps の環境を表示するための権限を割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c288-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="6c288-112">詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) の「環境へのアクセス許可の付与」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c288-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="6c288-113">**長期のソリューション**</span><span class="sxs-lookup"><span data-stu-id="6c288-113">**Long-term solution**</span></span>

<span data-ttu-id="6c288-114">Microsoft は、ユーザーが Core HR に追加される際に Onboard および Attract に適切な権限を自動的に割り当てることを検討しています。</span><span class="sxs-lookup"><span data-stu-id="6c288-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
