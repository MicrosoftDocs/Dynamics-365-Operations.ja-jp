---
title: 予算計画の妥当性ドキュメント
description: 妥当性ドキュメントは、予算を要求する人物に対して特定の予算が必要な理由の記述を提供します。
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5eb74b5d2b71372f99dd927ff6e2bee96e199a6f75b3ae920607e5ec37a4241a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752969"
---
# <a name="budget-planning-justification-documents"></a>予算計画の妥当性ドキュメント

[!include [banner](../includes/banner.md)]

妥当性ドキュメントは、予算を要求する人物に対して特定の予算が必要な理由の記述を提供します。 

予算計画テンプレートは、Microsoft Word で予算管理者によって作成され、現在の予算計画プロセスに割り当てられます。 予算の所有者はテンプレートを開き、予算の要求に基づいて Word に自動的にデータを設定できます。 カスタマイズされた妥当性ドキュメントの保存および予算計画への関連付けを行う前に、追加のテキストやデータを追加できます。

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Word 用 Microsoft Dynamics Office アドインの設定

1.  新規の Microsoft Word 文書を開きます。
2.  リボンの **挿入** をクリックして、**ストア** をクリックします。
3.  Microsoft Dynamics アドインを検索して、**追加** をクリックします。
4.  Word の右ウィンドウで、**サーバー情報の追加** をクリックします。
5.  サーバー URL を入力するか貼り付けて、**OK** をクリックします。

##### <a name="define-the-justification-template-in-microsoft-word"></a>Microsoft Word での妥当性テンプレートの定義

1.  ログイン後、Microsoft Dynamics Office アドインの **デザイン** をクリックします。
2.  ヘッダー情報については、**フィールドの追加** ボタンを使用します。
3.  BudgetPlanJustification のエンティティ データ ソースを選択して、**次へ** をクリックします。 **注記:** このエンティティは、どの妥当性ドキュメントにも必要です。 他のエンティティを使用できますが、このエンティティが含まれていない場合は、Microsoft Dynamics 365 Finance に戻るアップロードが失敗します。
4.  Word ドキュメントの BudgetPlanName、BudgetPlanPreparer、ResponsibilityCenter、DocumentNumber のラベルと値を追加します。 **注記:** 必要であれば、標準ラベルではなく独自のカスタム ラベルを使用できます。
5.  **完了** をクリックして、ヘッダー セクションを完了します。
6.  予算計画金額の明細行レベルの詳細については、**テーブルの追加** をクリックします。
7.  再度、BudgetPlanJustification のエンティティ データ ソースを選択して、**次へ** をクリックします。
8.  EffectiveDate、ScenarioName、AccountDisplayValue、AccountingCurrencyExpenseAmount のフィールドを追加します。 **注記:** コメントが個別の予算計画明細行内で使用できる場合、ここのテーブルに追加できます。
9.  エンド ユーザーに提示する説明をさらに追加して、ドキュメントに必要な書式やスタイルを実行します。
10. ドキュメントをローカル コンピューターに保存し、ファイルを閉じてから次に進みます。

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>妥当性テンプレートを使用するための予算計画プロセスの設定

1.  **予算作成** &gt; **設定** &gt; **予算計画** &gt; **妥当性ドキュメント テンプレート** の順に移動します。
2.  **新規** をクリックして、新しく作成された Microsoft Word 文書を参照します。
3.  テンプレートの表示名と説明を入力します。 **OK** をクリックします。
4.  **予算作成** &gt; **設定** &gt; **予算** **計画** &gt; **予算計画プロセス** の順に移動します。
5.  妥当性テンプレートを使用する必要があるプロセスを選択して、**編集** をクリックします。
6.  **妥当性ドキュメント テンプレート** フィールドで、適切なテンプレートを選択して保存します。

##### <a name="edit-and-save-personalized-justification-documents"></a>カスタマイズされた妥当性ドキュメントの編集および保存

1.  新しい予算計画を作成するか、既存の予算計画を開きます。
2.  **妥当性** ドロップダウン メニューで、**妥当性の新規作成** を選択します。
3.  詳細を入力した後、**妥当性** ドロップダウン メニューからカスタマイズされたドキュメントを選択してアップロードします。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]