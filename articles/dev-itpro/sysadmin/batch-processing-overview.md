---
title: バッチ処理の概要
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations でのバッチ処理の概要を示します。
author: hasaid
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2286e9731abed691d1cc171f88639ce091322d1
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864218"
---
# <a name="batch-processing-overview"></a>バッチ処理の概要

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations でのバッチ処理の概要を示します。

Finance and Operations では、多くのタスクをバッチ ジョブの一部として実行できます。 たとえば、バッチ ジョブには、レポートの印刷、管理の実行、電子ドキュメントの送信などのタスクを含めることができます。 バッチ ジョブを使用すると、通常の就業時間内におけるコンピュータまたはサーバーの処理速度の低下を回避できます。 

バッチ ジョブ内のタスクは、順次または同時のいずれかに実行できます。 また、タスク間に依存関係を作成できます。 つまり、前のタスクが成功したか失敗したかによってタスク順序が変わります。 

バッチ ジョブの再実行回数を設定できます。 たとえば、毎月、月末に請求書を自動処理するジョブを設定できます。 

バッチ ジョブを監視するために、警告を設定できます。 バッチジョブが成功した場合、失敗した場合、または実行が完了した場合に警告を送信できます。 

バッチ ジョブの処理後、履歴を表示できます。 履歴には、ジョブの実行中に発生したメッセージが含まれています。 

バッチ グループを使用してバッチ タスクをカテゴリ化し、特定のサーバーで実行します。 作業環境のサーバーには、別のソフトウェアがインストールされているサーバーや、1 日の内で使用できる時間が異なるサーバーがあります。 バッチ グループを使用すると、最も適したサーバーにバッチ タスクを割り当てることができます。 同じバッチ ジョブ内のタスクは、別の複数のバッチ グループに含めることもできます。 

たとえば、サーバー A がレポートを印刷するよう設定され、サーバー B が電子ドキュメントを送信するよう設定されます。 バッチ グループを使用することで、レポート タスクがサーバー A で実行され、電子ドキュメントがサーバー B で処理されることを保証することができます。

詳細については、[バッチ処理とバッチ サーバー](batch-server-overview.md) を参照してください。


## <a name="batch-functions"></a>バッチ関数

管理者およびバッチ マネージャーは、バッチ ジョブの作成とコピー、バッチ ジョブ ユーザーの変更、ジョブを実行しない期間の指定などの一般的なタスクを実行できます。 これらのタスクの詳細については、次のトピックを参照してください。

-  [バッチ ジョブの作成](tasks/create-batch-job.md)
-  [バッチ マネージャー ロール](runby.md)
-  [バッチ アクティブ期間](activeperiod.md)
-  [バッチ ジョブのコピー](copy-batch-job.md)
-  [バッチ警告のコンフィギュレーション](alerts.md)
-  [バッチ化された フォーム](enhanced-forms.md)
-  [バッチ履歴のクリーンアップ](batch-history-cleanup.md)
-  [実行中のバッチ ジョブの中止](batch-abort.md)

