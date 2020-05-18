---
title: ローカライズ可能なラベルの作成
description: この記事では、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ可能なラベルを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 18531
ms.assetid: 73615d1b-9088-496e-989e-d8996f30e76b
ms.search.region: Global
ms.author: shshabazz
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05ba812cc76a7c5c1e90f41f85863626ade28247
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329927"
---
# <a name="create-localizable-labels"></a>ローカライズ可能なラベルの作成

[!include [banner](../includes/banner.md)]

この記事では、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ可能なラベルを作成する方法について説明します。

この記事では、クライアント コンポーネントと HTML/JavaScript コントロールの**ローカライズ可能な**ラベルを作成するプロセスについて詳しく説明します。 このプロセスでは、既存のローカライズ ツールとラベル用のプロセスを使用して、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ  サポートを提供します。 次のプロセスでは、クライアント コンポーネントと HTML/JavaScript コントロールでラベルを使用できるように、ラベル ファイルを JavaScript に相当するものにシリアル化できるラベル リソース コントローラーが使用されています。 ラベル リソース コントローラーは自動的に配置されます。 /Resources/Labels エンドポイントに配置されている MVC サービスです。

## <a name="1-create-a-label-file"></a>1. ラベル ファイルの作成
開発者ツールを使用して、コントロールの領域に新しいラベル ファイルを作成するか、コントロールの領域に既存のラベル ファイルを使用します。 コントロールの領域は、チームによって決定されます。

-   拡張可能なコントロールについては、目標として、HTM リソース ファイルごとに 1 つのラベル ファイルを作成する必要があります。 複数の HTM リソースは、同じラベルのセットを共有している場合、1 つだけのラベル ファイルが HTM リソース ファイルのセットに対して必要となります。
-   クライアント コントロールおよびコンポーネントでは、一般に、多くの同じ機能 (たとえば、入力コントロール: StringEdit、コンボボックス、チェックボックスなど) を共有するコントロールは、同じラベル ファイルも共有する必要があります。

*X ++ のみで使用されるラベルを含めて、ラベル ファイルは使用しないでください。* ラベル ファイル全体がクライアントによってロードされると、シリアル化されるため、クライアント コンポーネント/コントロールで必要とされないラベルを別のラベル ファイルに保存してください。

## <a name="2-add-label-strings-to-the-label-file"></a>2. ラベル ファイルにラベル文字列を追加する
開発者ツールを使用して、ラベル文字列をラベル ファイルに追加します。 **拡張可能なコントロールの例:**

-   **ラベル ファイル名:** ClockControl
-   **ラベル ID:** Seconds
-   **ラベル文字列:** seconds

## <a name="3-request-the-label-file-as-a-javascript-file-by-using-resource-manager"></a>3. リソース マネージャーを使用して、ラベル ファイルを JavaScript ファイルとして要求する
タグ読み込みスクリプトを使用して、JavaScript ファイルを読み込みます。 ローディング タグは、ラベル リソース コントローラーがそこにあるため、/Resources/Labels のラベル ファイルを参照する必要があります。 **注記:** 拡張可能なコントロールの場合、コントローラーは自動的にラベル ファイル名を JavaScript のラベル ID の先頭に追加します。

```javascript
<script src="/Resources/Labels/ClockControl.js"></script>
```

返される JavaScript ファイルには、次の例のようなコードが含まれます。

```javascript
Globalize.addCultureInfo("en-us", {
    messages: {
        ClockControl_Seconds: "seconds"
    }
});
```

カルチャ情報は、現在のユーザーのカルチャに基づいて自動的に挿入されます。 コントロールの部分でユーザーのカルチャの設定、変更、読み取りに必要なアクションはありません。 上記のコードは、jQuery Globalize ラベル記憶域に各ラベル文字列を追加します。 HTML と JavaScript 全体でラベルを参照することができます。 スクリプト ファイルにある JavaScript コードは、ブラウザーによってファイルが読み込まれた時点で実行されます。 したがって、ラベルはすぐに使用できる状態になります。 HTML に他のスクリプト読み込みタグの**後**、ラベルスクリプトの読み込みタグを必ず追加してください。 スクリプト読み込みタグは、上から順に処理されます。 最後にラベル スクリプトを読み込むことによって、他のスクリプトが競合を起こさないようにするか、スクリプト ラベル ファイルに設定されているラベルを上書きすることができます。

## <a name="4-use-localizable-labels-in-html-and-javascript"></a>4. HTML と JavaScript でローカライズ可能なラベルを使用する
次のフレームワーク アプリケーション プログラミング インターフェイス (API) は、HTML (内部 **data-dyn-bind**) または JavaScript でラベルにアクセスするために使用できます。 **HTML**

```javascript
<!-- Example of using a localizable label with a Label Control. Supply the label to the "Text" property on the control -->
<div data-dyn-role="Label" data-dyn-bind="Text: $dyn.label('ClockControl_Seconds')"></div>
<!-- Example of using a localizable label with a basic HTML element. Supply the label to the "text" binding handler for the element -->
<div data-dyn-bind="text: $dyn.label('ClockControl_Seconds')"></div>
```

**JavaScript**

```javascript
/* Example of using a localizable label in JavaScript. */
var string mylabel = $dyn.label('ClockControl_Seconds');
```

HTML または JavaScript の変数を介してラベル ID を渡すこともできます。 **HTML**

```javascript
<div data-dyn-bind="text: $dyn.label($data.SecondsLabel)"></div>
```

**JavaScript**

```javascript
var string mylabel = $dyn.label(self.SecondsLabel);
```

**$dyn.label** API は、適切な名前のラベルを検索し、ユーザーにテキストを表示するために使用する文字列を返します。 この API は、現在のユーザーのカルチャに基づいてラベルを自動的に選択します。

## <a name="troubleshooting"></a>トラブルシューティング
ラベル ファイルが正しく作成され、そのラベルが展開されている場合は、ブラウザから直接、ラベルファイルの JavaScript バージョンを読み込むことができます。 JavaScript のラベル ファイルには、クライアントのホーム ページに移動して、URL にパス **/Resources/Labels/MyLabelFile.js** を加えてアクセスすることができます。ここで **MyLabelFile** は言語の接尾語なしのラベル ファイル名です。 MyLabelFile.en-us という名前の配置されたラベル ファイルのについては、これらの手順に従います。

1. ホーム ページに移動して、サインインします。 (ワン ボックス配置では、ホーム ページの URL は<https://usncax1aos.cloud.onebox.dynamics.com/en/> です。)
2. 目的の言語が**オプション** &gt; **言語および地域**で設定されていることを確認します。 (目的の言語に設定されている場合は言語を変更する必要はありません。) ユーザーの言語が現在のセッションで設定されたので、ラベル リソース コントローラーは、ラベル ファイルが読み込まれるときに使用する言語を認識します。
3. JavaScript バージョンのラベル ファイルを読み込むには、<strong>Resources/Labels/MyLabelFile.js</strong> を URL に追加してラベル ファイルに移動します。 (ワン ボックス配置では、全体の URL は<https://usncax1aos.cloud.onebox.dynamics.com/en/Resources/Labels/MyLabelFile.js> です。)
4. 対応するラベル ファイルは JSON シリアル化され、ブラウザーは現在のタブにテキストを表示するか、.js ファイルのダウンロードを促すメッセージを表示します。 ファイルをダウンロードする場合、ローカルでそれを開き、検査できます。

ブラウザーにファイルが見つからない場合は、ラベルの名前を誤って入力した、またはラベルを正しく展開しなかった可能性があります。 Web フォルダー/リソース/ラベルのラベルに物理的な .js ファイルはありません。 .js ファイルは、ラベル リソース コントローラーによって動的に生成されます。

### <a name="microsoft-visual-studio-form-previewer"></a>Microsoft Visual Studioフォーム プレビューアー

フォーム プレビューアーは、ラベル リソース コントローラー経由でラベルを読み込むようには現在設定されていません。 フォーム プレビューアーは、コード ビハインド (/Resources/Scripts にあります) の .js ファイルに直接定義されているラベルのみを読み込みます。 フォーム プレビューアを更新して、ラベル リソース コントローラから .js ファイルをロードできるようになるまでは、コントロールのコード ビハインドの .js ファイルにもラベルを定義するようにしてください。 これらのラベルへの依存関係は、将来の更新で削除されます。



