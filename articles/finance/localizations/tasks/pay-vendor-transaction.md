---
title: 顧客の受取手形の裏書による仕入先トランザクションの支払
description: このタスクは、顧客為替手形の裏書きによる仕入先トランザクションの支払について説明します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor, DimensionLookup, LedgerTransVoucher
ms.openlocfilehash: 55016d65e8f38cb62638ff892e2c43fb488eb09d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272090"
---
# <a name="pay-a-vendor-transaction-by-endorsing-a-customer-bill-of-exchange"></a>顧客の受取手形の裏書による仕入先トランザクションの支払

[!include [banner](../../includes/banner.md)]

このタスクは、顧客為替手形の裏書きによる仕入先トランザクションの支払について説明します。



このタスクを完了するには、少なくとも 1 つの [振出済] の状態の為替手形が必要です。



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="endorse-a-customer-bill-of-exchange-to-a-vendor"></a>仕入先に対する顧客の為替手形の裏書
1. [売掛金勘定] > [支払] > [為替手形] > [裏書為替手形] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * ステータスが「振出済」の為替手形を選択します。  
3. [仕入先に対する裏書] をクリックしてドロップ ダイアログを開きます。
4. [裏書日] フィールドに日付を入力します。
    * 日付は、為替手形の期日より後にすることはできません。  
5. [仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
    * 例: 「JPMF-000001」というレコードを選択します。  
7. [説明] フィールドに値を入力します。
8. BusinessUnit フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、選択された行のリンクをクリックします。
    * 例: 「003」というレコードを選択します。  
10. [仕入先に対する裏書] をクリックします。
11. [照会] をクリックします。
12. [伝票] をクリックします。
    * 会計伝票が裏書用に生成されていることを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
