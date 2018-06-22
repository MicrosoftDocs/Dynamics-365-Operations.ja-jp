---
title: "Microsoft Excel で受信ドキュメントを解析する"
description: "このトピックでは、受信した Microsoft Excel ファイルに含まれる内容を解析する電子申告 (ER) 形式の設計に関する情報を示します。"
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 001e287590b9f43ed38de803bcace3a25a6f6637
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2018

---

# <a name="parse-incoming-microsoft-excel-files"></a><span data-ttu-id="38706-103">受信した Microsoft Excel ファイルの解析</span><span class="sxs-lookup"><span data-stu-id="38706-103">Parse incoming Microsoft Excel files</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="38706-104">Microsoft Excel のブック (XLSX 形式のファイル) でデータを表す、受信した Microsoft Excel ファイルを解析する電子申告 (ER) の形式を設計できます。</span><span class="sxs-lookup"><span data-stu-id="38706-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="38706-105">その後、アプリケーションのデータを更新するのに、これらのファイルからの内容を使用できます。</span><span class="sxs-lookup"><span data-stu-id="38706-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="38706-106">これは、次のような場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="38706-106">This is useful if you:</span></span>

-   <span data-ttu-id="38706-107">新しいモデルおよびフォーマットをデザインし、実行時にテストします。</span><span class="sxs-lookup"><span data-stu-id="38706-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="38706-108">この場合、Excel は実際のアプリケーション データをシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="38706-108">In this case, Excel will simulate the actual application data.</span></span>
-   <span data-ttu-id="38706-109">アプリケーションを超えたデータを Excel で管理し、特定のレポートを送信するのに、このデータをインポートします。</span><span class="sxs-lookup"><span data-stu-id="38706-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="38706-110">この機能の詳細については、タスク ガイド **Microsoft Excel ファイルからの ER インポート データ (第 1 部: 形式の設計)** および **Microsoft Excel ファイルからの ER インポート データ (第 2 部: データのインポート)** を実行してください (7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部)。</span><span class="sxs-lookup"><span data-stu-id="38706-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="38706-111">これらのタスク ガイドは、 受信ドキュメントから情報をインポートしてアプリケーション データを更新する、ER 形式を使用した受信した Excel ファイルの解析方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="38706-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="38706-112">タスク ガイドは [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684)からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="38706-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="38706-113">上記のタスク ガイドを完了するには、次のファイルをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="38706-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="38706-114">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="38706-114">Content description</span></span>                        | <span data-ttu-id="38706-115">ファイル</span><span class="sxs-lookup"><span data-stu-id="38706-115">File</span></span>                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="38706-116">.XLSX 形式の受信ファイル - テンプレート</span><span class="sxs-lookup"><span data-stu-id="38706-116">Incoming file in .XLSX format - template</span></span>   | [<span data-ttu-id="38706-117">1099import template.xlsx</span><span class="sxs-lookup"><span data-stu-id="38706-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)  |
| <span data-ttu-id="38706-118">.XLSX 形式の受信ファイル - サンプル データ</span><span class="sxs-lookup"><span data-stu-id="38706-118">Incoming file in .XLSX format - sample data</span></span>| [<span data-ttu-id="38706-119">1099import data.xlsx</span><span class="sxs-lookup"><span data-stu-id="38706-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="38706-120">次のタスク ガイド [ER Create が外部ファイルからデータをインポートするために必要な設定](./tasks/er-required-configurations-import-data.md)を、現在の Dynamics 365 for Finance and Operation アプリケーションで実行していない場合、次のファイルをダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="38706-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="38706-121">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="38706-121">Content description</span></span>                        | <span data-ttu-id="38706-122">ファイル</span><span class="sxs-lookup"><span data-stu-id="38706-122">File</span></span>                                                                       |
---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="38706-123">ER モデル構成</span><span class="sxs-lookup"><span data-stu-id="38706-123">ER model configuration</span></span>                     | [<span data-ttu-id="38706-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="38706-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)            |


