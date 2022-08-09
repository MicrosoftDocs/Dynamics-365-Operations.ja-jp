---
title: カスタム ヘルプ ツールキット - HtmlFromRepoGenerator ツール
description: この記事では、財務と運用アプリ用のカスタム ヘルプ ツールキットに含まれている HtmlFromRepoGenerator ツールについて説明し ます。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 2fb2593b1440201acae4385675407e4c7bc9a1fa
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067730"
---
# <a name="custom-help-toolkit-the-htmlfromrepogenerator-tool"></a>カスタム ヘルプ ツールキット: HtmlFromRepoGenerator ツール

[!include [banner](../includes/banner.md)]

カスタム ヘルプ ツールキットには、マークダウン ファイル内の Microsoft コンテンツを取得してHTML ファイルに変換する **HtmlFromRepoGenerator** ツールが含まれています。 その後、HTML ファイルを Web サイト に展開できます。

## <a name="use-the-htmlfromrepogenerator-tool-to-get-markdown-files-and-generate-html-files"></a><a name="consoleapp"></a>HtmlFromRepoGenerator ツールを使用して、マークダウン ファイルを取得し HTML ファイルを生成する

**HtmlFromRepoGenerator** ツールには、Microsoft のソース ファイルに基づくカスタム ヘルプの作成をサポートする機能が用意されています。 ツールを使用して次のタスクを実行できます:

- Microsoft ドキュメント リポジトリをクローンします。
- Microsoft リポジトリのクローンから開発者および管理者のコンテンツを削除します。
- クローンに既に存在しないファイルへのリンクを更新します。
- 財務と運用クライアントでサポートされている言語オプションと一致するように **ms.locale** プロパティの値を更新します。

    クライアントが使用する言語記述子は、対応する GitHub リポジトリで使用されている言語記述子と異なります。 ローカライズされたカスタム ヘルプを呼び出す前に、ソース コンテンツの言語記述子を変更して、クライアントの言語と一致させる必要があります。 詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。

- コンテンツの公開に使用できる HTML ファイルを生成します。

    HTML ファイルは **d365F-O** サブフォルダーに生成されます。 ファイルは、ツールの一部であるスタイル シートとテンプレートに基づいて生成されます。 詳細については、この記事の[生成された HTML ファイルのスタイル変更](#modifying-the-styling-of-the-generated-html-files)を参照してください 。

- ローカライズされた Microsoft リポジトリと en-US リポジトリを比較して、相違点を特定し、それに応じてリンクを更新します。

> [!NOTE]
> カスタム ヘルプ ツールキットの最初のバージョンでは、このツールの名前は ConsoleApp でした。 このツールの名前が変更され、2020 年に更新されました。

### <a name="syntax"></a>構文

HtmlFromRepoGenerator.exe を実行するための構文は次のとおりです。

```
HtmlFromRepoGenerator.exe --Json <Articles/> --Out <path> --ExternalText <text> [--DoNotClone <true|false>] [--Repo <URL>] [--RemoveGitFolder <true|false>] [--ReplaceUrl <URL>] [--LogsDir <.\logs>] [--EnRepo <URL>] [--EnOut <path>] [--Lng <language code>] [--Rtl] [--?[--]]
```

パラメータの説明を以下に示します。

| パラメーター | 説明 |
|-----------|-------------|
| Json | **docfx.json** ファイルの場所の相対パスを指定します。 Microsoft ドキュメント リポジトリでは、この場所は通常、**articles/** です。 |
| 出庫 | 既存の複製されたリポジトリが存在するフォルダ、またはリポジトリの複製先のフォルダを指定します。 **HtmlFromRepoGenerator** ツールを実行してリポジトリを複製する場合、このフォルダが存在していない必要があります。 [製品およびヘルプの言語およびロケール記述子](language-locale.md) で説明されているように、フォルダ名に言語名を使用します。 |
| ExternalText | **HtmlFromRepoGenerator** ツールが元のリンクを置き換える必要がある場合に、更新されたリンクに追加するテキストを指定します。 |
| DoNotClone | 以前に複製されたリポジトリに対してツールを実行する場合、このパラメータを設定します。 |
| リポジトリ | リポジトリ URL を指定します。 以前に複製されたリポジトリに対してツールを実行する場合、このパラメータはオプションです。 Microsoft ドキュメント リポジトリの URL の例には、英語 (米国) の `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` と ドイツ語 (ドイツ) の `https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de` が含まれます。|
| RemoveGitFolder| **.git** フォルダを削除するかどうかを指定します。 |
| ReplaceUrl | ターゲット ファイルが存在しない場合、ファイル間のリンクを置き換える URL を指定します。 このパラメータは、相対リンクを絶対リンクに変換するために使用します。 |
| LogsDir | ログ ファイルを保存するフォルダを指定します。 |

次の追加パラメータは、ローカライズされた Microsoft ドキュメント リポジトリに対してツールを実行するときに使用されます。

| パラメーター | 説明 |
|-----------|-------------|
| EnRepo | en-US リポジトリの URL を指定します。 以前に複製されたリポジトリに対してツールを実行する場合、このパラメータはオプションです。 英語 (米国) 用の Microsoft ドキュメント リポジトリの URL は、`https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` です。 |
| EnOut | en-US リポジトリが存在するフォルダ、または複製するフォルダを指定します。 以前に複製されたリポジトリに対してツールを実行する場合、このフォルダが存在していない必要があります。 |
| Lng | 生成された HTML ファイルの **ms.locale** メタデータに使用する言語の値を指定します。 この値は、財務と運用クライアントの言語設定で指定されている値と一致する必要があります。 このパラメーターが設定されていない場合、ツールは **en-US** を使用します。 詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。 |
| Rtl | 言語が右から左 (RTL) の書式設定を使用する場合、このパラメータを含めます。 RTL 言語の例としては、アラビア語とヘブライ語があります。 |

## <a name="examples"></a>例

> [!NOTE]
> Microsoft リポジトリには多数のファイルが含まれているため、プロセスに数分かかります。 複数のローカライズされたリポジトリに対してツールを実行すると、プロセスに時間がかかります。

次の例では、en-US リポジトリを複製し、en-US の HTML ファイルを生成します。

```dos
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\en-US" --repo "https://github.com/MicrosoftDocs/Dynamics-365-unified-Operations-public" --externalText "(This is an external link)" --replaceUrl "https://docs.microsoft.com/en-us/dynamics365/supply-chain" --LogsDir D:\D365-Operations\logs\en-US
```

次の例では、以前に複製された en-US リポジトリを使用し、en-US の HTML ファイルを生成します。

```dos
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\en-US" --externalText "(This is an external link)" --replaceUrl "https://docs.microsoft.com/en-us/dynamics365/supply-chain" --LogsDir D:\D365-Operations\logs\en-US
```

次の例では、de-DE と en-US リポジトリを複製し、de の HTML ファイルを生成します。

```dos
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\de" --repo "https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de" --externalText "(This is an external link)" --EnRepo "https://github.com/MicrosoftDocs/Dynamics-365-unified-Operations-public" --EnOut "D:\D365-Operations\en-us" --replaceUrl "https://docs.microsoft.com/de-de/dynamics365/supply-chain" --lng "de" --LogsDir D:\D365-Operations\logs\de
```

次の例では、既存の de-DE と en-US リポジトリを使用し、de の HTML ファイルを生成します。 既存の de-DE リポジトリを使用する場合、そのリポジトリが最新であることを確認してください。

```dos
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\de" --DoNotClone --externalText "(This is an external link)" --enOut "D:\D365-Operations\en-us" --replaceUrl "https://docs.microsoft.com/de-de/dynamics365/supply-chain" --lng "de" --LogsDir D:\D365-Operations\logs\de
```

> [!IMPORTANT]
> **HtmlFromRepoGenerator** ツールは処理中にリンクを変更するため、以前に複製されたリポジトリに対してHtmlFromRepoGenerator.exe を複数回実行しないでください。 同じコンテンツに対して複数回実行すると、リンクが正しくなりません。 HtmlFromRepoGenerator.exe を再実行する場合、**HtmlFromRepoGenerator** ツールを使用してリポジトリの新しい複製を作成するか、既存の複製に対して行われたローカルの変更をすべて元に戻します。

## <a name="modifying-the-styling-of-the-generated-html-files"></a>生成された HTML ファイルのスタイルの変更

**HtmlFromRepoGenerator** ツールが生成する HTML ファイルは、一連の事前定義されたテンプレートに基づいています。 ほとんどの場合、**d365F-O\\styles** フォルダーのスタイル シートを編集して、コンテンツの外観を変更できます。

高度なシナリオでは、**HtmlFromRepoGenerator** ツールが使用するテンプレートを変更できます。 ソース ファイルは、GitHub リポジトリの **SourceCode** フォルダーに含まれています。 このテンプレートは、**SourceCode\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\»Resources** サブフォルダーにあります。

> [!NOTE]
> テンプレートを変更する場合、HtmlFromRepoGenerator.exe を再構築する必要があります。

詳細については、[DocFX テンプレート システムの概要](https://dotnet.github.io/docfx/tutorial/intro_template.html) を参照してください 。

## <a name="see-also"></a>参照

[カスタム ヘルプ ツールキット](custom-help-toolkit.md)  
[カスタム ヘルプの概要](custom-help-overview.md)  
[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)  
[Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
