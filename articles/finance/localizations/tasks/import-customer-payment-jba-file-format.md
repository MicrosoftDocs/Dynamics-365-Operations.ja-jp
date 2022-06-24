---
title: JBA のファイル形式の顧客支払のインポート
description: この記事では、JBA 形式の EFT ファイルのインポート方法について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4671617612f38559ef48a6711c90216c205601b7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874324"
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
