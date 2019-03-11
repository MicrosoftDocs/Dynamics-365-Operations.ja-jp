---
title: フィールドおよびフィールド グループのサブパターン
description: このトピックでは、フィールドおよびフィールド グループ フォームのサブパターンについて説明します。
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 12384
ms.assetid: f3bf8d00-8e6d-4af7-ab7e-3ff47fce9e21
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfe48630c2bfda898a800b0c2452c35fbb0fd051
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368680"
---
# <a name="fields-and-field-groups-subpattern"></a>フィールドおよびフィールド グループのサブパターン

[!include [banner](../includes/banner.md)]

このトピックでは、フィールドおよびフィールド グループ フォームのサブパターンについて説明します。 これは、最も一般的なデータ入力サブパターンです。 複数のフィールドまたはフィールドのグループを表示するのに動的な数の列を使用します。

<a name="usage"></a>用途
-----

フィールドおよびフィールド グループは最も一般的なデータ入力サブパターンであり、複数のフィールドまたはフィールドのグループを表示する動的列の数を使用します。 このサブパターンは、動的な高さや幅を持つコントロール (グリッド、ツリー、ラジオボタン、リストボックス、リストビューなどの)、または高さや幅の大きいコントロール (Chart など) では使用されません。 このパターン内のグループ コントロールを使用して、ラベルの下のフィールドをグループ化するか、テーブル フィールド グループにバインドすることができます。

### <a name="typical-contents"></a>標準的な内容

-   クイック タブの直接の子としてのグループまたはフィールド
-   フィールドを含むグループ
-   他のサブパターンを含めることができます:
    -   水平フィールドおよびボタン グループ

## <a name="wireframe"></a>ワイヤーフレーム
[![FieldsFieldGroups(1)](./media/fieldsfieldgroups1.png)](./media/fieldsfieldgroups1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   フィールドを 2 つ以上の列に強制するため、明示的な列とグループの使用を削除しました。
-   固定列から動的列に変更されました。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- \[コンテナー\] (列 = 入力)

    - *フィールド グループ (グループ)\[0..N\]*

        - フィールド ($Field) \[1..N\]
        - *ActionableFields (グループ)\[0..N\]* 水平フィールドとボタン グループ サブパターンを模倣します

    - *フィールド ($ フィールド)\[0..N\]*
    - *ActionableFields (グループ)\[0..N\]*

### <a name="core-components"></a>コア コンポーネント

-   FieldsAndFieldGroups サブパターンをコンテナー コントロールに適用します。
-   BP 警告に対処します。
    -   繰り越されたチェックである AX6.3 BP 以外に必要な追加の BP チェックはありません。

### <a name="related-patterns"></a>関連するパターン

-   [水平フィールドおよびボタン グループ](horizontal-fields-buttons-group-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **標準フォーム ガイドライン:**
    -   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   **フィールドおよびフィールド グループのガイドライン:**
    -   グループ内のフィールドは、ページ全体を越えて移動する必要があります。 [![FieldsFieldGroups(2)](./media/fieldsfieldgroups2.png)](./media/fieldsfieldgroups2.png)
    -   可能な場合は、不要なフィールド グループのラベルを削除します。
    -   フィールドが分かりやすくグループ分けされていることを確認します。
    -   すべてのフィールドがラベルを持つグループにあるか、またはグループ ラベルを表示しないかです。

## <a name="examples"></a>例
フォーム: **InventLocation (LocationNames)** [![FieldsFieldGroups(3)](./media/fieldsfieldgroups3.png)](./media/fieldsfieldgroups3.png)

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

-   ツールでは、パターン定義のコンテンツを模倣する代わりに、HorizontalFieldsButtonsGroup サブパターンを明示的に使用できるようにする必要があります。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

**InventLocation** [![FieldsFieldGroups(4)](./media/fieldsfieldgroups4.png)](./media/fieldsfieldgroups4.png)
