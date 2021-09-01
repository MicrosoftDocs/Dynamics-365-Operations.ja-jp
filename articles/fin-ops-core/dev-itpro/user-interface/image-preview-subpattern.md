---
title: 画像のプレビューのサブパターン
description: この記事では、イメージ プレビュー フォームのサブパターンについて説明します。 このサブパターンは、フォーム コンテナ内に表示されるほとんどの画像に使用できます。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 12444
ms.assetid: ac176ec7-7f14-47b8-908c-d2175a29fc5c
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 909314cfdf62ddc7e07c076453e0b324be2995f1a06ed0642358f993718b4be2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745106"
---
# <a name="image-preview-subpattern"></a>画像のプレビューのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、イメージ プレビュー フォームのサブパターンについて説明します。 このサブパターンは、フォーム コンテナ内、特にクイック タブまたはグループ内に表示されるほとんどの画像に使用できます。 

## <a name="usage"></a>用途

イメージ プレビューは、特にクイック タブまたはグループ内のフォーム コンテナー内に表示される大部分のイメージで使用できます。 このサブパターンは、FieldsAndFieldGroup サブパターンと FillText サブパターンと一緒に使用して、画像と関連するフィールドを結合することができます。 このサブパターンは、タイルまたはボタンに対しては、あるいはフィールド ステータス イメージに対しては使用されません。

### <a name="typical-contents"></a>標準的な内容

-   ツールバー (ActionPane、**スタイル**=**ストライプ**)
-   画像
-   サブパターンを含めることができます:
    -   フィールドおよびフィールド グループ
    -   テキスト入力

## <a name="wireframe"></a>ワイヤーフレーム
[![画像プレビューのワイヤーフレーム。](./media/imagepreview1.png)](./media/imagepreview1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   フィールドは、任意のフィールドがある場合、画像の右側にあります。
-   画像の上のアクション ウィンドウは関連付けられたアクション (たとえば、アップロードおよび選択) に使用できます。

## <a name="model"></a>モデル
### <a name="image-only--high-level-structure"></a>イメージのみ – 高度なレベル構造

- \[コンテナー\] (列 = 固定 – 1)

    - *ツール バー (ActionPane) \[オプション\]*
    - 画像

### <a name="image-and-fields--high-level-structure"></a>イメージやフィールド – 高度なレベル構造

- \[コンテナー\] (列 = 固定 – 1)

    - *ツール バー (ActionPane) \[オプション\]*
    - 画像
    - グループ化

        - 画像
        - グループ - メモ: フィールドのサブパターンを使用

### <a name="core-components"></a>コア コンポーネント

-   画像のプレビューのサブパターンをコンテナー コントロールに適用します。
-   BP 警告に対処します。
    -   繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。

### <a name="related-container-patterns"></a>関連するコンテナー パターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [テキスト入力](fill-text-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。

-   **画像のプレビューのガイドライン:**
    -   すべてのフィールドは画像の右側に配置する必要があります。

## <a name="examples"></a>例
フォーム: **RetailVisualProfile** **(ログイン)** 

[![画像プレビューの例。](./media/imagepreview2.png)](./media/imagepreview2.png)

## <a name="resources"></a>リソース
### <a name="typically-used-by-patterns"></a>通常、パターンによって使用される

-   [詳細マスター](details-master-form-pattern.md)
-   [詳細トランザクション](details-transaction-form-pattern.md)
-   [簡易詳細](simple-details-form-pattern.md)
-   [簡易リストと詳細](simple-list-details-form-pattern.md)
-   [目次](table-of-contents-form-pattern.md)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

なし。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

[![画像プレビューの例。](./media/imagepreview3.png)](./media/imagepreview3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]