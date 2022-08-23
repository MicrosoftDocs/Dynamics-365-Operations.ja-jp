---
title: 支払手数料の生成および転記
description: このタスクでは、日本の支払手数料を生成および転記する方法について説明します。
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
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, VendTableLookup
ms.openlocfilehash: 8c177e5a3a1ec44799e4f91786e0bff2df872d77
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270547"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
