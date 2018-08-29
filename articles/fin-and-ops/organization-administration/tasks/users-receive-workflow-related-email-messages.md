--- 
title: "ユーザーにワークフロー関連の電子メールを送信するシステムを構成する"
description: "ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。"
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="a154a-103">ユーザーにワークフロー関連の電子メールを送信するシステムを構成する</span><span class="sxs-lookup"><span data-stu-id="a154a-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a154a-104">ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="a154a-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="a154a-105">たとえば、ドキュメントが承認のためにユーザーに割り当てられたとき、電子メール メッセージをユーザーに送信できます。</span><span class="sxs-lookup"><span data-stu-id="a154a-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="a154a-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="a154a-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a154a-107">[システム管理] > [ユーザー] > [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a154a-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="a154a-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a154a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a154a-109">[ユーザー オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a154a-109">Click User options.</span></span>
4. <span data-ttu-id="a154a-110">[ワークフロー] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a154a-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="a154a-111">通知セクションが展開されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a154a-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="a154a-112">通知セクションで、ワークフロー関連イベントについてユーザーに通知する方法を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="a154a-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="a154a-113">[行項目ワークフロー通知タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="a154a-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="a154a-114">グループ化 – 複数の行項目の通知が、1 つの電子メール メッセージにまとめられます。</span><span class="sxs-lookup"><span data-stu-id="a154a-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="a154a-115">個別 – 電子メール メッセージが各行項目のために送信されます。</span><span class="sxs-lookup"><span data-stu-id="a154a-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="a154a-116">ユーザーがクライアントで通知を受信する場合は、[通知を電子メールで送信] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a154a-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="a154a-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a154a-117">Click Save.</span></span>
7. <span data-ttu-id="a154a-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a154a-118">Close the page.</span></span>


