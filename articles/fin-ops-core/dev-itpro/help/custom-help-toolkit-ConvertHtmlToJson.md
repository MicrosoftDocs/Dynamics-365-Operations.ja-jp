---
title: カスタム ヘルプ ツールキット - ConvertHtmlToJson ツール
description: このトピックでは、Finance and Operations アプリ用のカスタム ヘルプ ツールキットに含まれている ConvertHtmlToJson ツールについて説明し ます。
author: edupont04
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.service: dynamics-ax-platform
audience: IT Pro
ms.reviewer: tfehr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 8b3976ac82dbfb660530992a307de9a6b5970a34
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367044"
---
# <a name="custom-help-toolkit-the-converthtmltojson-tool"></a><span data-ttu-id="1fcb1-103">カスタム ヘルプ ツールキット: ConvertHtmlToJson ツール</span><span class="sxs-lookup"><span data-stu-id="1fcb1-103">Custom Help Toolkit: The ConvertHtmlToJson tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fcb1-104">[カスタム ヘルプ ツールキット](custom-help-toolkit.md) には、HTML ファイルを JavaScript Object Notation (JSON) ファイルに変換する **ConvertHtmlToJson** ツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-104">The [Custom Help Toolkit](custom-help-toolkit.md) includes the **ConvertHtmlToJson** tool, which converts HTML files to JavaScript Object Notation (JSON) files.</span></span> <span data-ttu-id="1fcb1-105">検索サービスは、JSON ファイルを使用してヘルプ コンテンツのインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-105">The search service uses the JSON files to index Help content.</span></span>

## <a name="use-the-converthtmltojson-tool-to-generate-json-files"></a><a name="json"></a><span data-ttu-id="1fcb1-106">ConvertHtmlToJson ツールを使用して JSON ファイルを生成する</span><span class="sxs-lookup"><span data-stu-id="1fcb1-106">Use the ConvertHtmlToJson tool to generate JSON files</span></span>

<span data-ttu-id="1fcb1-107">**ConvertHtmlToJson** ツールは、HTML ファイルを JSON ファイルに変換します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-107">The **ConvertHtmlToJson** tool transforms HTML files into JSON files.</span></span> <span data-ttu-id="1fcb1-108">次に、JSON ファイルを Microsoft Azure検索サービスに追加すると、ヘルプ コンテンツへの状況依存リンクが生成されます。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-108">You can then add the JSON files to the Microsoft Azure Search service, which will generate context-sensitive links to your Help content.</span></span>

<span data-ttu-id="1fcb1-109">JSON ファイルには、ターゲットのヘルプ ページが対象とするフォームと言語を識別するためにインデクサーが使用するメタデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-109">The JSON files include metadata that the indexer uses to identify the form and language that the target Help page is intended for.</span></span>

<span data-ttu-id="1fcb1-110">ConvertHtmlToJson.exe を実行するための構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-110">Here is the syntax for running ConvertHtmlToJson.exe.</span></span>

```
ConvertHtmlToJson.exe --h <path> -j <path> --v <true|false>
```

<span data-ttu-id="1fcb1-111">パラメータの説明を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-111">Here is an explanation of the parameters.</span></span>

| <span data-ttu-id="1fcb1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fcb1-112">Parameter</span></span> | <span data-ttu-id="1fcb1-113">説明</span><span class="sxs-lookup"><span data-stu-id="1fcb1-113">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="1fcb1-114">h</span><span class="sxs-lookup"><span data-stu-id="1fcb1-114">h</span></span> | <span data-ttu-id="1fcb1-115">処理する HTML ファイルのパスを指定します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-115">Specify the path of the HTML files to process.</span></span> |
| <span data-ttu-id="1fcb1-116">j</span><span class="sxs-lookup"><span data-stu-id="1fcb1-116">j</span></span> | <span data-ttu-id="1fcb1-117">JSON ファイルを保存するフォルダを指定します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-117">Specify the folder to save the JSON files to.</span></span> <span data-ttu-id="1fcb1-118">指定したフォルダは既に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-118">The specified folder must already exist.</span></span> |
| <span data-ttu-id="1fcb1-119">v</span><span class="sxs-lookup"><span data-stu-id="1fcb1-119">v</span></span> | <span data-ttu-id="1fcb1-120">このパラメーターを **true** に設定し、詳細ログを有効にします。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-120">Set this parameter to **true** to turn on verbose logging.</span></span> <span data-ttu-id="1fcb1-121">それ以外の場合、**false** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-121">Otherwise, set it to **false**.</span></span> |

## <a name="example"></a><span data-ttu-id="1fcb1-122">例</span><span class="sxs-lookup"><span data-stu-id="1fcb1-122">Example</span></span>

<span data-ttu-id="1fcb1-123">次の例では、詳細ログなしで JSON ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="1fcb1-123">The following example generates JSON files without verbose logging.</span></span>

```
ConvertHtmlToJson.exe --h D:\D365-Operations\d365F-O\supply-chain\de -j D:\D365-Operations\json\supply-chain\de
```

## <a name="see-also"></a><span data-ttu-id="1fcb1-124">参照</span><span class="sxs-lookup"><span data-stu-id="1fcb1-124">See also</span></span>

[<span data-ttu-id="1fcb1-125">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="1fcb1-125">Custom Help overview</span></span>](custom-help-overview.md)  
[<span data-ttu-id="1fcb1-126">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="1fcb1-126">Deploy custom Help to Azure</span></span>](walkthrough-help-azure.md)  
[<span data-ttu-id="1fcb1-127">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="1fcb1-127">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)  
[<span data-ttu-id="1fcb1-128">Dynamics AX カスタム ヘルプを Dynamics 365 で使用するために変換</span><span class="sxs-lookup"><span data-stu-id="1fcb1-128">Convert Dynamics AX custom Help for use in Dynamics 365</span></span>](migrate-dynamicsax2012.md)
