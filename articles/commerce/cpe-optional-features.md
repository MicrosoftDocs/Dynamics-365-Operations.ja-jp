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
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024732"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="6aaf9-103">Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6aaf9-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6aaf9-104">このトピックでは、Microsoft Dynamics 365 Commerce のプレビュー環境のオプション機能をコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6aaf9-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="6aaf9-105">Prerequisites</span></span>

<span data-ttu-id="6aaf9-106">トランザクション電子メール機能を評価する場合、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="6aaf9-107">プレビュー環境をプロビジョニングする Microsoft Azure サブスクリプションから使用できる電子メール サーバー (Simple Mail Transfer Protocol \[SMTP\] サーバー) が使用可能です。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="6aaf9-108">サーバーの完全修飾ドメイン名 (FQDN)/IP アドレス、SMTP ポート番号、および認証の詳細が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="6aaf9-109">新しいオムニ チャネル画像を取り込んでデジタル資産管理機能を評価するに場合は、コンテンツ管理システム (CMS) テナントの名前を使用できるようにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="6aaf9-110">この名前を検索する手順については、このトピックの後半で説明します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="6aaf9-111">>>>(Q: 手順はどこにありますか ?)</span><span class="sxs-lookup"><span data-stu-id="6aaf9-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="6aaf9-112">画像バックエンドのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6aaf9-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="6aaf9-113">メディア ベース URL の検索</span><span class="sxs-lookup"><span data-stu-id="6aaf9-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="6aaf9-114">この手順を完了する前に、[コマースでサイトを設定する](cpe-post-provisioning.md#set-up-your-site-in-commerce) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="6aaf9-115">プロビジョニング中に E コマースを初期化したときに作成した URL を使用して、コマース サイト管理ツールにサインインします ([E コマースの初期化](provisioning-guide.md#initialize-e-commerce) を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="6aaf9-116">**Fabrikam** サイトを開きます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="6aaf9-117">左側のメニューで、**資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="6aaf9-118">1 つの画像資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-118">Select any single image asset.</span></span>
1. <span data-ttu-id="6aaf9-119">右側のプロパティ インスペクターで、**公開 URL** プロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="6aaf9-120">値は URL です。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-120">The value is a URL.</span></span> <span data-ttu-id="6aaf9-121">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-121">Here is an example:</span></span>

    <span data-ttu-id="6aaf9-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="6aaf9-123">URL の最後の識別子 (前の例では **MA1nQC**) を文字列 **search?fileName=** と置換します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="6aaf9-124">この変更を行った後の URL の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="6aaf9-125">この URL は、メディア ベース URL です。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-125">This URL is your media base URL.</span></span> <span data-ttu-id="6aaf9-126">記録しておいてください。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="6aaf9-127">メディア ベース URL の更新</span><span class="sxs-lookup"><span data-stu-id="6aaf9-127">Update the media base URL</span></span>

1. <span data-ttu-id="6aaf9-128">Dynamics 365 Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="6aaf9-129">左側にあるメニューを使用して、**モジュール \> Retail \> チャネルの設定 \> チャネルのプロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="6aaf9-130">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-130">Select **Edit**.</span></span>
1. <span data-ttu-id="6aaf9-131">**プロファイルのプロパティ**で、**メディア サーバー ベース URL** プロパティ値を、以前に作成したメディア ベース URL と置き換えます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="6aaf9-132">左側のリストの、**既定**のチャネルで、他のチャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="6aaf9-133">**プロファイル プロパティ**で、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="6aaf9-134">追加されたプロパティに対して、**メディア サーバー ベース URL** をプロパティ キーとして選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="6aaf9-135">プロパティ値として、以前に作成したメディア ベース URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="6aaf9-136">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="6aaf9-137">電子メール サーバーのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6aaf9-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="6aaf9-138">ここで入力する SMTP サーバーまたは電子メール サービスは、環境に使用している Azure サブスクリプションからアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="6aaf9-139">Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="6aaf9-140">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 電子メール \> 電子メール パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="6aaf9-141">**SMTP 設定**タブの、**送信メール サーバー** フィールドで、SMTP サーバーまたは電子メールサービスの FQDN または IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="6aaf9-142">**SMTP ポート番号**フィールドで、ポート番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="6aaf9-143">(Secure Sockets Layer \[SSL\] を使用しない場合、既定のポート番号は **25** になります。)</span><span class="sxs-lookup"><span data-stu-id="6aaf9-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="6aaf9-144">認証が必要な場合は、**ユーザー名**および**パスワード** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="6aaf9-145">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-145">Select **Save**.</span></span>
1. <span data-ttu-id="6aaf9-146">**更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="6aaf9-147">**テスト電子メール** タブの、**電子メール プロバイダー** フィールドで、**SMTP** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="6aaf9-148">**送信先**フィールドで、テスト電子メールの送信先となる電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="6aaf9-149">**テスト電子メールの送信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="6aaf9-150">電子メール テンプレートのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6aaf9-150">Configure email templates</span></span>

<span data-ttu-id="6aaf9-151">電子メールを送信する各トランザクション イベントに関しては、有効な送信者の電子メール アドレスで電子メール テンプレートを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="6aaf9-152">Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="6aaf9-153">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 組織の電子メール テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="6aaf9-154">**リストを表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-154">Select **Show list**.</span></span>
1. <span data-ttu-id="6aaf9-155">リストの各テンプレートに関しては、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="6aaf9-156">**送信者電子メール** フィールドに、送信者の電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="6aaf9-157">オプション: **送信者名**フィールドに、送信者名として使用する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="6aaf9-158">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="6aaf9-159">電子メール テンプレートのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="6aaf9-159">Customize email templates</span></span>

<span data-ttu-id="6aaf9-160">電子メール テンプレートをカスタマイズして、異なる画像を使用するようにできます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="6aaf9-161">またはテンプレートのリンクを更新して、プレビュー環境に移動することもできます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="6aaf9-162">この手順では、既定のテンプレートをダウンロードし、システムのテンプレートを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="6aaf9-163">Web ブラウザーで、[Microsoft Dynamics 365 Commerce プレビューの既定の電子メール アドレス テンプレート ZIP ファイル](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) をローカル コンピューターにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="6aaf9-164">このファイルには、次の HTML ドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="6aaf9-165">注文確認モジュール テンプレート</span><span class="sxs-lookup"><span data-stu-id="6aaf9-165">Order confirmation template</span></span>
    - <span data-ttu-id="6aaf9-166">ギフト カード テンプレートの発行</span><span class="sxs-lookup"><span data-stu-id="6aaf9-166">Issue gift card template</span></span>
    - <span data-ttu-id="6aaf9-167">新しい注文テンプレート</span><span class="sxs-lookup"><span data-stu-id="6aaf9-167">New order template</span></span>
    - <span data-ttu-id="6aaf9-168">注文テンプレートのパック</span><span class="sxs-lookup"><span data-stu-id="6aaf9-168">Pack order template</span></span>
    - <span data-ttu-id="6aaf9-169">注文テンプレートのピック</span><span class="sxs-lookup"><span data-stu-id="6aaf9-169">Pick order template</span></span>

1. <span data-ttu-id="6aaf9-170">テキストまたは HTML エディターを使用してテンプレートをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="6aaf9-171">このトピックの後半にある、[サポートされているトークン](#supported-tokens-in-the-email-template) のリストを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="6aaf9-172">Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="6aaf9-173">左側にあるメニューを使用して、**モジュール \> 組織管理者 \> 設定 \> 組織の電子メール テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="6aaf9-174">左のリストを展開すると、すべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="6aaf9-175">カスタマイズする各テンプレートに関しては、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="6aaf9-176">リストでテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="6aaf9-177">**電子メール メッセージのコンテンツ**で、リストから適切な言語バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="6aaf9-178">(既定の言語は **en-us** です。)</span><span class="sxs-lookup"><span data-stu-id="6aaf9-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="6aaf9-179">**電子メール メッセージ コンテンツ**で、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="6aaf9-180">**電子メール テンプレートのアップロード** ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="6aaf9-181">**参照**を選択し、カスタマイズされたコンテンツを含む HTML ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="6aaf9-182">**アップロード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-182">Select **Upload**.</span></span> <span data-ttu-id="6aaf9-183">テンプレートがシステムにアップロードされ、プレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="6aaf9-184">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-184">Select **OK**.</span></span>
    1. <span data-ttu-id="6aaf9-185">オプション: テンプレートの**件名**プロパティをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="6aaf9-186">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="6aaf9-187">電子メール テンプレートでサポートされているトークン</span><span class="sxs-lookup"><span data-stu-id="6aaf9-187">Supported tokens in the email template</span></span>

<span data-ttu-id="6aaf9-188">電子メールが表示されると、これらのトークンは顧客と顧客の注文に適用される実際の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="6aaf9-189">販売注文</span><span class="sxs-lookup"><span data-stu-id="6aaf9-189">Sales order</span></span>

<span data-ttu-id="6aaf9-190">次のトークンは、販売注文全体に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="6aaf9-191">トークンの名前</span><span class="sxs-lookup"><span data-stu-id="6aaf9-191">Name of the token</span></span> | <span data-ttu-id="6aaf9-192">トークン</span><span class="sxs-lookup"><span data-stu-id="6aaf9-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="6aaf9-193">注文番号</span><span class="sxs-lookup"><span data-stu-id="6aaf9-193">Order number</span></span>      | <span data-ttu-id="6aaf9-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-194">%salesid%</span></span> |
| <span data-ttu-id="6aaf9-195">顧客の名前</span><span class="sxs-lookup"><span data-stu-id="6aaf9-195">Customer's name</span></span>   | <span data-ttu-id="6aaf9-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-196">%customername%</span></span> |
| <span data-ttu-id="6aaf9-197">配送先住所</span><span class="sxs-lookup"><span data-stu-id="6aaf9-197">Delivery address</span></span>  | <span data-ttu-id="6aaf9-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="6aaf9-199">請求先住所</span><span class="sxs-lookup"><span data-stu-id="6aaf9-199">Billing address</span></span>   | <span data-ttu-id="6aaf9-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-200">%customeraddress%</span></span> |
| <span data-ttu-id="6aaf9-201">注文日付</span><span class="sxs-lookup"><span data-stu-id="6aaf9-201">Order date</span></span>        | <span data-ttu-id="6aaf9-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-202">%shipdate%</span></span> |
| <span data-ttu-id="6aaf9-203">荷渡方法</span><span class="sxs-lookup"><span data-stu-id="6aaf9-203">Delivery mode</span></span>     | <span data-ttu-id="6aaf9-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="6aaf9-205">割引</span><span class="sxs-lookup"><span data-stu-id="6aaf9-205">Discount</span></span>          | <span data-ttu-id="6aaf9-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-206">%discount%</span></span> |
| <span data-ttu-id="6aaf9-207">売上税</span><span class="sxs-lookup"><span data-stu-id="6aaf9-207">Sales tax</span></span>         | <span data-ttu-id="6aaf9-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-208">%tax%</span></span> |
| <span data-ttu-id="6aaf9-209">注文合計</span><span class="sxs-lookup"><span data-stu-id="6aaf9-209">Order total</span></span>       | <span data-ttu-id="6aaf9-210">%total%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="6aaf9-211">販売明細行</span><span class="sxs-lookup"><span data-stu-id="6aaf9-211">Sales line</span></span>

<span data-ttu-id="6aaf9-212">次のトークンは、注文の各製品の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="6aaf9-213">**製品リスト - 開始**トークンを各製品に対して繰り返される HTML ブロックの先頭に、**製品リスト - 終了**トークンをブロックの末尾に配置します。</span><span class="sxs-lookup"><span data-stu-id="6aaf9-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="6aaf9-214">トークンの名前</span><span class="sxs-lookup"><span data-stu-id="6aaf9-214">Name of the token</span></span>      | <span data-ttu-id="6aaf9-215">トークン</span><span class="sxs-lookup"><span data-stu-id="6aaf9-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="6aaf9-216">製品リスト - 開始</span><span class="sxs-lookup"><span data-stu-id="6aaf9-216">Product list - start</span></span>   | <span data-ttu-id="6aaf9-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="6aaf9-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="6aaf9-218">Product list - 終了</span><span class="sxs-lookup"><span data-stu-id="6aaf9-218">Product list - end</span></span>     | <span data-ttu-id="6aaf9-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="6aaf9-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="6aaf9-220">製品名</span><span class="sxs-lookup"><span data-stu-id="6aaf9-220">Product name</span></span>           | <span data-ttu-id="6aaf9-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-221">%lineproductname%</span></span> |
| <span data-ttu-id="6aaf9-222">説明</span><span class="sxs-lookup"><span data-stu-id="6aaf9-222">Description</span></span>            | <span data-ttu-id="6aaf9-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="6aaf9-224">件数</span><span class="sxs-lookup"><span data-stu-id="6aaf9-224">Quantity</span></span>               | <span data-ttu-id="6aaf9-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-225">%linequantity%</span></span> |
| <span data-ttu-id="6aaf9-226">明細行の単価</span><span class="sxs-lookup"><span data-stu-id="6aaf9-226">Line unit price</span></span>        | <span data-ttu-id="6aaf9-227">%lineprice% (確認)</span><span class="sxs-lookup"><span data-stu-id="6aaf9-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="6aaf9-228">明細行の品目合計</span><span class="sxs-lookup"><span data-stu-id="6aaf9-228">line item total</span></span>        | <span data-ttu-id="6aaf9-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-229">%linenetamount%</span></span> |
| <span data-ttu-id="6aaf9-230">明細行割引</span><span class="sxs-lookup"><span data-stu-id="6aaf9-230">line discount</span></span>          | <span data-ttu-id="6aaf9-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-231">%linediscount%</span></span> |
| <span data-ttu-id="6aaf9-232">出荷日</span><span class="sxs-lookup"><span data-stu-id="6aaf9-232">Ship date</span></span>              | <span data-ttu-id="6aaf9-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-233">%lineshipdate%</span></span> |
| <span data-ttu-id="6aaf9-234">調達方法</span><span class="sxs-lookup"><span data-stu-id="6aaf9-234">Procurement method</span></span>     | <span data-ttu-id="6aaf9-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="6aaf9-236">配送先住所</span><span class="sxs-lookup"><span data-stu-id="6aaf9-236">delivery address</span></span>       | <span data-ttu-id="6aaf9-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="6aaf9-238">明細行の販売単位</span><span class="sxs-lookup"><span data-stu-id="6aaf9-238">Sales unit of the line</span></span> | <span data-ttu-id="6aaf9-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="6aaf9-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="6aaf9-240">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6aaf9-240">Additional resources</span></span>

[<span data-ttu-id="6aaf9-241">Dynamics 365 Commerce プレビュー環境の概要</span><span class="sxs-lookup"><span data-stu-id="6aaf9-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="6aaf9-242">Dynamics 365 Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="6aaf9-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="6aaf9-243">Dynamics 365 Commerce レビュー環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6aaf9-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="6aaf9-244">Dynamics 365 Commerce プレビュー環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="6aaf9-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="6aaf9-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="6aaf9-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="6aaf9-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="6aaf9-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="6aaf9-247">Microsoft Azure ポータル</span><span class="sxs-lookup"><span data-stu-id="6aaf9-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="6aaf9-248">Dynamics 365 Commerce Web サイト</span><span class="sxs-lookup"><span data-stu-id="6aaf9-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
