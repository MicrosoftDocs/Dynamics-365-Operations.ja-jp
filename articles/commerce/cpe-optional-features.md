---
title: Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境のオプション機能をコンフィギュレーションする方法について説明します。
author: psimolin
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b17f8e9b0d8a9a62714d0073561e66642b2eaf9
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057743"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="02e03-103">Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02e03-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="02e03-104">このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境のオプション機能をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="02e03-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02e03-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="02e03-105">Prerequisites</span></span>

<span data-ttu-id="02e03-106">トランザクション電子メール機能を評価する場合、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="02e03-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="02e03-107">プレビュー環境をプロビジョニングする Microsoft Azure サブスクリプションから使用できる電子メール サーバー (Simple Mail Transfer Protocol \[SMTP\] サーバー) が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="02e03-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="02e03-108">サーバーの完全修飾ドメイン名 (FQDN)/IP アドレス、SMTP ポート番号、および認証の詳細が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="02e03-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="02e03-109">新しいオムニ チャネル画像を取り込んでデジタル資産管理機能を評価するに場合は、コンテンツ管理システム (CMS) テナントの名前を使用できるようにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="02e03-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="02e03-110">この名前を検索する手順については、このトピックの後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="02e03-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="02e03-111">>>>(Q: 手順はどこにありますか ?)</span><span class="sxs-lookup"><span data-stu-id="02e03-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="02e03-112">画像バックエンドのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02e03-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="02e03-113">メディア ベース URL の検索</span><span class="sxs-lookup"><span data-stu-id="02e03-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="02e03-114">この手順を完了する前に、[コマースでサイトを設定する](cpe-post-provisioning.md#set-up-your-site-in-commerce) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02e03-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="02e03-115">プロビジョニング中に E コマースを初期化したときに作成した URL を使用して、コマース サイト管理ツールにサインインします ([E コマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="02e03-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="02e03-116">**Fabrikam** サイトを開きます。</span><span class="sxs-lookup"><span data-stu-id="02e03-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="02e03-117">左側のメニューで、**資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="02e03-118">1 つの画像資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-118">Select any single image asset.</span></span>
1. <span data-ttu-id="02e03-119">右側のプロパティ インスペクターで、**公開 URL** プロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="02e03-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="02e03-120">値は URL です。</span><span class="sxs-lookup"><span data-stu-id="02e03-120">The value is a URL.</span></span> <span data-ttu-id="02e03-121">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="02e03-121">Here is an example:</span></span>

    <span data-ttu-id="02e03-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。</span><span class="sxs-lookup"><span data-stu-id="02e03-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="02e03-123">URL の最後の識別子 (前の例では **MA1nQC**) を文字列 **search?fileName=** と置換します。</span><span class="sxs-lookup"><span data-stu-id="02e03-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="02e03-124">この変更を行った後の URL の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="02e03-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="02e03-125">この URL は、メディア ベース URL です。</span><span class="sxs-lookup"><span data-stu-id="02e03-125">This URL is your media base URL.</span></span> <span data-ttu-id="02e03-126">記録しておいてください。</span><span class="sxs-lookup"><span data-stu-id="02e03-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="02e03-127">メディア ベース URL の更新</span><span class="sxs-lookup"><span data-stu-id="02e03-127">Update the media base URL</span></span>

1. <span data-ttu-id="02e03-128">Dynamics 365 Commerce へサインインします。</span><span class="sxs-lookup"><span data-stu-id="02e03-128">Sign in to Dynamics 365 Commerce.</span></span>
1. <span data-ttu-id="02e03-129">左側のメニューを使用して、**モジュール \> 小売りとコマース \> チャネルの設定 \> チャネル プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="02e03-129">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="02e03-130">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-130">Select **Edit**.</span></span>
1. <span data-ttu-id="02e03-131">**プロファイルのプロパティ**で、**メディア サーバー ベース URL** プロパティ値を、以前に作成したメディア ベース URL と置き換えます。</span><span class="sxs-lookup"><span data-stu-id="02e03-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="02e03-132">左側のリストの、**既定**のチャネルで、他のチャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="02e03-133">**プロファイル プロパティ**で、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="02e03-134">追加されたプロパティに対して、**メディア サーバー ベース URL** をプロパティ キーとして選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="02e03-135">プロパティ値として、以前に作成したメディア ベース URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="02e03-136">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="02e03-137">電子メール サーバーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02e03-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="02e03-138">ここで入力する SMTP サーバーまたは電子メール サービスは、環境に使用している Azure サブスクリプションからアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="02e03-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="02e03-139">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="02e03-139">Sign in to Commerce.</span></span>
1. <span data-ttu-id="02e03-140">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 電子メール \> 電子メール パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="02e03-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="02e03-141">**SMTP 設定**タブの、**送信メール サーバー** フィールドで、SMTP サーバーまたは電子メールサービスの FQDN または IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="02e03-142">**SMTP ポート番号**フィールドで、ポート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="02e03-143">(Secure Sockets Layer \[SSL\] を使用しない場合、既定のポート番号は **25** になります。)</span><span class="sxs-lookup"><span data-stu-id="02e03-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="02e03-144">認証が必要な場合は、**ユーザー名**および**パスワード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="02e03-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-145">Select **Save**.</span></span>
1. <span data-ttu-id="02e03-146">**更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="02e03-147">**テスト電子メール** タブの、**電子メール プロバイダー** フィールドで、**SMTP** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="02e03-148">**送信先**フィールドで、テスト電子メールの送信先となる電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="02e03-149">**テスト電子メールの送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="02e03-150">電子メール テンプレートのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02e03-150">Configure email templates</span></span>

<span data-ttu-id="02e03-151">電子メールを送信する各トランザクション イベントに関しては、有効な送信者の電子メール アドレスで電子メール テンプレートを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02e03-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="02e03-152">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="02e03-152">Sign in to Commerce.</span></span>
1. <span data-ttu-id="02e03-153">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 組織の電子メール テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="02e03-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="02e03-154">**リストを表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-154">Select **Show list**.</span></span>
1. <span data-ttu-id="02e03-155">リストの各テンプレートに関しては、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="02e03-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="02e03-156">**送信者電子メール** フィールドに、送信者の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="02e03-157">オプション: **送信者名**フィールドに、送信者名として使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="02e03-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="02e03-158">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="02e03-159">電子メール テンプレートのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="02e03-159">Customize email templates</span></span>

<span data-ttu-id="02e03-160">電子メール テンプレートをカスタマイズして、異なる画像を使用するようにできます。</span><span class="sxs-lookup"><span data-stu-id="02e03-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="02e03-161">またはテンプレートのリンクを更新して、プレビュー環境に移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="02e03-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="02e03-162">この手順では、既定のテンプレートをダウンロードし、システムのテンプレートを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="02e03-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="02e03-163">Web ブラウザーで、[Microsoft Dynamics 365 Commerce プレビューの既定の電子メール アドレス テンプレート ZIP ファイル](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) をローカル コンピューターにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="02e03-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="02e03-164">このファイルには、次の HTML ドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="02e03-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="02e03-165">注文確認モジュール テンプレート</span><span class="sxs-lookup"><span data-stu-id="02e03-165">Order confirmation template</span></span>
    - <span data-ttu-id="02e03-166">ギフト カード テンプレートの発行</span><span class="sxs-lookup"><span data-stu-id="02e03-166">Issue gift card template</span></span>
    - <span data-ttu-id="02e03-167">新しい注文テンプレート</span><span class="sxs-lookup"><span data-stu-id="02e03-167">New order template</span></span>
    - <span data-ttu-id="02e03-168">注文テンプレートのパック</span><span class="sxs-lookup"><span data-stu-id="02e03-168">Pack order template</span></span>
    - <span data-ttu-id="02e03-169">注文テンプレートのピック</span><span class="sxs-lookup"><span data-stu-id="02e03-169">Pick order template</span></span>

1. <span data-ttu-id="02e03-170">テキストまたは HTML エディターを使用してテンプレートをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="02e03-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="02e03-171">このトピックの後半にある、[サポートされているトークン](#supported-tokens-in-the-email-template) のリストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="02e03-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="02e03-172">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="02e03-172">Sign in to Commerce.</span></span>
1. <span data-ttu-id="02e03-173">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 組織の電子メール テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="02e03-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="02e03-174">左のリストを展開すると、すべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02e03-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="02e03-175">カスタマイズする各テンプレートに関しては、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="02e03-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="02e03-176">リストでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="02e03-177">**電子メール メッセージのコンテンツ**で、リストから適切な言語バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="02e03-178">(既定の言語は **en-us** です。)</span><span class="sxs-lookup"><span data-stu-id="02e03-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="02e03-179">**電子メール メッセージ コンテンツ**で、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="02e03-180">**電子メール テンプレートのアップロード** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02e03-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="02e03-181">**参照**を選択し、カスタマイズされたコンテンツを含む HTML ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="02e03-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="02e03-182">**アップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-182">Select **Upload**.</span></span> <span data-ttu-id="02e03-183">テンプレートがシステムにアップロードされ、プレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="02e03-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="02e03-184">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-184">Select **OK**.</span></span>
    1. <span data-ttu-id="02e03-185">オプション: テンプレートの**件名**プロパティをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="02e03-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="02e03-186">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02e03-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="02e03-187">電子メール テンプレートでサポートされているトークン</span><span class="sxs-lookup"><span data-stu-id="02e03-187">Supported tokens in the email template</span></span>

<span data-ttu-id="02e03-188">電子メールが表示されると、これらのトークンは顧客と顧客の注文に適用される実際の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="02e03-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="02e03-189">販売注文</span><span class="sxs-lookup"><span data-stu-id="02e03-189">Sales order</span></span>

<span data-ttu-id="02e03-190">次のトークンは、販売注文全体に適用されます。</span><span class="sxs-lookup"><span data-stu-id="02e03-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="02e03-191">トークンの名前</span><span class="sxs-lookup"><span data-stu-id="02e03-191">Name of the token</span></span> | <span data-ttu-id="02e03-192">トークン</span><span class="sxs-lookup"><span data-stu-id="02e03-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="02e03-193">注文番号</span><span class="sxs-lookup"><span data-stu-id="02e03-193">Order number</span></span>      | <span data-ttu-id="02e03-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="02e03-194">%salesid%</span></span> |
| <span data-ttu-id="02e03-195">顧客の名前</span><span class="sxs-lookup"><span data-stu-id="02e03-195">Customer's name</span></span>   | <span data-ttu-id="02e03-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="02e03-196">%customername%</span></span> |
| <span data-ttu-id="02e03-197">配送先住所</span><span class="sxs-lookup"><span data-stu-id="02e03-197">Delivery address</span></span>  | <span data-ttu-id="02e03-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="02e03-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="02e03-199">請求先住所</span><span class="sxs-lookup"><span data-stu-id="02e03-199">Billing address</span></span>   | <span data-ttu-id="02e03-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="02e03-200">%customeraddress%</span></span> |
| <span data-ttu-id="02e03-201">注文日付</span><span class="sxs-lookup"><span data-stu-id="02e03-201">Order date</span></span>        | <span data-ttu-id="02e03-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="02e03-202">%shipdate%</span></span> |
| <span data-ttu-id="02e03-203">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="02e03-203">Delivery mode</span></span>     | <span data-ttu-id="02e03-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="02e03-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="02e03-205">割引</span><span class="sxs-lookup"><span data-stu-id="02e03-205">Discount</span></span>          | <span data-ttu-id="02e03-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="02e03-206">%discount%</span></span> |
| <span data-ttu-id="02e03-207">売上税</span><span class="sxs-lookup"><span data-stu-id="02e03-207">Sales tax</span></span>         | <span data-ttu-id="02e03-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="02e03-208">%tax%</span></span> |
| <span data-ttu-id="02e03-209">注文合計</span><span class="sxs-lookup"><span data-stu-id="02e03-209">Order total</span></span>       | <span data-ttu-id="02e03-210">%total%</span><span class="sxs-lookup"><span data-stu-id="02e03-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="02e03-211">販売明細行</span><span class="sxs-lookup"><span data-stu-id="02e03-211">Sales line</span></span>

<span data-ttu-id="02e03-212">次のトークンは、注文の各製品の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="02e03-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="02e03-213">**製品リスト - 開始**トークンを各製品に対して繰り返される HTML ブロックの先頭に、**製品リスト - 終了**トークンをブロックの末尾に配置します。</span><span class="sxs-lookup"><span data-stu-id="02e03-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="02e03-214">トークンの名前</span><span class="sxs-lookup"><span data-stu-id="02e03-214">Name of the token</span></span>      | <span data-ttu-id="02e03-215">トークン</span><span class="sxs-lookup"><span data-stu-id="02e03-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="02e03-216">製品リスト - 開始</span><span class="sxs-lookup"><span data-stu-id="02e03-216">Product list - start</span></span>   | <span data-ttu-id="02e03-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="02e03-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="02e03-218">Product list - 終了</span><span class="sxs-lookup"><span data-stu-id="02e03-218">Product list - end</span></span>     | <span data-ttu-id="02e03-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="02e03-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="02e03-220">製品名</span><span class="sxs-lookup"><span data-stu-id="02e03-220">Product name</span></span>           | <span data-ttu-id="02e03-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="02e03-221">%lineproductname%</span></span> |
| <span data-ttu-id="02e03-222">説明</span><span class="sxs-lookup"><span data-stu-id="02e03-222">Description</span></span>            | <span data-ttu-id="02e03-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="02e03-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="02e03-224">件数</span><span class="sxs-lookup"><span data-stu-id="02e03-224">Quantity</span></span>               | <span data-ttu-id="02e03-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="02e03-225">%linequantity%</span></span> |
| <span data-ttu-id="02e03-226">明細行の単価</span><span class="sxs-lookup"><span data-stu-id="02e03-226">Line unit price</span></span>        | <span data-ttu-id="02e03-227">%lineprice% (確認)</span><span class="sxs-lookup"><span data-stu-id="02e03-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="02e03-228">明細行の品目合計</span><span class="sxs-lookup"><span data-stu-id="02e03-228">line item total</span></span>        | <span data-ttu-id="02e03-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="02e03-229">%linenetamount%</span></span> |
| <span data-ttu-id="02e03-230">明細行割引</span><span class="sxs-lookup"><span data-stu-id="02e03-230">line discount</span></span>          | <span data-ttu-id="02e03-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="02e03-231">%linediscount%</span></span> |
| <span data-ttu-id="02e03-232">出荷日</span><span class="sxs-lookup"><span data-stu-id="02e03-232">Ship date</span></span>              | <span data-ttu-id="02e03-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="02e03-233">%lineshipdate%</span></span> |
| <span data-ttu-id="02e03-234">調達方法</span><span class="sxs-lookup"><span data-stu-id="02e03-234">Procurement method</span></span>     | <span data-ttu-id="02e03-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="02e03-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="02e03-236">配送先住所</span><span class="sxs-lookup"><span data-stu-id="02e03-236">delivery address</span></span>       | <span data-ttu-id="02e03-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="02e03-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="02e03-238">明細行の販売単位</span><span class="sxs-lookup"><span data-stu-id="02e03-238">Sales unit of the line</span></span> | <span data-ttu-id="02e03-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="02e03-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="02e03-240">追加リソース</span><span class="sxs-lookup"><span data-stu-id="02e03-240">Additional resources</span></span>

[<span data-ttu-id="02e03-241">Dynamics 365 Commerce プレビュー環境の概要</span><span class="sxs-lookup"><span data-stu-id="02e03-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="02e03-242">Dynamics 365 Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="02e03-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="02e03-243">Dynamics 365 Commerce レビュー環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="02e03-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="02e03-244">Dynamics 365 Commerce プレビュー環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="02e03-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="02e03-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="02e03-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="02e03-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="02e03-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="02e03-247">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="02e03-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="02e03-248">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="02e03-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
