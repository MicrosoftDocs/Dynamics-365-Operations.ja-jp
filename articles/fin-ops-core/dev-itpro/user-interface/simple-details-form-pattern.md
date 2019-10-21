---
title: 簡易詳細のフォーム パターン
description: この記事では、簡易詳細のフォーム パターンについて説明します。 このパターンは、フィールドの単純なセットだけがユーザーに提示されなければならない場合に使用されます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 14791
ms.assetid: ee67618d-edc8-4bc5-bccc-6872c4af6273
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba6d9dd397a4aefa0b24ae4f2d42df7ee9301a9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183038"
---
# <a name="simple-details-form-pattern"></a>簡易詳細のフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、簡易詳細のフォーム パターンについて説明します。 このパターンは、フィールドの単純なセットだけがユーザーに提示されなければならない場合に使用されます。

<a name="usage"></a>用途
-----

簡易詳細パターンは、フィールドの単純なセットだけがユーザーに提示されなければならない場合に使用されます。 例には、合計および顧客残高の表示が含まれます。 通常、シンプル・ディテール・パターンではビュー・モードが使用されます。 ただし、フォームが編集可能な情報を提供する場合、編集モードは親フォームに同期される必要があります。 このドキュメントでは、4 つのパターンについて説明します。

-   **ツールバーおよびフィールド付き簡易詳細** – これは基本の簡易詳細パターンで、複数のフィールドがこのフォームで表示されます。 これらのフィールドは、オプションでグループ内に表示されます。
-   **クイック タブ付き簡易詳細** – これは、フィールドがクイック タブに編成されているときに使用する簡易詳細パターンです。
-   **標準タブ付き簡易詳細** – これは、フィールドが標準タブに編成されているときに使用する簡易詳細パターンです。
-   **パノラマ付き簡易詳細** – これは、情報がパノラマ形式で表示されることを意図された情報の場合に使用する簡易詳細パターンです。

## <a name="wireframe"></a>ワイヤーフレーム

[![ワイヤーフレーム](./media/simpledetails1-1024x578.png)](./media/simpledetails1.png)

## <a name="pattern-changes"></a>パターンの変更
現在のバージョンの Microsoft Dynamics AX にこのパターンを使用するための計画された変更はありません。

## <a name="model"></a>モデル
### <a name="simple-details-wtoolbar-and-fields--high-level-structure"></a>ツール バーおよびフィールド付き簡易詳細: 高度レベル構造

- デザイン

    - ActionPane (ActionPane)
    - 本文 (グループ) – **注記:** フィールドのサブパターンが使用されます。

### <a name="simple-details-wfasttabs--high-level-structure"></a>クイック タブ付き簡易詳細 – 高レベル構造

- デザイン

    - ActionPane (ActionPane)
    - *HeaderGroup (グループ) \[オプション\]*
    - 本文 (タブ、Style=FastTabs)

        - BodyTabPages (TabPage 反復 1..N)

    - *FooterGroup (グループ) \[オプション\]*

### <a name="simple-details-wstandard-tabs--high-level-structure"></a>標準タブ付き簡易詳細 – 高レベル構造

- デザイン

    - ActionPane (ActionPane)
    - *HeaderGroup (グループ) \[オプション\]*
    - 本文 (タブ、Style=Tabs)

        - BodyTabPages (TabPage 反復 1..N)

    - *FooterGroup (グループ) \[オプション\]*

### <a name="simple-details-wpanorama--high-level-structure"></a>パノラマ付き簡易詳細 – 高レベル構造

- デザイン

    - ActionPane (ActionPane)
    - 本文 (タブ、Style=Panorama)

        - BodyTabPages (TabPage 反復 1..N)

    - *FooterGroup (グループ) \[オプション\]*

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** に SimpleDetails パターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    3.  **TabPage.Caption** は空ではありません。
    4.  MainMenu に、SimpleDetails フォームを参照するメニュー項目を含めないでください。

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)
-   [表形式フィールド](tabular-fields-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 **標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Dynamics AX の[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**簡易詳細** **ガイドライン:**

-   フォーム ページには、エンティティを正確に説明するフォーム キャプションが表示される必要があります。
    -   フォーム キャプションは、単数形にする必要があります。

## <a name="examples"></a>例
### <a name="simple-details-wtoolbar-and-fields"></a>ツール バーおよびフィールド付き簡易詳細

フォーム: **AgreementLine** 

[![ツールバーおよびフィールド付き簡易詳細](./media/simpledetails2-1024x688.png)](./media/simpledetails2.png)

### <a name="simple-details-wfasttabs"></a>クイック タブ付き簡易詳細

フォーム: **PlanActivityServiceDetails** 

[![クイック タブ付き簡易詳細](./media/simpledetails3-1024x587.png)](./media/simpledetails3.png)

### <a name="simple-details-wstandard-tabs"></a>標準タブ付き簡易詳細

フォーム: **HcmEmploymentDateManager** (**人事管理** &gt; **共通** &gt; **作業者** &gt; **作業者**の順にクリックし、**一般** &gt; **バージョン** &gt; **職歴**の順にクリックし、それから**日付マネージャー**をクリックします。) 

[![標準タブ付き簡易詳細](./media/simpledetails4-1024x588.png)](./media/simpledetails4.png)

### <a name="simple-details-wpanorama"></a>パノラマ付き簡易詳細

フォーム: **PdsMRCEventTracker** 

[![パノラマ付き簡易詳細](./media/simpledetails5-1024x510.png)](./media/simpledetails5.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   少量の関連するコンテンツを表示する簡易詳細のフォームに、全ページ フォーム以外のプレゼンテーションを設ける必要があるかどうかを調べます。
