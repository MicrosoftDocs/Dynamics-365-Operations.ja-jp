---
title: 給付金適格性処理
description: この手順は、給付金適格性処理が機能する方法を示します。
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: db8dd3e9c3401129ea5474d47f5401c552cab72b
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771385"
---
# <a name="benefit-eligibility-process"></a>給付金適格性処理

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この手順は、給付金適格性処理が機能する方法を示します。 プロセスが完了すると、結果を表示できます。 この手順の作成に使用するデモ データの会社は USMF です。

1. **人事管理 \> 福利厚生 \> 福利厚生** の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択した行のリンクを選択します。
4. **編集** を選択します。
5. **適格性** フィールドで、**ルール ベース** を選択します。
6. **ルール タイプ** フィールドで、福利厚生に適用する福利厚生のポリシー ルールを選択します。
7. アクション ウィンドウで、**福利厚生** を選択します。
8. **適格性イベントの作成** を選択します。
9. ドロップダウン ダイアログ ボックスの **イベント** フィールドに値を入力します。
10. **説明** フィールドで値を入力します。
11. **イベント タイプ** フィールドで、**未処理の登録** を選択します。
12. **適用開始日** フィールドで、日時を入力します。
13. **登録期間の開始日** フィールドで、日時を入力します。
14. **登録するまでの日数** フィールドに、数値を入力します。
15. **イベントの作成** を選択します。
16. **作業者** クイック タブで、**追加** を選択します。
17. **タイプ別に表示** フィールドで **従業員** を選択します。
18. **法人別に表示** フィールドで、**現在の法人** を選択します。
19. 一覧で、すべての行のマークを設定または解除します。
20.  **OK** を選択します。
21. **プロセス** を選択します。
22.  **OK** を選択します。
23. ページを更新します。
24. **結果を表示** を選択します。
25. **ステータス** 列フィルターを開きます。
26. 列を A から Z の順に並べ替えます。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
