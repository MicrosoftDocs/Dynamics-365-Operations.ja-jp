--- 
title: "バッチ ジョブの作成"
description: "バッチ ジョブは、自動処理のために Application Object Server (AOS) インスタンスに送信されるタスクのグループです。"
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b32c16a0c0045e22128746f81c6e9fd03370ac1f
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-batch-jobs"></a>バッチ ジョブの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

バッチ ジョブは、自動処理のために Application Object Server (AOS) インスタンスに送信されるタスクのグループです。 バッチ ジョブは、ジョブを作成したユーザーのセキュリティ資格情報を使用して実行されます。 バッチ ジョブを作成するには、次の手順に従います。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-the-batch-job"></a>バッチ ジョブの作成
1. [システム管理] > [照会] > [バッチ ジョブ] の順に移動します。
2. [新規] をクリックします。
3. [ジョブの説明] フィールドに値を入力します。
4. [開始予定日時] フィールドで、日時を入力します。
5. [保存] をクリックします。

## <a name="create-a-recurrence"></a>再実行の作成
1. アクション ウィンドウで、[バッチ ジョブ] をクリックします。
2. [再実行] をクリックします。
    * これらのオプションを使用して再実行の範囲とパターンを入力します。  
3. [OK] をクリックします。

## <a name="add-alerts"></a>警告の追加
1. アクション ウィンドウで、[バッチ ジョブ] をクリックします。
2. [警告] をクリックします。
    * バッチ ジョブの終了時、エラー発生時、またはキャンセル時に警告メッセージを表示するかを指定します。 そして、警告をポップアップ メッセージとして表示するかどうかを指定します。   
3. [OK] をクリックします。


