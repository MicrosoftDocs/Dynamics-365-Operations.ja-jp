---
title: ドキュメントの Reporting Services
description: この記事では、Microsoft Dynamics 365 for Finance and Operations で利用できる統合レポート ソリューションについて説明します。 このソリューションにより、サービス管理が簡略化され、開発者の生産性が向上し、ユーザーのレポート表示エクスペリエンスが強化されます。
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 69191
ms.assetid: 57aaba22-4068-4c3f-9428-7fcd99632295
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2616ef93dcf99ea35f1b123253c26663bda68009
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369210"
---
# <a name="document-reporting-services"></a><span data-ttu-id="94723-104">ドキュメントの Reporting Services</span><span class="sxs-lookup"><span data-stu-id="94723-104">Document Reporting Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94723-105">この記事では、Microsoft Dynamics 365 for Finance and Operations で利用できる統合レポート ソリューションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="94723-105">This article describes the integrated reporting solution that is available in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="94723-106">このソリューションにより、サービス管理が簡略化され、開発者の生産性が向上し、ユーザーのレポート表示エクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="94723-106">This solution simplifies service administration, increases developer productivity, and provides an enhanced report viewing experience for users.</span></span>

## <a name="document-reporting-services"></a><span data-ttu-id="94723-107">ドキュメントの Reporting Services</span><span class="sxs-lookup"><span data-stu-id="94723-107">Document Reporting Services</span></span>

<span data-ttu-id="94723-108">ドキュメント レポート サービス は、Microsoft SQL Server Reporting Services (SSRS) に基づいています。</span><span class="sxs-lookup"><span data-stu-id="94723-108">Document Reporting Services are based on Microsoft SQL Server Reporting Services (SSRS).</span></span> <span data-ttu-id="94723-109">Microsoft Dynamics 365 for Finance and Operations の現在のバージョンで、これらのサービスは Microsoft Azure 計算サービスでホストされます。</span><span class="sxs-lookup"><span data-stu-id="94723-109">In the current version of Microsoft Dynamics 365 for Finance and Operations, these services are hosted in the Microsoft Azure compute service.</span></span> <span data-ttu-id="94723-110">1 ボックス環境で開発している場合は、サービスも Azure コンピューティング エミュレーターでローカルに実行されます。</span><span class="sxs-lookup"><span data-stu-id="94723-110">If you're developing in a one-box environment, the services also run locally in the Azure compute emulator.</span></span>

### <a name="service-deployment--local-vs-cloud"></a><span data-ttu-id="94723-111">サービスの展開 - ローカルとクラウド</span><span class="sxs-lookup"><span data-stu-id="94723-111">Service deployment – Local vs. cloud</span></span>

<span data-ttu-id="94723-112">1 ボックス環境では、開発者は Microsoft Visual Studio 2015 を使用して、エンド ツー エンドでレポートを作成、変更、およびプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="94723-112">In a one-box environment, developers can create, modify, and preview reports, from end to end, by using Microsoft Visual Studio 2015.</span></span> <span data-ttu-id="94723-113">アプリケーションのメタデータ ストアにレポートを追加するために、別のプロセスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="94723-113">A separate process isn't required in order to add reports to the application's metadata store.</span></span> <span data-ttu-id="94723-114">レポートの変更は、他のソリューションの更新と一緒にパッケージ化され、ローカル環境での開発が完了した後にクラウドに展開されます。</span><span class="sxs-lookup"><span data-stu-id="94723-114">Changes to reports are packaged together with other solution updates and then deployed to the cloud after development is completed in the local environment.</span></span>

<span data-ttu-id="94723-115">[![document-reporting-services-topology](./media/document-reporting-services-topology.png)](./media/document-reporting-services-topology.png)</span><span class="sxs-lookup"><span data-stu-id="94723-115">[![document-reporting-services-topology](./media/document-reporting-services-topology.png)](./media/document-reporting-services-topology.png)</span></span>

### <a name="viewing-reports-in-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="94723-116">Dynamics 365 for Finance and Operations でレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="94723-116">Viewing reports in Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="94723-117">Finance and Operations がエンドユーザーに提供する拡張レポート表示エクスペリエンスは、Microsoft Visual Studio のレポート プレビュー エクスペリエンスと同じです。</span><span class="sxs-lookup"><span data-stu-id="94723-117">The enhanced report viewing experience that Finance and Operations provides for end users is the same as the report preview experience in Microsoft Visual Studio.</span></span> <span data-ttu-id="94723-118">Visual Studio で個別のデザインのプレビューは以後使用しません。</span><span class="sxs-lookup"><span data-stu-id="94723-118">You no longer use a separate design preview in Visual Studio.</span></span> <span data-ttu-id="94723-119">代わりに、Ctrl+F5 を押すだけで、Internet Explorer ウィンドウでレポートを作成してプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="94723-119">Instead, just press Ctrl+F5 to build and preview the report in an Internet Explorer window.</span></span> <span data-ttu-id="94723-120">レポートはクライアントに表示されるとおりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="94723-120">The report appears exactly as it would appear in the client.</span></span> <span data-ttu-id="94723-121">ユーザーのパラメーターの経験さえ同じです。</span><span class="sxs-lookup"><span data-stu-id="94723-121">Even the user's parameter experience is the same.</span></span> <span data-ttu-id="94723-122">次のスクリーン ショットは、Visual Studio から開いたレポート プレビューの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="94723-122">The following screen shot shows an example of a report preview that is opened from Visual Studio.</span></span>

<span data-ttu-id="94723-123">[![レポート プレビューの例](./media/2_report.png)](./media/2_report.png)</span><span class="sxs-lookup"><span data-stu-id="94723-123">[![Example of a report preview](./media/2_report.png)](./media/2_report.png)</span></span>

## <a name="service-administration-prerequisites"></a><span data-ttu-id="94723-124">サービス管理の前提条件</span><span class="sxs-lookup"><span data-stu-id="94723-124">Service administration prerequisites</span></span>
<span data-ttu-id="94723-125">次のテーブルは、Microsoft Dynamics AX 2012 のサービス管理の前提条件と現在のバージョンの Finance and Operations を比較しています。</span><span class="sxs-lookup"><span data-stu-id="94723-125">The following table compares the service administration prerequisites for Microsoft Dynamics AX 2012 and the current version of Finance and Operations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94723-126">AX 2012</span><span class="sxs-lookup"><span data-stu-id="94723-126">AX 2012</span></span></th>
<th><span data-ttu-id="94723-127">Dynamics 365 for Finance and Operations の現在のバージョン</span><span class="sxs-lookup"><span data-stu-id="94723-127">The current version of Dynamics 365 for Finance and Operations</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94723-128">レポートの開発環境には、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="94723-128">A report development environment has the following prerequisites:</span></span>
<ul>
<li><span data-ttu-id="94723-129">SSRS がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="94723-129">SSRS must be installed.</span></span></li>
<li><span data-ttu-id="94723-130">SSRS は、Reporting Services 構成マネージャーを使用して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94723-130">SSRS must be configured by using Reporting Services Configuration Manager.</span></span></li>
<li><span data-ttu-id="94723-131">Finance and Operations の SSRS 拡張機能をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="94723-131">SSRS extensions for Finance and Operations must be installed.</span></span></li>
</ul></td>
<td><span data-ttu-id="94723-132">Reporting Services は、アプリケーション サーバーとともに Azure コンピューティング エミュレーターで実行されます。</span><span class="sxs-lookup"><span data-stu-id="94723-132">Reporting services run in the Azure compute emulator, together with the application server.</span></span> <span data-ttu-id="94723-133">したがって、SSRS サービス管理の前提条件はありません。</span><span class="sxs-lookup"><span data-stu-id="94723-133">Therefore, there are no SSRS service administration prerequisites.</span></span> <span data-ttu-id="94723-134">レポートがローカル レポート作成サービスに配置された後は、クライアントからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="94723-134">After reports have been deployed to the local reporting services, they can be accessed from the client.</span></span></td>
</tr>
</tbody>
</table>

## <a name="developing-application-reports"></a><span data-ttu-id="94723-135">アプリケーションのレポートの開発</span><span class="sxs-lookup"><span data-stu-id="94723-135">Developing application reports</span></span>
<span data-ttu-id="94723-136">Visual Studio 2015 では、レポート ソリューションを完全に作成および検証できるので、Finance and Operations の現在のバージョンでレポートを作成するプロセスは AX 2012 で行うよりも簡単です。</span><span class="sxs-lookup"><span data-stu-id="94723-136">The process for developing a report in the current version of Finance and Operations is easier than it is in AX 2012, because you can create and validate a reporting solution entirely in Visual Studio 2015.</span></span> <span data-ttu-id="94723-137">次のテーブルは、Finance and Operations がどのようにしてクエリに基づく自動設計レポートを追加するための基本手順を簡素化するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="94723-137">The following table describes how Finance and Operations simplifies the basic procedure for adding an automatic design report that is based on a query.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="94723-138">AX 2012</span><span class="sxs-lookup"><span data-stu-id="94723-138">AX 2012</span></span></th>
<th><span data-ttu-id="94723-139">Dynamics 365 for Finance and Operations の現在のバージョン</span><span class="sxs-lookup"><span data-stu-id="94723-139">The current version of Dynamics 365 for Finance and Operations</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><ol>
<li><span data-ttu-id="94723-140">Microsoft Dynamics 365 for Finance and Operations クライアントで、アプリケーション オブジェクト ツリー (AOT) でクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="94723-140">In the Microsoft Dynamics 365 for Finance and Operations client, create a query in the Application Object Tree (AOT).</span></span></li>
<li><span data-ttu-id="94723-141">Visual Studio で、レポート プロジェクトを作成してクエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="94723-141">In Visual Studio, create a reporting project, and add the query to it.</span></span></li>
<li><span data-ttu-id="94723-142">Visual Studio モデル エディターでレポートを編集します。</span><span class="sxs-lookup"><span data-stu-id="94723-142">Edit the report in the Visual Studio model editor.</span></span></li>
<li><span data-ttu-id="94723-143">モデル エディタ ツールバーを使用して Visual Studio でレポート デザインをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="94723-143">Preview the report design in Visual Studio by using the model editor toolbar.</span></span></li>
<li><span data-ttu-id="94723-144">Visual Studio を使用して AOT にレポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="94723-144">Use Visual Studio to add the report to the AOT.</span></span></li>
<li><span data-ttu-id="94723-145">クライアントの AOT を使用してレポートのメニュー項目を作成し、メニュー項目をメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="94723-145">Use the AOT in the client to create a menu item for the report, and add the menu item to a menu.</span></span></li>
<li><span data-ttu-id="94723-146">AOT を使用してレポートをレポート サーバーに展開します。</span><span class="sxs-lookup"><span data-stu-id="94723-146">Use the AOT to deploy the report to the report server.</span></span></li>
<li><span data-ttu-id="94723-147">クライアントのレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="94723-147">Verify the report in the client.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="94723-148">Visual Studio で、レポート プロジェクトとクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="94723-148">In Visual Studio, create a reporting project and the query.</span></span></li>
<li><span data-ttu-id="94723-149">Visual Studio でレポートを編集します。</span><span class="sxs-lookup"><span data-stu-id="94723-149">Edit the report in Visual Studio.</span></span></li>
<li><span data-ttu-id="94723-150">Visual Studio で、メニュー項目にレポートを追加し、スタートアップ オブジェクトとしてメニュー項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="94723-150">In Visual Studio, add the report to a menu item, and set the menu item as a startup object.</span></span></li>
<li><span data-ttu-id="94723-151">AOT を使用してレポートをレポート サーバーに展開します。</span><span class="sxs-lookup"><span data-stu-id="94723-151">Use the AOT to deploy the report to the report server.</span></span></li>
<li><span data-ttu-id="94723-152">Ctrl+F5 キーを押し、Finance and Operations クライアントでレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="94723-152">Press Ctrl+F5 to verify the report in the Finance and Operations client.</span></span>
<blockquote>[!NOTE] <span data-ttu-id="94723-153">モデル エディタからのレポート デザインの個別のプレビューはありません。</span><span class="sxs-lookup"><span data-stu-id="94723-153">There is no longer a separate preview of the report design from the model editor.</span></span></blockquote>
</li>
<li><span data-ttu-id="94723-154">ソリューション全体が完了したら、ソリューション全体を 1 つのパッケージにしてクラウドに配置します。</span><span class="sxs-lookup"><span data-stu-id="94723-154">When the whole solution is completed, deploy it to the cloud in one package.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>
