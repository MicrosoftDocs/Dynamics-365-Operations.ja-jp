---
title: カスタム ヘルプ ツールキット - HtmlFromRepoGenerator ツール
description: このトピックでは、Finance and Operations アプリ用のカスタム ヘルプ ツールキットに含まれている HtmlFromRepoGenerator ツールについて説明し ます。
author: edupont04
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.service: dynamics-ax-platform
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 30f7703e2f7c46ae49daf3bc0f8a7e7079624686
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685091"
---
# <a name="custom-help-toolkit-the-htmlfromrepogenerator-tool"></a><span data-ttu-id="71ee1-103">カスタム ヘルプ ツールキット: HtmlFromRepoGenerator ツール</span><span class="sxs-lookup"><span data-stu-id="71ee1-103">Custom Help Toolkit: The HtmlFromRepoGenerator tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71ee1-104">カスタム ヘルプ ツールキットには、マークダウン ファイル内の Microsoft コンテンツを取得してHTML ファイルに変換する **HtmlFromRepoGenerator** ツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="71ee1-104">The Custom Help Toolkit includes the **HtmlFromRepoGenerator** tool, which gets Microsoft content in Markdown files and converts it to HTML files.</span></span> <span data-ttu-id="71ee1-105">その後、HTML ファイルを Web サイト に展開できます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-105">You can then deploy the HTML files to a website.</span></span>

## <a name="use-the-htmlfromrepogenerator-tool-to-get-markdown-files-and-generate-html-files"></a><a name="consoleapp"></a><span data-ttu-id="71ee1-106">HtmlFromRepoGenerator ツールを使用して、マークダウン ファイルを取得し HTML ファイルを生成する</span><span class="sxs-lookup"><span data-stu-id="71ee1-106">Use the HtmlFromRepoGenerator tool to get Markdown files and generate HTML files</span></span>

<span data-ttu-id="71ee1-107">**HtmlFromRepoGenerator** ツールには、Microsoft のソース ファイルに基づくカスタム ヘルプの作成をサポートする機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="71ee1-107">The **HtmlFromRepoGenerator** tool provides functionality that supports the creation of custom Help that is based on source files from Microsoft.</span></span> <span data-ttu-id="71ee1-108">ツールを使用して次のタスクを実行できます:</span><span class="sxs-lookup"><span data-stu-id="71ee1-108">You can use the tool to perform these tasks:</span></span>

- <span data-ttu-id="71ee1-109">Microsoft ドキュメント リポジトリをクローンします。</span><span class="sxs-lookup"><span data-stu-id="71ee1-109">Clone a Microsoft documentation repository (repo).</span></span>
- <span data-ttu-id="71ee1-110">Microsoft リポジトリのクローンから開発者および管理者のコンテンツを削除します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-110">Remove developer and admin content from your clone of the Microsoft repo.</span></span>
- <span data-ttu-id="71ee1-111">クローンに既に存在しないファイルへのリンクを更新します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-111">Update links to files that are no longer present in the clone.</span></span>
- <span data-ttu-id="71ee1-112">Finance and Operations クライアントでサポートされている言語オプションと一致するように **ms.locale** プロパティの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-112">Update the value of the **ms.locale** property so that it matches the language options that are supported by the Finance and Operations client.</span></span>

    <span data-ttu-id="71ee1-113">クライアントが使用する言語記述子は、対応する GitHub リポジトリで使用されている言語記述子と異なります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-113">The language descriptors that the client uses differ from the language descriptors that are used in the corresponding GitHub repos.</span></span> <span data-ttu-id="71ee1-114">ローカライズされたカスタム ヘルプを呼び出す前に、ソース コンテンツの言語記述子を変更して、クライアントの言語と一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-114">Before localized custom Help can be called, the language descriptors in the source content must be changed so that they match the client's languages.</span></span> <span data-ttu-id="71ee1-115">詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71ee1-115">For more information, see [Language and locale descriptors in the product and in Help](language-locale.md).</span></span>

- <span data-ttu-id="71ee1-116">コンテンツの公開に使用できる HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-116">Generate HTML files that can be used to publish content.</span></span>

    <span data-ttu-id="71ee1-117">HTML ファイルは **d365F-O** サブフォルダーに生成されます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-117">The HTML files will be generated in the **d365F-O** subfolder.</span></span> <span data-ttu-id="71ee1-118">ファイルは、ツールの一部であるスタイル シートとテンプレートに基づいて生成されます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-118">The files are generated based on style sheets and templates that are part of the tool.</span></span> <span data-ttu-id="71ee1-119">詳細については、このトピックの [生成された HTML ファイルのスタイル変更](#modifying-the-styling-of-the-generated-html-files) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="71ee1-119">For more information, see the [Modifying the styling of the generated HTML files](#modifying-the-styling-of-the-generated-html-files) section of this topic.</span></span>

- <span data-ttu-id="71ee1-120">ローカライズされた Microsoft リポジトリと en-US リポジトリを比較して、相違点を特定し、それに応じてリンクを更新します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-120">Compare a localized Microsoft repo to the en-US repo to identify differences and update links accordingly.</span></span>

<span data-ttu-id="71ee1-121">カスタム ヘルプ ツールキットの最初のバージョンでは、このツールの名前は ConsoleApp でした。</span><span class="sxs-lookup"><span data-stu-id="71ee1-121">In the first version of the Custom Help Toolkit, this tool was named ConsoleApp.</span></span>

### <a name="syntax"></a><span data-ttu-id="71ee1-122">構文</span><span class="sxs-lookup"><span data-stu-id="71ee1-122">Syntax</span></span>

<span data-ttu-id="71ee1-123">HtmlFromRepoGenerator.exe を実行するための構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="71ee1-123">Here is the syntax for running HtmlFromRepoGenerator.exe.</span></span>

```
HtmlFromRepoGenerator.exe --Json <Articles/> --Out <path> --ExternalText <text> [--DoNotClone <true|false>] [--Repo <URL>] [--RemoveGitFolder <true|false>] [--ReplaceUrl <URL>] [--LogsDir <.\logs>] [--EnRepo <URL>] [--EnOut <path>] [--Lng <language code>] [--Rtl] [--?[--]]
```

<span data-ttu-id="71ee1-124">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-124">Here is an explanation of the parameters.</span></span>

| <span data-ttu-id="71ee1-125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="71ee1-125">Parameter</span></span> | <span data-ttu-id="71ee1-126">説明</span><span class="sxs-lookup"><span data-stu-id="71ee1-126">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="71ee1-127">Json</span><span class="sxs-lookup"><span data-stu-id="71ee1-127">Json</span></span> | <span data-ttu-id="71ee1-128">**docfx.json** ファイルの場所の相対パスを指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-128">Specify a relative path for the location of the **docfx.json** file.</span></span> <span data-ttu-id="71ee1-129">Microsoft ドキュメント リポジトリでは、この場所は通常、**articles/** です。</span><span class="sxs-lookup"><span data-stu-id="71ee1-129">In Microsoft documentation repos, this location is typically **articles/**.</span></span> |
| <span data-ttu-id="71ee1-130">出庫</span><span class="sxs-lookup"><span data-stu-id="71ee1-130">Out</span></span> | <span data-ttu-id="71ee1-131">既存の複製されたリポジトリが存在するフォルダ、またはリポジトリの複製先のフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-131">Specify the folder where your existing cloned repo exists, or the folder to clone the repo to.</span></span> <span data-ttu-id="71ee1-132">**HtmlFromRepoGenerator** ツールを実行してリポジトリを複製する場合、このフォルダが存在していない必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-132">If you run the **HtmlFromRepoGenerator** tool to clone a repo, this folder must not already exist.</span></span> <span data-ttu-id="71ee1-133">[製品およびヘルプの言語およびロケール記述子](language-locale.md) で説明されているように、フォルダ名に言語名を使用します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-133">Use the language name as the folder name, as described in [Language and locale descriptors in the product and in Help](language-locale.md).</span></span> |
| <span data-ttu-id="71ee1-134">ExternalText</span><span class="sxs-lookup"><span data-stu-id="71ee1-134">ExternalText</span></span> | <span data-ttu-id="71ee1-135">**HtmlFromRepoGenerator** ツールが元のリンクを置き換える必要がある場合に、更新されたリンクに追加するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-135">Specify text that should be added to the updated links if the **HtmlFromRepoGenerator** tool must replace the original links.</span></span> |
| <span data-ttu-id="71ee1-136">DoNotClone</span><span class="sxs-lookup"><span data-stu-id="71ee1-136">DoNotClone</span></span> | <span data-ttu-id="71ee1-137">以前に複製されたリポジトリに対してツールを実行する場合、このパラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-137">Set this parameter when you run the tool against a previously cloned repo.</span></span> |
| <span data-ttu-id="71ee1-138">リポジトリ</span><span class="sxs-lookup"><span data-stu-id="71ee1-138">Repo</span></span> | <span data-ttu-id="71ee1-139">リポジトリ URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-139">Specify the repo URL.</span></span> <span data-ttu-id="71ee1-140">以前に複製されたリポジトリに対してツールを実行する場合、このパラメータはオプションです。</span><span class="sxs-lookup"><span data-stu-id="71ee1-140">This parameter is optional if you run the tool against a previously cloned repo.</span></span> <span data-ttu-id="71ee1-141">Microsoft ドキュメント リポジトリの URL の例には、英語 (米国) の `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` と ドイツ語 (ドイツ) の `https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de` が含まれます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-141">Examples of URLs for Microsoft documentation repos include `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` for English (United States) and `https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de` for German (Germany).</span></span>|
| <span data-ttu-id="71ee1-142">RemoveGitFolder</span><span class="sxs-lookup"><span data-stu-id="71ee1-142">RemoveGitFolder</span></span>| <span data-ttu-id="71ee1-143">**.git** フォルダを削除するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-143">Specify whether the **.git** folder should be removed.</span></span> |
| <span data-ttu-id="71ee1-144">ReplaceUrl</span><span class="sxs-lookup"><span data-stu-id="71ee1-144">ReplaceUrl</span></span> | <span data-ttu-id="71ee1-145">ターゲット ファイルが存在しない場合、ファイル間のリンクを置き換える URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-145">Specify the URL that should replace links between files when the target files aren't present.</span></span> <span data-ttu-id="71ee1-146">このパラメータは、相対リンクを絶対リンクに変換するために使用します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-146">This parameter is intended to be used to turn relative links into absolute links.</span></span> |
| <span data-ttu-id="71ee1-147">LogsDir</span><span class="sxs-lookup"><span data-stu-id="71ee1-147">LogsDir</span></span> | <span data-ttu-id="71ee1-148">ログ ファイルを保存するフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-148">Specify the folder to save logs files to.</span></span> |

<span data-ttu-id="71ee1-149">次の追加パラメータは、ローカライズされた Microsoft ドキュメント リポジトリに対してツールを実行するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-149">The following additional parameters are used when the tool is run against the localized Microsoft documentation repos.</span></span>

| <span data-ttu-id="71ee1-150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="71ee1-150">Parameter</span></span> | <span data-ttu-id="71ee1-151">説明</span><span class="sxs-lookup"><span data-stu-id="71ee1-151">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="71ee1-152">EnRepo</span><span class="sxs-lookup"><span data-stu-id="71ee1-152">EnRepo</span></span> | <span data-ttu-id="71ee1-153">en-US リポジトリの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-153">Specify the URL of the en-US repo.</span></span> <span data-ttu-id="71ee1-154">以前に複製されたリポジトリに対してツールを実行する場合、このパラメータはオプションです。</span><span class="sxs-lookup"><span data-stu-id="71ee1-154">This parameter is optional if you run the tool against a previously cloned repo.</span></span> <span data-ttu-id="71ee1-155">英語 (米国) 用の Microsoft ドキュメント リポジトリの URL は、`https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public` です。</span><span class="sxs-lookup"><span data-stu-id="71ee1-155">The URL of the Microsoft documentation repo for English (United States) is `https://github.com/MicrosoftDocs/Dynamics-365-Unified-Operations-public`.</span></span> |
| <span data-ttu-id="71ee1-156">EnOut</span><span class="sxs-lookup"><span data-stu-id="71ee1-156">EnOut</span></span> | <span data-ttu-id="71ee1-157">en-US リポジトリが存在するフォルダ、または複製するフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-157">Specify the folder where the en-US repo exists, or the folder to clone it to.</span></span> <span data-ttu-id="71ee1-158">以前に複製されたリポジトリに対してツールを実行する場合、このフォルダが存在していない必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-158">If you run the tool against a previously cloned repo, this folder must not already exist.</span></span> |
| <span data-ttu-id="71ee1-159">Lng</span><span class="sxs-lookup"><span data-stu-id="71ee1-159">Lng</span></span> | <span data-ttu-id="71ee1-160">生成された HTML ファイルの **ms.locale** メタデータに使用する言語の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-160">Specify the language value that should be used for **ms.locale** metadata in the generated HTML files.</span></span> <span data-ttu-id="71ee1-161">この値は、Finance and Operations クライアントの言語設定で指定されている値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-161">The value must correspond to the value that is specified in the language settings of the Finance and Operations client.</span></span> <span data-ttu-id="71ee1-162">このパラメーターが設定されていない場合、ツールは **en-US** を使用します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-162">If this parameter isn't set, the tool uses **en-US**.</span></span> <span data-ttu-id="71ee1-163">詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71ee1-163">For more information, see [Language and locale descriptors in the product and in Help](language-locale.md).</span></span> |
| <span data-ttu-id="71ee1-164">Rtl</span><span class="sxs-lookup"><span data-stu-id="71ee1-164">Rtl</span></span> | <span data-ttu-id="71ee1-165">言語が右から左 (RTL) の書式設定を使用する場合、このパラメータを含めます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-165">Include this parameter if the language uses right-to-left (RTL) formatting.</span></span> <span data-ttu-id="71ee1-166">RTL 言語の例としては、アラビア語とヘブライ語があります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-166">Examples of RTL languages include Arabic and Hebrew.</span></span> |

## <a name="examples"></a><span data-ttu-id="71ee1-167">例</span><span class="sxs-lookup"><span data-stu-id="71ee1-167">Examples</span></span>

> [!NOTE]
> <span data-ttu-id="71ee1-168">Microsoft リポジトリには多数のファイルが含まれているため、プロセスに数分かかります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-168">Because the Microsoft repos contain many files, the process takes several minutes.</span></span> <span data-ttu-id="71ee1-169">複数のローカライズされたリポジトリに対してツールを実行すると、プロセスに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-169">If you run the tool against multiple localized repos, the process takes longer.</span></span>

<span data-ttu-id="71ee1-170">次の例では、en-US リポジトリを複製し、en-US の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-170">The following example clones the en-US repo and generates HTML files for en-US.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\en-US" --repo "https://github.com/MicrosoftDocs/Dynamics-365-unified-Operations-public" --externalText "(This is an external link)" --replaceUrl "https://docs.microsoft.com/en-us/dynamics365/supply-chain" --LogsDir D:\D365-Operations\logs\en-US
```

<span data-ttu-id="71ee1-171">次の例では、以前に複製された en-US リポジトリを使用し、en-US の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-171">The following example uses a previously cloned en-US repo and generates HTML files for en-US.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\en-US" --externalText "(This is an external link)" --replaceUrl "https://docs.microsoft.com/en-us/dynamics365/supply-chain" --LogsDir D:\D365-Operations\logs\en-US
```

<span data-ttu-id="71ee1-172">次の例では、de-DE と en-US リポジトリを複製し、de の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-172">The following example clones the de-DE and en-US repos, and generates HTML files for de.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\de" --repo "https://github.com/MicrosoftDocs/Dynamics-365-Operations.de-de" --externalText "(This is an external link)" --EnRepo "https://github.com/MicrosoftDocs/Dynamics-365-unified-Operations-public" --EnOut "D:\D365-Operations\en-us" --replaceUrl "https://docs.microsoft.com/de-de/dynamics365/supply-chain" --lng "de" --LogsDir D:\D365-Operations\logs\de
```

<span data-ttu-id="71ee1-173">次の例では、既存の de-DE と en-US リポジトリを使用し、de の HTML ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-173">The following example uses the existing de-DE and en-US repos, and generates HTML files for de.</span></span> <span data-ttu-id="71ee1-174">既存の de-DE リポジトリを使用する場合、そのリポジトリが最新であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="71ee1-174">If you use the existing de-DE repo, make sure that it's up to date.</span></span>

```
HtmlFromRepoGenerator.exe --json articles/ --out "D:\D365-Operations\de" --DoNotClone --externalText "(This is an external link)" --enOut "D:\D365-Operations\en-us" --replaceUrl "https://docs.microsoft.com/de-de/dynamics365/supply-chain" --lng "de" --LogsDir D:\D365-Operations\logs\de
```

> [!IMPORTANT]
> <span data-ttu-id="71ee1-175">**HtmlFromRepoGenerator** ツールは処理中にリンクを変更するため、以前に複製されたリポジトリに対してHtmlFromRepoGenerator.exe を複数回実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="71ee1-175">Because the **HtmlFromRepoGenerator** tool changes links during processing, don't run HtmlFromRepoGenerator.exe more than one time against a previously cloned repo.</span></span> <span data-ttu-id="71ee1-176">同じコンテンツに対して複数回実行すると、リンクが正しくなりません。</span><span class="sxs-lookup"><span data-stu-id="71ee1-176">If it's run more than one time against the same content, links will be incorrect.</span></span> <span data-ttu-id="71ee1-177">HtmlFromRepoGenerator.exe を再実行する場合、**HtmlFromRepoGenerator** ツールを使用してリポジトリの新しい複製を作成するか、既存の複製に対して行われたローカルの変更をすべて元に戻します。</span><span class="sxs-lookup"><span data-stu-id="71ee1-177">If you want to rerun HtmlFromRepoGenerator.exe, either use the **HtmlFromRepoGenerator** tool to create a new clone of the repo, or revert all local changes that have been made to your existing clone.</span></span>

## <a name="modifying-the-styling-of-the-generated-html-files"></a><span data-ttu-id="71ee1-178">生成された HTML ファイルのスタイルの変更</span><span class="sxs-lookup"><span data-stu-id="71ee1-178">Modifying the styling of the generated HTML files</span></span>

<span data-ttu-id="71ee1-179">**HtmlFromRepoGenerator** ツールが生成する HTML ファイルは、一連の事前定義されたテンプレートに基づいています。</span><span class="sxs-lookup"><span data-stu-id="71ee1-179">The HTML files that the **HtmlFromRepoGenerator** tool generates are based on a set of predefined templates.</span></span> <span data-ttu-id="71ee1-180">ほとんどの場合、**d365F-O\\styles** フォルダーのスタイル シートを編集して、コンテンツの外観を変更できます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-180">In most cases, you can edit the style sheets in the **d365F-O\\styles** folder to change the appearance of your content.</span></span>

<span data-ttu-id="71ee1-181">高度なシナリオでは、**HtmlFromRepoGenerator** ツールが使用するテンプレートを変更できます。</span><span class="sxs-lookup"><span data-stu-id="71ee1-181">For advanced scenarios, you can change the templates that the **HtmlFromRepoGenerator** tool uses.</span></span> <span data-ttu-id="71ee1-182">ソース ファイルは、GitHub リポジトリの **SourceCode** フォルダーに含まれています。</span><span class="sxs-lookup"><span data-stu-id="71ee1-182">The source files are included in the **SourceCode** folder in the GitHub repo.</span></span> <span data-ttu-id="71ee1-183">このテンプレートは、**SourceCode\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\»Resources** サブフォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-183">The templates are in the **SourceCode\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\HtmlFromRepoGenerator\\Resources** subfolder.</span></span>

> [!NOTE]
> <span data-ttu-id="71ee1-184">テンプレートを変更する場合、HtmlFromRepoGenerator.exe を再構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="71ee1-184">If you change the templates, you must rebuild HtmlFromRepoGenerator.exe.</span></span>

<span data-ttu-id="71ee1-185">詳細については、[DocFX テンプレート システムの概要](https://dotnet.github.io/docfx/tutorial/intro_template.html) を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="71ee1-185">For more information, see [Introduction to DocFX Template System](https://dotnet.github.io/docfx/tutorial/intro_template.html).</span></span>

## <a name="see-also"></a><span data-ttu-id="71ee1-186">参照</span><span class="sxs-lookup"><span data-stu-id="71ee1-186">See also</span></span>

[<span data-ttu-id="71ee1-187">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="71ee1-187">Custom Help Toolkit</span></span>](custom-help-toolkit.md)  
[<span data-ttu-id="71ee1-188">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="71ee1-188">Custom Help overview</span></span>](custom-help-overview.md)  
[<span data-ttu-id="71ee1-189">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="71ee1-189">Deploy custom Help to Azure</span></span>](walkthrough-help-azure.md)  
[<span data-ttu-id="71ee1-190">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="71ee1-190">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)  
[<span data-ttu-id="71ee1-191">Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換</span><span class="sxs-lookup"><span data-stu-id="71ee1-191">Convert Dynamics AX custom Help for use in Dynamics 365</span></span>](migrate-dynamicsax2012.md)
