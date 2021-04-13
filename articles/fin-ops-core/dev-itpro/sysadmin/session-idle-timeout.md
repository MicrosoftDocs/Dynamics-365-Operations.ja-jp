---
title: セッション非活動タイムアウトの設定
description: このトピックでは、セッション非活動タイムアウトを設定する方法について説明します。
author: paulliew
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: IT Pro
ms.reviewer: sericks
ms.custom: 13531
ms.search.region: Global
ms.author: paulliew
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: Platform update 29
ms.openlocfilehash: 872c23448da3101c88d2e120f137256e4732dfa1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745906"
---
# <a name="set-the-session-inactivity-timeout"></a>セッション非活動タイムアウトの設定

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

セッション非活動タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非活動になれる時間の長さを表します。 ユーザーブラウザセッションにのみ影響します。

この値は、5 分から 60 分の間で設定できます。

この機能には、30 分の既定値があります。 最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。

> [!NOTE] 
> この機能は、Platform update 29 以降で利用できます。
>
> 以前 web.config (**WebClientStatefulSessionTimeoutInSeconds** キー) でセッション非活動タイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。 既定の変更では、web config で新しいセッション非活動タイムアウトを明示的に設定していない人にのみ変更が反映されます。

この値を変更するには、次の手順に従います。

1. **システム管理 > 設定 > システム パラメーター** を選択して、**システム パラメーター** ページを開きます。
2. **一般** タブの **セッションの管理** セクションで、**セッション非活動タイムアウト (分)** フィールドに値を入力します。
3. **保存** を選択します。 

    この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。 以下のような確認を求めるメッセージが表示されます。「非活動セッションタイムアウトの増加によって、システムに余分な負荷が発生することがあり、パフォーマンスが低下する可能性があります。 本当に続行しますか？ この値が大きくなるほど負荷が大きくなり、システム パフォーマンスに悪影響を与える可能性があります。 **はい** を選択して変更を保存するか、**いいえ** を選択して既存値に戻します。
    
### <a name="alerting-users-before-sessions-end-due-to-inactivity"></a>非操作時間の経過によりセッションが終了する前にユーザーに警告する
非活動によりセッションが中断されることをユーザーに認識させ、保存されていない変更をユーザーが失わないようにするために、非活動によるセッションの終了が設定される前にユーザーに通知され、再接続の機会が与えられます。 ユーザーへの通知は、**セッション非活動タイムアウト** の設定によって異なります。 

-  **セッション非活動タイムアウト** が 30 分を超える場合は、セッションが終了に設定される **5 分** 前にカウントダウン通知が表示されます。 
-  **セッション非活動タイムアウト** が 10 分～30 分の間である場合は、セッションが終了に設定される **2 分** 前にカウントダウン通知が表示されます。 
-  **セッション非活動タイムアウト** が 10 分以下の場合は、セッションが終了に設定される **30 秒** 前にカウントダウン通知が表示されます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]