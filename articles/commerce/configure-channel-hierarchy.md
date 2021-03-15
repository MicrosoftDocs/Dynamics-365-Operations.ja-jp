---
title: チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする
description: このトピックでは、Microsoft Dynamics 365 Commerce のチャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする方法について説明します。
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
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001028"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のチャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする方法について説明します。

## <a name="overview"></a>概要

チャンネル ナビゲーション階層は、製品を E コマース サイトまたは販売時点管理 (POS) で参照できるように、製品をカテゴリに編成します。 チャンネル ナビゲーション階層を使用して、小売とオンライン チャンネルをコンフィギュレーションする必要があります。

## <a name="configure-the-channel"></a>チャンネルのコンフィギュレーション

チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションするには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> 小売とコマース \> チャネル設定 \> チャネル カテゴリと製品属性** の順に移動します。
1. コンフィギュレーションするチェンネルを選択します。
1. アクション ウィンドウで、**属性メタデータの設定** を選択します。
1. **カテゴリ階層** のドロップダウン リストで該当するチャンネル ナビゲーション階層を選択します。
1. アクション ウィンドウで、**保存** を選択します。
1. **属性グループ** で、すべてのノードのグローバル属性となる属性グループを追加します。

次の図は、チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする方法を示しています。

![チャネル コンフィギュレーションの例](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>属性メタデータの設定

属性メタデータを設定すると、各ノードの属性をコンフィギュレーションできるようになります。

属性メタデータを設定するには、次の手順に従います。

1. アクション ウィンドウで、**属性メタデータの設定** を選択します。
1. 各ノードについて、**チャンネル製品属性** を選択します。
1. **チャンネルの属性を表示** を **はい** に設定し、**絞り込み可能** を **はい** に設定すると、そのチャンネルで絞り込み条件を有効にできます。
1. 必要に応じて各ノードをコンフィギュレーションした後、**アクション ウィンドウ** で、**保存** ボタンを選択して保存します。
1. 右上隅の **X** を選択すると、この画面を終了して **チャンネル カテゴリと製品属性** のページに戻ります。

次の図は、チャンネル カテゴリ ノードにコンフィギュレーションされているチャンネル製品属性の例を示しています。

![チャンネル カテゴリ ノードのチャンネル属性](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>変更の公開

変更を有効にするには、チャンネルを公開する必要があります。

変更を公開するには、次の手順に従います。

1. アクション ウィンドウで、**チャンネル更新の公開** を選択します。
1. **チャンネル更新を公開** のウィンドウで、**OK** を選択します。

次の図は、チャンネルの更新を公開する方法を示しています。

![チャネル更新の公開](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>追加リソース

[チャンネル ナビゲーション階層を作成する](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]