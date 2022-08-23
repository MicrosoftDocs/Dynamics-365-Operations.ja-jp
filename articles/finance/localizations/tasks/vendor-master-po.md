---
title: 月次締め請求書の対象にする仕入先マスターおよび発注書の設定
description: 日本では通常、仕入先はトランザクションに月次締め請求書を使用します。
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
ms.search.form: VendTable, PurchTable
ms.openlocfilehash: 4970d75bda595bbb4559dfe4faba90a1b9405d60
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285722"
---
# <a name="setup-vendor-master-and-purchase-order-to-be-target-of-consolidated-invoice"></a>月次締め請求書の対象にする仕入先マスターおよび発注書の設定

[!include [banner](../../includes/banner.md)]

日本では通常、仕入先はトランザクションに月次締め請求書を使用します。 



このタスクは、仕入先マスターおよび発注書を構成して月次締め請求書を使用する方法について説明します。 



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="set-up-vendor-master"></a>仕入先マスターの設定
1. [買掛金勘定] > [仕入先] > [すべての仕入先] の順に移動します。
2. 一覧で、選択された行のリンクをクリックします。
3. [支払] セクションを展開または折りたたみます。
    * 支払条件 で [締日] が使用されていることを確認します。  
    * 仕入先の [月次締め日] を指定します。  
    * このフィールドの更新には [編集] をクリックする必要がある場合があります。  

## <a name="set-a-purchase-order-to-be-target-of-consolidated-invoice"></a>月次締め請求書の対象とする発注書の設定
1. [買掛金勘定] > [発注書] > [すべての発注書] に移動します。
2. 一覧で、選択された行のリンクをクリックします。
3. [アクション] ウィンドウで、[オプション] をクリックします。
4. [ビューの変更] をクリックします。
5. [ヘッダーの表示] をクリックします。
    * [締めの対象] スライダーが「はい」に設定されていることを確認します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
