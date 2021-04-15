---
title: 作業時間カレンダーの作成
description: Dynamics 365 Human Resources で、作業時間カレンダー、休日、および非作業時間を定義します。
author: andreabichsel
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67b951cccae7708f8d831ff1d83738dc49360a48
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794520"
---
# <a name="create-a-working-time-calendar"></a>作業時間カレンダーの作成

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources で、作業時間カレンダーには、組織内で従業員が勤務している日数と時間が表示されます。 従業員が休暇申請を提出した場合、休日や休業日を気にする必要はありません。

休暇申請を効率化するには、組織に対して次の項目を構成します。

- 作業時間カレンダー
- 休日および休業日
- 非作業時間

最後の 2 つの項目は、作業時間カレンダーを設定している間に追加できます。 個別に構成または更新を行うこともできます。

## <a name="set-up-a-working-time-calendar"></a>作業時間カレンダーの設定

作業日数と時間を示す、少なくとも 1 つの作業時間カレンダーを設定します。 複数の国や地域に拠点がある場合は、それぞれの拠点に対して作業時間カレンダーを設定することもできます。

1. **組織管理** ページで、**カレンダー** を選択します。

2. **新規** を選択し、カレンダーに名前と説明を入力します。

3. **生成オプション** で、組織の作業日数を選択し、作業時間を入力します。 
   - 休日または休業日を追加するには、**休日および休業日** の横にある **追加** ボタンを選択します。
   - 昼食や休憩などの非作業時間を追加するには、**非作業時間** で **追加** を選択し、名前と時間の範囲を入力します。

4. **日数** で、**生成** を選択して、カレンダーに日数を生成します。 カレンダーに日付範囲を入力し、**日数の生成** を選択します。

5. 作業スケジュールを追加するには、**作業スケジュール** で、**追加** を選択し、各作業スケジュールに時刻を入力します。

## <a name="configure-holidays-and-closures"></a>休日および休業日の構成

休日および休業日は、作業時間カレンダーから個別に追加または変更できます。

1. **組織管理** ページで、**休日および休業日** を選択します。

2. **新規** を選択し、休日および休業日に名前と日付を入力します。

## <a name="configure-non-work-time"></a>非作業時間の構成

非作業時間は、作業時間カレンダーから個別に追加または変更できます。

1. **組織管理** ページで、**非作業時間** を選択します。

2. **新規** を選択し、非作業時間に名前と時間範囲を入力します。

休暇および欠勤の休日の修正プレビュー機能を有効にした場合、Human Resources は休日と休業日を使用して、カレンダーに登録されている従業員に対して調整する日数を決定します。

## <a name="see-also"></a>参照

- [休暇の概要](hr-leave-and-absence-overview.md)
- [休暇タイプのコンフィギュレーション](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]