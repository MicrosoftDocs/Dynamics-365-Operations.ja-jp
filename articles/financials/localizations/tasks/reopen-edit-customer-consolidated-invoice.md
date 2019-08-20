---
title: 顧客月次締め請求書の再オープンと編集
description: 日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustConsInvoice_JP, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d37dc0db21759544a0d00d4fd6e9fb64ce77b5
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848760"
---
# <a name="reopen-and-edit-a-customer-consolidated-invoice"></a>顧客月次締め請求書の再オープンと編集

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

