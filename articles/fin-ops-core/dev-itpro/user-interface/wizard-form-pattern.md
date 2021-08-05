---
title: ウィザードのフォーム パターン
description: この記事では、ウィザードのフォーム パターンに関する情報を提供します。 ウィザードは、ユーザーがタスクを実行するためのユーザー アシスタンス フォームです。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 14671
ms.assetid: 564b88d7-85f5-488a-bbbe-19eff7194321
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7e5a74a8c01e7e1f4b19d268eca760288866156
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359337"
---
# <a name="wizard-form-pattern"></a>ウィザードのフォーム パターン

[!include [banner](../includes/banner.md)]

この記事では、ウィザードのフォーム パターンに関する情報を提供します。 ウィザードは、順序付けられた一連のタブ ページを使用して、ユーザーがタスクを実行するユーザー アシスタントの特別なフォームです。

## <a name="usage"></a>用途

ウィザードは、順序付けられた一連のタブ ページを使用して、ユーザーがタスクを実行するユーザー アシスタントの特別なフォームです。 ウィザードは、学習または実行が難しい複雑または頻度の低いタスクで、または頻繁に実行する面倒なタスクで特に便利です。

## <a name="wireframe"></a>ワイヤーフレーム

[![ウィザード フォームのワイヤーフレーム。](./media/wizard1-1024x574.png)](./media/wizard1.png)

## <a name="pattern-changes"></a>パターンの変更
Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。

-   ウィザード ステップの 2 番目の指示は、そのステップの [タブ] ページのヘルプ テキスト プロパティですでに定義されていました。 この指示はタブページで静的テキスト コントロールとしてモデル化されるようになりました。

## <a name="model"></a>モデル
### <a name="high-level-structure"></a>高レベル構造体

- デザイン (スタイル = ウィザード; キャプション =&lt;ウィザード タイトル&gt;)

    - WizardContent (Tab)

        - WizardContentPage (TabPage) *\[1..N 回繰り返し、任意の名前を付けることができます。キャプションはページ タイトルに設定します\]*

            - MainInstruction (StaticText)
            - 本文 (グループ)

### <a name="core-components"></a>コア コンポーネント

1.  **Form.Design** にウィザード パターンを適用します。
2.  BP 警告に対処します。
    1.  **Design.Caption** は空ではありません。
    2.  このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。
    3.  **TabPage.Caption** は空ではありません (すべてのウィザードのコンテンツ ページで)。
    4.  **MainInstruction.Text** が空ではありません(すべてのウィザードのコンテンツ ページ)。

### <a name="commonly-used-subpatterns"></a>一般的に使用されるサブパターン

-   [フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)
-   [ツールバーおよびリスト](toolbar-list-subpattern.md)
-   [ツールバーおよびフィールド](toolbar-fields-subpattern.md)
-   [リスト パネル](list-panel-subpattern.md)

## <a name="ux-guidelines"></a>UX ガイドライン
検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。 このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。 ブラウザーでフォームを開いて、これらの手順を確認します。 

**標準フォーム ガイドライン:**

-   標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。

**ウィザード** **ガイドライン:**

-   各タブ ページには、タイトルがあるべきです。
-   各タブ ページには、主な指示があるべきです。
-   コンテンツは、ページあたりの論理グループに分割する必要があります。
-   ウィザードには、適切なページに **&lt; 次へ &gt;** および **&lt; 前へ &gt;** ボタンがあります。
-   ユーザーはウィザードをキャンセルすることもできます。キャンセルすると、ウィザードを開始する前の状態に戻ります。
-   各ウィザード ページ (タブ ページ) ごとに、質問が 1 つだけ尋ねられます。
-   一組の選択肢がユーザーに提示されたときは、チェック ボックスまたはコンボ ボックスが条件を満たしている場合でも、オプション ボタンを使用して代替を明確にする必要があります。
-   ウィザード フォームには以下の要素を含め **ません**。
    -   情報ボックス
    -   クイック タブ

## <a name="examples"></a>例
フォーム: **WrkCtrBulkResReqEditWizard** 

![ウィザードの例。](./media/wizard2.png)

## <a name="appendix"></a>付録
### <a name="frequently-asked-questions"></a>よく寄せられる質問

このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。

### <a name="open-issues"></a>未処理の問題

-   なし

### <a name="ax-2012-content"></a>AX 2012 コンテンツ

#### <a name="ax-2012-links"></a>AX 2012 リンク

-   [Microsoft DynamicsAX\[AX 2012\] の MSDN ウィザード](/dynamicsax-2012/developer/wizards-in-microsoft-dynamics-ax)
-   [ウィザード開発のための MSDN ガイドライン \[AX 2012\]](/dynamicsax-2012/developer/guidelines-for-wizard-development)

#### <a name="ax-2012-example"></a>AX 2012 の例

[![以前のバージョンの例。](./media/wizard3.png)](./media/wizard3.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]