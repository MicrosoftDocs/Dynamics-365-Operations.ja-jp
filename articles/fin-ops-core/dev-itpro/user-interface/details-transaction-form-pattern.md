---
title: 詳細トランザクション フォーム パターン
description: この記事では、詳細トランザクションのフォーム パターンに関する情報を提供します。 このパターンを使用すると、ユーザーはヘッダーの表示と明細行の表示間で切り替えができます。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 16281
ms.assetid: 016c8e36-0abe-4b55-a575-5696761959a5
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 751548f788b38639947a15f0fc29280ea74c114d
ms.sourcegitcommit: f9201fc3f11532d82c926c4d7867375116026ca3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/05/2022
ms.locfileid: "9114275"
---
# <a name="details-transaction-form-pattern"></a>詳細トランザクション フォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、詳細トランザクションのフォーム パターンに関する情報を提供します。 このパターンを使用するフォームには、ユーザーが切り替えることができる2 つの詳細ビューがあります - ヘッダー ビューおよび明細行ビュー

## <a name="usage"></a>用途

明細行 (フォームの詳細トランザクション) を含む詳細フォームは、ユーザーが切り替えることができる 2 つの詳細ビューを持てる 1 つのフォームで構成されます。 ヘッダー ビューには、ヘッダーに関連付けられているか一部となっているすべてのフィールドが含まれます。 行ビューには、行グリッド、行の詳細、および最も重要なヘッダー フィールドのコレクションを含むセクションが含まれています。

## <a name="wireframe"></a>ワイヤーフレーム
### <a name="line-view"></a>明細行の表示

[![ワイヤーフレーム: 行の表示。](./media/detailstransaction1-1024x575.png)](./media/detailstransaction1.png)

### <a name="header-view"></a>ヘッダーの表示

[![ワイヤーフレーム: ヘッダー表示。](./media/detailstransaction2-1024x576.png)](./media/detailstransaction2.png)

### <a name="grid-view"></a>グリッド ビュー

[![ワイヤーフレーム: グリッド ビュー。](./media/detailstransaction3-1024x575.png)](./media/detailstransaction3.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   リスト スタイル グリッド が詳細ビュー コンテンツの左側に追加されました。ヘッダー ビューまた行ビューのいずれかに表示されます。
-   リスト ページと詳細マスターは、1 つのフォームにマージされました。 この変更では、次の利点があります。
    -   ユーザーが一覧と詳細の間を移動するときのパフォーマンスが向上します。
    -   初期一覧で一括編集できます。
    -   これはリスト ページのプレビュー ウィンドウの消去に使用できます。
-   表示/編集、新規作成、削除、保存、最新の情報に更新、添付、および Excel にエクスポートの各アクションはすべてファンデーションによって提供され、ファンデーションによって提供されたボタンが削除されない限り、各アクションに明示的なアプリ ボタンを使用する必要はありません。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン

    - ActionPane (ActionPane)
    - SidePanel (グループ)

        - QuickFilter
        - *CustomFilters (グループ\] \[オプション\]*
        - NavigationList (グリッド、スタイル = リスト)

    - PanelTab (Tab ShowTabs=No)

        - DetailsPanel (TabPage)

            - TitleGroup (グループ)

                - HeaderTitle (文字列)
                - *EntityStatus (グループ) \[オプション\]*

                    - StatusFields (1..N)

            - HeaderLinePanels (Tab ShowTabs=No)

                - LinePanel (TabPage PanelStyle=Line)

                    - LineViewTab (Tab Style=FastTabs)

                        - LineViewHeader (TabPage)
                        - LineViewLines (TabPage)
                        - LineViewLineDetails (TabPage)

                            - LineDetailsTab (Tab Style=Standard)

                                - LineDetailsTabPages (TabPages 1..N)

                - HeaderPanel (TabPage PanelStyle=Header)

                    - HeaderViewTab (Tab Style=FastTabs)

                        - HeaderViewTabPages (TabPages 1..N)

        - GridPanel (TabPage PanelStyle=Grid)

            - CustomFilterGroup (グループ)

                - QuickFilter
                - *OtherFilters ($ フィールド)\[0..N\]*

            - MainGrid (グリッド)
            - MainGridDefaultAction (CommandButton)

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に DetailsTransaction パターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    3.  **TabPage.Caption** は空ではありません。
    4.  **TabPage.DataSource** は空ではありません。

### <a name="related-patterns"></a>関連するパターン

-   [詳細マスター](details-master-form-pattern.md)
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

**詳細トランザクション ガイドライン**

-   **新規** ボタンおよび **削除** ボタンは重複してはいけません。
-   **ActionPane** ガイドラインは、ActionPane ガイドライン セクションの[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **既定** の状態で、最初のクイック タブのコンテンツはスクロールせずに完全に表示される必要があります。
-   **クイック タブ** ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **ページ タイトル エリア**
    -   **&lt;ID&gt; : &lt;Description&gt;** という形式を使用する必要があります。
    -   リスト ページが詳細ページにマージされてから、詳細ページへのリンクをメイン メニューで提供する必要があります。
    -   ページ タイトルは、複数フォームの形式にする必要があります。
-   **ナビゲーション リスト グリッド**
    -   リスト スタイル グリッドは、グリッド行内に行が 3 行以上にまたがるフィールドはありません。
        -   通常は IDと説明だけで十分です。
        -   2 つ以上のフィールドが必要です。
    -   最後のフィールドは、トランザクションの合計でなければなりません。
-   **グリッド ビュー**
    -   グリッドには 2 〜 15 個のフィールドがあります。 通常はすべての必須フィールドが含まれているので、グリッド内にレコードを作成できます。
    -   リンクされているフィールドを使用すると、ユーザーは選択したレコードの詳細を開くことができます。
    -   既定では、クイック フィルターはフィルター シナリオに最も可能性が高いフィールドを使用する必要があります。
    -   リスト ページを開いたときに、フォーカスがクイック フィルターにある必要があります。
    -   **グリッド**
        -   **ID** フィールドが最初の列になり、次がマスタ エンティティ **ID** および **名前** フィールドになる必要があります。
        -   追加のグリッド ガイドラインは、グリッド ガイドライン セクションの [全般的なフォームのガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
    -   **情報ボックス** ガイドラインは、[情報ボックスのフォーム パターン](factbox-form-patterns.md) ドキュメントに統合されました。

## <a name="example"></a>例
フォーム: **SalesTable**

#### <a name="line-view"></a>明細行の表示

[![詳細トランザクションの例: 明細行の表示。](./media/detailstransaction4-1024x508.png)](./media/detailstransaction4.png)

#### <a name="header-view"></a>ヘッダーの表示

[![詳細トランザクションの例: ヘッダーの表示。](./media/detailstransaction5-1024x509.png)](./media/detailstransaction5.png)

#### <a name="grid-view"></a>グリッド ビュー

[![詳細トランザクションの例: グリッド ビュー。](./media/detailstransaction6-1024x509.png)](./media/detailstransaction6.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。
 
- **なぜヘッダーの表示は義務付けられているのですか?**
    - ヘッダー ビューは、詳細トランザクション パターンに必須です。 最初、ヘッダーの表示には行の表示ヘッダーの概要情報以外にない場合があります。 ただし、時間経過に伴い、アプリケーション チーム、国際化チーム、パートナー、および顧客によりそれが追加されます。 ヘッダーの表示が今後の変更で使用できることが重要です。 さらに、一貫した信頼性の高いフォーム構造には、使い勝手とアップグレード上のメリットがあります。

- **ページ上部のレコード タイトルの右側にヘッダー/明細行ボタンが表示されなくるのはなぜですか?** 
    - ページのヘッダー部分にあるヘッダー/明細行ボタンは、再現タブの再編成されたラジオ ボタンでした。 これらのページのアクセシビリティを向上させるために、**ヘッダー/明細行のプロキシを削除するボタン** 機能はラジオ ボタンを削除し、代わりにレコード タイトルの下にヘッダーと明細行を切り替えるネイティブ タブ コントロールを表示します。 この機能を有効にする前に、この機能がテスト資産およびタスク記録に与える影響を評価する必要があります。

        > [!NOTE]
        > この機能は、財務と運用アプリのバージョン 10.0.23 のプラットフォーム更新プログラムに含まれています。

### <a name="open-issues"></a>未処理の問題

現在ありません。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

#### <a name="ax-2012-links"></a>AX 2012 リンク

-   [ユーザー エクスペリエンス ガイドラインの詳細を含む MSDN 詳細フォーム \[AX 2012\]](/dynamicsax-2012/developer/details-form-with-lines-user-experience-guidelines)
-   [MSDN 詳細フォーム \[AX 2012\]](/dynamicsax-2012/developer/details-forms)

#### <a name="ax-2012-example"></a>AX 2012 の例

##### <a name="line-view"></a>明細行の表示

[![AX 2012 の例: 明細行の表示。](./media/detailstransaction7-1024x727.png)](./media/detailstransaction7.png)

##### <a name="header-view"></a>ヘッダーの表示

[![AX 2012 の例: ヘッダーの表示。](./media/detailstransaction8-1024x727.png)](./media/detailstransaction8.png)

##### <a name="grid-view"></a>グリッド ビュー

[![AX 2012 の例: グリッド ビュー。](./media/detailstransaction9-1024x727.png)](./media/detailstransaction9.png)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

