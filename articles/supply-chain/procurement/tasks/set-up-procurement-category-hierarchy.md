---
title: 調達カテゴリ階層の設定
description: この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaab2093eb2531b63f27717d828f7064a8f9ed1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207511"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>調達カテゴリ階層の設定

[!include [banner](../../includes/banner.md)]

この手順では、調達カテゴリ階層に新しいノードを作成する方法、および調達プロセスに使用する調達カテゴリをコンフィギュレーションする方法を示します。 通常、これらのタスクを実施するのは、購買マネージャーです。 この手順を開始する前に、調達タイプのカテゴリ階層が必要です。 デモ データの会社を使用すると、USMF 会社でこの手順を実行できます。


## <a name="add-a-new-procurement-category"></a>新しい調達カテゴリを追加します。
1. **ナビゲーション ウィンドウ > モジュール > 調達 > 委託販売 > 調達カテゴリ**の順に移動します。
2. アクション ウィンドウで、**カテゴリ階層の編集**を選択します。 現在の調達カテゴリ階層が、ページの左側に表示されます。 階層を修正しようとしています。  
3. アクション ウィンドウで、**新しいカテゴリ ノード**を選択します。 システムは、既定によりトップ ノードを選択します。 タスク ガイドの手順を実行している場合、[ロック解除] ボタンをクリックして、別の親ノードを選択し、新しいノードを挿入することができます。 その場合、タスクのガイドを再度ロックし、[新しいカテゴリ ノード] をクリックします。  
4. **名前**フィールドに値を入力します。
5. **説明**フィールドで、値を入力します。
6. **フレンドリ名**フィールドで、値を入力します。 フレンドリ名はオプションです。 これは、カテゴリの名前と一緒に、カテゴリのルックアップに表示されます。  
7. **保存** を選択します。

## <a name="add-products-to-your-new-procurement-category"></a>新しい調達カテゴリへの製品の追加
1. **調達 > 委託販売 > 調達カテゴリ**の順に移動します。 追加したノードを選択します。 タスク ガイドとしてこの手順を実行している場合は、ノードを選択するために、タスク ガイドのロック解除が必要な場合があります。  
2. **製品**セクションの展開を切り替えます。
3. 調達カテゴリに製品を関連付けるには、**追加**を選択します。
4. 調達カテゴリに追加する製品を選択します。
5. 矢印を選択して**選択済**テーブルに製品を追加します。
6. **OK** を選択します。
