---
title: 休暇パラメーターのコンフィギュレーション
description: Dynamics 365 Human Resources で休暇のための人事管理パラメーターを定義します。
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
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009657"
---
# <a name="configure-leave-and-absence-parameters"></a>休暇パラメーターのコンフィギュレーション

Dynamics 365 Human Resources で休暇計画を設定する前に、下記を含むすべての関連する人事管理パラメーターの設定を確認することをお勧めします。

- 休暇申請の番号順序
- 育児介護休業法 (FMLA) 設定
- 休暇申請のための従業員セルフ サービス設定
- 休暇および欠勤パラメーター

## <a name="view-and-change-human-resources-parameters"></a>人事管理パラメーターの表示および変更

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **設定**で、**人事管理パラメーター**を選択します。

3. **番号順序**タブで、**休暇申請 ID** のための**番号順序コード**を確認し、必要に応じて変更します。 この設定により、休暇申請に自動的に ID を割り当てるために使用される順序が決まります。

4. **FMLA** タブで、FMLA の設定を確認し必要に応じて変更します。

5. **従業員セルフ サービス** タブで、マネージャーが従業員に代わって休暇申請を入力できるようにするかどうかを指定します。

6. **休暇**タブで設定を確認し、必要に応じて変更します。

7. **保存** を選択します。

## <a name="configure-calendar-parameters"></a>カレンダー パラメーターのコンフィギュレーション

休暇カレンダー プレビュー機能を有効にした場合、追加のパラメータをコンフィギュレーションする必要があります。 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> 2020 年 2 月 3 日のプレビュー リリースでは、**保留中の休暇申請**のみ有効になっています。

1. **休暇および欠勤**のページで、**リンク** タブを選択します。

2. **設定**で、**人事管理パラメーター**を選択します。

3. **カレンダー** タブで、カレンダーの設定を必要に応じて変更します。

4. **保存** を選択します。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
