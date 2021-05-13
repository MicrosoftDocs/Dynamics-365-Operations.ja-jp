---
title: カスタム ヘルプ ツールキット - HtmlFromRepoGenerator ツール
description: このトピックでは、Finance and Operations アプリ用のカスタム ヘルプ ツールキットに含まれている HtmlFromRepoGenerator ツールについて説明し ます。
author: edupont04
ms.date: 05/11/2020
ms.topic: article
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 3e55b19bf0b27d7a5de1559d3cffd9c1897484e9
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897950"
---
# <a name="custom-help-toolkit-the-htmlfromrepogenerator-tool"></a><span data-ttu-id="23a6b-103">カスタム ヘルプ ツールキット: HtmlFromRepoGenerator ツール</span><span class="sxs-lookup"><span data-stu-id="23a6b-103">Custom Help Toolkit: The HtmlFromRepoGenerator tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23a6b-104">カスタム ヘルプ ツールキットには、マークダウン ファイル内の Microsoft コンテンツを取得してHTML ファイルに変換する **HtmlFromRepoGenerator** ツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="23a6b-104">The Custom Help Toolkit includes the **HtmlFromRepoGenerator** tool, which gets Microsoft content in Markdown files and converts it to HTML files.</span></span> <span data-ttu-id="23a6b-105">その後、HTML ファイルを Web サイト に展開できます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-105">You can then deploy the HTML files to a website.</span></span>

## <a name="use-the-htmlfromrepogenerator-tool-to-get-markdown-files-and-generate-html-files"></a><a name="consoleapp"></a><span data-ttu-id="23a6b-106">HtmlFromRepoGenerator ツールを使用して、マークダウン ファイルを取得し HTML ファイルを生成する</span><span class="sxs-lookup"><span data-stu-id="23a6b-106">Use the HtmlFromRepoGenerator tool to get Markdown files and generate HTML files</span></span>

<span data-ttu-id="23a6b-107">**HtmlFromRepoGenerator** ツールには、Microsoft のソース ファイルに基づくカスタム ヘルプの作成をサポートする機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="23a6b-107">The **HtmlFromRepoGenerator** tool provides functionality that supports the creation of custom Help that is based on source files from Microsoft.</span></span> <span data-ttu-id="23a6b-108">ツールを使用して次のタスクを実行できます:</span><span class="sxs-lookup"><span data-stu-id="23a6b-108">You can use the tool to perform these tasks:</span></span>

- <span data-ttu-id="23a6b-109">Microsoft ドキュメント リポジトリをクローンします。</span><span class="sxs-lookup"><span data-stu-id="23a6b-109">Clone a Microsoft documentation repository (repo).</span></span>
- <span data-ttu-id="23a6b-110">Microsoft リポジトリのクローンから開発者および管理者のコンテンツを削除します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-110">Remove developer and admin content from your clone of the Microsoft repo.</span></span>
- <span data-ttu-id="23a6b-111">クローンに既に存在しないファイルへのリンクを更新します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-111">Update links to files that are no longer present in the clone.</span></span>
- <span data-ttu-id="23a6b-112">Finance and Operations クライアントでサポートされている言語オプションと一致するように **ms.locale** プロパティの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-112">Update the value of the **ms.locale** property so that it matches the language options that are supported by the Finance and Operations client.</span></span>

    <span data-ttu-id="23a6b-113">クライアントが使用する言語記述子は、対応する GitHub リポジトリで使用されている言語記述子と異なります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-113">The language descriptors that the client uses differ from the language descriptors that are used in the corresponding GitHub repos.</span></span> <span data-ttu-id="23a6b-114">ローカライズされたカスタム ヘルプを呼び出す前に、ソース コンテンツの言語記述子を変更して、クライアントの言語と一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-114">Before localized custom Help can be called, the language descriptors in the source content must be changed so that they match the client's languages.</span></span> <span data-ttu-id="23a6b-115">詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23a6b-115">For more information, see [Language and locale descriptors in the product and in Help](language-locale.md).</span></span>

- <span data-ttu-id="23a6b-116">コンテンツの公開に使用できる HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-116">Generate HTML files that can be used to publish content.</span></span>

    <span data-ttu-id="23a6b-117">HTML ファイルは **d365F-O** サブフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-117">The HTML files will be generated in the **d365F-O** subfolder.</span></span> <span data-ttu-id="23a6b-118">ファイルは、ツールの一部であるスタイル シートとテンプレートに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-118">The files are generated based on style sheets and templates that are part of the tool.</span></span> <span data-ttu-id="23a6b-119">詳細については、このトピックの [生成された HTML ファイルのスタイル変更](#modifying-the-styling-of-the-generated-html-files) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="23a6b-119">For more information, see the [Modifying the styling of the generated HTML files](#modifying-the-styling-of-the-generated-html-files) section of this topic.</span></span>

- <span data-ttu-id="23a6b-120">ローカライズされた Microsoft リポジトリと en-US リポジトリを比較して、相違点を特定し、それに応じてリンクを更新します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-120">Compare a localized Microsoft repo to the en-US repo to identify differences and update links accordingly.</span></span>

> [!NOTE]
> <span data-ttu-id="23a6b-121">カスタム ヘルプ ツールキットの最初のバージョンでは、このツールの名前は ConsoleApp でした。</span><span class="sxs-lookup"><span data-stu-id="23a6b-121">In the first version of the Custom Help Toolkit, this tool was named ConsoleApp.</span></span> <span data-ttu-id="23a6b-122">このツールの名前が変更され、2020 年に更新されました。</span><span class="sxs-lookup"><span data-stu-id="23a6b-122">The tool was renamed and updated in 2020.</span></span>

### <a name="syntax"></a><span data-ttu-id="23a6b-123">構文</span><span class="sxs-lookup"><span data-stu-id="23a6b-123">Syntax</span></span>

<span data-ttu-id="23a6b-124">HtmlFromRepoGenerator.exe を実行するための構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="23a6b-124">Here is the syntax for running HtmlFromRepoGenerator.exe.</span></span>

```
HtmlFromRepoGenerator.exe --Json <Articles/> --Out <path> --ExternalText <text> [--DoNotClone <true|false>] [--Repo <URL>] [--RemoveGitFolder <true|false>] [--ReplaceUrl <URL>] [--LogsDir <.\logs>] [--EnRepo <URL>] [--EnOut <path>] [--Lng <language code>] [--Rtl] [--?[--]]
```

<span data-ttu-id="23a6b-125">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-125">Here is an explanation of the parameters.</span></span>

| <span data-ttu-id="23a6b-126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23a6b-126">Parameter</span></span> | <span data-ttu-id="23a6b-127">説明</span><span class="sxs-lookup"><span data-stu-id="23a6b-127">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="23a6b-128">Json</span><span class="sxs-lookup"><span data-stu-id="23a6b-128">Json</span></span> | <span data-ttu-id="23a6b-129">**docfx.json** ファイルの場所の相対パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-129">Specify a relative path for the location of the **docfx.json** file.</span></span> <span data-ttu-id="23a6b-130">Microsoft ドキュメント リポジトリでは、この場所は通常、**articles/** です。</span><span class="sxs-lookup"><span data-stu-id="23a6b-130">In Microsoft documentation repos, this location is typically **articles/**.</span></span> |
| <span data-ttu-id="23a6b-131">出庫</span><span class="sxs-lookup"><span data-stu-id="23a6b-131">Out</span></span> | <span data-ttu-id="23a6b-132">既存の複製されたリポジトリが存在するフォルダ、またはリポジトリの複製先のフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-132">Specify the folder where your existing cloned repo exists, or the folder to clone the repo to.</span></span> <span data-ttu-id="23a6b-133">**HtmlFromRepoGenerator** ツールを実行してリポジトリを複製する場合、このフォルダが存在していない必要があります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-133">If you run the **HtmlFromRepoGenerator** tool to clone a repo, this folder must not already exist.</span></span> <span data-ttu-id="23a6b-134">[製品およびヘルプの言語およびロケール記述子](language-locale.md) で説明されているように、フォルダ名に言語名を使用します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-134">Use the language name as the folder name, as described in [Language and locale descriptors in the product and in Help](language-locale.md).</span></span> |
| <span data-ttu-id="23a6b-135">ExternalText</span><span class="sxs-lookup"><span data-stu-id="23a6b-135">ExternalText</span></span> | <span data-ttu-id="23a6b-136">**HtmlFromRepoGenerator** ツールが元のリンクを置き換える必要がある場合に、更新されたリンクに追加するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-136">Specify text that should be added to the updated links if the **HtmlFromRepoGenerator** tool must replace the original links.</span></span> |
| <span data-ttu-id="23a6b-137">DoNotClone</span><span class="sxs-lookup"><span data-stu-id="23a6b-137">DoNotClone</span></span> | <span data-ttu-id="23a6b-138">以前に複製されたリポジトリに対してツールを実行する場合、このパラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-138">Set this parameter when you run the tool against a previously cloned repo.</span></span> |
| <span data-ttu-id="23a6b-139">リポジトリ</span><span class="sxs-lookup"><span data-stu-id="23a6b-139">Repo</span></span> | <span data-ttu-id="23a6b-140">リポジトリ URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-140">Specify the repo URL.</span></span> <span data-ttu-id="23a6b-141">以前に複製されたリポジトリに対してツールを実行する場合、このパラメータはオプションです。</span><span class="sxs-lookup"><span data-stu-id="23a6b-141">This parameter is optional if you run the tool against a previously cloned repo.</span></span> <span data-ttu-id="23a6b-142">Microsoft ドキュメント リポジトリの URL の例には、英語 (米国) の `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` と ドイツ語 (ドイツ) の `https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de` が含まれます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-142">Examples of URLs for Microsoft documentation repos include `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` for English (United States) and `https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de` for German (Germany).</span></span>|
| <span data-ttu-id="23a6b-143">RemoveGitFolder</span><span class="sxs-lookup"><span data-stu-id="23a6b-143">RemoveGitFolder</span></span>| <span data-ttu-id="23a6b-144">**.git** フォルダを削除するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-144">Specify whether the **.git** folder should be removed.</span></span> |
| <span data-ttu-id="23a6b-145">ReplaceUrl</span><span class="sxs-lookup"><span data-stu-id="23a6b-145">ReplaceUrl</span></span> | <span data-ttu-id="23a6b-146">ターゲット ファイルが存在しない場合、ファイル間のリンクを置き換える URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-146">Specify the URL that should replace links between files when the target files aren't present.</span></span> <span data-ttu-id="23a6b-147">このパラメータは、相対リンクを絶対リンクに変換するために使用します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-147">This parameter is intended to be used to turn relative links into absolute links.</span></span> |
| <span data-ttu-id="23a6b-148">LogsDir</span><span class="sxs-lookup"><span data-stu-id="23a6b-148">LogsDir</span></span> | <span data-ttu-id="23a6b-149">ログ ファイルを保存するフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-149">Specify the folder to save logs files to.</span></span> |

<span data-ttu-id="23a6b-150">次の追加パラメータは、ローカライズされた Microsoft ドキュメント リポジトリに対してツールを実行するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-150">The following additional parameters are used when the tool is run against the localized Microsoft documentation repos.</span></span>

| <span data-ttu-id="23a6b-151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="23a6b-151">Parameter</span></span> | <span data-ttu-id="23a6b-152">説明</span><span class="sxs-lookup"><span data-stu-id="23a6b-152">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="23a6b-153">EnRepo</span><span class="sxs-lookup"><span data-stu-id="23a6b-153">EnRepo</span></span> | <span data-ttu-id="23a6b-154">en-US リポジトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-154">Specify the URL of the en-US repo.</span></span> <span data-ttu-id="23a6b-155">以前に複製されたリポジトリに対してツールを実行する場合、このパラメータはオプションです。</span><span class="sxs-lookup"><span data-stu-id="23a6b-155">This parameter is optional if you run the tool against a previously cloned repo.</span></span> <span data-ttu-id="23a6b-156">英語 (米国) 用の Microsoft ドキュメント リポジトリの URL は、`https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` です。</span><span class="sxs-lookup"><span data-stu-id="23a6b-156">The URL of the Microsoft documentation repo for English (United States) is `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public`.</span></span> |
| <span data-ttu-id="23a6b-157">EnOut</span><span class="sxs-lookup"><span data-stu-id="23a6b-157">EnOut</span></span> | <span data-ttu-id="23a6b-158">en-US リポジトリが存在するフォルダ、または複製するフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-158">Specify the folder where the en-US repo exists, or the folder to clone it to.</span></span> <span data-ttu-id="23a6b-159">以前に複製されたリポジトリに対してツールを実行する場合、このフォルダが存在していない必要があります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-159">If you run the tool against a previously cloned repo, this folder must not already exist.</span></span> |
| <span data-ttu-id="23a6b-160">Lng</span><span class="sxs-lookup"><span data-stu-id="23a6b-160">Lng</span></span> | <span data-ttu-id="23a6b-161">生成された HTML ファイルの **ms.locale** メタデータに使用する言語の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-161">Specify the language value that should be used for **ms.locale** metadata in the generated HTML files.</span></span> <span data-ttu-id="23a6b-162">この値は、Finance and Operations クライアントの言語設定で指定されている値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-162">The value must correspond to the value that is specified in the language settings of the Finance and Operations client.</span></span> <span data-ttu-id="23a6b-163">このパラメーターが設定されていない場合、ツールは **en-US** を使用します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-163">If this parameter isn't set, the tool uses **en-US**.</span></span> <span data-ttu-id="23a6b-164">詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23a6b-164">For more information, see [Language and locale descriptors in the product and in Help](language-locale.md).</span></span> |
| <span data-ttu-id="23a6b-165">Rtl</span><span class="sxs-lookup"><span data-stu-id="23a6b-165">Rtl</span></span> | <span data-ttu-id="23a6b-166">言語が右から左 (RTL) の書式設定を使用する場合、このパラメータを含めます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-166">Include this parameter if the language uses right-to-left (RTL) formatting.</span></span> <span data-ttu-id="23a6b-167">RTL 言語の例としては、アラビア語とヘブライ語があります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-167">Examples of RTL languages include Arabic and Hebrew.</span></span> |

## <a name="examples"></a><span data-ttu-id="23a6b-168">例</span><span class="sxs-lookup"><span data-stu-id="23a6b-168">Examples</span></span>

> [!NOTE]
> <span data-ttu-id="23a6b-169">Microsoft リポジトリには多数のファイルが含まれているため、プロセスに数分かかります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-169">Because the Microsoft repos contain many files, the process takes several minutes.</span></span> <span data-ttu-id="23a6b-170">複数のローカライズされたリポジトリに対してツールを実行すると、プロセスに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-170">If you run the tool against multiple localized repos, the process takes longer.</span></span>

<span data-ttu-id="23a6b-171">次の例では、en-US リポジトリを複製し、en-US の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-171">The following example clones the en-US repo and generates HTML files for en-US.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\en-US" --repo "https://github.com/MicrosoftDocs/Dynamics-365-unified-Operations-public" --externalText "(This is an external link)" --replaceUrl "https://docs.microsoft.com/en-us/dynamics365/supply-chain" --LogsDir D:\D365-Operations\logs\en-US
```

<span data-ttu-id="23a6b-172">次の例では、以前に複製された en-US リポジトリを使用し、en-US の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-172">The following example uses a previously cloned en-US repo and generates HTML files for en-US.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\en-US" --externalText "(This is an external link)" --replaceUrl "https://docs.microsoft.com/en-us/dynamics365/supply-chain" --LogsDir D:\D365-Operations\logs\en-US
```

<span data-ttu-id="23a6b-173">次の例では、de-DE と en-US リポジトリを複製し、de の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-173">The following example clones the de-DE and en-US repos, and generates HTML files for de.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\de" --repo "https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de" --externalText "(This is an external link)" --EnRepo "https://github.com/MicrosoftDocs/Dynamics-365-unified-Operations-public" --EnOut "D:\D365-Operations\en-us" --replaceUrl "https://docs.microsoft.com/de-de/dynamics365/supply-chain" --lng "de" --LogsDir D:\D365-Operations\logs\de
```

<span data-ttu-id="23a6b-174">次の例では、既存の de-DE と en-US リポジトリを使用し、de の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-174">The following example uses the existing de-DE and en-US repos, and generates HTML files for de.</span></span> <span data-ttu-id="23a6b-175">既存の de-DE リポジトリを使用する場合、そのリポジトリが最新であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="23a6b-175">If you use the existing de-DE repo, make sure that it's up to date.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\de" --DoNotClone --externalText "(This is an external link)" --enOut "D:\D365-Operations\en-us" --replaceUrl "https://docs.microsoft.com/de-de/dynamics365/supply-chain" --lng "de" --LogsDir D:\D365-Operations\logs\de
```

> [!IMPORTANT]
> <span data-ttu-id="23a6b-176">**HtmlFromRepoGenerator** ツールは処理中にリンクを変更するため、以前に複製されたリポジトリに対してHtmlFromRepoGenerator.exe を複数回実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="23a6b-176">Because the **HtmlFromRepoGenerator** tool changes links during processing, don't run HtmlFromRepoGenerator.exe more than one time against a previously cloned repo.</span></span> <span data-ttu-id="23a6b-177">同じコンテンツに対して複数回実行すると、リンクが正しくなりません。</span><span class="sxs-lookup"><span data-stu-id="23a6b-177">If it's run more than one time against the same content, links will be incorrect.</span></span> <span data-ttu-id="23a6b-178">HtmlFromRepoGenerator.exe を再実行する場合、**HtmlFromRepoGenerator** ツールを使用してリポジトリの新しい複製を作成するか、既存の複製に対して行われたローカルの変更をすべて元に戻します。</span><span class="sxs-lookup"><span data-stu-id="23a6b-178">If you want to rerun HtmlFromRepoGenerator.exe, either use the **HtmlFromRepoGenerator** tool to create a new clone of the repo, or revert all local changes that have been made to your existing clone.</span></span>

## <a name="modifying-the-styling-of-the-generated-html-files"></a><span data-ttu-id="23a6b-179">生成された HTML ファイルのスタイルの変更</span><span class="sxs-lookup"><span data-stu-id="23a6b-179">Modifying the styling of the generated HTML files</span></span>

<span data-ttu-id="23a6b-180">**HtmlFromRepoGenerator** ツールが生成する HTML ファイルは、一連の事前定義されたテンプレートに基づいています。</span><span class="sxs-lookup"><span data-stu-id="23a6b-180">The HTML files that the **HtmlFromRepoGenerator** tool generates are based on a set of predefined templates.</span></span> <span data-ttu-id="23a6b-181">ほとんどの場合、**d365F-O\\styles** フォルダーのスタイル シートを編集して、コンテンツの外観を変更できます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-181">In most cases, you can edit the style sheets in the **d365F-O\\styles** folder to change the appearance of your content.</span></span>

<span data-ttu-id="23a6b-182">高度なシナリオでは、**HtmlFromRepoGenerator** ツールが使用するテンプレートを変更できます。</span><span class="sxs-lookup"><span data-stu-id="23a6b-182">For advanced scenarios, you can change the templates that the **HtmlFromRepoGenerator** tool uses.</span></span> <span data-ttu-id="23a6b-183">ソース ファイルは、GitHub リポジトリの **SourceCode** フォルダーに含まれています。</span><span class="sxs-lookup"><span data-stu-id="23a6b-183">The source files are included in the **SourceCode** folder in the GitHub repo.</span></span> <span data-ttu-id="23a6b-184">このテンプレートは、**SourceCode\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\»Resources** サブフォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-184">The templates are in the **SourceCode\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\Resources** subfolder.</span></span>

> [!NOTE]
> <span data-ttu-id="23a6b-185">テンプレートを変更する場合、HtmlFromRepoGenerator.exe を再構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23a6b-185">If you change the templates, you must rebuild HtmlFromRepoGenerator.exe.</span></span>

<span data-ttu-id="23a6b-186">詳細については、[DocFX テンプレート システムの概要](https://dotnet.github.io/docfx/tutorial/intro_template.html) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="23a6b-186">For more information, see [Introduction to DocFX Template System](https://dotnet.github.io/docfx/tutorial/intro_template.html).</span></span>

## <a name="see-also"></a><span data-ttu-id="23a6b-187">参照</span><span class="sxs-lookup"><span data-stu-id="23a6b-187">See also</span></span>

[<span data-ttu-id="23a6b-188">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="23a6b-188">Custom Help Toolkit</span></span>](custom-help-toolkit.md)  
[<span data-ttu-id="23a6b-189">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="23a6b-189">Custom Help overview</span></span>](custom-help-overview.md)  
[<span data-ttu-id="23a6b-190">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="23a6b-190">Deploy custom Help to Azure</span></span>](walkthrough-help-azure.md)  
[<span data-ttu-id="23a6b-191">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="23a6b-191">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)  
[<span data-ttu-id="23a6b-192">Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換</span><span class="sxs-lookup"><span data-stu-id="23a6b-192">Convert Dynamics AX custom Help for use in Dynamics 365</span></span>](migrate-dynamicsax2012.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]