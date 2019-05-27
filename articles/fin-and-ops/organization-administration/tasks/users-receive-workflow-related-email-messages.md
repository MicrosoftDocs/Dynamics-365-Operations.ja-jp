---
title: ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする
description: ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560501"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="bfaa4-103">ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする</span><span class="sxs-lookup"><span data-stu-id="bfaa4-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bfaa4-104">ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="bfaa4-105">たとえば、ドキュメントが承認のためにユーザーに割り当てられたとき、電子メール メッセージをユーザーに送信できます。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="bfaa4-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="bfaa4-107">[システム管理] > [ユーザー] > [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="bfaa4-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bfaa4-109">[ユーザー オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-109">Click User options.</span></span>
4. <span data-ttu-id="bfaa4-110">[ワークフロー] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="bfaa4-111">通知セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="bfaa4-112">通知セクションで、ワークフロー関連イベントについてユーザーに通知する方法を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="bfaa4-113">[行項目ワークフロー通知タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="bfaa4-114">グループ化 – 複数の行項目の通知が、1 つの電子メール メッセージにまとめられます。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="bfaa4-115">個別 – 電子メール メッセージが各行項目のために送信されます。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="bfaa4-116">ユーザーがクライアントで通知を受信する場合は、[通知を電子メールで送信] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="bfaa4-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-117">Click Save.</span></span>
7. <span data-ttu-id="bfaa4-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bfaa4-118">Close the page.</span></span>

