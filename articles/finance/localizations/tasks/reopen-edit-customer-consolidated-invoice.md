---
title: 顧客月次締め請求書の再オープンと編集
description: この記事では、確認済の顧客月次締め請求書を再度開いて変更する方法について説明します。
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
ms.search.form: CustConsInvoice_JP, SysQueryForm
ms.openlocfilehash: cc8b00a82e5dba85527d43910b355def3923cef7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282370"
---
# <a name="reopen-and-edit-a-customer-consolidated-invoice"></a>顧客月次締め請求書の再オープンと編集

[!include [banner](../../includes/banner.md)]

日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。 



この手順では、確定済の月次締め請求書の再オープンと変更について説明します。 手順を完了するためには、月次締め請求書が確定済である必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="reopen-a-consolidated-invoice"></a>月次締め請求書の再オープン
1. [売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 既に確定している請求書を選択します。  
3. [再オープン] をクリックします。

## <a name="remove-a-sales-order-from-a-consolidated-invoice"></a>月締め請求書から販売注文を削除
1. 一覧で、選択された行のリンクをクリックします。
2. [編集] をクリックします。
3. 一覧で、選択された行をマークします。
4. [削除] をクリックします。

## <a name="add-sales-orders-and-confirm-the-consolidated-invoice"></a>月締め請求書への販売注文の追加と確定
1. [請求書のクエリ] をクリックします。
2. [OK] をクリックします。
    * [月次締め日] 前に請求済の販売注文が含まれていることを確認します。  
3. [確認] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
