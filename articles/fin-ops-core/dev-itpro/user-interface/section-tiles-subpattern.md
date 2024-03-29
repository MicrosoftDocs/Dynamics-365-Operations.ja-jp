---
title: セクション タイルのサブパターン
description: この記事では、セクション タイルのサブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 29311
ms.assetid: 196e714a-ecfc-42b3-a7f5-84e29fb271bb
ms.openlocfilehash: a0c3af6e2077f7b4fce491bf381b845293247beb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273004"
---
# <a name="section-tiles-subpattern"></a>セクション タイルのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、セクション タイルのサブパターンに関する情報を提供します。 このサブパターンは、タイル、グラフ、および単一カードのセットを含む最初のパノラマ セクション (概要セクション) 専用の、運用ワークスペース パターンの一部として使用されます。 

## <a name="usage"></a>用途

セクション タイル サブパターンは、タイル、グラフ、および単一カードのセットを含む最初のパノラマ セクション (**概要** セクション) 専用の、運用ワークスペース パターンの一部として使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
[![セクション タイルのワイヤーフレーム。](./media/sectiontileswireframe.png)](./media/sectiontileswireframe.png)

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a>Microsoft Dynamics AX 用のパターンの変更
このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- TabPage

    - *TileButton (TileButton)\[0..N\]*
    - *TargetForm (FormPart)\[0..N\]*

フォーム パーツは、グラフまたは単一のカードをワークスペースの **集計** セクションに埋め込むために使用されます。 グラフを表す各フォームでは、[セクション チャート](section-chart-form-pattern.md)フォーム パターンを使用する必要があります。

### <a name="core-components"></a>コア コンポーネント

セクション タイルを運用ワークスペース内の最初のタブ ページに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [運用ワークスペース](workspace-form-pattern.md)
-   [セクション グラフ](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **集計** セクションは、「集計」という名前にするか、"Summary" という語を修飾するバリアントにする必要があります。
-   ワークスペースの 2 つのタイルに、同じ記号がある必要はありません。
-   最大 1 つの「新しい」タイルが必要です。
-   グラフのサイズは、タイル サイズの倍数に対応する必要があります。
    -   使用可能なサイズには縦 1 タイル × 横 2 タイル、2 × 2、2 × 3、2 × 4、2 × 6、4 × 4、4 × 6 および 4 × 8 が含まれます。

## <a name="examples"></a>例
フォーム: **PurchOrderMaintainWorkspace** (**すべてのワークスペース** &gt; **発注書の準備** (**集計** セクションを参照してください)

[![セクション タイルの例。](./media/sectiontilesexample.png)](./media/sectiontilesexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
