---
title: ヘルプ (ビデオを含む) の拡張、カスタマイズ、および共同作業
description: この記事では、財務と運用アプリの GitHub リポジトリとマークダウン ファイルを使用するためのヒントと秘訣を示します。
author: edupont04
ms.topic: article
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.date: 05/11/2020
ms.author: edupont
ms.openlocfilehash: 105c9d938272a0481e5687b2f0a99799db83f301
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866608"
---
# <a name="extend-customize-and-collaborate-on-the-help"></a>ヘルプの拡張、カスタマイズ、および共同作業

財務と運用アプリ向け Microsoft Help のソース ファイルは、GitHub の公開リポジトリで入手できます。 ソリューション プロバイダーは、特定のソリューションのコンテンツを簡単に拡張およびカスタマイズできます。 この記事では、GitHub リポジトリとマークダウン ファイルの使用方法について説明します。

GitHub リポジトリでマークダウン ファイルを作成する方法については、[ドキュメント寄稿者ガイド](/contribute/) を参照してください。 カスタム ヘルプを配置する方法については、[カスタム ヘルプの概要](custom-help-overview.md) を参照してください。

## <a name="contribute-to-the-content"></a>コンテンツに寄稿する

GitHub の利点の 1 つは、Microsoft チームが [MicrosoftDocs/Dynamics-365-Unified-Operations-public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public) リポジトリで提供するコア コンテンツに寄稿できることです。 たとえば、他のユーザーに役立つと思われる新しい記事がある場合や、既存の記事に修正がある場合などです。 Dynamics-365-Unified-Operations-public リポジトリに寄稿する場合は、リポジトリから Dynamics-365-Unified-Operations-public リポジトリへ *プル要求* を作成できます。 次に、Microsoft チームが要求を確認し、必要に応じて変更を反映します。

また、既存のドキュメントを寄稿し、編集することもできます。 開始するには、記事の **編集** ボタン (鉛筆記号) を選択します。 次のビデオでは、Microsoft ドキュメントに寄稿する方法を示します。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE36liB]

> [!NOTE]
> Microsoft は現在、Dynamics-365-Unified-Operations-public リポジトリに対してのみプル要求を受け付けており、言語固有のリポジトリへは受け付けていません。 翻訳についてのフィードバックがある場合は、関連するリポジトリで GitHub の問題を報告できます。

## <a name="extend-and-customize-microsoft-source-content-from-github-repos"></a>GitHub リポジトリから Microsoft ソース コンテンツを拡張とカスタマイズする

Microsoft は、ソース コンテンツと Microsoft がコンテンツを翻訳する各言語について、GitHub で個別のリポジトリを使用します。 [Dynamics-365-Unified-Operations-public](https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public) リポジトリには、英語 (米国) でのソース コンテンツが含まれています。 他の言語のコンテンツにアクセスする場合は、名前はパターン **Dynamics-365-Operations\<language\>-\<country\>** に従います。 たとえば、ドイツ語 (ドイツ) のバージョンは [Dynamics-365-Operations.de-de](https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de) という名前になります。

Microsoft がコンテンツの更新を公開すると、対応する GitHub リポジトリの *メイン* ブランチが更新されます。 ソース リポジトリは毎週更新されます。 ただし、関連する言語固有のリポジトリの更新頻度は低くなります。 頻度は、新しい翻訳がいつ使用可能になるかによって異なります。 Microsoft リポジトリの 1 つをフォークする場合、優先作業プロセスに応じて、Microsoft リポジトリからの更新でフォークを毎月またはそれ以下の頻度で更新することを選択できます。 GitHub プラットフォームとツールを使用すると、Microsoft が変更したファイルを変更した場合に起こり得るマージの競合を管理することができます。 詳細については、ドキュメント作成ガイドの [ドキュメント用に Git リポジトリをローカルに設定する](/contribute/get-started-setup-local)、または GitHub のヘルプの [リポジトリをフォークする](https://help.github.com/articles/fork-a-repo/) を参照してください。

> [!IMPORTANT]
> 2021 年 4 月、パブリック ソース リポジトリの既定のブランチの名前が *ライブ* から *メイン* に変更されました。 *ライブ* ブランチに依存するスクリプトがある場合は、代わりに *メイン* に依存して更新してください。 言語固有のリポジトリの既定のブランチの名前は後で変更されます。

> [!TIP]
> Microsoftのコンテンツをそのまま取得するだけであれば、GitHub について精通している必要はありません。 詳細については、この記事の [GitHub アカウントなしでコンテンツを取得する](#get-the-content-without-a-github-account)を参照してください。 ただし、Microsoft のコンテンツを拡張またはカスタマイズする場合は、GitHub で Microsoft に参加することをお勧めします。

<!--For guidance about what the Microsoft-provided content is all about, see [User Assistance Model](../user-assistance.md).-->

### <a name="get-started-with-github"></a>GitHub の使用を開始する

GitHub および Markdown の世界で Microsoft に参加するには、新しい用語とツールについて精通している必要があります。 次のリストは主な手順の概要を示しますが、[GitHub のドキュメント](https://help.github.com/en/github) やその他のフォーラムで、追加のコンテンツ、ツール、アイデアを検索できます。

1. GitHub にサインアップします。

    詳細については、ドキュメント寄稿者ガイドの [GitHub アカウントの設定](/contribute/get-started-setup-github) と [コンテンツ作成ツールのインストール](/contribute/get-started-setup-tools) を参照してください。

2. 適切なリポジトリをフォークします。

    カスタム ヘルプ ソリューションの Microsoft コンテンツを拡張してカスタマイズするには、リポジトリのフォークを作成する必要があります。 Markdown 形式の Microsoft コンテンツをカスタマイズする場合は、関連するリポジトリを手動でフォークし、お気に入りの Markdown エディターを使用することをお勧めします。 詳細については、ドキュメント寄稿者ガイドの [ドキュメント用に Git リポジトリをローカルに設定する](/contribute/get-started-setup-local) と [ドキュメントの Git と GitHub エッセンシャル](/contribute/git-github-fundamentals) を参照してください。

    > [!TIP]
    > GitHub リポジトリを公開する必要はありません。 パブリック リポジトリをフォークすると、新しいリポジトリの設定で、リポジトリをパブリックにするか、プライベートにするか、特定の GitHub アカウントに対してのみ使用可能にするかを指定できます。

### <a name="markdown-format"></a>Markdown 形式

トピックのテキストをフォーマットするために使用される構文は、[Markdig](https://github.com/lunet-io/markdig) Flavored Markdown という名前です。 この構文は、[CommonMark](https://commonmark.org/) に準拠しています。 Markdown の使用方法の詳細については、[GitHub での記述とフォーマットの概要](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/) を参照してください。

オープンソース ツールまたはその他のツールを使用して、Microsoft Word から Markdown に変換できます。 このようにして、コンテンツを簡単にリサイクルできます。


### <a name="get-updates-from-microsoft"></a>Microsoft から更新プログラムを入手

Microsoft は、コンテンツに頻繁な変更を加えており、これらの変更は、GitHub の公開リポジトリに表示されます。 基本リポジトリである MicrosoftDocs/Dynamics-365-Unified-Operations-public は、毎週更新されます。 ただし、例えば、毎月、年 2 回、または年 1 回の更新の入手を選択できます。 翻訳リポジトリは更新頻度が低いため、必要に応じて、毎月のスケジュールや更新頻度を下げることができます。  

Microsoft から最新バージョンのコンテンツを入手するときが来たら、Git のコマンド ラインまたは GitHub デスクトップを使用できます。 GitHub のヘルプには、[このプロセスが GitBash でどのように機能するかを示す例](https://help.github.com/en/articles/merging-an-upstream-repository-into-your-fork) が用意されています。 GitHub デスクトップでは、**現在のブランチにマージ** コマンドを使用して、変更を発生元からフォークにプルします。

複数の国または地域でソリューションを使用できる場合は、コンテンツを複数の言語で使用可能にする必要がある場合があります。 Microsoft には、サポートされる各言語ごとに GitHub リポジトリがありますが、構成ファイルは基本リポジトリの英語 (米国) バージョンである MicrosoftDocs/Dynamics-365-Unified-Operations-public でのみ使用できます。 [カスタム ヘルプ ツールキット](custom-help-toolkit.md) の HtmlFromRepoGenerator ツールを使用して、ファイルを入手できます。

Microsoft リポジトリは公開されているため、コンテンツを入手するために有効な GitHub アカウントを用意する必要はありません。 ただし、少なくとも、GitHub にアクセスできるシステム アカウントを組織に用意することをお勧めします。

詳細については、[カスタム ヘルプ ツールキット](custom-help-toolkit.md) を参照してください。

## <a name="get-the-content-without-a-github-account"></a>GitHub アカウントなしでコンテンツを取得する

コンテンツに関して Microsoft との共同作業を行う必要がない場合は、GitHub アカウントを持っていなくても、GitHub から最新バージョンのコンテンツを取得できます。 たとえば、関連する GitHub リポジトリを複製するだけです。 リポジトリのクローンを作成するために、GitHub アカウントは必要ありません。 Microsoft リポジトリは公開されているため、だれでもいつでもアクセスできます。

## <a name="translate-the-content"></a>コンテンツを翻訳する

[Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md) (DTS) を使用して、独自のコンテンツまたは Microsoft が提供するコンテンツを他の言語に翻訳できます。 このサービスは Microsoft Dynamics Lifecycle Services (LCS) でホストされ、現在 Word ドキュメントおよび HTML ファイルの翻訳をサポートしています。 詳細については、[ドキュメント ファイルの翻訳](../lifecycle-services/use-translation-service-ua.md) を参照してください。

## <a name="see-also"></a>参照

[Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md)  
[ドキュメント寄稿者ガイド](/contribute/)  
[Visual Studio Code 用 Docs Authoring Pack](/contribute/how-to-write-docs-auth-pack)  
[GitHub での記述とフォーマットの概要](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/)  
[Visual Studio Code](https://code.visualstudio.com/)  
[Atom](https://atom.io/)  
[DocFx](https://dotnet.github.io/docfx/)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
