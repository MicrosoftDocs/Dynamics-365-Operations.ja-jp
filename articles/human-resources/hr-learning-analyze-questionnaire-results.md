---
title: アンケート結果の分析
description: アンケートの統計情報は、一連の統計データに基づいて平均、合計、割合を計算するために使用できます。
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1da18dd32363308438b7f9da5b2e04e119e840cb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692922"
---
# <a name="analyzing-questionnaire-results"></a>アンケート結果の分析


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



アンケートの統計情報は、一連の統計データに基づいて平均、合計、割合を計算するために使用できます。 この手順を開始するには、**アンケート** > **結果の表示と分析** > **アンケート統計情報** の順に移動します。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="create-a-questionnaire-statistics-record"></a>アンケート統計レコードの作成
1. **アンケートの統計情報** に移動します。
2. **新規** をクリックします。
3. 一覧で、選択された行をマークします。
4. **統計情報** フィールドに値を入力します。
5. **説明** フィールドで、値を入力します。
6. **アンケート** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、選択された行のリンクをクリックします。
8. **一般** タブをクリックします。
    * 匿名結果や作業者の結果、連絡担当者、および申請者を含める場合に選択します。  
9. **作業者** チェック ボックスをオンまたはオフにします。
    * 年齢または勤続年数別に結果を表示する場合、結果をグループ化するのに使用する範囲を指定します。  
    * 年齢間隔に 5 を入力すると、5 才ごとに結果をグループ化します。  
10. **年齢** フィールドに数値を入力します。
    * 各結果グループ、各質問、または各質問別に、全体のアンケートに対して計算を実行する場合に選択します。  
    * 結果をグループ化する方法を選択します。  
    * たとえば、質問ごとに平均ポイントを計算し、結果グループをグループ化することによって質問を表示することをお勧めします。  
    * 計算の基になるデータを選択します。  
    * たとえば、作業者を対象に行ったアンケートの平均割合と作業者間で獲得した平均ポイント数を表示する場合です。  
11. **範囲** タブをクリックします。
    * 範囲の基準を満たすもののみに結果セットを制限して範囲を使用します。  
12. **グループ化** タブをクリックします。
    * グループ化を使用すると、結果を表示する方法を変更できます。  
    * たとえば、最初に性別ごとに、その次に年齢ごとに結果をグループ化します。  
13. 一覧で、目的のレコードを見つけ、選択します。
    * グループを **選択済み** の側に移動して、目的の順序に配置します。  

## <a name="execute-the-statistics-calculation"></a>統計計算の実行
1. **実行** をクリックします。
    * 結果に対して実行する計算機能を選択します。  
    * たとえば、選択したグループ化について、アンケートの平均割合を計算するか、または結果グループのポイントを合計します。  
2. **以前の検索結果を削除** チェック ボックスをオンまたはオフにします。
3. **OK** をクリックします。

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a>アンケート統計の実行結果を表示します。
1. **結果** をクリックします。
2. **結果** をクリックします。
3. ページを閉じます。



[!INCLUDE[footer-include](../includes/footer-banner.md)]
