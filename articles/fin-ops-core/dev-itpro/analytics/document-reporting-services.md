---
title: ドキュメント レポート サービス
description: このトピックでは、サービス管理が簡略化され、開発者の生産性が向上し、強化されたレポート表示を提供するレポート ソリューションについて説明します。
author: RichdiMSFT
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.custom: 69191
ms.assetid: 57aaba22-4068-4c3f-9428-7fcd99632295
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4b240c884777f3d00dd8fac6bc34ca023ab56fa
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193089"
---
# <a name="document-reporting-services"></a><span data-ttu-id="01e29-103">ドキュメント レポート サービス</span><span class="sxs-lookup"><span data-stu-id="01e29-103">Document Reporting Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01e29-104">この記事では、利用可能な統合レポート ソリューションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="01e29-104">This article describes the integrated reporting solution that are available.</span></span> <span data-ttu-id="01e29-105">このソリューションにより、サービス管理が簡略化され、開発者の生産性が向上し、ユーザーのレポート表示エクスペリエンスが強化されます。</span><span class="sxs-lookup"><span data-stu-id="01e29-105">This solution simplifies service administration, increases developer productivity, and provides an enhanced report viewing experience for users.</span></span>

## <a name="document-reporting-services"></a><span data-ttu-id="01e29-106">ドキュメントの Reporting Services</span><span class="sxs-lookup"><span data-stu-id="01e29-106">Document Reporting Services</span></span>

<span data-ttu-id="01e29-107">ドキュメント レポート サービス は、Microsoft SQL Server Reporting Services (SSRS) に基づいています。</span><span class="sxs-lookup"><span data-stu-id="01e29-107">Document Reporting Services are based on Microsoft SQL Server Reporting Services (SSRS).</span></span> <span data-ttu-id="01e29-108">アプリケーションの現在のバージョンで、これらのサービスは Microsoft Azure 計算サービスでホストされます。</span><span class="sxs-lookup"><span data-stu-id="01e29-108">In the current version of the application, these services are hosted in the Microsoft Azure Compute service.</span></span> <span data-ttu-id="01e29-109">1 ボックス環境で開発している場合は、サービスも Azure コンピューティング エミュレーターでローカルに実行されます。</span><span class="sxs-lookup"><span data-stu-id="01e29-109">If you're developing in a one-box environment, the services also run locally in the Azure compute emulator.</span></span>

### <a name="service-deployment--local-vs-cloud"></a><span data-ttu-id="01e29-110">サービスの展開 - ローカルとクラウド</span><span class="sxs-lookup"><span data-stu-id="01e29-110">Service deployment – Local vs. cloud</span></span>

<span data-ttu-id="01e29-111">1 ボックス環境では、開発者は Microsoft Visual Studio を使用して、エンド ツー エンドでレポートを作成、変更、およびプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="01e29-111">In a one-box environment, developers can create, modify, and preview reports, from end to end, by using Microsoft Visual Studio.</span></span> <span data-ttu-id="01e29-112">アプリケーションのメタデータ ストアにレポートを追加するために、別のプロセスは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="01e29-112">A separate process isn't required in order to add reports to the application's metadata store.</span></span> <span data-ttu-id="01e29-113">レポートの変更は、他のソリューションの更新と一緒にパッケージ化され、ローカル環境での開発が完了した後にクラウドに展開されます。</span><span class="sxs-lookup"><span data-stu-id="01e29-113">Changes to reports are packaged together with other solution updates and then deployed to the cloud after development is completed in the local environment.</span></span>

### <a name="viewing-reports"></a><span data-ttu-id="01e29-114">レポートを表示する</span><span class="sxs-lookup"><span data-stu-id="01e29-114">Viewing reports</span></span> 

<span data-ttu-id="01e29-115">エンド ユーザーに提供される拡張レポート表示エクスペリエンスは、Microsoft Visual Studio のレポート プレビュー エクスペリエンスと同じものです。</span><span class="sxs-lookup"><span data-stu-id="01e29-115">The enhanced report viewing experience that provides for end users is the same as the report preview experience in Microsoft Visual Studio.</span></span> <span data-ttu-id="01e29-116">Visual Studio で個別のデザインのプレビューは以後使用しません。</span><span class="sxs-lookup"><span data-stu-id="01e29-116">You no longer use a separate design preview in Visual Studio.</span></span> <span data-ttu-id="01e29-117">代わりに、Ctrl+F5 を押すだけで、Internet Explorer ウィンドウでレポートを作成してプレビューできます。</span><span class="sxs-lookup"><span data-stu-id="01e29-117">Instead, just press Ctrl+F5 to build and preview the report in an Internet Explorer window.</span></span> <span data-ttu-id="01e29-118">レポートはクライアントに表示されるとおりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="01e29-118">The report appears exactly as it would appear in the client.</span></span> <span data-ttu-id="01e29-119">ユーザーのパラメーターの経験さえ同じです。</span><span class="sxs-lookup"><span data-stu-id="01e29-119">Even the user's parameter experience is the same.</span></span> <span data-ttu-id="01e29-120">次の画像は、Visual Studio から開いたレポート プレビューの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="01e29-120">The following image shows an example of a report preview that is opened from Visual Studio.</span></span>

<span data-ttu-id="01e29-121">[![レポート プレビューの例](./media/2_report.png)](./media/2_report.png)</span><span class="sxs-lookup"><span data-stu-id="01e29-121">[![Example of a report preview](./media/2_report.png)](./media/2_report.png)</span></span>

## <a name="service-administration-prerequisites"></a><span data-ttu-id="01e29-122">サービス管理の前提条件</span><span class="sxs-lookup"><span data-stu-id="01e29-122">Service administration prerequisites</span></span>
<span data-ttu-id="01e29-123">次のテーブルは、Microsoft Dynamics AX 2012 とアプリケーションの現在のバージョンのサービス管理の前提条件を比較しています。</span><span class="sxs-lookup"><span data-stu-id="01e29-123">The following table compares the service administration prerequisites for Microsoft Dynamics AX 2012 and the current version of the application.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="01e29-124">AX 2012</span><span class="sxs-lookup"><span data-stu-id="01e29-124">AX 2012</span></span></th>
<th><span data-ttu-id="01e29-125">アプリケーションの現在のバージョン</span><span class="sxs-lookup"><span data-stu-id="01e29-125">The current version of the application</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="01e29-126">レポートの開発環境には、次の前提条件があります。</span><span class="sxs-lookup"><span data-stu-id="01e29-126">A report development environment has the following prerequisites:</span></span>
<ul>
<li><span data-ttu-id="01e29-127">SSRS がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="01e29-127">SSRS must be installed.</span></span></li>
<li><span data-ttu-id="01e29-128">SSRS は、Reporting Services 構成マネージャーを使用して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="01e29-128">SSRS must be configured by using Reporting Services Configuration Manager.</span></span></li>
<li><span data-ttu-id="01e29-129">アプリケーションの SSRS 拡張機能がインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="01e29-129">SSRS extensions for the application must be installed.</span></span></li>
</ul></td>
<td><span data-ttu-id="01e29-130">Reporting Services は、アプリケーション サーバーとともに Azure コンピューティング エミュレーターで実行されます。</span><span class="sxs-lookup"><span data-stu-id="01e29-130">Reporting services run in the Azure compute emulator, together with the application server.</span></span> <span data-ttu-id="01e29-131">したがって、SSRS サービス管理の前提条件はありません。</span><span class="sxs-lookup"><span data-stu-id="01e29-131">Therefore, there are no SSRS service administration prerequisites.</span></span> <span data-ttu-id="01e29-132">レポートがローカル レポート作成サービスに配置された後は、クライアントからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="01e29-132">After reports have been deployed to the local reporting services, they can be accessed from the client.</span></span></td>
</tr>
</tbody>
</table>

## <a name="developing-application-reports"></a><span data-ttu-id="01e29-133">アプリケーションのレポートの開発</span><span class="sxs-lookup"><span data-stu-id="01e29-133">Developing application reports</span></span>
<span data-ttu-id="01e29-134">Visual Studio では、レポート ソリューションを完全に作成および検証できるので、現在のバージョンでレポートを作成するプロセスは AX 2012 で行うよりも簡単です。</span><span class="sxs-lookup"><span data-stu-id="01e29-134">The process for developing a report in the current version is easier than it is in AX 2012, because you can create and validate a reporting solution entirely in Visual Studio.</span></span> <span data-ttu-id="01e29-135">次のテーブルは、アプリケーションがどのようにしてクエリに基づく自動設計レポートを追加するための基本手順を簡素化するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="01e29-135">The following table describes how the application simplifies the basic procedure for adding an automatic design report that is based on a query.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="01e29-136">AX 2012</span><span class="sxs-lookup"><span data-stu-id="01e29-136">AX 2012</span></span></th>
<th><span data-ttu-id="01e29-137">アプリケーションの現在のバージョン</span><span class="sxs-lookup"><span data-stu-id="01e29-137">The current version of the application</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><ol>
<li><span data-ttu-id="01e29-138">アプリケーションの、アプリケーション オブジェクト ツリー (AOT) でクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="01e29-138">In the application, create a query in the Application Object Tree (AOT).</span></span></li>
<li><span data-ttu-id="01e29-139">Visual Studio で、レポート プロジェクトを作成してクエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="01e29-139">In Visual Studio, create a reporting project, and add the query to it.</span></span></li>
<li><span data-ttu-id="01e29-140">Visual Studio モデル エディターでレポートを編集します。</span><span class="sxs-lookup"><span data-stu-id="01e29-140">Edit the report in the Visual Studio model editor.</span></span></li>
<li><span data-ttu-id="01e29-141">モデル エディタ ツールバーを使用して Visual Studio でレポート デザインをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="01e29-141">Preview the report design in Visual Studio by using the model editor toolbar.</span></span></li>
<li><span data-ttu-id="01e29-142">Visual Studio を使用して AOT にレポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="01e29-142">Use Visual Studio to add the report to the AOT.</span></span></li>
<li><span data-ttu-id="01e29-143">クライアントの AOT を使用してレポートのメニュー項目を作成し、メニュー項目をメニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="01e29-143">Use the AOT in the client to create a menu item for the report, and add the menu item to a menu.</span></span></li>
<li><span data-ttu-id="01e29-144">AOT を使用してレポートをレポート サーバーに展開します。</span><span class="sxs-lookup"><span data-stu-id="01e29-144">Use the AOT to deploy the report to the report server.</span></span></li>
<li><span data-ttu-id="01e29-145">クライアントのレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="01e29-145">Verify the report in the client.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="01e29-146">Visual Studio で、レポート プロジェクトとクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="01e29-146">In Visual Studio, create a reporting project and the query.</span></span></li>
<li><span data-ttu-id="01e29-147">Visual Studio でレポートを編集します。</span><span class="sxs-lookup"><span data-stu-id="01e29-147">Edit the report in Visual Studio.</span></span></li>
<li><span data-ttu-id="01e29-148">Visual Studio で、メニュー項目にレポートを追加し、スタートアップ オブジェクトとしてメニュー項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="01e29-148">In Visual Studio, add the report to a menu item, and set the menu item as a startup object.</span></span></li>
<li><span data-ttu-id="01e29-149">AOT を使用してレポートをレポート サーバーに展開します。</span><span class="sxs-lookup"><span data-stu-id="01e29-149">Use the AOT to deploy the report to the report server.</span></span></li>
<li><span data-ttu-id="01e29-150">Ctrl+F5 キーを押して、アプリケーションのレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="01e29-150">Press Ctrl+F5 to verify the report in the application.</span></span>
<blockquote>[!NOTE] <span data-ttu-id="01e29-151">モデル エディタからのレポート デザインの個別のプレビューはありません。</span><span class="sxs-lookup"><span data-stu-id="01e29-151">There is no longer a separate preview of the report design from the model editor.</span></span></blockquote>
</li>
<li><span data-ttu-id="01e29-152">ソリューション全体が完了したら、ソリューション全体を 1 つのパッケージにしてクラウドに配置します。</span><span class="sxs-lookup"><span data-stu-id="01e29-152">When the whole solution is completed, deploy it to the cloud in one package.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
