---
title: カレンダーの作成および作業時間の生成
description: カレンダーは、運営リソースの能力と作業時間を説明します。 この記事は、作業時間テンプレートに基づいて作業カレンダーを定義する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5c630297a8962d1bb383110881b2acdc872b9cd
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826100"
---
# <a name="create-calendars-and-generate-working-times"></a>カレンダーの作成および作業時間の生成



カレンダーは、運営リソースの能力と作業時間を説明します。 この記事は、作業時間テンプレートに基づいて作業カレンダーを定義する方法について説明します。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。

1. ホーム ページで、**リソース ライフサイクル管理**を選択します。
2. **カレンダー**を選択します。
3. **新規** を選択します。
4. **カレンダー** フィールドで、カレンダーを分類します。 これは、運営リソースまたはリソース グループなどのカレンダーを割り当てるときに参照として使用されるカレンダーの ID です。  
5. **名前**フィールドで、カレンダーに名前を付けます。
6. **標準作業日 (時)** で、数値を入力します。
7. 行が選択されていることを確認し、アクション ウィンドウから**作業時間**を選択します。
8. **作業時間の作成**を選択します。 作業をスケジュールできる期間のそれぞれの日の勤務時間を生成します。 徐々に、その他の期間にも勤務時間生成することができるようになります。  
9. **開始日**フィールドに日付を入力します。 このカレンダーがオープンになっている必要がある最初の日です。  
10. **終了日**フィールドに日付を入力します。 このカレンダーがオープンになっている最後の日です。  
11. **作業時間テンプレート** フィールドで、値を入力または選択します。 作業時間テンプレートは曜日ごとの勤務時間を定義します。  
12. **OK** を選択します。
13. ページを閉じます。

