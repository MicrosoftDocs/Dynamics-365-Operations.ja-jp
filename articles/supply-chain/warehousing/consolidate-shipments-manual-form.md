---
title: 出荷の連結ページを使用して出荷を手動で連結する
description: この記事では、複数の注文が倉庫にリリースされ、出荷の連結ページを使用して連結するシナリオを示します。
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 05f094b82b3d9bf9c095bc43f404aa7159bcafba
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427907"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>出荷の連結ページを使用して出荷を手動で連結する

[!include [banner](../includes/banner.md)]

この記事では、複数の注文が倉庫にリリースされ、**出荷の連結** ページを使用して連結するシナリオを示します。

## <a name="make-demo-data-available"></a>デモ データを有効化する

この記事のシナリオでは、Microsoft Dynamics 365 Supply Chain Management にて用意されている標準のデモ データに含まれる値とレコードを参照します。 ここで提供されている値を使用するには、デモデータがインストールされている環境で作業し、開始する前に法人を **usmf** に設定します。

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>出荷連結ポリシーおよび製品フィルタの設定

このシナリオでは、既にこの機能を有効にし、[出荷連結ポリシーの構成](configure-shipment-consolidation-policies.md)内の実習を完了しており、同ページ内に記述されているポリシーとその他のレコードを作成していることを前提としています。 このシナリオを続行する前に、この演習を行っている必要があります。

## <a name="create-the-sales-orders-for-this-scenario"></a>このシナリオで使用する販売注文の作成

シナリオで使用する一連の販売注文を作成することから始めます。 高度な倉庫 (WMS) プロセスが利用できる倉庫を使用する必要があります。 他の倉庫を明示的に指定していない場合は、次の注文セットのそれぞれに対して同じ倉庫が使用されなければなりません。

**売掛金勘定  \> 注文 \> すべての販売注文** に移動し、次のサブセクションで説明されている設定を含む販売注文のコレクションを作成します。

### <a name="create-sales-orders-1-and-2"></a>販売注文 1 と 2 の作成

1. 以下の設定で 2 つの同一の販売注文を作成します:

    - **顧客アカウント:** *US-007*
    - **プール :** *ShipCons*

1. 以下の設定で注文明細行を追加します:

    - **品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)
    - **数量:** *1.00*

1. **在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。

### <a name="create-sales-orders-3-and-4"></a>販売注文 3 と 4 の作成

1. 以下の設定で 2 つの同一の販売注文を作成します:

    - **顧客アカウント:** *US-007*
    - **プール :** このフィールドは空白のままにします。

1. 以下の設定で注文明細行を追加します:

    - **品目番号 :** *A0001* (**コード 4** フィルタが割り当てられていない品目)
    - **数量:** *1.00*

1. **在庫 \> 引当** を選択し、アクションウ ィンドウで **ロットの引当** を選択して、注文明細行を引当します。

## <a name="release-the-orders-to-the-warehouse"></a>注文を倉庫にリリースする

このシナリオで作成した各販売注文のリリースをするには、次の手順に従ってください。

1. **売掛金勘定 \> 注文 \> すべての販売注文** に移動します。
1. リリースする販売注文を検索して選択します。
1. アクション ウィンドウの、**倉庫** タブにて、**アクション\> 倉庫へのリリース** を選択して、選択された販売注文をリリースします。
1. このシナリオで作成したそれぞれの販売注文に対して、この手順を繰り返します。

## <a name="consolidate-shipments"></a>出荷の連結

1. **倉庫管理 \> 出荷 \> すべての出荷** に移動します。
1. 販売注文 1 が倉庫にリリースされた際に作成された出荷を検索して選択します。 (それぞれの **出荷連結ポリシー** フィールドには、*注文管理プール* を設定する必要があります。)
1. アクション ウィンドウの **出荷** タブで、**出荷 \> 出荷の連結** を選択します。
1. 連結の提案がされている出荷を確認します。 連結に提案は、同一のポリシーが設定された出荷を1つだけ設定する必要があります。
1. **出荷の連結** ページを閉じます。
1. 販売注文 3 が倉庫にリリースされた際に作成された出荷を検索して選択します。 (それぞれの **出荷連結ポリシー** フィールドには、*既定* を設定する必要があります。)
1. アクション ウィンドウの **出荷** タブで、**出荷 \> 出荷の連結** を選択します。
1. 連結の提案がされている出荷がないことを確認します。
1. **フィルタの表示** を選択します。
1. **フィルタ** ウィンドウで、**注文番号** フィルタを削除し、 **適用** を選択します。
1. 連結の提案がされている出荷を確認します。 連結に提案は、同一のポリシーが設定された出荷を1つだけ設定する必要があります。

## <a name="additional-resources"></a>追加リソース

- [出荷連結ポリシーの概要](about-shipment-consolidation-policies.md)
- [出荷連結ポリシーを構成する](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]