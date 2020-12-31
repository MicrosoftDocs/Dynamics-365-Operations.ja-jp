---
title: 簡易リストのフォーム パターン
description: この記事では、簡易リストのフォームのパターンに関する情報を提供します。 このパターンは、単純なエンティティのデータを維持するために使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 16261
ms.assetid: 47f02822-51d5-4db2-8d99-2706548301e5
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 246bdf55159a831cde0a066a60289a1b4f6f3cbd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687808"
---
# <a name="simple-list-form-pattern"></a>簡易リストのフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、簡易リストのフォームのパターンに関する情報を提供します。 このパターンは、単純なエンティティのデータを維持するために使用されます。

<a name="usage"></a>用途
-----

簡易リスト パターンは簡易エンティティのデータを管理するために使用します。 簡易エンティティは、フィールドが 6 つ以下で、親/子関係のないエンティティです。 依然として最大 15 フィールドのエンティティが単純なエンティティと見なされている場合、いくつかの例外があります。

## <a name="wireframe"></a>ワイヤーフレーム

[![ワイヤーフレーム](./media/simplelist1-1024x578.png)](./media/simplelist1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   上部の ActionPane ストリップ コントロールが標準の ActionPane に変換されました。
-   **新規**、**削除**、および **編集** ボタンは、フレームワークによって提供されます。
-   表示モードが既定で使用されます。
-   グリッドの上にクイック フィルターが追加されました。
-   フォームが依存関係があるフォームとして使用されているとき、親フォームのレコード コンテキストがフォーム キャプションの上に自動的に表示されます。
    -   依存関係があるフォームを使用するためのページ タイトル グループは、フレームワークを提供するため削除されました。
-   このパターンでは、グリッド内での複数選択が可能です。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン

    - ActionPane (ActionPane)
    - カスタム フィルター (グループ)

        - クイック フィルター (クイック フィルター)
        - *OtherFilters ($ フィールド)\[0..N\]*

    - TabularGrid (グリッド)
    - *フッター (グループ) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に SimpleList パターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  **Design.DataSource** は空ではありません。
    3.  **Grid.Datasource** を設定する必要があります。
    4.  このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    5.  **Design.Datasource** は **Grid.Datasource** と同じに設定されます。
    6.  プライマリ データ ソースのテーブルの主キー フィールドには、**IgnoreEDTRelation**=**はい** が含まれています。
    7.  グリッドには 15 個以上のフィールドが含めることはできません。

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [カスタム フィルター グループ](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**簡易リスト ガイドライン:**

-   既定では、クイック フィルターは名前または説明列を使用する必要があります。
-   リストには最大 15 の列を表示できます。

    **注記:** このガイドラインは AX 2012 から緩和されています。

-   **新規** ボタンまたは **削除** ボタンは重複してはいけません。
-   ページ タイトルは、複数フォームの形式にする必要があります。
-   データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。

## <a name="examples"></a>例
フォーム: **CustGroup** 

[![簡易リストの例](./media/simplelist2-1024x524.png)](./media/simplelist2.png) 

**注記:** 将来のクライアントの成果物では、グリッド線を右端と下端に延長する予定です。

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

この時点ではありません。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![AX 2012 の例](./media/simplelist3.png)](./media/simplelist3.png)
