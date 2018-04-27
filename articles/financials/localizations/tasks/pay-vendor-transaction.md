--- 
title: "顧客の受取手形の裏書による仕入先トランザクションの支払 (日本)"
description: "このタスクは、顧客為替手形の裏書きによる仕入先トランザクションの支払について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 54e752efd383a6740ec431f371f90091225cef4e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="pay-a-vendor-transaction-by-endorsing-a-customer-bill-of-exchange-japan"></a>顧客の受取手形の裏書による仕入先トランザクションの支払 (日本)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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
8. [BusinessUnit] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、選択された行のリンクをクリックします。
    * 例: 「003」というレコードを選択します。  
10. [仕入先に対する裏書] をクリックします。
11. [照会] をクリックします。
12. [伝票] をクリックします。
    * 会計伝票が裏書用に生成されていることを確認します。  


