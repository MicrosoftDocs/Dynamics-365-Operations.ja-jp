--- 
title: "ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする"
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 76ae3b1f479733f7e3a738fd43e52134bda7069a
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする

[!include[task guide banner](../../includes/task-guide-banner.md)]

ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。 たとえば、ドキュメントが承認のためにユーザーに割り当てられたとき、電子メール メッセージをユーザーに送信できます。 この手順の作成に使用するデモ データの会社は USMF です。

1. [システム管理] > [ユーザー] > [ユーザー] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [ユーザー オプション] をクリックします。
4. [ワークフロー] タブをクリックします。
    * 通知セクションが展開されていることを確認します。     通知セクションで、ワークフロー関連イベントについてユーザーに通知する方法を指定することができます。  
5. [行項目ワークフロー通知タイプ] フィールドで、オプションを選択します。
    * グループ化 – 複数の行項目の通知が、1 つの電子メール メッセージにまとめられます。    個別 – 電子メール メッセージが各行項目のために送信されます。  
    * ユーザーがクライアントで通知を受信する場合は、[通知を電子メールで送信] チェック ボックスを選択します。  
6. [保存] をクリックします。
7. ページを閉じます。


