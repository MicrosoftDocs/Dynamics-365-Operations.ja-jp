---
title: POS サインインの Azure Active Directory 認証の構成
description: このトピックでは、Azure Active Directory を Microsoft Dynamics 365 Commerce 販売時点管理の認証方法として構成する方法について説明します。
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937461"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="42609-103">POS サインインの Azure Active Directory 認証の構成</span><span class="sxs-lookup"><span data-stu-id="42609-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="42609-104">このトピックでは、Azure Active Directory (Azure AD) を Microsoft Dynamics 365 Commerce 販売時点管理 (POS) の認証方法として構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="42609-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="42609-105">Microsoft Azure、Microsoft 365、および Microsoft Teams など、他の Microsoft クラウド サービスと共に Dynamics 365 Commerce を使用している小売業者は、通常、アプリケーション間での安全でシームレスなサインイン エクスペリエンスのため、ユーザー資格情報の集中管理に Azure AD を使用します。</span><span class="sxs-lookup"><span data-stu-id="42609-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="42609-106">Commerce POS に Azure AD 認証を使用するには、最初に Azure AD を Commerce 本社の認証方法として構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="42609-107">POS 認証方法の構成</span><span class="sxs-lookup"><span data-stu-id="42609-107">Configure POS authentication method</span></span>

<span data-ttu-id="42609-108">Commerce 本社の POS 認証方法を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="42609-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="42609-109">**Retail と Commerce \> チャネル設定 \> POS の設定 \> POS プロファイル \> 機能プロファイル** の順に移動し、機能プロファイルを選択して変更します。</span><span class="sxs-lookup"><span data-stu-id="42609-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="42609-110">**機能** クイックタブの **POS スタッフ ログオン** セクションで、**ログオン認証方法** ドロップダウン リストから目的の認証方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="42609-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="42609-111">**ログオン認証方法** には 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="42609-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="42609-112">**個人 ID とパスワード** - この既定のオプションの場合、POS ユーザーが POS にサインインしてマネージャーの上書き機能にアクセスするために、個人 ID とパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="42609-113">**シングル サインオンなしの Azure AD** - このオプションの場合、POS ユーザーが Azure AD 資格情報を使用して POS にサインインし、マネージャー上書き機能にアクセスすることが必要です。</span><span class="sxs-lookup"><span data-stu-id="42609-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="42609-114">POS クライアントが更新されるか再度開いた場合、POS ユーザーは再度サインインするために Azure AD 資格情報を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="42609-115">**シングル サインオン 付きの Azure AD** - このオプションを選択した場合、POS ユーザーは、他の Web アプリケーションによって使用されている有効な Azure AD 資格情報を使用してクラウド POS (CPOS) にサインインするか、または Windows にサインインしている Azure AD 資格情報を使用して Modern POS (MPOS) にサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="42609-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="42609-116">両方の方法により、POS のサインイン画面で Azure AD 資格情報を入力する必要なくサインインできるようになります。</span><span class="sxs-lookup"><span data-stu-id="42609-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="42609-117">ただし、POS マネージャー上書き機能にアクセスするには、Azure AD 資格情報を使用してサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="42609-118">**Retail と Commerce > Retail および Commerce IT > 配送スケジュール** に移動し、**1070 (チャネル コンフィギュレーション)** ジョブを実行して、最新の機能プロファイル設定を POS クライアントに同期させます。</span><span class="sxs-lookup"><span data-stu-id="42609-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="42609-119">**シングル サインオンなしの Azure AD** の認証方法オプションは、Commerce バージョン 10.0.18 以前の **Azure Active Directory** オプションに代わります。</span><span class="sxs-lookup"><span data-stu-id="42609-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="42609-120">Azure AD 認証には有効なインターネット接続が必要で、POS がオフラインの場合は機能しません。</span><span class="sxs-lookup"><span data-stu-id="42609-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="42609-121">Azure AD アカウントを POS ユーザーに関連付ける</span><span class="sxs-lookup"><span data-stu-id="42609-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="42609-122">Azure AD を POS 認証方法として使用するには、Azure AD アカウントを Commerce 本社の POS ユーザーと関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="42609-123">Azure AD アカウントを Commerce 本社の POS ユーザーに関連付けるには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="42609-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="42609-124">**Retail と Commerce > 従業員 > 作業者** に移動し、作業者レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="42609-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="42609-125">アクション ウィンドウで **Commerce** タブを選択し、**外部 ID** の下で、**既存の ID の関連付け** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42609-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="42609-126">**既存の外部 ID を使用する** ダイアログ ボックスで、**電子メールで検索** を選択し、Azure AD 電子メール アドレスを入力して、**検索** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42609-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="42609-127">返された Azure AD アカウントを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42609-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="42609-128">上記の構成手順の後、**Commerce** タブの **エイリアス**、**UPN**、および **外部サブ ID** フィールドが入力されます。</span><span class="sxs-lookup"><span data-stu-id="42609-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="42609-129">**Retail と Commerce > Retail と Commerce IT > 配送スケジュール** で **1060 (スタッフ)** ジョブを実行して、最新の POS ユーザーと Azure AD アカント データをチャネルに同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="42609-130">ベスト プラクティスとして、パスワード、POS のアクセス許可、関連付けられている Azure AD アカウント、または従業員のアドレス帳などの作業者情報が Commerce 本社に更新された後、**1060 (スタッフ)** ジョブを実行して、最新の作業者情報とチャネルを同期することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42609-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="42609-131">POS クライアントはユーザーの認証および承認のチェックに使用する正しいデータを取得できます。</span><span class="sxs-lookup"><span data-stu-id="42609-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="42609-132">Azure AD 認証を使用した POS のレジスター ロックとサインアウト</span><span class="sxs-lookup"><span data-stu-id="42609-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="42609-133">POS が Azure AD 認証方法を使用するように構成されている場合、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="42609-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="42609-134">POS アプリケーションで、**レジスターのロック** 機能は使用できません。</span><span class="sxs-lookup"><span data-stu-id="42609-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="42609-135">**自動ロック** 機能は、**自動ログオフ** 機能と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="42609-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="42609-136">POS ユーザーが **ログオフ** を選択すると、シングル サインインが有効になっているかどうかにかかわらず、次回 POS を起動する場合にユーザーは Azure AD 資格情報を使用してサインインするよう求められます。</span><span class="sxs-lookup"><span data-stu-id="42609-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="42609-137">Azure AD 認証を使用したマネージャー上書き機能</span><span class="sxs-lookup"><span data-stu-id="42609-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="42609-138">POS が Azure AD 認証を使用するように構成されている場合、マネージャーの上書き機能は、マネージャーのユーザーの Azure AD 資格情報を求めるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42609-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="42609-139">マネージャーのサインインが承認されると、マネージャーの Azure AD 資格情報が削除され、以前のユーザーの Azure AD 資格情報がそれ以降の POS 操作に使用されます。</span><span class="sxs-lookup"><span data-stu-id="42609-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="42609-140">Commerce のバージョン 10.0.18 以前では、マネージャーの上書き機能は Azure AD をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="42609-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="42609-141">POS が Azure AD 認証方法を使用するよう構成されている場合でも、個人 ID とパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="42609-142">Apple iOS デバイス上の Safari Web ブラウザーで CPOS を使用する場合、Azure AD 認証でマネージャー上書き機能を使用するには、Safari の設定の **ポップアップをブロック** をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42609-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="42609-143">共有デバイスでの Azure AD ベースの POS 認証のセキュリティ ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="42609-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="42609-144">多くの小売業者は、複数のユーザーが共有の物理デバイスから POS アプリケーションにアクセスすることが必要な方法で小売店舗の環境を設定します。</span><span class="sxs-lookup"><span data-stu-id="42609-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="42609-145">このコンテキストでは、シングル サインインは便利でシームレスな認証エクスペリエンスを提供しますが、現在の POS ユーザーが、別のユーザーの資格情報が使用されて POS のトランザクションまたは操作が実行されていることを認識しないことがあるというセキュリティ ループホールが作成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="42609-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="42609-146">Azure AD 認証方法を使用するように POS を構成する前に、セキュリティ ポリシーと共有デバイスのサインイン設定を確認して、最も適合するオプションを決定することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42609-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="42609-147">小売環境で物理的なデバイスのサインインに共有アカウント (ローカル アカウントなど) を使用する場合は、**シングル サインオンなしの Azure AD** オプションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42609-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="42609-148">これにより、POS にサインインするのに各 POS ユーザーは明示的に Azure AD 資格情報を提供することになります。</span><span class="sxs-lookup"><span data-stu-id="42609-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="42609-149">小売環境で従業員が POS および物理的なホスティング デバイスにサインインするのに自分の Azure AD アカウントを使用する必要がある場合、**シングル サインオン 付きの Azure AD** オプションを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42609-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42609-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="42609-150">Additional resources</span></span>

[<span data-ttu-id="42609-151">作業者のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="42609-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="42609-152">小売機能プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="42609-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="42609-153">MPOS および Cloud POS の拡張ログオン機能の設定</span><span class="sxs-lookup"><span data-stu-id="42609-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="42609-154">共有環境におけるクラウド POS のセキュリティ ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="42609-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
