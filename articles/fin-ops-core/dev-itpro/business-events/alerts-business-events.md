---
title: ビジネス イベントとしての警告
description: このトピックでは、ビジネス イベントとしての警告について説明します。
author: Sunil-Garg
ms.date: 11/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 25
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 2f7e4c837e06d98fd79edd779bd2483c2996a95d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754132"
---
# <a name="alerts-as-business-events"></a>ビジネス イベントとしての警告

[!include[banner](../includes/banner.md)]

ユーザーが設定できる警告は 2 種類あります。 これらは変更ベースの警告と期日の警告です。 警告機能の詳細については [警告](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alerts-overview) を参照してください。

変更ベースの警告および期日の警告は、外部のアプリケーションやシステムを通知またはトリガーするメカニズムとして、ビジネス イベントを送信するように設定できます。 これにより、警告は高度なユーザー通知シナリオやシステム間の業務プロセス統合に関与できます。

警告からビジネス イベントを作成するには、**警告ルールの作成** ダイアログ ボックスで、**警告の対象** > **外部に送信** を **はい** に設定します。 

警告が処理されるようにするには、変更ベースまたは期日の警告のバッチ処理を、期日イベントのバッチ処理に設定する必要があります。 詳細については、[期日イベントに関するバッチ処理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/alerts-managing#set-up-processing-for-change-based-alerts) を参照してください。

警告をビジネス イベントとして送信するには、変更ベースの警告や期日の警告のビジネス イベントも有効である必要があります。 有効化プロセスの詳細については、[ビジネス イベントの有効化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page#activating-business-events) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]