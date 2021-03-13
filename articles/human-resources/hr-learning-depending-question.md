---
title: 前の質問の回答に応じた質問の作成
description: 条件付き質問は、前の質問に対する回答に基づいて、回答者に提供するフォローアップの質問を指定することを可能にします。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67dac872d6dc3a5046f5d554b1f185aa6607d193
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115007"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>前の質問の回答に応じた質問の作成



条件付き質問は、前の質問に対する回答に基づいて、回答者に提供するフォローアップの質問を指定することを可能にします。 たとえば、「コーヒーまたは紅茶を選択するか」と質問する場合、回答者がコーヒーまたは紅茶のどちらを回答に選ぶかによって、論理的なフォローアップ質問が特定されます。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="find-the-existing-questionnaire"></a>現在のアンケートを見つけます。
1. [アンケート] > [設計] > [アンケート] の順に移動します。
2. 一覧で、「WorkFH questionnaire」を選択します。

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>すべての質問と副質問をアンケートに追加する
1. [質問] をクリックします。
2. [新規] をクリックします。
3. [質問] フィールドで、質問番号「00016」を選択します。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. [保存] をクリックします。
7. ページを閉じます。

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>アンケート順序を条件に設定し、適切な質問を要求する質問を作成します。
1. [編集] をクリックします。
2. [設定] セクションを展開します。
3. [質問の順序] フィールドで、「00016」を選択します。
4. [条件付き質問] をクリックします。
5. ツリーで、「質問\以前の質問に対してなぜそのように回答したかを説明してください。」を選択します。
6. 主質問フィールドで、質問「00009」を選択する
7. 一覧で、選択された行のリンクをクリックします。
8. [回答] フィールドに、質問が依存する回答オプションの回答順序 ID を入力します。 たとえば、最初の回答オプションについて、「1」を入力します。
9. [保存] をクリックします。
10. ツリーで、「質問\自分の作業に対して公正な給料をもらっている」を選択します。
    * 依存関係を表示する更新された質問ツリーに注意します。  

