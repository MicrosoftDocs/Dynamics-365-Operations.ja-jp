---
title: Budget planning justification documents
description: "両端揃えのドキュメントが特定の予算が必要な理由についてする予算を要求される予定に物語を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Budget planning justification documents

両端揃えのドキュメントが特定の予算が必要な理由についてする予算を要求される予定に物語を提供します。 

予算の計画テンプレートは、Microsoft Wordで予算管理者によって作成され、現在の予算の計画プロセスに割り当てられます。 所有者とテンプレートを開き、自動的に予算の要求に基づいてWordで設定されたデータをとることができます割り当てます。 また、予算の計画に保存およびカスタマイズされた揃えのドキュメントを関連付ける前に追加テキストまたはデータを追加することもできます。

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Wordで展開設定Microsoft Dynamicsのオフィス

1.  Microsoft Wordのドキュメントを開きます。
2.  [**挿入**リボン払、[**店舗**。
3.  展開Microsoft Dynamicsの会社の検索]をクリックして** **追加します。
4.  Wordで、右ウィンドウで、[**サーバーの情報を追加します。**。
5.  入力のみ、またはサーバーURLを貼り付ける、およびクリックして**良い**。

##### <a name="define-the-justification-template-in-microsoft-word"></a>Microsoft Wordの根拠のテンプレートを定義します。

1.  [デザイン** **ログオン後に展開Microsoft Dynamicsの会社の日付。
2.  ヘッダー情報については、**フィールドを追加します**ボタンを使用します。
3.  BudgetPlanJustificationのエンティティのデータ ソースを選択し、をクリックして** [**。 **注記: **このエンティティは、両端揃えのドキュメントに必要です。 他のエンティティが使用できますが、このエンティティが含まれていない場合は、Microsoft Dynamics 365に戻るアップロードが失敗します。
4.  WordドキュメントのDocumentNumber BudgetPlanName、BudgetPlanPreparer、ResponsibilityCenterおよびラベル値と追加します。 **注記: **、標準ラベルをもむしろ分類します (必要な場合)、独自のカスタムを使用できます。
5.  ヘッダー セクションを完了します**可能な**。
6.  予算の金額の明細行レベルの詳細については、" **テーブルを追加します。**。
7.  再度、BudgetPlanJustificationのエンティティのデータ ソースを選択し、をクリックして** [**。
8.  EffectiveDate、ScenarioName、AccountDisplayValueとAccountingCurrencyExpenseAmountのフィールドを追加します。 **注記: **コメントが個別の予算の計画の行に追加して使用できる場合は、表に、ここに追加できます。
9.  エンドユーザーに提供する別の説明値を追加するドキュメントに必要な形式またはスタイルを作成することを実行します。
10. ドキュメントがローカル コンピュータに保存し、次に進みますファイルを閉じます。

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>両端揃えのテンプレートを使用する予算の計画プロセスを設定します。

1.  、Microsoft Dynamics 365では、設定は** ** &gt; ** **割り当てられます) &gt;。**予算の計画** &gt; **揃えのドキュメント テンプレート**。
2.  [**新しいMicrosoft Wordの新しく作成されたドキュメントに**および参照します。
3.  テンプレートの表示名と説明を入力します。 Click **OK**.
4.  **割り当てます** ** &gt; **設定は、&gt; 受信**予算** **計画** &gt; **予算の計画プロセス**。
5.  両端揃えのテンプレートを使用すると]を選択しますプロセス** **編集します。
6.  では**揃えのドキュメント テンプレート**フィールドにつき、適切なテンプレートを選択し、および保存します。

##### <a name="edit-and-save-personalized-justification-documents"></a>カスタマイズされた揃えのドキュメントを編集し、保存します。

1.  Dynamics 365 for Operationsで、新しい予算の計画を作成するか、または既存の予算の計画を開きます。
2.  [**行う**ドロップダウン メニューで**新しい揃えを作成します。**。
3.  **行う**ドロップダウン メニューからのカスタマイズされたドキュメントをアップロードするには、[詳細にデータを入力することになります。



