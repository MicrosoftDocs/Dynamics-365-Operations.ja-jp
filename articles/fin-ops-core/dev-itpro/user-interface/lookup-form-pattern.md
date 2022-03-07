---
title: ルックアップのフォーム パターン
description: このトピックでは、ルックアップ フォームのパターンについて説明します。
author: jasongre
ms.date: 11/09/2017
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 005d04bfa1062e1917f9ad33e8bda6962a656f5f
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781262"
---
# <a name="lookup-form-pattern"></a>ルックアップのフォーム パターン

[!include [banner](../includes/banner.md)]

このトピックでは、ルックアップ フォームのパターンについて説明します。 標準フレームワークによって指定されたルックアップで正しいデータが提供されない場合や、データの高度な視覚化が必要な場合は、カスタム ルックアップ フォームを使用する必要があります。

## <a name="usage"></a>用途

カスタム ルックアップ フォームは、標準フレームワークによって指定されたルックアップ (通常はテーブル定義で定義された AutoLookup フィールド グループを使用して生成される)、が正しいデータを提供しない場合、またはデータの高度な視覚化が必要な場合に使用する必要があります。 このドキュメントでは、3 つのパターンについて説明します。

-   **基本のルックアップ** – これは、リストまたはツリーが 1 つだけの基本のルックアップ パターンです。オプションのカスタム フィルターとアクションもあります。
-   **タブ付きのルックアップ** – このルックアップ パターンは、ルックアップの複数のビューをユーザーが利用できるようにする場合に使用されます。 タブ キャプションは表示されません。 代わりに、タブはコンボ ボックスを通じて選択されます。
-   **プレビュー付きのルックアップ** – このより高度なルックアップ パターンにより、ルックアップ グリッドの現在のレコードのプレビューが有効になります。

## <a name="wireframe"></a>ワイヤーフレーム
### <a name="lookup-basic"></a>基本のルックアップ

[![基本ルックアップ フォームのワイヤーフレーム。](./media/lookupform1.png)](./media/lookupform1.png)

### <a name="lookup-with-tabs"></a>タブ付きルックアップ

[![タブ付きルックアップ フォームのワイヤーフレーム。](./media/lookupform2.png)](./media/lookupform2.png)

### <a name="lookup-with-preview"></a>プレビューによるルックアップ

[![プレビューによるルックアップ フォームのワイヤーフレーム。](./media/lookupform3.png)](./media/lookupform3.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの変更を次に示します。

-   タブは非表示になり、コンボ ボックスで管理されている必要があります。
-   必要に応じてスプリッター/プレビューを追加します。

## <a name="model"></a>モデル
### <a name="lookup-basic--high-level-structure"></a>基本のルックアップ – 高度なレベル構造

- デザイン

    - *CustomFilter (グループ) \[オプション\]*
    - グリッド | ツリー | ListView
    - *LookupActions (グループ) \[オプション\]*

### <a name="lookup-wtabs--high-level-structure"></a>タブ付きルックアップ – 高度なレベル構造

- デザイン

    - *CustomFilter (グループ) \[オプション\]*
    - LookupTab (タブ)

        - LookupTabPage (TabPage、反復 1..N)

            - グリッド | ツリー | ListView

    - *LookupActions (グループ) \[オプション\]*

### <a name="lookup-wpreview--high-level-structure"></a>プレビュー付きルックアップ – 高度なレベル構造

- デザイン

    - *CustomFilter (グループ) \[オプション\]*
    - LookupContent (グループ)

        - グリッド | ツリー | ListView

    - VerticalSplitter (Group)

        - プレビュー (グループ)

    - LookupActions (ActionPane)

### <a name="core-components"></a>コア コンポーネント

-   Form.Design にルックアップ パターンを適用します。
-   BP 警告に対処します。
    -   EDT.FormHelp は、Style=Lookup であるフォームを参照しなければなりません。

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [カスタム フィルター グループ](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 **標準フォーム ガイドライン**

-   標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**ルックアップのガイドライン**

-   **グリッド** ガイドラインは、グリッドガイドライン セクションの [フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。
-   ルックアップ内に別の「ビュー」(タブ) を表示する必要がある場合は、コンボ ボックスを使用して、ユーザーがタブを切り替えるようにします。
-   必要に応じてルックアップでツリー ビューを使用することができます。 また、ツリー内のデータの追加フィールドの表示が複雑であるため、標準のグリッドを提供することも検討します。
-   グリッドに 5 つ以上の列を持たないでください。 ルックアップはすべての列を表示するようにサイズ変更されるので、5 列は非常に広いです。
-   **オプション プレビュー領域**:
    -   領域は、ユーザーが複数の類似レコードから選択する場合に役立ちます。 たとえば、John Smith という名前の 2 人の従業員がいる場合、プレビューはこれら 2 人をユーザーが区別できるよう、十分な情報を提供する必要があります。
    -   プレビューでは編集可能なフィールドを表示しないでください。
-   **カスタム フィルター** ガイドラインは [カスタム フィルター グループ](custom-filter-group-subpattern.md) サブパターン ドキュメントに統合されています。

## <a name="examples"></a>例
### <a name="lookup-basic"></a>基本のルックアップ

フォーム: **SysLanguageLookup** (ナビゲーション バーで **設定** &gt; **ユーザー設定** をクリックします。) 

[![基本ルックアップの例。](./media/lookupform4.png)](./media/lookupform4.png)

### <a name="lookup-with-tabs"></a>タブ付きルックアップ

フォーム: **CaseCategoryLookup** (**共通** &gt; **共通** &gt; **ケース** &gt; **すべてのケース** の順にクリックして、詳細に移動するケースを選択します。) 

![CaseCategoryLookup のタブ付きルックアップ フォームの例。](./media/lookupform5.png)

### <a name="lookup-with-preview"></a>プレビューによるルックアップ

フォーム: **HcmWorkerLookup** (**人事管理** &gt; **共通** &gt; **組織** &gt; **職位** &gt; **職位** の順にクリックし、詳細に移動するレコードをクリックします。 **作業者の割り当て** FastTab を展開し、**新規** をクリックして、次に **ワーカー** フィールドにドロップダウンの矢印をクリックします。 

[![HcmWorkerLookup のプレビューによるルックアップ フォームの例。](./media/lookupform6.png)](./media/lookupform6.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

-   **タブ付きのルックアップ パターンのタブを切り替える方法。**
    -   タブ付きルックアップ パターンは、Tab コントロールで **ShowTabs** を **No** に意図的に設定します。 これらのフォームは、カスタム フィルター グループ内のバインドされていないコンボ ボックスをモデル化するためのものです。 このコンボ ボックスは、タブ ヘッダーの代わりにタブを切り替えるために使用されます。
    -   これを行うには、次の手順に従います。
        1.  フォーム **run()** の **SysLookup::tab2ComboBox** メソッド転記 **super** を呼び出し、コンボ ボックスにルックアップに表示されているタブからキャプションを設定します。

            ```xpp
            // Generate view combobox based on tabs
            tab2ComboBoxItemMap = SysLookup::tab2ComboBox(Tab, switchView);
            ```

        2.  コンボ ボックスで **modified()** をオーバーライドし、コンボ ボックスで選択した値に基づいて表示されるタブを更新します。

            ```xpp
            Tab.tabChanged(Tab.tabValue(), tab2ComboBoxItemMap.lookup(this.selection()));
            ```
            
### <a name="open-issues"></a>未処理の問題

-   **最近使用した値をルックアップに組み込むことはできますか。**
    -   アプリのモデリングは、今すぐこの作業を行うことができます (通貨のルックアップなど)。 この機能の全般的なフレームワークの今後のサポートを検討しています。

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

**SysLanguageLookup (基本のルックアップ)** 

![基本ルックアップ フォームの例。](./media/lookupform7.png) 

**CaseCategoryLookup (タブ付きルックアップ)** 

[![タブ付きルックアップ フォームの例。](./media/lookupform8.png)](./media/lookupform8.png) 

**HcmWorkerLookup (プレビューによるルックアップ)** 

![プレビューによるルックアップ フォームの例。](./media/lookupform9.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]