---
title: ツールバーおよびリストのサブパターン
description: この記事では、ツールバーとリストのフォームのサブパターンについて説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 15931
ms.assetid: a60f829b-e496-453b-9e58-f7cb4d67114f
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28c459ec155a3a1e1af29d39238cd328fc77640e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358499"
---
# <a name="toolbar-and-list-subpattern"></a>ツールバーおよびリストのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、ツールバーとリストのフォームのサブパターンについて説明します。 このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。 

## <a name="usage"></a>用途

このサブパターンは、親エンティティの子コレクションを表形式グリッドまたはツリーのいずれかとして表示するために使用されます。 ツールバーに含まれるアクションは 10 個未満です。 グリッドを使用している場合は、10 未満のフィールドが含まれます。 この記事では、2 つのパターンについて説明します。

-   **ツールバーおよびリスト** – これはパターンの基本的なバージョンであり、既定で使用する必要があります。
-   **ツールバーおよびリスト (二重)** – このバリアントには、2 つのリストおよび各リストの上のオプションのツールバーが含まれます。

## <a name="wireframes"></a>ワイヤーフレーム
### <a name="toolbar-and-list"></a>ツールバーおよびリスト

[![ツールバーとリストのフォームのワイヤーフレーム。](./media/toolbarlist1.png)](./media/toolbarlist1.png)

### <a name="toolbar-and-list-double"></a>ツールバーおよびリスト (ダブル)

[![ツールバーとリスト (ダブル) のフォームのワイヤーフレーム。](./media/toolbarlist2.png)](./media/toolbarlist2.png)

## <a name="model"></a>モデル
### <a name="toolbar-and-list--high-level-structure"></a>ツールバーおよびリスト - 高度なレベル構造

- \[コンテナー\]

    - *ツールバー (ActionPane、スタイル = ストリップ) \[オプション\]*
    - *CustomFilterGroup (グループ) \[オプション\]*
    - グリッド | ツリー | ListView | テーブル
    - *フッター (グループ) \[オプション\]*

### <a name="toolbar-and-list-double--high-level-structure"></a>ツールバーおよびリスト (ダブル) - 高度なレベル構造

- \[コンテナ\]

    - *ツールバー1 (ActionPane、スタイル = ストリップ) \[オプション\]*
    - *CustomFilterGroup1 (グループ) \[オプション\]*
    - グリッド | ツリー | ListView | テーブル
    - *ツールバー2 (ActionPane、スタイル = ストリップ) \[オプション\]*
    - *CustomFilterGroup2 (グループ) \[オプション\]*
    - グリッド | ツリー | ListView | テーブル
    - *フッター (グループ) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

-   ToolbarList サブパターンをコンテナー コントロールに適用します。
-   BP 警告に対処します。
    -   **Grid.DataSource** を空にすることはできません。
    -   繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。

### <a name="related-patterns"></a>関連するパターン

-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**ツールバー** **ガイドライン:**

-   ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

## <a name="examples"></a>例
### <a name="toolbar-and-list"></a>ツールバーおよびリスト

フォーム: **VendTable (TabCommunication)** 

[![ツールバーおよびリストの例。](./media/toolbarlist3.png)](./media/toolbarlist3.png)

### <a name="toolbar-and-list-double"></a>ツールバーおよびリスト (ダブル)

フォーム: **SalesQuickQuote (TabPageExistingItems)** 

[![ツールバーおよびリスト (ダブル) の例。](./media/toolbarlist4.png)](./media/toolbarlist4.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-patterns"></a>通常、パターンによって使用される

-   [簡易リストと詳細](simple-list-details-form-pattern.md)
-   [目次](table-of-contents-form-pattern.md)
-   [詳細マスター](details-master-form-pattern.md)
-   [詳細トランザクション](details-transaction-form-pattern.md)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   **CommandButton.Command には、既定のアイコン、ラベル、およびツールチップを提供する追加アクションと削除アクションが含まれていますか。**
    -   まだありません。 配送できる 1052359 は、追加および削除コマンドの既定設定を調べます。
-   **移行コンテキストでアイコンのグループ間の区切り記号は重要ですか。**
    -   現在、ツールバーのボタン グループ間の区切り記号を表示しません。

### <a name="microsoft-dynamics-ax-2012-content"></a>Microsoft Dynamics AX 2012 コンテンツ

**VendTable** 

[![以前のバージョンの例。](./media/toolbarlist5.png)](./media/toolbarlist5.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]