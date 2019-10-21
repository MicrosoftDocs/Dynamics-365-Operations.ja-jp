---
title: ワークスペースの Power BI 統合のコンフィギュレーション
description: このトピックでは、PowerBI.com との統合をサポートする新しい Finance and Operations 環境を構成する方法を説明します。 このコンフィギュレーションにより、ワークスペースに Power BI コントロールが表示され、ユーザーはワークスペースに視覚エフェクトをピン留めすることができます。
author: MilindaV2
manager: AnnBe
ms.date: 07/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PowerBIConfiguration
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b51d1fa80f59f3e4131afedbd260d5263f30c1b9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174578"
---
# <a name="configure-power-bi-integration-for-workspaces"></a><span data-ttu-id="42d79-104">ワークスペースの Power BI 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="42d79-104">Configure Power BI integration for workspaces</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="42d79-105">概要</span><span class="sxs-lookup"><span data-stu-id="42d79-105">Overview</span></span>

<span data-ttu-id="42d79-106">ユーザーは、PowerBI.com アカウントからアプリケーション ワークスペースに、タイル、ダッシュ ボード、およびレポートをピン留めすることができます。</span><span class="sxs-lookup"><span data-stu-id="42d79-106">Users can pin tiles, dashboards, and reports from their own PowerBI.com account to application workspace.</span></span>

<span data-ttu-id="42d79-107">この機能を使用するには、構成を一度設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-107">This functionality requires a one-time configuration of your environment.</span></span> <span data-ttu-id="42d79-108">管理者は、Microsoft Power BI が正しく通信して認証できるようにするために、この手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-108">An administrator must do this step to enable Microsoft Power BI to communicate and authenticate correctly.</span></span>

<span data-ttu-id="42d79-109">ワークスペースに Power BI タイルを表示するには、サーバーはユーザーの代理として Power BI サービスに連絡し、視覚エフェクトにアクセスする必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-109">For a workspace to show a Power BI tile, the server must contact the Power BI service on behalf of a user and access the visualization.</span></span> <span data-ttu-id="42d79-110">そして、アプリケーション ワークスペースで視覚化を再描画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-110">It must then redraw the visualization in the application workspace.</span></span> <span data-ttu-id="42d79-111">サーバーが Power BI サービスに「ユーザーの代わりに」連絡するということが重要です。</span><span class="sxs-lookup"><span data-stu-id="42d79-111">The fact that the server contacts the Power BI service "on behalf of a user" is important.</span></span> <span data-ttu-id="42d79-112">`D365User@contoso.com` などのユーザーが BI PowerBI.com サービスに連絡するとき、Power BI は、ユーザーの PowerBI.com サブスクリプションからタイルとレポートのみを表示するはずです。</span><span class="sxs-lookup"><span data-stu-id="42d79-112">When a user, such as `D365User@contoso.com`, contacts the PowerBI.com service, Power BI should show only tiles and reports from the user's PowerBI.com subscription.</span></span>

<span data-ttu-id="42d79-113">この構成ステップが完了すると、PowerBI.com サービスに連絡できるようになります。</span><span class="sxs-lookup"><span data-stu-id="42d79-113">By completing this configuration step, you enable to contact the PowerBI.com service.</span></span>

## <a name="things-you-must-know-before-you-start"></a><span data-ttu-id="42d79-114">開始前に知っておく必要事項</span><span class="sxs-lookup"><span data-stu-id="42d79-114">Things you must know before you start</span></span> 

- <span data-ttu-id="42d79-115">アプリケーションのシステム管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-115">You must be a system administrator in the application.</span></span> <span data-ttu-id="42d79-116">このオプションは、**システム管理**メニューで利用できます。</span><span class="sxs-lookup"><span data-stu-id="42d79-116">This option is available on the **System administration** menu.</span></span>
- <span data-ttu-id="42d79-117">PowerBI.com のアカウントが必要です。</span><span class="sxs-lookup"><span data-stu-id="42d79-117">You must have a PowerBI.com account.</span></span> <span data-ttu-id="42d79-118">アカウントを持っていない場合は、試用版アカウントを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="42d79-118">You can create a trial account if you don't have an account.</span></span> <span data-ttu-id="42d79-119">(プロ ライセンスは、この構成ステップでは必要ありません。)</span><span class="sxs-lookup"><span data-stu-id="42d79-119">(A Pro license isn't required for this configuration step.)</span></span>
- <span data-ttu-id="42d79-120">自分の Power BI アカウントに、少なくとも 1 つのダッシュボードと 1 つのレポートがあることが必要です。</span><span class="sxs-lookup"><span data-stu-id="42d79-120">You must have at least one dashboard and one report in your Power BI account.</span></span> <span data-ttu-id="42d79-121">この構成ステップでは、ダッシュボードやレポートは必要ではありませんが、PowerBI.com アカウントにコンテンツが含まれていない場合コンフィギュレーションを検証することができないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="42d79-121">Although the dashboard and report aren't required for this configuration step, you might not be able to validate the configuration if you don't have any content in your PowerBI.com account.</span></span>
- <span data-ttu-id="42d79-122">Microsoft Azure Active Directory (Azure AD) アカウントの管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-122">You must be an administrator for your Microsoft Azure Active Directory (Azure AD) account.</span></span> <span data-ttu-id="42d79-123">管理者ではない場合は、管理者ユーザーはこのコンフィギュレーションの手順をユーザーのために実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-123">If you aren't the administrator, an administrative user must perform this configuration step for you.</span></span>
- <span data-ttu-id="42d79-124">構成されている Azure AD ドメインは、自分の PowerBI.com アカウントに使用したドメインと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-124">The Azure AD domain that is configured must be the same domain that you used for your PowerBI.com account.</span></span> <span data-ttu-id="42d79-125">たとえば、Contoso.com ドメインでアプリケーションをプロビジョニングした場合、そのドメイン内に `Tim@ContosoAX7.onmicrosoft.com` などの Power BI アカウントを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-125">For example, if you provisioned the application in the Contoso.com domain, you must have Power BI accounts in that domain, such as `Tim@ContosoAX7.onmicrosoft.com`.</span></span>

## <a name="registration-process"></a><span data-ttu-id="42d79-126">登録プロセス</span><span class="sxs-lookup"><span data-stu-id="42d79-126">Registration process</span></span> 

1. <span data-ttu-id="42d79-127">Azure テナント管理者アカウントを使用して https://portal.azure.com/ にログインします。</span><span class="sxs-lookup"><span data-stu-id="42d79-127">Sign in to https://portal.azure.com/ using an Azure tenant admin account.</span></span><br>
> [!NOTE]
> <span data-ttu-id="42d79-128">この手順を完了したユーザーは、アプリケーションを登録するテナントの管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-128">The user who completes this procedure must have Admin rights for the tenant to register applications.</span></span>

2. <span data-ttu-id="42d79-129">**Azure Active Directory** > **アプリの登録** > **新しいアプリケーションの登録**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="42d79-129">Go to **Azure Active Directory** > **App registrations** > **New application registration**.</span></span><br>
    <span data-ttu-id="42d79-130">![Azure ポータル アプリケーションの登録](media/Azure-Portal-AppRegistration.png)</span><span class="sxs-lookup"><span data-stu-id="42d79-130">![Azure Portal App Registration](media/Azure-Portal-AppRegistration.png)</span></span>

3. <span data-ttu-id="42d79-131">次の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="42d79-131">Enter the following values:</span></span>

- <span data-ttu-id="42d79-132">**名前** - アプリの名前。</span><span class="sxs-lookup"><span data-stu-id="42d79-132">**Name** - Your app name.</span></span>
- <span data-ttu-id="42d79-133">**アプリケーション タイプ** - Web アプリ/API</span><span class="sxs-lookup"><span data-stu-id="42d79-133">**Application type** - Web app/API</span></span>
- <span data-ttu-id="42d79-134">**サインオン URL** - クライアントのベース URL。</span><span class="sxs-lookup"><span data-stu-id="42d79-134">**Sign-on URL** - The base URL of your client.</span></span> <span data-ttu-id="42d79-135">たとえば、`https://contosoax7.cloud.dynamics.com`。</span><span class="sxs-lookup"><span data-stu-id="42d79-135">For example, `https://contosoax7.cloud.dynamics.com`.</span></span>

> [!NOTE]
> <span data-ttu-id="42d79-136">バージョンにより、URL の接尾語として /oauth を追加するか、`https://contosoax7.cloud.dynamics.com/oauth/` や `http://contosoax7.cloud.dynamics.com/oauth/` のように、プロトコルとして https の代わりに http を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-136">Depending on your version, you may need to add /oauth as a suffix to the URL, or use http instead of https as the protocol, such as: `https://contosoax7.cloud.dynamics.com/oauth/` or `http://contosoax7.cloud.dynamics.com/oauth/`.</span></span>
             
4. <span data-ttu-id="42d79-137">**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-137">Click **Create**.</span></span>
5. <span data-ttu-id="42d79-138">**アプリケーション ID** をコピーします。</span><span class="sxs-lookup"><span data-stu-id="42d79-138">Copy the **Application ID**.</span></span> <span data-ttu-id="42d79-139">これは、PowerBI.com サービスに接続するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="42d79-139">This will be used to connect to the PowerBI.com service.</span></span>
6. <span data-ttu-id="42d79-140">**設定** > **必要なアクセス許可** > **追加** > **API の選択** > **Power BI サービス (Power BI)** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-140">Click **Settings** > **Required permissions** > **Add** > **Select an API** > **Power BI Service (Power BI)**.</span></span>
7. <span data-ttu-id="42d79-141">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-141">Click **Select**.</span></span>
8. <span data-ttu-id="42d79-142">アクセスを有効にして **選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-142">Enable Access and click **Select**.</span></span><br>
    <span data-ttu-id="42d79-143">![Azure ポータル アプリのアクセス許可](media/Azure-Portal-AppPermissions.png)</span><span class="sxs-lookup"><span data-stu-id="42d79-143">![Azure Portal App Permissions](media/Azure-Portal-AppPermissions.png)</span></span>

9. <span data-ttu-id="42d79-144">**完了** をクリックし、**アクセス許可の付与** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-144">Click **Done** and then click **Grant Permissions**.</span></span>
10. <span data-ttu-id="42d79-145">**設定** > **キー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-145">Click **Settings** > **Keys**.</span></span>
11. <span data-ttu-id="42d79-146">**キーの説明** および **期限切れ日時** に値を入力し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-146">Enter a value for **Key description** and **Expires**, and then click **Save**.</span></span>

<span data-ttu-id="42d79-147">**アプリケーション ID** および **アプリケーション キー** を書き留めます。</span><span class="sxs-lookup"><span data-stu-id="42d79-147">Make a note of the **Application ID** and **Application Key**.</span></span> <span data-ttu-id="42d79-148">次の手順で、これらの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="42d79-148">You will use these values in the next procedure.</span></span>

## <a name="specify-power-bi-settings-in-finance-and-operations"></a><span data-ttu-id="42d79-149">Finance and Operations での Power BI の設定の指定</span><span class="sxs-lookup"><span data-stu-id="42d79-149">Specify Power BI settings in Finance and Operations</span></span>

1. <span data-ttu-id="42d79-150">クライアントで **Power BI コンフィギュレーション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42d79-150">In the client, open the **Power BI configuration** page.</span></span><br>
    <span data-ttu-id="42d79-151">![Power BIコンフィギュレーション ダイアログ](./media/D365-PBI-Configuration.png)</span><span class="sxs-lookup"><span data-stu-id="42d79-151">![Power BI configuration dialog](./media/D365-PBI-Configuration.png)</span></span>

2. <span data-ttu-id="42d79-152">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42d79-152">Select **Edit**.</span></span>
3. <span data-ttu-id="42d79-153">**有効** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="42d79-153">Set the **Enabled** option to **Yes**.</span></span>
4. <span data-ttu-id="42d79-154">**アプリケーション ID** フィールドで、前の手順で Power BI から取得した**アプリケーション ID** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="42d79-154">In the **Application ID** field, enter the **Application ID** value that you got from Power BI in the previous procedure.</span></span>
5. <span data-ttu-id="42d79-155">**アプリケーション キー** フィールドで、前の手順で Power BI から取得した**アプリケーション キー** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="42d79-155">In the **Application Key** field, enter the **Application Key** value that you got from Power BI in the previous procedure.</span></span>

    <span data-ttu-id="42d79-156">Power BI のコンテンツに**会社**という名前のテーブルおよび **ID** という名前の列がある場合にのみ、会社フィルターを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="42d79-156">You can apply the company filter only if your Power BI content has a table that is named **Company** and a column that is named **ID**.</span></span> <span data-ttu-id="42d79-157">リリース済の既存の Power BI コンテンツでは、この規約が使用されます。</span><span class="sxs-lookup"><span data-stu-id="42d79-157">Ready-made Power BI content that is released uses this convention.</span></span>

6. <span data-ttu-id="42d79-158">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-158">Click **Save**.</span></span>

<span data-ttu-id="42d79-159">次のセクションの手順を実行して変更を確認し、PowerBI.com の統合を有効にします。</span><span class="sxs-lookup"><span data-stu-id="42d79-159">Complete the steps in the next section to verify the changes and enable PowerBI.com integrations.</span></span>

## <a name="pin-tiles-to-a-workspace"></a><span data-ttu-id="42d79-160">ワークスペースにタイルを固定</span><span class="sxs-lookup"><span data-stu-id="42d79-160">Pin tiles to a workspace</span></span>

1. <span data-ttu-id="42d79-161">PowerBI.com コンフィギュレーションを検証するには、**開始する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42d79-161">To validate the PowerBI.com configuration, click **Get started**.</span></span><br>
> [!NOTE]
> <span data-ttu-id="42d79-162">変更を適用するにはブラウザーを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-162">You may need to refresh the browser to apply the changes.</span></span> <br>
> <span data-ttu-id="42d79-163">![Power BI の承認](./media/D365-PBI-GetStarted.png)</span><span class="sxs-lookup"><span data-stu-id="42d79-163">![Authorize Power BI](./media/D365-PBI-GetStarted.png)</span></span>

<span data-ttu-id="42d79-164">アプリケーションから Power BI をはじめて起動する場合は、クライアントから、Power BI へのサインインを承認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="42d79-164">If you're starting Power BI from the application for the first time, you're prompted to authorize sign-in to Power BI from the client.</span></span> <span data-ttu-id="42d79-165">**ここをクリックして Power BI に承認を与える** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42d79-165">Select **Click here to provide authorization to Power BI**.</span></span>

<span data-ttu-id="42d79-166">ユーザーは、初めて Power BI コンテンツをピン留めするとき、このステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-166">Users must complete this step the first time they pin Power BI content.</span></span>

2. <span data-ttu-id="42d79-167">Azure AD の同意ページが、お客様の同意を求めます。</span><span class="sxs-lookup"><span data-stu-id="42d79-167">The Azure AD consent page asks for your consent.</span></span> <span data-ttu-id="42d79-168">アプリケーションがユーザーに代わって PowerBI.com にアクセスするには、ユーザーの同意が必要です。</span><span class="sxs-lookup"><span data-stu-id="42d79-168">User consent is required for the application to access PowerBI.com on behalf of the user.</span></span> <span data-ttu-id="42d79-169">**受け入れる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42d79-169">Select **Accept**.</span></span>

3. <span data-ttu-id="42d79-170">Azure AD に既にサインインしているので、再度資格情報を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="42d79-170">Because you're already signed in to Azure AD, you don't have to enter your credentials again.</span></span> <span data-ttu-id="42d79-171">新しいタブが表示され、アプリケーションと Power BI の間の接続を承認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="42d79-171">A new tab appears, where you're prompted to authorize the connection between the application and Power BI.</span></span> <span data-ttu-id="42d79-172">接続を承認し元のタブに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42d79-172">Authorize the connection, and then return to the original tab.</span></span>

4. <span data-ttu-id="42d79-173">PowerBI.com アカウントのタイルの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="42d79-173">A list of tiles from your PowerBI.com account appears.</span></span> <span data-ttu-id="42d79-174">1 つまたは複数のタイルを選択し、選択したワークスペースにピン留めします。</span><span class="sxs-lookup"><span data-stu-id="42d79-174">Select one or more tiles to pin to the selected workspace.</span></span>
    <span data-ttu-id="42d79-175">![Power BI 統合の検証](./media/D365-PBI-Validation.png)</span><span class="sxs-lookup"><span data-stu-id="42d79-175">![Validate Power BI integration](./media/D365-PBI-Validation.png)</span></span>

## <a name="troubleshooting-common-errors"></a><span data-ttu-id="42d79-176">一般的なエラーのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="42d79-176">Troubleshooting common errors</span></span>

<span data-ttu-id="42d79-177">上の手順で **承諾** をクリックした後、プロセスが失敗した場合、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-177">In the procedure above, after you click **Accept**, you might receive the following error message if the process is unsuccessful.</span></span> <span data-ttu-id="42d79-178">エラーの詳細がメッセージの下部に表示されていることに注意します。</span><span class="sxs-lookup"><span data-stu-id="42d79-178">Note that the details of the error appear at the bottom of the message.</span></span> <span data-ttu-id="42d79-179">追加の技術情報は、原因を特定するのに役立つヒントを提供します。</span><span class="sxs-lookup"><span data-stu-id="42d79-179">Additional technical information provides clues that can help you determine what went wrong.</span></span>

### <a name="some-common-issues-and-the-resolution-steps"></a><span data-ttu-id="42d79-180">一般的な問題および解決手順</span><span class="sxs-lookup"><span data-stu-id="42d79-180">Some common issues and the resolution steps</span></span>

| <span data-ttu-id="42d79-181">エラー</span><span class="sxs-lookup"><span data-stu-id="42d79-181">Error</span></span>                                                       | <span data-ttu-id="42d79-182">解像度</span><span class="sxs-lookup"><span data-stu-id="42d79-182">Resolution</span></span> |
|-------------------------------------------------------------|------------|
| <span data-ttu-id="42d79-183">Power BI サービスを使用できません。</span><span class="sxs-lookup"><span data-stu-id="42d79-183">The Power BI service is unavailable.</span></span>                        | <span data-ttu-id="42d79-184">この問題は頻繁には発生しませんが、Power BI サービスに到達できないことがあります。</span><span class="sxs-lookup"><span data-stu-id="42d79-184">This issue doesn't occur very often, but the Power BI service might sometimes be unreachable.</span></span> <span data-ttu-id="42d79-185">再登録する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="42d79-185">You don't have to re-register.</span></span> <span data-ttu-id="42d79-186">後でタイルをワークスペースに固定してみてください。</span><span class="sxs-lookup"><span data-stu-id="42d79-186">Try to pin a tile to a workspace later.</span></span> |
| <span data-ttu-id="42d79-187">アプリケーションにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="42d79-187">You can't access the application.</span></span>                           | <span data-ttu-id="42d79-188">登録プロセス中に、**手順 3 アクセスする API** の下のすべてのチェック ボックスが選択されなかった可能性があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-188">You probably didn't select all the check boxes under **Step 3 Choose APIs to access** during the registration process.</span></span> <span data-ttu-id="42d79-189">Power BI を起動し、登録プロセスを再実行します。</span><span class="sxs-lookup"><span data-stu-id="42d79-189">Start Power BI, and re-run the registration process.</span></span> |
| <span data-ttu-id="42d79-190">Power BI タイル ページが空です (コンテンツが表示されません)。</span><span class="sxs-lookup"><span data-stu-id="42d79-190">The Power BI tiles page is empty (no content is shown).</span></span>     | <span data-ttu-id="42d79-191">PowerBI.com アカウントに、ダッシュ ボードまたはタイルがない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="42d79-191">Your PowerBI.com account might not have a dashboard or any tiles.</span></span> <span data-ttu-id="42d79-192">サンプル ダッシュ ボードなどのダッシュボードを追加して、もう一度をタイルをピン留めしてみてください。</span><span class="sxs-lookup"><span data-stu-id="42d79-192">Add a dashboard, such as a sample dashboard, and try to pin a tile again.</span></span> |
| <span data-ttu-id="42d79-193">Power BI の承認時にエラー</span><span class="sxs-lookup"><span data-stu-id="42d79-193">Error when authorizing Power BI</span></span>                             | <span data-ttu-id="42d79-194">Azure 管理者ダッシュボードの、**ユーザーおよびグループ \> ユーザー設定** の下で、**ユーザーはアプリが会社のデータにアクセスすることに同意できる** オプションが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="42d79-194">On the Azure Admin dashboard, under **Users and Groups \> User settings**, make sure that the **Users can consent to apps accessing company data on their behalf** option is set to **Yes**.</span></span> |

