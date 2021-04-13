---
title: ツールバーおよびフィールドのサブパターン
description: この記事では、ツールバーおよびフィールドのサブパターンについて説明します。 このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 15911
ms.assetid: c5d6aa38-1f5f-41e5-9d90-11766d34a947
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1be83f13945c258580f56e48c1916ec12a88518f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749579"
---
# <a name="toolbar-and-fields-subpattern"></a>ツールバーおよびフィールドのサブパターン

[!include [banner](../includes/banner.md)]

この記事では、ツールバーおよびフィールドのサブパターンについて説明します。 このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。 ツールバーに含まれるアクションは 10 個未満にしてください。

<a name="usage"></a>用途
-----

このコンテナー パターンは、データ フィールドのサブパターンの上にアクションを表示するために使用されます。 ツールバーに含まれるアクションは 10 個未満にしてください。

## <a name="wireframe"></a>ワイヤーフレーム

[![ツール バーおよびフィールドのサブパターンのワイヤーフレーム](./media/toolbarfields1.png)](./media/toolbarfields1.png)

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- \[コンテナー\]

    - ツールバー (ActionPane、スタイル=ストライプ)
    - ContentGroup (グループ) – **注記:** フィールドのサブパターンが使用されます。

### <a name="core-components"></a>コア コンポーネント

-   ToolbarFields サブパターンをコンテナー コントロールに適用します。
-   BP 警告に対処します。
    -   繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。

### <a name="related-patterns"></a>関連するパターン

-   [ツールバーおよびリスト](toolbar-list-subpattern.md)

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [表形式フィールド](tabular-fields-subpattern.md)
-   [分析コード式ビルダー](../financial/dimension-expression-builder-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**ツールバー** **ガイドライン:**

-   ツールバーのガイドラインは、Dynamics AX の [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

## <a name="examples"></a>例
### <a name="toolbar-and-fields"></a>ツールバーおよびフィールド

フォーム: **HcmPosition** **(WorkerAssignmentTabPage)** 

[![ツール バーおよびフィールドのサブパターンの例](./media/toolbarfields2-1024x131.png)](./media/toolbarfields2.png)

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

-   **ShowMoreLess グループは、パターンの一部にすべきですか、独自のサブパターンにする必要がありますか。**
    -   新しいパターンの追加を正当化するだけの十分な需要があるまで、**ShowMoreLess** グループをカスタム コンテナー パターンとして取り扱います。

### <a name="microsoft-dynamics-ax-2012-content"></a>Microsoft Dynamics AX 2012 コンテンツ

**HcmPosition** 

![以前のバージョンのツール バーおよびフィールド](./media/toolbarfields3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]