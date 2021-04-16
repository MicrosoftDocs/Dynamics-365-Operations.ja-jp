---
title: 財務諸表デザイナーでのレポート定義
description: この記事では、レポート定義に関する情報を示します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755447"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="0cfe7-103">財務諸表デザイナーでのレポート定義</span><span class="sxs-lookup"><span data-stu-id="0cfe7-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cfe7-104">この記事では、レポート定義に関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-104">This article provides information about report definitions.</span></span> <span data-ttu-id="0cfe7-105">レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="0cfe7-106">レポート定義は、レポートをカスタマイズするためのオプションおよび設定も提供します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="0cfe7-107">レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="0cfe7-108">レポート定義は、レポートのカスタマイズに使用できるオプションおよび設定も提供しています。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="0cfe7-109">行定義と列定義を定義したら、レポート定義に結合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="0cfe7-110">この時点で、詳細レベルおよびレポートの日付などの定義の他の側面も定義します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="0cfe7-111">これで、レポートの保存および生成ができます。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-111">You can then save and generate a report.</span></span> <span data-ttu-id="0cfe7-112">財務諸表は、レポート用に次の詳細レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="0cfe7-113">財務</span><span class="sxs-lookup"><span data-stu-id="0cfe7-113">Financial</span></span>
- <span data-ttu-id="0cfe7-114">[財務と勘定]</span><span class="sxs-lookup"><span data-stu-id="0cfe7-114">Financial and Account</span></span>
- <span data-ttu-id="0cfe7-115">[財務]、[勘定] および [トランザクション]</span><span class="sxs-lookup"><span data-stu-id="0cfe7-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="0cfe7-116">ただし、Microsoft Dynamics ERP システムにデータを格納する方法によって、トランザクションの詳細がレポートで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="0cfe7-117">レポート定義の作成</span><span class="sxs-lookup"><span data-stu-id="0cfe7-117">Create a report definition</span></span>
1. <span data-ttu-id="0cfe7-118">[レポート デザイナー] の **ファイル** メニューで、**新規** をクリックし、**レポート定義** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="0cfe7-119">**レポート**、**出荷および配送**、**ヘッダーおよびフッター**、**設定** タブで、適切な情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="0cfe7-120">レポート定義の内容</span><span class="sxs-lookup"><span data-stu-id="0cfe7-120">Contents of a report definition</span></span>
<span data-ttu-id="0cfe7-121">次の表は、レポート定義のタブと、情報の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0cfe7-122">タブ</span><span class="sxs-lookup"><span data-stu-id="0cfe7-122">Tab</span></span></th>
<th><span data-ttu-id="0cfe7-123">説明</span><span class="sxs-lookup"><span data-stu-id="0cfe7-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0cfe7-124">レポート </span><span class="sxs-lookup"><span data-stu-id="0cfe7-124">Report</span></span></td>
<td><span data-ttu-id="0cfe7-125">レポートを作成し、レポートをコンフィギュレーションし、既存のレポートを変更します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0cfe7-126">[出荷および配送]</span><span class="sxs-lookup"><span data-stu-id="0cfe7-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="0cfe7-127">レポートの出力のタイプと出力先を変更します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0cfe7-128">[ヘッダーとフッター]</span><span class="sxs-lookup"><span data-stu-id="0cfe7-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="0cfe7-129">レポートのヘッダーおよびフッターを定義および書式設定します。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="0cfe7-130">たとえば、ヘッダーまたはフッターにテキストや画像を追加できます。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="0cfe7-131">財務諸表は、画像の .bmp、.jpg、.png ファイルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="0cfe7-132">自動テキスト コードを追加して、会社名、レポート名、ページ番号などの他の情報を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="0cfe7-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0cfe7-133">設定</span><span class="sxs-lookup"><span data-stu-id="0cfe7-133">Settings</span></span></td>
<td><span data-ttu-id="0cfe7-134">次の設定などのレポート定義の設定を指定します :</span><span class="sxs-lookup"><span data-stu-id="0cfe7-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="0cfe7-135">金額の書式設定および丸め</span><span class="sxs-lookup"><span data-stu-id="0cfe7-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="0cfe7-136">詳細レポートの書式設定</span><span class="sxs-lookup"><span data-stu-id="0cfe7-136">Format detail reports</span></span></li>
<li><span data-ttu-id="0cfe7-137">レポート ツリーの書式設定</span><span class="sxs-lookup"><span data-stu-id="0cfe7-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="0cfe7-138">例外レポートの生成</span><span class="sxs-lookup"><span data-stu-id="0cfe7-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="0cfe7-139">通貨換算の指定</span><span class="sxs-lookup"><span data-stu-id="0cfe7-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="0cfe7-140">小計およびフィルターの勘定の詳細</span><span class="sxs-lookup"><span data-stu-id="0cfe7-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="0cfe7-141">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0cfe7-141">Additional resources</span></span>

[<span data-ttu-id="0cfe7-142">財務報告</span><span class="sxs-lookup"><span data-stu-id="0cfe7-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]