---
title: 支払手数料の生成および転記
description: このタスクでは、日本の支払手数料を生成および転記する方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, VendTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c88301964a95d720cbdc0eee983ecbe02937c2d3
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145088"
---
# <a name="generate-and-post-payment-fee"></a>支払手数料の生成および転記

[!include [banner](../../includes/banner.md)]

このタスクでは、日本の支払手数料を生成および転記する方法について説明します。



このタスクは デモ データ会社 JPMF を使用して作成されました。

1. [買掛金勘定] > [支払] > [支払仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
5. [明細行] をクリックします。
6. [勘定] フィールドで、任意の値を指定します。
    * たとえば、「JPMF-000001」と入力します。  
7. [借方] フィールドに数値を入力します。
    * 例: 「200000」と入力します。  
8. [保存] をクリックします。
9. [支払手数料] タブをクリックします。
    * 支払手数料が正しく生成されることを確認します。  
    * 支払金額、サード パーティ銀行口座、または銀行口座を変更して、これらのフィールドの組み合わせを変えると支払手数料の金額が変化することを確認できます。  
10. [転記] をクリックします。

