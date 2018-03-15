--- 
title: "小売明細書の支払コンフィギュレーション"
description: "この手順では、小売店舗支払方法のコンフィギュレーションが、小売明細書の作成と転記にどのように影響を及ぼすかを示します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 0ffd6dc5fff6d27ec3cfdcd68c53b2299c4100b9
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---
# <a name="payment-configurations-for-retail-statements"></a>小売明細書の支払コンフィギュレーション

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、小売店舗支払方法のコンフィギュレーションが、小売明細書の作成と転記にどのように影響を及ぼすかを示します。

このレコードでは、MXMF デモ会社を使用します。

1. [小売とコマース] > [チャンネル] > [小売店舗] > [すべての小売店舗] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. アクション ペインで、[設定] をクリックします。
5. [支払方法] をクリックします。
6. [転記] セクションを展開または折りたたみます。
7. [編集] をクリックします。
    * この支払方法に対して受領した勘定科目、または銀行口座への金額を転記するかどうかを選択します。  
    * 転記される必要がある支払方法の受領済金額の勘定を選択します。  
    * 受け取ったトランザクション金額の合計と、この支払方法でカウントされた金額の差額を転記する勘定を選択します。  
    * 別の差額勘定に差額が転記される必要がある場合、管理するために、このフィールドに金額を転記できます。 大きな差額を追跡するために、これを使用できます。  
    * [最大差額量] で定義された値を超えた場合に、受け取ったトランザクション金額の合計とカウントされた金額の差額を転記する勘定を選択します。  
    * 個別勘定への銀行入金額を転記するには、「はい」を選択します。  
    * このフィールドで、銀行入金額を、勘定科目、または銀行口座へ転記するかどうかを選択できます。  
    * 銀行入金額を転記する口座を選択します。  
    * 銀行入金額を銀行口座に転記するときの、銀行トランザクション タイプを選択します。  
    * 個別勘定への金庫保管額を転記するには、「はい」を選択します。  
    * 金庫保管額を、勘定科目、または銀行口座へ転記するかどうかを選択します。  
    * 金庫保管額を転記する口座を選択します。  
8. [保存] をクリックします。


