---
title: セッション アイドル タイムアウトの設定
description: このトピックでは、セッションアイドルタイムアウトを設定する方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 07/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 13531
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-08-02
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ccb32e1393e3fe776f2878a6a34bef97bbc12f0
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863645"
---
# <a name="set-the-session-idle-timeout"></a>セッション アイドル タイムアウトの設定

[!include [banner](../includes/banner.md)]

> [!NOTE]
> この機能は、Platform 更新 29 以降でのみ利用できます。

セッション アイドル タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非アクティブになれる時間の長さを表します。 ユーザーブラウザセッションにのみ影響します。

この値は、5 分から 60 分の間で設定できます。

この機能は UI に公開されており、既定値は 30 分です。 最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。

> [!IMPORTANT]
> 以前 web.config (**WebClientStatefulSessionTimeoutInSeconds**キー) でセッションアイドルタイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。 既定の変更では、web config で新しいセッションアイドルタイムアウトを明示的に設定していない人にのみ変更が反映されます。

UI の値を変更するには、次の手順を実行します。

1. Finance and Operations ダッシュボードから、**システム管理**ワークスペースをクリックします。
2. **システム設定**をクリックします。 これにより、**システムパラメータ** フォームが開きます。
3. **セッション管理** セクションで、**セッションアイドルタイムアウトを分**単位で目的の値に設定します。
4. **保存**をクリックします。 

    この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。 「アイドルセッションタイムアウトの増加によって、システムに余分な負荷が発生することがある」という確認を求めるメッセージが表示され、これにより、パフォーマンスが低下する可能性があります。 本当に続行しますか？ 値が高くなるほど負荷が高くなり、負荷がシステムパフォーマンスに悪影響を与える可能性があります。 **はい**をクリックして変更を保存するか、**いいえ**をクリックして既存の値に戻します。

