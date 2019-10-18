---
title: Dynamics 365 Talent (2019 年 4 月 9 日) の新機能や変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
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
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 08f3f8150a120817618ee4d31197f3088c7483ab
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024094"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-9-2019"></a>Dynamics 365 Talent (2019 年 4 月 9 日) の新機能や変更された機能

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>「問題の報告」と Lifecycle Services (LCS) の統合
Attract と Onboard では、問題をレポートする機能を使用してエンドユーザーによって記録された問題は、顧客の LCS プロジェクトでサポートの問題を自動的に作成するようになりました。 その後、管理者は問題をトリアージし、必要に応じて Microsoft に送信することができます。 これは、Core HR がエンド ユーザーのサポートの問題を処理する方法と一致しています。

### <a name="relevance-search"></a>関連情報の検索
人材プールで、特定のスキル、名前、または学歴について候補データベース全体を検索できるようになりました。 候補者プロファイルの検索したいセクションを指定する必要がなくなりました。 Attract はプロファイル全体を検索し、すべての一致した項目を強調表示します。 Attract はまた、候補者に利用可能なすべてのドキュメントを検索し、検索結果をインテリジェントにランク付けします。 さらに、検索結果をソース別、または銀メダリストかどうかでフィルター処理することもできます。 詳細については、[候補者プロファイルの検索および表示](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles) を参照してください。

### <a name="prospect-recommendations"></a>候補者の推奨事項
Attract は、組織の候補者データベースからインテリジェントな候補者の推奨事項を作成することで、有効にするとすぐ職務の調達に弾みをつけるのに役立ちます。 推奨事項には、関連する候補者を検索する際に特定されたスキルと教育情報が含まれます。 職務の採用プロセスで有効にした場合、これらの推奨事項は職務の下の**候補者**タブに表示されます。 詳細については、[候補者の推奨事項](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations)を参照してください。

### <a name="interviewer-availability-statuses"></a>面接者の使用可能状態
面接スケジューラは面接者が効率よく働くために時間をスケジュールするのに役立つ、**外出中、他の場所からの作業**ステータスを表示するようになります。

### <a name="candidate-interview-experience-save-calendar-invites"></a>候補者の面接経験: カレンダーの招待を保存
候補者は、候補者に送信された面接の概要の電子メールに添付されている .ics ファイルを使用して、自分の個人カレンダーに面接イベントをダウンロードして保存できるようになりました。

## <a name="changes-in-onboard"></a>Onboard の変更

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>問題の報告と Lifecycle Services (LCS) の統合
Attract と Onboard では、問題をレポートする機能を使用してエンドユーザーによって記録された問題は、顧客の LCS プロジェクトでサポートの問題を自動的に作成するようになりました。 その後、管理者は問題をトリアージし、必要に応じて Microsoft に送信することができます。 これは、Core HR がエンド ユーザーのサポートの問題を処理する方法と一致しています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2225 に適用されます。

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>基準の割合変動プランが誤った金額を読み込む
今週のリリースでは、基準プランの割合を使用して変動報酬報酬を読み込む際の問題が修正されました。
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>最終勤務日の日付の選択が正しく動作しません
この変更により、次の問題を修正 : ユーザーが**雇用の終了日**を編集し、カレンダーの管理を使用して日付を選択すると、選択に日付が追加されます。

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>行なわれるアクションによる個人のアクション タイプを制限する
この変更により、特定のアクションを実行するときに表示されるアクション タイプが制限されます。 たとえば、新しい職位が要求されると、選択するアクションの一覧に新しい職位アクションのみが表示されます。 以前は、新規アクションと編集アクションの両方が表示されていました。 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>第 2 の法人の従業員の報酬を転送
今回のリリースでは、転送が会社間転送である場合、第 2 の法人で補償が終了するようになりました。

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>転送中に雇用の予定の報酬を選択できません
従業員を新しい法人に転送するとき、転送プロセス中に新しい法人の報酬を設定できるようになりました。

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>ユーザーは職位の割り当て中に報酬を割り当てることができません
新しい職務割り当てを追加すると、固定報酬レコードを設定できるようになりました。 

## <a name="in-preview"></a>プレビュー

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>理由コードを休暇タイプに指定できるようにする
組織は、休暇申請に関する追加情報が必要な場合があります。 休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>休暇申請で特定の休暇タイプに理由コードが必要
従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 これは、会社の方針または規制要件が原因である可能性があります。 どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します。
従業員の休暇を追跡し、どのように計算するかを理解することにより、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇の付与ができるようになります。 HR は、残高の背後にある理由を確認するための、トランザクション (交付、見越、調整、および要求) の表示が新しくなりました。 

## <a name="coming-soon"></a>間もなく公開

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>重複する従業員チェックのためのユーザー インターフェイスの改良
この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するために、重複フォームは自動的に開きません。

###  <a name="email-support-for-alerts"></a>アラートの電子メールサポート
Finance and Operations のプラットフォーム更新プログラム 25 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。 
