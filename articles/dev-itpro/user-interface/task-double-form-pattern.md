---
title: タスク ダブルのフォーム パターン
description: この記事では、タスク ダブル フォームのパターンに関する情報を提供します。 このパターンは、以前は同じフォームに親エンティティと子エンティティを表示するために使用されていました。
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
ms.custom: 14651
ms.assetid: 9f28e5f9-efec-48c5-aaa6-b68a505c4df3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21df0b804b28f811a195e9ee4667e95886569f67
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537445"
---
# <a name="task-double-form-pattern"></a>タスク ダブルのフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、タスク ダブル フォームのパターンに関する情報を提供します。 このパターンは、以前は同じフォームに親エンティティと子エンティティを表示するために使用されていました。

<a name="usage"></a>用途
-----

このタイプのフォームは、以前は親/子エンティティを同じフォームに表示する場合に使用されていました。 新しいフォームの推奨パターンではありません。 このパターンを使用する新しいフォームを作成する必要はありません。 このパターンは、レガシー フォームの構造と安定性を提供し、より現代的なフォーム パターンへの移行パスも提供します。

## <a name="wireframe"></a>ワイヤーフレーム

[![patternTaskDouble](./media/patterntaskdouble.png)](./media/patterntaskdouble.png)[](./media/taskdouble1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   表示モードでフォームを開きます。
-   上部の ActionPane ストリップ コントロールが標準の ActionPane に変換されました。
-   親タブの **概要** ラベルが **リスト** に変更されました。
-   タブ コンテナーの内容は、応答レイアウト用の動的列を使用します。
-   子タブのリストのラベルは、**&lt;x&gt; リスト** で、ここで、**&lt;x&gt;** は、エンティティに基づいて適切な文字列に置き換えられます。 たとえば、子エンティティは通常請求と呼ばれ、タブのラベルは**請求リスト**である必要があります。
    -   例外: 子エンティティが何らかの「リスト」である場合は、末尾に「リスト」のワードは追加できません。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン

    - ActionPane (アクション ウィンドウ)
    - *CustomFilter (グループ) \[オプション\]*
    - ParentTab (Tab)

        - ParentList (TabPage) – **注記:** ツールバーとリストのサブパターンが使用されます。
        - 一般 (TabPage は 0..N を繰り返します)

    - *ParentFooterGroup (グループ) \[オプション\]*
    - HSplitter (グループ)
    - *ChildToolbar (アクション ペイン) \[オプション\]*
    - ChildTab (タブ)

        - ChildList (TabPage) – **注記:** ツールバーとリストのサブパターンが使用されます。
        - 一般 (TabPage、0..N を繰り返します)

    - *ChildFooterGroup(グループ) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** にタスク ダブルのパターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    3.  **TabPage.Caption** は空ではありません。
    4.  **TabPage.DataSource** は空ではありません。
    5.  **StaticText.Text** は空ではありません。

### <a name="related-patterns"></a>関連するパターン

-   [タスク シングル](task-single-form-pattern.md)

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [カスタム フィルター グループ](custom-filter-group-subpattern.md)
-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**タスクの二重ガイドライン:**

-   **概要** タブは、最初のタブであり、フォームを開いたときに有効になります。
-   子タブコントロールの最初のタブは、**Lines list** または適切なバリエーションと呼びます。
-   親グリッドでの選択内容により子グリッド内のコンテンツが更新されます。

## <a name="example"></a>例
フォーム: **HRMAbsenceTableHistory** 

[![タスク ダブルの例](./media/taskdouble2-1024x639.png)](./media/taskdouble2.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   なし

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![AX 2012 視覚例](./media/taskdouble3.png)](./media/taskdouble3.png)
