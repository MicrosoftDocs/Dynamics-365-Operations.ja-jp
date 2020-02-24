---
title: 休暇計画の累計
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 28b7d843d9dd652e45c24af09d0414530c06c4ac
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009659"
---
# <a name="accrue-leave-and-absence-plans"></a>休暇計画の累計

Dynamics 365 Human Resources において、複数の従業員または個々の従業員の休暇を累計することができます。

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>複数の従業員の休暇を累計する

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **休暇の管理**で、**休暇計画の累計**を選択します。

3. **休暇計画の累計**ダイアログ ボックス内の**累計の時点**で、**今日の日付**を選択するか、または**カスタム日付**を選択しカスタム日付を入力します。

4. バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。

   1. 累計処理の情報を入力します。

   2. 定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメーターで累計処理が実行されます。

## <a name="accrue-leave-and-absence-for-an-employee"></a>個々の従業員の休暇を累計する

1. 従業員のレコードで、**休暇**を選択します。

2. **休暇の累計**を選択します。

3. **休暇計画の累計**ダイアログ ボックス内の**累計の時点**で、**今日の日付**を選択するか、または**カスタム日付**を選択しカスタム日付を入力します。

4. バックグラウンドで累計処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。

   1. 累計処理の情報を入力します。

   2. 定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメーターで累計処理が実行されます。

## <a name="preview-features-for-leave-and-absence"></a>休暇のためのプレビュー機能

[!include [banner](includes/preview-feature-leave-absence.md)]

休暇のために、次のプレビュー機能を有効にできます。

- **休暇の発生を削除します**。 特定の計画や日付範囲に対する発生レコードを削除します。 発生日は今日または将来の日付にする必要があります。

- **休暇発生の監査**。 1 人またはすべての従業員の休暇発生が実行または削除されるたびに、アクションを実行した日付および人物と共にそれが表示されます。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇計画の作成](hr-leave-and-absence-plans.md)