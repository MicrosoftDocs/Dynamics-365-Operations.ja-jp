---
title: 信用状についての銀行融資と転記プロファイルの設定
description: この手順では、信用状のプロセスを必要とする銀行融資と転記プロファイルの作成を説明します。
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 945504cd73b743fb3711997274c537e51e5c6dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834647"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>信用状についての銀行融資と転記プロファイルの設定

[!include [banner](../../includes/banner.md)]

この手順では、信用状のプロセスを必要とする銀行融資と転記プロファイルの作成を説明します。 

このタスクでは、USMF というデモ会社を使用します。






## <a name="general-ledger-parameter"></a>一般会計パラメーター
1. [現金および銀行管理] > [設定] > [現金および銀行管理パラメーター] の順に移動します。
2. [銀行ドキュメント] セクションを展開します。
3. [輸入信用状の有効化] オプションを選択します。
4. [輸出信用状の有効化] オプションを選択します。
5. [保存] をクリックします。
6. ページを閉じます。

## <a name="create-bank-facility"></a>銀行融資の作成
1. [現金および銀行管理] > [設定] > [銀行融資] の順に移動します。
2. [新規] をクリックします。
3. [融資グループ] フィールドで、銀行融資グループの名前を入力します。
4. [説明] フィールドに、銀行融資グループの説明を入力します。
5. [保存] をクリックします。
6. [融資タイプ] タブをクリックします。
7. [新規] をクリックします。
8. [融資タイプ] フィールドに、固有のコードを入力します。
9. [説明] フィールドに値を入力します。
10. [融資グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 一覧で、目的のレコードを見つけ、選択します。
12. 一覧で、選択された行のリンクをクリックします。
13. [融資の種類] フィールドで、銀行融資の種類を選択します。
14. [保存] をクリックします。
15. ページを閉じます。

## <a name="bank-posting-profile"></a>銀行転記プロファイル
1. [現金および銀行管理] > [設定] > [銀行ドキュメントの転記プロファイル] の順に移動します。
2. [新規] をクリックします。
3. [アカウント/グループ番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的のレコードを見つけ、選択します。
5. 一覧で、選択された行のリンクをクリックします。
6. 決済の主勘定を選択します。
    * この勘定は、キャッシュ フロー予測の計算時に使用されます。  
7. [手数料勘定] フィールドで、経費トランザクションの勘定を選択します。
8. [保証金勘定] フィールドで、マージン トランザクションの勘定を選択します。
    * この勘定は、開始差益の転記時に借方に転記され、支払の転記時に貸方に転記されます。  
9. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]