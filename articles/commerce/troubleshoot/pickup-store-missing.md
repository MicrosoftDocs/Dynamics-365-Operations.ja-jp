---
title: 選択した店舗の一覧に小売店舗が表示されません
description: このトピックでは、店舗の一覧に小売店舗が表示されない場合に役立つトラブルシューティングガイドを示します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585418"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>選択した店舗の一覧に小売店舗が表示されません

[!include [banner](../../includes/banner.md)]

このトピックでは、店舗の一覧に小売店舗が表示されない場合に役立つトラブルシューティングガイドを示します。

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

[作業単位の作成](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[オンライン チャネルの設定](../channel-setup-online.md)
