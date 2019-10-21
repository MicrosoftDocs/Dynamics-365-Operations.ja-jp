---
title: セッション アイドル タイムアウトの設定
description: このトピックでは、セッション アイドル タイムアウトの設定方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 08/07/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: Platform update 29
ms.openlocfilehash: 8af87044854f7656108306442b49d26420a225c0
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248720"
---
# <a name="set-the-session-idle-timeout"></a>セッション アイドル タイムアウトの設定

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

セッション アイドル タイムアウト設定は、ユーザーのセッションがタイムアウトして閉じる前にユーザーが非アクティブになれる時間の長さを表します。 ユーザーブラウザセッションにのみ影響します。

この値は、5 分から 60 分の間で設定できます。

この機能には、30 分の既定値があります。 最大 60 分まで値を設定できますが、これによりシステムに余分な負荷が発生する可能性があります。

> [!NOTE] 
> この機能は、Platform update 29 以降で利用できます。

> [!IMPORTANT]
> 以前 web.config (**WebClientStatefulSessionTimeoutInSeconds**キー) でセッションアイドルタイムアウトを設定していた場合には、サポート要求を通じて、その以前の値が引き続き使用されます。 既定の変更では、web config で新しいセッションアイドルタイムアウトを明示的に設定していない人にのみ変更が反映されます。

この値を変更するには、次の手順に従います。

1. ダッシュボードから、**システム管理**ワークスペースを選択します。
2. **システム設定** の選択 これにより、**システム パラメーター** ページが開きます。
3. **セッション管理** セクションで、**セッション アイドル タイムアウトを分単位で** 設定します。
4. **保存** を選択します。 

    この値を 30 より大きい値に設定すると、選択を確認するメッセージが表示されます。 「アイドル セッション タイムアウトの増加によって、システムに余分な負荷が発生することがあります」 という確認メッセージが表示され、これにより、パフォーマンスが低下する可能性があります。 本当に続行しますか？ この値が大きくなるほど負荷が大きくなり、システム パフォーマンスに悪影響を与える可能性があります。 **はい**を選択して変更を保存するか、**いいえ**を選択して既存値に戻します。

