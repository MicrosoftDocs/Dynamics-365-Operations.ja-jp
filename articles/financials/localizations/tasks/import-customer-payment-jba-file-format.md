--- 
title: "JBA ファイル形式の顧客支払のインポート (日本)"
description: "日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
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
ms.openlocfilehash: 0ed5ff4bcfe994829653e0e38ebc95c82d6c97bf
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-customer-payment-with-jba-file-format-japan"></a>JBA ファイル形式の顧客支払のインポート (日本)

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。 



このタスクは、JBA 形式での EFT ファイルのインポートについて説明します。



この手順は、デモ会社 JPMF のデータを使用して作成されました。

1. [売掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに、「CustPay」と入力します。
4. [明細行] をクリックします。
5. [機能] をクリックします。
6. [支払のインポート] をクリックします。
7. [支払方法] フィールドに値を入力します。
    * たとえば、JBA (JP) の形式 A を使用する支払方法を入力します。  
8. [OK] をクリックします。
    * アップロードするファイルを選択します。  
9. [OK] をクリックします。
10. レポートを閉じる
    * 管理レポートが生成されます。  
    * 支払金額と説明がインポートされることを確認してください。  
11. [口座] フィールドで、「JPMF-000001」という値を指定します。
12. [転記] をクリックします。


