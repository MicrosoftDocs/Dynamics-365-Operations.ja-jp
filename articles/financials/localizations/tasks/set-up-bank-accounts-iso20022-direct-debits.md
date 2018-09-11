--- 
title: "顧客の設定と ISO20022 口座引落用の顧客銀行口座の設定"
description: "このタスクでは、顧客の銀行口座の設定、および ISO20022 口座引落などの顧客支払ファイルを生成するために必要な顧客口座引落の委任状の設定について説明します。"
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustBankAccounts, CustDirectDebitMandate, BankAccountTableLookUp,  LogisticsAddressCityLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5b4652b76e089d6beb2ce1513d06cf07a5ea3195
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>顧客の設定と ISO20022 口座引落用の顧客銀行口座の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、顧客の銀行口座の設定、および ISO20022 口座引落などの顧客支払ファイルを生成するために必要な顧客口座引落の委任状の設定について説明します。 設定された顧客支払形式によって、顧客または顧客の銀行口座について、この手順に含まれていない追加情報が必要になる場合があります。 

このタスクは、ドイツ内に通常の住所がある法人とデモ データの会社 DEMF を使用して作成されました。



これは、5 つのうち 4 つ目の手順で、電子レポートのコンフィギュレーションを使用する顧客支払処理を説明しています。


## <a name="set-up-a-customer-bank-account"></a>顧客銀行口座のの設定
1. [売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、値「DE-010」で [口座] フィールドをフィルターします。
3. 一覧で、選択された行のリンクをクリックします。
4. [アクション] ウィンドウで、[顧客] をクリックします。
5. [銀行口座] をクリックします。
6. [新規] をクリックします。
7. [銀行口座] フィールドに、値を入力します。
8. [名前] フィールドに値を入力します。
    * たとえば、「EUR bank」を入力します。  
9. [銀行グループ] フィールドで、値を入力または選択します。
10. [IBAN] フィールドに値を入力します。
    * たとえば、「DE36200400000628808808」を入力します。  
11. [SWIFT コード] フィールドに、値を入力します。
    * たとえば、「COBADEFFXXX」を入力します。  SWIFT \ BIC は多くの支払形式で必須ではありませんが、銀行口座への登録が推奨されていることに注意してください。  
12. [保存] をクリックします。
13. ページを閉じます。
14. [編集] をクリックします。
15. [支払の既定値] セクションを展開します。
16. [銀行口座] フィールドで、値を入力または選択します。

## <a name="add-a-direct-debit-mandate"></a>口座引落の委任状の追加
1. [口座引落委任状] セクションを展開します。
2. [追加] をクリックします。
3. [債権者の銀行口座] フィールドで、値を入力または選択します。
    * たとえば、[DEMF OPER] を選択します。  
4. [署名日] フィールドに日付を入力します。
5. 「はい」をクリックして、日付の更新を確認します。
6. [署名場所] フィールドで、値を入力または選択します。
7. [予定されている支払回数] フィールドに数値を入力します。
8. [OK] をクリックします。
9. [保存] をクリックします。


