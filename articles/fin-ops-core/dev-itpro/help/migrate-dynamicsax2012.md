---
title: Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換する
description: このトピックでは、Microsoft Dynamics AX のコンテンツを Dynamics 365 ソリューションで再利用する方法について説明します。
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
ms.openlocfilehash: f409dbac51d8dab5c7c025fd61d20ba3f15bc9ee
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3366989"
---
# <a name="convert-dynamics-ax-custom-help-for-use-in-dynamics-365"></a><span data-ttu-id="62138-103">Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換する</span><span class="sxs-lookup"><span data-stu-id="62138-103">Convert Dynamics AX custom Help for use in Dynamics 365</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62138-104">Microsoft Dynamics AX 2012 の既存のコンテンツがある場合は、Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce で再利用できます。</span><span class="sxs-lookup"><span data-stu-id="62138-104">If you have existing content from Microsoft Dynamics AX 2012, you can reuse it for Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Commerce.</span></span> <span data-ttu-id="62138-105">ただし、まず HTML ファイルを変換して、カスタム ヘルプ環境で使用できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62138-105">However, you must first transform the HTML files so that they can be used in the custom Help environment.</span></span>

## <a name="converting-ax-2012-content"></a><span data-ttu-id="62138-106">AX 2012 コンテンツの変換</span><span class="sxs-lookup"><span data-stu-id="62138-106">Converting AX 2012 content</span></span>

<span data-ttu-id="62138-107">Microsoft [カスタム ヘルプ ツールキット](custom-help-toolkit.md) には、AX 2012 の HTML ファイルを変換してカスタム ヘルプ環境で使用できるようにする Windows PowerShell スクリプト **run_ax2012.ps1** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="62138-107">The Microsoft [Custom Help Toolkit](custom-help-toolkit.md) includes a Windows PowerShell script, **run_ax2012.ps1**, that can transform AX 2012 HTML files so that they can be used in the custom Help environment.</span></span> <span data-ttu-id="62138-108">スクリプトにより、AX 2012 HTML ファイルに次の変更が加えられます:</span><span class="sxs-lookup"><span data-stu-id="62138-108">The script makes the following changes to the AX 2012 HTML files:</span></span>

- <span data-ttu-id="62138-109">**Microsoft.Help.F1** メタデータ名を **ms.search.form** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="62138-109">Replace the **Microsoft.Help.F1** metadata name with **ms.search.form**.</span></span>
- <span data-ttu-id="62138-110">**Title** メタデータ名を **title** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="62138-110">Replace the **Title** metadata name with **title**.</span></span>
- <span data-ttu-id="62138-111">ファイル名拡張子を **.htm** から **.html** に変更します。</span><span class="sxs-lookup"><span data-stu-id="62138-111">Change the file name extension from **.htm** to **.html**.</span></span>
- <span data-ttu-id="62138-112">次のメタデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="62138-112">Add the following metadata.</span></span>

    ```html
    <meta name="ms.search.region" content="Global" />
    <meta name="ms.search.scope" content="Operations, Core" />
    <meta name="ms.dyn365.ops.version" content="AX 7.0.0" />
    <meta name="ms.search.validFrom" content="2016-05-31" />
    <meta name="ms.search.industry" content="cross" />
    ```

### <a name="running-the-script"></a><span data-ttu-id="62138-113">スクリプトの実行</span><span class="sxs-lookup"><span data-stu-id="62138-113">Running the script</span></span>

<span data-ttu-id="62138-114">[コマンド プロンプト] ウィンドウから次のコマンドを実行することも、Windows PowerShell でスクリプトを直接実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="62138-114">You can run the following command from a Command Prompt window, or you can run the script directly in Windows PowerShell.</span></span>

```powershell
PowerShell.exe -File run_ax2012.ps1 "Original file location" "New file location"
```

<span data-ttu-id="62138-115">次のメタデータが現在使用されているか、インデックス作成中に使用できるように予約されています。</span><span class="sxs-lookup"><span data-stu-id="62138-115">The following metadata is currently used, or it's reserved so that it can be used during indexing.</span></span>

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

<span data-ttu-id="62138-116">必要なメタデータの説明については、[カスタム ヘルプ トピックのメタデータ要件](preparing-content.md#metadata) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62138-116">For a description of the required metadata, see [Metadata requirements for custom Help topics](preparing-content.md#metadata).</span></span>

## <a name="moving-to-markdown"></a><a name="moving-to-markdown"></a><span data-ttu-id="62138-117">Markdown への移行</span><span class="sxs-lookup"><span data-stu-id="62138-117">Moving to Markdown</span></span>

<span data-ttu-id="62138-118">既存のコンテンツを Markdown に変換するために、[PanDoc](https://pandoc.org) や Word の [Writage](http://www.writage.com) プラグインなど、さまざまなサードパーティ製ツールを使用できます。</span><span class="sxs-lookup"><span data-stu-id="62138-118">To convert your existing content to Markdown, you can use various third-party tools, such as [PanDoc](https://pandoc.org) and the [Writage](http://www.writage.com) plug-in for Word.</span></span>

<span data-ttu-id="62138-119">コンテンツを Markdown に変換した後で、[DocFx](https://dotnet.github.io/docfx/) などのオープン ソース ツールを使用して、Web サイトのコンテンツを生成できます。</span><span class="sxs-lookup"><span data-stu-id="62138-119">After you've converted your content to Markdown, you can use open-source tools such as [DocFx](https://dotnet.github.io/docfx/) to generate content for your website.</span></span> <span data-ttu-id="62138-120">一般に、Markdown で作業することにより、さまざまな オープン ソース ツールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="62138-120">In general, by working in Markdown, you gain access to a wide range of open-source tools.</span></span> <span data-ttu-id="62138-121">詳細については、[ヘルプの拡張、カスタマイズ、および共同作業](contributor-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62138-121">For more information, see [Extend, customize, and collaborate on the Help](contributor-guide.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="62138-122">参照</span><span class="sxs-lookup"><span data-stu-id="62138-122">See also</span></span>

[<span data-ttu-id="62138-123">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="62138-123">Custom Help overview</span></span>](custom-help-overview.md)  
[<span data-ttu-id="62138-124">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="62138-124">Custom Help Toolkit</span></span>](custom-help-toolkit.md)  
[<span data-ttu-id="62138-125">ヘルプの拡張、カスタマイズ、および共同作業</span><span class="sxs-lookup"><span data-stu-id="62138-125">Extend, customize, and collaborate on the Help</span></span>](contributor-guide.md)
