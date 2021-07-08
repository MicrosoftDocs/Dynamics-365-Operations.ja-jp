---
title: 電子メールのコンフィギュレーションと送信
description: 電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。
author: jasongre
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysEmailParameters
audience: IT Pro
ms.reviewer: sericks
ms.custom: 268274
ms.assetid: 194ca8fd-5e20-4464-9c85-08d2b5ff63ca
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a13a77688086c7d1c9825438bb44bcae1623e
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270721"
---
# <a name="configure-and-send-email"></a><span data-ttu-id="1d5b0-103">電子メールのコンフィギュレーションと送信</span><span class="sxs-lookup"><span data-stu-id="1d5b0-103">Configure and send email</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d5b0-104">電子メール サブシステムの動作は、管理者コンフィギュレーション、ユーザー コンフィギュレーション、およびユーザーの選択の組み合わせに影響されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-104">The behavior of the email subsystem is influenced by a combination of administrator configuration, user configuration, and user choices.</span></span> <span data-ttu-id="1d5b0-105">このトピックでは、関連情報を見つけやすくするために、管理者のセクションとユーザーのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-105">This topic is divided into sections for administrators and users to make it easy to find relevant information.</span></span>

<span data-ttu-id="1d5b0-106">管理者とユーザーの両方が電子メールのサブシステムの動作を設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-106">Both administrators and users set the behavior of the email subsystem.</span></span>

## <a name="administrator-email-parameters-page"></a><span data-ttu-id="1d5b0-107">[管理者] 電子メール パラメーター ページ</span><span class="sxs-lookup"><span data-stu-id="1d5b0-107">[Administrator] Email parameters page</span></span> 

### <a name="configuration-tab"></a><span data-ttu-id="1d5b0-108">構成タブ</span><span class="sxs-lookup"><span data-stu-id="1d5b0-108">Configuration tab</span></span>
<span data-ttu-id="1d5b0-109">**メール パラメーター** ページで、**構成** タブの次の設定に注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-109">On the **Email parameters** page, note the following settings on the **Configuration** tab.</span></span>

| <span data-ttu-id="1d5b0-110">フィールド</span><span class="sxs-lookup"><span data-stu-id="1d5b0-110">Field</span></span>                 | <span data-ttu-id="1d5b0-111">説明</span><span class="sxs-lookup"><span data-stu-id="1d5b0-111">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="1d5b0-112">バッチ電子メール プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1d5b0-112">Batch email provider</span></span>  | <span data-ttu-id="1d5b0-113">バッチ方式または非対話型のプロセスで送信される電子メールの送信に使用される電子メール プロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-113">Specifies which email provider will be used to send emails that are sent by processes in a batch or non-interactive manner.</span></span> <span data-ttu-id="1d5b0-114">Exchange プロバイダーは、バッチ プロセスに関連付けられているアカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-114">The Exchange provider will use the account associated with the batch process.</span></span> |
| <span data-ttu-id="1d5b0-115">添付ファイル サイズの上限</span><span class="sxs-lookup"><span data-stu-id="1d5b0-115">Attachment size limit</span></span> | <span data-ttu-id="1d5b0-116">電子メール サブシステム経由で送信できる 1 つの電子メールの最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-116">Specifies the maximum size of a single email that can be sent via the email subsystem.</span></span> |

<span data-ttu-id="1d5b0-117">**メール履歴** セクションには 2 つの目的があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-117">The **Email history** section serves two purposes.</span></span> <span data-ttu-id="1d5b0-118">まず、**メール履歴** ページへのエントリ ポイントを提供します。これにより、送信を防ぐことができたかもしれないメールのエラーなど、管理者がすべての送信済みメールを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-118">First, it provides an entry point to the **Email history** page, which allows administrators to review all sent emails, including any errors that might have prevented an email from being sent.</span></span> <span data-ttu-id="1d5b0-119">次に、メールの履歴を維持する期間を構成できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-119">Second, it allows you to configure how long to maintain email history.</span></span> <span data-ttu-id="1d5b0-120">既定では、メール履歴は過去 30 日間保持されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-120">By default, the last 30 days of email history is retained.</span></span> <span data-ttu-id="1d5b0-121">これは、**メール履歴の保持日数** をゼロ以外の値に変更することで調整できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-121">This can be adjusted by changing the **Number of days to retain email history** field to a non-zero amount.</span></span> <span data-ttu-id="1d5b0-122">0 値は、既定の金額と動作に戻ります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-122">A value of zero reverts back to the default amount and behavior.</span></span>

<span data-ttu-id="1d5b0-123">バージョン 10.0.16 では、機能管理でご使用の環境で **電子メール調整** 機能がオンになっている場合、**電子メール調整** セクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-123">In version 10.0.16, an **Email throttling** section is visible if the **Email throttling** feature has been turned on for your environment in Feature management.</span></span> <span data-ttu-id="1d5b0-124">この機能により非対話型の電子メール プロバイダー (バッチ電子メール プロバイダーなど) は 1 分あたりの送信制限に従うことができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-124">This feature enables non-interactive email providers (such as the batch email provider) to adhere to a per-minute sending limit.</span></span> <span data-ttu-id="1d5b0-125">したがって、システムがプロバイダーが許可する数を超える電子メールを送信しようとした場合に、いくつかのエラーを防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-125">Therefore, it can help prevent some errors if the system tries to send more emails than the provider allows.</span></span> <span data-ttu-id="1d5b0-126">具体的に、1 分あたりの送信制限に達したために最初に電子メールを送信できない場合、電子メールの送信試行は最大 1 分間延期されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-126">Specifically, if an email can't be originally sent because the per-minute sending limit has been reached, the send attempt for the email will be deferred for up to one minute.</span></span> <span data-ttu-id="1d5b0-127">10 回の延期後、1 分あたりの送信制限に達した場合でも、システムは電子メールを送信しようとします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-127">After ten deferrals, the system will try to send the email even if the per-minute sending limit has been reached.</span></span> <span data-ttu-id="1d5b0-128">Microsoft 365 電子メール プロバイダーの送信制限は、[Exchange Online 送信制限](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits) に応じて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-128">The sending limits for Microsoft 365 email providers are automatically set according to [Exchange Online sending limits](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#sending-limits).</span></span> <span data-ttu-id="1d5b0-129">他のすべての電子メール プロバイダーについては、手動での構成が必要です。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-129">Manual configuration is required for all other email providers.</span></span> <span data-ttu-id="1d5b0-130">**1 分あたりの電子メール送信制限** フィールドを **0** にリセットすることにより、プロバイダーから 1 分あたりの送信制限を削除できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-130">You can remove the per-minute sending limit from a provider by resetting the **per-minute email sending limit** field to **0**.</span></span>

### <a name="smtp-settings-tab"></a><span data-ttu-id="1d5b0-131">SMTP 設定タブ</span><span class="sxs-lookup"><span data-stu-id="1d5b0-131">SMTP settings tab</span></span>
<span data-ttu-id="1d5b0-132">**電子メール パラメーター** ページの、**SMTP 設定** タブで、次の設定に注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-132">On the **Email parameters** page, note the following settings on the **SMTP settings** tab.</span></span>

#### <a name="server-information"></a><span data-ttu-id="1d5b0-133">サーバー情報</span><span class="sxs-lookup"><span data-stu-id="1d5b0-133">Server information</span></span>
<table>
<thead>  
<tr>
<th><span data-ttu-id="1d5b0-134">フィールド</span><span class="sxs-lookup"><span data-stu-id="1d5b0-134">Field</span></span></th>
<th><span data-ttu-id="1d5b0-135">説明</span><span class="sxs-lookup"><span data-stu-id="1d5b0-135">Description</span></span></th>
</tr>
</thead>
<tbody>
  <tr>
    <td><span data-ttu-id="1d5b0-136">送信メール サーバー</span><span class="sxs-lookup"><span data-stu-id="1d5b0-136">Outgoing mail server</span></span></td>
    <td><span data-ttu-id="1d5b0-137">目的の Simple Mail Transfer Protocol (SMTP) サーバーのホスト名。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-137">The host name of the desired Simple Mail Transfer Protocol (SMTP) server.</span></span>
      <ul>
        <li><span data-ttu-id="1d5b0-138"><a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Microsoft 365 製品</a> (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-138">For <a href="https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c">Microsoft 365 production</a> (including \*.onmicrosoft.com accounts), use smtp.office365.com.</span></span> <span data-ttu-id="1d5b0-139">(<strong>設定</strong> &gt; <strong>メール</strong> &gt; <strong>POP および IMAP</strong>の outlook.office.com でこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="1d5b0-139">(You can find this setting at outlook.office.com at <strong>Settings</strong> &gt; <strong>Mail</strong> &gt; <strong>POP and IMAP</strong>.)</span></span></li>
        <li><span data-ttu-id="1d5b0-140">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-140">For Outlook/Hotmail, use smtp-mail.outlook.com.</span></span></li>
      </ul>
    </td>
  </tr>
    
  <tr>
    <td><span data-ttu-id="1d5b0-141">SMTP ポート番号</span><span class="sxs-lookup"><span data-stu-id="1d5b0-141">SMTP port number</span></span></td>
    <td><span data-ttu-id="1d5b0-142">通常、セキュリティで保護して送信するためにポート番号は 587 に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-142">Typically, the port number should be set to 587 for secure transport.</span></span></td>
  </tr>

  <tr>
    <td><span data-ttu-id="1d5b0-143">SSL が必要です</span><span class="sxs-lookup"><span data-stu-id="1d5b0-143">SSL required</span></span></td>
    <td><span data-ttu-id="1d5b0-144">安全なトランスポートをを使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-144">Determines whether secure transport is used.</span></span> <span data-ttu-id="1d5b0-145">これは通常、内部またはトラブルシューティングのシナリオを除き、<strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-145">Typically, this is <strong>Yes</strong>, except for internal or troubleshooting scenarios.</span></span></td>
  </tr>
</tbody>
</table>  
  
#### <a name="authentication"></a><span data-ttu-id="1d5b0-146">認証</span><span class="sxs-lookup"><span data-stu-id="1d5b0-146">Authentication</span></span>

<table>
<thead>  
<tr>
<th><span data-ttu-id="1d5b0-147">フィールド</span><span class="sxs-lookup"><span data-stu-id="1d5b0-147">Field</span></span></th>
<th><span data-ttu-id="1d5b0-148">説明</span><span class="sxs-lookup"><span data-stu-id="1d5b0-148">Description</span></span></th>
</tr>
</thead>
<tbody>
  <tr>
    <td><span data-ttu-id="1d5b0-149">認証が必要です</span><span class="sxs-lookup"><span data-stu-id="1d5b0-149">Authentication required</span></span></td>
    <td><span data-ttu-id="1d5b0-150">電子メールの送信にユーザー名とパスワードが必要かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-150">Determines whether a user name and password are needed to send emails.</span></span> </td>
  </tr>

  <tr>
    <td><span data-ttu-id="1d5b0-151"><strong>ユーザー名</strong>と<strong>パスワード</strong></span><span class="sxs-lookup"><span data-stu-id="1d5b0-151"><strong>User name</strong> and <strong>Password</strong></span></span></td>
    <td><span data-ttu-id="1d5b0-152">認証が必要な場合は、電子メールを送信する適切なメール アカウントを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-152">If authentication is required, specify the appropriate mail account to send email from.</span></span> <span data-ttu-id="1d5b0-153">すべてのユーザーは SMTP アカウントを指定し <strong> 送信者 </strong> および <strong> 代理送信 </strong> 許可をし、SMTP で送信する機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-153">All users need to provide the SMTP account <strong>Send As</strong> and <strong>Send On Behalf Of</strong> permissions to enable the ability to send SMTP mail.</span></span> <span data-ttu-id="1d5b0-154">[送信者] 権限は、Microsoft 365 管理センター (portal.office.com/Admin) にて、<strong> ユーザー </strong> &gt; <strong> 有効なユーザー </strong> &gt; <strong> ユーザー </strong> &gt; <strong> メールボックスのアクセス許可を編集 </strong> &gt; <strong> このメールボックスから電子メールを送信する </strong> で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-154">You can configure Send As permissions in the Microsoft 365 admin center (portal.office.com/Admin) at <strong>Users</strong> &gt; <strong>Active users</strong> &gt; <strong>User</strong> &gt; <strong>Edit mailbox permissions</strong> &gt; <strong>Send email from this mailbox</strong>.</span></span> <span data-ttu-id="1d5b0-155">詳細については、<a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Microsoft 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-155">For more information, see <a href="https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E">Enable sending email from another user's mailbox in Microsoft 365</a>.</span></span>
    </td>
  </tr>
      
</tbody>

</table>

## <a name="administrator-email-distributor-batch-process"></a><span data-ttu-id="1d5b0-156">[管理者] 電子メール配布バッチ処理</span><span class="sxs-lookup"><span data-stu-id="1d5b0-156">[Administrator] Email distributor batch process</span></span>

<span data-ttu-id="1d5b0-157">ユーザーの操作なしに、SMTP 経由でサーバーから直接送信される電子メールは、**電子メール ディストリビューター バッチ** プロセスによって送信されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-157">Email that is sent directly from the server, without user interaction, via SMTP is sent by the **Email distributor batch** process.</span></span> <span data-ttu-id="1d5b0-158">電子メールのキューの処理には、そのバッチ処理を開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-158">That batch process must be started to process the email queue.</span></span> <span data-ttu-id="1d5b0-159">プロセスを開始するには、**電子メール配布バッチ** ウィンドウ (**システム管理**&gt;**定期タスク**&gt;**電子メール処理**&gt;**バッチ**) を開いて、**バッチ処理** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-159">To start the process, open the **Email distributor batch** pane (**System administration** &gt; **Periodic tasks** &gt; **Email processing** &gt; **Batch**) and turn on **Batch processing**.</span></span>

<span data-ttu-id="1d5b0-160">為替プロバイダーを使用している場合、バッチ プロセス (通常は管理者) に関連付けられているユーザー アカウントが送信者になります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-160">If the Exchange provider is used, then the user account associated with the batch process (usually admin) will be sender.</span></span>

## <a name="administrator-user-email"></a><span data-ttu-id="1d5b0-161">[管理者] ユーザーの電子メール</span><span class="sxs-lookup"><span data-stu-id="1d5b0-161">[Administrator] User email</span></span>

<span data-ttu-id="1d5b0-162">各ユーザーの既定の **送信元** アドレスは、**ユーザー** ページの **電子メール** フィールドから取得されます (**システム管理** &gt; **ユーザー** &gt; **ユーザー**)。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-162">The default **send from** address for each user is pulled from the **Email** field on the **Users** page (**System administration** &gt; **Users** &gt; **Users**).</span></span> <span data-ttu-id="1d5b0-163">管理者は必要に応じて、**オプション** ページの **送信者電子メール** フィールドを使用して、この既定の **送信元** を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-163">Administrators can override this **send from** default if needed using the **Sender email** field on the **Options** page.</span></span>

## <a name="user-email-provider-selection-section-on-the-options-page"></a><span data-ttu-id="1d5b0-164">[ユーザー] オプション ページの電子メール プロバイダーの選択セクション</span><span class="sxs-lookup"><span data-stu-id="1d5b0-164">[User] Email provider selection section on the Options page</span></span>

<span data-ttu-id="1d5b0-165">**オプション** ページは、**設定 &gt; ユーザー オプション** から開くことができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-165">The **Options** page can be opened via **Settings &gt; User options**.</span></span> <span data-ttu-id="1d5b0-166">**電子メール プロバイダーの選択** セクションは、**アカウント** タブにあります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-166">The **Email provider selection** section is on the **Account** tab.</span></span>

| <span data-ttu-id="1d5b0-167">フィールド</span><span class="sxs-lookup"><span data-stu-id="1d5b0-167">Field</span></span>             | <span data-ttu-id="1d5b0-168">説明</span><span class="sxs-lookup"><span data-stu-id="1d5b0-168">Description</span></span> |
|-------------------|-------------|
| <span data-ttu-id="1d5b0-169">電子メール プロバイダー ID</span><span class="sxs-lookup"><span data-stu-id="1d5b0-169">Email provider ID</span></span> | <span data-ttu-id="1d5b0-170">ユーザーは、電子メールを送信するときに使用する電子メール プロバイダーを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-170">Allows the user to select the email provider that should be used when sending an email.</span></span> <span data-ttu-id="1d5b0-171">ここでオプションを選択することは、**どのように電子メール送信しますか** ダイアログ ボックスで **今後確認しない** をオンにするのと同じです。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-171">Selecting an option here is the equivalent of selecting **Do not ask again** in the **How would you like to send email** dialog box.</span></span> <span data-ttu-id="1d5b0-172">空白のオプション **使用する電子メール プロバイダーの入力を求める** を選択すると、メールが送信されるときに **電子メールを送信する方法** ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-172">Selecting the blank option **Prompt for which email provider to use** will cause the **How would you like to send email** dialog box to display when an email is going to be sent.</span></span> |
| <span data-ttu-id="1d5b0-173">送信者の電子メール</span><span class="sxs-lookup"><span data-stu-id="1d5b0-173">Sender email</span></span>    | <span data-ttu-id="1d5b0-174">管理者が電子メールの **ソース** フィールドでユーザーに電子メール アドレスの上書きを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-174">Allows the administrator to provide an email address override for the user in the **From** field of the email.</span></span> <span data-ttu-id="1d5b0-175">既定では、ユーザー アカウントに関連付けられた電子メール エイリアスは新しい電子メールの **ソース** フィールドとして使用されますが、このユーザー オプションの電子メール アドレスによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-175">By default, the email alias that is associated with the user account is used as the **From** field in new emails, but this user option email address will override that.</span></span> <span data-ttu-id="1d5b0-176">SMTP で電子メールを送信するとき、ユーザーは交換または SMTP サーバー上で構成された適切な **送信者** および **代理送信者** アクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-176">When sending email via SMTP, the user needs to have appropriate **Send As** and **Send On Behalf Of** permissions configured in Exchange or on the SMTP server.</span></span><blockquote>[!NOTE] <span data-ttu-id="1d5b0-177">**送信者** および **代理送信** 権限は、 Microsoft 365 管理センター (portal.office.com/Admin) にて、**ユーザー** &gt; **有効なユーザー** &gt; **ユーザー** &gt; **メール ボックスのアクセス許可を編集** &gt; **このメールボックスから電子メールを送信する** で構成することができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-177">You can configure **Send As** and **Send On Behalf Of** permissions in the Microsoft 365 admin center (portal.office.com/Admin) at **Users** &gt; **Active users** &gt; **User** &gt; **Edit mailbox permissions** &gt; **Send email from this mailbox**.</span></span> <span data-ttu-id="1d5b0-178">詳細については、[Microsoft 365 で別のユーザーのメールボックスからの電子メールの送信を有効にする](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-178">For more information, see [Enable sending email from another user's mailbox in Microsoft 365](https://support.office.com/article/Enable-sending-email-from-another-user-s-mailbox-in-Office-365-2B828C5F-41AB-4904-97B9-3B63D8129C4E).</span></span></blockquote> |

## <a name="user-how-would-you-like-to-send-email-dialog-box-optional"></a><span data-ttu-id="1d5b0-179">[ユーザー] 電子メール ダイアログ ボックスをどのように送信しますか (省略可)</span><span class="sxs-lookup"><span data-stu-id="1d5b0-179">[User] How would you like to send email dialog box (optional)</span></span>

<span data-ttu-id="1d5b0-180">電子メールを送信するときは、**電子メールをどのように送信しますか** ダイアログ ボックスが表示され、それに電子メールを送信するために使用可能なオプションが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-180">When an email is going to be sent, the user will see the **How would you like to send email** dialog box that will list the available options for sending email.</span></span>

| <span data-ttu-id="1d5b0-181">フィールド</span><span class="sxs-lookup"><span data-stu-id="1d5b0-181">Field</span></span>                                                                  | <span data-ttu-id="1d5b0-182">説明</span><span class="sxs-lookup"><span data-stu-id="1d5b0-182">Description</span></span> |
|------------------------------------------------------------------------|-------------|
| <span data-ttu-id="1d5b0-183">Outlook などの電子メール アプリケーションを使用します</span><span class="sxs-lookup"><span data-stu-id="1d5b0-183">Use an email app, such as Outlook</span></span>                                      | <span data-ttu-id="1d5b0-184">生成された電子メール (.eml) を持つを提供します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-184">Provides the user with a generated email (.eml) file.</span></span> |
| <span data-ttu-id="1d5b0-185">Exchange 電子メール サーバーを使用します</span><span class="sxs-lookup"><span data-stu-id="1d5b0-185">Use Exchange email server</span></span>                                              | <span data-ttu-id="1d5b0-186">テナントに関連付けられている Exchange Online サーバーを使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-186">Uses the Exchange Online server associated with the tenant.</span></span> <span data-ttu-id="1d5b0-187">**Exchange** メール プロバイダーは、現在、オンプレミス環境を含むパブリック クラウドの外部ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-187">The **Exchange** mail provider is currently not supported outside the public cloud, including on-premises environments.</span></span> |
| <span data-ttu-id="1d5b0-188">システムの電子メール クライアントの使用</span><span class="sxs-lookup"><span data-stu-id="1d5b0-188">Use the system email client</span></span> | <span data-ttu-id="1d5b0-189">**電子メール送信する** 構成ダイアログ ボックスを開いて、結果を電子メールで SMTP 経由で送信します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-189">Opens the **Send email** composition dialog box and then sends the resulting email via SMTP.</span></span> |
| <span data-ttu-id="1d5b0-190">今後このメッセージを表示しない</span><span class="sxs-lookup"><span data-stu-id="1d5b0-190">Do not ask again</span></span>                                                       | <span data-ttu-id="1d5b0-191">このフィールドが選択されていない場合は、次回に電子メールが送信されたときに最後に選択したオプションが使用され、ダイアログ ボックスが表示されません。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-191">If this field is not selected, the next time an email is sent the most recently selected option will be used and the dialog box will not open.</span></span> |

## <a name="user-send-email-dialog-box-optional"></a><span data-ttu-id="1d5b0-192">[ユーザー] 電子メール ダイアログ ボックスを送信 (省略可)</span><span class="sxs-lookup"><span data-stu-id="1d5b0-192">[User] Send email dialog box (optional)</span></span>

<span data-ttu-id="1d5b0-193">**電子メール送信** ダイアログ ボックスが開き、送信される電子メールの内容を編集できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-193">The **Send email** dialog box is opened to allow the user to edit the contents of the email that will be sent.</span></span> <span data-ttu-id="1d5b0-194">次のフィールドの一部は、このウィンドウであらかじめ設定されています。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-194">Some of the following fields will be pre-populated in this window.</span></span>

| <span data-ttu-id="1d5b0-195">フィールド</span><span class="sxs-lookup"><span data-stu-id="1d5b0-195">Field</span></span>                                                     | <span data-ttu-id="1d5b0-196">説明</span><span class="sxs-lookup"><span data-stu-id="1d5b0-196">Description</span></span> |
|-----------------------------------------------------------|-------------|
| <span data-ttu-id="1d5b0-197">自</span><span class="sxs-lookup"><span data-stu-id="1d5b0-197">From</span></span>                                                      | <span data-ttu-id="1d5b0-198">**オプション** ページの **メール** フィールドから取得されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-198">Populated from the **Email** field on the **Options** page.</span></span> |
| <span data-ttu-id="1d5b0-199">**宛先**、**Cc**、**Bcc**、**件名**、および **本文**</span><span class="sxs-lookup"><span data-stu-id="1d5b0-199">**To**, **Cc**, **Bcc**, **Subject**, and **Body**</span></span> | <span data-ttu-id="1d5b0-200">電子メールの送信を開始したプロセスによって指定された値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-200">Populated with values specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="1d5b0-201">これらのフィールドは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-201">These fields can be edited as needed by the user.</span></span> |
| <span data-ttu-id="1d5b0-202">添付ファイル リスト</span><span class="sxs-lookup"><span data-stu-id="1d5b0-202">Attachments list</span></span>                                          | <span data-ttu-id="1d5b0-203">電子メールの送信を開始したプロセスによって指定されたファイルが添付される場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-203">May be populated with attachments specified by the process that initiated the sending of the email.</span></span> <span data-ttu-id="1d5b0-204">このリストは、必要に応じてユーザーが編集できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-204">This list can be edited as needed by the user.</span></span> |

<span data-ttu-id="1d5b0-205">電子メールを送信する準備ができたら、**送信** ボタンを使用して SMTP 経由で電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-205">When the email is ready to be sent, the **Send** button will cause the email to be sent via SMTP.</span></span>

## <a name="usage-scenarios-to-verify-if-email-is-configured-correctly"></a><span data-ttu-id="1d5b0-206">電子メールが正しく設定されているかどうかを確認するための使用シナリオ</span><span class="sxs-lookup"><span data-stu-id="1d5b0-206">Usage scenarios to verify if email is configured correctly</span></span>

### <a name="send-mail-via-a-local-mail-client"></a><span data-ttu-id="1d5b0-207">ローカル メール クライアント経由で電子メールを送信</span><span class="sxs-lookup"><span data-stu-id="1d5b0-207">Send mail via a local mail client</span></span>

<span data-ttu-id="1d5b0-208">SysEmail フレームワークで有効になっている電子メール ワークフローでは、添付ファイルを含む電子メール メッセージ (.eml files) を生成できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-208">Email workflows that are enabled via the SysEmail framework can generate email messages (.eml files) that contain attachments.</span></span> <span data-ttu-id="1d5b0-209">これらのメッセージは Microsoft Outlook または他の電子メール クライアント経由で送信することができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-209">You can then send these messages via Microsoft Outlook or another email client.</span></span>

1. <span data-ttu-id="1d5b0-210">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-210">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
2. <span data-ttu-id="1d5b0-211">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-211">Select **US-008 Sparrow Retail**.</span></span>
3. <span data-ttu-id="1d5b0-212">**回収** &gt; **顧客残高** &gt; **コレクション** の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-212">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
4. <span data-ttu-id="1d5b0-213">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-213">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
5. <span data-ttu-id="1d5b0-214">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-214">Click **OK** to accept the default values in the dialog box.</span></span>
6. <span data-ttu-id="1d5b0-215">メール オプションの使用を促すメッセージが表示された場合は、**再度確認しない** チェック ボックス (このオプションは **ユーザー オプション** ページから変更できます) をオフにし、**Outlook などの電子メール アプリケーションを使用** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-215">If you're prompted for the mail option to use, clear the **Do not ask again** check box (you can change this option from the **User options** page), select **Use an email app, such as Outlook**, and then click **OK**.</span></span>
7. <span data-ttu-id="1d5b0-216">コンピューター上で Internet Explorer を使用している場合は、生成される電子メール (.eml) ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-216">If you're using Internet Explorer on your computer, open the email (.eml) file that is generated.</span></span> <span data-ttu-id="1d5b0-217">VM 上で Internet Explorer を使用している場合は、ファイルをコンピューターにコピーし、そのコンピュータでファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-217">If you're using Internet Explorer on the VM, copy the file to your computer, and open it there.</span></span>
8. <span data-ttu-id="1d5b0-218">**宛先** フィールドの電子メール アドレスと生成されたブック添付ファイルに注意します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-218">Note the email address in the **To** field and the generated workbook attachment.</span></span>

### <a name="send-mail-via-smtp"></a><span data-ttu-id="1d5b0-219">SMTP 経由でメールを送信</span><span class="sxs-lookup"><span data-stu-id="1d5b0-219">Send mail via SMTP</span></span>

<span data-ttu-id="1d5b0-220">SysEmail フレームワークを介して有効になっている電子メール ワークフローは、簡単な電子メール ダイアログ ボックスで作成し、Simple Mail Transfer Protocol (SMTP) 経由で送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-220">Email workflows that are enabled via the SysEmail framework can also be created in a simple email dialog box and then sent via Simple Mail Transfer Protocol (SMTP).</span></span>

1. <span data-ttu-id="1d5b0-221">**電子メール パラメーター** のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-221">Go to the **Email parameters** page.</span></span>
2. <span data-ttu-id="1d5b0-222">**SMTP 設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-222">Click **SMTP settings**.</span></span>
3. <span data-ttu-id="1d5b0-223">**送信メール サーバー** を要求された SMTP サーバーに設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-223">Set the **Outgoing mail server** to the desired SMTP server:</span></span>

    - <span data-ttu-id="1d5b0-224">[Microsoft 365 製品](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (\*.onmicrosoft.com アカウントを含む) では、smtp.office365.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-224">For [Microsoft 365 production](https://support.office.com/article/Outlook-settings-for-POP-and-IMAP-access-for-Office-365-for-business-or-Microsoft-Exchange-accounts-7fc677eb-2491-4cbc-8153-8e7113525f6c) (including \*.onmicrosoft.com accounts) use smtp.office365.com.</span></span> <span data-ttu-id="1d5b0-225">(**設定** &gt; **メール** &gt; **POP および IMAP** で outlook.office.com を通してこの設定を検索します。.)</span><span class="sxs-lookup"><span data-stu-id="1d5b0-225">(Find this setting via outlook.office.com, at **Settings** &gt; **Mail** &gt; **POP and IMAP**.)</span></span>
    - <span data-ttu-id="1d5b0-226">Outlook/Hotmail で smtp-mail.outlook.com を使用します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-226">For Outlook/Hotmail use smtp-mail.outlook.com.</span></span>

4. <span data-ttu-id="1d5b0-227">ユーザー名とパスワードを適切な電子メール アカウントとパスワードに設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-227">Set the user name and password to an appropriate email account and password.</span></span>
5. <span data-ttu-id="1d5b0-228">**SSLRequired** を有効のままにして、**SMTP ポート番号** は **587** に設定したままにします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-228">Leave **SSLRequired** turned on, and leave **SMTP port number** set to **587**.</span></span>
6. <span data-ttu-id="1d5b0-229">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-229">Click **Save**.</span></span>
7. <span data-ttu-id="1d5b0-230">Internet Explorer で、**売掛金勘定** &gt; **顧客** &gt; **すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-230">In Internet Explorer, navigate to **Accounts receivable** &gt; **Customers** &gt; **All customers**.</span></span>
8. <span data-ttu-id="1d5b0-231">**US-008 Sparrow Retail** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-231">Select **US-008 Sparrow Retail**.</span></span>
9. <span data-ttu-id="1d5b0-232">**回収** &gt; **顧客残高** &gt; **コレクション** の順にクリックし、**コレクション** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-232">Click **Collect** &gt; **Customer balances** &gt; **Collections** to open the **Collections** page.</span></span>
10. <span data-ttu-id="1d5b0-233">**連絡** &gt; **電子メール** &gt; **連絡先に対する明細書** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-233">Click **Communicate** &gt; **Email** &gt; **Statements to contact**.</span></span>
11. <span data-ttu-id="1d5b0-234">ダイアログ ボックスで既定値を承諾する場合は、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-234">Click **OK** to accept the default values in the dialog box.</span></span>
12. <span data-ttu-id="1d5b0-235">メール オプションを使用するように求められたら、**Microsoft Dynamics 365 for Finance and Operations 電子メール クライアントの使用** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-235">If you're prompted for the mail option to use, select **Use the Microsoft Dynamics 365 for Finance and Operations email client**, and then click **OK**.</span></span>
13. <span data-ttu-id="1d5b0-236">テスト メッセージを受信するには、**宛先アドレス** をメール アドレスに変更します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-236">To receive the test message, change the **To address** to your email address.</span></span>

    <span data-ttu-id="1d5b0-237">SMTP 設定で指定されたアカウントが、電子メール アカウントの **Send As** および **Send On Behalf Of** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-237">Ensure that the account specified in the SMTP settings is able to **Send As** and **Send On Behalf Of** your email account.</span></span> <span data-ttu-id="1d5b0-238">これを確実にするための最も簡単な方法は、電子メール アカウントを SMTP 設定で使用することです。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-238">The easiest way to ensure this to use your email account in the SMTP settings.</span></span>

14. <span data-ttu-id="1d5b0-239">メッセージの件名および本文を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-239">Enter a subject and body for the message.</span></span>
15. <span data-ttu-id="1d5b0-240">**送信** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-240">Click **Send**.</span></span> <span data-ttu-id="1d5b0-241">メッセージは 1 〜 5 分で配信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-241">The message should be delivered in one to five minutes.</span></span>

## <a name="administrator-workflow-email-notifications"></a><span data-ttu-id="1d5b0-242">[管理者] ワークフロー電子メール通知</span><span class="sxs-lookup"><span data-stu-id="1d5b0-242">[Administrator] Workflow email notifications</span></span>

<span data-ttu-id="1d5b0-243">ワークフロー電子メールのコンフィギュレーションは連携して動作する関連設定の集合です。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-243">Workflow email configuration is a collection of related settings that work in conjunction.</span></span>

### <a name="workflow-email-notification-setup"></a><span data-ttu-id="1d5b0-244">ワークフロー電子メール通知のセットアップ</span><span class="sxs-lookup"><span data-stu-id="1d5b0-244">Workflow email notification setup</span></span>

1. <span data-ttu-id="1d5b0-245">電子メール設定の確認:</span><span class="sxs-lookup"><span data-stu-id="1d5b0-245">Verify email settings:</span></span>

    1. <span data-ttu-id="1d5b0-246">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-246">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
    2. <span data-ttu-id="1d5b0-247">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-247">Verify that SMTP is enabled.</span></span>
    3. <span data-ttu-id="1d5b0-248">SMTP メール サーバーの設定を設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-248">Set the SMTP mail server settings.</span></span>

2. <span data-ttu-id="1d5b0-249">電子メールのバッチ処理が実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-249">Verify that the email batch process is running:</span></span>

    1. <span data-ttu-id="1d5b0-250">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **電子メール ディストリビューター バッチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-250">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Email distributor batch**.</span></span>
    2. <span data-ttu-id="1d5b0-251">**バッチ プロセス** オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-251">Enable the **Batch processing** option.</span></span>
    3. <span data-ttu-id="1d5b0-252">必要に応じて、電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-252">Optionally, adjust the recurrence of the email process:</span></span>

        1. <span data-ttu-id="1d5b0-253">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-253">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
        2. <span data-ttu-id="1d5b0-254">カウントを調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-254">Adjust the count.</span></span>
        3. <span data-ttu-id="1d5b0-255">必要に応じて毎分実行するように調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-255">Adjust to run every minute if needed.</span></span>

3. <span data-ttu-id="1d5b0-256">ワークフロー通知システムの電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-256">Verify workflow notification system email templates:</span></span>

    1. <span data-ttu-id="1d5b0-257">**システム管理** \> **設定** \> **電子メール** \> **システムの電子メール テンプレート** (システム全体のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-257">Go to **System administration** \> **Setup** \> **Email** \> **System email templates** (for system-wide templates).</span></span>
    2. <span data-ttu-id="1d5b0-258">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-258">Verify that the **Sender email** field is set and valid.</span></span>

4. <span data-ttu-id="1d5b0-259">ワークフロー通知組織の電子メール テンプレートを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-259">Verify workflow notification organization email templates:</span></span>

    1. <span data-ttu-id="1d5b0-260">**組織管理** \> **設定** \> **組織の電子メール テンプレート** (組織固有のテンプレート) の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-260">Go to **Organization administration** \> **Setup** \> **Organization email templates** (for organization-specific templates).</span></span>
    2. <span data-ttu-id="1d5b0-261">**送信者電子メール** フィールドが設定済みで有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-261">Verify that the **Sender email** field is set and valid.</span></span>

5. <span data-ttu-id="1d5b0-262">ユーザーが電子メール通知を受信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-262">Verify that the user can receive email notifications:</span></span>

    1. <span data-ttu-id="1d5b0-263">**設定** \> **ユーザー オプション** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-263">Go to **Settings** \> **User options**.</span></span>
    2. <span data-ttu-id="1d5b0-264">**勘定** タブに移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-264">Go to the **Account** tab.</span></span>

       1. <span data-ttu-id="1d5b0-265">**メール プロバイダー ID** (SMTP など) を設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-265">Set the **Email provider ID** (for example, SMTP).</span></span>
       2. <span data-ttu-id="1d5b0-266">また、既定の **送信元** アドレスが現在のユーザーに対して使用されていない場合は、**送信者電子メール** の上書きを設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-266">Optionally, set a **Sender email** override if the default **send from** address should not be used for the current user.</span></span>

    3. <span data-ttu-id="1d5b0-267">**ワークフロー** タブに移動します。電子メールで通知を送信するオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-267">Navigate to the **Workflow** tab. Set the option to send notifications in email to **Yes**.</span></span>

6. <span data-ttu-id="1d5b0-268">ワークフロー システムが電子メール通知を送信することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-268">Verify that the workflow system will send email notifications:</span></span>

    <span data-ttu-id="1d5b0-269">通知する必要があるワークフローごとに、ワークフロー エディターでワークフロー プロパティを開きます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-269">For each workflow that should have a notification, open the workflow properties in the workflow editor.</span></span>

    1. <span data-ttu-id="1d5b0-270">**基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-270">Click **Basic settings**.</span></span> <span data-ttu-id="1d5b0-271">ワークフロー通知の電子メール テンプレートを調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-271">Adjust the email template for the workflow notifications.</span></span>
    2. <span data-ttu-id="1d5b0-272">**通知** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-272">Click **Notifications**.</span></span>

        1. <span data-ttu-id="1d5b0-273">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-273">Enable the events for which a user should be notified.</span></span>
        2. <span data-ttu-id="1d5b0-274">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-274">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

    3. <span data-ttu-id="1d5b0-275">ユーザーに通知される必要のあるワークフロー承認要素:</span><span class="sxs-lookup"><span data-stu-id="1d5b0-275">On a workflow approval element for which a user should be notified:</span></span>

        1. <span data-ttu-id="1d5b0-276">**プロパティ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-276">Go to **Properties**.</span></span>
        2. <span data-ttu-id="1d5b0-277">ユーザーに通知するべきイベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-277">Enable the events for which a user should be notified.</span></span>
        3. <span data-ttu-id="1d5b0-278">有効なイベント通知ごとにワークフロー通知の受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-278">Set the recipient of the workflow notification for each event notification that is enabled.</span></span>

### <a name="workflow-email-notification-testing"></a><span data-ttu-id="1d5b0-279">ワークフロー電子メール通知のテスト</span><span class="sxs-lookup"><span data-stu-id="1d5b0-279">Workflow email notification testing</span></span>

<span data-ttu-id="1d5b0-280">電子メール通知のテストでは、単に通知をトリガーし、それを確認するだけです。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-280">The testing for email notifications is to simply trigger the notification and then check for it.</span></span>

1. <span data-ttu-id="1d5b0-281">電子メール通知に対して設定されているワークフローを送信します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-281">Submit a workflow that has been set up for email notifications.</span></span>
2. <span data-ttu-id="1d5b0-282">ワークフロー履歴をチェックして、ワークフロー作業項目が予定されたユーザーに割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-282">Check the workflow history to make sure that a workflow work item was assigned to the expected user.</span></span>
3. <span data-ttu-id="1d5b0-283">**システム管理** \> **定期タスク** \> **メール処理** \> **バッチメール送信ステータス** で、保留になっておりメール通知のステータスを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-283">Check the status of the pending email notification in **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch email sending status**.</span></span>

    <span data-ttu-id="1d5b0-284">電子メールが送信に失敗した場合は、SMTP メール アカウントを開くことができることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-284">If the email is fails to send, make sure that the SMTP mail account can be opened.</span></span>

4. <span data-ttu-id="1d5b0-285">適切な受信トレイで電子メール通知を確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-285">Check for the email notification in the appropriate inbox.</span></span>

## <a name="exchange-mail-provider"></a><span data-ttu-id="1d5b0-286">Exchange メール プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1d5b0-286">Exchange mail provider</span></span>

<span data-ttu-id="1d5b0-287">**電子メール パラメーター** ページで管理者は対話型の電子メール プロバイダーおよびバッチ電子メール プロバイダーとして **Exchange** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-287">The **Email parameters** page allows an administrator to select **Exchange** as an interactive email provider and as the Batch email provider.</span></span> <span data-ttu-id="1d5b0-288">**Exchange** メール プロバイダーは、現在のユーザーの Exchange Online アカウントを使用して電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-288">The **Exchange** mail provider will use the current user's Exchange Online account to send emails.</span></span> <span data-ttu-id="1d5b0-289">バッチ電子メール プロバイダーとして使用された場合は、バッチ アカウントが使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-289">When used as the Batch email provider, the batch account will be used.</span></span> <span data-ttu-id="1d5b0-290">追加のコンフィギュレーションは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-290">No additional configuration is needed.</span></span> <span data-ttu-id="1d5b0-291">トラブルシューティングが必要な場合は、現在のユーザーのアカウントにサインインできることと、そのアカウントから目的の受信者に電子メールを送信できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-291">If troubleshooting is needed, ensure that it’s possible to sign in to the current user's account and that emails can be sent from that account to the intended recipients.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1d5b0-292">Exchange メール プロバイダーは、外部ユーザーにはサポートされていません。これらのユーザーは、そのテナントで Exchange アカウントを持っていないためです</span><span class="sxs-lookup"><span data-stu-id="1d5b0-292">The Exchange mail provider is not supported for external users, as those users will not have Exchange accounts on that tenant</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="1d5b0-293">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1d5b0-293">Troubleshooting</span></span>

### <a name="common-issues-with-sending-email"></a><span data-ttu-id="1d5b0-294">電子メール送信に関する一般的な問題</span><span class="sxs-lookup"><span data-stu-id="1d5b0-294">Common issues with sending email</span></span>

<span data-ttu-id="1d5b0-295">メール設定のトラブルシューティングに役立つ標準プロセスがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-295">There are a few standard processes that can help you troubleshoot the configuration of email settings.</span></span> 

#### <a name="verify-email-settings-and-send-a-test-email"></a><span data-ttu-id="1d5b0-296">電子メール設定の確認とテスト電子メールの送信</span><span class="sxs-lookup"><span data-stu-id="1d5b0-296">Verify email settings and send a test email</span></span>

1. <span data-ttu-id="1d5b0-297">**システム管理** \> **設定** \> **電子メール** \> **電子メール パラメータ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-297">Go to **System administration** \> **Setup** \> **Email** \> **Email parameters**.</span></span>
2. <span data-ttu-id="1d5b0-298">SMTP が有効であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-298">Verify that SMTP is enabled.</span></span>
3. <span data-ttu-id="1d5b0-299">SMTP メール サーバーの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-299">Verify the settings of the SMTP mail server.</span></span>
4. <span data-ttu-id="1d5b0-300">アカウントとパスワードが正確であるかことを確認するために、別のウィンドウで SMTP アカウントにログインします。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-300">Sign in to the SMTP account in a separate window to make sure that the account and password are correct.</span></span>
5. <span data-ttu-id="1d5b0-301">**システム管理** \> **設定** \> **電子メール** \> **電子メールのパラメータ** \> **テスト電子メール** を使用してテスト電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-301">Send a test email using **System administration** \> **Setup** \> **Email** \> **Email parameters** \> **Test email**.</span></span>

#### <a name="verify-that-the-email-batch-process-is-running"></a><span data-ttu-id="1d5b0-302">電子メールのバッチ処理が実行されていることを確認</span><span class="sxs-lookup"><span data-stu-id="1d5b0-302">Verify that the email batch process is running</span></span>

1. <span data-ttu-id="1d5b0-303">**システム管理** \> **定期処理のタスク** \> **電子メールの処理** \> **バッチ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-303">Go to **System administration** \> **Periodic tasks** \> **Email processing** \> **Batch**.</span></span>
2. <span data-ttu-id="1d5b0-304">**バッチ処理** オプションが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-304">Make sure that the **Batch processing** option is set to **Yes**.</span></span>
3. <span data-ttu-id="1d5b0-305">電子メール プロセスの再実行を調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-305">Review the recurrence of the email process:</span></span>
    1. <span data-ttu-id="1d5b0-306">**終了日なし** を選択し、メール バッチ処理のすべての反復を調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-306">Select **No end date** to adjust all recurrences of the email batch process.</span></span>
    2. <span data-ttu-id="1d5b0-307">必要に応じて回数を調整します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-307">Adjust the count as needed.</span></span>

#### <a name="review-the-status-of-batch-emails"></a><span data-ttu-id="1d5b0-308">バッチ電子メールの状態の確認</span><span class="sxs-lookup"><span data-stu-id="1d5b0-308">Review the status of batch emails</span></span>

1.  <span data-ttu-id="1d5b0-309">**システム管理** > **定期処理のタスク** > **電子メールの処理** > **バッチ電子メール送信状態** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-309">Go to **System administration** > **Periodic tasks** > **Email processing** > **Batch email sending status**.</span></span>
2. <span data-ttu-id="1d5b0-310">電子メールが正しいアカウントから送信されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-310">Verify that emails are being sent from the correct account.</span></span> 
    -  <span data-ttu-id="1d5b0-311">アカウントが正しくない場合、必要に応じてユーザー オプション、システム テンプレート、組織テンプレートなどの設定を調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-311">If the account is incorrect, you need to adjust settings such as user options, system templates, or organization templates, as needed.</span></span>
3. <span data-ttu-id="1d5b0-312">すべての電子メール ユーザー アカウントに、構成された SMTP アカウントに対して **送信** のアクセス許可が付与されていることを確認します (**すべての電子メール アカウントに適切なアクセス許可があることを確認する** のセクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-312">Verify that all email user accounts have been granted permission to **Send As** for the configured SMTP account (see the section titled **Verify all email accounts have appropriate permissions**).</span></span>
    
#### <a name="review-any-errors-on-the-email-history-page"></a><span data-ttu-id="1d5b0-313">**メールの履歴** ページでエラーを確認する</span><span class="sxs-lookup"><span data-stu-id="1d5b0-313">Review any errors on the **Email history** page</span></span>

1.  <span data-ttu-id="1d5b0-314">**システム管理** /> **設定** /> **電子メール** /> **電子メール履歴** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-314">Go to **System administration** /> **Setup** /> **Email** /> **Email history**.</span></span> 
    -  <span data-ttu-id="1d5b0-315">このページでは、送信を防ぐことができたかもしれないメールのエラーなど、管理者がすべての送信済みメールを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-315">This page allows administrators to review all sent emails, including any errors that might have prevented an email from being sent.</span></span> <span data-ttu-id="1d5b0-316">**メール履歴** ページは、対話と、非対話 / バッチメールを表示します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-316">The **Email history** page will show interactive as well as non-interactive/batch emails.</span></span> 
2.  <span data-ttu-id="1d5b0-317">**メール ステータス** が **エラー** となっているメールに対しては、**エラー詳細** タブでエラー メッセージをレビューして、必要な処置を取るべきかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-317">For any emails with an **Email status** of **Failed**, review the error message on the **Failure details** tab and determine if corrective actions should be taken.</span></span> <span data-ttu-id="1d5b0-318">これらのエラーについては、このトピックで後ほど詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-318">Some pf these errors are covered later in this topic.</span></span>  

#### <a name="verify-all-email-accounts-have-appropriate-send-as-permissions"></a><span data-ttu-id="1d5b0-319">すべての電子メール アカウントに適切な送信アクセス許可があることを確認する</span><span class="sxs-lookup"><span data-stu-id="1d5b0-319">Verify all email accounts have appropriate Send as permissions</span></span>
<span data-ttu-id="1d5b0-320">Microsoft 365 管理センターで、電子メールの送信に使用されるすべてのユーザー メール アカウントに、構成された SMTP アカウントに対する **送信者** と **代理送信** アクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-320">In the Microsoft 365 admin center, verify that all user mail accounts that will be used to send emails have **Send As** and **Send On Behalf Of** permissions for the configured SMTP account.</span></span> <span data-ttu-id="1d5b0-321">詳細については、[Microsoft 365 の別のユーザーにメールボックスのアクセス許可を与える](/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user?view=o365-worldwide) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-321">For more information, see [Give mailbox permissions to another user in Microsoft 365](/microsoft-365/admin/add-users/give-mailbox-permissions-to-another-user?view=o365-worldwide).</span></span>

#### <a name="verify-user-mailboxes"></a><span data-ttu-id="1d5b0-322">ユーザー メールボックスを確認</span><span class="sxs-lookup"><span data-stu-id="1d5b0-322">Verify user mailboxes</span></span>
<span data-ttu-id="1d5b0-323">影響を受ける (またはすべての) ユーザー メールボックスにサインインして、それらが有効であり、サインインを使用してアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-323">Consider signing in to the affected (or all) user mailboxes to verify that they are valid and can be accessed using sign in.</span></span>

### <a name="specific-smtp-email-issues"></a><span data-ttu-id="1d5b0-324">特定の SMTP 電子メールの問題</span><span class="sxs-lookup"><span data-stu-id="1d5b0-324">Specific SMTP email issues</span></span> 

<span data-ttu-id="1d5b0-325">電子メールが SMTP を介して送信されたときに引き続き問題が発生する場合は、以下の特定のエラーのいずれかが発生している可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-325">If you continue to experience issues when email is sent via SMTP, you may be running into one of the specific errors below.</span></span> <span data-ttu-id="1d5b0-326">そうでない場合は、[SMTPer.net](https://www.smtper.net/) などのツールに SMTP アカウント情報を入力して、SMTP サーバーとアカウントが有効で正しく機能していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-326">If not, consider entering the SMTP account information in a tool such as [SMTPer.net](https://www.smtper.net/) to verify that the SMTP server and account are valid and working correctly.</span></span>

### <a name="smtp-emails-fail-to-send-with-if-your-smtp-server-doesnt-support-authentication-please-clear-the-smtp-user-name-and-password"></a><span data-ttu-id="1d5b0-327">SMTP メールは、「SMTP サーバーが認証をサポートしていない場合は、SMTP ユーザー名とパスワードをクリアしてください」と送信できません</span><span class="sxs-lookup"><span data-stu-id="1d5b0-327">SMTP emails fail to send with "If your SMTP server doesn't support authentication, please clear the SMTP user name and password"</span></span>

<span data-ttu-id="1d5b0-328">**問題:** バージョン 10.0.19/Platform update 39 以降に移行すると、SMTP メールの送信に失敗し、「SMTP サーバーが認証をサポートしていない場合は、SMTP ユーザー名とパスワードをクリアしてください」というメッセージが添付されます</span><span class="sxs-lookup"><span data-stu-id="1d5b0-328">**Issue:** After moving to version 10.0.19/Platform update 39 or later, SMTP emails may fail to send and are accompanied by the following message: "If your SMTP server doesn't support authentication, please clear the SMTP user name and password"</span></span>

<span data-ttu-id="1d5b0-329">**説明:** これは、Microsoft の推奨事項に従って .NET SMTP メール クライアント (現在は廃止されています) から MailKit への移行に関連しています。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-329">**Explanation:** This is related to a migration from the .NET SMTP mail client (which is now obsolete) to MailKit per Microsoft recommendations.</span></span> <span data-ttu-id="1d5b0-330">この移行の結果、メール サーバーが認証をサポートしていなかった場合の SMTP ユーザー名とパスワードの処理に関する動作が変更されました。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-330">A result of this migration is a change in behavior regarding the handling of SMTP user name and password in situations where the mail server didn't support authentication.</span></span> <span data-ttu-id="1d5b0-331">以前は、SMTP ユーザー名が提供されましたが、サーバーが認証をサポートしていなかった場合、.NET SMTP メール クライアントは提供されたユーザー名とパスワードを無視し、認証なしで続行していました。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-331">Previously, if a SMTP user name was provided but the server didn't support authentication, the .NET SMTP mail client would ignore the provided user name and password and continue without authentication.</span></span> <span data-ttu-id="1d5b0-332">この動作により、顧客は認証されたメール サーバーを使用しているという誤った考えに陥る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-332">This behavior may have lead customers to the false belief they were using an authenticated mail server.</span></span> <span data-ttu-id="1d5b0-333">MailKit では、ユーザー名が提供されている場合、認証が必要です。これにより、認証をサポートしていないメール サーバーでエラーが発生し、電子メールの送信が失敗します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-333">With MailKit, if a user name is provided, authentication is required, which will trigger an error for mail servers that don't support authentication and will cause emails to fail to send.</span></span> 

<span data-ttu-id="1d5b0-334">**修正:** ユーザーは **電子メール パラメーター** ページ (**システム管理 > 設定 > 電子メール** の下部) に移動し、**SMTP 設定** タブ ページで **ユーザー名** および **パスワード** フィールドをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-334">**Fix:** The user needs to go to the **Email parameters** page (under **System administration > Setup > Email**), and clear the **User name** and **Password** fields on the **SMTP settings** tab page.</span></span>

### <a name="smtp-emails-fail-to-send-with-5757-smtp-error-or-an-indication-that-youre-not-authenticated-or-authentication-is-required"></a><span data-ttu-id="1d5b0-335">SMTP メールは、「5.7.57 SMTP」エラーが送信されないか、認証されていない、または認証が必要というメッセージが表示される</span><span class="sxs-lookup"><span data-stu-id="1d5b0-335">SMTP emails fail to send with "5.7.57 SMTP" error or an indication that you're not authenticated or authentication is required</span></span>

<span data-ttu-id="1d5b0-336">**問題:** SMTP を介して送信された電子メールは、次のいずれかの理由で送信できません。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-336">**Issue:** Emails sent via SMTP fail to send for one of the following reasons:</span></span> 
-  <span data-ttu-id="1d5b0-337">「5.5.57 SMTP」例外</span><span class="sxs-lookup"><span data-stu-id="1d5b0-337">An "5.5.57 SMTP" exception</span></span>
-  <span data-ttu-id="1d5b0-338">ユーザーが認証されていません</span><span class="sxs-lookup"><span data-stu-id="1d5b0-338">The user is not authenticated</span></span>
-  <span data-ttu-id="1d5b0-339">ユーザー認証が必要です</span><span class="sxs-lookup"><span data-stu-id="1d5b0-339">User authentication is required</span></span> 

<span data-ttu-id="1d5b0-340">**説明:** メール サーバーが、SMTP ユーザーの資格情報が無効であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-340">**Explanation:** The mail server is indicating that the SMTP user credentials are invalid.</span></span>   

<span data-ttu-id="1d5b0-341">**修正:** SMTP ユーザーの資格情報が正しいか確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-341">**Fix:** Verify that the SMTP user credentials are correct.</span></span>  

### <a name="smtp-emails-fail-to-send-with-microsoftdynamicsaxxppsecuritycryptoencryptionexception-encryption-error-occurred-with-exception"></a><span data-ttu-id="1d5b0-342">SMTP メールは「Microsoft.Dynamics.Ax.Xpp.Security.CryptoEncryptionException: 暗号化エラーが例外で発生しました」で送信に失敗します</span><span class="sxs-lookup"><span data-stu-id="1d5b0-342">SMTP emails fail to send with "Microsoft.Dynamics.Ax.Xpp.Security.CryptoEncryptionException: Encryption error occurred with exception"</span></span>

<span data-ttu-id="1d5b0-343">**問題:** SMTP を介して送信された電子メールが送信に失敗し、次の例外をトリガーします: 「Microsoft.Dynamics.Ax.Xpp.Security.CryptoEncryptionException: 暗号化エラーが例外で発生しました」</span><span class="sxs-lookup"><span data-stu-id="1d5b0-343">**Issue:** Emails sent via SMTP fail to send and trigger the following exception: "Microsoft.Dynamics.Ax.Xpp.Security.CryptoEncryptionException: Encryption error occurred with exception"</span></span>

<span data-ttu-id="1d5b0-344">**説明:** SMTP パスワードは、単一の環境に固有のキーを使用して暗号化されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-344">**Explanation:** The SMTP password is encrypted using a key specific to a single environment.</span></span>  <span data-ttu-id="1d5b0-345">このエラーは通常、環境間でデータベースを移行した後でパスワードを復号化できない場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-345">This error typically surfaces when the password can no longer be decrypted after a database migration between environments.</span></span>

<span data-ttu-id="1d5b0-346">**修正:** **電子メール パラメーター** ページの [SMTP 設定タブ](#smtp-settings-tab) で SMTP パスワードをクリアして再入力します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-346">**Fix:** Clear and reenter the SMTP password on the [SMTP settings tab](#smtp-settings-tab) on the **Email parameters** page.</span></span> 

### <a name="smtp-emails-fail-to-send-with-client-does-not-have-permissions-to-send-as-this-sender"></a><span data-ttu-id="1d5b0-347">SMTP メールは「クライアントにこの送信者として送信するアクセス許可がありません」と送信できません</span><span class="sxs-lookup"><span data-stu-id="1d5b0-347">SMTP emails fail to send with "Client does not have permissions to send as this sender"</span></span>

<span data-ttu-id="1d5b0-348">**問題:** SMTP を使用してメールを送信すると、「クライアントにこの送信者として送信するアクセス許可がありません」というエラーで送信に失敗する場合があります。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-348">**Issue:** When sending email using SMTP, some emails may fail to send with the following error: "Client does not have permissions to send as this sender."</span></span>  

<span data-ttu-id="1d5b0-349">**説明:** この問題は、通常、電子メール アカウントの **送信者** アクセス許可が正しく設定されていないために発生します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-349">**Explanation:** This issue is usually caused by incorrect setup of the **Send As** permissions for the email account.</span></span> 

<span data-ttu-id="1d5b0-350">**修正:** 電子メール アカウントに適切な **送信者** アクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-350">**Fix:** Ensure there are appropriate **Send As** permissions for the email account.</span></span> <span data-ttu-id="1d5b0-351">詳細については、[すべての電子メール アカウントに適切な送信アクセス許可があることを確認する](#verify-all-email-accounts-have-appropriate-send-as-permissions) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-351">For details, see [Verify all email accounts have appropriate Send as permissions](#verify-all-email-accounts-have-appropriate-send-as-permissions).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="1d5b0-352">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="1d5b0-352">Frequently asked questions</span></span>

### <a name="where-do-workflow-email-templates-come-from"></a><span data-ttu-id="1d5b0-353">ワークフロー電子メール テンプレートはどこから取得されますか。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-353">Where do workflow email templates come from?</span></span>

<span data-ttu-id="1d5b0-354">ワークフローがシステムレベル (会社固有ではない) または組織レベル (会社固有) のワークフローのいずれであるかによって、電子メール テンプレートは、システム電子メール テンプレートまたは組織の電子メール テンプレートから取得されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-354">The email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>

### <a name="what-email-limits-apply-when-using-exchange-or-smtp"></a><span data-ttu-id="1d5b0-355">Exchange または SMTP を使用する場合、どのような電子メール制限が適用されますか?</span><span class="sxs-lookup"><span data-stu-id="1d5b0-355">What email limits apply when using Exchange or SMTP?</span></span>  

<span data-ttu-id="1d5b0-356">システムは Exchange や一般的な電子メール クライアントのような SMTP サーバーと通信するため、標準の動作と制限が適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-356">The system communicates with Exchange or an SMTP server like a typical email client, so standard behavior and limits apply.</span></span> <span data-ttu-id="1d5b0-357">たとえば、標準の [Exchange Online 送受信制限](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)が適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d5b0-357">For example, standard [Exchange Online receiving and sending limits](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits) apply.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="1d5b0-358">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1d5b0-358">Additional resources</span></span>

[<span data-ttu-id="1d5b0-359">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="1d5b0-359">Troubleshoot the Office integration</span></span>](../../dev-itpro/office-integration/office-integration-troubleshooting.md)

[<span data-ttu-id="1d5b0-360">Office 統合のチュートリアル</span><span class="sxs-lookup"><span data-stu-id="1d5b0-360">Office integration tutorial</span></span>](../../dev-itpro/office-integration/office-integration-tutorial.md)

<span data-ttu-id="1d5b0-361">[Microsoft Dynamics AX での電子メール機能のコンフィギュレーション [AX 2012]](/dynamicsax-2012/appuser-itpro/configure-email-functionality-in-microsoft-dynamics-ax)</span><span class="sxs-lookup"><span data-stu-id="1d5b0-361">[Configure email functionality in Microsoft Dynamics AX [AX 2012]](/dynamicsax-2012/appuser-itpro/configure-email-functionality-in-microsoft-dynamics-ax)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
