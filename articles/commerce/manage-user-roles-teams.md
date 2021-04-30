---
title: Microsoft Teams でユーザーとロールを管理する
description: このトピックでは、Microsoft Dynamics 365 Commerce のユーザーロールを Microsoft Teams で管理する方法を説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 53cdd1966e76dfcfc427e73520a680a610667617
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908809"
---
# <a name="manage-user-roles-in-microsoft-teams"></a><span data-ttu-id="5a4ad-103">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="5a4ad-103">Manage user roles in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a4ad-104">このトピックでは、Microsoft Dynamics 365 Commerce のユーザーロールを Microsoft Teams で管理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-104">This topic describes how to manage Microsoft Dynamics 365 Commerce user roles in Microsoft Teams.</span></span>

<span data-ttu-id="5a4ad-105">Teams 内の各店舗またはチャネルに対してチームを作成する場合は、そのチームに対応するグループのメンバー数 (たとえば、`HOUSTON_D365@<YourTenantAzureADDomain>.com`)。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-105">As you create a team for each store or channel in Teams, a group membership that corresponds to the team is created (for example, `HOUSTON_D365@<YourTenantAzureADDomain>.com`).</span></span> <span data-ttu-id="5a4ad-106">チーム グループのメンバーとなっているすべての店舗の従業員には、**オーナー** または **メンバー** 2つのユーザー ロールのうちの1つが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-106">All the store workers under a team group membership are assigned one of two user roles: **Owner** or **Member**.</span></span> <span data-ttu-id="5a4ad-107">**所有者** のユーザー ロールを持つ店舗の従業員は、プライベート チャンネルの追加、メンバーの追加または削除などの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-107">Store employees who have the **Owner** user role can perform operations such as adding a private channel, and adding or deleting members.</span></span> <span data-ttu-id="5a4ad-108">通常、店長は **所有者** のユーザー ロールを持っています。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-108">Typically, store managers have the **Owner** user role.</span></span>

<span data-ttu-id="5a4ad-109">次の図は、チーム メンバーの一覧と、Microsoft Teams 管理センターでのユーザー ロールの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-109">The following illustration shows an example of a list of team members and their user roles in the Microsoft Teams admin center.</span></span>

![Microsoft Teams 管理センターのチーム メンバーとユーザー ロール](media/d365-commerce-teams-integration-user-roles.png)

<span data-ttu-id="5a4ad-111">詳細については、[Microsoft Teams におけるチームの所有者とメンバーの割り当て](https://docs.microsoft.com/microsoftteams/assign-roles-permissions)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a4ad-111">For more information, see [Assign team owners and members in Microsoft Teams](https://docs.microsoft.com/microsoftteams/assign-roles-permissions).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a4ad-112">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5a4ad-112">Additional resources</span></span>

[<span data-ttu-id="5a4ad-113">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="5a4ad-113">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="5a4ad-114">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="5a4ad-114">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="5a4ad-115">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="5a4ad-115">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="5a4ad-116">Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="5a4ad-116">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="5a4ad-117">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="5a4ad-117">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="5a4ad-118">Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="5a4ad-118">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
