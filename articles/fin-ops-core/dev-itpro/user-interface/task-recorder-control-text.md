---
title: コントロールに対してタスク レコーダーが生成するテキストの制御
description: この記事では、タスク レコーダーがコントロールに対して生成する命令ラベルを決定する方法について説明します。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 17711
ms.assetid: 9b75a1e3-cc76-4a2f-ae30-7e5a485b30b1
ms.openlocfilehash: 828d9c1c7ab2d4891570823b32b46e6a056ec5aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286674"
---
# <a name="control-the-text-that-task-recorder-generates-for-a-control"></a>コントロールに対してタスク レコーダーが生成するテキストの制御

[!include [banner](../includes/banner.md)]

この記事では、タスク レコーダーがコントロールに対して生成する命令ラベルを決定する方法について説明します。 また、これらのラベルがユーザーにとって意味があることを確認できる方法について説明します。

タスク ガイド、Microsoft Word 文書、およびヘルプ コンテンツは、可読性のためにコンテンツ作成標準に適合するように、すべてのコントロールには有用で意味のある指示ラベルが必要です。 最初に、次の 2 つの項目を定義する必要があります。

-   **コントロール ラベル** - コントロールのラベル プロパティから取得される値です。
-   **命令ラベル** – コントロールがそのコントロールの使用方法について記述する際にタスク レコーダーに指示するラベル (「OK をクリック」、「ファーストネームフィールドに「John」と入力します」など)。

コントロールがタスク レコーダーにイベントを記録するとき、次の 3 つの方法を使用して、ユーザーに表示される命令ラベルを決定できます。

-   タスク レコーダー イベントのログの一部として、コントロールは使用する正確な命令ラベル ID を指定することがあります。 ベスト プラクティスとして、ラベル ID に名前を付ける方法は以下のとおりです。\[クライアント コントロール タイプ名\]\_\[プロパティまたはコマンド名\]指示ラベル ID の手動仕様については、この記事の後半のコード例を参照してください (**OptionalInstructionLabelIDOverride**)。
-   コントロールが命令ラベル ID を明示的に指定していない場合、Task Recorder は SysTaskRecorderLabel ファイルを参照して、次の命名構文に適合する既存の命令ラベル ID を検索しようとします: \[client control type name\]\_\[property or command name\]。このタイプの命令ラベル ID が見つかった場合、タスク レコーダーはそれを使用します。
-   ラベルが、上記の方法を使用して特定できない場合、タスク レコーダは、より汎用的な指示ラベルに転用されます。 一般的な指示ラベルは、SysTaskRecorder ラベル ファイルにあります。 コマンド用の汎用命令ラベルが 1つ とプロパティ用の汎用命令ラベルがもう 1 つあります。
    -   コマンドの一般的な指示ラベルを次に示します。
        -   **ラベル ID:** CommandUserAction
        -   **ラベル文字列:** %2 %1
    -   プロパティの一般的な指示ラベルを次に示します。
        -   **ラベル ID:** PropertySetValue
        -   **ラベル文字列:** %1 フィールドに %2 と入力する

タスク レコーダーは、(前の 3 つの方法のいずれかで) 使用する命令ラベルを決定すると、次の引数を使用してそのラベルの文字列の書式設定を行います。

-   **%1** – この引数は、コントロール ラベルです。 タスク レコーダーは、対話可能なラベルを調べることによってコントロール ラベルを取得します。 ただし、コントロールはこのラベルを上書きし、個々のラベルを提供します。 この記事の後半のサンプル コードを参照してください (**OptionalControlLabelOverride**)。
-   **%2** – この引数は、値 (プロパティの場合) またはコマンド名 (コマンドの場合) のいずれかです。 この値は、イベントのロギングの一部として、コントロールがタスク レコーダーに送信した値になります。 ただし、生データの値は、エンドユーザーにとって醜いまたは意味がないものです。 したがって、コントロールでは、未処理のデータ値の代わりにタスク レコーダーが表示できる値のユーザー フレンドリなバージョンを提供することもできます。 この記事の後半のサンプル コードを参照してください (**OptionalValueLabelOverride**)。
-   **%3**–**%5** – これらはコマンド引数であり、めったに使用されません。 ただし、たとえば、グリッドはそれらを使用して行番号を記録します。

## <a name="case-study"></a>事例研究
改善の事例研究のようにチェック ボックス コントロールを使用しましょう。 現在、方法 1 または方法 2 (この記事の前のセクションを参照) のいずれかを介するチェックボックスに対して命令ラベルが指定されていません。 したがって、代わりに汎用プロパティ命令ラベルが使用されます。 他のユーザーが、**失敗した場合に情報ログを表示する** という名前のフィールドのチェック ボックスをオンにし記録する場合、現在の出荷タスク レコーダーは次のようになります。


> 失敗時に情報ログ表示フィールドで、True と入力します。

ただし、通常エンド ユーザーは、チェック ボックスを **True** に設定することの意味を理解していない場合があります。 したがって、次のようなラベルを生成するためのチェック ボックスの改善が推奨されます。

> 失敗時に情報ログ表示をチェックしてください。

こうした改善を行うには、新しいラベル ID を追加する必要があります。 その後、イベントがメソッド 1 を使用してタスク レコーダーにログオンしているときに、そのユーザーはラベル ID を使用する必要があります。

-   **ラベル ID:** Checkbox\_Value
-   **ラベル文字列:** 「%2 %1」

この変更により、次のような出力が生成されます。

> 失敗時に infolog を表示します。

これは見たいものではありません。 したがって、チェックボックスがプロパティ変更イベントをタスク レコーダーに記録すると、「チェック」または「チェック解除」のいずれかを示す特定の<*値ラベル* を渡す必要があります。 コントロールが明示的に値ラベルを指定した場合、タスク レコーダーは記録された生データ値 (この場合は **True** または **False**) の代わりにその値ラベルを使用します。 この記事の後半のサンプル コードを参照してください (**OptionalValueLabelOverride**)。 ユーザーが新しいラベルを作成し、イベントがタスク レコーダーに記録されたときの値ラベルを指定すると、コントロールは適切なテキスト出力を行います。

> 失敗時に情報ログ表示をチェックしてください。

最後に、チェック ボックスには、チェック ボックスの「例の値」を使用するため、2 番目の命令ラベルが必要です。 「値の例」は、タスク レコーダーがユーザーに対して指示ラベルを表示する特別な方法を示します。 タスク記録の作成者は、タスク ガイドが、ガイドが記録されたときに入力されたものと同じ値を入力することをユーザーに指示するかどうか、またはビジネス要件に固有の独自の値を入力することをユーザーに指示するかどうかを指定できます。 値指示ラベルの例では、以下のラベル ID 構文が表示されます。\[クライアント コントロール タイプ名\]\_\[プロパティ名\]\_チェックボックス例に対する例。値ラベルは次のようになります。

-   **ラベル ID:** Checkbox\_Value\_Example
-   **ラベル文字列:** 「%1 フィールドをオンまたはオフにします」。

次のコード例は、X++ コントロールによってプロパティ変更イベントがタスク レコーダーに記録される様子を示しています。 C++ カーネル コントロールには、同様のアプリケーション プログラミング インターフェイス (API) が存在します。 コマンド イベントに、同種の API があります。

```xpp
[FormPropertyAttribute(FormPropertyKind::Value, #MyPropertyName)]
    public str value(str_value = valueProperty.parmValue())
    {
        if(!prmIsDefault(_value))
        {
            using (var scope = SysTaskRecorder::addPropertyUserAction(#MyPropertyName, this, _value, [OptionalInstructionLabelIDOverride], [OptionalValueLabelOverride], [OptionalControlLabelOverride]))
            {
                // Property set logic goes here
                valueProperty.setValueOrBinding(_value);
            }
        }
    }
```




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
