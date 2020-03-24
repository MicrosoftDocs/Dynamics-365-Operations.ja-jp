---
title: Attract の電子メール設定のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Talent - Attract で送信される電子メールの構成方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: e641e3f0d1873d91be1a1dc9bc22eb734a2b21d5
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124730"
---
# <a name="configure-email-settings-in-attract"></a><span data-ttu-id="f39fe-103">Attract の電子メール設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f39fe-103">Configure email settings in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f39fe-104">ブランドは信頼を確立し、候補者がポジションに応募する前に、候補者との関係を構築するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-104">Your brand establishes trust and helps you build a relationship with candidates before they even apply for your positions.</span></span> <span data-ttu-id="f39fe-105">ポジティブなブランド認識は、優秀な人材を引き付け、既に在籍している従業員のロイヤルティを高めます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-105">Positive brand perception attracts top talent and increases the loyalty of existing employees.</span></span> <span data-ttu-id="f39fe-106">Microsoft Dynamics 365 Talent: Attract を使用すると、会社のブランドを反映するように電子メールを構成できます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-106">Microsoft Dynamics 365 Talent: Attract lets you configure emails so that they reflect your company's brand.</span></span> <span data-ttu-id="f39fe-107">したがって、職務候補者が応募プロセスを進めていくにつれて、候補者に一貫したエクスペリエンスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-107">Therefore, you can provide a consistent experience to job candidates as they progress through the application process.</span></span>

<span data-ttu-id="f39fe-108">Attract を使用すると、次のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-108">Attract lets you perform these actions:</span></span>

- <span data-ttu-id="f39fe-109">会社の Microsoft Exchange 電子メール サービス アカウントが使用されるように電子メールの設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f39fe-109">Configure email settings so that your company's Microsoft Exchange email service account is used.</span></span> <span data-ttu-id="f39fe-110">このようにして、候補者は電子メールがあなたの会社から送られているということを認知します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-110">In this way, candidates know that the emails are coming from your company.</span></span> <span data-ttu-id="f39fe-111">たとえば、候補者が `contoso@microsoft.com` の代わりに、`recruiting@contoso.com` から電子メールを受け取るように設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-111">For example, you can configure your settings so that candidates receive emails from `recruiting@contoso.com` instead of `contoso@microsoft.com`.</span></span>
- <span data-ttu-id="f39fe-112">電子メール テンプレートにグローバル ヘッダーおよびフッターを設定することで、すべての電子メール通信に一貫したブランドを作成します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-112">Create consistent branding for all your email communications by setting a global header and footer for email templates.</span></span> 

> [!NOTE]
> <span data-ttu-id="f39fe-113">会社の電子メール サービス アカウントを使用して電子メールを送信できるようにするためには、包括採用アドオンが必要です。</span><span class="sxs-lookup"><span data-stu-id="f39fe-113">To configure Attract so that it uses your company's email service account to send email, you need the Comprehensive hiring add-on.</span></span>

## <a name="connect-an-email-service-account"></a><span data-ttu-id="f39fe-114">電子メール サービス アカウントの接続</span><span class="sxs-lookup"><span data-stu-id="f39fe-114">Connect an email service account</span></span>

<span data-ttu-id="f39fe-115">会社の電子メールサービス アカウントを接続することにより、求職者に対してブランド化された電子メール エクスペリエンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-115">By connecting your company's email service account, you can create a branded email experience for your job candidates.</span></span> <span data-ttu-id="f39fe-116">会社のアカウントに接続していない場合、Attract は既定の Microsoft ブランドの電子メール サービス アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-116">If you don't connect your company account, Attract uses the default Microsoft-branded email service account.</span></span>

1. <span data-ttu-id="f39fe-117">**設定** (右上隅にあるギヤ記号) を選択してから、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-117">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="f39fe-118">**電子メール設定**タブの**電子メール サービス アカウント**で、**会社のアカウントへの接続**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-118">On the **Email settings** tab, under **Email service accounts**, select **Connect a company account**.</span></span>

    ![会社の電子メール サービス アカウントを Attract に接続する](./media/attract-admin-email-service-accounts.png)

    <span data-ttu-id="f39fe-120">共有メール アカウントの作成方法については、[Exchange Online の共有メールボックス](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f39fe-120">For more information about how to create a shared email account, see [Shared mailboxes in Exchange Online](https://docs.microsoft.com/exchange/collaboration-exo/shared-mailboxes).</span></span>

3. <span data-ttu-id="f39fe-121">Microsoft のサインイン ウィンドウで、会社の資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="f39fe-121">In the Microsoft sign-in window, sign in by using your corporate credentials.</span></span>
4. <span data-ttu-id="f39fe-122">まだ電子メール サービス アカウントを設定していない場合、または新しいアカウントを追加する場合は**新しいサービス アカウントの追加**を選択し、電子メール情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-122">If you haven't yet set up an email service account, or if you want to add a new one, select **Add new service account**, and then enter your email information.</span></span> <span data-ttu-id="f39fe-123">使用する電子メール サービス アカウントを既に設定している場合は、それを選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-123">If you've already set up the email service account that you want to use, select it.</span></span>

<span data-ttu-id="f39fe-124">電子メール サービス アカウントのコンフィギュレーションが正常に完了すると、**電子メール サービス アカウント**の下に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-124">When your email service account is successfully configured, you will see it listed under **Email service accounts**.</span></span>

## <a name="disconnect-an-email-service-account"></a><span data-ttu-id="f39fe-125">電子メール サービス アカウントの接続解除</span><span class="sxs-lookup"><span data-stu-id="f39fe-125">Disconnect an email service account</span></span>

<span data-ttu-id="f39fe-126">Attract を使用した電子メール通信で会社のドメインの使用を中止したい場合は、電子メール サービス アカウントを接続解除できます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-126">If you want to stop using your company's domain in email communications through Attract, you can disconnect an email service account.</span></span>

1. <span data-ttu-id="f39fe-127">**設定** (右上隅にあるギヤ記号) を選択してから、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-127">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="f39fe-128">**電子メール設定**タブの**電子メール サービス アカウント**で、接続を解除する電子メール サービス アカウントの横にある**詳細**ボタン (縦の 3 つの点) を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-128">On the **Email settings** tab, under **Email service accounts**, select the **More** button (three vertical dots) next to the email service account that you want to disconnect.</span></span>
3. <span data-ttu-id="f39fe-129">**電子メール アカウントの接続解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-129">Select **Disconnect email account**.</span></span>

    ![会社の電子メール サービス アカウントを接続解除する](./media/attract-admin-disconnect-email-account.png)

4. <span data-ttu-id="f39fe-131">操作を確認するメッセージが表示されたら、**接続解除**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-131">When you're prompted to confirm the operation, select **Disconnect**.</span></span>

    ![会社の電子メール サービス アカウントの接続解除を確認する](./media/attract-admin-email-confirm-disconnect.png)

<span data-ttu-id="f39fe-133">別の電子メール サービス アカウントに接続しない場合、Attract から送信された電子メールには、既定の Microsoft ブランドの電子メール サービス アカウントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-133">If you don't connect a different email service account, emails that are sent from Attract will use the default Microsoft-branded email service account.</span></span>

## <a name="configure-email-template-settings"></a><span data-ttu-id="f39fe-134">電子メール テンプレート設定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f39fe-134">Configure email template settings</span></span>

<span data-ttu-id="f39fe-135">会社のロゴの画像やその他の情報を、ブランド化されたヘッダーとして電子メールにアップロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-135">You can upload an image of your company's logo and other information as a branded header for your emails.</span></span> <span data-ttu-id="f39fe-136">また、プライバシー ポリシーおよび使用条件へのリンクを、電子メール フッターで提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-136">You can also provide links to your privacy policy and terms of use in email footers.</span></span>

> [!NOTE]
> <span data-ttu-id="f39fe-137">お客様は、ご自身の所在国や地域における法律、および電子メールの受信者の所在国や地域における法律を遵守する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f39fe-137">You must comply with all applicable laws of your country or region, and also the country or region that governs the email recipient.</span></span> <span data-ttu-id="f39fe-138">これらの法律には、スパム規制が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f39fe-138">These laws include anti-spam regulations.</span></span>

1. <span data-ttu-id="f39fe-139">**設定** (右上隅にあるギヤ記号) を選択してから、**管理センター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-139">Select **Settings** (the gear symbol in the upper-right corner), and then select **Admin center**.</span></span>
2. <span data-ttu-id="f39fe-140">**メール設定**タブの**電子メール テンプレート設定**で、メール ヘッダーとして使用する画像をイメージ ボックスにドラッグするか、イメージ ボックスをクリックしてファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-140">On the **Email settings** tab, under **Email template settings**, drag the image that you want to use as your email header into the image box, or click in the image box to browse for the file.</span></span> <span data-ttu-id="f39fe-141">既存の画像を置き換えるには、まずその横にある**削除**を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f39fe-141">To replace an existing image, you must first select **Remove** next to it.</span></span> <span data-ttu-id="f39fe-142">画像は、JPEG、JPG、PNG、または SVG ファイルにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f39fe-142">The image must be a JPEG, JPG, PNG, or SVG file.</span></span> <span data-ttu-id="f39fe-143">推奨される画像のサイズは、幅 25 ~ 800 ピクセルで、高さが 25 ~ 150 ピクセルです。</span><span class="sxs-lookup"><span data-stu-id="f39fe-143">The recommended size for images is between 25 and 800 pixels wide, and between 25 and 150 pixels high.</span></span> <span data-ttu-id="f39fe-144">ヘッダーの最大ファイル サイズは 1 メガ バイト (MB) です。</span><span class="sxs-lookup"><span data-stu-id="f39fe-144">The maximum file size for the header is 1 megabyte (MB).</span></span>

    ![会社の電子メール ヘッダーの画像の追加](./media/attract-admin-email-header.png)

3. <span data-ttu-id="f39fe-146">**通信に関するプライバシー ポリシー**には、会社のプライバシー ポリシーへのリンクを記載してください。</span><span class="sxs-lookup"><span data-stu-id="f39fe-146">Under **Your Privacy policy for communications**, provide a link to your company's privacy policy.</span></span> <span data-ttu-id="f39fe-147">**通信に関する使用条件**には、会社の使用条件へのリンクを記載してください。</span><span class="sxs-lookup"><span data-stu-id="f39fe-147">Under **Your Terms and conditions for communication**, provide a link to your company's terms of use.</span></span>

    ![会社のプライバシー ポリシーおよび電子メール フッターの使用条件へのリンクを追加する](./media/attract-admin-email-footer.png)

4. <span data-ttu-id="f39fe-149">**保存**を選択して、電子メール テンプレート設定を保存します。</span><span class="sxs-lookup"><span data-stu-id="f39fe-149">Select **Save** to save your email template settings.</span></span>
