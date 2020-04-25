---
title: 休暇計画の見越計上
description: Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3048f9b6b52a150219067430abb54e5b5bf5c3e4
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197316"
---
# <a name="accrue-leave-and-absence-plans"></a>休暇計画の見越計上

Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>複数の従業員の休暇を累計する

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **休暇の管理**で、**休暇計画の累計**を選択します。

3. **休暇計画の累計** ダイアログ ボックスが表示されます。 **累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。

4. バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。

   1. 累計処理の情報を入力します。

   2. 定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメーターで累計処理が実行されます。

## <a name="accrue-leave-and-absence-for-an-employee"></a>個々の従業員の休暇を累計する

1. 従業員のレコードで、**休暇**を選択します。

2. **休暇の累計**を選択します。

3. **休暇計画の累計** ダイアログ ボックスが表示されます。 **累計の時点** で、**今日の日付** を選択するか、**カスタム日付** を選択しカスタム日付を入力します。

4. バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。

   1. 累計処理の情報を入力します。

   2. 定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメーターで累計処理が実行されます。

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>複数従業員の休暇の発生を削除する

特定の計画や日付範囲に対する発生レコードを削除します。 発生日は今日または将来の日付にする必要があります。

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **休暇の管理**で、**休暇計画の累計の削除** を選択します。

3. **休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。 

4. 該当する場合は、**残日数調整の削除** を選択します。

5. **有給休暇付与日** を入力または選択します。 この日付は、今日または将来のいずれかでなければなりません。 

6. **OK** を選択します。 累計処理では、設定したパラメーターで発生を削除します。 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>単一従業員の休暇の発生を削除する

1. 従業員のレコードで、**休暇**を選択します。

2. **休暇計画の累計の削除** を選択します。

3. **休暇計画の累計の削除** ダイアログ ボックスで、**休暇計画** を選択します。 

4. 該当する場合は、**残日数調整の削除** を選択します。

5. **有給休暇付与日** を入力または選択します。 この日付は、今日または将来のいずれかでなければなりません。 

6. **OK** を選択します。 累計処理では、設定したパラメーターで発生を削除します。 

## <a name="review-leave-accrual-and-deletion-processes"></a>休暇の発生および削除プロセスの確認

**休暇発生の監査** は、1 人またはすべての従業員の発生を実行または削除するたびに表示されます。 アクションを実行した日付と担当者も表示されます。

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **休暇の管理**で、**休暇発生の監査の削除** を選択します。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇および欠勤計画の作成](hr-leave-and-absence-plans.md)
