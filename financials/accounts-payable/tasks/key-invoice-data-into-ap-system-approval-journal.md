--- 
title: "承認仕訳帳を使用した買掛金勘定への請求書データの入力"
description: "このタスク ガイドでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法を示します。"
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: d7cf810f1d8eabb9989fdd858585afcdf2e9574b
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>承認仕訳帳を使用した買掛金勘定への請求書データの入力

[!include[task guide banner](../../includes/task-guide-banner.md)]

このタスク ガイドでは、仕入帳を使用して請求書を作成した後、承認仕訳帳を使用して経費勘定を更新する方法を示します。


## <a name="create-and-post-and-invoice"></a>請求書の作成と転記
1. [買掛金勘定] > [請求書] > [仕入帳] の順に移動します。
2. [新規] をクリックします。
3. 使用する仕入帳の名前を選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. 登録を開いて経費明細行を入力するには [明細行] をクリックします。
6. 仕入先を選択してください。 たとえば、US-104 を入力または選択
7. [請求書] フィールドに値を入力します。
8. [説明] フィールドで値を入力します。
9. [貸方] フィールドに数値を入力します。
10. [承認者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 承認者を強調表示して [選択] をクリックすると、その承認者を選択します。
12. [転記] をクリックします。
13. ページを閉じます。
14. ページを閉じます。

## <a name="approve-an-invoice"></a>請求書の承認
1. [買掛金勘定] > [請求書] > [請求書の承認] の順に移動します。
2. [新規] をクリックします。
3. 使用する請求書承認仕訳帳の名前を選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. 明細行をクリックすると、承認する請求書を選択できるページが表示されます。
6. [伝票の検索] を選択すると、承認待ちの請求書をすべて表示します。
7. 作成した請求書をマークします。
8. [選択] をクリックします。
    * 上の手順で選択した伝票は、選択後にこのリストに移動されます。  
9. [OK] をクリックします。
10. 請求書に経費勘定を追加するには、勘定番号フィールドをクリックします。
11. 勘定番号を入力し、Tab キーでこのフィールドから移動します。 たとえば、600120 と入力します。
12. [転記] をクリックします。
13. 転記されたエントリを表示するには、[伝票] をクリックします。
    * 承認保留中の請求書の勘定は、取消されて実際の経費勘定に置き換えられます。  


