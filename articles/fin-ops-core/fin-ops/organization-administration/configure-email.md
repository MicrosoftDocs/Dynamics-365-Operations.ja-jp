---
title: 電子メールのコンフィギュレーションと送信
description: 電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。
author: ChrisGarty
manager: AnnBe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysEmailParameters
audience: IT Pro
ms.reviewer: sericks
ms.custom: 268274
ms.assetid: 194ca8fd-5e20-4464-9c85-08d2b5ff63ca
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f66cca1d8725edde8c2feb9594d0400503cf8d5
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694373"
---
# <a name="configure-and-send-email"></a><span data-ttu-id="d4534-103">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="d4534-103">Configure and send email</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d4534-104">電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-104">The behavior of the email subsystem is influenced by a combination of administrator configuration, user configuration, and user choices.</span></span> <span data-ttu-id="d4534-105">このトピックでは、関連情報を見つけやすくするために、管理者のセクションとユーザーのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="d4534-105">This topic is divided into sections for administrators and users to make it easy to find relevant information.</span></span>

<span data-ttu-id="d4534-106">管理者とユーザーの両方が電子メールのサブシステムの動作を設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-106">Both administrators and users set the behavior of the email subsystem.</span></span>

## <a name="administrator-email-parameters-page"></a><span data-ttu-id="d4534-107">[管理者] 電子メール パラメーター ページ</span><span class="sxs-lookup"><span data-stu-id="d4534-107">[Administrator] Email parameters page</span></span> 

### <a name="configuration-tab"></a><span data-ttu-id="d4534-108">構成タブ</span><span class="sxs-lookup"><span data-stu-id="d4534-108">Configuration tab</span></span>
<span data-ttu-id="d4534-109">**メール パラメーター** ページで、**構成** タブの次の設定に注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="d4534-109">On the **Email parameters** page, note the following settings on the **Configuration** tab.</span></span>

| <span data-ttu-id="d4534-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="d4534-110">Field</span></span>                 | <span data-ttu-id="d4534-111">説明</span><span class="sxs-lookup"><span data-stu-id="d4534-111">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d4534-112">バッチ電子メール プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d4534-112">Batch email provider</span></span>  | <span data-ttu-id="d4534-113">バッチ方式または非対話型のプロセスで送信される電子メールの送信に使用される電子メール プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-113">Specifies which email provider will be used to send emails that are sent by processes in a batch or non-interactive manner.</span></span> <span data-ttu-id="d4534-114">Exchange プロバイダーは、バッチ プロセスに関連付けられているアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="d4534-114">The Exchange provider will use the account associated with the batch process.</span></span> |
| <span data-ttu-id="d4534-115">添付ファイル サイズの上限</span><span class="sxs-lookup"><span data-stu-id="d4534-115">Attachment size limit</span></span> | <span data-ttu-id="d4534-116">電子メール サブシステム経由で送信できる 1 つの電子メールの最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-116">Specifies the maximum size of a single email that can be sent via the email subsystem.</span></span> |

<span data-ttu-id="d4534-117">プラットフォーム更新 32 では、**メール履歴** ページが追加されており、送信を防ぐことができたかもしれないメールのエラーなど、管理者がすべての送信済みメールを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-117">In Platform update 32, an **Email history** page was added to allow administrators to review all sent emails, including any errors that might have prevented an email from being sent.</span></span> <span data-ttu-id="d4534-118">既定では、メール履歴は過去 30 日間保持されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-118">By default, the last 30 days of email history is retained.</span></span> <span data-ttu-id="d4534-119">これは、 **メール履歴の保持日数** をゼロ以外の値に変更することで構成できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-119">This can be configured by changing the **Number of days to retain email history** to a non-zero amount.</span></span> <span data-ttu-id="d4534-120">ゼロは規定の値と動作を提供します。</span><span class="sxs-lookup"><span data-stu-id="d4534-120">Zero provides the default amount and behavior.</span></span>

<span data-ttu-id="d4534-121">バージョン 10.0.16/プラットフォーム 40 では、環境で機能管理の **電子メール調整** 機能が有効になっている場合、**電子メール調整** セクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-121">In version 10.0.16/Platform 40, an **Email throttling** section is visible, if your environment has enabled the **Email throttling** feature in Feature management.</span></span> <span data-ttu-id="d4534-122">この機能により非対話型の電子メール プロバイダー (バッチ電子メール プロバイダーなど) は 1 分あたりの送信制限に従うことができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-122">This feature allows non-interactive email providers  (such as the batch email provider) to adhere to a per-minute sending limit.</span></span> <span data-ttu-id="d4534-123">これにより、システムからプロバイダーが許可する数を超える電子メールを送信しようとするエラーを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-123">This can prevent errors from the system attempting to send more emails than the provider allows.</span></span> <span data-ttu-id="d4534-124">Microsoft 365 電子メール プロバイダーの送信制限は、[Exchange Online 送信制限](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits?sending-limits#sending-limits) に応じて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-124">The sending limits for Microsoft 365 email providers are set automatically according to [Exchange Online sending limits](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits?sending-limits#sending-limits).</span></span> <span data-ttu-id="d4534-125">他のすべての電子メール プロバイダーについては、手動での構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="d4534-125">Manual configuration is required for all other email providers.</span></span> <span data-ttu-id="d4534-126">1 分あたりの送信制限は、**1 分あたりの電子メール送信制限** フィールドを 0 にリセットすることによってプロバイダーから削除できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-126">The per-minute sending limit can be removed from a provider by resetting the **per-minute email sending limit** field to 0.</span></span>

### <a name="smtp-settings-tab"></a><span data-ttu-id="d4534-127">SMTP 設定タブ</span><span class="sxs-lookup"><span data-stu-id="d4534-127">SMTP settings tab</span></span>
<span data-ttu-id="d4534-128">**電子メール パラメーター** ページの、**SMTP 設定** タブで、次の設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="d4534-128">On the **Email parameters** page, note the following settings on the **SMTP settings** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4534-129">フィールド</span><span class="sxs-lookup"><span data-stu-id="d4534-129">Field</span></span></th>
<th><span data-ttu-id="d4534-130">説明</span><span class="sxs-lookup"><span data-stu-id="d4534-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4534-131">送信メール サーバー</span><span class="sxs-lookup"><span data-stu-id="d4534-131">Outgoing mail server</span></span></td>
<td><span data-ttu-id="d4534-132">目的の SMTP サーバーのホスト名。</span><span class="sxs-lookup"><span data-stu-id="d4534-132">The host name of the desired SMTP server.</span></span>
<ul>
<li><span data-ttu-id="d4534-133"><a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Microsoft 365 製品</a> (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4534-133">For <a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Microsoft 365 production</a> (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="d4534-134">(<strong>設定</strong> &gt; <strong>メール</strong> &gt; <strong>POP および IMAP</strong>の outlook.office.com でこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="d4534-134">(You can find this setting at outlook.office.com at <strong>Settings</strong> &gt; <strong>Mail</strong> &gt; <strong>POP and IMAP</strong>.)</span></span></li>
<li><span data-ttu-id="d4534-135">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4534-135">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="d4534-136">SMTP ポート番号</span><span class="sxs-lookup"><span data-stu-id="d4534-136">SMTP port number</span></span></td>
<td><span data-ttu-id="d4534-137">通常、セキュリティで保護して送信するためにポート番号は 587 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4534-137">Typically, the port number should be set to 587 for secure transport.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4534-138"><strong>ユーザー名</strong>と<strong>パスワード</strong></span><span class="sxs-lookup"><span data-stu-id="d4534-138"><strong>User name</strong> and <strong>Password</strong></span></span></td>
<td><span data-ttu-id="d4534-139">必要に応じて、適切なメール アカウントを使用して電子メールの送信を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-139">Specify, as needed, to send the email via the appropriate mail account.</span></span> <span data-ttu-id="d4534-140">すべてのユーザーは SMTP アカウントを指定し <strong>送信者</strong>および <strong>代理送信</strong>許可をし、Simple Mail Transfer Protocol (SMTP) で送信する機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d4534-140">All users need to provide the SMTP account <strong>Send As</strong> and <strong>Send On Behalf Of</strong> permissions to enable the ability to send Simple Mail Transfer Protocol (SMTP) mail.</span></span> <span data-ttu-id="d4534-141">[送信者] 権限は、Microsoft 365 管理センター (portal.office.com/Admin) にて、<strong>ユーザー</strong> &gt; <strong>有効なユーザー</strong> &gt; <strong>ユーザー</strong> &gt; <strong>メールボックスのアクセス許可を編集</strong> &gt; <strong>このメールボックスから電子メールを送信する</strong> で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-141">You can configure Send As permissions in the Microsoft 365 admin center (portal.office.com/Admin), at <strong>Users</strong> &gt; <strong>Active users</strong> &gt; <strong>User</strong> &gt; <strong>Edit mailbox permissions</strong> &gt; <strong>Send email from this mailbox</strong>.</span></span> <span data-ttu-id="d4534-142">詳細については、<a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Microsoft 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4534-142">For more information, see <a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Enable sending email from another user's mailbox in Microsoft 365</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4534-143">SSL が必須かどうかを指定します</span><span class="sxs-lookup"><span data-stu-id="d4534-143">Specify if SSL is required</span></span></td>
<td><span data-ttu-id="d4534-144">安全なトランスポートをを使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-144">Determines whether secure transport is used.</span></span> <span data-ttu-id="d4534-145">これは通常、内部またはトラブルシューティングのシナリオを除き、<strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="d4534-145">Typically, this is <strong>Yes</strong>, except for internal or troubleshooting scenarios.</span></span></td>
</tr>
</tbody>
</table>

## <a name="administrator-email-distributor-batch-process"></a><span data-ttu-id="d4534-146">[管理者] 電子メール配布バッチ処理</span><span class="sxs-lookup"><span data-stu-id="d4534-146">[Administrator] Email distributor batch process</span></span>

<span data-ttu-id="d4534-147">ユーザーの操作なしに、SMTP 経由でサーバーから直接送信される電子メールは、**電子メール ディストリビューター バッチ** プロセスによって送信されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-147">Email that is sent directly from the server, without user interaction, via SMTP is sent by the **Email distributor batch** process.</span></span> <span data-ttu-id="d4534-148">電子メールのキューの処理には、そのバッチ処理を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4534-148">That batch process must be started to process the email queue.</span></span> <span data-ttu-id="d4534-149">プロセスを開始するには、**電子メール配布バッチ** ウィンドウ (**システム管理**&gt;**定期タスク**&gt;**電子メール処理**&gt;**バッチ**) を開いて、**バッチ処理** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="d4534-149">To start the process, open the **Email distributor batch** pane (**System administration** &gt; **Periodic tasks** &gt; **Email processing** &gt; **Batch**) and turn on **Batch processing**.</span></span>

<span data-ttu-id="d4534-150">為替プロバイダーを使用している場合、バッチ プロセス (通常は管理者) に関連付けられているユーザー アカウントが送信者になります。</span><span class="sxs-lookup"><span data-stu-id="d4534-150">If the Exchange provider is used, then the user account associated with the batch process (usually admin) will be sender.</span></span>

## <a name="administrator-user-email"></a><span data-ttu-id="d4534-151">[管理者] ユーザーの電子メール</span><span class="sxs-lookup"><span data-stu-id="d4534-151">[Administrator] User email</span></span>

<span data-ttu-id="d4534-152">各ユーザーの既定の **送信元** アドレスは、**ユーザー** ページの **電子メール** フィールドから取得されます (**システム管理** &gt; **ユーザー** &gt; **ユーザー**)。</span><span class="sxs-lookup"><span data-stu-id="d4534-152">The default **send from** address for each user is pulled from the **Email** field on the **Users** page (**System administration** &gt; **Users** &gt; **Users**).</span></span> <span data-ttu-id="d4534-153">管理者は必要に応じて、**オプション** ページの **送信者電子メール** フィールドを使用して、この既定の **送信元** を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="d4534-153">Administrators can override this **send from** default if needed using the **Sender email** field on the **Options** page.</span></span>

## <a name="user-email-provider-selection-section-on-the-options-page"></a><span data-ttu-id="d4534-154">[ユーザー] オプション ページの電子メール プロバイダーの選択セクション</span><span class="sxs-lookup"><span data-stu-id="d4534-154">[User] Email provider selection section on the Options page</span></span>

<span data-ttu-id="d4534-155">**オプション** ページは、**設定 &gt; ユーザー オプション** から開くことができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-155">The **Options** page can be opened via **Settings &gt; User options**.</span></span> <span data-ttu-id="d4534-156">**電子メール プロバイダーの選択** セクションは、**アカウント** タブにあります。</span><span class="sxs-lookup"><span data-stu-id="d4534-156">The **Email provider selection** section is on the **Account** tab.</span></span>

| <span data-ttu-id="d4534-157">フィールド</span><span class="sxs-lookup"><span data-stu-id="d4534-157">Field</span></span>             | <span data-ttu-id="d4534-158">説明</span><span class="sxs-lookup"><span data-stu-id="d4534-158">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="d4534-159">電子メール プロバイダー ID</span><span class="sxs-lookup"><span data-stu-id="d4534-159">Email provider ID</span></span> | <span data-ttu-id="d4534-160">ユーザーは、電子メールを送信するときに使用する電子メール プロバイダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-160">Allows the user to select the email provider that should be used when sending an email.</span></span> <span data-ttu-id="d4534-161">ここでオプションを選択することは、**どのように電子メール送信しますか** ダイアログ ボックスで **今後確認しない** をオンにするのと同じです。</span><span class="sxs-lookup"><span data-stu-id="d4534-161">Selecting an option here is the equivalent of selecting **Do not ask again** in the **How would you like to send email** dialog box.</span></span> <span data-ttu-id="d4534-162">空白のオプション **使用する電子メール プロバイダーの入力を求める** を選択すると、メールが送信されるときに **電子メールを送信する方法** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-162">Selecting the blank option **Prompt for which email provider to use** will cause the **How would you like to send email** dialog box to display when an email is going to be sent.</span></span> |
| <span data-ttu-id="d4534-163">送信者の電子メール</span><span class="sxs-lookup"><span data-stu-id="d4534-163">Sender email</span></span>    | <span data-ttu-id="d4534-164">管理者が電子メールの **ソース** フィールドでユーザーに電子メール アドレスの上書きを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d4534-164">Allows the administrator to provide an email address override for the user in the **From** field of the email.</span></span> <span data-ttu-id="d4534-165">既定では、ユーザー アカウントに関連付けられた電子メール エイリアスは新しい電子メールの **ソース** フィールドとして使用されますが、このユーザー オプションの電子メール アドレスによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d4534-165">By default, the email alias that is associated with the user account is used as the **From** field in new emails, but this user option email address will override that.</span></span> <span data-ttu-id="d4534-166">SMTP で電子メールを送信するとき、ユーザーは交換または SMTP サーバー上で構成された適切な **送信者** および **代理送信者** アクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4534-166">When sending email via SMTP, the user needs to have appropriate **Send As** and **Send On Behalf Of** permissions configured in Exchange or on the SMTP server.</span></span><blockquote>[!NOTE] <span data-ttu-id="d4534-167">**送信者** および **代理送信** 権限は、 Microsoft 365 管理センター (portal.office.com/Admin) にて、**ユーザー** &gt; **有効なユーザー** &gt; **ユーザー** &gt; **メール ボックスのアクセス許可を編集** &gt; **このメールボックスから電子メールを送信する** で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-167">You can configure **Send As** and **Send On Behalf Of** permissions in the Microsoft 365 admin center (portal.office.com/Admin) at **Users** &gt; **Active users** &gt; **User** &gt; **Edit mailbox permissions** &gt; **Send email from this mailbox**.</span></span> <span data-ttu-id="d4534-168">詳細については、[Microsoft 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4534-168">For more information, see [Enable sending email from another user's mailbox in Microsoft 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span></blockquote> |

## <a name="user-how-would-you-like-to-send-email-dialog-box-optional"></a><span data-ttu-id="d4534-169">[ユーザー] 電子メールをどのように送信しますかダイアログ ボックス (省略可)</span><span class="sxs-lookup"><span data-stu-id="d4534-169">[User] How would you like to send email dialog box (optional)</span></span>

<span data-ttu-id="d4534-170">電子メールを送信するときは、**電子メールをどのように送信しますか** ダイアログ ボックスが表示され、それに電子メールを送信するために使用可能なオプションが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-170">When an email is going to be sent, the user will see the **How would you like to send email** dialog box that will list the available options for sending email.</span></span>

| <span data-ttu-id="d4534-171">フィールド</span><span class="sxs-lookup"><span data-stu-id="d4534-171">Field</span></span>                                                                  | <span data-ttu-id="d4534-172">説明</span><span class="sxs-lookup"><span data-stu-id="d4534-172">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| <span data-ttu-id="d4534-173">Outlook などの電子メール アプリケーションを使用します</span><span class="sxs-lookup"><span data-stu-id="d4534-173">Use an email app, such as Outlook</span></span>                                      | <span data-ttu-id="d4534-174">生成された電子メール (.eml) を持つを提供します。</span><span class="sxs-lookup"><span data-stu-id="d4534-174">Provides the user with a generated email (.eml) file.</span></span> |
| <span data-ttu-id="d4534-175">Exchange 電子メール サーバーを使用します</span><span class="sxs-lookup"><span data-stu-id="d4534-175">Use Exchange email server</span></span>                                              | <span data-ttu-id="d4534-176">テナントに関連付けられている Exchange Online サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="d4534-176">Uses the Exchange Online server associated with the tenant.</span></span> <span data-ttu-id="d4534-177">オンプレミス Exchange サーバーは、現時点では **Exchange** メール プロバイダーに対応していません。</span><span class="sxs-lookup"><span data-stu-id="d4534-177">On-premises Exchange servers are currently not supported for the **Exchange** mail provider.</span></span> |
| <span data-ttu-id="d4534-178">システムの電子メール クライアントの使用</span><span class="sxs-lookup"><span data-stu-id="d4534-178">Use the system email client</span></span> | <span data-ttu-id="d4534-179">**電子メール送信する** 構成ダイアログ ボックスを開いて、結果を電子メールで SMTP 経由で送信します。</span><span class="sxs-lookup"><span data-stu-id="d4534-179">Opens the **Send email** composition dialog box and then sends the resulting email via SMTP.</span></span> |
| <span data-ttu-id="d4534-180">今後このメッセージを表示しない</span><span class="sxs-lookup"><span data-stu-id="d4534-180">Do not ask again</span></span>                                                       | <span data-ttu-id="d4534-181">このフィールドが選択されていない場合は、次回に電子メールが送信されたときに最後に選択したオプションが使用され、ダイアログ ボックスが表示されません。</span><span class="sxs-lookup"><span data-stu-id="d4534-181">If this field is not selected, the next time an email is sent the most recently selected option will be used and the dialog box will not open.</span></span> |

## <a name="user-send-email-dialog-box-optional"></a><span data-ttu-id="d4534-182">[ユーザー] 電子メールの送信ダイアログ ボックス (省略可)</span><span class="sxs-lookup"><span data-stu-id="d4534-182">[User] Send email dialog box (optional)</span></span>

<span data-ttu-id="d4534-183">**電子メール送信** ダイアログ ボックスが開き、送信される電子メールの内容を編集できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-183">The **Send email** dialog box is opened to allow the user to edit the contents of the email that will be sent.</span></span> <span data-ttu-id="d4534-184">次のフィールドの一部は、このウィンドウであらかじめ設定されています。</span><span class="sxs-lookup"><span data-stu-id="d4534-184">Some of the following fields will be pre-populated in this window.</span></span>

| <span data-ttu-id="d4534-185">フィールド</span><span class="sxs-lookup"><span data-stu-id="d4534-185">Field</span></span>                                                     | <span data-ttu-id="d4534-186">説明</span><span class="sxs-lookup"><span data-stu-id="d4534-186">Description</span></span> |
|-----------------------------------------------------------|-------------|
| <span data-ttu-id="d4534-187">自</span><span class="sxs-lookup"><span data-stu-id="d4534-187">From</span></span>                                                      | <span data-ttu-id="d4534-188">**オプション** ページの **メール** フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-188">Populated from the **Email** field on the **Options** page.</span></span> |
| <span data-ttu-id="d4534-189">**宛先**、**Cc**、**Bcc**、**件名**、および **本文**</span><span class="sxs-lookup"><span data-stu-id="d4534-189">**To**, **Cc**, **Bcc**, **Subject**, and **Body**</span></span> | <span data-ttu-id="d4534-190">電子メールの送信を開始したプロセスによって指定された値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-190">Populated with values specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="d4534-191">これらのフィールドは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-191">These fields can be edited as needed by the user.</span></span> |
| <span data-ttu-id="d4534-192">添付ファイル リスト</span><span class="sxs-lookup"><span data-stu-id="d4534-192">Attachments list</span></span>                                          | <span data-ttu-id="d4534-193">電子メールの送信を開始したプロセスによって指定されたファイルが添付される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d4534-193">May be populated with attachments specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="d4534-194">このリストは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-194">This list can be edited as needed by the user.</span></span> |

<span data-ttu-id="d4534-195">電子メールを送信する準備ができたら、**送信** ボタンを使用して SMTP 経由で電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-195">When the email is ready to be sent, the **Send** button will cause the email to be sent via SMTP.</span></span>

## <a name="usage-scenarios-to-verify-if-email-is-configured-correctly"></a><span data-ttu-id="d4534-196">電子メールが正しく設定されているかどうかを確認するための使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="d4534-196">Usage scenarios to verify if email is configured correctly</span></span>

### <a name="send-mail-via-a-local-mail-client"></a><span data-ttu-id="d4534-197">ローカル メール クライアント経由で電子メールを送信</span><span class="sxs-lookup"><span data-stu-id="d4534-197">Send mail via a local mail client</span></span>

<span data-ttu-id="d4534-198">SysEmail フレームワークで有効になっている電子メール ワークフローでは、添付ファイルを含む電子メール メッセージ (.eml files) を生成できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-198">Email workflows that are enabled via the SysEmail framework can generate email messages (.eml files) that contain attachments.</span></span> <span data-ttu-id="d4534-199">これらのメッセージは Microsoft Outlook または他の電子メール クライアント経由で送信することができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-199">You can then send these messages via Microsoft Outlook or another email client.</span></span>

1. <span data-ttu-id="d4534-200">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-200">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
2. <span data-ttu-id="d4534-201">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4534-201">Select **US-008 Sparrow Retail**.</span></span>
3. <span data-ttu-id="d4534-202">**回収** &gt; **顧客残高** &gt; **コレクション** の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d4534-202">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
4. <span data-ttu-id="d4534-203">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-203">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
5. <span data-ttu-id="d4534-204">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-204">Click **OK** to accept the default values in the dialog box.</span></span>
6. <span data-ttu-id="d4534-205">メール オプションの使用を促すメッセージが表示された場合は、**再度確認しない** チェック ボックス (このオプションは **ユーザー オプション** ページから変更できます) をオフにし、**Outlook などの電子メール アプリケーションを使用** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-205">If you're prompted for the mail option to use, clear the **Do not ask again** check box (you can change this option from the **User options** page), select **Use an email app, such as Outlook**, and then click **OK**.</span></span>
7. <span data-ttu-id="d4534-206">コンピューター上で Internet Explorer を使用している場合は、生成される電子メール (.eml) ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d4534-206">If you're using Internet Explorer on your computer, open the email (.eml) file that is generated.</span></span> <span data-ttu-id="d4534-207">VM 上で Internet Explorer を使用している場合は、ファイルをコンピューターにコピーし、そのコンピュータでファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d4534-207">If you're using Internet Explorer on the VM, copy the file to your computer, and open it there.</span></span>
8. <span data-ttu-id="d4534-208">**宛先** フィールドの電子メール アドレスと生成されたブック添付ファイルに注意します。</span><span class="sxs-lookup"><span data-stu-id="d4534-208">Note the email address in the **To** field and the generated workbook attachment.</span></span>

### <a name="send-mail-via-smtp"></a><span data-ttu-id="d4534-209">SMTP 経由でメールを送信</span><span class="sxs-lookup"><span data-stu-id="d4534-209">Send mail via SMTP</span></span>

<span data-ttu-id="d4534-210">SysEmail フレームワークを介して有効になっている電子メール ワークフローは、簡単な電子メール ダイアログ ボックスで作成し、Simple Mail Transfer Protocol (SMTP) 経由で送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="d4534-210">Email workflows that are enabled via the SysEmail framework can also be created in a simple email dialog box and then sent via Simple Mail Transfer Protocol (SMTP).</span></span>

1. <span data-ttu-id="d4534-211">**電子メール パラメーター** のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-211">Go to the **Email parameters** page.</span></span>
2. <span data-ttu-id="d4534-212">**SMTP 設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-212">Click **SMTP settings**.</span></span>
3. <span data-ttu-id="d4534-213">**送信メール サーバー** を要求された SMTP サーバーに設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-213">Set the **Outgoing mail server** to the desired SMTP server:</span></span>

    - <span data-ttu-id="d4534-214">[Microsoft 365 製品](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4534-214">For [Microsoft 365 production](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="d4534-215">(**設定** &gt; **メール** &gt; **POP および IMAP** で outlook.office.com を通してこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="d4534-215">(Find this setting via outlook.office.com, at **Settings** &gt; **Mail** &gt; **POP and IMAP**.)</span></span>
    - <span data-ttu-id="d4534-216">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4534-216">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span>

4. <span data-ttu-id="d4534-217">ユーザー名とパスワードを適切な電子メール アカウントとパスワードに設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-217">Set the user name and password to an appropriate email account and password.</span></span>
5. <span data-ttu-id="d4534-218">**SSLRequired** を有効のままにして、**SMTP ポート番号** は **587** に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="d4534-218">Leave **SSLRequired** turned on, and leave **SMTP port number** set to **587**.</span></span>
6. <span data-ttu-id="d4534-219">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-219">Click **Save**.</span></span>
7. <span data-ttu-id="d4534-220">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-220">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
8. <span data-ttu-id="d4534-221">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d4534-221">Select **US-008 Sparrow Retail**.</span></span>
9. <span data-ttu-id="d4534-222">**回収** &gt; **顧客残高** &gt; **コレクション** の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="d4534-222">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
10. <span data-ttu-id="d4534-223">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-223">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
11. <span data-ttu-id="d4534-224">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-224">Click **OK** to accept the default values in the dialog box.</span></span>
12. <span data-ttu-id="d4534-225">メール オプションを使用するように求められたら、**Microsoft Dynamics 365 for Finance and Operations 電子メール クライアントの使用** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-225">If you're prompted for the mail option to use, select **Use the Microsoft Dynamics 365 for Finance and Operations email client**, and then click **OK**.</span></span>
13. <span data-ttu-id="d4534-226">テスト メッセージを受信するには、**宛先アドレス** をメール アドレスに変更します。</span><span class="sxs-lookup"><span data-stu-id="d4534-226">To receive the test message, change the **To address** to your email address.</span></span>

    <span data-ttu-id="d4534-227">SMTP 設定で指定されたアカウントが、電子メール アカウントの **Send As** および **Send On Behalf Of** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-227">Ensure that the account specified in the SMTP settings is able to **Send As** and **Send On Behalf Of** your email account.</span></span> <span data-ttu-id="d4534-228">これを確実にするための最も簡単な方法は、電子メール アカウントを SMTP 設定で使用することです。</span><span class="sxs-lookup"><span data-stu-id="d4534-228">The easiest way to ensure this to use your email account in the SMTP settings.</span></span>

14. <span data-ttu-id="d4534-229">メッセージの件名および本文を入力します。</span><span class="sxs-lookup"><span data-stu-id="d4534-229">Enter a subject and body for the message.</span></span>
15. <span data-ttu-id="d4534-230">**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-230">Click **Send**.</span></span> <span data-ttu-id="d4534-231">メッセージは 1 〜 5 分で配信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4534-231">The message should be delivered in one to five minutes.</span></span>

## <a name="administrator-workflow-email-notifications"></a><span data-ttu-id="d4534-232">[管理者] ワークフロー電子メール通知</span><span class="sxs-lookup"><span data-stu-id="d4534-232">[Administrator] Workflow email notifications</span></span>

<span data-ttu-id="d4534-233">ワークフロー電子メールのコンフィギュレーションは連携して動作する関連設定の集合です。</span><span class="sxs-lookup"><span data-stu-id="d4534-233">Workflow email configuration is a collection of related settings that work in conjunction.</span></span>

### <a name="workflow-email-notification-setup"></a><span data-ttu-id="d4534-234">ワークフロー電子メール通知のセットアップ</span><span class="sxs-lookup"><span data-stu-id="d4534-234">Workflow email notification setup</span></span>

1. <span data-ttu-id="d4534-235">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="d4534-235">Verify email settings:</span></span>

    1. <span data-ttu-id="d4534-236">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-236">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="d4534-237">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-237">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="d4534-238">SMTP メール サーバーの設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-238">Set the SMTP mail server settings.</span></span>

2. <span data-ttu-id="d4534-239">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-239">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="d4534-240">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール ディストリビューター バッチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-240">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Email distributor batch**.</span></span>
    2. <span data-ttu-id="d4534-241">**バッチ プロセス** オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d4534-241">Enable the **Batch processing** option.</span></span>
    3. <span data-ttu-id="d4534-242">必要に応じて、電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-242">Optionally, adjust the recurrence of the email process:</span></span>

        1. <span data-ttu-id="d4534-243">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-243">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="d4534-244">カウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-244">Adjust the count.</span></span>
        3. <span data-ttu-id="d4534-245">必要に応じて毎分実行するように調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-245">Adjust to run every minute if needed.</span></span>

3. <span data-ttu-id="d4534-246">ワークフロー通知システムの電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-246">Verify workflow notification system email templates:</span></span>

    1. <span data-ttu-id="d4534-247">**システム管理** \> **設定** \> **電子メール** \> **システムの電子メール テンプレート** (システム全体のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-247">Go to **System administration** \> **Setup** \> **Email** \> **System email templates** (for system-wide templates).</span></span>
    2. <span data-ttu-id="d4534-248">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-248">Verify that the **Sender email** field is set and valid.</span></span>

4. <span data-ttu-id="d4534-249">ワークフロー通知組織の電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-249">Verify workflow notification organization email templates:</span></span>

    1. <span data-ttu-id="d4534-250">**組織管理** \> **設定** \> **組織の電子メール テンプレート** (組織固有のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-250">Go to **Organization administration** \> **Setup** \> **Organization email templates** (for organization-specific templates).</span></span>
    2. <span data-ttu-id="d4534-251">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-251">Verify that the **Sender email** field is set and valid.</span></span>

5. <span data-ttu-id="d4534-252">ユーザーが電子メール通知を受信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-252">Verify that the user can receive email notifications:</span></span>

    1. <span data-ttu-id="d4534-253">**設定** \> **ユーザー オプション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-253">Go to **Settings** \> **User options**.</span></span>
    2. <span data-ttu-id="d4534-254">**勘定** タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-254">Go to the **Account** tab.</span></span>

       1. <span data-ttu-id="d4534-255">**メール プロバイダー ID** (SMTP など) を設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-255">Set the **Email provider ID** (for example, SMTP).</span></span>
       2. <span data-ttu-id="d4534-256">また、既定の **送信元** アドレスが現在のユーザーに対して使用されていない場合は、**送信者電子メール** の上書きを設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-256">Optionally, set a **Sender email** override if the default **send from** address should not be used for the current user.</span></span>

    3. <span data-ttu-id="d4534-257">**ワークフロー** タブに移動します。電子メールで通知を送信するオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-257">Navigate to the **Workflow** tab. Set the option to send notifications in email to **Yes**.</span></span>

6. <span data-ttu-id="d4534-258">ワークフロー システムが電子メール通知を送信することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-258">Verify that the workflow system will send email notifications:</span></span>

    <span data-ttu-id="d4534-259">通知する必要があるワークフローごとに、ワークフロー エディターでワークフロー プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="d4534-259">For each workflow that should have a notification, open the workflow properties in the workflow editor.</span></span>

    1. <span data-ttu-id="d4534-260">**基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-260">Click **Basic settings**.</span></span> <span data-ttu-id="d4534-261">ワークフロー通知の電子メール テンプレートを調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-261">Adjust the email template for the workflow notifications.</span></span>
    2. <span data-ttu-id="d4534-262">**通知** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-262">Click **Notifications**.</span></span>

        1. <span data-ttu-id="d4534-263">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d4534-263">Enable the events for which a user should be notified.</span></span>
        2. <span data-ttu-id="d4534-264">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-264">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

    3. <span data-ttu-id="d4534-265">ユーザーに通知される必要のあるワークフロー承認要素:</span><span class="sxs-lookup"><span data-stu-id="d4534-265">On a workflow approval element for which a user should be notified:</span></span>

        1. <span data-ttu-id="d4534-266">**プロパティ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-266">Go to **Properties**.</span></span>
        2. <span data-ttu-id="d4534-267">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d4534-267">Enable the events for which a user should be notified.</span></span>
        3. <span data-ttu-id="d4534-268">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-268">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

### <a name="workflow-email-notification-testing"></a><span data-ttu-id="d4534-269">ワークフロー電子メール通知のテスト</span><span class="sxs-lookup"><span data-stu-id="d4534-269">Workflow email notification testing</span></span>

<span data-ttu-id="d4534-270">電子メール通知のテストでは、単に通知をトリガーし、それを確認するだけです。</span><span class="sxs-lookup"><span data-stu-id="d4534-270">The testing for email notifications is to simply trigger the notification and then check for it.</span></span>

1. <span data-ttu-id="d4534-271">電子メール通知に対して設定されているワークフローを送信します。</span><span class="sxs-lookup"><span data-stu-id="d4534-271">Submit a workflow that has been set up for email notifications.</span></span>
2. <span data-ttu-id="d4534-272">ワークフロー履歴をチェックして、ワークフロー作業項目が予定されたユーザーに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-272">Check the workflow history to make sure that a workflow work item was assigned to the expected user.</span></span>
3. <span data-ttu-id="d4534-273">**システム管理** \> **定期タスク** \> **メール処理** \> **バッチメール送信ステータス** で、保留になっておりメール通知のステータスを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-273">Check the status of the pending email notification in **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch email sending status**.</span></span>

    <span data-ttu-id="d4534-274">電子メールが送信に失敗した場合は、SMTP メール アカウントを開くことができることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-274">If the email is fails to send, make sure that the SMTP mail account can be opened.</span></span>

4. <span data-ttu-id="d4534-275">適切な受信トレイで電子メール通知を確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-275">Check for the email notification in the appropriate inbox.</span></span>

## <a name="troubleshoot-email"></a><span data-ttu-id="d4534-276">電子メールのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d4534-276">Troubleshoot email</span></span>

<span data-ttu-id="d4534-277">メール設定のトラブルシューティングに役立つ標準的な手順がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="d4534-277">There are a few standard steps that can help you troubleshoot the configuration of email settings.</span></span>

1. <span data-ttu-id="d4534-278">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="d4534-278">Verify email settings:</span></span>

    1. <span data-ttu-id="d4534-279">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-279">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="d4534-280">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-280">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="d4534-281">SMTP メール サーバーの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-281">Verify the settings of the SMTP mail server.</span></span>
    4. <span data-ttu-id="d4534-282">アカウントとパスワードが正確であるかことを確認するために、別のウィンドウで SMTP アカウントにログインします。</span><span class="sxs-lookup"><span data-stu-id="d4534-282">Sign in to the SMTP account in a separate window to make sure that the account and password are correct.</span></span>
    5. <span data-ttu-id="d4534-283">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="d4534-283">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>

2. <span data-ttu-id="d4534-284">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-284">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="d4534-285">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **バッチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-285">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch**.</span></span>
    2. <span data-ttu-id="d4534-286">**バッチ処理** オプションが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-286">Make sure that the **Batch processing** option is set to **Yes**.</span></span>
    3. <span data-ttu-id="d4534-287">電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-287">Review the recurrence of the email process:</span></span>

        1. <span data-ttu-id="d4534-288">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-288">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="d4534-289">必要に応じてカウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="d4534-289">Adjust the count as you require.</span></span>

3. <span data-ttu-id="d4534-290">コンテンツとバッチメールのステータスをレビューするには、**システム管理** \> **定期タスク** \> **メール処理** \> **バッチメール送信ステータス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4534-290">To review the contents and status of batch emails, go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch email sending status**.</span></span>

    1. <span data-ttu-id="d4534-291">プラットフォーム更新プログラム 28 より前のリリースを使用している場合は、フォームをパーソナライズして電子メールの差出人を追加し確認しやすくします。</span><span class="sxs-lookup"><span data-stu-id="d4534-291">If you're using a release that is earlier than Platform update 28, personalize the form to add the email sender for easy review.</span></span> <span data-ttu-id="d4534-292">これを行うには、グリッド ヘッダーを右クリックし **列の追加** を選択して **電子メール** を選択して、**挿入** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4534-292">To do this, right-click the grid header, select **Add columns**, select **Email**, and then click **Insert**.</span></span> <span data-ttu-id="d4534-293">**電子メール** フィールドがグリッドに追加されていない場合は、**メッセージの表示** を選択してから **電子メール** フィールドを選択して送信者を表示できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-293">If the **Email** field isn't added into the grid, you can view the sender by selecting **Show message**, and then selecting the **Email** field.</span></span>
    2. <span data-ttu-id="d4534-294">電子メールが正しいアカウントから送信されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-294">Verify that emails are being sent from the correct account.</span></span> <span data-ttu-id="d4534-295">アカウントが正しくない場合、必要に応じてユーザー オプション、システム テンプレート、組織テンプレートなどの設定を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4534-295">If the account is incorrect, you need to adjust settings such as user options, system templates,  or organization templates, as needed.</span></span>
    3. <span data-ttu-id="d4534-296">すべての電子メール ユーザー アカウントに構成された SMTP アカウントの **Send As** へのアクセス許可が付与されていることを確認します (詳細は手順 4 を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="d4534-296">Verify that all email user accounts have been granted permission to **Send As** for the configured SMTP account (see step 4 for details).</span></span>
    
4. <span data-ttu-id="d4534-297">プラットフォーム更新 32 では、**メール履歴** ページが追加されており、送信を防ぐことができたかもしれないメールのエラーなど、管理者がすべての送信済みメールを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="d4534-297">In Platform update 32, an **Email history** page was added to allow administrators to review all sent emails, including any errors that might have prevented an email from being sent.</span></span> <span data-ttu-id="d4534-298">**メール履歴** ページは、対話と、非対話 / バッチメールを表示します。</span><span class="sxs-lookup"><span data-stu-id="d4534-298">The **Email history** page will show interactive as well as non-interactive/batch emails.</span></span> <span data-ttu-id="d4534-299">**メール ステータス** が **エラー** となっているメールに対しては、**エラー詳細** タブでエラー メッセージをレビューして、必要な処置を取るべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d4534-299">For any emails that have an **Email status** of **Failed**, review the error message on the **Failure details** tab and determine if corrective actions should be taken.</span></span>

5. <span data-ttu-id="d4534-300">Microsoft 365 管理センターで、電子メールの送信に使用されるすべてのユーザー メール アカウントに、構成された SMTP アカウントに対する **送信者** と **代理送信** アクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-300">In the Microsoft 365 admin center, verify that all user mail accounts that will be used to send emails have **Send As** and **Send On Behalf Of** permissions for the configured SMTP account.</span></span> <span data-ttu-id="d4534-301">詳細については、[Microsoft 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d4534-301">For more information, see [Enable sending email from another user's mailbox in Microsoft 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span>
6. <span data-ttu-id="d4534-302">すべてのユーザー メールボックスにサインインして、メールボックスが有効で、サインインを使用してアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-302">Sign in to all user mailboxes to verify that they are valid and can be accessed using sign in.</span></span>
7. <span data-ttu-id="d4534-303">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="d4534-303">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>
8. <span data-ttu-id="d4534-304">SMTP 設定を別の環境から移行した場合は、パスワード フィールドをクリアしてパスワードを再入力し、フィールドの暗号化が保存された値に悪影響を与えていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-304">If the SMTP settings were migrated from another environment, clear the password field and re-enter the password to ensure that the field encryption hasn't negatively affected the stored value.</span></span>
9. <span data-ttu-id="d4534-305">SMTP を介して電子メールを送信すると問題が発生する場合は、[SMTPer.net](https://www.smtper.net/) のようなツールに SMTP アカウント情報を入力して SMTP サーバーとアカウントが有効で正しく機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-305">If you continue to experience issues when email is sent via SMTP, enter the SMTP account information in a tool such as [SMTPer.net](https://www.smtper.net/) to verify that the SMTP server and account are valid and working correctly.</span></span>


## <a name="troubleshoot-the-exchange-mail-provider"></a><span data-ttu-id="d4534-306">Exchange メール プロバイダーのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d4534-306">Troubleshoot the Exchange mail provider</span></span>

<span data-ttu-id="d4534-307">**電子メール パラメーター** ページで管理者は対話型の電子メール プロバイダーおよびバッチ電子メール プロバイダーとして Exchange を選択できます。</span><span class="sxs-lookup"><span data-stu-id="d4534-307">The **Email parameters** page allows an administrator to select Exchange as an interactive email provider and as the Batch email provider.</span></span> <span data-ttu-id="d4534-308">Exchange メール プロバイダーは、現在のユーザーの Exchange Online アカウントを使用して電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="d4534-308">The Exchange mail provider will use the current user's Exchange Online account to send emails.</span></span> <span data-ttu-id="d4534-309">バッチ電子メール プロバイダーとして使用された場合は、バッチ アカウントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-309">When used as the Batch email provider, the batch account will be used.</span></span> <span data-ttu-id="d4534-310">追加のコンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d4534-310">No additional configuration is needed.</span></span> <span data-ttu-id="d4534-311">トラブルシューティングが必要な場合は、現在のユーザーのアカウントにサインインできることと、そのアカウントから目的の受信者に電子メールを送信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d4534-311">If troubleshooting is needed, ensure that the current user's account can be signed into and that emails can be sent from that account to the intended recipients.</span></span>

### <a name="exchange-mail-provider-not-supported-for-external-users"></a><span data-ttu-id="d4534-312">外部ユーザーに対しては、Exchange メール プロバイダーはサポートされていません</span><span class="sxs-lookup"><span data-stu-id="d4534-312">Exchange mail provider not supported for external users</span></span>

<span data-ttu-id="d4534-313">主テナントに対して外部であるユーザーはそのテナントで Exchange アカウントを持たず、そのため Exchange メール プロバイダーは、外部ユーザーをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="d4534-313">Users that are external to the primary tenant will not have exchange accounts on that tenant, so the Exchange mail provider is not supported for external users.</span></span>

## <a name="other-notes"></a><span data-ttu-id="d4534-314">その他のメモ</span><span class="sxs-lookup"><span data-stu-id="d4534-314">Other notes</span></span>

<span data-ttu-id="d4534-315">システムは Exchange や一般的な電子メール クライアントのような SMTP サーバーと通信するため、標準の動作と制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-315">The system communicates with Exchange or an SMTP server like a typical email client, so standard behavior and limits apply.</span></span> <span data-ttu-id="d4534-316">たとえば、標準の [Exchange Online 送受信制限](https://technet.microsoft.com/library/exchange-online-limits.aspx#RecipientLimits)が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-316">For example, standard [Exchange Online receiving and sending limits](https://technet.microsoft.com/library/exchange-online-limits.aspx#RecipientLimits) apply.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="d4534-317">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d4534-317">Troubleshooting</span></span>

### <a name="where-do-workflow-email-templates-come-from"></a><span data-ttu-id="d4534-318">ワークフロー電子メール テンプレートはどこから取得されますか。</span><span class="sxs-lookup"><span data-stu-id="d4534-318">Where do workflow email templates come from?</span></span>

<span data-ttu-id="d4534-319">ワークフローがシステムレベル (会社固有ではない) または組織レベル (会社固有) のワークフローのいずれであるかによって、電子メール テンプレートは、システム電子メール テンプレートまたは組織の電子メール テンプレートから取得されます。</span><span class="sxs-lookup"><span data-stu-id="d4534-319">The email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d4534-320">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d4534-320">Additional resources</span></span>

[<span data-ttu-id="d4534-321">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d4534-321">Troubleshoot the Office integration</span></span>](../../dev-itpro/office-integration/office-integration-troubleshooting.md)

[<span data-ttu-id="d4534-322">Office 統合のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="d4534-322">Office integration tutorial</span></span>](../../dev-itpro/office-integration/office-integration-tutorial.md)

<span data-ttu-id="d4534-323">[Microsoft Dynamics AX [AX 2012] で電子メール機能をコンフィギュレーションする](https://technet.microsoft.com/library/aa834374.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4534-323">[Configure email functionality in Microsoft Dynamics AX [AX 2012]](https://technet.microsoft.com/library/aa834374.aspx)</span></span>
