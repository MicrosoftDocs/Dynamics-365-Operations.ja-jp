---
title: 新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない
description: このトピックでは、新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: d11f9cd46c4db42825717524241e496d53fa8e15
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020783"
---
# <a name="products-and-categories-dont-appear-in-commerce-site-builder-after-a-new-site-is-mapped"></a>新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない

[!include [banner](../../includes/banner.md)]

このトピックでは、新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されない場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

新しいサイトがマッピングされた後、製品とカテゴリが Commerce サイト ビルダーに表示されません。

## <a name="resolution"></a>解像度

### <a name="add-products-to-channel-categories-in-commerce-headquarters"></a>Commerce 本社のチャネル カテゴリへの製品の追加

Commerce 本社のチャネル カテゴリに製品を追加するには、次の手順に従います。

1. **Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動します。
1. 左のナビゲーションで、eコマース サイトに表示するカテゴリを選択します。
1. **製品** クイックタブで、**追加** を選択します。
1. **利用できる製品** セクションで、表示する製品を選択し、**追加** を選択します。
1. **OK** を選択します。
1. **製品** クイックタブに製品が表示されたら、アクション ウィンドウで **チャネル更新の公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[チャンネル ナビゲーション階層を使用するようにチャンネルをコンフィギュレーションする](../configure-channel-hierarchy.md)
