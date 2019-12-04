---
title: ビジネス イベントとしての警告
description: このトピックでは、ビジネス イベントとしての警告について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 11/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 25
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: e3317a93e05f861af9bd8aa87c6cac5d1cb50f99
ms.sourcegitcommit: 01e43f0f71425a399dda55b6ec315a4186bcf830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2019
ms.locfileid: "2801433"
---
# <a name="alerts-as-business-events"></a>ビジネス イベントとしての警告

[!include[banner](../includes/banner.md)]

ユーザーが設定できる警告は 2 種類あります。 これらは変更ベースの警告と期日の警告です。 警告機能の詳細については [警告](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/alerts-overview) を参照してください。

変更ベースの警告および期日の警告は、外部のアプリケーションやシステムを通知またはトリガーするメカニズムとして、ビジネス イベントを送信するように設定できます。 これにより、警告は高度なユーザー通知シナリオやシステム間の業務プロセス統合に関与できます。

警告からビジネス イベントを作成するには、**警告ルールの作成**ダイアログ ボックスで、**警告の対象** > **外部に送信**を**はい**に設定します。 

警告が処理されるようにするには、変更ベースまたは期日の警告のバッチ処理を、期日イベントのバッチ処理に設定する必要があります。 詳細については、[期日イベントに関するバッチ処理](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/alerts-managing#set-up-processing-for-change-based-alerts) を参照してください。

警告をビジネス イベントとして送信するには、変更ベースの警告や期日の警告のビジネス イベントも有効である必要があります。 有効化プロセスの詳細については、[ビジネス イベントの有効化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page#activating-business-events) を参照してください。
