---
title: セクション タブ付きリストのサブパターン
description: この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。
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
ms.custom: 29291
ms.assetid: 3f8b00ff-54f0-4e32-bd7f-b94a74785537
ms.openlocfilehash: 6926736a18eedb0e65a35f3e05aab0d3301e51b0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273008"
---
# <a name="section-tabbed-list-subpattern"></a>セクション タブ付きリストのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、セクション タブ付きリストのサブパターンに関する情報を提供します。 このサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。

## <a name="usage"></a>用途

セクション タブ付きリストのサブパターンは、それぞれにデータのフィルタ処理されたリストを含む垂直タブセットが入ったパノラマ セクション専用の、運用ワークスペース パターンの一部として使用されます。

## <a name="wireframe"></a>ワイヤーフレーム
[![セクション タブ付きリストのワイヤーフレーム。](./media/sectiontabbedlistwireframe.png)](./media/sectiontabbedlistwireframe.png)

## <a name="pattern-changes-for-microsoft-dynamics-ax"></a>Microsoft Dynamics AX 用のパターンの変更
このパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- TabPage
- TabbedList (タブ) (Style=VerticalTabs)

    - *TabbedListPage (TabPage)\[0..N\]*

        - TargetForm (FormPart)

各フォーム パーツでは、セクションの内容を含むフォームを指します。 これらのフォームはそれぞれ、Form Part Section List フォーム パターンの 1 つを使用する必要があります。

### <a name="core-components"></a>コア コンポーネント

セクション タブ付きリストをワークスペース内の適切なタブ ページに適用します。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [運用ワークスペース](workspace-form-pattern.md)
-   [フォーム パート セクション リスト](section-list-form-pattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   少なくとも 1 つのリストはタブ付きリストのセクション内に含まれている必要があります。
-   各フォーム パーツ コントロールでは、いずれかの[フォーム パーツ セクション リスト](section-list-form-pattern.md)パターンを使用するフォームを指す必要があります。

## <a name="examples"></a>例
フォーム: **PurchOrderMaintainWorkspace** (**すべてのワークスペース** &gt; **発注書の準備**) 

[![タブ付きリストのセクションの例。](./media/tabbedlistsectionexample.png)](./media/tabbedlistsectionexample.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

None


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
