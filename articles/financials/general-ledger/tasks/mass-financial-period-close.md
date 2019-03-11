---
title: 財務期間一括終了
description: この手順では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2988b7ab0837cc9a3e4f1c4eaf3fe6e219fa721
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "311384"
---
# <a name="mass-financial-period-close"></a>財務期間一括終了

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。 またこのタスクは、特定のモジュールに転記されたユーザー グループを制限する方法を示します。

1. [総勘定元帳] > [期間の締め] > [元帳カレンダー] の順に移動します。
    * 表示された法人の一覧は、ページで選択した会計カレンダーに依存することに注意してください。 選択された会計カレンダーを使用する法人のみが表示されます。  
2. [編集] をクリックします。
3. 状態を変更する期間を選択します。
4. 状態を更新する法人を選択します。
    * グリッドの左上のチェック マークを選択することにより、すべての法人をすばやく選択できます。  
5. [モジュール アクセスの更新] を選択して、選択されたモジュールへのアクセスの転記を定義します。
    * モジュールの状態は、グリッドのレコードを編集することにより順番に更新できます。 ボタンは、複数の法人のレコードをすばやく更新する場合に役に立ちます。  
6. [アプリケーション モジュール] フィールドで、状態を更新するモジュールを選択します。 [選択] をクリックします。
7. [アクセス レベル] で、[すべて]、[なし]、または特定のユーザー グループを選択します。 [選択] をクリックします。
    * [すべて] は、オープン期間の場合、モジュールの編集アクセス許可を持つすべてのユーザーが転記できることを示します。 [なし] は、オープン期間の場合、ユーザーがモジュールに転記できないことを示します。 [特定のユーザー グループ] は、オープン期間の場合に、このグループのユーザーのみがモジュールに転記できることを示します。  
8. [更新] をクリックします。
9. 状態を更新する別の期間を選択します。
10. 状態を更新する法人を選択します。
11. [期間の状態の更新] を選択し、状態を [保留中]、[未処理]、または [完全に終了] に設定します。
    * [オープン] は、ユーザーにアクセス許可がある場合に転記できる期間を示します。 [保留中] は、期間は転記できないが、再度開くことができることを意味します。 [完全に閉じる] は、期間が終了され、開くことができないことを意味します。 調整は転記できません。 すべての調整と監査が完了するまで、期間を [完全に閉じる] と設定しないようにお勧めします。  
12. [更新] をクリックします。

