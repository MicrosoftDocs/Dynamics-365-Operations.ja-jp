---
title: JBA のファイル形式の顧客支払のインポート
description: この記事では、JBA 形式の EFT ファイルのインポート方法について説明します。
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
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, SrsReportViewerForm
ms.openlocfilehash: 8df551e7f1bd6ff33fa116e520ff05bd85ff0f4a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280588"
---
# <a name="import-customer-payment-with-jba-file-format"></a>JBA のファイル形式の顧客支払のインポート

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
