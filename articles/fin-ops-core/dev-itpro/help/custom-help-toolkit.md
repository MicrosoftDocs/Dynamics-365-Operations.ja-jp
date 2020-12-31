---
title: カスタム ヘルプ ツールキット
description: このトピックでは、Finance and Operations アプリ用のカスタム ヘルプ ツールキットのコンポーネントについて説明します。
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
ms.openlocfilehash: 4216965e4f5dce36f6250b5cffc3982b8207cf48
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685092"
---
# <a name="custom-help-toolkit"></a><span data-ttu-id="ebd90-103">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="ebd90-103">Custom Help Toolkit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebd90-104">Microsoft は、カスタマイズされた Finance and Operations ソリューションの状況依存ヘルプを準備するのに役立つスクリプトとツールを含む GitHub リポジトリ を公開しました。</span><span class="sxs-lookup"><span data-stu-id="ebd90-104">Microsoft has published a GitHub repository (repo) that includes scripts and tools that can help you prepare context-sensitive Help for customized Finance and Operations solutions.</span></span> <span data-ttu-id="ebd90-105">この状況依存ヘルプには、製品内の **ヘルプ** ウィンドウからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ebd90-105">This context-sensitive Help can be accessed from the in-product **Help** pane.</span></span>

## <a name="tools-in-the-toolkit"></a><span data-ttu-id="ebd90-106">ツールキットのツール</span><span class="sxs-lookup"><span data-stu-id="ebd90-106">Tools in the toolkit</span></span>

<span data-ttu-id="ebd90-107">カスタム ヘルプ ツールキットは、[https://github.com/microsoft/dynamics365f-o-custom-help](https://github.com/microsoft/dynamics365f-o-custom-help/) から入手できます。</span><span class="sxs-lookup"><span data-stu-id="ebd90-107">The Custom Help Toolkit is available at [https://github.com/microsoft/dynamics365f-o-custom-help](https://github.com/microsoft/dynamics365f-o-custom-help/).</span></span> <span data-ttu-id="ebd90-108">リポジトリには、次のツールとそのツールのソースコードが含まれています:</span><span class="sxs-lookup"><span data-stu-id="ebd90-108">The repo contains the following tools and the source code for those tools:</span></span>

- <span data-ttu-id="ebd90-109">**HtmlFromRepoGenerator** ツール</span><span class="sxs-lookup"><span data-stu-id="ebd90-109">The **HtmlFromRepoGenerator** tool</span></span>

    <span data-ttu-id="ebd90-110">詳細については、[カスタム ヘルプ ツールキット: HtmlFromRepoGenerator ツール](custom-help-toolkit-HtmlFromRepoGenerator.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd90-110">For more information, see [Custom Help Toolkit: The HtmlFromRepoGenerator tool](custom-help-toolkit-HtmlFromRepoGenerator.md).</span></span>

- <span data-ttu-id="ebd90-111">**ConvertHtmlToJson** ツール</span><span class="sxs-lookup"><span data-stu-id="ebd90-111">The **ConvertHtmlToJson** tool</span></span>

    <span data-ttu-id="ebd90-112">詳細については、[カスタム ヘルプ ツールキット: ConvertHtmlToJson ツール](custom-help-toolkit-ConvertHtmlToJson.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd90-112">For more information, see [Custom Help Toolkit: The ConvertHtmlToJson tool](custom-help-toolkit-ConvertHtmlToJson.md).</span></span>

- <span data-ttu-id="ebd90-113">**HtmlLocaleChanger** ツール</span><span class="sxs-lookup"><span data-stu-id="ebd90-113">The **HtmlLocaleChanger** tool</span></span>

    <span data-ttu-id="ebd90-114">詳細については、[カスタム ヘルプ ツールキット: HtmlLocaleChanger ツール](custom-help-toolkit-HtmlLocaleChanger.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd90-114">For more information, see [Custom Help Toolkit: The HtmlLocaleChanger tool](custom-help-toolkit-HtmlLocaleChanger.md).</span></span>

- <span data-ttu-id="ebd90-115">**ヘルプ ウィンドウ拡張機能** Microsoft Visual Studio プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ebd90-115">The **Help Pane extension** Microsoft Visual Studio project</span></span>

    <span data-ttu-id="ebd90-116">詳細については、[カスタム ヘルプ Web サイトを ヘルプ ウィンドウに接続する](connect-help-pane.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd90-116">For more information, see [Connect a custom Help website to the Help pane](connect-help-pane.md).</span></span>

- <span data-ttu-id="ebd90-117">Dynamics AX 2012 メタデータ スクリプト</span><span class="sxs-lookup"><span data-stu-id="ebd90-117">Dynamics AX 2012 metadata scripts</span></span>

    <span data-ttu-id="ebd90-118">詳細については、[Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換](migrate-dynamicsax2012.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ebd90-118">For more information, see [Convert Dynamics AX custom Help for use in Dynamics 365](migrate-dynamicsax2012.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ebd90-119">ツールキットの最初のバージョンは、[GitHub リポジトリのリリース](https://github.com/microsoft/dynamics365f-o-custom-help/releases) として入手できます。</span><span class="sxs-lookup"><span data-stu-id="ebd90-119">The first version of the toolkit is available as a [release in the GitHub repo](https://github.com/microsoft/dynamics365f-o-custom-help/releases).</span></span>

## <a name="see-also"></a><span data-ttu-id="ebd90-120">参照</span><span class="sxs-lookup"><span data-stu-id="ebd90-120">See also</span></span>

[<span data-ttu-id="ebd90-121">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="ebd90-121">Custom Help overview</span></span>](custom-help-overview.md)  
[<span data-ttu-id="ebd90-122">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="ebd90-122">Deploy custom Help to Azure</span></span>](walkthrough-help-azure.md)  
<span data-ttu-id="ebd90-123">[カスタム ヘルプ Web サイトを [ヘルプ] ウィンドウに接続する](connect-help-pane.md)</span><span class="sxs-lookup"><span data-stu-id="ebd90-123">[Connect a custom Help website to the Help pane](connect-help-pane.md)</span></span>  
[<span data-ttu-id="ebd90-124">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="ebd90-124">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)  
[<span data-ttu-id="ebd90-125">Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換</span><span class="sxs-lookup"><span data-stu-id="ebd90-125">Convert Dynamics AX custom Help for use in Dynamics 365</span></span>](migrate-dynamicsax2012.md)
