---
title: Finance and Operations アプリ ソリューションのコードの移行
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) で、コードをアップグレードおよび分析する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Lifecycle Services
ms.custom: 196993
ms.assetid: aa01254e-4c18-43e4-81a1-0ef42a27871d
ms.search.region: Global
ms.author: omarc
ms.openlocfilehash: ec4d4d58dd1b211c2532e2f1b14c422049fdbb36
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183279"
---
# <a name="migrate-code-for-finance-and-operations-apps-solutions"></a><span data-ttu-id="54551-103">Finance and Operations アプリ ソリューションのコードの移行</span><span class="sxs-lookup"><span data-stu-id="54551-103">Migrate code for Finance and Operations apps solutions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="54551-104">ソリューション パッケージを完成させるための第一歩は、Microsoft Dynamics Lifecycle Services (LCS) の **Finance and Operations アプリ ソリューションの移行と作成**のベスト プラクティスを使用してコードをアップグレードすることです。</span><span class="sxs-lookup"><span data-stu-id="54551-104">To complete your solution package, the first step is to upgrade your code by using the best practices in **Migrate and Create Finance and Operations Apps Solutions** in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="54551-105">ステップが完了したら、カスタマイズ分析のレポート (CAR) を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54551-105">After that step is completed, you must run the Customization Analysis Report (CAR).</span></span> <span data-ttu-id="54551-106">このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="54551-106">This report analyzes your customization and extension models, and runs a predefined set of best practice rules.</span></span> 

<span data-ttu-id="54551-107">CAR を生成するには、開発環境で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="54551-107">To generate the CAR, run the following command on a development environment.</span></span>

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

<span data-ttu-id="54551-108">このコマンドの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="54551-108">Here is an example of this command.</span></span>

    xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx

<span data-ttu-id="54551-109">xppbp.exe ファイルは、c:\\packages\\bin または I:\\AosService\\Packages\\LocalDirectory\\bin に配置されています。</span><span class="sxs-lookup"><span data-stu-id="54551-109">The xppbp.exe file is located in c:\\packages\\bin or I:\\AosService\\Packages\\LocalDirectory\\bin.</span></span> <span data-ttu-id="54551-110">レポートの**問題**タブ上に表示される警告またはエラーを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54551-110">You must resolve any warnings or errors that appear on the **Issues** tab of the report.</span></span> <span data-ttu-id="54551-111">CAR のコピーを、検証ミーティングよりも前に、Microsoft に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54551-111">You must then submit a copy of the CAR to Microsoft before your validation meeting.</span></span> <span data-ttu-id="54551-112">詳細については、[カスタマイズ分析のレポート](../dev-tools/customization-analysis-report.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54551-112">For more information, see [Customization Analysis Report](../dev-tools/customization-analysis-report.md).</span></span> <span data-ttu-id="54551-113">問題と例外の詳細については、Dynamics 365 Community ブログの投稿[カスタマイズ分析のレポート: 例外と既知の問題](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54551-113">For information about issues and exceptions, see the [Customization Analysis Report: Exceptions and known issues](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) post on the Dynamics 365 Community blog.</span></span>

## <a name="extensibility"></a><span data-ttu-id="54551-114">拡張性</span><span class="sxs-lookup"><span data-stu-id="54551-114">Extensibility</span></span>
<span data-ttu-id="54551-115">Microsoft Dynamics 365 for Finance and Operationsバージョン 8.0 (2018年4月) では、すべての製品モデルがシールされます。</span><span class="sxs-lookup"><span data-stu-id="54551-115">In Microsoft Dynamics 365 for Finance and Operations version 8.0 (April 2018), all product models are sealed.</span></span> <span data-ttu-id="54551-116">したがって、拡張機能ベースのカスタマイズのみが現在サポートされています。</span><span class="sxs-lookup"><span data-stu-id="54551-116">Therefore, only extension-based customizations are currently supported.</span></span> <span data-ttu-id="54551-117">拡張機能の詳細については、[拡張機能](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-home-page)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54551-117">For more information about extensibility, see [Extensibility](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/extensibility-home-page).</span></span>

<span data-ttu-id="54551-118">ソリューション パッケージを完成させるための第一歩は、LCS の <strong>Migrate and Create Finance and Operations アプリ ソリューション</strong> のベスト プラクティスを使用してコードをアップグレードすることです。</span><span class="sxs-lookup"><span data-stu-id="54551-118">The first step in completing your solution package is to upgrade your code using the best practices in <strong>Migrate and Create Finance and Operations Apps Solutions</strong> in LCS.</span></span> <span data-ttu-id="54551-119">このステップが完了したら、カスタマイズ分析レポートを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54551-119">After this step is complete, you must run the Customization Analysis report.</span></span> <span data-ttu-id="54551-120">このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="54551-120">This report analyzes your customization and extension models, and runs a predefined set of best practice rules.</span></span> 

<span data-ttu-id="54551-121">カスタマイズ分析レポート (CAR) を生成するには、開発環境で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="54551-121">To generate the Customization Analysis report (CAR), run the following command on a development environment.</span></span>

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

<span data-ttu-id="54551-122">このコマンドの見方の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="54551-122">Here's an example of how this command might look.</span></span>

    xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx

<span data-ttu-id="54551-123">xppbp.exe ファイルは、*c:\packages\bin* または *I:\AosService\Packages\LocalDirectory\bin)* にあります。</span><span class="sxs-lookup"><span data-stu-id="54551-123">The xppbp.exe file is located in *c:\packages\bin* or *I:\AosService\Packages\LocalDirectory\bin)*.</span></span> <span data-ttu-id="54551-124">レポートの**問題**タブ上に表示される警告またはエラーを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54551-124">Any warnings or errors that appear on the **Issues** tab of the report must be resolved.</span></span> <span data-ttu-id="54551-125">CAR レポートのコピーは、検証ミーティングよりも前に、Microsoft に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="54551-125">A copy of the CAR report must be submitted to Microsoft prior to your validation meeting.</span></span> <span data-ttu-id="54551-126">詳細については、[カスタマイズ分析のレポート](../dev-tools/customization-analysis-report.md) および、問題と例外に関する [Dynamics コミュニティのブログ](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="54551-126">For more information, see [Customization Analysis Report](../dev-tools/customization-analysis-report.md) or refer to the [Dynamics Community blog](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) for issues and exceptions.</span></span>

<a name="additional-resources"></a><span data-ttu-id="54551-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="54551-127">Additional resources</span></span>
--------
[<span data-ttu-id="54551-128">AppSource のアプリを公開</span><span class="sxs-lookup"><span data-stu-id="54551-128">Publishing an App in AppSource</span></span>](lcs-solutions-app-source.md)

[<span data-ttu-id="54551-129">コードの移行の技術概念ガイド</span><span class="sxs-lookup"><span data-stu-id="54551-129">Technical Concepts Guide for code migration</span></span>](../dev-tools/developer-home-page.md#code-migration)