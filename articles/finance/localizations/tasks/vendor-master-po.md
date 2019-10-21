---
title: 月次締め請求書の対象にする仕入先マスターおよび発注書の設定
description: 日本では通常、仕入先はトランザクションに月次締め請求書を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 514f5f51b9fead0f1f8c39ecf52ad1944b296e5b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174645"
---
# <a name="setup-vendor-master-and-purchase-order-to-be-target-of-consolidated-invoice"></a>月次締め請求書の対象にする仕入先マスターおよび発注書の設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

