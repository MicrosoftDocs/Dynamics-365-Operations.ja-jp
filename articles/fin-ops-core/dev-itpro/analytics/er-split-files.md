---
title: ファイル サイズとコンテンツ量に基づいて、生成された XML ファイルを分割する
description: このトピックでは、ファイルのサイズおよびコンテンツの品目数量に基づいて生成されるファイルを分割する方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: cde95430022d94c42bdd985b5e4a8f9f5147d000
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181361"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="76f09-103">ファイル サイズとコンテンツ量に基づいて、生成された XML ファイルを分割する</span><span class="sxs-lookup"><span data-stu-id="76f09-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="76f09-104">XML 形式で送信ドキュメントを生成するための電子申告 (ER) 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="76f09-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="76f09-105">場合によっては、それらのドキュメントは、ファイルの最大サイズまたはいくつかの XML ノードの最大数などの特定の条件を満たしている場合にのみ受領できます。</span><span class="sxs-lookup"><span data-stu-id="76f09-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="76f09-106">それらのドキュメントの受信者が指定する要件を満たす電子ドキュメントを生成する ER 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="76f09-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="76f09-107">FILE 形式要素については、ER 式としてファイル サイズの制限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="76f09-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="76f09-108">ER レポートの生成時に定義されている制限を超過した場合、ER は現在のファイルを作成し終えて次のファイルの作成に移ります。</span><span class="sxs-lookup"><span data-stu-id="76f09-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="76f09-109">任意の XML ELEMENT 形式については、ER 式として要素の数の制限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="76f09-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="76f09-110">生成されるファイルで XML ノードの数が ER レポートの実行時に定義される制限を超過する場合、ER は現在のファイルを作成し終えて次のファイルの作成に移ります。</span><span class="sxs-lookup"><span data-stu-id="76f09-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="76f09-111">任意の XML SEQUENCE 形式要素については、ER 式として子要素の数の制限を定義できます。</span><span class="sxs-lookup"><span data-stu-id="76f09-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="76f09-112">生成されるファイルで形式要素の入れ子になった XML ノードの数が ER レポートの実行時に定義される制限を超過する場合、ER は現在のファイルを作成し終えて次のファイルの作成に移ります。</span><span class="sxs-lookup"><span data-stu-id="76f09-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="76f09-113">任意の XML ELEMENT 形式要素を non-breakable としてマークできます。</span><span class="sxs-lookup"><span data-stu-id="76f09-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="76f09-114">この方法で、単一の生成されるファイルの形式要素で生成される XML ノードの入れ子になった品目を保持できます。</span><span class="sxs-lookup"><span data-stu-id="76f09-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="76f09-115">XML ELEMENT および XML SEQUENCE 形式要素を使用して生成されるファイルに XML ノードを追加するだけでなく、未加工の XML 形式要素を使用できます。</span><span class="sxs-lookup"><span data-stu-id="76f09-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="76f09-116">ただし、未加工の XML 形式要素の使用により追加するノードは、ノードの数の計算時に要素の数の制限を評価するとは見なされません。</span><span class="sxs-lookup"><span data-stu-id="76f09-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="76f09-117">特定の制限を超えるたびに生成された出力を分割するように構成された FILE 形式要素のファイルの出力先をコンフィギュレーションした場合、それぞれの生成された出力が個別のファイルとして構成されたファイルの出力先に送信されます。</span><span class="sxs-lookup"><span data-stu-id="76f09-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="76f09-118">出力を分割して作成されるファイルに固有の名前を付けるには、FILE 形式要素の ER 式をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="76f09-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="76f09-119">NUMBER SEQUENCE タイプの ER データ ソースを含める場合、番号順序は個々の分割出力に対して増加します。</span><span class="sxs-lookup"><span data-stu-id="76f09-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="76f09-120">この機能の詳細については、**7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677)** 業務プロセスの一部である**ファイルのサイズおよびコンテンツの品目数量に基づく ER 分割 XML ファイル** タスクガイドを再生し、[Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="76f09-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="76f09-121">このタスク ガイドでは、ファイル サイズおよびコンテンツの品目数量の制限に基づいて生成されたファイルを分割するため、ER 形式のコンフィギュレーションのプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="76f09-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="76f09-122">タスクガイドを完了するには、次のファイルをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="76f09-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="76f09-123">ER モデル コンフィギュレーション - XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="76f09-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="76f09-124">ER 形式コンフィギュレーション - XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="76f09-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="76f09-125">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="76f09-125">Additional resources</span></span>
[<span data-ttu-id="76f09-126">電子申告の送信先</span><span class="sxs-lookup"><span data-stu-id="76f09-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="76f09-127">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="76f09-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
