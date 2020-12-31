---
title: メッセージング API - アクション センター、メッセージ バー、メッセージ詳細
description: このトピックでは、メッセージング システムについて説明します。
author: jasongre
manager: AnnBe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 64153
ms.assetid: b69ec992-9bde-469e-99bb-773feb9489ff
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5217b03373a8ee7150de31301fc8e3c695499d86
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683949"
---
# <a name="messaging-apis---action-center-message-bar-and-message-details"></a><span data-ttu-id="00e47-103">メッセージング API - アクション センター、メッセージ バー、メッセージ詳細</span><span class="sxs-lookup"><span data-stu-id="00e47-103">Messaging APIs - Action center, message bar, and message details</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="00e47-104">このトピックでは、Finance and Operations アプリのメッセージング システムについて、特にメッセージを作成してエンド ユーザーにルーティングするために使用されるアプリケーション プログラミング インターフェイス (API) の観点から、説明します。</span><span class="sxs-lookup"><span data-stu-id="00e47-104">This topic describes the messaging system in Finance and Operations apps, specifically in terms of the application programming interfaces (APIs) that are used to create and route messages to end users.</span></span>  

## <a name="introduction"></a><span data-ttu-id="00e47-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="00e47-105">Introduction</span></span>

<span data-ttu-id="00e47-106">このエクスペリエンスを改善するために、Finance and Operations アプリ用に新しいメッセージング システムが作成されました。</span><span class="sxs-lookup"><span data-stu-id="00e47-106">A new messaging system was created for Finance and Operations apps to improve this experience.</span></span> <span data-ttu-id="00e47-107">以前のバージョンと比較すると、Finance and Operations アプリのメッセージング システムには次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="00e47-107">Compared to earlier versions, the messaging system for Finance and Operations apps includes the following features:</span></span>

+ <span data-ttu-id="00e47-108">コンテキストのあるメッセージの関連性が強化されました (フォームとグローバル)。</span><span class="sxs-lookup"><span data-stu-id="00e47-108">Improved association of a message with its context (form versus global).</span></span>
+ <span data-ttu-id="00e47-109">中断のレベル (なし、軽微、および中断) を強化しました。</span><span class="sxs-lookup"><span data-stu-id="00e47-109">Improved level of interruption (none, subtle, and interrupting).</span></span>
+ <span data-ttu-id="00e47-110">メッセージの種類間での明確さと、その用途が強化されました。</span><span class="sxs-lookup"><span data-stu-id="00e47-110">Improved clarity between types of messages and their use.</span></span>
+ <span data-ttu-id="00e47-111">メッセージを表示するために使用されるコントロールは、フォーム コンテキストに基づいて deterministic です。</span><span class="sxs-lookup"><span data-stu-id="00e47-111">The control that is used to display messages is deterministic and based on form context.</span></span>

## <a name="backwards-compatibility-of-info-warningcheckfailed-and-error"></a><span data-ttu-id="00e47-112">Info()、warning()/checkfailed()、error() の下位互換性</span><span class="sxs-lookup"><span data-stu-id="00e47-112">Backwards compatibility of info(), warning()/checkfailed(), and error()</span></span> 
<span data-ttu-id="00e47-113">以前のバージョンの Finance and Operations アプリからの **info()**、**warning()**、**error()** のアプリケーション プログラミング インターフェイス (API) は、引き続きサポートされますが、これらのAPIは現在、フレームワークの新しいメッセージング システム上にあります。</span><span class="sxs-lookup"><span data-stu-id="00e47-113">The **info()**, **warning()**, and **error()** application programming interfaces (APIs) from earlier versions of Finance and Operations apps are still supported; however, these APIs now sit upon the framework's new messaging system.</span></span> <span data-ttu-id="00e47-114">API呼び出しのコンテキストを使用して、ユーザーにメッセージを提示する最適な方法を決定することにより、メッセージは確定的にメッセージまたはアクション センター (中断しない方法で) にルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="00e47-114">Messages are routed deterministically to the message or Action center (in a non-interrupting manner) by using the context of the API call to determine the best way to present the message to the user.</span></span> <span data-ttu-id="00e47-115">一般に、API の使用がフォームから生成された場合、そのメッセージが同じフォーム上のメッセージ バーで表示されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-115">In general, if the use of the API originated from a form, the message appears in a message bar on that same form.</span></span> <span data-ttu-id="00e47-116">(ドロップ ダイアログとスライダ ダイアログは、どちらもフォームと見なされます。)</span><span class="sxs-lookup"><span data-stu-id="00e47-116">(Drop dialogs and slider dialogs are both considered forms.)</span></span> 

<span data-ttu-id="00e47-117">次の図は、ページ アクションに対応する **情報**、**警告**/**checkfailed**、**エラー** メッセージ バー、または **info()**、**warning()**、**error()** からの同期作成メッセージを示しています。</span><span class="sxs-lookup"><span data-stu-id="00e47-117">The following illustration shows **info**, **warning**/**checkfailed**, and **error** message bars that correspond to page actions, or synchronous-authored messages that come from **info()**, **warning()**, and **error()**.</span></span> 

<span data-ttu-id="00e47-118">[![情報、警告/checkfailed、エラー メッセージを示すスクリーン ショット](./media/cli-legacyMessages.png)](./media/cli-legacyMessages.png)</span><span class="sxs-lookup"><span data-stu-id="00e47-118">[![Screenshot showing info, warning/checkfailed, and error messages](./media/cli-legacyMessages.png)](./media/cli-legacyMessages.png)</span></span>

> [!NOTE]
> <span data-ttu-id="00e47-119">スライダー ダイアログからこれらの API が呼び出されても、メッセージが表示される前にそのスライダー ダイアログが閉じられると、メッセージはスライダー ダイアログの親ページのメッセージ バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-119">If these APIs are called from a slider dialog, but that slider dialog is closed before the message appears, the message is shown in a message bar on the slider dialog's parent page.</span></span> <span data-ttu-id="00e47-120">メッセージが表示される前にそのスライダー ダイアログ ボックスが閉じられ、親ページが存在しない場合、メッセージは、アクション センターにルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="00e47-120">If that slider dialog is closed before the message appears, and there is no parent page, the message is routed to the Action center.</span></span> <span data-ttu-id="00e47-121">メッセージング API は必ずメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="00e47-121">The messaging API never fails to show a message.</span></span> <span data-ttu-id="00e47-122">適切なホスト ページが見つからない場合は、メッセージがアクション センターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-122">If an appropriate host page isn't found, the message is sent to the Action center.</span></span>

<span data-ttu-id="00e47-123">**info()**、**warning()**/**checkfailed()**、または **error()** が非同期プロセス (たとえば、バッチ) から呼び出された場合、考慮するフォーム コンテキストはなく、メッセージはアクション センターに送信されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-123">If **info()**, **warning()**/**checkfailed()**, or **error()** is called from an asynchronous process (for example, a batch), there is no form context to consider, and the messages are sent to the Action center.</span></span> <span data-ttu-id="00e47-124">(アクション センターを開くには、ナビゲーションバーの **メッセージを表示** ボタンをクリックします。) 次の図は、アクション センターの各種メッセージの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="00e47-124">(To open the Action center, click the **Show messages** button on the navigation bar.) The following illustration shows examples of each type of message in the Action center.</span></span> 

<span data-ttu-id="00e47-125">[![アクション センターのメッセージ](./media/2_api.png)](./media/2_api.png)</span><span class="sxs-lookup"><span data-stu-id="00e47-125">[![Messages the in Action center](./media/2_api.png)](./media/2_api.png)</span></span>

> [!NOTE]
> <span data-ttu-id="00e47-126">**Box()** API を使用して、ユーザーに中断エラーを表します。</span><span class="sxs-lookup"><span data-stu-id="00e47-126">Use the **Box()** API to express an interrupting error to the user.</span></span>                                                               

## <a name="backwards-compatibility-of-setprefix"></a><span data-ttu-id="00e47-127">SetPrefix() の下位互換性</span><span class="sxs-lookup"><span data-stu-id="00e47-127">Backwards compatibility of SetPrefix()</span></span> 
<span data-ttu-id="00e47-128">Finance and Operations アプリは、下位互換性のために **SetPrefix()** API もサポートしています。</span><span class="sxs-lookup"><span data-stu-id="00e47-128">Finance and Operations apps also support the **SetPrefix()** API for backwards compatibility.</span></span> <span data-ttu-id="00e47-129">ただし、メッセージング システムでは、**SetPrefix()** の結果は、積極的にユーザーを中断しません; 代わりに、結果が (以前のバージョンと同様に) 収集および保存され、メッセージ バーまたはアクション センターの通知がユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-129">However, in the messaging system, the results of **SetPrefix()** don't actively interrupt the user; instead, the results are collected and stored (as in previous versions), and a message bar or Action center notification is presented to the user.</span></span> <span data-ttu-id="00e47-130">この通知は、関連するタスクが完了し、ユーザーが確認する必要のあるメッセージがある可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="00e47-130">This notification indicates that the related task has been completed, and that it might have messages that the user should review.</span></span> <span data-ttu-id="00e47-131">「結果の通知」メッセージは、実際にはタスクによる **SetPrefix()** の最初の呼び出しを使ってメッセージをフレーム化します。</span><span class="sxs-lookup"><span data-stu-id="00e47-131">The "Notification of results" message actually uses the task's first call to **SetPrefix()** to frame the message.</span></span> <span data-ttu-id="00e47-132">この動作は、最初の呼び出しが結果の「タイトル」であった以前のバージョンの動作に類似しています。</span><span class="sxs-lookup"><span data-stu-id="00e47-132">This behavior is similar to the behavior in previous versions, where the first call was the "title" of the results.</span></span> <span data-ttu-id="00e47-133">この例では、「転記の結果」が **SetPrefix()** への最初の呼び出しのアプリケーションから取得されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-133">In this example, "Posting Results" comes from the application's first call to **SetPrefix()**.</span></span>

<span data-ttu-id="00e47-134">[![SetPrefix の例](./media/3_api.png)](./media/3_api.png)</span><span class="sxs-lookup"><span data-stu-id="00e47-134">[![SetPrefix example](./media/3_api.png)](./media/3_api.png)</span></span> 

<span data-ttu-id="00e47-135">ユーザーは、**メッセージの詳細** をクリックして、新しい **メッセージの詳細** ウィンドウを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="00e47-135">The user can then click **Message details** to open the new **Message details** pane.</span></span> 

<span data-ttu-id="00e47-136">[![メッセージの詳細ウィンドウ](./media/4_api.png)](./media/4_api.png)</span><span class="sxs-lookup"><span data-stu-id="00e47-136">[![Message details pane](./media/4_api.png)](./media/4_api.png)</span></span>

## <a name="message"></a><span data-ttu-id="00e47-137">Message()</span><span class="sxs-lookup"><span data-stu-id="00e47-137">Message()</span></span> 
<span data-ttu-id="00e47-138">**メッセージ** API には、いくつかの便利なメッセージング機能があります。</span><span class="sxs-lookup"><span data-stu-id="00e47-138">The **Message** API provides some useful messaging capabilities.</span></span> <span data-ttu-id="00e47-139">**Message ()** API を使用すると、メッセージを明示的に追加および削除できるため、メッセージのライフサイクルをより詳細に制御できます。</span><span class="sxs-lookup"><span data-stu-id="00e47-139">The **Message()** API gives you more control over the lifecycle of a message by allowing you to explicitly add and remove messages.</span></span> <span data-ttu-id="00e47-140">この API は、保存境界を超えたとき以外に検証メッセージを削除する必要がある場合や、データ検証に必ずしも関連しないユーザー エクスペリエンスの側面に関する情報メッセージを表示する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="00e47-140">This API can be useful when validation messages need to be removed at times other than when a save boundary has been crossed, or for displaying informational messages about aspects of the user's experience that aren't necessarily related to data validation.</span></span> <span data-ttu-id="00e47-141">この例では、現在のレコードが表示されるときにメッセージは表示されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-141">In this example, the message is shown when the current record is displayed.</span></span>

![メッセージの例::情報メッセージに使用される API を追加する](./media/cli-legacyInfo.png)

```xpp
messageId = Message::Add(MessageSeverity::Informational, "The customer is marked as inactive");
```

<span data-ttu-id="00e47-143">新しいレコードがページに表示されると、メッセージはクリアされます。</span><span class="sxs-lookup"><span data-stu-id="00e47-143">The message can then be cleared when a new record is shown on the page.</span></span>

```xpp
Message::Remove(messageId);
```

<span data-ttu-id="00e47-144">バージョン 10.0.10 / Platform update 34 以降では、**Message::AddAction()** メソッドを使用して、メッセージ内にアクションを埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="00e47-144">Starting in version 10.0.10 / Platform update 34, you can use the **Message::AddAction()** method to embed an action within a message.</span></span> <span data-ttu-id="00e47-145">このメソッドは、表示メニュー項目またはアクション メニュー項目に関連付けられた 1 つのアクションの追加をサポートし、リンク ボタンとして視覚化されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-145">This method supports adding a single action that is associated with a display or action menu item, which is then visualized as a link button.</span></span> <span data-ttu-id="00e47-146">アクションは、バージョン 10.0.16/Platform update 40 までメッセージ バーにルーティングされるメッセージでのみサポートされ、その時点でアクション センターまたはメッセージの詳細ウィンドウにルーティングされるメッセージに、これらのアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-146">The actions are only supported in messages that are routed to the message bar until version 10.0.16 / Platform update 40, at which time these actions can be seen in messages that are routed to the Action center or the Message details pane.</span></span>

<span data-ttu-id="00e47-147">この例では、システム管理者に特定の必要なバッチ ジョブが実行されていないことを示すメッセージがトリガーされ、**バッチ ジョブ** ページに直接移動するアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="00e47-147">In this example, a message is triggered for a system administrator indicating a particular required batch job is not running and exposes an action to go directly to the **Batch jobs** page.</span></span>  

![メッセージの例: アクションをメッセージに埋め込むために使用する AddAction API](./media/cli-messageAddAction.png)

```xpp
MenuItemMessageAction actionData = new MenuItemMessageAction();
actionData.MenuItemName("BatchJob");
str jsonData = FormJsonSerializer::serializeClass(actionData);

int64 messageId = Message::AddAction(MessageSeverity::Informational, "The Test batch job is not currently running", "Go to Batch jobs", MessageActionType::DisplayMenuItem, jsonData);

```

<span data-ttu-id="00e47-149">以下のメッセージタイプがサポートされています: **MessageSeverity::Info**、**MessageSeverity::Warning**、および **MessageSeverity::Error**。</span><span class="sxs-lookup"><span data-stu-id="00e47-149">The following messaging types are supported: **MessageSeverity::Info**, **MessageSeverity::Warning**, and **MessageSeverity::Error**.</span></span> <span data-ttu-id="00e47-150">また、**Message()** API を使用するメッセージは確定的となります。</span><span class="sxs-lookup"><span data-stu-id="00e47-150">Messages that use the **Message()** API are also deterministic.</span></span> <span data-ttu-id="00e47-151">メッセージ バーまたはアクション センターにルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="00e47-151">They can be routed to a message bar or the Action center.</span></span>

## <a name="systemnotificationsmanager"></a><span data-ttu-id="00e47-152">SystemNotificationsManager()</span><span class="sxs-lookup"><span data-stu-id="00e47-152">SystemNotificationsManager()</span></span> 
<span data-ttu-id="00e47-153">**SystemNotificationsManager()** API は、アクション センターに送信されるように設計された通知を対象としています。</span><span class="sxs-lookup"><span data-stu-id="00e47-153">The **SystemNotificationsManager()** API targets notifications designed to be sent to the Action center.</span></span> <span data-ttu-id="00e47-154">この API は、次の機能を提供します:</span><span class="sxs-lookup"><span data-stu-id="00e47-154">This API provides the following features:</span></span> 

+ <span data-ttu-id="00e47-155">1 つ以上のアクションの通知への関連付け</span><span class="sxs-lookup"><span data-stu-id="00e47-155">Associating one or more actions to the notification</span></span> 
+ <span data-ttu-id="00e47-156">通知を一連のユーザー、または 1 つ以上のセキュリティ ロールのすべてのユーザーにルーティングする</span><span class="sxs-lookup"><span data-stu-id="00e47-156">Routing a notification to a set of users, or to all the users in one or more security roles</span></span>
+ <span data-ttu-id="00e47-157">通知の有効期限の定義</span><span class="sxs-lookup"><span data-stu-id="00e47-157">Defining an expiration date for the notification</span></span>
+ <span data-ttu-id="00e47-158">通知の状態の追跡 (通知に "完了" としてマークできるなど)</span><span class="sxs-lookup"><span data-stu-id="00e47-158">Tracking the state of the notification (e.g. you can mark a notification as "Completed")</span></span>  

<span data-ttu-id="00e47-159">この例では、ユーザーが Excel へのエクスポートを完了した後に通知が発生します。</span><span class="sxs-lookup"><span data-stu-id="00e47-159">In this example, a notification is raised after an export to Excel is completed by a user.</span></span> <span data-ttu-id="00e47-160">このメッセージは、エクスポートされたファイルへのリンクが使用できなくなるまで、アクション センターで今後 48 時間使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="00e47-160">The message will be available in the Action center for the next 48 hours, after which the link to the exported file is no longer available.</span></span>   

![SystemNotificationsManager APIを使用して送信されたメッセージの例](./media/cli-systemNotification.png)

```xpp
// Set up the notification 
SystemNotificationDataContract notification = new SystemNotificationDataContract();
notification.Users().value(1, curUserId());
notification.Title("Export to Excel finished");
notification.RuleId('ExcelStaticExport');
notification.Message("We finished your export from the Customers page");
notification.ExpirationDateTime(DateTimeUtil::addHours(DateTimeUtil::utcNow(), 48));

// Set up the action associated with the notification
SystemNotificationActionDataContract action = new SystemNotificationActionDataContract();
action.Message("Click to download");
action.Type(SystemNotificationActionType::AxActionMenuFunction);

SystemNotificationMenuFunctionDataContract actionData = new SystemNotificationMenuFunctionDataContract();
actionData.MenuItemName(menuItemActionStr(ExportToExcelStaticOpenFileAction));
actionData.Data(fileName);
action.Data(FormJsonSerializer::serializeClass(actionData));
notification.Actions().value(1, action);

SystemNotificationsManager::AddNotification(notification);
```

## <a name="additional-resources"></a><span data-ttu-id="00e47-162">追加リソース</span><span class="sxs-lookup"><span data-stu-id="00e47-162">Additional resources</span></span>

[<span data-ttu-id="00e47-163">ユーザー インターフェイス開発のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="00e47-163">User interface development home page</span></span>](user-interface-development-home-page.md)
