---
title: "バッチ処理"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations のバッチ処理の概要について説明します。"
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 34377119b12c537679c423d79449169f3d25dc21
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="batch-processing"></a>バッチ処理

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 for Finance and Operations のバッチ処理の概要について説明します。

Finance and Operations では、多くのタスクをバッチ ジョブの一部として実行できます。 たとえば、バッチ ジョブには、レポートの印刷、管理の実行、電子ドキュメントの送信などのタスクを含めることができます。 バッチ ジョブを使用すると、通常の就業時間内におけるコンピュータまたはサーバーの処理速度の低下を回避できます。 

バッチ ジョブ内のタスクは、順次または同時のいずれかに実行できます。 また、タスク間に依存関係を作成できます。 つまり、前のタスクが成功したか失敗したかによってタスク順序が変わります。 

バッチ ジョブの再実行回数を設定できます。 たとえば、毎月、月末に請求書を自動処理するジョブを設定できます。 

バッチ ジョブを監視するために、警告を設定できます。 バッチジョブが成功した場合、失敗した場合、または実行が完了した場合に警告を送信できます。 

バッチ ジョブの処理後、履歴を表示できます。 履歴には、ジョブの実行中に発生したメッセージが含まれています。 

バッチ グループを使用してバッチ タスクをカテゴリ化し、特定のサーバーで実行します。 作業環境のサーバーには、別のソフトウェアがインストールされているサーバーや、1 日の内で使用できる時間が異なるサーバーがあります。 バッチ グループを使用すると、最も適したサーバーにバッチ タスクを割り当てることができます。 同じバッチ ジョブ内のタスクは、別の複数のバッチ グループに含めることもできます。 

たとえば、サーバー A がレポートを印刷するよう設定され、サーバー B が電子ドキュメントを送信するよう設定されます。 バッチ グループを使用することで、レポート タスクがサーバー A で実行され、電子ドキュメントがサーバー B で処理されることを保証することができます。




