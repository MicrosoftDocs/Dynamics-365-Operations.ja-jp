---
title: 社内の商品移動の移動文書の設定
description: この手順では、社内の製品移動に関わるドキュメントを設定する方法を示します。
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
ms.openlocfilehash: 333c5b5e5cfa25e705c9864542517f8ec5532dfe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282337"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a>社内の商品移動の移動文書の設定

[!include [banner](../../includes/banner.md)]

この手順では、社内の製品移動に関わるドキュメントを作成する方法を示します。 この手順はリトアニアに主たる所在地を置く法人のみが使用できます。 この手順は、リトアニアに主たる事務所を置く企業 DEMF のデモデータを使用して作成されました。 この手順を完了する前に、"社内の製品移動に関わるドキュメントの設定" の手順を実施する必要があります。 この手順は在庫経理担当者を対象としています。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="create-a-transfer-order"></a>移動オーダーの作成
1. [在庫管理] > [受信した注文] > [移動オーダー] の順に移動します。
2. [新規] をクリックします。
3. [移動元倉庫] フィールドで値を入力または選択します。
4. [移動先倉庫] フィールドで値を入力または選択します。
5. [追加] をクリックします。
6. 一覧で、選択された行をマークします。
7. [品目番号] フィールドで、値を入力または選択します。

## <a name="enter-transportation-details-for-the-transfer-order"></a>移動オーダーの配送情報を入力する
1. [保存] をクリックします。
2. アクション ウィンドウで、[発送] をクリックします。
3. [輸送の詳細] をクリックします。
4. [配送情報の印刷] フィールドで、[はい] を選択します。
5. [製品配送元] フィールドで、値を入力または選択します。
6. [パッケージ] フィールドに値を入力します。
7. [積荷のリスクレベル] フィールドで、値を入力します。
8. [配送業者] フィールドで、値を入力または選択します。
9. [モデル] フィールドで、値を入力または選択します。
10. [登録番号] フィールドに値を入力します。
11. [トレーラー登録番号] フィールドに値を入力します。
12. [ドライバー] フィールドで、値を入力または選択します。
13. [ドライバー名] フィールドに値を入力します。
14. [保存] をクリックします。
15. ページを閉じます。

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>未転記の移動オーダーの梱包明細を表示する 
1. [梱包明細] をクリックします。
2. [OK] をクリックします。
3. ページを閉じます。

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>転記済みの移動オーダーの梱包明細を表示する 
1. アクション ウィンドウで、[移動オーダー] をクリックします。
2. アクション ウィンドウで、[発送] をクリックします。
3. [発送移動オーダー] をクリックします。
4. [一般] タブをクリックします。
5. [更新] フィールドで、オプションを選択します。
6. [概要] タブをクリックします。
7. [梱包明細] フィールドに値を入力します。
8. [OK] をクリックします。
9. アクション ウィンドウで、[発送] をクリックします。
10. [梱包明細] をクリックします。
11. [OK] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
