---
title: 作業時間テンプレートの作成
description: 作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ef913777c8e2aa14af21e28ed56362e31b3d70a1a52e988a90ad94f59b77b70
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741264"
---
# <a name="create-working-time-templates"></a>作業時間テンプレートの作成

[!include [banner](../../includes/banner.md)]

作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。 この手順は、作業時間の間隔を分類するための作業時間のスケジューリングのプロパティを使用して作業時間テンプレートを定義する方法について説明します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。

1. **ワークスペース > リソース ライフサイクル管理** の順にクリックします。
1. **作業時間テンプレート** を選択します。

## <a name="create-working-time-template"></a>作業時間テンプレートの作成

1. **新規** を選択します。
1. **作業時間テンプレート** フィールドで、値を入力します。
1. **名前** フィールドに値を入力します。
1. **月曜日** セクションを展開します。
1. **追加** を選択します。
1. **ソース** フィールドに時刻を入力します。
    * 午前の作業開始時間を指定します。  
1. **ターゲット** フィールドに時刻を入力します。
    * 作業者の昼休みの時間を指定します。  
1. **追加** を選択します。
1. **ソース** フィールドに時刻を入力します。
    * 作業が昼食後に再開する時間を指定します。  
1. **ターゲット** フィールドに時刻を入力します。
    * 作業日の終了を指定します。  

## <a name="replicate-working-times-to-all-week-days"></a>作業時間を平日すべてに複製

1. **日数のコピー** を選択します。
    * 月曜日から火曜日まで勤務時間の定義をコピーします。  
1. **OK** を選択します。
1. **日数のコピー** を選択します。
    * 月曜日から水曜日まで勤務時間の定義をコピーします。  
1. **終了日** フィールドで、オプションを選択します。
1. **OK** を選択します。
1. **日数のコピー** を選択します。
    * 月曜日から木曜日まで勤務時間の定義をコピーします。  
1. **終了日** フィールドで、オプションを選択します。
1. **OK** を選択します。
1. **日数のコピー** を選択します。
    * 月曜日から金曜日まで勤務時間の定義をコピーします。  
1. **終了日** フィールドで、オプションを選択します。
1. **OK** を選択します。

## <a name="define-time-slots-for-special-operations"></a>特別工程のタイム スロットを定義

1. **金曜日** セクションを展開します。
1. 一覧で、目的のレコードを見つけ、選択します。
1. **プロパティ** フィールドで、値を入力または選択します。
1. 一覧で、目的のレコードを見つけ、選択します。
1. **プロパティ** フィールドで、値を入力または選択します。

## <a name="mark-weekend-days-as-closed-for-pickup"></a>週末日を払出不可としてマーク

1. **土曜日** セクションを展開します。
1. **払出不可** フィールドで、*はい* を選択します。
1. **日曜日** セクションを展開します。
1. **払出不可** フィールドで、*はい* を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]