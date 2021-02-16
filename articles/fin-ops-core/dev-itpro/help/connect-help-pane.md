---
title: カスタム ヘルプ Web サイトを [ヘルプ] ウィンドウに接続する
description: このトピックでは、製品内の [ヘルプ] ウィンドウをカスタム ヘルプ コンテンツで拡張する方法について説明します。
author: edupont04
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 4a950e20c4c333acf58d8a16a817eb611177b791
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685099"
---
# <a name="connect-a-custom-help-website-to-the-help-pane"></a>カスタム ヘルプ Web サイトを [ヘルプ] ウィンドウに接続する

[!include [banner](../includes/banner.md)]

Finance and Operations ソリューションのカスタム ヘルプ コンテンツを提供する場合は、**ヘルプ** ウィンドウを拡張して、コンテンツを使用することができます。 Microsoft Visual Studio の Finance and Operations 開発環境を使用して、この 1 回限りのコンフィギュレーションを完了します。 完了したら、ユーザーは、タスク ガイド、Microsoft ヘルプ コンテンツ、ヘルプ コンテンツのタブを選択できます。

[カスタム ヘルプ Web サイト](custom-help-overview.md#custom-help-sites) を製品内 **ヘルプ** ウィンドウに接続するプロセスには、次の手順があります:

1. Visual Studio の **ヘルプ** ウィンドウを拡張します。
2. 言語にインデックスを割り当てます。
3. 言語のフォールバックをカスタマイズします。

> [!IMPORTANT]
> 以下の手順には、Visual Studio で Finance and Operations アプリの開発ツールが必要です。 詳細については、[Visual Studio の開発ツール](../dev-tools/development-tools-overview.md) を参照してください。

## <a name="extend-the-help-pane-and-assign-the-custom-help-indexes-to-languages"></a><a name="extendhelppane"></a>[ヘルプ] ウィンドウを拡張してカスタム ヘルプ インデックスを言語に割り当てる

[カスタム ヘルプ ツールキット](custom-help-toolkit.md) の **ヘルプ ウィンドウ拡張** フォルダには、Finance and Operations 開発環境で開くことができる **AzureSearchCustomHelp** ソリューションが含まれています。 このフォルダには、Visual Studio のソリューションにインポートできる **HelppaneOption.axpp** プロジェクトも含まれています。

### <a name="extend-the-help-pane"></a>[ヘルプ] ウィンドウを拡張する

1. Finance and Operations 開発環境で、**AzureSearchCustomHelp.sln** ソリューションを開きます。
2. **Dynamics 365** メニューで、**プロジェクトのインポート** を選択します。
3. **ファイル名** フィールドで、**HelppaneOption.axpp** プロジェクトのパスを指定し、**OK** を選択してインポート プロセスを完了します。 参照が欠落しないように参照を更新します。
4. **HelppaneMacro** ファイルで、次のパラメータの値を更新します:

    - **\[WebAppName\]** – [Web アプリの作成](walkthrough-help-azure.md#webapp) で作成した Web アプリの名前を指定します。 たとえば、**MyCustomHelpWebApp** を指定します。
    - **管理キー値** – Azure Cognitive Search サービスの管理キーを指定します。 キーは、[Azure ポータル](https://portal.azure.com/) の検索サービスの左側にある **設定** の **アクセス キー** にあります。
    - **\[SearchServiceName\]** – [検索サービスの作成](walkthrough-help-azure.md#searchservice) で作成した検索サービスの名前を指定します。 たとえば、**mycustomhelpsearch** を指定します。

    次の例は、HelppaneMacro ファイルのコンテンツを示します。

    ```
    #define.webApp('http://[WebAppName].azurewebsites.net/')
    #define.queryApiKey('Admin key value')
    #define.defaultstring('dashboard')
    #define.searchservicename('[SearchServiceName]')
    #define.CustomResultError('error')
    #define.CustomTabPage('CustomTabPage')
    #define.CustomHelp('Custom Help')
    #define.CustomTitle('CustomTitle')
    #define.htm('html')
    ```

5. オプション: **ヘルプ** ウィンドウに表示されるユーザー インターフェイス (UI) の文字列を変更する場合は、**Customhelppane.en-US.label.txt** ファイルを編集します。

次に、カスタム ヘルプの検索インデックスが使用する言語を指定する必要があります。

### <a name="assign-a-custom-index-to-a-language"></a>言語にカスタム インデックスを割り当てる

1. ソリューションで **Language.config** ファイルを開きます。
2. 一覧で、インデックスの言語を検索し、**index=""**、**parentindex=""**、または **ultimateindex=""** キーを使用してインデックス名を指定します。

    たとえば、英語 (米国) とドイツ語 (オーストリア) の検索インデックスを作成し、それぞれ **myenusindex** と **mydeatindex** という名前を付けたとします。 この場合、エントリは次のようになります。

    ```
    <add language="en-US" ultimateindex="myenusindex" />
    <add language="de-AT" parentlanguage="de" index="mydeatindex" />
    ```

3. オプション: 次のセクションで説明するように、インデックスの言語のフォールバックをカスタマイズします。
4. **AzureSearchCustomHelp** ソリューションを構築します。

結果は、顧客プロジェクトの資産ライブラリまたは Microsoft Dynamics Lifecycle Services (LCS) のソリューション プロジェクトにアップロードするモデルです。

## <a name="customize-language-fallback"></a>言語のフォールバックをカスタマイズする

*言語のフォールバック* とは、目的の言語が結果を返さないか、または存在しない場合に、**ヘルプ** ウィンドウが追加の言語で検索を実行することを意味します。

> [!NOTE]
> 追加の言語でカスタム インデックスを使用できる必要があります。

検索とフォールバックの順序には、次の優先順位があります:

1. クライアントで設定されている言語 (たとえば、**de-AT**)
2. その言語の **parentlanguage** 属性で定義されている言語 (たとえば、**\<add language="de-AT" parentlanguage="de" index="mydeindex" /\>**)
3. **ultimateindex** 属性が設定されている言語 (たとえば、**\<add language="en-US" ultimateindex="myenusindex" /\>**)

> [!IMPORTANT]
> **parentlanguage** 属性が設定されている場合は、対応する **parentindex** キーが必要です。

次のシナリオは、**language="de"** には **parentindex="indexde"** があり、**de-DE** と **de-AT** の両方が **de** の子孫であるため有効です。

```
<add language="de" parentindex="indexde"/>
<add language="de-DE" parentlanguage="de" index=""/>
<add language="de-AT" parentlanguage="de-DE" index="indexdeat"/>
```

言語の詳細については、[言語、翻訳、適応](language-locale.md#languages-translations-and-adaptations) を参照してください。

次のセクションでは、コンフィギュレーションの例を示します。

### <a name="help-content-for-one-locale"></a>1 つのロケールのヘルプ コンテンツ

このコンフィギュレーションでは、英語 (米国) のみのヘルプ コンテンツがあります。 クライアントが設定されているロケールに関係なく、ヘルプ コンテンツは英語 (米国) で表示されます。

```
<add language="en-US" ulitmateindex="indexenus"/>
```

### <a name="help-content-for-multiple-locales"></a>複数のロケールのヘルプ コンテンツ

このコンフィギュレーションでは、フランス語、ドイツ語、英語 (米国) のヘルプ コンテンツがあります。 **de** ロケールに設定されているクライアントは、ドイツ語でヘルプ コンテンツを表示し、**fr** ロケールに設定されているクライアントは、フランス語でコンテンツを表示し、他のロケールに設定されているクライアントは、コンテンツを英語 (米国) で表示します。

```
<add language="en-US" ulitmateindex="indexenus"/>
<add language="fr" parentindex="indexfr"/>
<add language="de" parentindex="indexde"/>
```

クライアントが **de** または **fr** ロケールに設定されているが、それぞれドイツ語またはフランス語のコンテンツで結果が見つからない場合は、コンテンツが使用できる場合は、結果が英語 (米国) で表示されます。

### <a name="help-content-that-uses-parent-locales"></a>親ロケールを使用するヘルプ コンテンツ

このコンフィギュレーションでは、ドイツ語、ドイツ語 (オーストリア)、英語 (米国) のヘルプ コンテンツがあります。 たとえば、オーストリアの機能に関連するトピックがいくつかありますが、それ以外はドイツ語のトピックを使用できます。

```
<add language="en-US" ulitmateindex="indexenus"/>
<add language="de" parentindex="indexde"/>
<add language="de-AT" parentlanguage="de" index="indexdeat"/>
```

クライアントが **de-AT** ロケールに設定されているが、ドイツ語 (オーストリア) コンテンツで結果が見つからない場合は、コンテンツが使用できる場合は、結果がドイツ語と英語 (米国) で表示されます。

## <a name="see-also"></a>参照

[Azure にカスタム ヘルプを展開](walkthrough-help-azure.md)  
[カスタム ヘルプ ツールキット](custom-help-toolkit.md)  
[製品およびヘルプの言語およびロケール記述子](language-locale.md)  
[Finance and Operations アプリのヘルプ エクスペリエンスのコンフィギュレーション](../../fin-ops/get-started/help-connect.md)  
[ヘルプ システム](../../fin-ops/get-started/help-overview.md)
