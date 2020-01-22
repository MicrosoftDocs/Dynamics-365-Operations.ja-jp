---
title: Dynamics 365 Talent - Core HR (2018 年 11 月 27 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d6b5f5f7b62c400679df5eb014dee05f02e11d0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897491"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-27-2018"></a>Dynamics 365 Talent - Core HR (2018 年 11 月 27 日) の新機能および変更された機能

**ビルド 8.1.2064**

このトピックでは、Core HR の新機能または変更された機能について説明します。


## <a name="changes"></a>変更

### <a name="unable-to-create-a-note-in-case-management"></a>ケース管理にメモを作成できない

ケース管理のケース ログでメモを編集または作成しようとするときの問題のために、変更が加えられました。

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>報酬のワークスペースの分析タブでの誤った表記の単語 

報酬ワークスペースの、報酬分析グラフの「Ethnic Origin」のスペルを修正するための変更が加えられました。

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>従業員セルフ サービス ワークスペースは、ユーザーが作業者に割り当てられていないときには表示されない 

**従業員セルフ サービス** ワークスペースが、作業者に割り当てられていないユーザーの起動時の最初のページとして選択されているときに変更されました。 この状況では、既定のダッシュ ボードが表示されます。

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>休暇と欠勤エラー: オブジェクト参照がオブジェクトのインスタンスに設定されていない

**自分自身に割り当てられた作業項目**リストに休暇と欠勤の記録を承認した後、このエラーを修正するための休暇と欠勤への変更が加えられました。

### <a name="unable-to-recall-an-image-workflow"></a>イメージのワークフローを取り消すことができない

イメージのワークフローを取り消した後は、ワークフローは「キャンセル済」に設定され、従業員セルフ サービス ワークスペースの既存の要求を削除することができます。

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>退職後に何度も表示される再雇用された従業員や契約社員 

この更新により、再雇用されて退職した従業員は退職リストに 1 回のみ表示されます。 

## <a name="known-issue"></a>既知の問題

- **問題**: 作業者に新しい添付ファイルを追加する時、**新規**および**編集**ボタンが灰色表示になります。 
- **回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。 **作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
