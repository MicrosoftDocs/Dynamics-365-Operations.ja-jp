---
title: 非推奨のマスター プラン エンジンで作成したジョブをキャンセルする
description: この記事では、非推奨のマスター プラン エンジンを使用する有効なプラン ジョブを取り消す方法について説明します。
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740880"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>非推奨のマスター プラン エンジンで作成したジョブをキャンセルする

[!include [banner](../includes/banner.md)]

非推奨のマスター プラン エンジンを使用して作成したジョブをキャンセルするための複数のオプションがあります。 たとえば、マスター プラン ジョブが誤って開始された、または予想よりも長い時間実行していて終了したい場合、キャンセルすることができます。

計画ジョブをキャンセルする最善の方法は、**未完了の計画プロセス** ページからのキャンセルです。 **バッチ ジョブ** および **バッチ ジョブ拡張** ページからの代替オプションは、**未完了の計画プロセス** ページからマスタープラン ジョブをキャンセルしても数分以内に完了しなかった場合にのみ使用してください。

## <a name="preferred-cancel-option"></a>優先するキャンセル オプション

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>未完了の計画プロセス ページからマスター プラン ジョブをキャンセルする

1. **マスター プラン > 照会およびレポート > マスター プラン > 未完了の計画プロセス** の順に移動します。
2. キャンセルする計画プロセスを含む行を選択します。
3. **キャンセル** を選択します。

## <a name="additional-cancel-options"></a>追加のキャンセル オプション

これらは、**未完了の計画プロセス** ページからのマスター プラン ジョブをキャンセルしても数分以内に完了しなかった場合にのみ使用してください。

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>**バッチ ジョブ** ページからマスター プラン ジョブを削除する

1. **システム管理 > 照会 > バッチ ジョブ** の順に移動します。
2. 削除する計画ジョブを含む行を選択します。
3. **削除** を選択します。

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>**バッチ ジョブ拡張** ページからのマスター プラン ジョブ タスクを中止する

1. **システム管理 > 照会 > バッチ ジョブ** の順に移動します。
2. 一覧にジョブ ID が表示されない場合、**拡張フォームに切り替える** をクリックします。それ以外の場合は次の手順に進みます。
3. バッチ ジョブを開きます。 終了するタスクを含むバッチ ジョブの **ジョブ ID** を選択します。
4. **バッチ タスク** で、終了するタスクを選択します。
5. **ステータスの変更** を選択し、**キャンセル** を選択して、**OK** をクリックします。
6. **バッチ タスク** クイック タブで **中止** をクリックします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]