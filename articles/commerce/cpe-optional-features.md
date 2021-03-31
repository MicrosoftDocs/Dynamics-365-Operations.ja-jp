---
title: Dynamics 365 Commerce の評価環境のオプション機能を構成する
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境のオプション機能を構成する方法について説明します。
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: def99a34404357e28501de5ccf11c6130d53f34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213821"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="83367-103">Dynamics 365 Commerce 評価環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="83367-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83367-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価環境のオプション機能を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83367-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83367-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="83367-105">Prerequisites</span></span>

<span data-ttu-id="83367-106">トランザクション電子メール機能を評価する場合、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="83367-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="83367-107">評価環境をプロビジョニングする Microsoft Azure のサブスクリプションから使用できるメールサーバー (シンプル メール トランスファー プロトコル \[SMTP\] サーバー) が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="83367-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="83367-108">サーバーの完全修飾ドメイン名 (FQDN)/IP アドレス、SMTP ポート番号、および認証の詳細が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="83367-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="83367-109">画像バックエンドのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="83367-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="83367-110">メディア ベース URL の検索</span><span class="sxs-lookup"><span data-stu-id="83367-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="83367-111">この手順を完了する前に、[コマースでサイトを設定する](cpe-post-provisioning.md#set-up-your-site-in-commerce) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83367-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="83367-112">プロビジョニングの実行時に eコマースを初期化した際に作成した URL を使用して、コマース サイトの管理ツールにサイン インします ([eコマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="83367-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="83367-113">**Fabrikam** サイトを開きます。</span><span class="sxs-lookup"><span data-stu-id="83367-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="83367-114">左側のメニューで、**メディア ライブラリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="83367-115">1 つの画像資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-115">Select any single image asset.</span></span>
1. <span data-ttu-id="83367-116">右側のプロパティ インスペクターで、**公開 URL** プロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="83367-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="83367-117">値は URL です。</span><span class="sxs-lookup"><span data-stu-id="83367-117">The value is a URL.</span></span> <span data-ttu-id="83367-118">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="83367-118">Here is an example:</span></span>

    <span data-ttu-id="83367-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。</span><span class="sxs-lookup"><span data-stu-id="83367-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="83367-120">URL の最後の識別子 (前の例では **MA1nQC**) を文字列 **search?fileName=** と置換します。</span><span class="sxs-lookup"><span data-stu-id="83367-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="83367-121">この変更を行った後の URL の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="83367-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="83367-122">この URL は、メディア ベース URL です。</span><span class="sxs-lookup"><span data-stu-id="83367-122">This URL is your media base URL.</span></span> <span data-ttu-id="83367-123">記録しておいてください。</span><span class="sxs-lookup"><span data-stu-id="83367-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="83367-124">メディア ベース URL の更新</span><span class="sxs-lookup"><span data-stu-id="83367-124">Update the media base URL</span></span>

1. <span data-ttu-id="83367-125">コマースの本部にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="83367-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="83367-126">左側のメニューを使用して、**モジュール \> 小売りとコマース \> チャネルの設定 \> チャネル プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83367-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="83367-127">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-127">Select **Edit**.</span></span>
1. <span data-ttu-id="83367-128">**プロファイルのプロパティ** で、**メディア サーバー ベース URL** プロパティ値を、以前に作成したメディア ベース URL と置き換えます。</span><span class="sxs-lookup"><span data-stu-id="83367-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="83367-129">使用可能な他のチャネル **scXXXXXXXXX** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="83367-130">**プロファイル プロパティ** で、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="83367-131">追加されたプロパティに対して、**メディア サーバー ベース URL** をプロパティ キーとして選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="83367-132">プロパティ値として、以前に作成したメディア ベース URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="83367-133">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="83367-134">電子メール サーバーの構成とテストを行います</span><span class="sxs-lookup"><span data-stu-id="83367-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="83367-135">ここで入力する SMTP サーバーまたは電子メール サービスは、環境に使用している Azure サブスクリプションからアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="83367-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="83367-136">コマースの本部にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="83367-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="83367-137">左側のメニューを使用して、**モジュール  \>  小売とコマース \> 本部の設定 \> パラメーター \> 電子メールパラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="83367-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="83367-138">**SMTP 設定** タブの、**送信メール サーバー** フィールドで、SMTP サーバーまたは電子メールサービスの FQDN または IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="83367-139">**SMTP ポート番号** フィールドで、ポート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="83367-140">(Secure Sockets Layer \[SSL\] を使用しない場合、既定のポート番号は **25** になります。)</span><span class="sxs-lookup"><span data-stu-id="83367-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="83367-141">認証が必要な場合は、**ユーザー名** および **パスワード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="83367-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-142">Select **Save**.</span></span>
1. <span data-ttu-id="83367-143">**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="83367-144">**テスト電子メール** タブの、**電子メール プロバイダー** フィールドで、**SMTP** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="83367-145">**送信先** フィールドで、テスト電子メールの送信先となる電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="83367-146">**テスト電子メールの送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="83367-147">電子メール テンプレートのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="83367-147">Configure email templates</span></span>

<span data-ttu-id="83367-148">電子メールを送信する各トランザクション イベントに関しては、有効な送信者の電子メール アドレスで電子メール テンプレートを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83367-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="83367-149">コマースの本部にサイン インします。</span><span class="sxs-lookup"><span data-stu-id="83367-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="83367-150">左側のメニューを使用して、**モジュール  \>  小売とコマース \> 本部の設定 \> パラメーター \> 組織のメール テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="83367-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="83367-151">**リストを表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-151">Select **Show list**.</span></span>
1. <span data-ttu-id="83367-152">リストの各テンプレートに関しては、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="83367-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="83367-153">**送信者電子メール** フィールドに、送信者の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="83367-154">オプション: **送信者名** フィールドに、送信者名として使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="83367-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="83367-155">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="83367-156">電子メール テンプレートのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="83367-156">Customize email templates</span></span>

<span data-ttu-id="83367-157">電子メール テンプレートをカスタマイズして、異なる画像を使用するようにできます。</span><span class="sxs-lookup"><span data-stu-id="83367-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="83367-158">またはテンプレートのリンクを更新して、評価環境に移動することも可能です。</span><span class="sxs-lookup"><span data-stu-id="83367-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="83367-159">この手順では、既定のテンプレートをダウンロードし、システムのテンプレートを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="83367-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="83367-160">Web ブラウザーで、[Microsoft Dynamics 365 Commerce 評価版既定の電子メール アドレス テンプレート ZIP ファイル](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)をローカル コンピューターにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="83367-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="83367-161">このファイルには、次の HTML ドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="83367-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="83367-162">注文確認モジュール テンプレート</span><span class="sxs-lookup"><span data-stu-id="83367-162">Order confirmation template</span></span>
    - <span data-ttu-id="83367-163">ギフト カード テンプレートの発行</span><span class="sxs-lookup"><span data-stu-id="83367-163">Issue gift card template</span></span>
    - <span data-ttu-id="83367-164">新しい注文テンプレート</span><span class="sxs-lookup"><span data-stu-id="83367-164">New order template</span></span>
    - <span data-ttu-id="83367-165">注文テンプレートのパック</span><span class="sxs-lookup"><span data-stu-id="83367-165">Pack order template</span></span>
    - <span data-ttu-id="83367-166">注文テンプレートのピック</span><span class="sxs-lookup"><span data-stu-id="83367-166">Pick order template</span></span>

1. <span data-ttu-id="83367-167">テキストまたは HTML エディターを使用してテンプレートをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="83367-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="83367-168">このトピックの後半にある、[サポートされているトークン](#supported-tokens-in-the-email-template) のリストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="83367-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="83367-169">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="83367-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="83367-170">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 組織の電子メール テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="83367-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="83367-171">左のリストを展開すると、すべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83367-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="83367-172">カスタマイズする各テンプレートに関しては、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="83367-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="83367-173">リストでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="83367-174">**電子メール メッセージのコンテンツ** で、リストから適切な言語バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="83367-175">(既定の言語は **en-us** です。)</span><span class="sxs-lookup"><span data-stu-id="83367-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="83367-176">**電子メール メッセージ コンテンツ** で、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="83367-177">**電子メール テンプレートのアップロード** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83367-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="83367-178">**参照** を選択し、カスタマイズされたコンテンツを含む HTML ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="83367-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="83367-179">**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-179">Select **Upload**.</span></span> <span data-ttu-id="83367-180">テンプレートがシステムにアップロードされ、プレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83367-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="83367-181">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-181">Select **OK**.</span></span>
    1. <span data-ttu-id="83367-182">オプション: テンプレートの **件名** プロパティをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="83367-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="83367-183">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="83367-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="83367-184">電子メール テンプレートでサポートされているトークン</span><span class="sxs-lookup"><span data-stu-id="83367-184">Supported tokens in the email template</span></span>

<span data-ttu-id="83367-185">電子メールが表示されると、これらのトークンは顧客と顧客の注文に適用される実際の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="83367-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="83367-186">販売注文</span><span class="sxs-lookup"><span data-stu-id="83367-186">Sales order</span></span>

<span data-ttu-id="83367-187">次のトークンは、販売注文全体に適用されます。</span><span class="sxs-lookup"><span data-stu-id="83367-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="83367-188">トークンの名前</span><span class="sxs-lookup"><span data-stu-id="83367-188">Name of the token</span></span> | <span data-ttu-id="83367-189">トークン</span><span class="sxs-lookup"><span data-stu-id="83367-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="83367-190">注文番号</span><span class="sxs-lookup"><span data-stu-id="83367-190">Order number</span></span>      | <span data-ttu-id="83367-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="83367-191">%salesid%</span></span> |
| <span data-ttu-id="83367-192">顧客の名前</span><span class="sxs-lookup"><span data-stu-id="83367-192">Customer's name</span></span>   | <span data-ttu-id="83367-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="83367-193">%customername%</span></span> |
| <span data-ttu-id="83367-194">配送先住所</span><span class="sxs-lookup"><span data-stu-id="83367-194">Delivery address</span></span>  | <span data-ttu-id="83367-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="83367-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="83367-196">請求先住所</span><span class="sxs-lookup"><span data-stu-id="83367-196">Billing address</span></span>   | <span data-ttu-id="83367-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="83367-197">%customeraddress%</span></span> |
| <span data-ttu-id="83367-198">注文日付</span><span class="sxs-lookup"><span data-stu-id="83367-198">Order date</span></span>        | <span data-ttu-id="83367-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="83367-199">%shipdate%</span></span> |
| <span data-ttu-id="83367-200">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="83367-200">Delivery mode</span></span>     | <span data-ttu-id="83367-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="83367-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="83367-202">割引</span><span class="sxs-lookup"><span data-stu-id="83367-202">Discount</span></span>          | <span data-ttu-id="83367-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="83367-203">%discount%</span></span> |
| <span data-ttu-id="83367-204">売上税</span><span class="sxs-lookup"><span data-stu-id="83367-204">Sales tax</span></span>         | <span data-ttu-id="83367-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="83367-205">%tax%</span></span> |
| <span data-ttu-id="83367-206">注文合計</span><span class="sxs-lookup"><span data-stu-id="83367-206">Order total</span></span>       | <span data-ttu-id="83367-207">%total%</span><span class="sxs-lookup"><span data-stu-id="83367-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="83367-208">販売明細行</span><span class="sxs-lookup"><span data-stu-id="83367-208">Sales line</span></span>

<span data-ttu-id="83367-209">次のトークンは、注文の各製品の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="83367-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="83367-210">**製品リスト - 開始** トークンを各製品に対して繰り返される HTML ブロックの先頭に、**製品リスト - 終了** トークンをブロックの末尾に配置します。</span><span class="sxs-lookup"><span data-stu-id="83367-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="83367-211">トークンの名前</span><span class="sxs-lookup"><span data-stu-id="83367-211">Name of the token</span></span>      | <span data-ttu-id="83367-212">トークン</span><span class="sxs-lookup"><span data-stu-id="83367-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="83367-213">製品リスト - 開始</span><span class="sxs-lookup"><span data-stu-id="83367-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="83367-214">Product list - 終了</span><span class="sxs-lookup"><span data-stu-id="83367-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="83367-215">製品名</span><span class="sxs-lookup"><span data-stu-id="83367-215">Product name</span></span>           | <span data-ttu-id="83367-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="83367-216">%lineproductname%</span></span> |
| <span data-ttu-id="83367-217">説明</span><span class="sxs-lookup"><span data-stu-id="83367-217">Description</span></span>            | <span data-ttu-id="83367-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="83367-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="83367-219">件数</span><span class="sxs-lookup"><span data-stu-id="83367-219">Quantity</span></span>               | <span data-ttu-id="83367-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="83367-220">%linequantity%</span></span> |
| <span data-ttu-id="83367-221">明細行の単価</span><span class="sxs-lookup"><span data-stu-id="83367-221">Line unit price</span></span>        | <span data-ttu-id="83367-222">%lineprice% (確認)</span><span class="sxs-lookup"><span data-stu-id="83367-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="83367-223">明細行の品目合計</span><span class="sxs-lookup"><span data-stu-id="83367-223">line item total</span></span>        | <span data-ttu-id="83367-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="83367-224">%linenetamount%</span></span> |
| <span data-ttu-id="83367-225">明細行割引</span><span class="sxs-lookup"><span data-stu-id="83367-225">line discount</span></span>          | <span data-ttu-id="83367-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="83367-226">%linediscount%</span></span> |
| <span data-ttu-id="83367-227">出荷日</span><span class="sxs-lookup"><span data-stu-id="83367-227">Ship date</span></span>              | <span data-ttu-id="83367-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="83367-228">%lineshipdate%</span></span> |
| <span data-ttu-id="83367-229">調達方法</span><span class="sxs-lookup"><span data-stu-id="83367-229">Procurement method</span></span>     | <span data-ttu-id="83367-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="83367-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="83367-231">配送先住所</span><span class="sxs-lookup"><span data-stu-id="83367-231">delivery address</span></span>       | <span data-ttu-id="83367-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="83367-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="83367-233">明細行の販売単位</span><span class="sxs-lookup"><span data-stu-id="83367-233">Sales unit of the line</span></span> | <span data-ttu-id="83367-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="83367-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="83367-235">追加リソース</span><span class="sxs-lookup"><span data-stu-id="83367-235">Additional resources</span></span>

[<span data-ttu-id="83367-236">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="83367-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="83367-237">Dynamics 365 Commerce 評価環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="83367-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="83367-238">Dynamics 365 Commerce の評価環境を構成する</span><span class="sxs-lookup"><span data-stu-id="83367-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="83367-239">Dynamics 365 Commerce 評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="83367-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="83367-240">Dynamics 365 Commerce 評価環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="83367-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="83367-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="83367-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="83367-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="83367-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="83367-243">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="83367-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="83367-244">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="83367-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]