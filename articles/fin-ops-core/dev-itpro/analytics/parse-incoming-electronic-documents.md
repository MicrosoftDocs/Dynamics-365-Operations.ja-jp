---
title: アプリケーションのデータを更新するために受信したドキュメントを解析する
description: このトピックでは、受信したドキュメントを解析し、選択したコンテンツをアプリケーション データに適用して更新できるように電子報告 (ER) 形式を設定する方法について説明します。
author: nickselin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2017-11-10
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 880b73c68727f2617dae332c85b95d0e86d1f33f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191559"
---
# <a name="parse-incoming-documents-to-update-application-data"></a><span data-ttu-id="f2daf-103">アプリケーションのデータを更新するために受信したドキュメントを解析する</span><span class="sxs-lookup"><span data-stu-id="f2daf-103">Parse incoming documents to update application data</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2daf-104">電子申告 (ER) 書式をデザインしてアプリケーション内で実行し、受信した電子ドキュメントを解析し、その内容を使用してアプリケーション データを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="f2daf-104">You can design Electronic reporting (ER) formats and run them in the application, to parse incoming electronic documents and then use their content to update application data.</span></span>

<span data-ttu-id="f2daf-105">導入された次の新しい ER 機能は、XML 形式の受信する電子ドキュメンの解析を改善します。</span><span class="sxs-lookup"><span data-stu-id="f2daf-105">The following new ER functionality that has been introduced improves the parsing of incoming electronic documents in XML format:</span></span>

- <span data-ttu-id="f2daf-106">**CASE** 形式要素は、XML 形式の受信電子ドキュメントを解析するように構成された ER 形式のルート要素として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f2daf-106">The **CASE** format element can be used as a root element of the ER format that is configured to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="f2daf-107">**FILE** 形式要素は、**CASE** 要素の入れ子になった要素としてサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f2daf-107">The **FILE** format element is supported as a nested element of the **CASE** element.</span></span> <span data-ttu-id="f2daf-108">したがって、1 つの ER フォーマットを設定して、異なるルート XML 要素を含む可能性のある受信電子ドキュメントを解析することができます。</span><span class="sxs-lookup"><span data-stu-id="f2daf-108">Therefore, you can configure a single ER format to parse incoming electronic documents that might contain different root XML elements.</span></span>
- <span data-ttu-id="f2daf-109">**入れ子になった要素の順序を解析**属性が ER 形式の XML 形式要素に導入されました。</span><span class="sxs-lookup"><span data-stu-id="f2daf-109">A **Parsing order of nested elements** attribute has been introduced for XML format elements in ER formats.</span></span> <span data-ttu-id="f2daf-110">この属性を使用すると、読み込まれるファイルで予期される 1 つの XML 要素を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="f2daf-110">You can use this attribute to define a single XML element that is expected in the incoming file.</span></span> <span data-ttu-id="f2daf-111">ネストされた要素には 2 つの有効なシーケンスがあります。</span><span class="sxs-lookup"><span data-stu-id="f2daf-111">There are two valid sequences of the nested elements:</span></span>

    - <span data-ttu-id="f2daf-112">**形式どおり** - 受信ファイルは、ファイル内の入れ子になった要素の順序は、ER 形式に記載されている順序と同じ場合に有効です。</span><span class="sxs-lookup"><span data-stu-id="f2daf-112">**As in format** – The incoming file is valid when the sequence of nested elements in the file is the same as the order that is described in the ER format.</span></span>
    - <span data-ttu-id="f2daf-113">**任意** - 着信ファイルは、そのファイル内の順番に関係なく、ER 形式のすべての入れ子になった要素が解析ファイルに存在する場合に有効です。</span><span class="sxs-lookup"><span data-stu-id="f2daf-113">**Any** – The incoming file is valid when all nested elements in the ER format are present in the parsing file, regardless of their sequence in that file.</span></span>

<span data-ttu-id="f2daf-114">この機能の詳細をよく理解するためには、タスク ガイド、\[ER - 受信ドキュメントを解析してアプリケーション データを更新する\] (「7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発」(10677) ビジネス プロセスの一部) を再生します。</span><span class="sxs-lookup"><span data-stu-id="f2daf-114">To become more familiar with the details of this feature, play the task guide, ER - Parse incoming documents to update application data (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="f2daf-115">このタスク ガイドは、Web サービスからの応答を ER 形式を使用して解析する方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="f2daf-115">This task guide shows how the responses from a web service can be parsed by using an ER format.</span></span>

<span data-ttu-id="f2daf-116">タスク ガイドのいくつかの手順を完了するには、次のファイルをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2daf-116">To complete some steps of the task guide, you must download the following files:</span></span>

| <span data-ttu-id="f2daf-117">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="f2daf-117">Content description</span></span>           | <span data-ttu-id="f2daf-118">ファイル</span><span class="sxs-lookup"><span data-stu-id="f2daf-118">File</span></span>                                                              |
|-------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="f2daf-119">ER データ モデル構成</span><span class="sxs-lookup"><span data-stu-id="f2daf-119">ER data model configuration</span></span>   | [<span data-ttu-id="f2daf-120">EFSTAmodel.xml</span><span class="sxs-lookup"><span data-stu-id="f2daf-120">EFSTAmodel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)  |
| <span data-ttu-id="f2daf-121">ER フォーマット構成</span><span class="sxs-lookup"><span data-stu-id="f2daf-121">ER format configuration</span></span>       | [<span data-ttu-id="f2daf-122">EFSTAformat.xml</span><span class="sxs-lookup"><span data-stu-id="f2daf-122">EFSTAformat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="f2daf-123">Web サービス応答サンプル 1</span><span class="sxs-lookup"><span data-stu-id="f2daf-123">Web service response sample 1</span></span> | [<span data-ttu-id="f2daf-124">Response1.xml</span><span class="sxs-lookup"><span data-stu-id="f2daf-124">Response1.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)   |
| <span data-ttu-id="f2daf-125">Web サービス応答サンプル 2</span><span class="sxs-lookup"><span data-stu-id="f2daf-125">Web service response sample 2</span></span> | [<span data-ttu-id="f2daf-126">Response2.xml</span><span class="sxs-lookup"><span data-stu-id="f2daf-126">Response2.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)   |
| <span data-ttu-id="f2daf-127">Web サービス応答サンプル 3</span><span class="sxs-lookup"><span data-stu-id="f2daf-127">Web service response sample 3</span></span> | [<span data-ttu-id="f2daf-128">Response3.xml</span><span class="sxs-lookup"><span data-stu-id="f2daf-128">Response3.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)   |
| <span data-ttu-id="f2daf-129">Web サービス応答サンプル 4</span><span class="sxs-lookup"><span data-stu-id="f2daf-129">Web service response sample 4</span></span> | [<span data-ttu-id="f2daf-130">Response4.xml</span><span class="sxs-lookup"><span data-stu-id="f2daf-130">Response4.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)   |