---
title: 拡張可能なコントロールのキーボード ショートカット
description: このトピックでは、拡張可能なコントロールのキーボード ショートカットを実装するための推奨される方法について説明します。
author: robinarh
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: C0E2E0F9-19C1-4CE0-A81C-1ACFA841F6AB
ms.search.region: Global
ms.author: robinarh
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 31e66922bd98ff832b172d3928dd910aa5bb2071
ms.sourcegitcommit: a3fbcd63f10f204350a058a124ba80abeb34309e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2019
ms.locfileid: "2564133"
---
# <a name="keyboard-shortcuts-for-extensible-controls"></a>拡張可能なコントロールのキーボード ショートカット

[!include [banner](../includes/banner.md)]

キーボード ショートカットは、拡張可能コントロールを作成するときの重要な考慮事項です。 このトピックでは、拡張可能なコントロールのキーボード ショートカットを選択するのに役立つ情報を提供します。 また、拡張可能なコントロールのキーボード ショートカットを実装するための推奨される方法について説明します。

## <a name="overview"></a>概要
アクセシビリティに関しては、キーボード専用ユーザーがコントロールを使用できることが重要です。 したがって、キーボード ショートカットは、拡張可能コントロールを作成するときの重要な考慮事項です。 このトピックでは、キーボード ショートカットとして使用するキーの組み合わせを選択するのに役立つ情報を提供します。 ここでは、Finance and Operations アプリおよびサポートされているブラウザーで使用されているショートカット、実装を計画しているショートカット、1 つ以上のブラウザーがオーバーライドを許可しないショートカットを取り上げます。 このトピックは、拡張可能なコントロールのキーボード ショートカットを実装するための推奨の方法についても説明します。

## <a name="choosing-a-key-combination"></a>キーの組み合わせの選択
キーボード ショートカットとして使用するキーの組み合わせを選択するときは、その他の既存のショートカットを分かっていることが重要です。 この方法で、ショートカットが既存のショートカットと重複しないことを保証できます。 既存のショートカットと衝突しようとすると、次のいずれかの結果が発生する可能性があります。

- この新しいキーボード ショートカットは、ブラウザーがそのキーの組み合わせを上書きすることを許可していないか、フレームワーク提供のショートカットが新しいショートカットよりも優先されるため動作しない可能性があります。
- 新しいキーボード ショートカットを使用すると、想定されているキーボード機能が削除されることがあります。これは、ユーザーが特定のキーの組み合わせによってブラウザー内の特定の機能を実行するためです。 または、フレームワークによって指定されたショートカットまたはその他のコントロール ショートカットを上書きすることによって、キーボード専用のユーザーは使用いようにすることもできます。

これらの潜在的な問題のため、キーの組み合わせを選択する際はこのガイダンスに従うことをお勧めします。

- 現在、Finance and Operations アプリで使用されている、または今後の実装で計画されているキーの組み合わせは、選択**しない**でください。
- サポートされているすべてのブラウザーで機能するためのキーの組み合わせを選択**します**。
- サポートされているブラウザで使用されているショートカットを上書きするときは**よく**注意してください。 重要な、または頻繁に使用されるブラウザー機能のショートカットを無効にしないでください。
- コントロール固有の動作のために、より長いキーの組み合わせ (3 つのキー) を使用**します**。 ユーザー定義のキーボード ショートカット用に、短い組み合わせを予約する必要があります。
- この組み合わせはいくつかの東ヨーロッパ言語の Alt+Gr にマップされ、他のショートカットと競合するため、Ctrl+Alt を含むキーの組み合わせを選択**しない**でください。

### <a name="keyboard-shortcut-links"></a>キーボード ショートカットのリンク
Finance and Operations アプリおよびサポートされているブラウザーに記載されているキーボード ショートカットへのリンクを次に示します。

- <a href="../../fin-ops/get-started/shortcut-keys.md">キーボード ショートカット</a>
- <a href="https://support.microsoft.com/help/13805">Microsoft Edge</a>
- <a href="https://support.google.com/chrome/answer/157179">Google Chrome</a>
- <a href="https://support.microsoft.com/help/15357/windows-internet-explorer-11-keyboard-shortcuts">Internet Explorer 11</a>
- <a href="https://support.apple.com/kb/PH21483">Apple Safari</a>

### <a name="planned-keyboard-shortcuts"></a>計画されているキーボード ショートカット 
使用されているキーボード ショートカットに加えて、今後の実装が計画されているいくつかのショートカットがあります。 フレームワークによって指定されたショートカットと競合を避けるために、拡張可能なコントロールには以下のキーの組み合わせを選択しないでください。
<table>
<tbody>
<tr>
<th>ショートカット</th>
<th>機能</th>
</tr>
<tr>
<td>F3</td>
<td>最も近い QuickFilter に移動します。</td>
</tr>
<tr>
<td>Alt + F3</td>
<td>現在のコントロールの値に基づくフィルターを追加します (値によるフィルター)。</td>
</tr>
<tr>
<td>Alt + Shift + F3</td>
<td>すべてのユーザー定義のフィルターをクリアします。</td>
</tr>
<tr>
<td>F6</td>
<td>最も近いツール バーに移動します。</td>
</tr>
<tr>
<td>Shift + F7</td>
<td>トースト メッセージに移動します。</td>
</tr>
</tbody>
</table>

### <a name="browseroperating-system-keyboard-shortcuts-to-avoid"></a>ブラウザーおよびオペレーティング システムのキーボード ショートカットを回避

#### <a name="keyboard-shortcuts-that-correspond-to-important-functionality"></a>重要な機能に対応するキーボード ショートカット
以下のテーブルは、ブラウザーまたはオペレーティング システムの重要な機能に対応するキーボード ショートカットの包括的ではない、簡潔なリストです。 この表では、キーの組み合わせを選択しないでください。
<table>
<tbody>
<tr>
<th>ショートカット</th>
<th>機能</th>
</tr>
</tbody>
<tbody>
<tr>
<td>Ctrl + A</td>
<td>現在のフィールドのすべてのテキストを選択するか、ページ上のすべてのコンテンツを選択します。</td>
</tr>
<tr>
<td>Ctrl+C</td>
<td>コピー。</td>
</tr>
<tr>
<td>Ctrl + V</td>
<td>貼り付け。</td>
</tr>
<tr>
<td>Ctrl + X</td>
<td>切り取り。</td>
</tr>
<tr>
<td>F5</td>
<td>ページを更新します。</td>
</tr>
<tr>
<td>Ctrl + F5</td>
<td>ページを更新し、キャッシュされたコンテンツを無視します。</td>
</tr>
<tr>
<td>Shift + F10</td>
<td>右クリックをシミュレートします。</td>
</tr>
<tr>
<td>Tab または Shift+Tab</td>
<td>前後のコントロールに移動します。</td>
</tr>
<tr>
<td>Ctrl + Tab / Ctrl + Shift + Tab</td>
<td>前後のブラウザー タブに移動します。</td>
</tr>
<tr>
<td>Alt+Tab / Alt+Shift+Tab</td>
<td>前後のアプリケーションに移動します。</td>
</tr>
<tr>
<td>Alt + 右矢印/Alt + 左矢印</td>
<td>ブラウザ履歴で、前後のページに移動します。</td>
</tr>
</tbody>
</table>

#### <a name="keyboard-shortcuts-that-cant-be-overridden-by-some-browsers"></a>ブラウザーによってオーバーライドできないキーボード ショートカット
ブラウザーによっては、以下のキーボード ショートカットを上書きできません。 したがって、ショートカットは一部のブラウザーで機能しないため、次のキーの組み合わせは選択しないでください。
<table>
<tbody>
<tr>
<td>Alt+A</td>
<td>Alt+T</td>
<td>Ctrl + F4</td>
<td>Alt+Tab</td>
</tr>
<tr>
<td>Alt+C</td>
<td>Alt+V</td>
<td>Alt + F5</td>
<td>Alt+Shift+Tab</td>
</tr>
<tr>
<td>Alt+D</td>
<td>Ctrl + W</td>
<td>Alt + F6</td>
<td>スペース バー</td>
</tr>
<tr>
<td>Alt+Shift+D</td>
<td>Ctrl + Shift + W</td>
<td>Alt + Shift + F6</td>
<td>Alt+Shift+Backspace</td>
</tr>
<tr>
<td>Alt+E</td>
<td>Alt+X</td>
<td>F12</td>
<td>Ctrl + Pause/Break</td>
</tr>
<tr>
<td>Alt+F</td>
<td>Ctrl + Shift + 0</td>
<td>Ctrl + Esc</td>
<td>Ctrl + Shift + Pause/Break</td>
</tr>
<tr>
<td>Alt+H</td>
<td>Ctrl + Shift + 7</td>
<td>Ctrl + Shift + Esc</td>
<td>Ctrl + Page up</td>
</tr>
<tr>
<td>Ctrl + N</td>
<td>F1</td>
<td>Alt+Esc</td>
<td>Ctrl + Page down</td>
</tr>
<tr>
<td>Ctrl + Shift + N</td>
<td>Ctrl + F1</td>
<td>Alt+Shift+Esc</td>
<td>Ctrl + プラス記号 (+)</td>
</tr>
<tr>
<td>Ctrl + Shift + Q</td>
<td>Ctrl + Shift + F1</td>
<td>Ctrl + Tab</td>
<td>Shift + プラス記号 (+)</td>
</tr>
<tr>
<td>Ctrl + T</td>
<td>Shift + F1</td>
<td>Ctrl + Shift + Tab</td>
<td>Ctrl + マイナス記号 (-)</td>
</tr>
</tbody>
</table>

## <a name="implementing-keyboard-shortcuts"></a>キーボード ショートカットの実装
このセクションに記載されている登録メカニズムを使用して、キーボード ショートカットを実装することをお勧めします。 この方法でコントロールのショートカットを登録すると、いくつかの利点があります。

- 必要な修飾子キーのみを指定します。 その他のモディファイアーを押すと、ショートカットは実行されません。 したがって、Ctrl + Shift +下向き矢印を押しても、Ctrl +下向き矢印に定義されたキーボード ショートカットはトリガーされません。</li>
- コードは再利用することができます。
- <strong>false</strong> をハンドラー関数で返す場合、伝達はイベントで停止しません。 <strong>true</strong> を返す場合、(または戻り値を指定しない場合)、伝達は停止されます。
- Ctrl およびメタの変更要因は同じように処理されます。 したがって、iOS と Microsoft Windows の両方で動作するキーボード ショートカットを指定できます。 たとえば、Windows でのショートカット Ctrl + G は、iOS で Meta + G に翻訳されます。
- キーボード ショートカット用の組み込みテレメトリが使用されます。

### <a name="define-a-keyboard-shortcut"></a>キーボード ショートカットを定義する

1. コントロールのプロトタイプにショートカット オブジェクトを定義します。 次に、ショートカット オブジェクト内のキーボード ショートカットを定義します。 これらのショートカットは、次の構造が必要です。 使用しようとしているキー コードが、$dyn.ui.KeyCodes オブジェクトで定義されていることを確認します。

    ```
    Shortcuts: {
        Name: {
            Keys: { modifier1: true, modifier2:true, 
                keyCode: $dyn.ui.KeyCodes.* }, 
            // Only specify the modifiers you need 
            // (between alt, ctrl/meta, shift)
            Handler: function (evt) {
                // Code to handle shortcut.
            },
            // Additional code.
    }
    ```

    キーボード ショートカットに 1 つ以上のキー コードを適用する必要がある場合は、次のように、コードの配列で渡します。

    ```
    Keys: {modifier1:true, 
        keyCode:[$dyn.ui.KeyCodes.*, $dyn.ui.KeyCodes.*, ... ] } 
    // Note: If any of these keyCodes match then the handler is called. I.E. 
    // The keyCodes in the array are OR'd not AND'd
    ```
2. 次のコードを使用して keyDown ハンドラーを追加します。

    ```
    keydown: function (event) {
        $dyn.util.handleShortcuts(this, event);
    },
    ```

3. keyDown ハンドラーをバインドします。 keyDown ハンドラーは自動的にフォーム オブジェクトにバインドされます。 その他のコントロールは、通常のバインドに関してだけ、keyDown ハンドラーに手動でバインドしてください。 

    > [!IMPORTANT]
    > 「keyDown」では、大文字と小文字が区別されます。

    ```
    <div data-dyn-bind="keyDown: $data.keydown"></div>;
    ```

### <a name="examples"></a>例
次にフォーム例を示します。

```
Shortcuts: {
    Save: {
        Keys: { ctrl: true, keyCode: $dyn.ui.KeyCodes.letterS },
        Handler: function (evt) {
            var control = evt ? $dyn.context(evt.target) : undefined;
            this.executeShortcuts(true, "SaveRecord", control);
        },
    },
    New: {
        Keys: { alt: true, keyCode: $dyn.ui.KeyCodes.letterN },
        Handler: function (evt) {
            var control = evt ? $dyn.context(evt.target) : undefined;
            this.executeShortcuts(true, "NewRecord", control);
        },
    },
    Delete: {
        Keys: { alt: true, keyCode: $dyn.ui.KeyCodes.deleteKey },
        Handler: function (evt) {
            this.executeShortcuts(false, "DeleteRecord");
        },
    },
    // Additional code
}
```

フォーム コントロールを拡張するダイアログの例を次に示します。
```
Shortcuts: $dyn.extendPrototype($dyn.controls.Form.prototype.Shortcuts, {
    InvokeDefaultButton: {
        Keys: { keyCode: $dyn.ui.KeyCodes.enter },
        Handler: function (evt) {
            this.executeShortcuts(false, "InvokeDefaultButton");
        }
    },
})
```


