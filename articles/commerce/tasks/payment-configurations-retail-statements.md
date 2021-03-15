---
title: 小売明細書の支払構成
description: この手順では、明細書の作成や転記の方法に影響する、Commerce の店舗支払方法のコンフィギュレーションを示します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b1fc042bff4d801ae893b0370b67cd8e11ba95f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982318"
---
# <a name="payment-configurations-for-retail-statements"></a>小売明細書の支払構成

[!include [banner](../includes/banner.md)]

この手順では、明細書の作成や転記の方法に影響する、Commerce の店舗支払方法のコンフィギュレーションを示します。

このレコードでは、MXMF デモ会社を使用します。

1. Retail および Commerce > チャネル > 店舗 > すべての店舗の順に移動します。
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]