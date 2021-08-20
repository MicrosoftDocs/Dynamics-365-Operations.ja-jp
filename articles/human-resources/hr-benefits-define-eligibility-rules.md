---
title: 給付金の適格性ルールおよびポリシーの定義
description: この記事では、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 57bcce908dec0b202880d865bbb6014ae13e385642dc2785b16c33abc4ab53bf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752060"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a>給付金の適格性ルールおよびポリシーの定義

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、給付金の適格性ルールとポリシーを作成する方法、給付金にルールを割り当てる方法を示します。  

## <a name="create-benefit-eligibility-policy-rule-type"></a>給付金の適格性ポリシー ルールのタイプを作成する

1. **人事管理 > 給付金 > 適格性 > 給付金の適格性ポリシー タイプ** の順に移動します。
2. **新規** を選択します。
3. **ルール名** フィールドに値を入力します。
4. **説明** フィールドで値を入力します。
5. **クエリ名** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。
6. 一覧で、選択した行のリンクを選択します。
7. **保存** を選択します。
8. ページを閉じます。

## <a name="benefit-eligibility-policy"></a>給付金の適格性ポリシー

1. **人事管理 > 給付金 > 適格性 > 給付金の適格性ポリシー** の順に移動します。
2. 既存の給付金のポリシーを選択します。
3. 一覧で、選択した行のリンクを選択します。
4. **ポリシーの組織** セクションの展開を切り替えます。 ここでポリシーに追加する組織を追加・削除できます。
5. **ポリシー ルール** セクションを展開または折りたたみます。
6. 一覧で、以前に作成したポリシー ルールを検索します。
7. **ポリシー ルールの作成** を選択します。
8. **有効日** フィールドに、有効にするポリシーの有効日を入力します。
    * 有効な終了日を設定することで、将来的にポリシールールを変更することができるため、変更を有効にしたいときにポリシーへの変更を行う手間が省かれます。  
9. 必要に応じて、**条件の追加** フィールドに 「where 句」 を追加します。
    * たとえば、営業マネージャーのみにルールを適用したい場合は、where 句を作成して次のように記述します : Where ポジションの説明がセールスマネージャーと等しい。 ルール内で複数の where 条件をまとめて追加することができます。  
10. **OK** を選択します。
11. ページを閉じます。

## <a name="assign-rule-to-benefit"></a>ルールに寄付金を割り当てる

1. **人事管理 > 福利厚生 > 福利厚生** の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択した行のリンクを選択します。
4. **適格性ルール** のセクションを展開、または折りたたみます。
5. **編集** を選択します。
6. **適格性** フィールドで、ルールを選択します。
7. **ルール タイプ** フィールドで、以前に作成したルールを選択します。
9. 一覧で、選択した行のリンクを選択します。
10. **保存** を選択します。
11. フォームを閉じます。



[!INCLUDE[footer-include](../includes/footer-banner.md)]