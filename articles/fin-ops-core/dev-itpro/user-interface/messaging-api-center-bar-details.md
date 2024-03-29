---
title: メッセージング API - アクション センター、メッセージ バー、メッセージ詳細
description: この記事では、メッセージング システムについて説明します。
author: jasongre
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 64153
ms.assetid: b69ec992-9bde-469e-99bb-773feb9489ff
ms.openlocfilehash: f2ca71e12512de2ec088812ae926ce6083ac1747
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291728"
---
# <a name="messaging-apis---action-center-message-bar-and-message-details"></a>メッセージング API - アクション センター、メッセージ バー、メッセージ詳細

[!include [banner](../includes/banner.md)]

この記事では、財務と運用アプリのメッセージング システムについて、特にメッセージを作成してエンド ユーザーにルーティングするために使用されるアプリケーション プログラミング インターフェイス (API) の観点から、説明します。  

## <a name="introduction"></a>概要

このエクスペリエンスを改善するために、財務と運用アプリ用に新しいメッセージング システムが作成されました。 以前のバージョンと比較すると、財務と運用アプリのメッセージング システムには次の機能が含まれています:

+ コンテキストのあるメッセージの関連性が強化されました (フォームとグローバル)。
+ 中断のレベル (なし、軽微、および中断) を強化しました。
+ メッセージの種類間での明確さと、その用途が強化されました。
+ メッセージを表示するために使用されるコントロールは、フォーム コンテキストに基づいて deterministic です。

## <a name="backwards-compatibility-of-info-warningcheckfailed-and-error"></a>Info()、warning()/checkfailed()、error() の下位互換性 
以前のバージョンの財務と運用アプリからの **info()**、**warning()**、および **error()** のアプリケーション プログラミング インターフェイス (API) は引き続きサポートされますが、これらの API は現在、フレームワークの新しいメッセージング システム上にあります。 API呼び出しのコンテキストを使用して、ユーザーにメッセージを提示する最適な方法を決定することにより、メッセージは確定的にメッセージまたはアクション センター (中断しない方法で) にルーティングされます。 一般に、API の使用がフォームから生成された場合、そのメッセージが同じフォーム上のメッセージ バーで表示されます。 (ドロップ ダイアログとスライダ ダイアログは、どちらもフォームと見なされます。) 

次の図は、ページ アクションに対応する **情報**、**警告**/**checkfailed**、**エラー** メッセージ バー、または **info()**、**warning()**、**error()** からの同期作成メッセージを示しています。 

[![情報、警告/checkfailed、エラー メッセージを示すスクリーン ショット。](./media/cli-legacyMessages.png)](./media/cli-legacyMessages.png)

> [!NOTE]
> スライダー ダイアログからこれらの API が呼び出されても、メッセージが表示される前にそのスライダー ダイアログが閉じられると、メッセージはスライダー ダイアログの親ページのメッセージ バーに表示されます。 メッセージが表示される前にそのスライダー ダイアログ ボックスが閉じられ、親ページが存在しない場合、メッセージは、アクション センターにルーティングされます。 メッセージング API は必ずメッセージを表示します。 適切なホスト ページが見つからない場合は、メッセージがアクション センターに送信されます。

**info()**、**warning()**/**checkfailed()**、または **error()** が非同期プロセス (たとえば、バッチ) から呼び出された場合、考慮するフォーム コンテキストはなく、メッセージはアクション センターに送信されます。 (アクション センターを開くには、ナビゲーションバーの **メッセージを表示** ボタンをクリックします。) 次の図は、アクション センターの各種メッセージの例を示しています。 

[![アクション センターのメッセージ。](./media/2_api.png)](./media/2_api.png)

> [!NOTE]
> **Box()** API を使用して、ユーザーに中断エラーを表します。                                                               

## <a name="backwards-compatibility-of-setprefix"></a>SetPrefix() の下位互換性 
財務と運用アプリは、下位互換性のために **SetPrefix()** API もサポートしています。 ただし、メッセージング システムでは、**SetPrefix()** の結果は、積極的にユーザーを中断しません; 代わりに、結果が (以前のバージョンと同様に) 収集および保存され、メッセージ バーまたはアクション センターの通知がユーザーに表示されます。 この通知は、関連するタスクが完了し、ユーザーが確認する必要のあるメッセージがある可能性があることを示します。 「結果の通知」メッセージは、実際にはタスクによる **SetPrefix()** の最初の呼び出しを使ってメッセージをフレーム化します。 この動作は、最初の呼び出しが結果の「タイトル」であった以前のバージョンの動作に類似しています。 この例では、「転記の結果」が **SetPrefix()** への最初の呼び出しのアプリケーションから取得されます。

[![SetPrefix の例。](./media/3_api.png)](./media/3_api.png) 

ユーザーは、**メッセージの詳細** をクリックして、新しい **メッセージの詳細** ウィンドウを開くことができます。 

[![メッセージの詳細ウィンドウ。](./media/4_api.png)](./media/4_api.png)

## <a name="message"></a>Message() 
**メッセージ** API には、いくつかの便利なメッセージング機能があります。 **Message ()** API を使用すると、メッセージを明示的に追加および削除できるため、メッセージのライフサイクルをより詳細に制御できます。 この API は、保存境界を超えたとき以外に検証メッセージを削除する必要がある場合や、データ検証に必ずしも関連しないユーザー エクスペリエンスの側面に関する情報メッセージを表示する場合に役立ちます。 この例では、現在のレコードが表示されるときにメッセージは表示されます。

![メッセージの例::情報メッセージに使用される API を追加します。](./media/cli-legacyInfo.png)

```xpp
messageId = Message::Add(MessageSeverity::Informational, "The customer is marked as inactive");
```

新しいレコードがページに表示されると、メッセージはクリアされます。

```xpp
Message::Remove(messageId);
```

バージョン 10.0.10 / Platform update 34 以降では、**Message::AddAction()** メソッドを使用して、メッセージ内にアクションを埋め込むことができます。 このメソッドは、表示メニュー項目またはアクション メニュー項目に関連付けられた 1 つのアクションの追加をサポートし、リンク ボタンとして視覚化されます。 アクションは、バージョン 10.0.16/Platform update 40 までメッセージ バーにルーティングされるメッセージでのみサポートされ、その時点でアクション センターまたはメッセージの詳細ウィンドウにルーティングされるメッセージに、これらのアクションが表示されます。

この例では、システム管理者に特定の必要なバッチ ジョブが実行されていないことを示すメッセージがトリガーされ、**バッチ ジョブ** ページに直接移動するアクションが表示されます。  

![メッセージの例: アクションをメッセージに埋め込むために使用する AddAction API。](./media/cli-messageAddAction.png)

```xpp
MenuItemMessageAction actionData = new MenuItemMessageAction();
actionData.MenuItemName("BatchJob");
str jsonData = FormJsonSerializer::serializeClass(actionData);

int64 messageId = Message::AddAction(MessageSeverity::Informational, "The Test batch job is not currently running", "Go to Batch jobs", MessageActionType::DisplayMenuItem, jsonData);

```

以下のメッセージタイプがサポートされています: **MessageSeverity::Info**、**MessageSeverity::Warning**、および **MessageSeverity::Error**。 また、**Message()** API を使用するメッセージは確定的となります。 メッセージ バーまたはアクション センターにルーティングできます。

## <a name="systemnotificationsmanager"></a>SystemNotificationsManager() 
**SystemNotificationsManager()** クラスでは、アクション センターに通知を送信できます。 このクラスは、次の機能を提供します: 

+ 1 つ以上のアクションの通知への関連付け。 
+ 通知を一連のユーザー、または 1 つ以上のセキュリティ ロールのすべてのユーザーにルーティングする。
+ 通知の有効期限の定義。
+ 通知の状態の追跡 (通知に「完了」としてマークできるなど)。  
+ RuleID によって通知に適用されるルールまたはプロセスを定義する。  

この例では、ユーザーが Excel へのエクスポートを完了した後に通知が発生します。 このメッセージは、エクスポートされたファイルへのリンクが使用できなくなるまで、アクション センターで今後 48 時間使用できるようになります。   

> [!NOTE]
> **AddNotification()** API は、以前にこの例で使用されています。 バージョン 10.0.23 の場合、API は廃止され、**AddSystemNotification()** API に置き換えられる予定です。 新しい API は、RuleID と ExpirationDateTime の設定を要求します。 

![SystemNotificationsManager API を使用して送信されたメッセージの例。](./media/cli-systemNotification.png)

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

SystemNotificationsManager::AddSystemNotification(notification);
```

## <a name="additional-resources"></a>追加リソース

[ユーザー インターフェイス開発のホーム ページ](user-interface-development-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

