---
title: 電子メールのコンフィギュレーションと送信
description: 電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。
author: ChrisGarty
manager: AnnBe
ms.date: 07/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysEmailParameters
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 268274
ms.assetid: 194ca8fd-5e20-4464-9c85-08d2b5ff63ca
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 162825ac589c98a062c8c5c5a80cb51bd78a8ee9
ms.sourcegitcommit: 6c4fab381c8974e9aef4421058f31c9917806a45
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/24/2019
ms.locfileid: "1788322"
---
# <a name="configure-and-send-email"></a><span data-ttu-id="f3d7b-103">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="f3d7b-103">Configure and send email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3d7b-104">電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-104">The behavior of the email subsystem is influenced by a combination of administrator configuration, user configuration, and user choices.</span></span> <span data-ttu-id="f3d7b-105">このトピックは、管理者のセクションとユーザーのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-105">This topic is divided into sections for administrators and users.</span></span> <span data-ttu-id="f3d7b-106">このトピックでは、関連情報を見つけやすくするために、管理者のセクションとユーザーのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-106">This topic is divided into sections for administrators and users to make it easy to find relevant information.</span></span>

<span data-ttu-id="f3d7b-107">Dynamics 365 for Finance and Operations では、管理者とユーザーの両方が電子メールのサブシステムの動作を設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-107">In Dynamics 365 for Finance and Operations both administrators and users set the behavior of the email subsystem.</span></span>

## <a name="administrator-email-parameters-page"></a><span data-ttu-id="f3d7b-108">管理者: 電子メール パラメーター ページ</span><span class="sxs-lookup"><span data-stu-id="f3d7b-108">Administrator: Email parameters page</span></span>

<span data-ttu-id="f3d7b-109">**電子メール パラメーター**ページの、**電子メール プロバイダー**タブで、次の設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-109">On the **Email parameters** page, note the following settings on the **Email providers** tab.</span></span>

| <span data-ttu-id="f3d7b-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="f3d7b-110">Field</span></span>                 | <span data-ttu-id="f3d7b-111">説明</span><span class="sxs-lookup"><span data-stu-id="f3d7b-111">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f3d7b-112">バッチ電子メール プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f3d7b-112">Batch email provider</span></span>  | <span data-ttu-id="f3d7b-113">バッチ方式または非対話型のプロセスで送信される電子メールの送信に使用される電子メール プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-113">Specifies which email provider will be used to send emails that are sent by processes in a batch or non-interactive manner.</span></span> <span data-ttu-id="f3d7b-114">Exchange プロバイダーは、バッチ プロセスに関連付けられているアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-114">The Exchange provider will use the account associated with the batch process.</span></span> |
| <span data-ttu-id="f3d7b-115">添付ファイル サイズの上限</span><span class="sxs-lookup"><span data-stu-id="f3d7b-115">Attachment size limit</span></span> | <span data-ttu-id="f3d7b-116">電子メール サブシステム経由で送信できる 1 つの電子メールの最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-116">Specifies the maximum size of a single email that can be sent via the email subsystem.</span></span> |

<span data-ttu-id="f3d7b-117">**電子メール パラメーター**ページの、**SMTP 設定**タブで、次の設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-117">On the **Email parameters** page, note the following settings on the **SMTP settings** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f3d7b-118">フィールド</span><span class="sxs-lookup"><span data-stu-id="f3d7b-118">Field</span></span></th>
<th><span data-ttu-id="f3d7b-119">説明</span><span class="sxs-lookup"><span data-stu-id="f3d7b-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f3d7b-120">送信メール サーバー</span><span class="sxs-lookup"><span data-stu-id="f3d7b-120">Outgoing mail server</span></span></td>
<td><span data-ttu-id="f3d7b-121">目的の SMTP サーバーのホスト名。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-121">The host name of the desired SMTP server.</span></span>
<ul>
<li><span data-ttu-id="f3d7b-122"><a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Office 365 製品</a> (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-122">For <a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Office 365 production</a> (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="f3d7b-123">(<strong>設定</strong> &gt; <strong>メール</strong> &gt; <strong>POP および IMAP</strong>の outlook.office.com でこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="f3d7b-123">(You can find this setting at outlook.office.com at <strong>Settings</strong> &gt; <strong>Mail</strong> &gt; <strong>POP and IMAP</strong>.)</span></span></li>
<li><span data-ttu-id="f3d7b-124">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-124">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="f3d7b-125">SMTP ポート番号</span><span class="sxs-lookup"><span data-stu-id="f3d7b-125">SMTP port number</span></span></td>
<td><span data-ttu-id="f3d7b-126">通常、セキュリティで保護して送信するためにポート番号は 587 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-126">Typically, the port number should be set to 587 for secure transport.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f3d7b-127"><strong>ユーザー名</strong>と<strong>パスワード</strong></span><span class="sxs-lookup"><span data-stu-id="f3d7b-127"><strong>User name</strong> and <strong>Password</strong></span></span></td>
<td><span data-ttu-id="f3d7b-128">必要に応じて、適切なメール アカウントを使用して電子メールの送信を指定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-128">Specify, as needed, to send the email via the appropriate mail account.</span></span> <span data-ttu-id="f3d7b-129">すべてのユーザーは SMTP アカウントを指定し <strong>送信者</strong>および <strong>代理送信</strong>許可をし、Simple Mail Transfer Protocol (SMTP) で送信する機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-129">All users need to provide the SMTP account <strong>Send As</strong> and <strong>Send On Behalf Of</strong> permissions to enable the ability to send Simple Mail Transfer Protocol (SMTP) mail.</span></span> <span data-ttu-id="f3d7b-130">Send As 権限は、Office 365 管理センター (portal.office.com/Admin) にて、<strong>ユーザー</strong> &gt; <strong>有効なユーザー</strong> &gt; <strong>ユーザー</strong> &gt; <strong>メールボックスのアクセス許可を編集</strong> &gt; <strong>このメールボックスから電子メールを送信する</strong> で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-130">You can configure Send As permissions in the Office 365 admin center (portal.office.com/Admin), at <strong>Users</strong> &gt; <strong>Active users</strong> &gt; <strong>User</strong> &gt; <strong>Edit mailbox permissions</strong> &gt; <strong>Send email from this mailbox</strong>.</span></span> <span data-ttu-id="f3d7b-131">詳細については、<a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-131">For more information, see <a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Enable sending email from another user's mailbox in Office 365</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f3d7b-132">SSL が必須かどうかを指定します</span><span class="sxs-lookup"><span data-stu-id="f3d7b-132">Specify if SSL is required</span></span></td>
<td><span data-ttu-id="f3d7b-133">安全なトランスポートをを使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-133">Determines whether secure transport is used.</span></span> <span data-ttu-id="f3d7b-134">これは通常、内部またはトラブルシューティングのシナリオを除き、<strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-134">Typically, this is <strong>Yes</strong>, except for internal or troubleshooting scenarios.</span></span></td>
</tr>
</tbody>
</table>

## <a name="administrator-email-distributor-batch-process"></a><span data-ttu-id="f3d7b-135">管理者: 電子メール配布バッチ処理</span><span class="sxs-lookup"><span data-stu-id="f3d7b-135">Administrator: Email Distributor batch process</span></span>

<span data-ttu-id="f3d7b-136">ユーザーの操作なしに、SMTP 経由でサーバーから直接送信される電子メールは、**電子メール ディストリビューター バッチ**プロセスによって送信されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-136">Email that is sent directly from the server, without user interaction, via SMTP is sent by the **Email distributor batch** process.</span></span> <span data-ttu-id="f3d7b-137">電子メールのキューの処理には、そのバッチ処理を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-137">That batch process must be started to process the email queue.</span></span> <span data-ttu-id="f3d7b-138">プロセスを開始するには、**電子メール配布バッチ**ウィンドウ (**システム管理**&gt;**定期タスク**&gt;**電子メール処理**&gt;**バッチ**)] を開いて、**バッチ処理** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-138">To start the process, open the **Email distributor batch** pane (**System administration** &gt; **Periodic tasks** &gt; **Email processing** &gt; **Batch**) and turn on **Batch processing**.</span></span>

<span data-ttu-id="f3d7b-139">為替プロバイダーを使用している場合、バッチ プロセス (通常は管理者) に関連付けられているユーザー アカウントが送信者になります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-139">If the Exchange provider is used, then the user account associated with the batch process (usually admin) will be sender.</span></span>

## <a name="administrator-user-email"></a><span data-ttu-id="f3d7b-140">管理者ユーザー: ユーザーの電子メール</span><span class="sxs-lookup"><span data-stu-id="f3d7b-140">Administrator: User email</span></span>

<span data-ttu-id="f3d7b-141">各ユーザーのデフォルトのメールアドレスは、**ユーザー**ページ (**システム管理**&gt; **ユーザー** &gt; **ユーザー**) の **電子メール** 電子メールフィールドから取得します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-141">The default email address for each user is pulled from the **Email** field on the **Users** page (**System administration** &gt; **Users** &gt; **Users**).</span></span> <span data-ttu-id="f3d7b-142">各ユーザーがサインインするために電子メール アドレスを指定する必要がありますが、そのためにフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-142">An email address should be specified for each user for sign in, so this field should be populated.</span></span> <span data-ttu-id="f3d7b-143">必要に応じて、この既定値をオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-143">Users can override this default if needed.</span></span>

## <a name="user-email-provider-selection-section-on-the-options-page"></a><span data-ttu-id="f3d7b-144">ユーザー: [オプション] ページの電子メール プロバイダーの選択セクション</span><span class="sxs-lookup"><span data-stu-id="f3d7b-144">User: Email provider selection section on the Options page</span></span>

<span data-ttu-id="f3d7b-145">**オプション** ページは、**設定 &gt; ユーザー オプション** から開くことができます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-145">The **Options** page can be opened via **Settings &gt; User options**.</span></span> <span data-ttu-id="f3d7b-146">**電子メール プロバイダーの選択** セクションは、**アカウント** タブにあります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-146">The **Email provider selection** section is on the **Account** tab.</span></span>

| <span data-ttu-id="f3d7b-147">フィールド</span><span class="sxs-lookup"><span data-stu-id="f3d7b-147">Field</span></span>             | <span data-ttu-id="f3d7b-148">説明</span><span class="sxs-lookup"><span data-stu-id="f3d7b-148">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="f3d7b-149">電子メール プロバイダー ID</span><span class="sxs-lookup"><span data-stu-id="f3d7b-149">Email provider ID</span></span> | <span data-ttu-id="f3d7b-150">ユーザーは、電子メールを送信するときに使用する電子メール プロバイダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-150">Allows the user to select the email provider that should be used when sending an email.</span></span> <span data-ttu-id="f3d7b-151">ここでオプションを選択することは、**どのように電子メール送信しますか** ダイアログ ボックスで **今後確認しない** をオンにするのと同じです。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-151">Selecting an option here is the equivalent of selecting **Do not ask again** in the **How would you like to send email** dialog box.</span></span> <span data-ttu-id="f3d7b-152">空白のオプション **使用する電子メール プロバイダーの入力を求める** を選択すると、メールが送信されるときに **電子メールを送信する方法** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-152">Selecting the blank option **Prompt for which email provider to use** will cause the **How would you like to send email** dialog box to display when an email is going to be sent.</span></span> |
| <span data-ttu-id="f3d7b-153">電子メール</span><span class="sxs-lookup"><span data-stu-id="f3d7b-153">Email</span></span>             | <span data-ttu-id="f3d7b-154">ユーザーが電子メールの**ソース**フィールドの電子メール アドレスの上書きを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-154">Allows the user to provide an email address override for the **From** field of the email.</span></span> <span data-ttu-id="f3d7b-155">既定では、ユーザー アカウントに関連付けられた電子メール エイリアスは新しい電子メールの**ソース** フィールドとして使用されますが、このユーザー オプションの電子メール アドレスによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-155">By default, the email alias that associated with the user account is used as the **From** field in new emails, but this user option email address will override that.</span></span> <span data-ttu-id="f3d7b-156">SMTP で電子メールを送信するとき、ユーザーは適切な **Send As**および **Send On Behalf Of** アクセス許可を Exchange または SMTP サーバー上で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-156">When sending email via SMTP the user needs to have appropriate **Send As** and **Send On Behalf Of** permissions configured in Exchange or on the SMTP server.</span></span><blockquote>[!NOTE] <span data-ttu-id="f3d7b-157">**Send As** および **Send On Behalf Of** 権限は、Office 365 管理センター (portal.office.com/Admin) にて、**ユーザー** &gt; **有効なユーザー** &gt; **ユーザー** &gt; **メール ボックスのアクセス許可を編集** &gt; **このメールボックスから電子メールを送信する**で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-157">You can configure **Send As** and **Send On Behalf Of** permissions in the Office 365 admin center (portal.office.com/Admin) at **Users** &gt; **Active users** &gt; **User** &gt; **Edit mailbox permissions** &gt; **Send email from this mailbox**.</span></span> <span data-ttu-id="f3d7b-158">詳細については、[Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-158">For more information, see [Enable sending email from another user's mailbox in Office 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span></blockquote> |

## <a name="user-optional-how-would-you-like-to-send-email-dialog-box"></a><span data-ttu-id="f3d7b-159">ユーザー (省略可): 電子メール ダイアログ ボックスをどのように送信しますか</span><span class="sxs-lookup"><span data-stu-id="f3d7b-159">User (optional): How would you like to send email dialog box</span></span>

<span data-ttu-id="f3d7b-160">電子メールを送信するときは、**電子メールをどのように送信しますか** ダイアログ ボックスが表示され、それに電子メールを送信するために使用可能なオプションが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-160">When an email is going to be sent, the user will see the **How would you like to send email** dialog box that will list the available options for sending email.</span></span>

| <span data-ttu-id="f3d7b-161">フィールド</span><span class="sxs-lookup"><span data-stu-id="f3d7b-161">Field</span></span>                                                                  | <span data-ttu-id="f3d7b-162">説明</span><span class="sxs-lookup"><span data-stu-id="f3d7b-162">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| <span data-ttu-id="f3d7b-163">Outlook などの電子メール アプリケーションを使用します</span><span class="sxs-lookup"><span data-stu-id="f3d7b-163">Use an email app, such as Outlook</span></span>                                      | <span data-ttu-id="f3d7b-164">生成された電子メール (.eml) を持つを提供します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-164">Provides the user with a generated email (.eml) file.</span></span> |
| <span data-ttu-id="f3d7b-165">Exchange 電子メール サーバーを使用します</span><span class="sxs-lookup"><span data-stu-id="f3d7b-165">Use Exchange email server</span></span>                                              | <span data-ttu-id="f3d7b-166">テナントに関連付けられている Exchange Online サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-166">Uses the Exchange Online server associated with the tenant.</span></span> <span data-ttu-id="f3d7b-167">電子メールは、Exchange Webサービス (EWS) を使用して送信されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-167">The email will be sent using Exchange Web Services (EWS).</span></span> <span data-ttu-id="f3d7b-168">オンプレミス Exchange サーバーは、この時点では **Exchange** メール プロバイダーでサポートされていません、</span><span class="sxs-lookup"><span data-stu-id="f3d7b-168">On-premises Exchange servers are not supported at this time for the **Exchange** mail provider.</span></span> |
| <span data-ttu-id="f3d7b-169">Microsoft Dynamics 365 for Finance and Operations 電子メール クライアントを使用します</span><span class="sxs-lookup"><span data-stu-id="f3d7b-169">Use the Microsoft Dynamics 365 for Finance and Operations email client</span></span> | <span data-ttu-id="f3d7b-170">**電子メール送信する**構成ダイアログ ボックスを開いて、結果を電子メールで SMTP 経由で送信します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-170">Opens the **Send email** composition dialog box and then sends the resulting email via SMTP.</span></span> |
| <span data-ttu-id="f3d7b-171">今後このメッセージを表示しない</span><span class="sxs-lookup"><span data-stu-id="f3d7b-171">Do not ask again</span></span>                                                       | <span data-ttu-id="f3d7b-172">このフィールドが選択されていない場合は、次回に電子メールが送信されたときに最後に選択したオプションが使用され、ダイアログ ボックスが表示されません。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-172">If this field is not selected, the next time an email is sent the most recently selected option will be used and the dialog box will not open.</span></span> |

## <a name="user-optional-send-email-dialog-box"></a><span data-ttu-id="f3d7b-173">ユーザー (省略可): 電子メール ダイアログ ボックスを送信</span><span class="sxs-lookup"><span data-stu-id="f3d7b-173">User (optional): Send email dialog box</span></span>

<span data-ttu-id="f3d7b-174">**電子メール送信** ダイアログ ボックスが開き、送信される電子メールの内容を編集できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-174">The **Send email** dialog box is opened to allow the user to edit the contents of the email that will be sent.</span></span> <span data-ttu-id="f3d7b-175">次のフィールドの一部は、このウィンドウであらかじめ設定されています。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-175">Some of the following fields will be pre-populated in this window.</span></span>

| <span data-ttu-id="f3d7b-176">フィールド</span><span class="sxs-lookup"><span data-stu-id="f3d7b-176">Field</span></span>                                                     | <span data-ttu-id="f3d7b-177">説明</span><span class="sxs-lookup"><span data-stu-id="f3d7b-177">Description</span></span> |
|-----------------------------------------------------------|-------------|
| <span data-ttu-id="f3d7b-178">自</span><span class="sxs-lookup"><span data-stu-id="f3d7b-178">From</span></span>                                                      | <span data-ttu-id="f3d7b-179">**オプション** ページの **メール** フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-179">Populated from the **Email** field on the **Options** page.</span></span> |
| <span data-ttu-id="f3d7b-180">**宛先**、**Cc**、**Bcc**、**件名**、および**本文**</span><span class="sxs-lookup"><span data-stu-id="f3d7b-180">**To**, **Cc**, **Bcc**, **Subject**, and **Body**</span></span> | <span data-ttu-id="f3d7b-181">電子メールの送信を開始したプロセスによって指定された値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-181">Populated with values specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="f3d7b-182">これらのフィールドは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-182">These fields can be edited as needed by the user.</span></span> |
| <span data-ttu-id="f3d7b-183">添付ファイル リスト</span><span class="sxs-lookup"><span data-stu-id="f3d7b-183">Attachments list</span></span>                                          | <span data-ttu-id="f3d7b-184">電子メールの送信を開始したプロセスによって指定されたファイルが添付される場合があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-184">May be populated with attachments specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="f3d7b-185">このリストは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-185">This list can be edited as needed by the user.</span></span> |

<span data-ttu-id="f3d7b-186">電子メールを送信する準備ができたら、**送信** ボタンを使用して SMTP 経由で電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-186">When the email is ready to be sent, the **Send** button will cause the email to be sent via SMTP.</span></span>

## <a name="usage-scenarios-to-verify-if-email-is-configured-correctly"></a><span data-ttu-id="f3d7b-187">電子メールが正しく設定されているかどうかを確認するための使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="f3d7b-187">Usage scenarios to verify if email is configured correctly</span></span>

### <a name="send-mail-via-a-local-mail-client"></a><span data-ttu-id="f3d7b-188">ローカル メール クライアント経由で電子メールを送信</span><span class="sxs-lookup"><span data-stu-id="f3d7b-188">Send mail via a local mail client</span></span>

<span data-ttu-id="f3d7b-189">SysEmail フレームワークで有効になっている電子メール ワークフローでは、添付ファイルを含む電子メール メッセージ (.eml files) を生成できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-189">Email workflows that are enabled via the SysEmail framework can generate email messages (.eml files) that contain attachments.</span></span> <span data-ttu-id="f3d7b-190">これらのメッセージは Microsoft Outlook または他の電子メール クライアント経由で送信することができます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-190">You can then send these messages via Microsoft Outlook or another email client.</span></span>

1. <span data-ttu-id="f3d7b-191">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-191">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
2. <span data-ttu-id="f3d7b-192">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-192">Select **US-008 Sparrow Retail**.</span></span>
3. <span data-ttu-id="f3d7b-193">**回収** &gt; **顧客残高** &gt; **コレクション**の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-193">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
4. <span data-ttu-id="f3d7b-194">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-194">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
5. <span data-ttu-id="f3d7b-195">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-195">Click **OK** to accept the default values in the dialog box.</span></span>
6. <span data-ttu-id="f3d7b-196">メール オプションの使用を促すメッセージが表示された場合は、**再度確認しない**チェック ボックス (このオプションは**ユーザー オプション** ページから変更できます) をオフにし、**Outlook などの電子メール アプリケーションを使用**を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-196">If you're prompted for the mail option to use, clear the **Do not ask again** check box (you can change this option from the **User options** page), select **Use an email app, such as Outlook**, and then click **OK**.</span></span>
7. <span data-ttu-id="f3d7b-197">コンピューター上で Internet Explorer を使用している場合は、生成される電子メール (.eml) ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-197">If you're using Internet Explorer on your computer, open the email (.eml) file that is generated.</span></span> <span data-ttu-id="f3d7b-198">VM 上で Internet Explorer を使用している場合は、ファイルをコンピューターにコピーし、そのコンピュータでファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-198">If you're using Internet Explorer on the VM, copy the file to your computer, and open it there.</span></span>
8. <span data-ttu-id="f3d7b-199">**宛先**フィールドの電子メール アドレスと生成されたブック添付ファイルに注意します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-199">Note the email address in the **To** field and the generated workbook attachment.</span></span>

### <a name="send-mail-via-smtp"></a><span data-ttu-id="f3d7b-200">SMTP 経由でメールを送信</span><span class="sxs-lookup"><span data-stu-id="f3d7b-200">Send mail via SMTP</span></span>

<span data-ttu-id="f3d7b-201">SysEmail フレームワークを介して有効になっている電子メール ワークフローは、簡単な電子メール ダイアログ ボックスで作成し、Simple Mail Transfer Protocol (SMTP) 経由で送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-201">Email workflows that are enabled via the SysEmail framework can also be created in a simple email dialog box and then sent via Simple Mail Transfer Protocol (SMTP).</span></span>

1. <span data-ttu-id="f3d7b-202">Finance and Operations で、**電子メール パラメーター** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-202">In Finance and Operations, go to the **Email parameters** page.</span></span>
2. <span data-ttu-id="f3d7b-203">**SMTP 設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-203">Click **SMTP settings**.</span></span>
3. <span data-ttu-id="f3d7b-204">**送信メール サーバー** を要求された SMTP サーバーに設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-204">Set the **Outgoing mail server** to the desired SMTP server:</span></span>

    - <span data-ttu-id="f3d7b-205">[Office 365 製品](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-205">For [Office 365 production](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="f3d7b-206">(**設定** &gt; **メール** &gt; **POP および IMAP**で outlook.office.com を通してこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="f3d7b-206">(Find this setting via outlook.office.com, at **Settings** &gt; **Mail** &gt; **POP and IMAP**.)</span></span>
    - <span data-ttu-id="f3d7b-207">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-207">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span>

4. <span data-ttu-id="f3d7b-208">ユーザー名とパスワードを適切な電子メール アカウントとパスワードに設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-208">Set the user name and password to an appropriate email account and password.</span></span>
5. <span data-ttu-id="f3d7b-209">**SSLRequired** を有効のままにして、**SMTP ポート番号**は **587** に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-209">Leave **SSLRequired** turned on, and leave **SMTP port number** set to **587**.</span></span>
6. <span data-ttu-id="f3d7b-210">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-210">Click **Save**.</span></span>
7. <span data-ttu-id="f3d7b-211">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-211">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
8. <span data-ttu-id="f3d7b-212">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-212">Select **US-008 Sparrow Retail**.</span></span>
9. <span data-ttu-id="f3d7b-213">**回収** &gt; **顧客残高** &gt; **コレクション**の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-213">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
10. <span data-ttu-id="f3d7b-214">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-214">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
11. <span data-ttu-id="f3d7b-215">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-215">Click **OK** to accept the default values in the dialog box.</span></span>
12. <span data-ttu-id="f3d7b-216">メール オプションを使用するように求められたら、**Microsoft Dynamics 365 for Finance and Operations 電子メール クライアントの使用**を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-216">If you're prompted for the mail option to use, select **Use the Microsoft Dynamics 365 for Finance and Operations email client**, and then click **OK**.</span></span>
13. <span data-ttu-id="f3d7b-217">テスト メッセージを受信するには、**宛先アドレス**をメール アドレスに変更します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-217">To receive the test message, change the **To address** to your email address.</span></span>

    <span data-ttu-id="f3d7b-218">SMTP 設定で指定されたアカウントが、電子メール アカウントの **Send As** および **Send On Behalf Of** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-218">Ensure that the account specified in the SMTP settings is able to **Send As** and **Send On Behalf Of** your email account.</span></span> <span data-ttu-id="f3d7b-219">これを確実にするための最も簡単な方法は、電子メール アカウントを SMTP 設定で使用することです。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-219">The easiest way to ensure this to use your email account in the SMTP settings.</span></span>

14. <span data-ttu-id="f3d7b-220">メッセージの件名および本文を入力します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-220">Enter a subject and body for the message.</span></span>
15. <span data-ttu-id="f3d7b-221">**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-221">Click **Send**.</span></span> <span data-ttu-id="f3d7b-222">メッセージは 1 〜 5 分で配信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-222">The message should be delivered in one to five minutes.</span></span>

## <a name="administrator-workflow-email-notifications"></a><span data-ttu-id="f3d7b-223">管理者: ワークフロー電子メール通知</span><span class="sxs-lookup"><span data-stu-id="f3d7b-223">Administrator: Workflow email notifications</span></span>

<span data-ttu-id="f3d7b-224">ワークフロー電子メールのコンフィギュレーションは連携して動作する関連設定の集合です。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-224">Workflow email configuration is a collection of related settings that work in conjunction.</span></span>

### <a name="workflow-email-notification-setup"></a><span data-ttu-id="f3d7b-225">ワークフロー電子メール通知のセットアップ</span><span class="sxs-lookup"><span data-stu-id="f3d7b-225">Workflow email notification setup</span></span>

1. <span data-ttu-id="f3d7b-226">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="f3d7b-226">Verify email settings:</span></span>

    1. <span data-ttu-id="f3d7b-227">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-227">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="f3d7b-228">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-228">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="f3d7b-229">SMTP メール サーバーの設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-229">Set the SMTP mail server settings.</span></span>

2. <span data-ttu-id="f3d7b-230">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-230">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="f3d7b-231">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール ディストリビューター バッチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-231">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Email distributor batch**.</span></span>
    2. <span data-ttu-id="f3d7b-232">**バッチ プロセス**オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-232">Enable the **Batch processing** option.</span></span>
    3. <span data-ttu-id="f3d7b-233">必要に応じて、電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-233">Optionally, adjust the recurrence of the email process:</span></span>

        1. <span data-ttu-id="f3d7b-234">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-234">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="f3d7b-235">カウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-235">Adjust the count.</span></span>
        3. <span data-ttu-id="f3d7b-236">必要に応じて毎分実行するように調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-236">Adjust to run every minute if needed.</span></span>

3. <span data-ttu-id="f3d7b-237">ワークフロー通知システムの電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-237">Verify workflow notification system email templates:</span></span>

    1. <span data-ttu-id="f3d7b-238">**システム管理** \> **設定** \> **電子メール** \> **システムの電子メール テンプレート** (システム全体のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-238">Go to **System administration** \> **Setup** \> **Email** \> **System email templates** (for system-wide templates).</span></span>
    2. <span data-ttu-id="f3d7b-239">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-239">Verify that the **Sender email** field is set and valid.</span></span>

4. <span data-ttu-id="f3d7b-240">ワークフロー通知組織の電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-240">Verify workflow notification organization email templates:</span></span>

    1. <span data-ttu-id="f3d7b-241">**組織管理** \> **設定** \> **組織の電子メール テンプレート** (組織固有のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-241">Go to **Organization administration** \> **Setup** \> **Organization email templates** (for organization-specific templates).</span></span>
    2. <span data-ttu-id="f3d7b-242">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-242">Verify that the **Sender email** field is set and valid.</span></span>

5. <span data-ttu-id="f3d7b-243">ユーザーが電子メール通知を受信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-243">Verify that the user can receive email notifications:</span></span>

    1. <span data-ttu-id="f3d7b-244">**設定** \> **ユーザー オプション**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-244">Go to **Settings** \> **User options**.</span></span>
    2. <span data-ttu-id="f3d7b-245">**勘定**タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-245">Go to the **Account** tab.</span></span>

       1. <span data-ttu-id="f3d7b-246">メール プロバイダー ID (SMTP など) を設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-246">Set the email provider ID (for example, SMTP).</span></span>
       2. <span data-ttu-id="f3d7b-247">必要に応じて、ユーザー設定の既定になっていなかった場合は、プロバイダーの電子メール アドレスを設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-247">Optionally, set the email address for the provider if it was not the default from the user setup.</span></span>

    3. <span data-ttu-id="f3d7b-248">**ワークフロー** タブに移動します。電子メールで通知を送信するオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-248">Navigate to the **Workflow** tab. Set the option to send notifications in email to **Yes**.</span></span>

6. <span data-ttu-id="f3d7b-249">ワークフロー システムが電子メール通知を送信することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-249">Verify that the workflow system will send email notifications:</span></span>

    <span data-ttu-id="f3d7b-250">通知する必要があるワークフローごとに、ワークフロー エディターでワークフロー プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-250">For each workflow that should have a notification, open the workflow properties in the workflow editor.</span></span>

    1. <span data-ttu-id="f3d7b-251">**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-251">Click **Basic settings**.</span></span> <span data-ttu-id="f3d7b-252">ワークフロー通知の電子メール テンプレートを調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-252">Adjust the email template for the workflow notifications.</span></span>
    2. <span data-ttu-id="f3d7b-253">**通知**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-253">Click **Notifications**.</span></span>

        1. <span data-ttu-id="f3d7b-254">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-254">Enable the events for which a user should be notified.</span></span>
        2. <span data-ttu-id="f3d7b-255">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-255">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

    3. <span data-ttu-id="f3d7b-256">ユーザーに通知される必要のあるワークフロー承認要素:</span><span class="sxs-lookup"><span data-stu-id="f3d7b-256">On a workflow approval element for which a user should be notified:</span></span>

        1. <span data-ttu-id="f3d7b-257">**プロパティ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-257">Go to **Properties**.</span></span>
        2. <span data-ttu-id="f3d7b-258">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-258">Enable the events for which a user should be notified.</span></span>
        3. <span data-ttu-id="f3d7b-259">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-259">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

### <a name="workflow-email-notification-testing"></a><span data-ttu-id="f3d7b-260">ワークフロー電子メール通知のテスト</span><span class="sxs-lookup"><span data-stu-id="f3d7b-260">Workflow email notification testing</span></span>

<span data-ttu-id="f3d7b-261">電子メール通知のテストでは、単に通知をトリガーし、それを確認するだけです。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-261">The testing for email notifications is to simply trigger the notification and then check for it.</span></span>

1. <span data-ttu-id="f3d7b-262">電子メール通知に対して設定されているワークフローを送信します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-262">Submit a workflow that has been set up for email notifications.</span></span>
2. <span data-ttu-id="f3d7b-263">ワークフロー履歴をチェックして、ワークフロー作業項目が予定されたユーザーに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-263">Check the workflow history to make sure that a workflow work item was assigned to the expected user.</span></span>
3. <span data-ttu-id="f3d7b-264">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール送信ステータス** で、保留中の電子メール通知の状態を確認してください。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-264">Check the status of the pending email notification in **System administration** \> **Periodic tasks** \> **Email processing** \> **Email sending status**.</span></span>

    <span data-ttu-id="f3d7b-265">電子メールが送信に失敗した場合は、SMTP メール アカウントを開くことができることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-265">If the email is fails to send, make sure that the SMTP mail account can be opened.</span></span>

4. <span data-ttu-id="f3d7b-266">適切な受信トレイで電子メール通知を確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-266">Check for the email notification in the appropriate inbox.</span></span>

## <a name="troubleshoot-email"></a><span data-ttu-id="f3d7b-267">電子メールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f3d7b-267">Troubleshoot email</span></span>

<span data-ttu-id="f3d7b-268">メール設定のトラブルシューティングに役立つ標準的な手順がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-268">There are a few standard steps that can help you troubleshoot the configuration of email settings.</span></span>

1. <span data-ttu-id="f3d7b-269">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="f3d7b-269">Verify email settings:</span></span>

    1. <span data-ttu-id="f3d7b-270">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-270">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="f3d7b-271">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-271">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="f3d7b-272">SMTP メール サーバーの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-272">Verify the settings of the SMTP mail server.</span></span>
    4. <span data-ttu-id="f3d7b-273">アカウントとパスワードが正確であるかことを確認するために、別のウィンドウで SMTP アカウントにログインします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-273">Sign in to the SMTP account in a separate window to make sure that the account and password are correct.</span></span>
    5. <span data-ttu-id="f3d7b-274">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-274">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>

2. <span data-ttu-id="f3d7b-275">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-275">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="f3d7b-276">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **バッチ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-276">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch**.</span></span>
    2. <span data-ttu-id="f3d7b-277">**バッチ処理**オプションが**はい**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-277">Make sure that the **Batch processing** option is set to **Yes**.</span></span>
    3. <span data-ttu-id="f3d7b-278">電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-278">Review the recurrence of the email process:</span></span>

        1. <span data-ttu-id="f3d7b-279">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-279">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="f3d7b-280">必要に応じてカウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-280">Adjust the count as you require.</span></span>

3. <span data-ttu-id="f3d7b-281">保留中の電子メールの内容とステータスを確認するには、**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール送信ステータス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-281">To review the contents and status of the pending emails, go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Email sending status**.</span></span>

    1. <span data-ttu-id="f3d7b-282">プラットフォーム更新プログラム 28 より前のリリースを使用している場合は、フォームをパーソナライズして電子メールの差出人を追加し確認しやすくします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-282">If you're using a release that is earlier than Platform update 28, personalize the form to add the email sender for easy review.</span></span> <span data-ttu-id="f3d7b-283">これを行うには、グリッド ヘッダーを右クリックし **列の追加** を選択して **電子メール** を選択して、**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-283">To do this, right-click the grid header, select **Add columns**, select **Email**, and then click **Insert**.</span></span> <span data-ttu-id="f3d7b-284">**電子メール** フィールドがグリッドに追加されていない場合は、**メッセージの表示** を選択してから **電子メール** フィールドを選択して送信者を表示できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-284">If the **Email** field isn't added into the grid, you can view the sender by selecting **Show message**, and then selecting the **Email** field.</span></span>
    2. <span data-ttu-id="f3d7b-285">電子メールが正しいアカウントから送信されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-285">Verify that emails are being sent from the correct account.</span></span> <span data-ttu-id="f3d7b-286">アカウントが正しくない場合、必要に応じてユーザー オプション、システム テンプレート、組織テンプレートなどの設定を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-286">If the account is incorrect, you need to adjust settings such as user options, system templates,  or organization templates, as needed.</span></span>
    3. <span data-ttu-id="f3d7b-287">すべての電子メール ユーザー アカウントに構成された SMTP アカウントの **Send As** へのアクセス許可が付与されていることを確認します (詳細は手順 4 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-287">Verify that all email user accounts have been granted permission to **Send As** for the configured SMTP account (see step 4 for details).</span></span>

4. <span data-ttu-id="f3d7b-288">Office 365 管理センターで、電子メールの送信に使用されるすべてのユーザー メール アカウントに、構成された SMTP アカウントに対する **Send As** と **Send On Behalf Of** アクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-288">In the Office 365 admin center, verify that all user mail accounts that will be used to send emails have **Send As** and **Send On Behalf Of** permissions for the configured SMTP account.</span></span> <span data-ttu-id="f3d7b-289">詳細については、[Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-289">For more information, see [Enable sending email from another user's mailbox in Office 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span>
5. <span data-ttu-id="f3d7b-290">有効かつログインできることを確認するために、すべてのユーザー メールボックスにログインします。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-290">Sign in to all user mailboxes to verify that they are valid and can be signed in to.</span></span>
6. <span data-ttu-id="f3d7b-291">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-291">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>
7. <span data-ttu-id="f3d7b-292">SMTP を介して電子メールを送信すると問題が発生する場合は、[SMTPer.net](https://www.smtper.net/) のようなツールに SMTP アカウント情報を入力して SMTP サーバーとアカウントが有効で正しく機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-292">If you continue to experience issues when email is sent via SMTP, enter the SMTP account information in a tool such as [SMTPer.net](https://www.smtper.net/) to verify that the SMTP server and account are valid and working correctly.</span></span>

## <a name="troubleshoot-the-exchange-mail-provider"></a><span data-ttu-id="f3d7b-293">Exchange メール プロバイダーのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f3d7b-293">Troubleshoot the Exchange mail provider</span></span>

<span data-ttu-id="f3d7b-294">**電子メール パラメーター** ページで管理者は対話型の電子メール プロバイダーおよびバッチ電子メール プロバイダーとして Exchange を選択できます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-294">The **Email parameters** page allows an administrator to select Exchange as an interactive email provider and as the Batch email provider.</span></span> <span data-ttu-id="f3d7b-295">Exchange メール プロバイダーは、現在のユーザーの Exchange Online アカウントを使用して電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-295">The Exchange mail provider will use the current user's Exchange Online account to send emails.</span></span> <span data-ttu-id="f3d7b-296">バッチ電子メール プロバイダーとして使用された場合は、バッチ アカウントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-296">When used as the Batch email provider, the batch account will be used.</span></span> <span data-ttu-id="f3d7b-297">追加のコンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-297">No additional configuration is needed.</span></span> <span data-ttu-id="f3d7b-298">トラブルシューティングが必要な場合は、現在のユーザーのアカウントにサインインできることと、そのアカウントから目的の受信者に電子メールを送信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-298">If troubleshooting is needed, ensure that the current user's account can be signed into and that emails can be sent from that account to the intended recipients.</span></span>

## <a name="other-notes"></a><span data-ttu-id="f3d7b-299">その他のメモ</span><span class="sxs-lookup"><span data-stu-id="f3d7b-299">Other notes</span></span>

<span data-ttu-id="f3d7b-300">システムは Exchange や一般的な電子メール クライアントのような SMTP サーバーと通信するため、標準の動作と制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-300">The system communicates with Exchange or an SMTP server like a typical email client, so standard behavior and limits apply.</span></span> <span data-ttu-id="f3d7b-301">たとえば、標準の [Exchange Online 送受信制限](https://technet.microsoft.com/library/exchange-online-limits.aspx#RecipientLimits)が適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3d7b-301">For example, standard [Exchange Online receiving and sending limits](https://technet.microsoft.com/library/exchange-online-limits.aspx#RecipientLimits) apply.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3d7b-302">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f3d7b-302">Additional resources</span></span>

[<span data-ttu-id="f3d7b-303">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f3d7b-303">Office integration troubleshooting</span></span>](../../dev-itpro/office-integration/office-integration-troubleshooting.md)

[<span data-ttu-id="f3d7b-304">Office 統合のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="f3d7b-304">Office integration tutorial</span></span>](../../dev-itpro/office-integration/office-integration-tutorial.md)

<span data-ttu-id="f3d7b-305">[Microsoft Dynamics AX での電子メール機能のコンフィギュレーション [AX 2012]](https://technet.microsoft.com/library/aa834374.aspx)</span><span class="sxs-lookup"><span data-stu-id="f3d7b-305">[Configure email functionality in Microsoft Dynamics AX [AX 2012]](https://technet.microsoft.com/library/aa834374.aspx)</span></span>
