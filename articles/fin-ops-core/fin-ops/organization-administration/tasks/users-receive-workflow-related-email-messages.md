---
title: ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする
description: ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b7a953ea54286a7e48b392728d2cc9bb2902072
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692821"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>ワークフロー関連の電子メール メッセージを受信するためのユーザーを有効にする

[!include [banner](../../includes/banner.md)]

ワークフロー関連のイベントが発生するときに電子メール メッセージを送信するようにシステムを構成することができます。 たとえば、ドキュメントが承認のためにユーザーに割り当てられたとき、電子メール メッセージをユーザーに送信できます。 この手順の作成に使用するデモ データの会社は USMF です。

1. **ナビゲーション ウィンドウ > モジュール > システム管理 > ユーザー > ユーザー** の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. **アクション ウィンドウ** で、**ユーザー オプション** をクリックします。
4. **ワークフロー** タブをクリックします。**通知** セクションが展開されていることを確認します。 **通知** セクションで、ワークフローに関連するイベントについてユーザーに通知する方法を指定することができます。  
5. **行項目ワークフロー通知タイプ** フィールドで、オプションを選択します。
    - グループ化 – 複数の行項目の通知が、1 つの電子メール メッセージにまとめられます。
    - 個別 – 電子メール メッセージが各行項目のために送信されます。  
    - ユーザーがクライアントで通知を受信する場合は、**通知を電子メールで送信** チェック ボックスを選択します。  
6. **保存** をクリックします。
7. ページを閉じます。

> [!NOTE]
> ワークフローがシステムレベル (会社固有ではない) または組織レベル (会社固有) のワークフローのいずれであるかによって、ワークフローの電子メール テンプレートは、システム電子メール テンプレートまたは組織の電子メール テンプレートから取得されます。
