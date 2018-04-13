--- 
title: "スケジューリングを使用したアンケートの配布"
description: "アンケートのスケジューリングによって、複数の回答者に対するアンケートを計画して配布することができます。"
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63a02a64ff28531bae950f1b61d9167eaa0b0373
ms.openlocfilehash: 8dd7365a18f371694f21a19efca76bd3e29ed641
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2017

---
# <a name="distribute-questionnaires-using-scheduling"></a>スケジューリングを使用したアンケートの配布

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

アンケートのスケジューリングによって、複数の回答者に対するアンケートを計画して配布することができます。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-a-questionnaire-schedule"></a>アンケートのスケジューリングの作成
1. [アンケート] > [配分] > [アンケートのスケジュール] の順に移動します。
2. [新規] をクリックします。
3. [スケジューリング] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
    * 応答に関連付けられた名前を使わずに応答を記録する場合、スケジュールを [匿名] に設定します。  
    * 匿名結果を許可するには、最初に HR パラメータで設定する必要があります。  
5. [タイプ] フィールドで、計画タイプを選択します。  この例では、Satisfaction タイプを使用します。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. [日付] フィールドに日付を入力します。
9. 従業員セルフサービス セクションの電子メールを展開します。
10. [件名] フィールドに値を入力します。
    * 例: アンケートの対象  
11. [テキスト] フィールドで、電子メールメッセージの本文を入力します。 変数は、システム内の値を置換するために使用できることに注意してください。
    * 例:   %P% 様、従業員セルフサービスにログインして、従業員の健康アンケートを完了してください。  Contoso  
12. [保存] をクリックします。

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>[設定の詳細] を使用して、回答対象のアンケートと回答者を選択するために使用するクエリを選択します。
1. [設定の詳細] をクリックします。
2. リストから、アンケートの回答者を検索するのに使用するクエリを選択します。
    * 例: 作業者  
3. [表示] をクリックするか、クエリを変更して特定のユーザーを選択するか、クエリを調整して特定の基準に一致する従業員を検索します。
    * すべての回答者が、システム内のユーザーである必要があることに注意してください。  
4. 一覧で、Person の行をマークします。
5. [基準] フィールドで、値を入力または選択します。
    * Julia Funderburk を選択  
6. リストで、Julia Funderburk を選択
7. [OK] をクリックします。
8. [アンケート] タブをクリックします。
9. ツリーで、「アンケート タイプ Satisfaction Survey のノード」を展開します。
10. ツリーで、「従業員の健康評価」をチェックします。
11. [OK] をクリックします。
12. [計画済回答セッション] をクリックします。
    * [計画済回答セッション] が、それぞれの選択または質問されたユーザーに対して作成されたことに注意してください。  
13. ページを閉じます。

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>アンケートのスケジュールを開始して、回答者がアンケートを完了できるようにします。
1. [機能] をクリックします。
2. [開始] をクリックします。
3. [OK] をクリックします。

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>使用できるアンケートを回答者に通知する電子メールを送信します。
1. [機能] をクリックします。
2. [電子メールの送信] をクリックします。
3. [キャンセル] をクリックします。

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>[計画済回答セッション] を使用して、アンケートを完了する必要がある人を監視します。
1. [計画済回答セッション] をクリックします。
    * 予定セッションを終了する準備ができたら、残りの計画済回答セッションを削除します。  
2. [削除] をクリックします。
3. [はい] をクリックします。
4. ページを閉じます。

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>すべての回答者がアンケートを完了し、および/または残りのすべての計画済回答セッションが削除されたときに、スケジュールを終了します。
1. [機能] をクリックします。
2. [終了] をクリックします。
3. [OK] をクリックします。


