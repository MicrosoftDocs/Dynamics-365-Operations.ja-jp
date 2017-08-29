--- 
title: "支払手数料の生成および転記 (日本)"
description: "このタスクでは、日本の支払手数料を生成および転記する方法について説明します。"
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 44293d4e6b56d2def1e76ba776cb727d93b6e166
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="generate-and-post-payment-fee-japan"></a>支払手数料の生成および転記 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


