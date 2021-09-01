---
title: デリゲートを使用してアプリケーション起動をカスタマイズする
description: このトピックでは、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。
author: jorisdg
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: e33e724d38b6d13b729635ff8a11df615b59c1cc3099a6fc24a277246fdccd09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754318"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]