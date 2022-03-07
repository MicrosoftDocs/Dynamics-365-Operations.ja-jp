---
title: 倉庫管理における作業が関連付けられている在庫の移動
description: 在庫移動を使用すると、引当済の在庫を移動することが許可されている倉庫作業者を指定できます。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d996886a90037f288e839c54c8c9d932cabb21f19f2aef1552ca82b192c96a51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736554"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>倉庫管理における作業が関連付けられている在庫の移動

[!include [banner](../includes/banner.md)]

在庫移動を使用すると、引当済の在庫を移動することが許可されている倉庫作業者を指定できます。 これにより、作業者が既に作成されているピッキング作業に対して新しいピッキング場所を選択できないように規制している倉庫内での柔軟性が実現します。 また、倉庫マネージャーは、経験の浅い従業員がどの機能を管理するかを制御できます。

倉庫作業者の日常的な工程を管理する柔軟性は、このような場合に役立ちます。

## <a name="scenario-1"></a>シナリオ 1

会社は比較的小さな入庫エリアを所有しており、待機中のパレットとボックスで混雑しています。 当日は大量の出荷が予定されているため、入荷係はパレットの一部を二次受信ステージング エリアに移動させて入庫エリアをクリアすることを決定します。

## <a name="scenario-2"></a>シナリオ 2

経験豊富な倉庫作業員は、倉庫内の商品を近くの3箇所に分けて少量ずつ置くのではなく、1箇所にまとめる機会に気付きました。 作業者は、これらの場所からそれぞれを同じ場所およびナンバープレート上に物品を移動することによって数量を集約したいと考えています。

## <a name="scenario-3"></a>シナリオ 3

パレットは BAYDOOR01 の近くにある STAGE01 などのステージング場所で出荷を待機しています。 計画の変更によりトラックは BAYDOOR04 に到着する予定です。 出荷係はこれを認識しており、トラックが STAGE01 から積み込まれるのを待つ必要がないことを確認する必要があります。 出荷係は、STAGE01 から新しい目的地に近い STAGE04 へその品目を移動することを指定します。

### <a name="current-limitations"></a>現在の制限

移動ができる作業引当は、販売注文、移動オーダーの出庫、移動オーダーの入庫、発注書、および補充作業に限定されます。

移動する品目は、作業明細行が分割されないように制限されています。 これは、Loc1 から 100 個ある品目 A の作業ラインがある場合、そこから 30 個ある品目 A のみを別の場所に移動することはできないことを意味します。 これにより、場所が異なるため、既存の作業明細行は 30 と 70 に分割されるようになります。

ステージング シナリオでは、商品を移動させるライセンス プレート、または商品を移動するライセンス プレートは、ワーク オーダーのターゲット LP として設定され、LP 全体の移動のみが許可されるため、ターゲット LP は分割されません。

アド ホック振替のみが現在サポートされています。 テンプレート モバイル デバイスのメニュー項目で、移動により引当済の在庫を移動できなくなることを意味します。

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>個々の作業者の引当済の在庫を移動するためのアクセス許可を設定します。

引当済の在庫の移動を許可されている作業者については、**倉庫管理 \> 設定 \> 作業者** の **作業に関連した在庫の移動を許可する** チェックボックスを選択します。  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
