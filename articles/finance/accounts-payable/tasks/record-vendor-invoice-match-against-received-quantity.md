---
title: 仕入先請求書の受領記録および入庫済数量との照合
description: 発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。
author: ShivamPandey-msft
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9d3fab4be1de90783d5885cf46b9e0cf6ee74b5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820620"
---
# <a name="record-vendor-invoice-and-match-against-received-quantity"></a>仕入先請求書の受領記録および入庫済数量との照合

[!include [banner](../../includes/banner.md)]

発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。 始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。 

[買掛金勘定パラメータ] ページで、[請求書照合の検証を有効にする] オプションがオンで、[明細行照合ポリシー] のフィールドが [承認の要求] に設定され、[明細行照合ポリシー] が [スリーウェイ マッチング] に設定されていることを確認します。

この手順では、USMF というデモ会社を使用します。 買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。


## <a name="create-a-purchase-order"></a>発注書の作成
1. [すべての発注書] に移動します。
2. [新規] をクリックします。
3. [仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. [仕入先] フィールドに値を入力します。
5. [OK] をクリックします。
6. [明細行の追加] をクリックします。
7. [品目番号] フィールドに値を入力します。
8. アクション ウィンドウで、[購買] をクリックします。
9. [確認] をクリックします。

## <a name="post-a-product-receipt"></a>製品受領書の転記
1. アクション ウィンドウで、[入庫] をクリックします。
2. [製品受領書] をクリックします。
3. 一覧で、選択された行をマークします。
4. [製品受領書] フィールドで、値を入力します。
5. [OK] をクリックします。

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>仕入先請求書の製品受領書との記録および照合
1. アクション ウィンドウで、[請求書] をクリックします。
2. [請求書] をクリックします。
3. [数] フィールドに値を入力します。
4. [既定の取得元: 注文済数量] をクリックして、ドロップ ダイアログを開きます。
5. [明細行の既定の数量] フィールドで、オプションを選択します。
6. [OK] をクリックします。
7. [はい] をクリックします。
8. [製品受領書の照合] をクリックします。
9. [OK] をクリックします。
10. アクション ウィンドウで、[確認] をクリックします。
11. [照合の詳細] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]