---
title: 出荷連結ポリシーが上書きされた際に出荷を連結する
description: この記事では、1 つ以上の販売明細を、倉庫へのリリース ページから倉庫に手動でリリースする必要があり、かつリリース前にシステム定義の出荷連結ポリシーを上書きする必要があるシナリオを示します。
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2c4fed880c423790b979f27511d8d5697bd244c
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427958"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>出荷連結ポリシーが上書きされた際に出荷を連結する

[!include [banner](../includes/banner.md)]

この記事では、1 つ以上の販売明細を、**倉庫へのリリース** ページから倉庫に手動でリリースする必要があり、かつリリース前にシステム定義の出荷連結ポリシーを上書きする必要があるシナリオを示します。 例えば、通常はオープン出荷で連結されていない注文をオープン出荷で連結する必要がある場合など、出荷の連結ポリシーの上書きが必要になる場合があります。

このシナリオでは、一連の販売注文を作成してから、その注文を倉庫にリリースする前に既定の出荷連結ポリシーを上書きします。

## <a name="make-demo-data-available"></a>デモ データを有効化する

この記事のシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモ データに含まれる値とレコードを参照します。 ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>出荷連結ポリシーおよび製品フィルタの設定

このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。 このシナリオを続行する前に、この演習を行っている必要があります。

## <a name="create-the-sales-orders-for-this-scenario"></a>このシナリオで使用する販売注文の作成

1. **売掛金勘定 \> 注文 \> すべての販売注文を** に移動し、次のような同一の販売注文を3つ作成します:

    - **顧客アカウント:** *US-002*

1. 以下の設定で注文明細行を追加します:

    - **品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)
    - **数量:** *1.00*

1. **在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>[倉庫へのリリース] ページから販売注文をリリースする

倉庫へのリリース時に出荷の連結ポリシーを上書きするには、次の手順に従います。

1. **倉庫管理 \> 倉庫へのリリース \> 倉庫へのリリース** に移動します。
1. 上部ウィンドウで、このシナリオで作成した最初の販売注文を選択します。
1. **追加** を選択して、倉庫へのリリースに明細行を追加します。 *既定* の出荷連結ポリシーが下部ウィンドウに適用されていることを確認します。
1. 下部ウィンドウで、**新規出荷連結ポリシーの選択** を選択します。
1. 同一のポリシーを持つ、その他のオープンな出荷との連結を可能にするポリシーを選択します。 たとえば、*CustomerOrderNo* ポリシーを選択します。
1. **倉庫へのリリース** を選択します。
1. このシナリオで作成した、2番目と3番目の販売注文を選択します。
1. **追加** を選択して、倉庫へのリリースに明細行を追加します。 *既定* の出荷連結ポリシーが下部ウィンドウに適用されていることを確認します。
1. 2番目の明細行を選択し、**新規出荷連結ポリシーの選択** フィールドで、*CustomerOrderNo* ポリシーを選択します。
1. 両方の明細行で **倉庫へのリリース** を選択します。

## <a name="verify-the-shipments"></a>出荷の確認

次の 2 つの出荷が作成されている必要があります:

- 1つ目の出荷は、*CustomerOrderNo* の出荷連結ポリシーを使用して作成された 3 つの行で構成されます。
- 2つ目の出荷は、*既定* の出荷連結ポリシーを使用して作成された 1 つの行で構成されます。

作成された出荷を確認するには、次の手順に従います。

1. **倉庫管理 \> 出荷 \> すべての出荷** に移動します。
1. 必要な出荷を検索して選択します。
1. **出荷連結ポリシー** フィールドで、出荷の作成時に使用された連結ポリシーを確認します。

## <a name="additional-resources"></a>追加リソース

- [出荷連結ポリシーの概要](about-shipment-consolidation-policies.md)
- [出荷連結ポリシーを構成する](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]