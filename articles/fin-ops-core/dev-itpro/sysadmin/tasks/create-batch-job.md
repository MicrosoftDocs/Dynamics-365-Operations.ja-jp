---
title: バッチ ジョブの作成
description: バッチ ジョブは、自動処理のために Application Object Server (AOS) インスタンスに送信されるタスクのグループです。
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6eee5c6dd7daf2b0c79dd34d15a7dde919bdd60
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143676"
---
# <a name="create-a-batch-job"></a>バッチ ジョブの作成

[!include [banner](../../includes/banner.md)]

バッチ ジョブは、自動処理のために Application Object Server (AOS) インスタンスに送信されるタスクのグループです。 バッチ ジョブは、ジョブを作成したユーザーのセキュリティ資格情報を使用して実行されます。 バッチ ジョブを作成するには、次の手順に従います。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-the-batch-job"></a>バッチ ジョブの作成
1. **ナビゲーション ウィンドウ > モジュール > システム管理 > 紹介 > バッチ ジョブ**の順に移動します。
2. **新規** をクリックします。
3. **ジョブの説明**フィールドに、値を入力します。
4. **開始予定日時**フィールドに、日時を入力します。
5. **保存**をクリックします。

## <a name="create-a-recurrence"></a>再実行の作成
1. アクションウィンドウで、**バッチ ジョブ**をクリックします。
2. **再実行**をクリックします。 これらのオプションを使用して再実行の範囲とパターンを入力します。  
3. **OK**をクリックします。

## <a name="add-alerts"></a>警告の追加
1. アクションウィンドウで、**バッチ ジョブ**をクリックします。
2. **警告**をクリックします。 バッチ ジョブの終了時、エラー発生時、またはキャンセル時に警告メッセージを表示するかを指定します。 そして、警告をポップアップ メッセージとして表示するかどうかを指定します。   
3. **OK**をクリックします。

## <a name="adjust-batch-job-status"></a>バッチ ジョブ状態の調整
1. **システム管理 > 照会 > バッチ ジョブ**の順に移動します。
2. 適切なバッチ ジョブを選択します。
3. アクション ウィンドウで、**バッチ ジョブ > 機能 > 状態の変更**をクリックします。
4. 適切な状態を選択します。
    - **源泉徴収** : バッチ ジョブを**源泉徴収**に設定して、バッチ ジョブ スケジューラから源泉徴収されるようにします。 *停止*することを意味します。
    - **待機中** : バッチ ジョブを**待機中**に設定して、バッチ ジョブ スケジューラによる集荷を待機します。 *移動*することを意味します。
5. **OK**をクリックします。
