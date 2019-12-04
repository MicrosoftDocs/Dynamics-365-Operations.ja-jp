---
title: 電子メールのコンフィギュレーションと送信
description: 電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。
author: ChrisGarty
manager: AnnBe
ms.date: 10/10/2019
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
ms.openlocfilehash: bd046cfb3a0a98c4d707c68ffd6b2ae8c00574d1
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812423"
---
# <a name="configure-and-send-email"></a><span data-ttu-id="4d4a1-103">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="4d4a1-103">Configure and send email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d4a1-104">電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-104">The behavior of the email subsystem is influenced by a combination of administrator configuration, user configuration, and user choices.</span></span> <span data-ttu-id="4d4a1-105">このトピックでは、関連情報を見つけやすくするために、管理者のセクションとユーザーのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-105">This topic is divided into sections for administrators and users to make it easy to find relevant information.</span></span>

<span data-ttu-id="4d4a1-106">管理者とユーザーの両方が電子メールのサブシステムの動作を設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-106">Both administrators and users set the behavior of the email subsystem.</span></span>

## <a name="administrator-email-parameters-page"></a><span data-ttu-id="4d4a1-107">管理者: 電子メール パラメーター ページ</span><span class="sxs-lookup"><span data-stu-id="4d4a1-107">Administrator: Email parameters page</span></span>

<span data-ttu-id="4d4a1-108">**電子メール パラメーター**ページの、**電子メール プロバイダー**タブで、次の設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-108">On the **Email parameters** page, note the following settings on the **Email providers** tab.</span></span>

| <span data-ttu-id="4d4a1-109">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d4a1-109">Field</span></span>                 | <span data-ttu-id="4d4a1-110">説明</span><span class="sxs-lookup"><span data-stu-id="4d4a1-110">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="4d4a1-111">バッチ電子メール プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4d4a1-111">Batch email provider</span></span>  | <span data-ttu-id="4d4a1-112">バッチ方式または非対話型のプロセスで送信される電子メールの送信に使用される電子メール プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-112">Specifies which email provider will be used to send emails that are sent by processes in a batch or non-interactive manner.</span></span> <span data-ttu-id="4d4a1-113">Exchange プロバイダーは、バッチ プロセスに関連付けられているアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-113">The Exchange provider will use the account associated with the batch process.</span></span> |
| <span data-ttu-id="4d4a1-114">添付ファイル サイズの上限</span><span class="sxs-lookup"><span data-stu-id="4d4a1-114">Attachment size limit</span></span> | <span data-ttu-id="4d4a1-115">電子メール サブシステム経由で送信できる 1 つの電子メールの最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-115">Specifies the maximum size of a single email that can be sent via the email subsystem.</span></span> |

<span data-ttu-id="4d4a1-116">**電子メール パラメーター**ページの、**SMTP 設定**タブで、次の設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-116">On the **Email parameters** page, note the following settings on the **SMTP settings** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4d4a1-117">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d4a1-117">Field</span></span></th>
<th><span data-ttu-id="4d4a1-118">説明</span><span class="sxs-lookup"><span data-stu-id="4d4a1-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4d4a1-119">送信メール サーバー</span><span class="sxs-lookup"><span data-stu-id="4d4a1-119">Outgoing mail server</span></span></td>
<td><span data-ttu-id="4d4a1-120">目的の SMTP サーバーのホスト名。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-120">The host name of the desired SMTP server.</span></span>
<ul>
<li><span data-ttu-id="4d4a1-121"><a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Office 365 製品</a> (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-121">For <a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Office 365 production</a> (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="4d4a1-122">(<strong>設定</strong> &gt; <strong>メール</strong> &gt; <strong>POP および IMAP</strong>の outlook.office.com でこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="4d4a1-122">(You can find this setting at outlook.office.com at <strong>Settings</strong> &gt; <strong>Mail</strong> &gt; <strong>POP and IMAP</strong>.)</span></span></li>
<li><span data-ttu-id="4d4a1-123">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-123">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="4d4a1-124">SMTP ポート番号</span><span class="sxs-lookup"><span data-stu-id="4d4a1-124">SMTP port number</span></span></td>
<td><span data-ttu-id="4d4a1-125">通常、セキュリティで保護して送信するためにポート番号は 587 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-125">Typically, the port number should be set to 587 for secure transport.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d4a1-126"><strong>ユーザー名</strong>と<strong>パスワード</strong></span><span class="sxs-lookup"><span data-stu-id="4d4a1-126"><strong>User name</strong> and <strong>Password</strong></span></span></td>
<td><span data-ttu-id="4d4a1-127">必要に応じて、適切なメール アカウントを使用して電子メールの送信を指定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-127">Specify, as needed, to send the email via the appropriate mail account.</span></span> <span data-ttu-id="4d4a1-128">すべてのユーザーは SMTP アカウントを指定し <strong>送信者</strong>および <strong>代理送信</strong>許可をし、Simple Mail Transfer Protocol (SMTP) で送信する機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-128">All users need to provide the SMTP account <strong>Send As</strong> and <strong>Send On Behalf Of</strong> permissions to enable the ability to send Simple Mail Transfer Protocol (SMTP) mail.</span></span> <span data-ttu-id="4d4a1-129">Send As 権限は、Office 365 管理センター (portal.office.com/Admin) にて、<strong>ユーザー</strong> &gt; <strong>有効なユーザー</strong> &gt; <strong>ユーザー</strong> &gt; <strong>メールボックスのアクセス許可を編集</strong> &gt; <strong>このメールボックスから電子メールを送信する</strong> で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-129">You can configure Send As permissions in the Office 365 admin center (portal.office.com/Admin), at <strong>Users</strong> &gt; <strong>Active users</strong> &gt; <strong>User</strong> &gt; <strong>Edit mailbox permissions</strong> &gt; <strong>Send email from this mailbox</strong>.</span></span> <span data-ttu-id="4d4a1-130">詳細については、<a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-130">For more information, see <a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Enable sending email from another user's mailbox in Office 365</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4d4a1-131">SSL が必須かどうかを指定します</span><span class="sxs-lookup"><span data-stu-id="4d4a1-131">Specify if SSL is required</span></span></td>
<td><span data-ttu-id="4d4a1-132">安全なトランスポートをを使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-132">Determines whether secure transport is used.</span></span> <span data-ttu-id="4d4a1-133">これは通常、内部またはトラブルシューティングのシナリオを除き、<strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-133">Typically, this is <strong>Yes</strong>, except for internal or troubleshooting scenarios.</span></span></td>
</tr>
</tbody>
</table>

## <a name="administrator-email-distributor-batch-process"></a><span data-ttu-id="4d4a1-134">管理者: 電子メール配布バッチ処理</span><span class="sxs-lookup"><span data-stu-id="4d4a1-134">Administrator: Email Distributor batch process</span></span>

<span data-ttu-id="4d4a1-135">ユーザーの操作なしに、SMTP 経由でサーバーから直接送信される電子メールは、**電子メール ディストリビューター バッチ**プロセスによって送信されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-135">Email that is sent directly from the server, without user interaction, via SMTP is sent by the **Email distributor batch** process.</span></span> <span data-ttu-id="4d4a1-136">電子メールのキューの処理には、そのバッチ処理を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-136">That batch process must be started to process the email queue.</span></span> <span data-ttu-id="4d4a1-137">プロセスを開始するには、**電子メール配布バッチ**ウィンドウ (**システム管理**&gt;**定期タスク**&gt;**電子メール処理**&gt;**バッチ**)] を開いて、**バッチ処理** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-137">To start the process, open the **Email distributor batch** pane (**System administration** &gt; **Periodic tasks** &gt; **Email processing** &gt; **Batch**) and turn on **Batch processing**.</span></span>

<span data-ttu-id="4d4a1-138">為替プロバイダーを使用している場合、バッチ プロセス (通常は管理者) に関連付けられているユーザー アカウントが送信者になります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-138">If the Exchange provider is used, then the user account associated with the batch process (usually admin) will be sender.</span></span>

## <a name="administrator-user-email"></a><span data-ttu-id="4d4a1-139">管理者ユーザー: ユーザーの電子メール</span><span class="sxs-lookup"><span data-stu-id="4d4a1-139">Administrator: User email</span></span>

<span data-ttu-id="4d4a1-140">各ユーザーのデフォルトのメールアドレスは、**ユーザー**ページ (**システム管理**&gt; **ユーザー** &gt; **ユーザー**) の **電子メール** 電子メールフィールドから取得します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-140">The default email address for each user is pulled from the **Email** field on the **Users** page (**System administration** &gt; **Users** &gt; **Users**).</span></span> <span data-ttu-id="4d4a1-141">各ユーザーがサインインするために電子メール アドレスを指定する必要がありますが、そのためにフィールドを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-141">An email address should be specified for each user for sign in, so this field should be populated.</span></span> <span data-ttu-id="4d4a1-142">必要に応じて、この既定値をオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-142">Users can override this default if needed.</span></span>

## <a name="user-email-provider-selection-section-on-the-options-page"></a><span data-ttu-id="4d4a1-143">ユーザー: [オプション] ページの電子メール プロバイダーの選択セクション</span><span class="sxs-lookup"><span data-stu-id="4d4a1-143">User: Email provider selection section on the Options page</span></span>

<span data-ttu-id="4d4a1-144">**オプション** ページは、**設定 &gt; ユーザー オプション** から開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-144">The **Options** page can be opened via **Settings &gt; User options**.</span></span> <span data-ttu-id="4d4a1-145">**電子メール プロバイダーの選択** セクションは、**アカウント** タブにあります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-145">The **Email provider selection** section is on the **Account** tab.</span></span>

| <span data-ttu-id="4d4a1-146">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d4a1-146">Field</span></span>             | <span data-ttu-id="4d4a1-147">説明</span><span class="sxs-lookup"><span data-stu-id="4d4a1-147">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="4d4a1-148">電子メール プロバイダー ID</span><span class="sxs-lookup"><span data-stu-id="4d4a1-148">Email provider ID</span></span> | <span data-ttu-id="4d4a1-149">ユーザーは、電子メールを送信するときに使用する電子メール プロバイダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-149">Allows the user to select the email provider that should be used when sending an email.</span></span> <span data-ttu-id="4d4a1-150">ここでオプションを選択することは、**どのように電子メール送信しますか** ダイアログ ボックスで **今後確認しない** をオンにするのと同じです。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-150">Selecting an option here is the equivalent of selecting **Do not ask again** in the **How would you like to send email** dialog box.</span></span> <span data-ttu-id="4d4a1-151">空白のオプション **使用する電子メール プロバイダーの入力を求める** を選択すると、メールが送信されるときに **電子メールを送信する方法** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-151">Selecting the blank option **Prompt for which email provider to use** will cause the **How would you like to send email** dialog box to display when an email is going to be sent.</span></span> |
| <span data-ttu-id="4d4a1-152">電子メール</span><span class="sxs-lookup"><span data-stu-id="4d4a1-152">Email</span></span>             | <span data-ttu-id="4d4a1-153">ユーザーが電子メールの**ソース**フィールドの電子メール アドレスの上書きを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-153">Allows the user to provide an email address override for the **From** field of the email.</span></span> <span data-ttu-id="4d4a1-154">既定では、ユーザー アカウントに関連付けられた電子メール エイリアスは新しい電子メールの**ソース** フィールドとして使用されますが、このユーザー オプションの電子メール アドレスによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-154">By default, the email alias that associated with the user account is used as the **From** field in new emails, but this user option email address will override that.</span></span> <span data-ttu-id="4d4a1-155">SMTP で電子メールを送信するとき、ユーザーは適切な **Send As**および **Send On Behalf Of** アクセス許可を Exchange または SMTP サーバー上で構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-155">When sending email via SMTP the user needs to have appropriate **Send As** and **Send On Behalf Of** permissions configured in Exchange or on the SMTP server.</span></span><blockquote>[!NOTE] <span data-ttu-id="4d4a1-156">**Send As** および **Send On Behalf Of** 権限は、Office 365 管理センター (portal.office.com/Admin) にて、**ユーザー** &gt; **有効なユーザー** &gt; **ユーザー** &gt; **メール ボックスのアクセス許可を編集** &gt; **このメールボックスから電子メールを送信する**で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-156">You can configure **Send As** and **Send On Behalf Of** permissions in the Office 365 admin center (portal.office.com/Admin) at **Users** &gt; **Active users** &gt; **User** &gt; **Edit mailbox permissions** &gt; **Send email from this mailbox**.</span></span> <span data-ttu-id="4d4a1-157">詳細については、[Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-157">For more information, see [Enable sending email from another user's mailbox in Office 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span></blockquote> |

## <a name="user-optional-how-would-you-like-to-send-email-dialog-box"></a><span data-ttu-id="4d4a1-158">ユーザー (省略可): 電子メール ダイアログ ボックスをどのように送信しますか</span><span class="sxs-lookup"><span data-stu-id="4d4a1-158">User (optional): How would you like to send email dialog box</span></span>

<span data-ttu-id="4d4a1-159">電子メールを送信するときは、**電子メールをどのように送信しますか** ダイアログ ボックスが表示され、それに電子メールを送信するために使用可能なオプションが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-159">When an email is going to be sent, the user will see the **How would you like to send email** dialog box that will list the available options for sending email.</span></span>

| <span data-ttu-id="4d4a1-160">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d4a1-160">Field</span></span>                                                                  | <span data-ttu-id="4d4a1-161">説明</span><span class="sxs-lookup"><span data-stu-id="4d4a1-161">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| <span data-ttu-id="4d4a1-162">Outlook などの電子メール アプリケーションを使用します</span><span class="sxs-lookup"><span data-stu-id="4d4a1-162">Use an email app, such as Outlook</span></span>                                      | <span data-ttu-id="4d4a1-163">生成された電子メール (.eml) を持つを提供します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-163">Provides the user with a generated email (.eml) file.</span></span> |
| <span data-ttu-id="4d4a1-164">Exchange 電子メール サーバーを使用します</span><span class="sxs-lookup"><span data-stu-id="4d4a1-164">Use Exchange email server</span></span>                                              | <span data-ttu-id="4d4a1-165">テナントに関連付けられている Exchange Online サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-165">Uses the Exchange Online server associated with the tenant.</span></span> <span data-ttu-id="4d4a1-166">電子メールは、Exchange Webサービス (EWS) を使用して送信されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-166">The email will be sent using Exchange Web Services (EWS).</span></span> <span data-ttu-id="4d4a1-167">オンプレミス Exchange サーバーは、この時点では **Exchange** メール プロバイダーでサポートされていません、</span><span class="sxs-lookup"><span data-stu-id="4d4a1-167">On-premises Exchange servers are not supported at this time for the **Exchange** mail provider.</span></span> |
| <span data-ttu-id="4d4a1-168">システムの電子メール クライアントの使用</span><span class="sxs-lookup"><span data-stu-id="4d4a1-168">Use the system email client</span></span> | <span data-ttu-id="4d4a1-169">**電子メール送信する**構成ダイアログ ボックスを開いて、結果を電子メールで SMTP 経由で送信します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-169">Opens the **Send email** composition dialog box and then sends the resulting email via SMTP.</span></span> |
| <span data-ttu-id="4d4a1-170">今後このメッセージを表示しない</span><span class="sxs-lookup"><span data-stu-id="4d4a1-170">Do not ask again</span></span>                                                       | <span data-ttu-id="4d4a1-171">このフィールドが選択されていない場合は、次回に電子メールが送信されたときに最後に選択したオプションが使用され、ダイアログ ボックスが表示されません。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-171">If this field is not selected, the next time an email is sent the most recently selected option will be used and the dialog box will not open.</span></span> |

## <a name="user-optional-send-email-dialog-box"></a><span data-ttu-id="4d4a1-172">ユーザー (省略可): 電子メール ダイアログ ボックスを送信</span><span class="sxs-lookup"><span data-stu-id="4d4a1-172">User (optional): Send email dialog box</span></span>

<span data-ttu-id="4d4a1-173">**電子メール送信** ダイアログ ボックスが開き、送信される電子メールの内容を編集できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-173">The **Send email** dialog box is opened to allow the user to edit the contents of the email that will be sent.</span></span> <span data-ttu-id="4d4a1-174">次のフィールドの一部は、このウィンドウであらかじめ設定されています。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-174">Some of the following fields will be pre-populated in this window.</span></span>

| <span data-ttu-id="4d4a1-175">フィールド</span><span class="sxs-lookup"><span data-stu-id="4d4a1-175">Field</span></span>                                                     | <span data-ttu-id="4d4a1-176">説明</span><span class="sxs-lookup"><span data-stu-id="4d4a1-176">Description</span></span> |
|-----------------------------------------------------------|-------------|
| <span data-ttu-id="4d4a1-177">自</span><span class="sxs-lookup"><span data-stu-id="4d4a1-177">From</span></span>                                                      | <span data-ttu-id="4d4a1-178">**オプション** ページの **メール** フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-178">Populated from the **Email** field on the **Options** page.</span></span> |
| <span data-ttu-id="4d4a1-179">**宛先**、**Cc**、**Bcc**、**件名**、および**本文**</span><span class="sxs-lookup"><span data-stu-id="4d4a1-179">**To**, **Cc**, **Bcc**, **Subject**, and **Body**</span></span> | <span data-ttu-id="4d4a1-180">電子メールの送信を開始したプロセスによって指定された値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-180">Populated with values specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="4d4a1-181">これらのフィールドは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-181">These fields can be edited as needed by the user.</span></span> |
| <span data-ttu-id="4d4a1-182">添付ファイル リスト</span><span class="sxs-lookup"><span data-stu-id="4d4a1-182">Attachments list</span></span>                                          | <span data-ttu-id="4d4a1-183">電子メールの送信を開始したプロセスによって指定されたファイルが添付される場合があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-183">May be populated with attachments specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="4d4a1-184">このリストは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-184">This list can be edited as needed by the user.</span></span> |

<span data-ttu-id="4d4a1-185">電子メールを送信する準備ができたら、**送信** ボタンを使用して SMTP 経由で電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-185">When the email is ready to be sent, the **Send** button will cause the email to be sent via SMTP.</span></span>

## <a name="usage-scenarios-to-verify-if-email-is-configured-correctly"></a><span data-ttu-id="4d4a1-186">電子メールが正しく設定されているかどうかを確認するための使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="4d4a1-186">Usage scenarios to verify if email is configured correctly</span></span>

### <a name="send-mail-via-a-local-mail-client"></a><span data-ttu-id="4d4a1-187">ローカル メール クライアント経由で電子メールを送信</span><span class="sxs-lookup"><span data-stu-id="4d4a1-187">Send mail via a local mail client</span></span>

<span data-ttu-id="4d4a1-188">SysEmail フレームワークで有効になっている電子メール ワークフローでは、添付ファイルを含む電子メール メッセージ (.eml files) を生成できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-188">Email workflows that are enabled via the SysEmail framework can generate email messages (.eml files) that contain attachments.</span></span> <span data-ttu-id="4d4a1-189">これらのメッセージは Microsoft Outlook または他の電子メール クライアント経由で送信することができます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-189">You can then send these messages via Microsoft Outlook or another email client.</span></span>

1. <span data-ttu-id="4d4a1-190">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-190">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
2. <span data-ttu-id="4d4a1-191">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-191">Select **US-008 Sparrow Retail**.</span></span>
3. <span data-ttu-id="4d4a1-192">**回収** &gt; **顧客残高** &gt; **コレクション**の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-192">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
4. <span data-ttu-id="4d4a1-193">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-193">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
5. <span data-ttu-id="4d4a1-194">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-194">Click **OK** to accept the default values in the dialog box.</span></span>
6. <span data-ttu-id="4d4a1-195">メール オプションの使用を促すメッセージが表示された場合は、**再度確認しない**チェック ボックス (このオプションは**ユーザー オプション** ページから変更できます) をオフにし、**Outlook などの電子メール アプリケーションを使用**を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-195">If you're prompted for the mail option to use, clear the **Do not ask again** check box (you can change this option from the **User options** page), select **Use an email app, such as Outlook**, and then click **OK**.</span></span>
7. <span data-ttu-id="4d4a1-196">コンピューター上で Internet Explorer を使用している場合は、生成される電子メール (.eml) ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-196">If you're using Internet Explorer on your computer, open the email (.eml) file that is generated.</span></span> <span data-ttu-id="4d4a1-197">VM 上で Internet Explorer を使用している場合は、ファイルをコンピューターにコピーし、そのコンピュータでファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-197">If you're using Internet Explorer on the VM, copy the file to your computer, and open it there.</span></span>
8. <span data-ttu-id="4d4a1-198">**宛先**フィールドの電子メール アドレスと生成されたブック添付ファイルに注意します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-198">Note the email address in the **To** field and the generated workbook attachment.</span></span>

### <a name="send-mail-via-smtp"></a><span data-ttu-id="4d4a1-199">SMTP 経由でメールを送信</span><span class="sxs-lookup"><span data-stu-id="4d4a1-199">Send mail via SMTP</span></span>

<span data-ttu-id="4d4a1-200">SysEmail フレームワークを介して有効になっている電子メール ワークフローは、簡単な電子メール ダイアログ ボックスで作成し、Simple Mail Transfer Protocol (SMTP) 経由で送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-200">Email workflows that are enabled via the SysEmail framework can also be created in a simple email dialog box and then sent via Simple Mail Transfer Protocol (SMTP).</span></span>

1. <span data-ttu-id="4d4a1-201">**電子メール パラメーター**のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-201">Go to the **Email parameters** page.</span></span>
2. <span data-ttu-id="4d4a1-202">**SMTP 設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-202">Click **SMTP settings**.</span></span>
3. <span data-ttu-id="4d4a1-203">**送信メール サーバー** を要求された SMTP サーバーに設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-203">Set the **Outgoing mail server** to the desired SMTP server:</span></span>

    - <span data-ttu-id="4d4a1-204">[Office 365 製品](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-204">For [Office 365 production](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="4d4a1-205">(**設定** &gt; **メール** &gt; **POP および IMAP**で outlook.office.com を通してこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="4d4a1-205">(Find this setting via outlook.office.com, at **Settings** &gt; **Mail** &gt; **POP and IMAP**.)</span></span>
    - <span data-ttu-id="4d4a1-206">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-206">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span>

4. <span data-ttu-id="4d4a1-207">ユーザー名とパスワードを適切な電子メール アカウントとパスワードに設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-207">Set the user name and password to an appropriate email account and password.</span></span>
5. <span data-ttu-id="4d4a1-208">**SSLRequired** を有効のままにして、**SMTP ポート番号**は **587** に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-208">Leave **SSLRequired** turned on, and leave **SMTP port number** set to **587**.</span></span>
6. <span data-ttu-id="4d4a1-209">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-209">Click **Save**.</span></span>
7. <span data-ttu-id="4d4a1-210">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-210">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
8. <span data-ttu-id="4d4a1-211">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-211">Select **US-008 Sparrow Retail**.</span></span>
9. <span data-ttu-id="4d4a1-212">**回収** &gt; **顧客残高** &gt; **コレクション**の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-212">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
10. <span data-ttu-id="4d4a1-213">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-213">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
11. <span data-ttu-id="4d4a1-214">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-214">Click **OK** to accept the default values in the dialog box.</span></span>
12. <span data-ttu-id="4d4a1-215">メール オプションを使用するように求められたら、**Microsoft Dynamics 365 for Finance and Operations 電子メール クライアントの使用**を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-215">If you're prompted for the mail option to use, select **Use the Microsoft Dynamics 365 for Finance and Operations email client**, and then click **OK**.</span></span>
13. <span data-ttu-id="4d4a1-216">テスト メッセージを受信するには、**宛先アドレス**をメール アドレスに変更します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-216">To receive the test message, change the **To address** to your email address.</span></span>

    <span data-ttu-id="4d4a1-217">SMTP 設定で指定されたアカウントが、電子メール アカウントの **Send As** および **Send On Behalf Of** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-217">Ensure that the account specified in the SMTP settings is able to **Send As** and **Send On Behalf Of** your email account.</span></span> <span data-ttu-id="4d4a1-218">これを確実にするための最も簡単な方法は、電子メール アカウントを SMTP 設定で使用することです。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-218">The easiest way to ensure this to use your email account in the SMTP settings.</span></span>

14. <span data-ttu-id="4d4a1-219">メッセージの件名および本文を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-219">Enter a subject and body for the message.</span></span>
15. <span data-ttu-id="4d4a1-220">**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-220">Click **Send**.</span></span> <span data-ttu-id="4d4a1-221">メッセージは 1 〜 5 分で配信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-221">The message should be delivered in one to five minutes.</span></span>

## <a name="administrator-workflow-email-notifications"></a><span data-ttu-id="4d4a1-222">管理者: ワークフロー電子メール通知</span><span class="sxs-lookup"><span data-stu-id="4d4a1-222">Administrator: Workflow email notifications</span></span>

<span data-ttu-id="4d4a1-223">ワークフロー電子メールのコンフィギュレーションは連携して動作する関連設定の集合です。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-223">Workflow email configuration is a collection of related settings that work in conjunction.</span></span>

### <a name="workflow-email-notification-setup"></a><span data-ttu-id="4d4a1-224">ワークフロー電子メール通知のセットアップ</span><span class="sxs-lookup"><span data-stu-id="4d4a1-224">Workflow email notification setup</span></span>

1. <span data-ttu-id="4d4a1-225">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="4d4a1-225">Verify email settings:</span></span>

    1. <span data-ttu-id="4d4a1-226">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-226">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="4d4a1-227">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-227">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="4d4a1-228">SMTP メール サーバーの設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-228">Set the SMTP mail server settings.</span></span>

2. <span data-ttu-id="4d4a1-229">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-229">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="4d4a1-230">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール ディストリビューター バッチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-230">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Email distributor batch**.</span></span>
    2. <span data-ttu-id="4d4a1-231">**バッチ プロセス**オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-231">Enable the **Batch processing** option.</span></span>
    3. <span data-ttu-id="4d4a1-232">必要に応じて、電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-232">Optionally, adjust the recurrence of the email process:</span></span>

        1. <span data-ttu-id="4d4a1-233">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-233">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="4d4a1-234">カウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-234">Adjust the count.</span></span>
        3. <span data-ttu-id="4d4a1-235">必要に応じて毎分実行するように調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-235">Adjust to run every minute if needed.</span></span>

3. <span data-ttu-id="4d4a1-236">ワークフロー通知システムの電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-236">Verify workflow notification system email templates:</span></span>

    1. <span data-ttu-id="4d4a1-237">**システム管理** \> **設定** \> **電子メール** \> **システムの電子メール テンプレート** (システム全体のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-237">Go to **System administration** \> **Setup** \> **Email** \> **System email templates** (for system-wide templates).</span></span>
    2. <span data-ttu-id="4d4a1-238">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-238">Verify that the **Sender email** field is set and valid.</span></span>

4. <span data-ttu-id="4d4a1-239">ワークフロー通知組織の電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-239">Verify workflow notification organization email templates:</span></span>

    1. <span data-ttu-id="4d4a1-240">**組織管理** \> **設定** \> **組織の電子メール テンプレート** (組織固有のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-240">Go to **Organization administration** \> **Setup** \> **Organization email templates** (for organization-specific templates).</span></span>
    2. <span data-ttu-id="4d4a1-241">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-241">Verify that the **Sender email** field is set and valid.</span></span>

5. <span data-ttu-id="4d4a1-242">ユーザーが電子メール通知を受信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-242">Verify that the user can receive email notifications:</span></span>

    1. <span data-ttu-id="4d4a1-243">**設定** \> **ユーザー オプション**に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-243">Go to **Settings** \> **User options**.</span></span>
    2. <span data-ttu-id="4d4a1-244">**勘定**タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-244">Go to the **Account** tab.</span></span>

       1. <span data-ttu-id="4d4a1-245">メール プロバイダー ID (SMTP など) を設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-245">Set the email provider ID (for example, SMTP).</span></span>
       2. <span data-ttu-id="4d4a1-246">必要に応じて、ユーザー設定の既定になっていなかった場合は、プロバイダーの電子メール アドレスを設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-246">Optionally, set the email address for the provider if it was not the default from the user setup.</span></span>

    3. <span data-ttu-id="4d4a1-247">**ワークフロー** タブに移動します。電子メールで通知を送信するオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-247">Navigate to the **Workflow** tab. Set the option to send notifications in email to **Yes**.</span></span>

6. <span data-ttu-id="4d4a1-248">ワークフロー システムが電子メール通知を送信することを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-248">Verify that the workflow system will send email notifications:</span></span>

    <span data-ttu-id="4d4a1-249">通知する必要があるワークフローごとに、ワークフロー エディターでワークフロー プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-249">For each workflow that should have a notification, open the workflow properties in the workflow editor.</span></span>

    1. <span data-ttu-id="4d4a1-250">**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-250">Click **Basic settings**.</span></span> <span data-ttu-id="4d4a1-251">ワークフロー通知の電子メール テンプレートを調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-251">Adjust the email template for the workflow notifications.</span></span>
    2. <span data-ttu-id="4d4a1-252">**通知**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-252">Click **Notifications**.</span></span>

        1. <span data-ttu-id="4d4a1-253">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-253">Enable the events for which a user should be notified.</span></span>
        2. <span data-ttu-id="4d4a1-254">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-254">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

    3. <span data-ttu-id="4d4a1-255">ユーザーに通知される必要のあるワークフロー承認要素:</span><span class="sxs-lookup"><span data-stu-id="4d4a1-255">On a workflow approval element for which a user should be notified:</span></span>

        1. <span data-ttu-id="4d4a1-256">**プロパティ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-256">Go to **Properties**.</span></span>
        2. <span data-ttu-id="4d4a1-257">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-257">Enable the events for which a user should be notified.</span></span>
        3. <span data-ttu-id="4d4a1-258">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-258">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

### <a name="workflow-email-notification-testing"></a><span data-ttu-id="4d4a1-259">ワークフロー電子メール通知のテスト</span><span class="sxs-lookup"><span data-stu-id="4d4a1-259">Workflow email notification testing</span></span>

<span data-ttu-id="4d4a1-260">電子メール通知のテストでは、単に通知をトリガーし、それを確認するだけです。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-260">The testing for email notifications is to simply trigger the notification and then check for it.</span></span>

1. <span data-ttu-id="4d4a1-261">電子メール通知に対して設定されているワークフローを送信します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-261">Submit a workflow that has been set up for email notifications.</span></span>
2. <span data-ttu-id="4d4a1-262">ワークフロー履歴をチェックして、ワークフロー作業項目が予定されたユーザーに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-262">Check the workflow history to make sure that a workflow work item was assigned to the expected user.</span></span>
3. <span data-ttu-id="4d4a1-263">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール送信ステータス** で、保留中の電子メール通知の状態を確認してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-263">Check the status of the pending email notification in **System administration** \> **Periodic tasks** \> **Email processing** \> **Email sending status**.</span></span>

    <span data-ttu-id="4d4a1-264">電子メールが送信に失敗した場合は、SMTP メール アカウントを開くことができることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-264">If the email is fails to send, make sure that the SMTP mail account can be opened.</span></span>

4. <span data-ttu-id="4d4a1-265">適切な受信トレイで電子メール通知を確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-265">Check for the email notification in the appropriate inbox.</span></span>

## <a name="troubleshoot-email"></a><span data-ttu-id="4d4a1-266">電子メールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="4d4a1-266">Troubleshoot email</span></span>

<span data-ttu-id="4d4a1-267">メール設定のトラブルシューティングに役立つ標準的な手順がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-267">There are a few standard steps that can help you troubleshoot the configuration of email settings.</span></span>

1. <span data-ttu-id="4d4a1-268">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="4d4a1-268">Verify email settings:</span></span>

    1. <span data-ttu-id="4d4a1-269">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-269">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="4d4a1-270">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-270">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="4d4a1-271">SMTP メール サーバーの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-271">Verify the settings of the SMTP mail server.</span></span>
    4. <span data-ttu-id="4d4a1-272">アカウントとパスワードが正確であるかことを確認するために、別のウィンドウで SMTP アカウントにログインします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-272">Sign in to the SMTP account in a separate window to make sure that the account and password are correct.</span></span>
    5. <span data-ttu-id="4d4a1-273">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-273">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>

2. <span data-ttu-id="4d4a1-274">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-274">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="4d4a1-275">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **バッチ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-275">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch**.</span></span>
    2. <span data-ttu-id="4d4a1-276">**バッチ処理**オプションが**はい**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-276">Make sure that the **Batch processing** option is set to **Yes**.</span></span>
    3. <span data-ttu-id="4d4a1-277">電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-277">Review the recurrence of the email process:</span></span>

        1. <span data-ttu-id="4d4a1-278">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-278">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="4d4a1-279">必要に応じてカウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-279">Adjust the count as you require.</span></span>

3. <span data-ttu-id="4d4a1-280">保留中の電子メールの内容とステータスを確認するには、**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール送信ステータス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-280">To review the contents and status of the pending emails, go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Email sending status**.</span></span>

    1. <span data-ttu-id="4d4a1-281">プラットフォーム更新プログラム 28 より前のリリースを使用している場合は、フォームをパーソナライズして電子メールの差出人を追加し確認しやすくします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-281">If you're using a release that is earlier than Platform update 28, personalize the form to add the email sender for easy review.</span></span> <span data-ttu-id="4d4a1-282">これを行うには、グリッド ヘッダーを右クリックし **列の追加** を選択して **電子メール** を選択して、**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-282">To do this, right-click the grid header, select **Add columns**, select **Email**, and then click **Insert**.</span></span> <span data-ttu-id="4d4a1-283">**電子メール** フィールドがグリッドに追加されていない場合は、**メッセージの表示** を選択してから **電子メール** フィールドを選択して送信者を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-283">If the **Email** field isn't added into the grid, you can view the sender by selecting **Show message**, and then selecting the **Email** field.</span></span>
    2. <span data-ttu-id="4d4a1-284">電子メールが正しいアカウントから送信されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-284">Verify that emails are being sent from the correct account.</span></span> <span data-ttu-id="4d4a1-285">アカウントが正しくない場合、必要に応じてユーザー オプション、システム テンプレート、組織テンプレートなどの設定を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-285">If the account is incorrect, you need to adjust settings such as user options, system templates,  or organization templates, as needed.</span></span>
    3. <span data-ttu-id="4d4a1-286">すべての電子メール ユーザー アカウントに構成された SMTP アカウントの **Send As** へのアクセス許可が付与されていることを確認します (詳細は手順 4 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-286">Verify that all email user accounts have been granted permission to **Send As** for the configured SMTP account (see step 4 for details).</span></span>

4. <span data-ttu-id="4d4a1-287">Office 365 管理センターで、電子メールの送信に使用されるすべてのユーザー メール アカウントに、構成された SMTP アカウントに対する **Send As** と **Send On Behalf Of** アクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-287">In the Office 365 admin center, verify that all user mail accounts that will be used to send emails have **Send As** and **Send On Behalf Of** permissions for the configured SMTP account.</span></span> <span data-ttu-id="4d4a1-288">詳細については、[Office 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-288">For more information, see [Enable sending email from another user's mailbox in Office 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span>
5. <span data-ttu-id="4d4a1-289">有効かつログインできることを確認するために、すべてのユーザー メールボックスにログインします。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-289">Sign in to all user mailboxes to verify that they are valid and can be signed in to.</span></span>
6. <span data-ttu-id="4d4a1-290">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-290">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>
7. <span data-ttu-id="4d4a1-291">SMTP 設定を別の環境から移行した場合は、パスワード フィールドをクリアしてパスワードを再入力し、フィールドの暗号化が保存された値に悪影響を与えていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-291">If the SMTP settings were migrated from another environment, clear the password field and re-enter the password to ensure that the field encryption hasn't negatively affected the stored value.</span></span>
8. <span data-ttu-id="4d4a1-292">SMTP を介して電子メールを送信すると問題が発生する場合は、[SMTPer.net](https://www.smtper.net/) のようなツールに SMTP アカウント情報を入力して SMTP サーバーとアカウントが有効で正しく機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-292">If you continue to experience issues when email is sent via SMTP, enter the SMTP account information in a tool such as [SMTPer.net](https://www.smtper.net/) to verify that the SMTP server and account are valid and working correctly.</span></span>

## <a name="troubleshoot-the-exchange-mail-provider"></a><span data-ttu-id="4d4a1-293">Exchange メール プロバイダーのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="4d4a1-293">Troubleshoot the Exchange mail provider</span></span>

<span data-ttu-id="4d4a1-294">**電子メール パラメーター** ページで管理者は対話型の電子メール プロバイダーおよびバッチ電子メール プロバイダーとして Exchange を選択できます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-294">The **Email parameters** page allows an administrator to select Exchange as an interactive email provider and as the Batch email provider.</span></span> <span data-ttu-id="4d4a1-295">Exchange メール プロバイダーは、現在のユーザーの Exchange Online アカウントを使用して電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-295">The Exchange mail provider will use the current user's Exchange Online account to send emails.</span></span> <span data-ttu-id="4d4a1-296">バッチ電子メール プロバイダーとして使用された場合は、バッチ アカウントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-296">When used as the Batch email provider, the batch account will be used.</span></span> <span data-ttu-id="4d4a1-297">追加のコンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-297">No additional configuration is needed.</span></span> <span data-ttu-id="4d4a1-298">トラブルシューティングが必要な場合は、現在のユーザーのアカウントにサインインできることと、そのアカウントから目的の受信者に電子メールを送信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-298">If troubleshooting is needed, ensure that the current user's account can be signed into and that emails can be sent from that account to the intended recipients.</span></span>

## <a name="other-notes"></a><span data-ttu-id="4d4a1-299">その他のメモ</span><span class="sxs-lookup"><span data-stu-id="4d4a1-299">Other notes</span></span>

<span data-ttu-id="4d4a1-300">システムは Exchange や一般的な電子メール クライアントのような SMTP サーバーと通信するため、標準の動作と制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-300">The system communicates with Exchange or an SMTP server like a typical email client, so standard behavior and limits apply.</span></span> <span data-ttu-id="4d4a1-301">たとえば、標準の [Exchange Online 送受信制限](https://technet.microsoft.com/library/exchange-online-limits.aspx#RecipientLimits)が適用されます。</span><span class="sxs-lookup"><span data-stu-id="4d4a1-301">For example, standard [Exchange Online receiving and sending limits](https://technet.microsoft.com/library/exchange-online-limits.aspx#RecipientLimits) apply.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d4a1-302">追加リソース</span><span class="sxs-lookup"><span data-stu-id="4d4a1-302">Additional resources</span></span>

[<span data-ttu-id="4d4a1-303">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="4d4a1-303">Troubleshoot the Office integration</span></span>](../../dev-itpro/office-integration/office-integration-troubleshooting.md)

[<span data-ttu-id="4d4a1-304">Office 統合のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="4d4a1-304">Office integration tutorial</span></span>](../../dev-itpro/office-integration/office-integration-tutorial.md)

<span data-ttu-id="4d4a1-305">[Microsoft Dynamics AX での電子メール機能のコンフィギュレーション [AX 2012]](https://technet.microsoft.com/library/aa834374.aspx)</span><span class="sxs-lookup"><span data-stu-id="4d4a1-305">[Configure email functionality in Microsoft Dynamics AX [AX 2012]](https://technet.microsoft.com/library/aa834374.aspx)</span></span>
