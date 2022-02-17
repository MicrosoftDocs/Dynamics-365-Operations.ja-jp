---
title: 新しい給付金の作成
description: このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。
author: twheeloc
ms.date: 11/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 222bac97d461cd0a090c3e5d99594c07724818ff
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066979"
---
# <a name="create-a-new-benefit"></a>新しい給付金の作成


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。 このタスクの作成に使用するデモ データの会社は USMF です。 このタスクは、報酬と給付金マネージャーのために用意されています。


## <a name="create-benefit-elements"></a>給付金の要素の作成

1. **人事管理 \> 給付金 \> 設定 \> 給付金の要素** に移動します。
2. **新規** を選択します。
3. **タイプ** フィールドに、作成する福利厚生タイプの名前を入力します。
4. **説明** フィールドで値を入力します。
5. **同時登録** フィールドで、オプションを選択します。

    複数の医療プランに登録する従業員の能力を制限するには、**種類ごとに 1 つの登録** を選択します。

6. **給与カテゴリ** フィールドで、オプションを選択します。
7. **プラン** タブで、**新規** を選択します。
8. **プラン** フィールドに値を入力します。
9. **説明** フィールドで値を入力します。
10. **タイプ** フィールドで、値を入力または選択します。
11. **給与の影響** フィールドで、オプションを選択します。
12. **保存** を選択します。

## <a name="create-a-benefit"></a>給付金の作成

1. **人事管理 \> 福利厚生 \> 福利厚生** の順に移動します。
2. **新規** を選択します。
3. ドロップダウン ダイアログ ボックスの **プラン** フィールドに値を入力するか選択します。
4. **オプション** フィールドで値を入力または選択します。
5. **有効開始** フィールドで、日付と時刻を入力します。
6. **福利厚生の作成** を選択します。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
