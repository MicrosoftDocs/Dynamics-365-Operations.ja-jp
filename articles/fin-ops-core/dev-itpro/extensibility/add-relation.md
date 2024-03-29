---
title: 拡張機能を使用してテーブルに関係を追加
description: この記事では、テーブルにリレーションを追加する方法について説明します。
author: ivanv-microsoft
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.custom: 268724
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 71dec8e961834293581c27ca53cd2f11ee560eb9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270979"
---
# <a name="add-relations-to-tables-through-extension"></a>拡張機能を使用してテーブルに関係を追加

[!include [banner](../includes/banner.md)]

複数のテーブルにあるデータとの高機能かつ安全な相互作用を可能にするには、2 つのテーブル間のリンクを記述するリレーションを定義して参照整合性を保証する必要があります。 関係を定義することにより、入力されたデータの検証および関連情報のルックアップ機能を有効にできます。 

テーブルを拡張することにより新しいリレーションを追加することができます。

次の例では、新しいフィールド **MyInventLocationId** が InventTable テーブルに追加されます。 このフィールドは、倉庫が含まれる InventLocation テーブルへの参照です。

1. 新しい拡張モデルで、InventTable テーブルの拡張機能を作成します。
1. 通常のテーブルにリレーションを作成するのと同じように、新しいリレーションを作成します。
1. **関連テーブル**、**関係タイプ**、**カーディナリティ** プロパティと、関係に適用される他のプロパティを指定します。
1. 同じ値を持つ InventTable テーブルと InventLocation テーブルからフィールドを指定してリンクを追加します。 この場合、フィールドは InventTable テーブルでは **MyInventLocationId** であり、InventLocation テーブルでは **InventLocationId** となります。

次の図は、新しいリレーションを示しています。

![新しい関係。](media/AddRelationToExistingTable.jpg)

## <a name="troubleshooting"></a>トラブルシューティング

### <a name="navigation-property-methods-not-working"></a>ナビゲーション プロパティ メソッド が動作しない
**問題** - テーブル拡張機能を使用して外部キー関係が作成されると、ナビゲーション プロパティ メソッドは動作しません。 コンパイラは拡張テーブルでナビゲーション メソッドの呼び出しを許可しません。

**解決策** - ナビゲーション メソッドは現時点でサポートされていません。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
