---
title: セクション関連リンクのサブパターン
description: この記事では、関連リンクのサブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 29331
ms.assetid: 984d7c6b-cf0a-4056-88f3-c32c92ca3401
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0f7a1297f63d7bbc9a9f558d785b30b17cbebe2
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781252"
---
# <a name="section-related-links-subpattern"></a>セクション関連リンクのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、関連リンクのサブパターンに関する情報を提供します。 このサブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。

## <a name="usage"></a>用途

セクション関連リンク サブパターンは、他のフォームへのリンクのセットを含む最後のパノラマ セクション専用の運用ワークスペース パターンの一部として使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
[![セクション関連リンクのワイヤーフレーム。](./media/sectionrelatedlinkswireframe.png)](./media/sectionrelatedlinkswireframe.png)

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

[![セクション関連リンクの例。](./media/sectionrelatedlinksexample.png)](./media/sectionrelatedlinksexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]