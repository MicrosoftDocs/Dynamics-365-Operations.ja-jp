---
title: Dynamics 365 Commerce と Microsoft Teams の統合を有効化する
description: このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams の統合を有効化する方法について説明します。
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
ms.openlocfilehash: eb0b8b419b302fbd0bc107bca22f8b26774ba3c7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019838"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="970b1-103">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="970b1-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="970b1-104">このトピックでは、Microsoft Dynamics 365 Commerce と Microsoft Teams の統合を有効化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="970b1-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="970b1-105">Teams に Dynamics 365 Commerce からの情報を提供し、Teams と 販売時点管理 (POS) のアプリケーション間でタスク管理機能を同期させるには、Commerce 本部で統合機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="970b1-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="970b1-106">Teams の 統合を有効にした場合、Teams とデータを共有することに同意することになります。</span><span class="sxs-lookup"><span data-stu-id="970b1-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="970b1-107">Teams と共有するデータは、ご利用の Commerce データとは異なる国に存在する可能性があり、また、異なるコンプライアンス基準の対象となる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="970b1-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="970b1-108">詳細については、[Microsoft トラストセンター](https://www.microsoft.com/trust-center) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="970b1-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="970b1-109">マイクロソフトのプライバシー ポリシーについては、 [Microsoft プライバシー ステートメント](https://aka.ms/privacy)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="970b1-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="970b1-110">Teams との統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="970b1-110">Enable Teams integration</span></span>

<span data-ttu-id="970b1-111">Microsoft Teams と Commerce との統合を有効にする前に、Azure ポータルで Teams アプリケーションをテナントに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="970b1-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="970b1-112">Azure ポータルで Teams アプリケーションをテナントに登録するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="970b1-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="970b1-113">[クイック スタート : Microsoft IDプラットフォームにアプリを登録する](/azure/active-directory/develop/quickstart-register-app) に記載の手順に従い、Azure ポータルで Teams アプリケーションをテナントに登録します。</span><span class="sxs-lookup"><span data-stu-id="970b1-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="970b1-114">登録されたアプリケーションの **概要** ページから **アプリケーション (クライアント) ID** 値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="970b1-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="970b1-115">この値は、Commerce 本部で Teams を有効にするために使用します。</span><span class="sxs-lookup"><span data-stu-id="970b1-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="970b1-116">手順 1 で[証明書を追加](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)した際に入力した証明書の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="970b1-116">Copy the certificate value that was entered when you [added a certificate](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="970b1-117">証明書は、公開鍵やアプリケーション キーとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="970b1-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="970b1-118">この値は、Commerce 本部で Teams を有効にするために使用します。</span><span class="sxs-lookup"><span data-stu-id="970b1-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="970b1-119">Commerce 本部で Teams の統合を有効にするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="970b1-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="970b1-120">**Retail と Commerce \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="970b1-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="970b1-121">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="970b1-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="970b1-122">**有効化 Microsoft Teams 統合** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="970b1-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="970b1-123">**アプリケーション ID** と **アプリケーション キー** の各フィールドで、Azure ポータルで Teams アプリケーションを登録した際に取得した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970b1-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="970b1-124">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="970b1-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="970b1-125">次の図は、Commerce 本部での Teams 統合の設定例です。</span><span class="sxs-lookup"><span data-stu-id="970b1-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![Commerce 本部の Teams 統合構成](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="970b1-127">Teams との統合を無効化する</span><span class="sxs-lookup"><span data-stu-id="970b1-127">Disable Teams integration</span></span>

<span data-ttu-id="970b1-128">Commerce 本部で Microsoft Teams の統合を無効にするには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="970b1-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="970b1-129">**Retail と Commerce \> チャネル設定 \> Microsoft Teams 統合の構成** に移動します。</span><span class="sxs-lookup"><span data-stu-id="970b1-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="970b1-130">アクション ウィンドウで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="970b1-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="970b1-131">**有効化 Microsoft Teams 統合** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="970b1-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="970b1-132">**アプリケーションID** フィールドと **アプリケーション キー** フィールドから値をクリアします。</span><span class="sxs-lookup"><span data-stu-id="970b1-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="970b1-133">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="970b1-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="970b1-134">Commerce と Teams の統合を無効にすると、POS 端末には Teams アプリケーションから発行されたタスクが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="970b1-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="970b1-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="970b1-135">Additional resources</span></span>

[<span data-ttu-id="970b1-136">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="970b1-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="970b1-137">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="970b1-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="970b1-138">Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="970b1-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="970b1-139">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="970b1-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="970b1-140">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="970b1-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="970b1-141">Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="970b1-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)