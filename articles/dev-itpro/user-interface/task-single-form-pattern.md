---
title: タスク シングルのフォーム パターン
description: この記事では、タスク シングル フォームのパターンに関する情報を提供します。 このパターンは、ユーザーが複数のレコードを持つ単一のデータソースから発生したと認識するデータを表示するために以前は使用されていました。
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
ms.custom: 14634
ms.assetid: 38cb1058-ed69-4ffa-9bfd-4b65cc8d2a49
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e0028ab8f5d84c42ac2166d1824117f92e68076
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512635"
---
# <a name="task-single-form-pattern"></a>タスク シングルのフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、タスク シングル フォームのパターンに関する情報を提供します。 このパターンは、ユーザーが複数のレコードを持つ単一のデータソースから発生したと認識するデータを表示するために以前は使用されていました。

<a name="usage"></a>用途
-----

このタイプのフォームは、データが複数のレコードを持つ単一のデータ ソースから発生したとユーザーが認識することを表す場合に使用されました。 新しいフォームの推奨パターンではありません。 このパターンを使用する新しいフォームを作成する必要はありません。 このパターンは、レガシー フォームの構造と安定性を提供し、より現代的なフォーム パターンへの移行パスも提供します。

## <a name="wireframe"></a>ワイヤーフレーム
[![ワイヤーフレーム](./media/tasksingle1-1024x577.png)](./media/tasksingle1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   表示モードでフォームを開きます。
-   コマンドは、ツールバー (アクション ペイン ストライプ) から標準アクション ペインに移動されています。
-   最初のタブの **概要** ラベルが **リスト** に変更されました。
-   タブ コンテナーのコンテンツは、応答レイアウトに動的列を使用します。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン

    - ActionPane (アクション ウィンドウ)
    - *CustomFilter (グループ) \[オプション\]*
    - タブ (タブ)

        - 概要 (TabPage)

            - グリッド (グリッド)
            - *RowExtension (グループ) \[オプション\]*

        - 一般 (TabPage、0..N を繰り返します)

    - *FooterGroup (グループ) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に TaskSingle パターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    3.  **TabPage.Caption** は空ではありません。
    4.  **TabPage.DataSource** は空ではありません。
    5.  **StaticText.Text** は空ではありません。

### <a name="related-patterns"></a>関連するパターン

-   [タスク ダブル](task-double-form-pattern.md)

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [カスタム フィルター グループ](custom-filter-group-subpattern.md)
-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**タスクの 1 つのガイドライン :**

-   **概要** タブは、最初のタブであり、フォームを開いたときに有効になります。
-   **全般** タブは 2 つ目のタブにする必要があり、ラベル **全般** が必要です。

## <a name="examples"></a>例
フォーム: **LedgerJournalTable** 

[![タスク シングルの例 1](./media/tasksingle2-1024x669.png)](./media/tasksingle2.png) 

[![タスク シングルの例 2](./media/tasksingle3-1024x424.png)](./media/tasksingle3.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   なし

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![AX 2012 視覚例](./media/tasksingle4.png)](./media/tasksingle4.png)
