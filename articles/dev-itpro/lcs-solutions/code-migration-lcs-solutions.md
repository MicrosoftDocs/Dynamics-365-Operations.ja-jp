---
title: "LCS ソリューションのコードの移行"
description: "このトピックでは、LCS ソリューションのコードをアップグレードおよび分析する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 196993
ms.assetid: aa01254e-4c18-43e4-81a1-0ef42a27871d
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 180e12c9a61ffb7df15c68062d3875c2683608ba
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="migrate-code-for-an-lcs-solution"></a><span data-ttu-id="0ae6e-103">LCS ソリューションのコードの移行</span><span class="sxs-lookup"><span data-stu-id="0ae6e-103">Migrate code for an LCS solution</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ae6e-104">ソリューション パッケージを完成させるための第一歩は、LCS の <strong>Migrate and Create Finance and Operations Solutions</strong> のベストプラクティスを使用してコードをアップグレードすることです。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-104">The first step in completing your solution package is to upgrade your code using the best practices in <strong>Migrate and Create Finance and Operations Solutions</strong> in LCS.</span></span> <span data-ttu-id="0ae6e-105">このステップが完了したら、カスタマイズ分析レポートを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-105">After this step is complete, you must run the Customization Analysis report.</span></span> <span data-ttu-id="0ae6e-106">このレポートは、カスタマイズおよび拡張モデルを分析し、事前定義されたベスト プラクティスのルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-106">This report analyzes your customization and extension models, and runs a predefined set of best practice rules.</span></span> 

<span data-ttu-id="0ae6e-107">カスタマイズ分析レポート (CAR) を生成するには、Microsoft Dynamics 365 for Finance and Operations 開発環境で次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-107">To generate the Customization Analysis report (CAR), run the following command on a Microsoft Dynamics 365 for Finance and Operations development environment.</span></span>

    xppbp.exe -metadata=<local packages folder> -all -model=<ModelName> -xmlLog=C:\BPCheckLogcd.xml -module=<PackageName> -car=<reportlocation>

<span data-ttu-id="0ae6e-108">このコマンドの見方の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-108">Here's an example of how this command might look.</span></span>

    xppbp.exe -metadata=C:\Packages -all -model=MyAppSuiteCustomizations -xmlLog=C:\temp\BPCheckLogcd.xml -module=ApplicationSuite -car=c:\temp\CAReport.xlsx

<span data-ttu-id="0ae6e-109">xppbp.exe ファイルは、*c:\packages\bin* または *I:\AosService\Packages\LocalDirectory\bin)* にあります。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-109">The xppbp.exe file is located in *c:\packages\bin* or *I:\AosService\Packages\LocalDirectory\bin)*.</span></span> <span data-ttu-id="0ae6e-110">レポートの**問題**タブ上に表示される警告またはエラーを解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-110">Any warnings or errors that appear on the **Issues** tab of the report must be resolved.</span></span> <span data-ttu-id="0ae6e-111">CAR レポートのコピーは、検証ミーティングよりも前に、Microsoft に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-111">A copy of the CAR report must be submitted to Microsoft prior to your validation meeting.</span></span> <span data-ttu-id="0ae6e-112">詳細については、Finance and Operations ヘルプ トピック、[カスタマイズ分析のレポート](../dev-tools/customization-analysis-report.md) および、問題と例外に関する [Dynamics コミュニティのブログ](http://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ae6e-112">For more information, see the Finance and Operations Help topic, [Customization Analysis Report](../dev-tools/customization-analysis-report.md) or refer to the [Dynamics Community blog](http://community.dynamics.com/ax/b/newdynamicsax/archive/2016/03/21/customization-analysis-report-exceptions-and-known-issues) for issues and exceptions.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0ae6e-113">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0ae6e-113">Additional resources</span></span>
--------

[<span data-ttu-id="0ae6e-114">AppSource 向け LCS ソリューション ホームページ</span><span class="sxs-lookup"><span data-stu-id="0ae6e-114">LCS Solutions for AppSource home page</span></span>](lcs-solutions-app-source.md)

[<span data-ttu-id="0ae6e-115">コードの移行の技術概念ガイド</span><span class="sxs-lookup"><span data-stu-id="0ae6e-115">Technical Concepts Guide for code migration</span></span>](../dev-tools/developer-home-page.md#code-migration)




