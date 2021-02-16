---
title: 詳細マスター フォーム パターン
description: このトピックでは、詳細マスター フォームのパターンについて説明します。 詳細フォームは、データ入力の基本方法です。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12373
ms.assetid: e4518f56-57b5-4cf1-b197-3fbaea7be861
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ecb2094f3f7d788b3ede13049dea034e057f286
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687591"
---
# <a name="details-master-form-pattern"></a>詳細マスター フォーム パターン

[!include [banner](../includes/banner.md)]

このトピックでは、詳細マスター フォームのパターンについて説明します。 詳細フォームは、データ入力の基本方法です。

<a name="usage"></a>用途
-----

詳細フォームは、データ入力の基本方法です。 これらのフォームにより、ユーザーはデータを表示、編集、および操作できます。 これらフォーム タイプのすべてのコンテンツは展開および折りたたむことのできるクイック タブとして構造化されているため、複数のクイック タブを同時に開くことができます。 クイック タブには、フィールドやグリッドを含めることができ、各クイック タブはローカル ツール バーを持つことができます。 このドキュメントでは、2 つのパターンについて説明します。

-   **詳細マスター** - これは、基本の詳細マスター パターンです。 これは既定で使用されるパターンです。
-   **タブ付き詳細マスター** - エンティティがカテゴリにグループ化できるクイック タブ (15 以上) を多数必要とする場合は、このパターンを使用する必要があります。

どちらの場合も、グリッド ビューの構成は同じです。

## <a name="wireframe"></a>ワイヤーフレーム
### <a name="details-master"></a>詳細マスター

#### <a name="details-view"></a>詳細ビュー

[![詳細マスター ワイヤーフレーム: 詳細ビュー](./media/detailsmaster1-1024x578.png)](./media/detailsmaster1.png)

#### <a name="grid-view"></a>グリッド ビュー

[![詳細マスター ワイヤーフレーム: グリッド ビュー](./media/detailsmaster2-1024x575.png)](./media/detailsmaster2.png)

### <a name="details-master-with-standard-tabs"></a>標準タブによる詳細マスター

#### <a name="details-view"></a>詳細ビュー

[![標準タブ ワイヤーフレームによる詳細マスター: 詳細ビュー](./media/detailsmaster3-1024x576.png)](./media/detailsmaster3.png)

#### <a name="grid-view"></a>グリッド ビュー

[![標準タブ ワイヤーフレームによる詳細マスター: グリッド ビュー](./media/detailsmaster4-1024x575.png)](./media/detailsmaster4.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   詳細ビューコンテンツの左側にリスト スタイル グリッドが追加されました。
-   リスト ページと詳細マスターが 1 つのフォームにマージされました。
    -   一覧と詳細の間を移動するときのパフォーマンスが向上します。
    -   初期一覧で一括編集を有効にします。
    -   プレビュー ウィンドウの一覧ページの消去を許可します。
-   表示/編集、新規作成、削除、保存、最新の情報に更新、添付、および Excel にエクスポートの各アクションはすべてファンデーションによって提供され、ファンデーションによって提供されたボタンが削除されない限り、各アクションに明示的なアプリ ボタンを使用する必要はありません。
-   以前に TOC 拡張機能を使用したマスター詳細フォームでは、標準タブ パターン付きマスター詳細を使用する必要があります。

## <a name="model"></a>モデル
### <a name="details-master-basic--high-level-structure"></a>詳細マスター (基本) – 高レベル構造体

- デザイン

    - ActionPane (ActionPane)
    - SidePanel (グループ)

        - QuickFilter
        - *CustomFilter (グループ) \[オプション\]*
        - NavigationList (グリッド、スタイル = リスト)

    - MainTab (Tab ShowTabs=No)

        - DetailsTabPage (TabPage)

            - TitleGroup (グループ)

                - HeaderTitle (文字列)
                - *EntityStatus (グループ) \[オプション\]*

                    StatusFields (1..N)

            - DetailsTab (タブ スタイル =FastTabs)

                - DetailsTabPage (TabPages *反復 1..N*)

        - GridTabPage (TabPage)

            - CustomFilterGroup (グループ)

                - QuickFilter
                - *OtherFilters ($ フィールド)\[0..N\]*

            - MainGrid (グリッド)
            - MainGridDefaultAction (CommandButton)

### <a name="details-master-with-standard-tabs--high-level-structure"></a>標準タブの詳細による詳細マスター – 高度な構造

- デザイン

    - ActionPane (ActionPane)
    - SidePanel (グループ)

        - QuickFilter
        - *CustomFilter (グループ) \[オプション\]*
        - NavigationList (グリッド、スタイル = リスト)

    - MainTab (Tab ShowTabs=No)

        - DetailsTabPage (TabPage)

            - TitleGroup (グループ)

                - HeaderTitle (文字列)
                - *EntityStatus (グループ) \[オプション\]*

                    - StatusFields (1…N)

            - CategoryTab (タブ スタイル = タブ)

                - CategoryTabPage (TabPages *反復 3..N*)

                    - TabHeader (グループ)
                    - DetailsTab (タブ スタイル =FastTabs)

                        - DetailsTabPage (TabPages *反復 1..N*)

        - GridTabPage (TabPage)

            - CustomFilterGroup (グループ)

                - QuickFilter
                - *OtherFilters ($ フィールド)\[0..N\]*

            - MainGrid (グリッド)
            - MainGridDefaultAction (CommandButton)

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に DetailsMaster パターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  フォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    3.  **TabPage.Caption** は空ではありません。

### <a name="related-patterns"></a>関連するパターン

-   [詳細トランザクション](details-transaction-form-pattern.md)
-   [簡易リストと詳細](simple-list-details-form-pattern.md)

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)
-   [入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md)
-   [カスタム フィルター グループ](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 **標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**詳細マスターガイドライン**

-   **新規** ボタンおよび **削除** ボタンは重複してはいけません。
-   従来のタブではなく、フィールドをグループ化するのにクイック タブを使用する必要がありますか。 詳細マスター / 標準タブ パターンは、関連するこれらのクイック タブを従来のタブにグループ化します。
    -   **既定** の状態で、最初のクイック タブのコンテンツはスクロールせずに完全に表示される必要があります。
    -   **クイック タブ** ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **ActionPane** ガイドラインは、ActionPane ガイドライン セクションの[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **ページ タイトル エリア:**
    -   "&lt;ID&gt; : &lt;Description&gt;" という形式を使用する必要があります。
    -   リスト ページが詳細ページにマージされている場合は、詳細ページへのリンクをメイン メニューで提供する必要があります。
    -   ページ タイトルは、複数フォームの形式にする必要があります。
-   **情報ボックス** ガイドラインは、[情報ボックスのフォーム パターン](factbox-form-patterns.md) ドキュメントに統合されました。
-   **ナビゲーション リスト グリッド:**
    -   リスト スタイル グリッドは、グリッド行内に行が 3 行以上にまたがるフィールドはありません。
        -   通常は IDと説明だけで十分です。
        -   2 つ以上のフィールドが必要です。
-   **グリッド ビュー:**
    -   グリッドには 2 〜 15 個のフィールドがあります。 通常はすべての必須フィールドが含まれているので、グリッド内にレコードを作成できます。
    -   リンクされているフィールドを使用すると、ユーザーは選択したレコードの詳細を開くことができます。
    -   クイック フィルターの既定値は、フィルター シナリオに最も可能性が高いフィールドに設定されます。
    -   **グリッド:**
        -   **ID** フィールドは最初の列にする必要があります (グリッドで必要な場合)。 それ以外の場合、**名前** フィールドは最初の列にする必要があります。
        -   追加のグリッド ガイドラインは、グリッド ガイドライン セクションの [全般的なフォームのガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

## <a name="examples"></a>例
### <a name="details-master-basic"></a>詳細マスター (基本)

フォーム: **CustTable**

#### <a name="details-view-navigation-list-off"></a>詳細ビュー (ナビゲーション リスト オフ)

[![詳細マスター (基本) の例: 詳細ビュー (ナビゲーション リスト オフ)](./media/detailsmaster5-1024x510.png)](./media/detailsmaster5.png)

#### <a name="details-view-navigation-list-on"></a>詳細ビュー (ナビゲーション リスト オン)

[![詳細マスター (基本) の例: 詳細ビュー (ナビゲーション リスト オン)](./media/detailsmaster6-1024x509.png)](./media/detailsmaster6.png)

#### <a name="grid-view"></a>グリッド ビュー

[![詳細マスター (基本) の例: グリッド ビュー](./media/detailsmaster7-1024x509.png)](./media/detailsmaster7.png)

### <a name="details-master-with-standard-tabs"></a>標準タブによる詳細マスター

フォーム: **HcmWorker**

#### <a name="details-view-navigation-list-off"></a>詳細ビュー (ナビゲーション リスト オフ)

[![詳細マスター / 標準タブの例: 詳細ビュー (ナビゲーション リスト オフ)](./media/detailsmaster8-1024x508.png)](./media/detailsmaster8.png)

#### <a name="details-view-navigation-list-on"></a>詳細ビュー (ナビゲーション リスト オン)

[![標準タブの例による詳細マスター: 詳細ビュー (ナビゲーション リスト オン)](./media/detailsmaster9-1024x508.png)](./media/detailsmaster9.png)

#### <a name="grid-view"></a>グリッド ビュー

[![標準タブ例による詳細マスター: グリッド ビュー](./media/detailsmaster10-1024x509.png)](./media/detailsmaster10.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

なし。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

#### <a name="ax-2012-links"></a>AX 2012 リンク
-   [AX 2012 MSDN 詳細のフォーム](https://msdn.microsoft.com/library/hh397318.aspx)

#### <a name="ax-2012-example"></a>AX 2012 の例

##### <a name="details-master-basic"></a>詳細マスター (基本)

[![AX 2012 の例: 詳細マスター (基本) 1](./media/detailsmaster11-1024x647.png)](./media/detailsmaster11.png) 

[![AX 2012 の例: 詳細マスター (基本) 2](./media/detailsmaster12-1024x647.png)](./media/detailsmaster12.png)

##### <a name="details-master-with-standard-tabs"></a>標準タブによる詳細マスター

[![AX 2012 の例: 標準タブ 1 による詳細マスター](./media/detailsmaster13-1024x726.png)](./media/detailsmaster13.png) 

[![AX 2012 の例: 標準タブ 2 による詳細マスター](./media/detailsmaster14-1024x620.png)](./media/detailsmaster14.png)



