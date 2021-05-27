---
title: Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング
description: ここでは、Microsoft Teams の組織データを利用して Dynamics 365 Commerce のプロビジョニングを行う方法について説明します。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1cb28fb50bdc972d1dae6d03a45f70a2f3a63357
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022449"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="a6bda-103">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="a6bda-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6bda-104">ここでは、Microsoft Teams の組織データを利用して Dynamics 365 Commerce のプロビジョニングを行う方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a6bda-105">Dynamics 365 Commerce では、まだ小売店舗にチームを設定していない場合に、簡単に Teams をプロビジョニングすることができます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="a6bda-106">Commerce から Teams で使用する情報を活用することで、店舗の従業員が Teams を使い始めることができるようになります。</span><span class="sxs-lookup"><span data-stu-id="a6bda-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="a6bda-107">この情報には、組織階層、店舗名、従業員情報、Azure Active Directory (Azure AD) 勘定などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="a6bda-108">Teams の準備のプロセスには、2つの主要な手順があります :</span><span class="sxs-lookup"><span data-stu-id="a6bda-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="a6bda-109">Teams では、小売店舗ごとにチームを作成し、店舗の従業員を適切なチームのメンバーとして追加します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="a6bda-110">従業員が複数の小売店に関連付けられている場合、その情報がチームのメンバーに反映されます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="a6bda-111">各地域のマネージャーをメンバーに加えたコミュニケーション チームを作り、Teams からのタスクの公開を容易にします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="a6bda-112">Commerc から Teams に組織階層をアップロードします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="a6bda-113">Commerce 本部で Teams をプロビジョンする</span><span class="sxs-lookup"><span data-stu-id="a6bda-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="a6bda-114">Microsoft Teams のプロビジョニングを行う前に、次の作業を行います :</span><span class="sxs-lookup"><span data-stu-id="a6bda-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="a6bda-115">すべての地域マネージャーがコミュニケーション マネージャーとなっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="a6bda-116">すべての店舗マネージャと従業員の Azure アカウントが Commerce 本部内のマネージャまたは従業員の作業者レコードに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="a6bda-117">Commerce 本部で Teams をプロビジョニングするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a6bda-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a6bda-118">**Retail と Commerce \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="a6bda-119">アクション ペインで、**チームのプロビジョニング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="a6bda-120">**チームの準備** という名前のバッチ ジョブが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="a6bda-121">**システム管理 \> 照会 \> バッチジョブ** に移動し、**Teams のプロビジョニング** の説明がある最新のジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="a6bda-122">このジョブの実行が終了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="a6bda-123">地域マネージャー、店舗マネージャー、店舗従業員のいずれもが Teams のライセンスに関連付けられていない場合、次のエラーメッセージが表示される場合があります : 「ユーザーの適用可能な Sku カテゴリの取得に失敗しました」</span><span class="sxs-lookup"><span data-stu-id="a6bda-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="a6bda-124">この問題を修正するには、アクション ペインの **チームとメンバーの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="a6bda-125">Teams 管理センターでTeams のプロビジョニングを検証する</span><span class="sxs-lookup"><span data-stu-id="a6bda-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="a6bda-126">Microsoft Teams 管理センターで Microsoft Teams のプロビジョニングを検証するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a6bda-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="a6bda-127">[Teams 管理センター](https://admin.teams.microsoft.com/)に移動し、eコマース テナントの管理者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="a6bda-128">左ナビゲーション ペインウで、**Teams** を選択して展開し、**チームの管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="a6bda-129">Commerce の小売店舗ごとにひとつのチームが作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="a6bda-130">チームを選択し、店舗従業員がメンバーとして追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="a6bda-131">左ナビゲーション ペインで **ユーザー** を選択し、すべての店舗のすべての店舗の従業員がユーザーとして追加されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="a6bda-132">次の図は、Teams 管理センターの **チームの管理** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="a6bda-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Teams 管理センターの [チームの管理] ページの例](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="a6bda-134">Commerce の組織階層を Teams にアップロードする</span><span class="sxs-lookup"><span data-stu-id="a6bda-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="a6bda-135">Commerce の組織階層を Microsoft Teams で使用すると、同じ階層構造を使用しているすべての店舗または選択した店舗にタスクを発行することができます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="a6bda-136">Commerce の組織階層を Teams にアップロードするには、以下の手順で行います。</span><span class="sxs-lookup"><span data-stu-id="a6bda-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="a6bda-137">Commerce 本部で、**Retail と Commerce \> チャネルの設定 \> Microsoft Teams 統合の構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="a6bda-138">**対象の階層をダウンロード** を選択し、**地域別の小売店舗** を選択して組織階層のコンマ区切り値 (CSV) ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="a6bda-139">[Microsoft Teams PowerShell のインストール](/microsoftteams/teams-powershell-install)に記載の手順に従って、Microsoft Teams PowerShell モジュールをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="a6bda-140">Teams の PowerShell ウィンドウでプロンプト ウィンドウが表示された場合は、ご利用の Azure AD テナントの管理者アカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="a6bda-141">[チームが対象とする階層を設定する](/microsoftteams/set-up-your-team-hierarchy) に記載の手順に従って、対象の階層に CSV ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-141">Follow the steps in [Set up your team targeting hierarchy](/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="a6bda-142">組織階層が Teams にアップロードされたことを確認する</span><span class="sxs-lookup"><span data-stu-id="a6bda-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="a6bda-143">Microsoft Teams に組織階層がアップロードされたことを確認するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a6bda-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="a6bda-144">Teams は通信マネージャーとしてサインインします。</span><span class="sxs-lookup"><span data-stu-id="a6bda-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="a6bda-145">左のナビゲーション ペインで、**Planner によるタスク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="a6bda-146">**公開済 リスト** タブで、ダミーのタスクを含む新しいリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="a6bda-147">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a6bda-147">Select **Publish**.</span></span> <span data-ttu-id="a6bda-148">次の図の例のように、**公開対象者** ダイアログ ボックスに組織階層が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6bda-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![公開対象者のダイアログボックスに表示される組織階層の例](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="a6bda-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a6bda-150">Additional resources</span></span>

[<span data-ttu-id="a6bda-151">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="a6bda-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="a6bda-152">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="a6bda-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="a6bda-153">Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="a6bda-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="a6bda-154">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="a6bda-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="a6bda-155">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="a6bda-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="a6bda-156">Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="a6bda-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)