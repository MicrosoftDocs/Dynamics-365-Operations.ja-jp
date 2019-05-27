---
title: 仕入先月次締め請求書の再オープンと編集
description: 日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendConsInvoice_JP, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4c2bfc08853231b8795fb98855584f4eaad2cfe
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552411"
---
# <a name="reopen-and-edit-a-vendor-consolidated-invoice"></a>仕入先月次締め請求書の再オープンと編集

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、連結プロセス中に請求書を見逃した場合、月次締め請求書を再オープンしてその請求書を追加する必要があります。 



この手順では、確定済の月次締め請求書の再オープンと変更について説明します。 手順を完了するためには、月次締め請求書が確定済である必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="reopen-a-consolidated-invoice"></a>月次締め請求書の再オープン
1. [買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [再オープン] をクリックします。

## <a name="remove-a-purchase-order-a-consolidated-invoice"></a>月締め請求書から発注書を削除
1. 一覧で、選択された行のリンクをクリックします。
2. [編集] をクリックします。
3. 削除する請求書をマークします。
4. [削除] をクリックします。

## <a name="add-purchase-orders-and-confirm-the-consolidated-invoice"></a>月締め請求書への発注書の追加と確定
1. [請求書のクエリ] をクリックします。
2. [OK] をクリックします。
    * [月次締め日] 前に請求されている発注書が追加されていることを確認します。  
3. [確認] をクリックします。

