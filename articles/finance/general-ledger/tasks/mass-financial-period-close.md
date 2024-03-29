---
title: 財務期間一括決算
description: この記事では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。
author: aprilolson
ms.date: 11/16/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a85d512842b27f2d74507be16a8f2819f483e0d
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779829"
---
# <a name="mass-financial-period-close"></a>財務期間一括決算

[!include [banner](../../includes/banner.md)]

この記事では、保留中期間の設定方法、または期間の完全な終了方法、または複数の法人を一度に扱う方法を示します。 またこのタスクは、特定のモジュールに転記されたユーザー グループを制限する方法を示します。

1. ナビゲーション ウィンドウで、**一般会計 > 決算期間 > 元帳カレンダー** の順に移動します。 

>[!NOTE]
> 表示された法人の一覧は、ページで選択した会計カレンダーに依存します。 選択された会計カレンダーを使用する法人のみが表示されます。

2. **編集** を選択します。
3. 状態を変更する期間を選択します。
4. 状態を更新する法人を選択します。 グリッドの左上のチェック マークを選択することにより、すべての法人をすばやく選択できます。  
5. **モジュール アクセスの更新** を選択して、選択されたモジュールへのアクセスの転記を定義します。 モジュールの状態は、グリッドのレコードを編集することにより順番に更新できます。 ボタンは、複数の法人のレコードをすばやく更新する場合に役に立ちます。  
6. **アプリケーション** モジュールで、状態を更新するモジュールを選択します。 **選択** をクリックします。
7. **アクセス** レベルで、**すべて**、**なし**、または特定のユーザー グループを選択します。 **選択** をクリックします。  
- **すべて** - オープン期間の場合、モジュールの編集アクセス許可を持つすべてのユーザーが転記できます。 
- **なし** - オープン期間の場合、ユーザーがモジュールに転記できません。 [特定のユーザー グループ] は、オープン期間の場合に、このグループのユーザーのみがモジュールに転記できることを示します。  
8. **更新** を選択します。 
9. 状態を更新する別の期間を選択します。
10. 状態を更新する法人を選択します。
11. **期間の状態の更新** を選択し、状態を **保留中**、**オープン**、または **完全に閉じる** に設定します。 **オープン** は、ユーザーにアクセス許可がある場合に転記できる期間を示します。 **保留中** は、期間は転記できないが、再度開くことができることを意味します。 **完全に閉じる** は、期間が終了され、開くことができないことを意味します。 調整は転記できません。 すべての調整と監査が完了するまで、期間を **完全に閉じる** と設定しないようにお勧めします。  
12. **更新プログラム** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
