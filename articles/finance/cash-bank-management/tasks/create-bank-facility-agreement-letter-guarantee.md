---
title: 信用保証状の銀行融資契約の作成
description: このタスクは、信用保証状を処理する銀行融資契約を作成します。
author: angelad116
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1b92b152e0b378733cfadc2c37231f9229f1e0c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780072"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a>信用保証状の銀行融資契約の作成

[!include [banner](../../includes/banner.md)]

このタスクは、信用保証状を処理する銀行融資契約を作成します。 このタスクでは、USMF というデモ会社を使用します。 


## <a name="create-bank-facility-agreement"></a>銀行融資契約の作成
1. **現金および銀行管理 > 信用保証状 > 銀行融資契約** の順に移動します。
2. **新規** をクリックします。
3. **契約番号** フィールドで、トランザクションの銀行の契約番号を入力します。
4. **銀行口座** フィールドで、信用保証状が開いている銀行口座番号を選択します。 
5. 一覧で、選択された行のリンクをクリックします。
6. **開始日** フィールドで、日付と時刻を入力します。
7. **終了日** フィールドで、日付と時刻を入力します。
8. [一般] セクションの展開を切り替えます。
9. **行の追加** をクリックします。
10. **融資タイプ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 一覧で、目的のレコードを見つけ、選択します。
12. 一覧で、選択された行のリンクをクリックします。
13. **限度** フィールドに、銀行との交渉に基づく金額を入力します。
14. **保存** をクリックします。
15. [信用保証状] セクションの展開を切り替えます。
16. **計算方法** フィールドで、オプションを選択します。
    * 必要に応じて、現金保証、払出コミッション、拡張コミッション、値コミッションの増加、または値コミッションの減少の計算方法および割合の詳細を入力します。   
17. **保存** をクリックします。

## <a name="extend-bank-facility-agreement"></a>銀行融資契約の拡張
1. **拡張** をクリックして、ドロップ ダイアログを開きます。
2. **新しい契約番号** フィールドに値を入力します。
3. **終了日** フィールドで、日付と時刻を入力します。
4. **拡張** をクリックします。
5. **保存** をクリックします。
6. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
