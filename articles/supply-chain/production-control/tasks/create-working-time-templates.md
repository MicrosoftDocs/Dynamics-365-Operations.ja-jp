---
title: 作業時間テンプレートの作成
description: 作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5bd1b384fe66dd7d59b776bdf1154cc5b8262ce
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826527"
---
# <a name="create-working-time-templates"></a>作業時間テンプレートの作成

[!include [banner](../../includes/banner.md)]

作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。 この手順は、作業時間の間隔を分類するための作業時間のスケジューリングのプロパティを使用して作業時間テンプレートを定義する方法について説明します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。

1. [すべてのワークスペース] > [リソース ライフサイクル管理] の順に移動します。
2. [作業時間] テンプレートをクリックします。

## <a name="create-working-time-template"></a>作業時間テンプレートの作成
1. [新規] をクリックします。
2. [作業時間テンプレート] フィールドで、値を入力します。
3. [名前] フィールドに値を入力します。
4. [月曜日] セクションを展開します。
5. [追加] をクリックします。
6. [ソース] フィールドに時刻を入力します。
    * 午前の作業開始時間を指定します。  
7. [ターゲット] フィールドに時刻を入力します。
    * 作業者の昼休みの時間を指定します。  
8. [追加] をクリックします。
9. [ソース] フィールドに時刻を入力します。
    * 作業が昼食後に再開する時間を指定します。  
10. [ターゲット] フィールドに時刻を入力します。
    * 作業日の終了を指定します。  

## <a name="replicate-working-times-to-all-week-days"></a>作業時間を平日すべてに複製
1. [日数のコピー] をクリックします。
    * 月曜日から火曜日まで勤務時間の定義をコピーします。  
2. [OK] をクリックします。
3. [日数のコピー] をクリックします。
    * 月曜日から水曜日まで勤務時間の定義をコピーします。  
4. [終了日] フィールドで、オプションを選択します。
5. [OK] をクリックします。
6. [日数のコピー] をクリックします。
    * 月曜日から木曜日まで勤務時間の定義をコピーします。  
7. [終了日] フィールドで、オプションを選択します。
8. [OK] をクリックします。
9. [日数のコピー] をクリックします。
    * 月曜日から金曜日まで勤務時間の定義をコピーします。  
10. [終了日] フィールドで、オプションを選択します。
11. [OK] をクリックします。

## <a name="define-time-slots-for-special-operations"></a>特別工程のタイム スロットを定義
1. [金曜日] セクションを展開します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [プロパティ] フィールドで、値を入力または選択します。
4. 一覧で、目的のレコードを見つけ、選択します。
5. [プロパティ] フィールドで、値を入力または選択します。

## <a name="mark-weekend-days-as-closed-for-pickup"></a>週末日を払出不可としてマーク
1. [土曜日] セクションを展開します。
2. [払出不可] フィールドで [はい] を選択します。
3. [日曜日] セクションを展開します。
4. [払出不可] フィールドで [はい] を選択します。

