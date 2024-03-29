---
title: バッチ処理の概要
description: この記事では、バッチ処理の概要を示します。
author: Peakerbl
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom:
- "62333"
- intro-internal
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70e595536788b8714fbdf8a2adf65572e722b62e
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109059"
---
# <a name="batch-processing-overview"></a>バッチ処理の概要

[!include [banner](../includes/banner.md)]

この記事では、バッチ処理の概要を示します。

財務と運用では、多くのタスクをバッチ ジョブの一部として実行できます。 たとえば、バッチ ジョブには、レポートの印刷、管理の実行、電子ドキュメントの送信などのタスクを含めることができます。 バッチ ジョブを使用すると、通常の就業時間内におけるコンピュータまたはサーバーの処理速度の低下を回避できます。 

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
-  [バッチ マネージャーのセキュリティ ロール](runby.md)
-  [有効なバッチ期間](activeperiod.md)
-  [バッチ ジョブのコピー](copy-batch-job.md)
-  [警告の設定](alerts.md)
-  [拡張バッチ フォーム](enhanced-forms.md)
-  [バッチジョブ履歴のクリーンアップ](batch-history-cleanup.md)
-  [実行中のバッチ ジョブの中止](batch-abort.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
