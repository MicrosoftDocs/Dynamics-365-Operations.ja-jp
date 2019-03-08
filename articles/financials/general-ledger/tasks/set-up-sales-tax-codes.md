---
title: 消費税コードを設定します
description: 売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "349173"
---
# <a name="set-up-sales-tax-codes"></a>消費税コードを設定します

[!include [task guide banner](../../includes/task-guide-banner.md)]

売上税コードは、法人が計算、収集、税務当局への支払いの義務のあるそれぞれの間接税または関税について作成されます。

このタスクでは、USMF というデモ会社を使用します。



1. [税] > [間接税] > [売上税] > [売上税コード] の順に移動します。
2. [新規] をクリックします。
3. [売上税コード] フィールドで、値を入力します。
4. [名前] フィールドに値を入力します。
5. [決済期間] を選択すると、この売上税の報告と支払いを行う売上税所轄官庁の指定や、その間隔の指定ができます。
6. 一覧で、選択された行のリンクをクリックします。
7. 総勘定元帳に売上税を転記する主勘定を指定するには、[元帳転記グループ] を選択します。
8. 一覧で、目的のレコードを見つけ、選択します。
9. 一覧で、選択された行のリンクをクリックします。
10. [計算] クイック タブを展開します。
    * [計算] クイックタブには、売上税額の計算方法を制御する複数のフィールドがあります。  
11. [アクション] ペインで [売上税コード] をクリックします。
12. [値] をクリックします。
13. 一覧で、選択された行をマークします。
14. 税コードの値を入力します。
    * [計算] クイック タブの [元] フィールドで、単位あたりの金額がオンの場合、売上税金額の計算では、値にトランザクションの数量が乗算されます。  税コードが単位に基づく税でない場合、値は、売上税金額を計算するためにこの税コードの発生元に適用される割合を示す値になります。     
15. [保存] をクリックします。
16. ページを閉じます。
17. [保存] をクリックします。

