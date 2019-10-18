---
title: 請求書および AP システムの重要データの監査
description: 発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c6e8967fe4db67ff98fc7093792bdb82b73a33d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178603"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a>請求書および AP システムの重要データの監査

[!include [task guide banner](../../includes/task-guide-banner.md)]

発注書の商品またはサービスに対する請求書を仕入先から受け取ったときに、請求書の支払を承認する前に商品またはサービスをすでに受け取っていることが、業務プロセスで要求されている場合があります。 始める前に、[請求書照合] コンフィギュレーション キーが選択されていることを確認します。 

[買掛金勘定パラメータ] ページで、[請求書照合の検証を有効にする] オプションがオンで、[明細行照合ポリシー] のフィールドが [承認の要求] に設定され、[明細行照合ポリシー] が [スリーウェイ マッチング] に設定されていることを確認します。

この手順では、USMF というデモ会社を使用します。 買掛金勘定マネージャーまたは会計マネージャーのロールでは、次の手順を実行します。


## <a name="create-a-purchase-order"></a>発注書の作成
1. **すべての発注書**に移動します。
2. **新規** をクリックします。
3. **仕入先口座**フィールドに値を入力します。
4. **OK** をクリックします。
5. **行の追加**をクリックします。
6. **品目番号**フィールドに値を入力します。
7. アクション ウィンドウで、**購買**をクリックします。
8. **確定** をクリックします。

## <a name="post-a-product-receipt"></a>製品受領書の転記
1. アクション ウィンドウで、**受入**をクリックします。
2. **製品受領書**をクリックします。
3. **製品受領書**フィールドに値を入力します。
4. **OK** をクリックします。

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>仕入先請求書の製品受領書との記録および照合
1. アクション ウィンドウで、**請求書 > 請求書**をクリックします。
2. **数**フィールドに値を入力します。
3. **既定の取得元: 注文済数量**をクリックして、ドロップ ダイアログを開きます。
4. **明細行の既定の数量**フィールドで、オプションを選択します。
5. **OK** をクリックします。
6. **はい** をクリックします。
7. **製品受領書の照合**をクリックします。
8. **OK** をクリックします。
9. アクション ウィンドウで、**確認**をクリックします。
10. **照合の詳細**をクリックします。

