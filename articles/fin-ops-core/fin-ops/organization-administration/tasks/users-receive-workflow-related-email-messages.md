---
title: ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする
description: ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a81e01c36081ce7131ee65344f583755fa3bfd3
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564193"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="c3a3c-103">ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする</span><span class="sxs-lookup"><span data-stu-id="c3a3c-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3a3c-104">ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="c3a3c-105">たとえば、ドキュメントが承認のためにユーザーに割り当てられたとき、電子メール メッセージをユーザーに送信できます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="c3a3c-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c3a3c-107">**ナビゲーション ウィンドウ > モジュール > システム管理 > ユーザー > ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="c3a3c-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c3a3c-109">**アクション ウィンドウ** で、**ユーザー オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="c3a3c-110">**ワークフロー** タブをクリックします。**通知** セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="c3a3c-111">**通知** セクションで、ワークフローに関連するイベントについてユーザーに通知する方法を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="c3a3c-112">**行項目ワークフロー通知タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="c3a3c-113">グループ化 – 複数の行項目の通知が、1 つの電子メール メッセージにまとめられます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="c3a3c-114">個別 – 電子メール メッセージが各行項目のために送信されます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="c3a3c-115">ユーザーがクライアントで通知を受信する場合は、**通知を電子メールで送信** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="c3a3c-116">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-116">Click **Save**.</span></span>
7. <span data-ttu-id="c3a3c-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="c3a3c-118">ワークフローがシステムレベル (会社固有ではない) または組織レベル (会社固有) のワークフローのいずれであるかによって、ワークフローの電子メール テンプレートは、システム電子メール テンプレートまたは組織の電子メール テンプレートから取得されます。</span><span class="sxs-lookup"><span data-stu-id="c3a3c-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]