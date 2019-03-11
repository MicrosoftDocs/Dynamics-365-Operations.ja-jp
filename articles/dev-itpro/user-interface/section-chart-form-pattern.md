---
title: セクション グラフのフォーム パターン
description: この記事では、セクション グラフのフォーム パターンに関する情報を提供します。 このパターンは主に、作業ワークスペース パターンと組み合わせて使用されます。特に、チャート コントロールを含むフォームに使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29271
ms.assetid: 049887b5-6277-4902-96ec-a81a3d2348c3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a25c66c54b72f23ee4e7ecbf34b5e9c11ef09065
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369860"
---
# <a name="section-chart-form-pattern"></a>セクション グラフのフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、セクション グラフのフォーム パターンに関する情報を提供します。 このパターンは主に、作業ワークスペース パターンと組み合わせて使用されます。特に、チャート コントロールを含むフォームに使用されます。

<a name="usage"></a>用途
-----

セクション グラフ フォーム パターンは、主に運用ワークスペース パターンと組み合わせて使用することを意図しています。 具体的には、グラフ セクションまたは集計セクションに、グラフが含まれるフォームをポイントするフォーム パーツ コントロールが含まれます。 これらの参照されるフォームは、セクション グラフ パターンを使用することを意図しています。

## <a name="wireframe"></a>ワイヤーフレーム
[![sectionChartWireframe](./media/sectionchartwireframe1.png)](./media/sectionchartwireframe1.png)

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations 用のパターンの変更
このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- フォーム デザイン

    - *HeaderGroup (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。
    - グラフ

### <a name="core-components"></a>コア コンポーネント

セクション グラフ パターンを適切なフォーム/コンテナーに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [運用ワークスペース](workspace-form-pattern.md)
-   [セクション積み上げグラフ](section-stacked-chart-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 None

## <a name="examples"></a>例
フォーム: **FmBiChartPart\_VehicleByModel** (**すべてのワークスペース** &gt; **予約管理** (**統計**セクションを参照してください) 

[![sectionChartExample](./media/sectionchartexample.png)](./media/sectionchartexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None
