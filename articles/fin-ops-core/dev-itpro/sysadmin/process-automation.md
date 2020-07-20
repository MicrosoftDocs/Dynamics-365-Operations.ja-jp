---
title: プロセスの自動化
description: このトピックでは、プロセスの自動化を使用して、バッチ サーバーによって実行されるプロセスを簡単にスケジューリングする方法について詳しく説明します。
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508188"
---
# <a name="process-automation"></a>プロセスの自動化

[!include[banner](../includes/banner.md)]

プロセスの自動化を使用すると、バッチ サーバーによって実行されるプロセスを簡単にスケジューリングすることができます。 更新されたスケジュール済作業のカレンダー表示では、、エンド ユーザーがスケジュール済および完了済の作業を表示してアクションを実行できるようになります。

## <a name="administration"></a>管理

すべてのプロセス自動化の全体管理ページは、システム管理モジュールの**設定**メニューにあります。 このページには、システムで設定されているすべての自動化されたプロセス (シリーズ) が一覧表示されます。 また、このページから新しいプロセスの自動化を直接追加することもできます。 シリーズを設定した後は、この一覧から各シリーズを管理できます。 シリーズ全体を編集したり、削除したり、リスト ビューにすべての発生を表示したり、一定の期間にスケジュール済の作業を一時停止する場合にこのシリーズを無効にしたりできます。 

## <a name="calendar-view"></a>カレンダー表示 
プロセス自動化の主な利点の 1 つとして、スケジュール済の作業を単純なカレンダー表示で確認できる機能があります。  この表示では、一度に 1 週間の作業を表示できます。 このビューは、**プロセスの自動化**ページの右側に表示されます。 選択したシリーズのスケジュール済の作業が設定されます。 

[![プロセス自動化カレンダー](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>発生の変更
それぞれの発生は、その発生を作成したシリーズによって定義されている他の発生に影響を与えることなく変更できます。 スケジュール済の作業の発生をカレンダー表示から編集するには、**表示/編集**ボタンを選択して**発生**を選択します。 これにより、シリーズの設定ウィザードで最初に表示されたすべての設定にアクセスでき、選択した発生に対して 1 回限りの変更を行うことができます。 スケジュール済の作業の発生は、カレンダー表示の**無効**ボタンを選択することによって無効にすることもできます。 

## <a name="developer-documentation"></a>開発者のドキュメント 
開発者ドキュメントは、開発者がプロセス自動化フレームワークを拡張できるようするため、現在作成中です。 このドキュメントでは、プロセス自動化ウィザードでスケジュールされたバッチ サーバーによって実行され、カレンダー表示に自動的に表示される必要があるカスタム プロセスを作成する方法について説明します。
