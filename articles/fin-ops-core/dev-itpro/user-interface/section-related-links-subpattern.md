---
title: セクション関連リンクのサブパターン
description: この記事では、関連リンクのサブパターンに関する情報を提供します。 このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29331
ms.assetid: 984d7c6b-cf0a-4056-88f3-c32c92ca3401
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42818f11527598d36cb716e2fe39186a1aeb2d85
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687294"
---
# <a name="section-related-links-subpattern"></a>セクション関連リンクのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、関連リンクのサブパターンに関する情報を提供します。 このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。

<a name="usage"></a>用途
-----

セクション関連リンク サブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
[![セクション関連リンクのワイヤーフレーム](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a>Microsoft Dynamics AX 用のパターンの変更
このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- TabPage

    - *LinkButton ($ ボタン)\[0..N\]*
    - *ButtonGroup (グループ)\[0..N\]*

- LinkButton ($Button) \[1..N\]

### <a name="core-components"></a>コア コンポーネント

セクション関連リンクを運用ワークスペース内の適切なタブ ページに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [運用ワークスペース](workspace-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 None

## <a name="examples"></a>例
フォーム: **PurchOrderProcessReceiptsWorkspace** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ** (**リンク** セクションを参照してください) 

[![セクション関連リンクの例](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None
