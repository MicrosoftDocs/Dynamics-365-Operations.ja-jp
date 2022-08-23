---
title: 選択した店舗の一覧に小売店舗が表示されません
description: この記事には、店舗の一覧に小売店舗が表示されない場合に役立つトラブルシューティング ガイドが含まれます。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: b6cec3d9d598be221516506388e4797ad579a610
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286755"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>選択した店舗の一覧に小売店舗が表示されません

[!include [banner](../../includes/banner.md)]

この記事には、店舗の一覧に小売店舗が表示されない場合に役立つトラブルシューティング ガイドが含まれます。

## <a name="description"></a>説明

店舗の一覧に商品を受け取ることができる小売店舗は、表示されません。

## <a name="resolution"></a>解像度

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Commerce 本社の店舗住所の経度と緯度を構成します

Commerce 本社の店舗住所の経度と緯度を構成するには次の手順に従います。

1. **Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。
1. eコマース サイトの集荷オプションの中から表示する店舗を検索します。 **作業単位数** 値をメモします。
1. **組織管理 \> 組織 \> 作業単位** の順に移動します。
1. 以前にメモした作業単位番号を検索し、検索結果の作業単位を選択します。
1. **住所** クイック タブで、**その他のオプション** を選択し、**詳細** を選択します。
1. **一般** クイック タブで、**経度** フィールドと **緯度** フィールドが正しく設定されていることを確認します。 この手順の一環として、値が正または負の数として正しく指定されていることを確認します。

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Commerce 本社でのフルフィルメント グループを構成します

Commerce 本社でフルフィルメント グループを構成するには、次の手順に従います。

1. **Retail と Commerce \> チャネル \> オンライン ストア** に移動します。
1. 構成するオンライン ストアを選択します。
1. アクション ペインで、**設定** を選択し、**フルフィルメント グループの割り当て** を選択します。
1. **フルフィルメント グループの割り当て** ページで、オンラインストアのフルフィルメント グループを選択します。
1. **設定** で、フルフィルメント グループに対して小売店舗が正しく構成されていることを確認します。

## <a name="additional-resources"></a>追加リソース 

[作業単位の作成](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[オンライン チャネルの設定](../channel-setup-online.md)
