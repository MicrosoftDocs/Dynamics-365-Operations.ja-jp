---
title: 資産除去責務の支払利子の減価償却および見越計上
description: 日本では、資産除去責務 (ARO) の減価償却は固定資産と一緒に処理されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09c57f0c2e8464f57e3ee5ae7942c1013f26bece
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236169"
---
# <a name="depreciate-and-accrue-the-interest-expense-for-asset-retirement-obligations"></a>資産除去責務の支払利子の減価償却および見越計上

[!include [banner](../../includes/banner.md)]

日本では、資産除去責務 (ARO) の減価償却は固定資産と一緒に処理されます。 また、ARO の総額を認識するためには、支払利子を見越計上する必要があります。



このタスクを使用して、ARO を減価償却し支払利子を見越計上します。 



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



このタスクはデモ会社 JPMF のデータを使用して完了しました。


## <a name="depreciate-a-fixed-asset-with-asset-retirement-obligation"></a>資産除去責務がある固定資産の減価償却
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで値を選択します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [償却提案] をクリックします。
8. [終了日] フィールドで、日付を入力します。
9. [フィルター] をクリックします。
10. [基準] フィールドに値を入力します。
11. [OK] をクリックします。
12. [OK] をクリックします。
    * 資産除去責務の減価償却は、[ドキュメント タイプ] フィールドごとに示されます。  
13. [転記] をクリックします。

## <a name="accrue-the-interest-expense"></a>支払利子の計上
1. ページを閉じます。
2. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
3. [新規] をクリックします。
4. [名前] フィールドで値を選択します。
5. [保存] をクリックします。
6. [明細行] をクリックします。
7. [提案] をクリックします。
8. [除去費用の費用配分] をクリックします。
9. [終了日] フィールドで、日付を入力します。
10. [フィルター] をクリックします。
11. [基準] フィールドに値を入力します。
12. [OK] をクリックします。
13. [OK] をクリックします。
    * 支払利子のレコードが提案されていることを確認します。  
    * 支払利子は、トランザクション タイプごとに示されます。  
14. [転記] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]