---
title: フォーム、製品、およびコントロールのユーザー補助機能
description: この記事は、フォーム、製品、またはコントロールのユーザー補助機能を有効にするためのベスト プラクティスについて説明します。 アクセシビリティ チェックリストも含まれます。
author: jasongre
ms.date: 08/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.custom: 104943
ms.assetid: 5b97c471-212a-4487-baef-120d01063319
ms.openlocfilehash: 65036d1c13516f1ffca9e628572957c3d318277a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286682"
---
# <a name="accessibility-in-forms-products-and-controls"></a>フォーム、製品、およびコントロールのユーザー補助機能

[!include [banner](../includes/banner.md)]

この記事は、フォーム、製品、またはコントロールのユーザー補助機能を有効にするためのベスト プラクティスについて説明します。 アクセシビリティ チェックリストも含まれます。

ユーザー補助は包括的です。つまり、障害のある人は、障害のない人と同じタスクを実行できます。 アクセス可能なコントロールまたはフォームの作成は、セキュリティで保護され、高性能、または理解しやすい基本的なものにする必要があります。

## <a name="keyboard"></a>キーボード

アクセシビリティの基盤はキーボード専用アクセスです。 キーボードを使用してフォームのすべてのアクションを実行できるとき、全盲の人または手の使用に制限がある人がこのフォームを利用できます。 これは、タブ シーケンス、直接アクション (保存の **Ctrl + S** など)、またはユーザーがナビゲーション ペイン、アプリ バー、メッセージ センター、メッセージ バーなどのコントロールに移動できるようにする他のショートカット キーを使用してすべてのコントロールに到達できることを意味します。 簡単なテストでは、単にマウスを取り外し、キーボードのみを使用してすべてのコア シナリオとセカンダリ シナリオを完了します。

## <a name="color"></a>色

色の使用が推奨されており、記録やその他の情報の状態や状態を表す一般的な方法です。 ただし、色は、状態またはステータスが伝達される唯一の方法ではありません。 付属記号、ヘルプ テキスト、または追加の列に、状態またはステータスのテキスト説明を含める必要があります。 簡単なテストは、システムのすべての色の使用を識別し、色が状態またはステータスを表すために使用されていないことを確認してください。 一般的な例では、赤色は「注意が必要」を表し、緑色は「OK」の状態を意味します。

## <a name="images"></a>イメージ

画像を表示するとき、画像を説明するラベルが必要です。 イメージがレコードの状態またはステータスを表す場合は、付随するヘルプ テキストまたは追加の列に、状態またはステータスの説明文を含める必要があります。 イメージがロゴのような記号である場合は、説明は必要ありません。 「進行中」などのステータスを伝えるフォームまたはグリッド上にイメージがある場合、スクリーン リーダーを使用している人に読み取られるツールチップがイメージにあることを確認します。

```xpp
public display container statusImageDataMethod()
{
    ImageReference statusImage;
    if (this.Status == NoYes::Yes)
    {
        statusImage = ImageReference::constructForSymbol(ImageReferenceSymbol::Accept, "Accept");
        // a product ready example would use a label in place of an embedded string
    }
    else
    {
        statusImage = ImageReference::constructForSymbol(ImageReferenceSymbol::Cancel, "Cancel");  
        // a product ready example would use a label in place of an embedded string
    }
    return statusImage.pack();
}
```

## <a name="extensible-controls"></a>拡張可能なコントロール

拡張可能なコントロールは、単にフレームワークによって提供されるコントロールの拡張子ですが、同じ使いやすさとアクセシビリティが必要です。 さらに、セグメント化されたエントリ コントロールやグラフなどのウィジェットまたは他の視覚的にリッチなコントロールは、目が見えるユーザーから非表示になるアクセス可能リッチ インターネット アプリケーション (ARIA) タグを提供する必要がありますが、目の見えないユーザーにはスクリーン リーダーを通じてコントロールの使用について説明を提示します。 拡張可能コントロールのすべてのアクションは、キーボードで可能でなければなりません。

## <a name="layout-and-dynamic-management-of-forms"></a>フォームのレイアウトと動的管理

視覚に障害があるまたは盲人のユーザーが、値の選択や入力などのアクションによって、大幅にまたは予期せずにフォームの再レイアウトをするとしても驚くことはありません。

### <a name="accessibility-checklist"></a>アクセシビリティ チェックリスト

| 措置 | 説明 | 成功基準 | 検証済み (x) |
|---|--------------|----------------------|-------------------|
| すべての機能に対するキーボードのみのアクセス | ドリル ダウン、ルックアップ、ハイパーリンク、データ入力アクション、およびショートカットキー。         | すべてのアクションはマウスを使用せずに完了することができます。     | |
| 表示されているフォーカス インジケーター       |    | どのコントロールがフォーカスされているか常に明らかになります。               | |
| フォーカス注文           | 非論理的な場所に「ジャンプ」することはできません。           | タブ移動では、非論理的部分またはフォームの予期しない部分にはジャンプしません。  | |
| フォーカス トラッピング                | コントロールに「トラップ」することはできませんが、フォーカスはキーボードを使用して管理外にできる必要があります。            | コントロールにタブ移動した場合、タブ アウトや、エスケープを可能にする同等のショートカット キーを許可する必要があります。             | |
| テキストのイメージ                | イメージを使ってテキストを表示することはできません。               | たとえば、テキストの画像であるボタン ラベルを持つことはできません。 ロゴは除外されます。  | |
| 色の使用           | 色だけではステータスや状態を伝えることはできません。      | フォームまたはグリッド上のすべてのステータス インジケーターはユニークな形状または各色のためのテクスチャを持つ必要があります。 詳細については、このドキュメントの「色」セクションを参照してください。            | |
| テキストのコントラスト                 | 最低 4.5:1 の比率です。     | 拡張可能なコントロールは、コンプライアンスを確実にするためにフレームワーク カラーのテーマを使用する必要があります。      | |
| ユーザー入力の手順       | ウィジェットまたは他のマルチ ステップ コントロールには、ユーザビリティ概要ラベルまたはヘルプ テキスト (ARIA タグ内に埋め込み可能) が必要です。            | スクリーン リーダーを使用するとき、コントロールを導入とそのラベルまたは目的の説明が必要です。              | |
| コンテキストの変更             | UI コンポーネントの設定変更、またはUI コンポーネントへのデータ入力が、自動的に予期せぬコンテキストの変更を自動的に引き起こし、コンテキストの変更が発生することをユーザに最初に知らせずにユーザーを混乱させることはありません。 | たとえば、ドロップダウン ボックスで値を選択またはチェック ボックスをクリックしても、フォームのレイアウトが予期せずにまたは非標準の方法で変更されることはありません。            | |
| 整合性のある UI                 | ウィジェットまたは他の要素は製品全体で一貫して動作する必要があります。 異なる動作をする、2 つの類似した外観やモデル化された要素は存在できません。              | たとえば、チェック ボックスを選択してもウィンドウは開きません。         | |
| 優れたモーター制御            | マウスを使用する必要はありません。 「固定キー」をサポートする必要があります。             | ユーザーは、移動するターゲットをクリックするように強制したり (プル右)、マウスを必要とするその他のアクションを強制したりすることはできません。 キーボードでも同じ操作が可能でなければなりません。             | |
| ビデオの使用          | ビデオ (オーディオ付き) はテキスト付きである必要があります。     | あらかじめ記録されたコンテンツを表示するとき、聴覚に障害のある人は、コンテンツを使用するためにサポートするテキストが必要です。                | |
| イメージの使用                 |    | すべてのイメージは特定のコンテンツを説明するテキストに添付される必要があります。 たとえば、状態またはステータスを説明および一致するグリッドでの「ツールヒント」または副次列。  | |
| 通信                 | Skype などの VoIP やその他の電気通信デバイスやソフトウェアは、キーボードからアクセス可能で利用可能でなければなりません。       | VoIP または電気通信の使用は法的義務です。         | |
| ナビゲーション            |    | ナビゲーション コントロールは、実行された場合にナビゲーションが発生することを通信する必要があります。      | |

## <a name="extensible-controls--insights-for-accessibility"></a>拡張可能なコントロール - アクセシビリティのインサイト

拡張可能コントロールは、単にフレームワークの拡張です。 拡張可能なコントロールの相互作用は、他のどのフレームワーク コントロールとも変わらないと考えられるべきです。 コントロールがマウス アクションを提供する視覚的にリッチなウィジェットであるとき、作成者は、同等のキーボード アクセス機能を使用できるようにする必要があります。 ウィジェットは、標準的なプレゼンテーションとは異なる「アクセス可能モード」で実行されないことがあります。 代わりに、ウィジェットはコントロールの状態を有効化したり切り替えたりする必要なく同様の機能を提供する必要があります。 すべてのカラーの使用はテーマ カラーに基づいている必要があります。モードが「ハイ コントラスト」の場合、配色がテーマの変更と一致します。 World Wide Web コンソーシアム (W3C) Web サイトは、[サポートされている状態およびプロパティ](https://www.w3.org/WAI/PF/aria-1.1/states_and_properties) のガイダンスを提供します。 このサイトは、ARIA タグの役に立つリソースであり、以下に示す定義を提供します。

### <a name="controls-should-do-this"></a>コントロールが行う必要がある操作

#### <a name="introduce-itself"></a>それ自体を導入します

重要なことは、コントロールを名前で識別するだけではなく、(ラベルまたは ARIA タグを使用して) 動作の簡単な概要を示すべきであることです。 説明テキストがローカライズ用のフレームワーク ラベル経由で指定されていることを確認します。

- *aria describedby* - オブジェクトを説明する要素 (または複数の要素) を識別します。

#### <a name="introduce-itself---example"></a>それ自体の導入 - 例

```html
<http://www.w3.org/TR/WCAG20-TECHS/ARIA1.html>
<button aria-label="Close" aria-describedby="descriptionClose" onclick="myDialog.close()"></button>
<div id="descriptionClose">Closing this window will discard any information entered and return you to the main page</div>
```

#### <a name="indicate-when-it-is-busy"></a>ビジー状態であることを示します

視覚障害のあるユーザーにとって、なぜコントロールが反応しないのかは、必ずしも明確ではないかもしれません。 「ビジー」のメッセージを指定すると、そのような場合に役立ちます。

- *aria-busy (状態)* - 要素とそのサブツリーが現在更新されているかどうかを示します。

#### <a name="indicate-when-it-is-busy---example"></a>ビジー状態であることを示す - 例

```html
<p aria-live=”polite” aria-busy=”true”></p>
```

#### <a name="indicate-that-the-contents-have-been-validated-and-are-invalid"></a>内容が検証されて、有効でないことを示す

非同期の性質により、フィールド状態の動的な変化が発生します。 メッセージ バーは、それ自体を視覚障害のあるユーザーに紹介し、コントロール自体は無効な状態を表す必要があります。

- *aria-invalid (状態)* - 入力された値が、アプリケーションが予期している形式に準拠していないことを示します。

#### <a name="indicate-when-a-field-is-readonly"></a>フィールドが読み取りであることを示します

- *aria-readonly* - 要素が編集可能ではなく、操作可能であることを示します。 関連する *aria-disabled* を参照してください。

#### <a name="indicate-that-the-field-requires-input-mandatory"></a>フィールドに入力が必要であることを示します (必須)

視覚的なシンボルによって、目の見えるユーザーはフィールドが必須であることを理解できます。 盲目のユーザーには識別タグが必要です。

- *aria-required* - フォームが送信される前に、要素にユーザー 入力が必要であることを示します。

#### <a name="describe-the-state-of-a-toggled-value"></a>切り替えられた値の状態を説明

切り替えコントロールには切り替え状態があります。 このタグがその状態が表わしています。

- *aria-pressed (状態)* - 切り替えボタンの現在の「押された」状態を示します。 関連する *aria-checked* および *aria-selected* を参照してください。

- *aria-valuenow* - 範囲ウィジェットの現在の値を定義します。 関連する *aria-valuetext* を参照してください。

- *aria-valuetext* - 範囲ウィジェットに *aria-valuenow* の人が判読可能な代替テキストを定義します。

### <a name="controls-could-do-this"></a>コントロールが行うことができる操作

#### <a name="indicate-an-expanded-state"></a>展開された状態の表示

複雑な相互作用を学習できますが、現在の状態は実験なしでは決して簡単に判断できません。 *aria-expanded* タグを使用するとき、コントロールがその現在の状態を説明します。 例として、コントロールのタブまたはクイック タブ セクションへのタブ移動があります。

- *aria-expanded (状態)* - 要素または別のグループ化されている要素が、現在展開されているか折りたたまれているかを示します。

#### <a name="describe-applicable-context-menu"></a>適用できるコンテキスト メニューの説明

財務と運用アプリではコンテキスト メニューを提供します。 アプリケーション作成者が現在のコントロールまたはコンテキストに機能を提供したときに、ユーザーはその機能を公表することができます。

- *aria-haspopup* - 要素にポップアップ コンテキスト メニューまたはサブ レベルのメニューがあることを示します。

### <a name="other-miscellaneous-controls"></a>その他のコントロール

- *aria-live* - 要素が更新されることを示し、ユーザー エージェント、支援テクノロジー、およびユーザーがライブ リージョンから期待できる更新の種類を示します。

- *aria-multiline* - テキスト ボックスが複数行の入力を受け入れるか、一行だけを受け入れるかを示します。

- *aria-multiselectable* - ユーザーが現在選択可能な子孫からひとつ以上の項目を選択できることを示します。

- *aria-orientation* - 要素と方向が水平か垂直かを示します。

- *aria-setsize* - 現在の listitems および treeitem のセット内の項目の数を定義します。 セット内のすべての要素が DOM にある場合は必要ありません。 関連する *aria-posinset* を参照してください。

- *aria-sort* - テーブルまたはグリッド内の項目を昇順または降順でソートするかどうかを示します。

- *aria-valuemax* - 範囲ウィジェットの最大許容値を定義します。

- *aria-valuemin* - 範囲ウィジェットの最小許容値を定義します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
