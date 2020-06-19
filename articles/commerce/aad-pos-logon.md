---
title: POS サインインの Azure Active Directory 認証を有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) のサインイン エクスペリエンスを構成して、Azure Active Directory 認証を使用できるようにする方法について説明します。
author: boycezhu
manager: annbe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 4f5a02348e8cef44424ae5d6a49de02d762ba245
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410038"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="f489e-103">POS サインインの Azure Active Directory 認証を有効にする</span><span class="sxs-lookup"><span data-stu-id="f489e-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="f489e-104">Microsoft Dynamics 365 Commerce を使用する多くの顧客は、他の Microsoft クラウド サービスも使用しており、Azure Active Directory (Azure AD) を使用して、これらのサービスのユーザー資格情報を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="f489e-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="f489e-105">そのような場合、顧客はアプリケーション間で同じ Azure AD アカウントを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f489e-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="f489e-106">このトピックでは、Commerce 販売時点管理 (POS) のサインイン エクスペリエンスを構成して、 Azure AD 認証を使用できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f489e-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="f489e-107">Azure AD 認証の構成</span><span class="sxs-lookup"><span data-stu-id="f489e-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="f489e-108">店舗の POS サインインの認証方法として Azure AD を使用できるようにするには、店舗の機能プロファイルの設定を構成してから、それらの設定を POS クライアントに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f489e-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="f489e-109">機能プロファイルを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f489e-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="f489e-110">**Retail および Commerce** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **機能プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f489e-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="f489e-111">変更する機能プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f489e-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="f489e-112">**関数**クイック タブの、**POS スタッフ ログオン** セクションで、**ログオン認証方法**フィールドの値を**従業員 ID とパスワード**から **Azure Active Directory** に変更します。</span><span class="sxs-lookup"><span data-stu-id="f489e-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="f489e-113">既定では、すべての機能プロファイルは、POS 認証方法として**従業員 ID とパスワード**を使用します。</span><span class="sxs-lookup"><span data-stu-id="f489e-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="f489e-114">したがって、Azure AD を使用する場合は、**ログオン認証方法**フィールドの値を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f489e-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="f489e-115">選択した機能プロファイルにリンクされているすべての小売用店舗は、この変更によって影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="f489e-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="f489e-116">POS クライアントにこの設定を適用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f489e-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="f489e-117">**Retail と Commerce** \> **Retail と Commerce IT** \> **配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f489e-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="f489e-118">**1070** (**チャネル構成**) 配布スケジュールを実行します。</span><span class="sxs-lookup"><span data-stu-id="f489e-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="f489e-119">Azure AD 認証にはインターネット接続が必要です。</span><span class="sxs-lookup"><span data-stu-id="f489e-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="f489e-120">POS がオフライン モードの場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="f489e-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="f489e-121">現時点では、**マネージャー優先**機能は、 Azure AD の認証方法としてサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f489e-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="f489e-122">Azure AD が POS サインインの認証方法として構成されている場合でも、オペレーター ID とパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f489e-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="f489e-123">Azure AD アカウントと作業者の関連付け</span><span class="sxs-lookup"><span data-stu-id="f489e-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="f489e-124">店舗の作業者が POS アプリケーションへのサインインに Azure AD アカウントを使用する前に、Azure AD アカウントがその作業者に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f489e-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="f489e-125">Azure AD アカウントを作業者に関連付けるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f489e-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="f489e-126">**Retail と Commerce** \> **従業員** \> **作業者**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f489e-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="f489e-127">作業者の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f489e-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="f489e-128">アクション ウィンドウ、**Commerce** タブの、**外部 ID** グループで、**既存の ID の関連付け**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f489e-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="f489e-129">**既存の外部 ID を使用する**ダイアログ ボックスで、**電子メールで検索**を選択し、Azure AD 電子メール アドレスを入力して、**検索**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f489e-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="f489e-130">返された Azure AD アカウントをを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f489e-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="f489e-131">**Commerce** タブの**エイリアス**、**UPN**、および**外部サブ ID** フィールドが入力されます。</span><span class="sxs-lookup"><span data-stu-id="f489e-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f489e-132">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f489e-132">Additional resources</span></span>

[<span data-ttu-id="f489e-133">MPOS および Cloud POS の拡張ログオン機能の設定</span><span class="sxs-lookup"><span data-stu-id="f489e-133">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="f489e-134">小売機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="f489e-134">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="f489e-135">作業者のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f489e-135">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
