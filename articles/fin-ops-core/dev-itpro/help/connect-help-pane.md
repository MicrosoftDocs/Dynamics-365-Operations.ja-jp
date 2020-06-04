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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: aae6b629e262feae912ee83e74d042a112e16f9b
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367047"
---
# <a name="connect-a-custom-help-website-to-the-help-pane"></a><span data-ttu-id="4a454-103">カスタム ヘルプ Web サイトを [ヘルプ] ウィンドウに接続する</span><span class="sxs-lookup"><span data-stu-id="4a454-103">Connect a custom Help website to the Help pane</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a454-104">Finance and Operations ソリューションのカスタム ヘルプ コンテンツを提供する場合は、**ヘルプ** ウィンドウを拡張して、コンテンツを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="4a454-104">If you deliver custom Help content for a Finance and Operations solution, you can extend the **Help** pane so that it consumes that content.</span></span> <span data-ttu-id="4a454-105">Microsoft Visual Studio の Finance and Operations 開発環境を使用して、この 1 回限りのコンフィギュレーションを完了します。</span><span class="sxs-lookup"><span data-stu-id="4a454-105">You complete this one-time configuration by using the Finance and Operations development environment in Microsoft Visual Studio.</span></span> <span data-ttu-id="4a454-106">完了したら、ユーザーは、タスク ガイド、Microsoft ヘルプ コンテンツ、ヘルプ コンテンツのタブを選択できます。</span><span class="sxs-lookup"><span data-stu-id="4a454-106">After you've finished, users can select among tabs for task guides, Microsoft Help content, and your Help content.</span></span>

<span data-ttu-id="4a454-107">[カスタム ヘルプ Web サイト](custom-help-overview.md#custom-help-sites) を製品内 **ヘルプ** ウィンドウに接続するプロセスには、次の手順があります:</span><span class="sxs-lookup"><span data-stu-id="4a454-107">The process for connecting your [custom Help website](custom-help-overview.md#custom-help-sites) to the in-product **Help** pane involves the following steps:</span></span>

1. <span data-ttu-id="4a454-108">Visual Studio の **ヘルプ** ウィンドウを拡張します。</span><span class="sxs-lookup"><span data-stu-id="4a454-108">Extend the **Help** pane in Visual Studio.</span></span>
2. <span data-ttu-id="4a454-109">言語にインデックスを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="4a454-109">Assign an index to a language.</span></span>
3. <span data-ttu-id="4a454-110">言語のフォールバックをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="4a454-110">Customize language fallback.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a454-111">以下の手順には、Visual Studio で Finance and Operations アプリの開発ツールが必要です。</span><span class="sxs-lookup"><span data-stu-id="4a454-111">The procedures that follow require the development tools for Finance and Operations apps in Visual Studio.</span></span> <span data-ttu-id="4a454-112">詳細については、[Visual Studio の開発ツール](../dev-tools/development-tools-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a454-112">For more information, see [Development tools in Visual Studio](../dev-tools/development-tools-overview.md).</span></span>

## <a name="extend-the-help-pane-and-assign-the-custom-help-indexes-to-languages"></a><a name="extendhelppane"></a><span data-ttu-id="4a454-113">[ヘルプ] ウィンドウを拡張してカスタム ヘルプ インデックスを言語に割り当てる</span><span class="sxs-lookup"><span data-stu-id="4a454-113">Extend the Help pane and assign the custom Help indexes to languages</span></span>

<span data-ttu-id="4a454-114">[カスタム ヘルプ ツールキット](custom-help-toolkit.md) の **ヘルプ ウィンドウ拡張** フォルダには、Finance and Operations 開発環境で開くことができる **AzureSearchCustomHelp** ソリューションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a454-114">The **Help Pane extension** folder of the [Custom Help Toolkit](custom-help-toolkit.md) contains the **AzureSearchCustomHelp** solution that you can open in the Finance and Operations development environment.</span></span> <span data-ttu-id="4a454-115">このフォルダには、Visual Studio のソリューションにインポートできる **HelppaneOption.axpp** プロジェクトも含まれています。</span><span class="sxs-lookup"><span data-stu-id="4a454-115">That folder also contains the **HelppaneOption.axpp** project that you can then import into the solution in Visual Studio.</span></span>

### <a name="extend-the-help-pane"></a><span data-ttu-id="4a454-116">[ヘルプ] ウィンドウを拡張する</span><span class="sxs-lookup"><span data-stu-id="4a454-116">Extend the Help pane</span></span>

1. <span data-ttu-id="4a454-117">Finance and Operations 開発環境で、**AzureSearchCustomHelp.sln** ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="4a454-117">In the Finance and Operations development environment, open the **AzureSearchCustomHelp.sln** solution.</span></span>
2. <span data-ttu-id="4a454-118">**Dynamics 365** メニューで、**プロジェクトのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a454-118">On the **Dynamics 365** menu, select **Import project**.</span></span>
3. <span data-ttu-id="4a454-119">**ファイル名** フィールドで、**HelppaneOption.axpp** プロジェクトのパスを指定し、**OK** を選択してインポート プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="4a454-119">In the **File name** field, specify the path of the **HelppaneOption.axpp** project, and then select **OK** to complete the import process.</span></span> <span data-ttu-id="4a454-120">参照が欠落しないように参照を更新します。</span><span class="sxs-lookup"><span data-stu-id="4a454-120">Update the references so that no references are missing.</span></span>
4. <span data-ttu-id="4a454-121">**HelppaneMacro** ファイルで、次のパラメータの値を更新します:</span><span class="sxs-lookup"><span data-stu-id="4a454-121">In the **HelppaneMacro** file, update the values of the following parameters:</span></span>

    - <span data-ttu-id="4a454-122">**\[WebAppName\]** – [Web アプリの作成](walkthrough-help-azure.md#webapp) で作成した Web アプリの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a454-122">**\[WebAppName\]** – Specify the name of the web app that you created in [Create a web app](walkthrough-help-azure.md#webapp).</span></span> <span data-ttu-id="4a454-123">たとえば、**MyCustomHelpWebApp** を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a454-123">For example, specify **MyCustomHelpWebApp**.</span></span>
    - <span data-ttu-id="4a454-124">**管理キー値** – Azure Cognitive Search サービスの管理キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="4a454-124">**Admin key value** – Specify the admin key for the Azure Cognitive Search service.</span></span> <span data-ttu-id="4a454-125">キーは、[Azure ポータル](https://portal.azure.com/) の検索サービスの左側にある **設定** の **アクセス キー** にあります。</span><span class="sxs-lookup"><span data-stu-id="4a454-125">You can find the key in **Access keys** under **Settings** on the left of the search service in the [Azure portal](https://portal.azure.com/).</span></span>
    - <span data-ttu-id="4a454-126">**\[SearchServiceName\]** – [検索サービスの作成](walkthrough-help-azure.md#searchservice) で作成した検索サービスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a454-126">**\[SearchServiceName\]** – Specify the name of the search service that you created in [Create a search service](walkthrough-help-azure.md#searchservice).</span></span> <span data-ttu-id="4a454-127">たとえば、**mycustomhelpsearch** を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a454-127">For example, specify **mycustomhelpsearch**.</span></span>

    <span data-ttu-id="4a454-128">次の例は、HelppaneMacro ファイルのコンテンツを示します。</span><span class="sxs-lookup"><span data-stu-id="4a454-128">The following example shows the content of the HelppaneMacro file.</span></span>

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

5. <span data-ttu-id="4a454-129">オプション: **ヘルプ** ウィンドウに表示されるユーザー インターフェイス (UI) の文字列を変更する場合は、**Customhelppane.en-US.label.txt** ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="4a454-129">Optional: If you want to change any of the user interface (UI) strings that appear in the **Help** pane, edit the **Customhelppane.en-US.label.txt** file.</span></span>

<span data-ttu-id="4a454-130">次に、カスタム ヘルプの検索インデックスが使用する言語を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a454-130">Next, you must specify the language that the search index for your custom Help is intended for.</span></span>

### <a name="assign-a-custom-index-to-a-language"></a><span data-ttu-id="4a454-131">言語にカスタム インデックスを割り当てる</span><span class="sxs-lookup"><span data-stu-id="4a454-131">Assign a custom index to a language</span></span>

1. <span data-ttu-id="4a454-132">ソリューションで **Language.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4a454-132">Open the **Language.config** file in the solution.</span></span>
2. <span data-ttu-id="4a454-133">一覧で、インデックスの言語を検索し、**index=""**、**parentindex=""**、または **ultimateindex=""** キーを使用してインデックス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a454-133">In the list, find the language of the index, and specify an index name by using the **index=""**, **parentindex=""**, or **ultimateindex=""** key.</span></span>

    <span data-ttu-id="4a454-134">たとえば、英語 (米国) とドイツ語 (オーストリア) の検索インデックスを作成し、それぞれ **myenusindex** と **mydeatindex** という名前を付けたとします。</span><span class="sxs-lookup"><span data-stu-id="4a454-134">For example, you created search indexes for English (United States) and German (Austria), and you named them **myenusindex** and **mydeatindex**, respectively.</span></span> <span data-ttu-id="4a454-135">この場合、エントリは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4a454-135">In this case, here is what your entries will look like.</span></span>

    ```
    <add language="en-US" ultimateindex="myenusindex" />
    <add language="de-AT" parentlanguage="de" index="mydeatindex" />
    ```

3. <span data-ttu-id="4a454-136">オプション: 次のセクションで説明するように、インデックスの言語のフォールバックをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="4a454-136">Optional: Customize language fallback for your index, as described in the next section.</span></span>
4. <span data-ttu-id="4a454-137">**AzureSearchCustomHelp** ソリューションを構築します。</span><span class="sxs-lookup"><span data-stu-id="4a454-137">Build the **AzureSearchCustomHelp** solution.</span></span>

<span data-ttu-id="4a454-138">結果は、顧客プロジェクトの資産ライブラリまたは Microsoft Dynamics Lifecycle Services (LCS) のソリューション プロジェクトにアップロードするモデルです。</span><span class="sxs-lookup"><span data-stu-id="4a454-138">The result is a model that you upload to the Asset library of the customer project or the solution project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="customize-language-fallback"></a><span data-ttu-id="4a454-139">言語のフォールバックをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="4a454-139">Customize language fallback</span></span>

<span data-ttu-id="4a454-140">*言語のフォールバック* とは、目的の言語が結果を返さないか、または存在しない場合に、**ヘルプ** ウィンドウが追加の言語で検索を実行することを意味します。</span><span class="sxs-lookup"><span data-stu-id="4a454-140">*Language fallback* means that the **Help** pane runs a search in additional languages if the intended language either doesn't return a result or doesn't exist.</span></span>

> [!NOTE]
> <span data-ttu-id="4a454-141">追加の言語でカスタム インデックスを使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a454-141">A custom index must be available for the additional languages.</span></span>

<span data-ttu-id="4a454-142">検索とフォールバックの順序には、次の優先順位があります:</span><span class="sxs-lookup"><span data-stu-id="4a454-142">The search and fallback order have the following order of priority:</span></span>

1. <span data-ttu-id="4a454-143">クライアントで設定されている言語 (たとえば、**de-AT**)</span><span class="sxs-lookup"><span data-stu-id="4a454-143">The language that is set in the client (for example, **de-AT**)</span></span>
2. <span data-ttu-id="4a454-144">その言語の **parentlanguage** 属性で定義されている言語 (たとえば、**\<add language="de-AT" parentlanguage="de" index="mydeindex" /\>**)</span><span class="sxs-lookup"><span data-stu-id="4a454-144">The language that is defined in the **parentlanguage** attribute for that language (for example, **\<add language="de-AT" parentlanguage="de" index="mydeindex" /\>**)</span></span>
3. <span data-ttu-id="4a454-145">**ultimateindex** 属性が設定されている言語 (たとえば、**\<add language="en-US" ultimateindex="myenusindex" /\>**)</span><span class="sxs-lookup"><span data-stu-id="4a454-145">The language that the **ultimateindex** attribute is set for (for example, **\<add language="en-US" ultimateindex="myenusindex" /\>**)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a454-146">**parentlanguage** 属性が設定されている場合は、対応する **parentindex** キーが必要です。</span><span class="sxs-lookup"><span data-stu-id="4a454-146">If the **parentlanguage** attribute is set, there must be a corresponding **parentindex** key.</span></span>

<span data-ttu-id="4a454-147">次のシナリオは、**language="de"** には **parentindex="indexde"** があり、**de-DE** と **de-AT** の両方が **de**の子孫であるため有効です。</span><span class="sxs-lookup"><span data-stu-id="4a454-147">The following scenario is valid, because **language="de"** has **parentindex="indexde"**, and both **de-DE** and **de-AT** are descendants of **de**.</span></span>

```
<add language="de" parentindex="indexde"/>
<add language="de-DE" parentlanguage="de" index=""/>
<add language="de-AT" parentlanguage="de-DE" index="indexdeat"/>
```

<span data-ttu-id="4a454-148">言語の詳細については、[言語、翻訳、適応](language-locale.md#languages-translations-and-adaptations) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a454-148">For more information about languages, see [Languages, translations, and adaptations](language-locale.md#languages-translations-and-adaptations).</span></span>

<span data-ttu-id="4a454-149">次のセクションでは、コンフィギュレーションの例を示します。</span><span class="sxs-lookup"><span data-stu-id="4a454-149">The following sections provide sample configurations.</span></span>

### <a name="help-content-for-one-locale"></a><span data-ttu-id="4a454-150">1 つのロケールのヘルプ コンテンツ</span><span class="sxs-lookup"><span data-stu-id="4a454-150">Help content for one locale</span></span>

<span data-ttu-id="4a454-151">このコンフィギュレーションでは、英語 (米国) のみのヘルプ コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="4a454-151">In this configuration, you have Help content only for English (United States).</span></span> <span data-ttu-id="4a454-152">クライアントが設定されているロケールに関係なく、ヘルプ コンテンツは英語 (米国) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a454-152">Regardless of the locale that clients are set to, they will show the Help content in English (United States).</span></span>

```
<add language="en-US" ulitmateindex="indexenus"/>
```

### <a name="help-content-for-multiple-locales"></a><span data-ttu-id="4a454-153">複数のロケールのヘルプ コンテンツ</span><span class="sxs-lookup"><span data-stu-id="4a454-153">Help content for multiple locales</span></span>

<span data-ttu-id="4a454-154">このコンフィギュレーションでは、フランス語、ドイツ語、英語 (米国) のヘルプ コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="4a454-154">In this configuration, you have Help content for French, German, and English (United States).</span></span> <span data-ttu-id="4a454-155">**de** ロケールに設定されているクライアントは、ドイツ語でヘルプ コンテンツを表示し、**fr** ロケールに設定されているクライアントは、フランス語でコンテンツを表示し、他のロケールに設定されているクライアントは、コンテンツを英語 (米国) で表示します。</span><span class="sxs-lookup"><span data-stu-id="4a454-155">Clients that are set to the **de** locale will show the Help content in German, clients that are set to the **fr** locale will show the content in French, and clients that are set to any other locale will show the content in English (United States).</span></span>

```
<add language="en-US" ulitmateindex="indexenus"/>
<add language="fr" parentindex="indexfr"/>
<add language="de" parentindex="indexde"/>
```

<span data-ttu-id="4a454-156">クライアントが **de** または **fr** ロケールに設定されているが、それぞれドイツ語またはフランス語のコンテンツで結果が見つからない場合は、コンテンツが使用できる場合は、結果が英語 (米国) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a454-156">If clients are set to the **de** or **fr** locale, but no results are found in the German or French content, respectively, results will be shown in English (United States), if content is available in that language.</span></span>

### <a name="help-content-that-uses-parent-locales"></a><span data-ttu-id="4a454-157">親ロケールを使用するヘルプ コンテンツ</span><span class="sxs-lookup"><span data-stu-id="4a454-157">Help content that uses parent locales</span></span>

<span data-ttu-id="4a454-158">このコンフィギュレーションでは、ドイツ語、ドイツ語 (オーストリア)、英語 (米国) のヘルプ コンテンツがあります。</span><span class="sxs-lookup"><span data-stu-id="4a454-158">In this configuration, you have Help content for German, German (Austria), and English (United States).</span></span> <span data-ttu-id="4a454-159">たとえば、オーストリアの機能に関連するトピックがいくつかありますが、それ以外はドイツ語のトピックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a454-159">For example, you have several topics that are related specifically to features for Austria, but topics in German can be used otherwise.</span></span>

```
<add language="en-US" ulitmateindex="indexenus"/>
<add language="de" parentindex="indexde"/>
<add language="de-AT" parentlanguage="de" index="indexdeat"/>
```

<span data-ttu-id="4a454-160">クライアントが **de-AT** ロケールに設定されているが、ドイツ語 (オーストリア) コンテンツで結果が見つからない場合は、コンテンツが使用できる場合は、結果がドイツ語と英語 (米国) で表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a454-160">If the client is set to the **de-AT** locale, but no results are found in the German (Austria) content, results will be shown in German and English (United States), if content is available in those languages.</span></span>

## <a name="see-also"></a><span data-ttu-id="4a454-161">参照</span><span class="sxs-lookup"><span data-stu-id="4a454-161">See also</span></span>

[<span data-ttu-id="4a454-162">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="4a454-162">Deploy custom Help to Azure</span></span>](walkthrough-help-azure.md)  
[<span data-ttu-id="4a454-163">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="4a454-163">Custom Help Toolkit</span></span>](custom-help-toolkit.md)  
[<span data-ttu-id="4a454-164">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="4a454-164">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)  
[<span data-ttu-id="4a454-165">Finance and Operations アプリのヘルプ エクスペリエンスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4a454-165">Configure the Help experience for Finance and Operations apps</span></span>](../../fin-ops/get-started/help-connect.md)  
[<span data-ttu-id="4a454-166">ヘルプ システム</span><span class="sxs-lookup"><span data-stu-id="4a454-166">Help system</span></span>](../../fin-ops/get-started/help-overview.md)
