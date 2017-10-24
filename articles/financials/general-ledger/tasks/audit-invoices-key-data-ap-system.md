--- 
title: "請求書および買掛金勘定の重要データの監査"
description: "発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。"
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5cd9448c95b7ec0c4a82aca3d21d961259dfb109
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>請求書および買掛金勘定の重要データの監査

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


