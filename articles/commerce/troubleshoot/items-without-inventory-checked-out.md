---
title: 在庫のない品目を清算できる
description: この記事では、顧客が在庫切れ品目を買い物カゴに追加してチェックアウトに進む際に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282737"
---
# <a name="items-without-inventory-can-be-checked-out"></a>在庫のない品目を清算できる

[!include [banner](../../includes/banner.md)]

この記事では、顧客が在庫切れ品目を買い物カゴに追加してチェックアウトに進む際に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

ユーザーは、店舗に在庫がない場合でも品目をカートに追加し、チェックアウト ページに進みます。

## <a name="resolution"></a>解像度

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Commerce サイト ビルダーの在庫切れエラーを表示するプロパティの有効化

Commerce サイト ビルダーの **在庫切れエラーを表示する** プロパティを有効にするには、次の手順を実行します。

1. 作業しているサイトを選択します。
1. 左のナビゲーション ウィンドウで、**ページ** を選択します。
1. **CartPage** を選択してして開きます。
1. **買い物かご 1** スロットを選択してから **編集** を選択し、プロパティ ウィンドウで **在庫切れエラーを表示する** チェック ボックス を選択します。
1. ページを保存してプ公開します。

## <a name="additional-resources"></a>追加リソース

[在庫設定の適用](../inventory-settings.md)

[小売チャンネルの引当可能在庫数量の計算](../calculated-inventory-retail-channels.md)

[在庫バッファーと在庫レベルのコンフィギュレーション](../inventory-buffers-levels.md)
