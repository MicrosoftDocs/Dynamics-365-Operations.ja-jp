---
title: Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換する
description: この記事では、Microsoft Dynamics AX のコンテンツを Dynamics 365 ソリューションで再利用する方法について説明します。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: b51c81ecdf38ebeba6a697d2c012912a0b011e01
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866587"
---
# <a name="convert-dynamics-ax-custom-help-for-use-in-dynamics-365"></a>Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換する

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012 の既存のコンテンツがある場合は、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、および Dynamics 365 Commerce で再利用できます。 ただし、まず HTML ファイルを変換して、カスタム ヘルプ環境で使用できるようにする必要があります。

## <a name="converting-ax-2012-content"></a>AX 2012 コンテンツの変換

Microsoft [カスタム ヘルプ ツールキット](custom-help-toolkit.md) には、AX 2012 の HTML ファイルを変換してカスタム ヘルプ環境で使用できるようにする Windows PowerShell スクリプト **run_ax2012.ps1** が含まれています。 スクリプトにより、AX 2012 HTML ファイルに次の変更が加えられます:

- **Microsoft.Help.F1** メタデータ名を **ms.search.form** に置き換えます。
- **Title** メタデータ名を **title** に置き換えます。
- ファイル名拡張子を **.htm** から **.html** に変更します。
- 次のメタデータを追加します。

    ```html
    <meta name="ms.search.region" content="Global" />
    <meta name="ms.search.scope" content="Operations, Core" />
    <meta name="ms.dyn365.ops.version" content="AX 7.0.0" />
    <meta name="ms.search.validFrom" content="2016-05-31" />
    <meta name="ms.search.industry" content="cross" />
    ```

### <a name="running-the-script"></a>スクリプトの実行

[コマンド プロンプト] ウィンドウから次のコマンドを実行することも、Windows PowerShell でスクリプトを直接実行することもできます。

```powershell
PowerShell.exe -File run_ax2012.ps1 "Original file location" "New file location"
```

次のメタデータが現在使用されているか、インデックス作成中に使用できるように予約されています。

```html
<meta name="title" content="Title of file" />
<meta name="ms.locale" content="locale" />
<meta name="ms.search.form" content="FormAOTName" />
<meta name="description" content="Description of file" />
<meta name="ms.search.region" content="Global" />
<meta name="ms.search.scope" content="Operations, Core" />
<meta name="ms.dyn365.ops.version" content="AX 7.0.0" />
<meta name="ms.search.validFrom" content="2016-05-31" />
<meta name="ms.search.industry" content="cross" />
```

必要なメタデータの説明については、[カスタム ヘルプ トピックのメタデータ要件](preparing-content.md#metadata) を参照してください。

## <a name="moving-to-markdown"></a><a name="moving-to-markdown"></a>Markdown への移行

既存のコンテンツを Markdown に変換するために、[PanDoc](https://pandoc.org) や Word の [Writage](http://www.writage.com) プラグインなど、さまざまなサードパーティ製ツールを使用できます。

コンテンツを Markdown に変換した後で、[DocFx](https://dotnet.github.io/docfx/) などのオープン ソース ツールを使用して、Web サイトのコンテンツを生成できます。 一般に、Markdown で作業することにより、さまざまな オープン ソース ツールにアクセスできます。 詳細については、[ヘルプの拡張、カスタマイズ、および共同作業](contributor-guide.md) を参照してください。

## <a name="see-also"></a>参照

[カスタム ヘルプの概要](custom-help-overview.md)  
[カスタム ヘルプ ツールキット](custom-help-toolkit.md)  
[ヘルプの拡張、カスタマイズ、および共同作業](contributor-guide.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]