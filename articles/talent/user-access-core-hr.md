---
title: ユーザーは人事管理にアクセスできるが、Onboard または Attract にアクセスできない
description: このトピックでは、ユーザーが Microsoft Dynamics 365 Talent - 人事管理にはアクセスできるが、Attract または Onboard にはアクセスできない問題を解決する方法について説明します。
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461740"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="5ef7f-103">ユーザーは人事管理にアクセスできるが、Onboard または Attract にアクセスできない</span><span class="sxs-lookup"><span data-stu-id="5ef7f-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ef7f-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="5ef7f-104">**Environment details**</span></span>

- <span data-ttu-id="5ef7f-105">Microsoft Dynamics Lifecycle Services (LCS) の配置がユーザー A によって実行されました。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="5ef7f-106">ユーザー A は、Microsoft Dynamics 365 Human Resources にユーザーとしてユーザー B を追加します。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5ef7f-107">**問題点**</span><span class="sxs-lookup"><span data-stu-id="5ef7f-107">**Issue**</span></span>

<span data-ttu-id="5ef7f-108">ユーザー B は人事管理にアクセスできますが、Talent: Attract または Talent: Onboard アプリにはアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="5ef7f-109">ユーザーが **エクスペリエンス アプリ** に移動しようとすると、代わりに試用環境に移動してしまいます。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="5ef7f-110">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="5ef7f-110">**Solution**</span></span>

<span data-ttu-id="5ef7f-111">ユーザー B は、プロビジョニング プロセス中にユーザー A が作成した Microsoft Power Apps の環境を表示するための権限を割り当てられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="5ef7f-112">詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) の「環境へのアクセス許可の付与」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="5ef7f-113">**長期のソリューション**</span><span class="sxs-lookup"><span data-stu-id="5ef7f-113">**Long-term solution**</span></span>

<span data-ttu-id="5ef7f-114">Microsoft は、ユーザーが人事管理に追加される際に Onboard および Attract に適切な権限を自動的に割り当てることを検討しています。</span><span class="sxs-lookup"><span data-stu-id="5ef7f-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
