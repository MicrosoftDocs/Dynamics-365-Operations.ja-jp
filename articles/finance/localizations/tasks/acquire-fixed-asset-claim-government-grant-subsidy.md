---
title: 固定資産の取得と政府助成金の申請
description: 固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。
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
ms.openlocfilehash: 65798979459b5dbe2729274dbb37d77d2e61256c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990064"
---
# <a name="acquire-a-fixed-asset-and-claim-for-the-government-grant-subsidy"></a>固定資産の取得と政府助成金の申請

[!include [banner](../../includes/banner.md)]

固定資産の取得および政府補助金の申請についての説明を見るには、このタスクを使用します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



このタスクでは、JPMF のデモ データを使用します。


## <a name="acquire-the-fixed-asset"></a>固定資産の取得
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [明細行] をクリックします。
5. [日付] フィールドに日付を入力します。
6. [勘定] フィールドで、任意の値を指定します。
    * 取得する固定資産を選択します。  
7. [帳簿] フィールドに値を入力します。
8. [借方] フィールドに数値を入力します。
9. [保存] をクリックします。
10. [転記] をクリックします。

## <a name="claim-the-fixed-asset-for-a-government-grant"></a>固定資産の政府助成金の申請
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [圧縮記帳の提案] をクリックします。
8. [フィルター] をクリックします。
    * フィルタ処理により、固定資産のより速く検索できます。  
9. [基準] フィールドに値を入力します。
10. [OK] をクリックします。
11. [OK] をクリックします。
12. [日付] フィールドに日付を入力します。
    * 助成金を仕訳入力する会計日を入力します。  
13. [貸方] フィールドに数値を入力します。
    * 政府助成金を入力します。  
14. [転記] をクリックします。

