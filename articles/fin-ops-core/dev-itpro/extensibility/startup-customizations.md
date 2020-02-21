---
title: デリゲートを使用してアプリケーション起動をカスタマイズする
description: このトピックでは、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: c1978e468e67de5a22427dae9a7f1b55163c5a16
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983648"
---
# <a name="customize-application-startup-by-using-delegates"></a>デリゲートを使用してアプリケーション起動をカスタマイズする

[!include [banner](../includes/banner.md)]

Dynamics AX 2012 では、クライアントが初期化中に発生したイベント (Application.Startup デリゲート) をサブスクライブできるカスタマイズ ポイントがありました。 これらのイベントはリッチ クライアントの概念がないため推奨されません。 サーバーで、サーバー セッションのみが考慮されますが、以前のリリースからロジックを移行できるため、新しいイベントが **ApplicationStartupEventManager** クラスに追加されました。 

次のセクションでは、拡張機能を使用して既存のフォームに追加できる新しいデータ ソースについて説明します。

## <a name="static-delegate-void-onsystemstartup"></a>static delegate void onSystemStartup()
- このイベントは、システムの起動時に発生します。 
- これは起動時に AOS につき 1 回発生します。

## <a name="static-delegate-void-onfirsttimeuserinteractivesessioncreated"></a>static delegate void onFirstTimeUserInteractiveSessionCreated()
- このイベントは、ユーザーが初めてインタラクティブ セッションを作成しているときに発生します。 
- これは AOS ごとのユーザーにつき 1 回発生します。

## <a name="static-delegate-void-onfirsttimeusernoninteractivesessioncreated"></a>static delegate void onFirstTimeUserNonInteractiveSessionCreated()
- このイベントは、ユーザーが初めて非インタラクティブ セッションを作成しているときに発生します。 
- これは AOS ごとのユーザーにつき 1 回発生します。

## <a name="static-delegate-void-oninteractivesessioncreated"></a>static delegate void onInteractiveSessionCreated()
- このイベントは、インタラクティブ セッションが作成され、使用できる状態になったときに発生します。 
- これは、すべてのユーザーのインタラクティブ セッション作成につき 1 回発生します。

## <a name="static-delegate-void-onsessioncreatedboolean-_isbatch-boolean-_isinteractive"></a>static delegate void onSessionCreated(boolean _isBatch, boolean _isInteractive)
- このイベントは、セッションが作成され、使用できる状態になったときに発生します。 
- これは、すべてのユーザーのインタラクティブ セッション作成につき 1 回発生します。
- *_isBatch* はシステムがバッチ ジョブを実行しているかどうかを指定します。
- *_isInteractive* はセッションが対話型であるかを指定します。

