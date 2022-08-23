---
title: 新しい製品階層の作成
description: この記事では、Microsoft Dynamics 365 Commerce で新しい製品階層を作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 54a29381bb9231766d76b653904339d4bd60c257
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270130"
---
# <a name="create-a-new-product-hierarchy"></a>新しい製品階層の作成


[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で新しい製品階層を作成する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce は複数の小売チャンネルをサポートします。 これらの小売チャンネルには、オンライン ストア、コール センター、および小売用店舗 (従来型の店舗とも呼ばれる) が含まれます。 各小売店舗チャネルは、独自の支払方法、価格グループ、POS レジスタ、収入/経費勘定、およびスタッフを持つことができます。 小売店舗チャネルを作成する前に、これらのすべての要素を設定する必要があります。 

Commerce の製品階層は、組織の全体的な製品階層を定義するために使用されます。 販売促進、価格決定とプロモーション、および品揃え計画に Commerce 製品階層を使用できます。 組織ごとに、1 つの Commerce 製品階層だけを割り当てることができます。

## <a name="create-and-configure-a-product-hierarchy"></a>製品階層の作成およびコンフィギュレーション

Commerce 製品階層を作成してコンフィギュレーションするには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 製品とカテゴリ \> Commerce 製品階層** の順に移動します。
1. 階層がまだ存在しない場合、**アクション ウィンドウ** で **新規** を選択して階層のルートを作成します。
1. **一般** の下で:
    1. **名前** ボックスに、名前を入力します。
    1. **説明** ボックスに、説明を入力します。
    1. **フレンドリ名** ボックスに、フレンドリ名を入力します。
    1. **有効** を **はい** に設定します。

## <a name="add-hierarchy-nodes"></a>階層ノードの追加

階層ノードを追加するには、次の手順を実行します。

1. アクション ウィンドウで、**カテゴリ階層の編集** を選択します。
1. 新しいノードを追加する親ノードを選択し、**新しいカテゴリ ノード** を選択します。
1. **一般** セクションで、**名前**、**説明**、**フレンドリ名**、および **キーワード** を指定します。
1. **一般** の下で:
    1. **名前** ボックスに、名前を入力します。
    1. **説明** ボックスに、説明を入力します。
    1. **フレンドリ名** ボックスに、フレンドリ名を入力します。
    1. **キーワード** ボックスで、関連するキーワードを入力します。
    1. **表示順序** ボックスで、表示順序の番号を入力します (オプション)。
1. アクション ウィンドウで、**保存** を選択します。
1. 上記の手順を繰り返して、ノードを追加します。

次の図は、新しい製品階層ノードの作成を示しています。

![製品階層を作成します。](media/create-product-hierarchy.png)

## <a name="other-settings"></a>その他の設定

必要に応じて、各グループにカテゴリ属性グループを割り当てることもできます。  

## <a name="additional-resources"></a>追加リソース

[コマース階層](retail-hierarchies.md)

[製品カテゴリおよび製品の管理](category-management-product-creation.md)

[販売促進エンティティの並べ替え順序の変更](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
