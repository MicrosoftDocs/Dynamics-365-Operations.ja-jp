---
title: 顧客の受取手形の裏書による仕入先トランザクションの支払
description: このタスクは、顧客為替手形の裏書きによる仕入先トランザクションの支払について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor, DimensionLookup, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 167ac45bbf4aa58675d49ca1e70cb0661e4be275
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820499"
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