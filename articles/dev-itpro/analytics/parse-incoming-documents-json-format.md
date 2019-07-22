---
title: JSON 形式で受信したドキュメントを解析する
description: このトピックでは、受信した JavaScript Object Notation (JSON) 形式のドキュメントを解析するように電子報告 (ER) 形式を設定する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 05/20/2019
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
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 92ef83bc1783b00a4d7d9739ca1c17e863c7ff44
ms.sourcegitcommit: f6581bab16225a027f4fbfad25fdef45bd286489
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/27/2019
ms.locfileid: "1703924"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="d5a70-103">JSON 形式で受信したドキュメントを解析する</span><span class="sxs-lookup"><span data-stu-id="d5a70-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d5a70-104">JavaScript に基づくテキスト形式 (つまり、JavaScript Object Notation \[JSON\] 形式のファイル) のデータを表す、受信した電子ドキュメントを解析するよう、電子申告 (ER) 形式をデザインすることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="d5a70-105">この機能の詳細については、次のテーブルに示すファイルをダウンロードし、外部 JSON ファイルからデータをインポートするための形式コンフィギュレーションの ER 作成というタスク ガイドを再生します。</span><span class="sxs-lookup"><span data-stu-id="d5a70-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="d5a70-106">このタスク ガイドは、受信する JSON ファイルを解析し、アプリケーション データを更新するために ER 形式を使用する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="d5a70-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="d5a70-107">肩書き</span><span class="sxs-lookup"><span data-stu-id="d5a70-107">Title</span></span>                                  | <span data-ttu-id="d5a70-108">ファイル名</span><span class="sxs-lookup"><span data-stu-id="d5a70-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="d5a70-109">ER フォーマット構成</span><span class="sxs-lookup"><span data-stu-id="d5a70-109">ER format configuration</span></span>                | [<span data-ttu-id="d5a70-110">仕入先の trans_JSON.xml をインポートするための形式</span><span class="sxs-lookup"><span data-stu-id="d5a70-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="d5a70-111">.csv 形式の受信ファイルのサンプル</span><span class="sxs-lookup"><span data-stu-id="d5a70-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="d5a70-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="d5a70-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="d5a70-113">必要量</span><span class="sxs-lookup"><span data-stu-id="d5a70-113">Requirements</span></span>

<span data-ttu-id="d5a70-114">外部 JSON ファイルからデータをインポートするための形式コンフィギュレーションの ER 作成のタスク ガイドを完了する前に、次の条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5a70-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="d5a70-115">JSON ファイルの親要素は、オブジェクト要素にのみなることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="d5a70-116">オブジェクトに対して入れ子になった要素はプロパティ要素である必要があるので、有効な JSON 構造が作成されます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="d5a70-117">JSON 配列は、オブジェクトのプロパティ要素に入れ子になった要素にのみなることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="d5a70-118">JSON 配列には JSON オブジェクトのみ含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="d5a70-119">文字列、数値、および入れ子になった配列を直接含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="d5a70-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="d5a70-120">これらの配列の要素は、形式内で指定されている順序で解析されます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="d5a70-121">各 JSON オブジェクトの多様性の設定が考慮されます。</span><span class="sxs-lookup"><span data-stu-id="d5a70-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="d5a70-122">また、まだ完了していない場合は、[外部ファイルから電子申告にデータをインポートするのに必要なコンフィギュレーションの ER 作成](tasks/er-required-configurations-import-data.md) タスク ガイドを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5a70-122">Additionally, you must complete the [ER Create required configurations to import data from an external file for electronic reporting](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="d5a70-123">タスクガイドを完成させるには、次のファイルをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="d5a70-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="d5a70-124">肩書き</span><span class="sxs-lookup"><span data-stu-id="d5a70-124">Title</span></span>                  | <span data-ttu-id="d5a70-125">ファイル名</span><span class="sxs-lookup"><span data-stu-id="d5a70-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="d5a70-126">ER モデル構成</span><span class="sxs-lookup"><span data-stu-id="d5a70-126">ER model configuration</span></span> | [<span data-ttu-id="d5a70-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="d5a70-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
