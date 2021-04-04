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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]