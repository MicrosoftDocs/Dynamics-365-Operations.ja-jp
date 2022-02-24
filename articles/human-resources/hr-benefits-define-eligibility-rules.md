---
title: 給付金の適格性ルールおよびポリシーの定義
description: この記事では、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419364"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>給付金の適格性ルールおよびポリシーの定義

この記事では、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。  

この記録の作成に使用するデモ データの会社は USMF です。


## <a name="create-benefit-eligibility-policy-rule-type"></a>給付金の適格性ポリシー ルールのタイプを作成する
1. [人事管理] > [給付金] > [適格性] > [給付金の適格性ポリシー タイプ] の順に移動します。
2. [新規] をクリックします。
3. [ルール名] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [クエリ名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
7. [保存] をクリックします。
8. ページを閉じます。

## <a name="benefit-eligibility-policy"></a>給付金の適格性ポリシー
1. [人事管理] > [給付金] > [適格性] > [給付金の適格性ポリシ] の順に移動します。
2. 既存の給付金のポリシーを選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [ポリシーの組織] セクションの展開を切り替えます。  ポリシーに追加する組織をここで追加、または削除できます。
5. [ポリシー ルール] のセクションを展開または折りたたみます。
6. 一覧で、以前に作成したポリシー ルールを検索します。
7. [ポリシー ルールの作成] をクリックします。
8. [有効日] フィールドに、有効にするポリシーの有効日を入力します。
    * 有効日と終了日の設定により、ポリシー ルールを修正でき、それらの変更を有効化するときに、ポリシーへの変更を行う手間が省かれます。  
9. 
    * たとえば、販売マネージャにのみルールを適用する場合、職位は販売マネージャーであることを説明する [Where] 句を作成できます。  ルールでは、複数の [Where] ステートメントを AND と OR で結合して使用できます。  
10. [OK] をクリックします。
11. ページを閉じます。
12. ページを閉じます。

## <a name="assign-rule-to-benefit"></a>ルールに寄付金を割り当てる
1. [人事管理] > [福利厚生] > [福利厚生] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [適格性ルール] のセクションを展開または折りたたみます。
5. [編集] をクリックします。
6. [適格性] フィールドで、「ルール ベース」を一覧から選択します。
7. [ルール タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、以前に作成したルールを検索し、選択します。
9. 一覧で、選択された行のリンクをクリックします。
10. [保存] をクリックします。
11. フォームを閉じます。

