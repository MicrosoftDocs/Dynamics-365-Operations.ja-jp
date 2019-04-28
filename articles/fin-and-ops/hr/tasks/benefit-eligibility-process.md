---
title: 給付金適格性処理
description: この手順は、給付金適格性処理が機能する方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b842d76d2c02b7f5daa45c5a34c8f61029f6c035
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "855635"
---
# <a name="benefit-eligibility-process"></a>給付金適格性処理

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、給付金適格性処理が機能する方法を示します。 プロセスが完了すると、結果を表示できます。 この手順の作成に使用するデモ データの会社は USMF です。

1. [人事管理] > [福利厚生] > [福利厚生] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. [編集] をクリックします。
5. [適格性] フィールドで、「ルール ベース」を選択します。
6. [ルール タイプ] フィールドで、福利厚生に適用する福利厚生のポリシー ルールを選択します。
7. [アクション] ウィンドウで、[福利厚生] をクリックします。
8. [適格性イベントの作成] をクリックして、ドロップ ダイアログを開きます。
9. [イベント] フィールドに値を入力します。
10. [説明] フィールドで値を入力します。
11. [イベント タイプ] フィールドで、「未処理の登録」を選択します。
12. [適用開始日] フィールドで、日時を入力します。
13. [登録期間の開始日] フィールドで、日時を入力します。
14. [登録するまでの日数] フィールドに、数値を入力します。
15. [イベントの作成] をクリックします。
16. [作業者のクイックタブに追加] をクリックします。
17. [タイプ別に表示] フィールドで「従業員」を選択します。
18. [法人別に表示] フィールドで、「現在の法人」を選択します。
19. 一覧で、すべての行のマークを設定または解除します。
20. [OK] をクリックします。
21. [プロセス] をクリックします。
22. [OK] をクリックします。
23. ページを更新します。
24. [結果の表示] をクリックします。
25. [ステータス列フィルター] を開きます。
26. 昇順で並べ替え

