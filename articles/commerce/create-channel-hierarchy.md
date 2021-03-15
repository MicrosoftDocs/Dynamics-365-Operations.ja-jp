---
title: チャネル ナビゲーション階層の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce にチャネル ナビゲーション階層を作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 89e24496d35ea0a02bd985f76d7579e1914d9290
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972985"
---
# <a name="create-a-channel-navigation-hierarchy"></a>チャネル ナビゲーション階層の作成


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce にチャネル ナビゲーション階層を作成する方法について説明します。

## <a name="overview"></a>概要

チャネル ナビゲーション階層は、製品をグループ化してカテゴリに整理し、製品をオンラインまたは販売時点管理 (POS) で閲覧できるようにします。

## <a name="create-a-channel-navigation-hierarchy"></a>チャネル ナビゲーション階層の作成

チャネルのナビゲーション階層を作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 製品とカテゴリ \> チャネル ナビゲーション カテゴリ** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **名前** ボックスに、名前を入力します。
1. **説明** ボックスに、説明を入力します。
1. **作成** を選択します。
1. アクション ウィンドウで、**新しいカテゴリ ノード** を選択してルート ノードを作成します。
1. **名前** ボックスに、名前を入力します。
1. **説明** ボックスに、説明を入力します。
1. **フレンドリ名** ボックスに、フレンドリ名を入力します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、ルート ノードの例を示しています。

![サンプル ルート ノード](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>ナビゲーション カテゴリ ノードの作成

チャネルの製品カテゴリを表すその他のナビゲーション カテゴリ ノードを作成するには、次の手順に従います。

1. ナビゲーション ウィンドウで、カテゴリを追加する親ノードを選択します。
1. アクション ウィンドウで、**新しいカテゴリ ノード** を選択します。
1. **名前** ボックスに、名前を入力します。
1. **説明** ボックスに、説明を入力します。
1. **フレンドリ名** ボックスに、フレンドリ名を入力します。
1. **表示の順序** ボックスに、表示順序を入力します (オプション)。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、チャネル ナビゲーション階層の完成例を示しています。

![サンプル チャネル階層](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>製品をカテゴリ ノードに追加する

カテゴリ ノードに製品を追加するには、次の手順に従います。

1. カテゴリ ノードを選択します。
1.  **製品** で、**追加** を選択します。
1. 製品番号または製品名を使用して追加する新しい製品を検索し、**OK** を選択します。
1. アクション ウィンドウで、**保存** を選択します。

> [!NOTE]
> 選択されたチャネルで製品を表示するために、チャネル ナビゲーション階層内ノードへの製品の追加だけでなく、その製品を製品に類別する必要もあります。

次の図は、製品が追加されたノードの例を示しています。

![カテゴリ ノードに追加された製品](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>製品属性グループをカテゴリ ノードに追加

> [!NOTE]
> 属性グループは、チャネル ナビゲーション階層内ノードに追加する前に作成する必要があります。

カテゴリ ノードへ製品属性グループを追加するには、次の手順に従います。

1. カテゴリ ノードを選択します。
1. **製品属性グループ** で、**追加** を選択します。
1. 追加する属性グループを検索し、**OK** を選択します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、製品属性グループが追加されたサンプル ノードを示しています。

![ノードで製品属性グループの表示](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>追加リソース

[品揃えの設定](set-up-assortments.md)

[属性および属性グループの管理](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]