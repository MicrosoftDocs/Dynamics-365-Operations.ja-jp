---
title: 品目を使用して、基本倉庫が有効な品目の品目を着荷仕訳帳登録します。
description: この手順では、在庫管理モジュールで、"基本倉庫保管" を使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec8c1912435cf822db6eaecc5fff3dbcac793f77
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977066"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>品目を使用して、基本倉庫が有効な品目の品目を着荷仕訳帳登録します。

[!include [banner](../../includes/banner.md)]

この手順では、在庫管理モジュールで、"基本倉庫保管" を使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。 これは通常、入荷係により行われます。 表示されているサンプル値を使用して、デモ データの会社 USMF でこの手順を実行できます。  USMF を使用していない場合、このガイドを開始する前に、未処理の発注書明細行と共に確認済の発注書が必要です。 明細行の品目は在庫がある必要があります。 その品目は、倉庫管理プロセスが有効化された保管分析コード グループと関連付けられている必要があります。


## <a name="create-item-arrival-journal-header"></a>着荷仕訳帳ヘッダーの作成
1. [在庫管理] > [仕訳入力] > [品目到着] > [品目到着] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
    * USMF を使用している場合、「WHS」と入力できます。 その他のデータを使用している場合、名前を選択した仕訳帳は次のプロパティを必要とします : ピッキング場所の確認 は いいえ に設定し、検査管理 は いいえ に設定する必要があります。  
4. [梱包明細] フィールドに値を入力します。
    * これは、仕入先によって発行された梱包明細の梱包明細 ID です。 固有の参照番号を追加します。  
5. [番号] フィールドで発注書を選択します。
6. [OK] をクリックします。

## <a name="add-lines-to-item-arrival-journal"></a>行を着荷仕訳帳に追加する
1. [機能] をクリックします。
2. [行の作成] をクリックします。
    * この明細行はこの仕訳帳に手動で入力でき、または自動的に作成できます。 そして、これを自動的に作成する方法を示します。  
3. [数量の初期化] チェック ボックスをオンまたはオフにします。
    * さらに、購買注文明細行で登録されていない数量と仕訳帳明細行の数量を初期化します。  
4. [OK] をクリックします。

## <a name="post-the-journal"></a>仕訳帳の転記
1. [転記] をクリックします。
2. [OK] をクリックします。

## <a name="generate-the-product-receipt"></a>製品受領書の生成
1. [機能] をクリックします。
2. [製品受領書] をクリックします。
3. [OK] をクリックします。

