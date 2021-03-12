---
title: JBA 形式で EFT 支払ファイルを生成
description: 日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6322791b30b955878180dcd9e81b4d7007caebff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990003"
---
# <a name="generate-eft-payment-file-with-jba-format"></a>JBA 形式で EFT 支払ファイルを生成

[!include [banner](../../includes/banner.md)]

日本では一般的に、銀行間の電子資金決済 (EFT) には全国銀行協会 (JBA) のファイル形式が使用されています。 



このタスクでは、JBA 形式を使用した EFT ファイルの生成方法について説明します。



この手順では、JPMF デモ会社のデータを使用します。

1. [買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに、「VendaPay」と入力します。
4. [明細行] をクリックします。
5. [口座] フィールドで、「JPMF-000001」という値を指定します。
6. [借方] フィールドに数値を入力します。
7. 後で参照するために、[相手勘定] フィールドの値をメモします。
8. [保存] をクリックします。
9. [支払の生成] をクリックします。
10. [支払方法] フィールドで、JBA のファイル形式に対して有効化されている支払方法を選択します。
11. [名前] フィールドで、生成されたファイルのファイル名を指定します。
12. [銀行口座] フィールドで、前にメモした値を使用します。
    * 仕入先の仕訳帳明細行で [相殺銀行口座] を選択します。  
13. [OK] をクリックします。
    * 支払管理レポートを印刷する場合は、スライダーを切り替えます。  
14. [OK] をクリックします。
    * .zip ファイルが生成され、ファイルをダウンロードするように求めるメッセージが表示されます。  
    * [支払ステータス] が、[送信済] に切り替わります。  

