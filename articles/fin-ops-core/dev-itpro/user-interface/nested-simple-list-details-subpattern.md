---
title: 入れ子になった簡易リストおよび簡易詳細のサブパターン
description: このトピックでは、子エンティティまたは子エンティティに関する情報を表示するために使用される入れ子になった簡易リストおよび詳細 (NSL+D) サブパターンに関する情報を提供します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 14741
ms.assetid: f71aa535-8480-4ed8-b0c9-404f3e6285dd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c24e7a02554cd1ef3baeba4371a8c68bdbb3588e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357488"
---
# <a name="nested-simple-list-and-details-subpattern"></a>入れ子になった簡易リストおよび簡易詳細のサブパターン

[!include [banner](../includes/banner.md)]

このトピックでは、ネストされた簡易リストと詳細 (NSL+D) サブパターンについての情報を提供します。 このサブパターンは、子エンティティが別のフォーム タイプ内に存在するとき、セカンダリ エンティティ、すなわち、その子エンティティに関する情報を表示するために使用されます。

## <a name="usage"></a>用途

この記事では、ネストされた簡易リストと詳細 (NSL + D) サブパターンという名前の簡易リストと詳細 (SL + D) パターンの変形について説明します。 SL&D フォーム パターンは、フォーム上の主エンティティに関する情報の表示に使用されます。一方、NSL + D サブパターンは、別のフォーム タイプ内にその子エンティティが表示される場合、セカンダリ エンティティまたは子エンティティに関する情報の表示に使用されます。 子エンティティに関連する情報は、グリッド (10 以上のフィールド) には多すぎるが、子エンティティ自体のフォームには足りない量である必要があります。 NSL+D サブパターンは、SL+D フォーム パターンを少し異なります。

-   別の NSL+D サブパターン内では NSL+D サブパターンを入れ子にしない場合があります。
-   NSL + D サブパターンは、コンテキスト アクションのツール バーを使用します。
-   NSL+D サブパターンの詳細部分は、SL+D パターンよりも単純です。 NSL + D サブパターンはグループのみ使用しますが、SL+D パターンはコンテンツをクイック タブに整理します。

## <a name="wireframe"></a>ワイヤーフレーム

![簡易リストと詳細パターンのワイヤーフレーム。](./media/nestedsimplelistanddetails1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   このパターンは新しいものです。 SL+D パターンへのパターンの変更は、[簡易リストと詳細](simple-list-details-form-pattern.md)パターン ドキュメントで確認できます。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- &lt;コンテナ&gt;

    - ActionPane (ActionPane Style=Strip)
    - ContainerBody (グループの列 = 2)

        - ListContainer (グループ)

            - グリッド | ツリー | ListView

        - DetailsContainer (グループ)

            - DetailsHeader (グループ)
            - *DetailsGroup (グループ) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

1.  NestedSimpleListDetails サブパターンをコンテナー コントロールに適用します。
2.  必要な BP チェックを解決します。
    1.  **Grid.Datasource=&lt;セカンダリ データ ソース&gt;** に設定します。
    2.  グリッド データ ソース **InsertIfEmpty**=**No** を設定します。
    3.  **ActionPane.DataSource**=**&lt;グリッドと同じデータ ソース&gt;** を設定します。
    4.  ツール バー コマンドの追加プロパティを設定します。
    5.  ツール バー コマンドの削除プロパティを設定します。
    6.  グリッドのデータ ソースが読み取り専用の場合は、ツールバーに **追加**/**削除** ボタンがあることを確認します。

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

**標準フォーム ガイドライン**

-   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**入れ子になった簡易リスト & 詳細ガイドライン**

-   **新規** ボタンまたは **削除** ボタンは重複してはいけません。
-   **グリッド** は、パターンのリスト部分に使用します。
    -   グリッドは、**list-style** グリッドにする必要があります。
    -   リスト スタイル グリッドでは、リスト スタイル グリッドの各レコードに 3 行 (行) まで表示します。 通常は IDと説明だけで十分です。
    -   データが存在しないとき、グリッド コントロールは新しいレコードを自動的に追加できません。
-   **詳細** セクションがコンテナー本体の右側に表示されます:
    -   グリッドに表示されているのと同じ順序で、グリッドの列を Details Header Group の最初のフィールドとして表示します。
    -   レコードが追加されるとき、フォーカスは詳細セクションの最初のフィールドに移動するはずです。

## <a name="examples"></a>例
フォーム: **HcmJob** (**TaskTabPage**) [![入れ子になった簡易リストおよび詳細サブパターンの例。](./media/nestedsimplelistanddetails2.png)](./media/nestedsimplelistanddetails2.png)

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

-   **入れ子になったパターンの詳細領域には、クイック タブを配置すべきではありません。フレームワークが確認/適用します。**
    -   現在のところ、このパターン内ではタブの種類を許可していません。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![例。](./media/nestedsimplelistanddetails3.png)](./media/nestedsimplelistanddetails3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]