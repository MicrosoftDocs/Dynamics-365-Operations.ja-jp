---
title: リスト パネルのサブパターン
description: この記事では、リスト パネル フォームのサブパターンに関する情報を提供します。このサブパターンは、互いにデータを移動する 2 つのリストを管理します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12433
ms.assetid: 81df4016-d7b9-4376-8a78-bdd435d686f6
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5700e74f5367b9aebd49f3c6d72fe7eb878511cf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745707"
---
# <a name="list-panel-subpattern"></a>リスト パネルのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、リスト パネル フォームのサブパターンに関する情報を提供します。 アプリケーション チームはこのサブパターンを使用して相互にデータを移動する 2 つのリストを管理します。

<a name="usage"></a>用途
-----

リスト パネルは、アプリケーション チームがそれぞれの間でデータを移動する 2 つのリストを管理するために使用するサブパターンです。 このパターンは、相互にデータを移動する 2 つのリストを管理する **SysListPanel** クラス (プログラム的) アプローチのモデル化バージョンを表すことを意図しています。 リスト パネル サブパターンは、次のコントロールに対して適用できます。

-   TabPage コントロール
-   グループ コントロール

## <a name="wireframe"></a>ワイヤーフレーム
[![リスト パネルのワイヤーフレーム](./media/listpanel1-1024x339.png)](./media/listpanel1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   リスト (Grid/ListView) およびツリー コントロールがサポートされます。
-   右側のパネルは選択したセクションです。
-   左側のパネルは利用可能なセクションです。
-   6 つのボタンをアクションとして使用できます。
    -   追加
    -   削除
    -   すべて追加 (オプション)
    -   すべて削除 (オプション)
    -   上へ移動 (オプション)
    -   下へ移動 (オプション)

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- \[コンテナ\]

    - *CustomFilterGroup (グループ) \[オプション\]*
    - ListPanelGroup (グループ)

        - AvailablePanel (グループ)

            - グリッド | ツリー | ListView | ListBox

        - ActionPanel (グループ)

            - AddButton (ボタン)
            - RemoveButton (ボタン)
            - *AllAllButton (ボタン) \[オプション\]*
            - *RemoveAllButton (ボタン) \[オプション\]*

        - SelectedPanel (グループ)

            - グリッド | ツリー | ListView | ListBox\*

        - *MoveUpDownPanel \[オプション\]*

            - MoveUpButton (ボタン)
            - MoveDownButton (ボタン)

### <a name="core-components"></a>コア コンポーネント

-   ListPanel サブパターンをコンテナー (TabPage またはグループ) コントロールに適用します。
-   BP 警告に対処します。
    -   繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **標準フォーム ガイドライン:**
    -   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

## <a name="examples"></a>例
フォーム: **SalesSummaryParameters (GroupQuotation)** 

[![リスト パネルの例](./media/listpanel3.png)](./media/listpanel3.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-patterns"></a>通常、パターンによって使用される

-   [簡易リストと詳細](simple-list-details-form-pattern.md)
-   [目次](table-of-contents-form-pattern.md)
-   [詳細マスター](details-master-form-pattern.md)
-   [ダイアログ](dialog-form-pattern.md)
-   [ウィザード](wizard-form-pattern.md)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   なし

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![リスト パネルの例](./media/listpanel4.png)](./media/listpanel4.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]