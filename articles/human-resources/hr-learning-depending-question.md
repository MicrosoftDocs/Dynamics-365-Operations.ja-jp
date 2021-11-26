---
title: 前の質問の回答に応じた質問の作成
description: 条件付き質問は、前の質問に対する回答に基づいて、回答者に提供するフォローアップの質問を指定することを可能にします。
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11787aa0b32c0d7493e4528b00304e51f01a655f
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728909"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>前の質問の回答に応じた質問の作成

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



条件付き質問は、前の質問に対する回答に基づいて、回答者に提供するフォローアップの質問を指定することを可能にします。 たとえば、「コーヒーまたは紅茶を選択するか」と質問する場合、回答者がコーヒーまたは紅茶のどちらを回答に選ぶかによって、論理的なフォローアップ質問が特定されます。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="find-the-existing-questionnaire"></a>現在のアンケートを見つけます。
1. **アンケート** > **設計** > **アンケート** の順に移動します。
2. 一覧で、「WorkFH questionnaire」を選択します。

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>すべての質問と副質問をアンケートに追加する
1. **質問** をクリックします。
2. **新規** をクリックします。
3. **質問** フィールドで、質問番号「00016」を選択します。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. **保存** をクリックします。
7. ページを閉じます。

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>アンケート順序を条件に設定し、適切な質問を要求する質問を作成します。
1. **編集** をクリックします。
2. **設定** セクションを展開します。
3. **質問の順序** フィールドで、「条件付」を選択します。
4. **条件付き質問** をクリックします。
5. ツリーで、「質問\以前の質問に対してなぜそのように回答したかを説明してください。」を選択します。
6. **主質問** フィールドで、質問「00009」を選択します。
7. 一覧で、選択された行のリンクをクリックします。
8. **回答** フィールドに、質問が依存する回答オプションの回答順序 ID を入力します。 たとえば、最初の回答オプションについて、「1」を入力します。
9. **保存** をクリックします。
10. ツリーで、「質問\自分の作業に対して公正な給料をもらっている」を選択します。
    * 依存関係を表示する更新された質問ツリーに注意します。  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
