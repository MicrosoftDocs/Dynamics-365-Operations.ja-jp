---
title: マスター プラン ジョブのキャンセル
description: この記事では、組み込み計画機能を使用する有効な計画ジョブを取り消す方法について説明します。
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
ms.openlocfilehash: 6a9667be9921fdde7e1ca5de68c7f51d48905ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860786"
---
# <a name="cancel-a-master-planning-job"></a>マスター プラン ジョブのキャンセル

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management には、マスター プラン ジョブをキャンセルする複数のオプションがあります。 たとえば、マスター プラン ジョブが誤って開始された、または予想よりも長い時間実行していて終了したい場合、キャンセルすることができます。 計画ジョブをキャンセルする最善の方法は、**未完了の計画プロセス** ページからのキャンセルです。 **バッチ ジョブ** および **バッチ ジョブ拡張** ページからの代替オプションは、**未完了の計画プロセス** ページからマスタープラン ジョブをキャンセルしても数分以内に完了しなかった場合にのみ使用してください。

## <a name="preferred-cancel-option"></a>優先するキャンセル オプション
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>**未完了の計画プロセス** ページからマスター プラン ジョブをキャンセルする
1. **マスター プラン > 照会およびレポート > マスター プラン > 未完了の計画プロセス** の順に移動します。
2. キャンセルする計画プロセスを含む行を選択します。
3. **キャンセル** をクリックします。

## <a name="additional-cancel-options"></a>追加のキャンセル オプション
これらは、**未完了の計画プロセス** ページからのマスター プラン ジョブをキャンセルしても数分以内に完了しなかった場合にのみ使用してください。

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>**バッチ ジョブ** ページからマスター プラン ジョブを削除する
1. **システム管理 > 照会 > バッチ ジョブ** の順に移動します。
2. 削除する計画ジョブを含む行を選択します。
3. **削除** をクリックします。

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>**バッチ ジョブ拡張** ページからのマスター プラン ジョブ タスクを中止する
1. **システム管理 > 照会 > バッチ ジョブ** の順に移動します。
2. 一覧にジョブ ID が表示されない場合、**拡張フォームに切り替える** をクリックします。それ以外の場合は次の手順に進みます。
3. バッチ ジョブを開きます。 終了するタスクを含むバッチ ジョブの **ジョブ ID** をクリックします。
4. **バッチ タスク** で、終了するタスクを選択します。
5. **ステータスの変更** をクリックし、**キャンセル**、続いて **OK** をクリックします。
6. **バッチ タスク** クイック タブで **中止** をクリックします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]