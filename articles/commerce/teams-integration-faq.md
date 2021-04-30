---
title: Dynamics 365 Commerce と Microsoft Teams の統合に関するよくあるご質問
description: このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams 統合に関連してよく寄せられる質問に対する回答を示します。
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
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908859"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="b6f8f-103">Dynamics 365 Commerce と Microsoft Teams の統合に関するよくあるご質問</span><span class="sxs-lookup"><span data-stu-id="b6f8f-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6f8f-104">このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams 統合に関連してよく寄せられる質問に対する回答を示します。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="b6f8f-105">Commerce から Teams を準備する間、店舗内でチームの所有者になるユーザーとは。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="b6f8f-106">すべての店長は対応するチーム グループに所有者として自動的に追加され、プライベート チャンネルの追加やメンバーの追加や削除などの操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="b6f8f-107">Commerce Headquarters で従業員に "通信マネージャ" ロールを割り当てるにはどのようにしますか。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="b6f8f-108">Microsoft Teams の通信マネージャは、タスク リストを作成および公開できます。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="b6f8f-109">通信マネージャになる必要がある組織の従業員には、Commerce Headquarters で "小売作業マネージャ" ロールが割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="b6f8f-110">Commerce Headquarters の従業員に小売作業マネージャ ロールを割り当てるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="b6f8f-111">**Retail と Commerce \> 従業員 \> ユーザー** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="b6f8f-112">従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-112">Select an employee.</span></span>
1. <span data-ttu-id="b6f8f-113">**ユーザーのロール** クイック タブで、**ロールの割り当て** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="b6f8f-114">**ユーザーへのロールの割り当て** ダイアログ ボックスで **Retail タスク マネージャー** ロールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="b6f8f-115">特定の組織階層を Microsoft Teams へアップロード可能にする方法は?</span><span class="sxs-lookup"><span data-stu-id="b6f8f-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="b6f8f-116">Commerce Headquarters では、すべての組織の階層を 1 つ以上の目的に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="b6f8f-117">次の例の図に示すように、Microsoft Teams にプロビジョニングする階層に **Retail レポート** 目的が関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Commerce Headquarters での組織階層の目的の例](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="b6f8f-119">小売用店舗の作業者が Azure Active Directory(Azure AD) を使用して販売時点管理 (POS) にログインするにはどのようにしますか 。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="b6f8f-120">Azure AD 認証を使用する Commerce POS のサインイン体験を構成する方法については、[POS サインインの Azure Active Directory 認証を有効にする](aad-pos-logon.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="b6f8f-121">Microsoft Teams の組織でチームを既に作成している場合、Commerce Headquarters で店舗と対応するチームをマップするにはどのようにしますか。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="b6f8f-122">既存のチームがある場合に店舗とチームをマップする方法については、[Microsoft Teams の組織に既存のチームがある場合の、店舗と対応するチームのマップ](map-stores-existing-teams.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="b6f8f-123">セッション 記憶域に保存されている Microsoft Graph API トークンをクリアする方法は?</span><span class="sxs-lookup"><span data-stu-id="b6f8f-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="b6f8f-124">Azure Active Directory (Azure AD) アカウントで販売時点管理 POS にログインしたユーザーは、POS からサインアウトするか、アプリケーションを閉じてセッション ストレージ記憶域をクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="b6f8f-125">推奨されるベスト プラクティスは、常に店舗作業員が POS ターミナルをロックするか、ターミナルを使用しない場合にセッションからサインアウトを行う方法です。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="b6f8f-126">店舗に店長がいない場合の方法は?</span><span class="sxs-lookup"><span data-stu-id="b6f8f-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="b6f8f-127">店舗にマネージャーが存在しない場合、チーム グループは、店舗または Teams に対して作成されません。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="b6f8f-128">店舗長が会社を離職した場合の問題は?</span><span class="sxs-lookup"><span data-stu-id="b6f8f-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="b6f8f-129">所有者ロールを持つユーザーは、Commerce Headquarters で新しい店舗マネージャを追加し、Teams を再プロビジョニングして、グループのチームで必要な権限を新しいマネージャに与えすることができます。</span><span class="sxs-lookup"><span data-stu-id="b6f8f-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="b6f8f-130">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b6f8f-130">Additional resources</span></span>

[<span data-ttu-id="b6f8f-131">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="b6f8f-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="b6f8f-132">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="b6f8f-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="b6f8f-133">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="b6f8f-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="b6f8f-134">Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="b6f8f-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="b6f8f-135">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="b6f8f-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="b6f8f-136">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="b6f8f-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
