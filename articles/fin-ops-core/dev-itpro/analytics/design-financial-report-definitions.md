---
title: 財務諸表デザイナーでのレポート定義
description: この記事では、レポート定義に関する情報を示します。 レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。 レポート定義は、レポートをカスタマイズするためのオプションおよび設定も提供します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174147"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="a207b-105">財務諸表デザイナーでのレポート定義</span><span class="sxs-lookup"><span data-stu-id="a207b-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a207b-106">この記事では、レポート定義に関する情報を示します。</span><span class="sxs-lookup"><span data-stu-id="a207b-106">This article provides information about report definitions.</span></span> <span data-ttu-id="a207b-107">レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。</span><span class="sxs-lookup"><span data-stu-id="a207b-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a207b-108">レポート定義は、レポートをカスタマイズするためのオプションおよび設定も提供します。</span><span class="sxs-lookup"><span data-stu-id="a207b-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="a207b-109">レポート定義は、行定義、列定義、およびオプションのレポート ツリー定義を使用してレポートを作成するレポート コンポーネント (または構成要素) です。</span><span class="sxs-lookup"><span data-stu-id="a207b-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a207b-110">レポート定義は、レポートのカスタマイズに使用できるオプションおよび設定も提供しています。</span><span class="sxs-lookup"><span data-stu-id="a207b-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="a207b-111">行定義と列定義を定義したら、レポート定義に結合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a207b-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="a207b-112">この時点で、詳細レベルおよびレポートの日付などの定義の他の側面も定義します。</span><span class="sxs-lookup"><span data-stu-id="a207b-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="a207b-113">これで、レポートの保存および生成ができます。</span><span class="sxs-lookup"><span data-stu-id="a207b-113">You can then save and generate a report.</span></span> <span data-ttu-id="a207b-114">財務諸表は、レポート用に次の詳細レベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="a207b-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="a207b-115">財務</span><span class="sxs-lookup"><span data-stu-id="a207b-115">Financial</span></span>
- <span data-ttu-id="a207b-116">[財務と勘定]</span><span class="sxs-lookup"><span data-stu-id="a207b-116">Financial and Account</span></span>
- <span data-ttu-id="a207b-117">[財務]、[勘定] および [トランザクション]</span><span class="sxs-lookup"><span data-stu-id="a207b-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="a207b-118">ただし、Microsoft Dynamics ERP システムにデータを格納する方法によって、トランザクションの詳細がレポートで使用できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a207b-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="a207b-119">レポート定義の作成</span><span class="sxs-lookup"><span data-stu-id="a207b-119">Create a report definition</span></span>
1. <span data-ttu-id="a207b-120">[レポート デザイナー] の**ファイル**メニューで、**新規**をクリックし、**レポート定義**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a207b-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="a207b-121">**レポート**、**出荷および配送**、**ヘッダーおよびフッター**、**設定**タブで、適切な情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a207b-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="a207b-122">レポート定義の内容</span><span class="sxs-lookup"><span data-stu-id="a207b-122">Contents of a report definition</span></span>
<span data-ttu-id="a207b-123">次の表は、レポート定義のタブと、情報の使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a207b-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a207b-124">タブ</span><span class="sxs-lookup"><span data-stu-id="a207b-124">Tab</span></span></th>
<th><span data-ttu-id="a207b-125">説明</span><span class="sxs-lookup"><span data-stu-id="a207b-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a207b-126">レポート </span><span class="sxs-lookup"><span data-stu-id="a207b-126">Report</span></span></td>
<td><span data-ttu-id="a207b-127">レポートを作成し、レポートをコンフィギュレーションし、既存のレポートを変更します。</span><span class="sxs-lookup"><span data-stu-id="a207b-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a207b-128">[出荷および配送]</span><span class="sxs-lookup"><span data-stu-id="a207b-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="a207b-129">レポートの出力のタイプと出力先を変更します。</span><span class="sxs-lookup"><span data-stu-id="a207b-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a207b-130">[ヘッダーとフッター]</span><span class="sxs-lookup"><span data-stu-id="a207b-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="a207b-131">レポートのヘッダーおよびフッターを定義および書式設定します。</span><span class="sxs-lookup"><span data-stu-id="a207b-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="a207b-132">たとえば、ヘッダーまたはフッターにテキストや画像を追加できます。</span><span class="sxs-lookup"><span data-stu-id="a207b-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="a207b-133">財務諸表は、画像の .bmp、.jpg、.png ファイルをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a207b-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="a207b-134">自動テキスト コードを追加して、会社名、レポート名、ページ番号などの他の情報を挿入できます。</span><span class="sxs-lookup"><span data-stu-id="a207b-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a207b-135">設定</span><span class="sxs-lookup"><span data-stu-id="a207b-135">Settings</span></span></td>
<td><span data-ttu-id="a207b-136">次の設定などのレポート定義の設定を指定します :</span><span class="sxs-lookup"><span data-stu-id="a207b-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="a207b-137">金額の書式設定および丸め</span><span class="sxs-lookup"><span data-stu-id="a207b-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="a207b-138">詳細レポートの書式設定</span><span class="sxs-lookup"><span data-stu-id="a207b-138">Format detail reports</span></span></li>
<li><span data-ttu-id="a207b-139">レポート ツリーの書式設定</span><span class="sxs-lookup"><span data-stu-id="a207b-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="a207b-140">例外レポートの生成</span><span class="sxs-lookup"><span data-stu-id="a207b-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="a207b-141">通貨換算の指定</span><span class="sxs-lookup"><span data-stu-id="a207b-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="a207b-142">小計およびフィルターの勘定の詳細</span><span class="sxs-lookup"><span data-stu-id="a207b-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="a207b-143">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="a207b-143">Additional resources</span></span>

[<span data-ttu-id="a207b-144">財務報告</span><span class="sxs-lookup"><span data-stu-id="a207b-144">Financial reporting</span></span>](financial-reporting-intro.md)