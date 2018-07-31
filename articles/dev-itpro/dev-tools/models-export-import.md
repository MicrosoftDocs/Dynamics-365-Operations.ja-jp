---
title: "モデルのエクスポートとインポート"
description: "モデル ファイルは顧客およびパートナーにモデルを配布して、開発環境にインストールすることができます。 これらは Lifecycle Services (LCS) ソリューションの主要なコンポーネントです。 モデル ファイルには、モデル記述子ファイル、メタデータ、ソース コード、および参照先の .NET アセンブリ (ある場合) が含まれます。 この記事では、モデルをモデル ファイルにエクスポートし、モデル ファイルをインストールし、開発環境でモデルを削除する方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 20451
ms.assetid: 9eb3be56-6382-43df-a247-eae0dcaf46b8
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 75f4aff14ab883f294f214ecd8c53b5c7cb1f291
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="export-and-import-a-model"></a><span data-ttu-id="c1f2a-106">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="c1f2a-106">Export and import a model</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1f2a-107">モデル ファイルは顧客およびパートナーにモデルを配布して、開発環境にインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-107">Model files let you distribute models to customers and partners, and can be installed in development environments.</span></span> <span data-ttu-id="c1f2a-108">これらは Lifecycle Services (LCS) ソリューションの主要なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-108">They are key components of a Lifecycle Services (LCS) solution.</span></span> <span data-ttu-id="c1f2a-109">モデル ファイルには、モデル記述子ファイル、メタデータ、ソース コード、および参照先の .NET アセンブリ (ある場合) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-109">Model files contain a model descriptor file, metadata, source code, and referenced .NET assemblies (when applicable).</span></span> <span data-ttu-id="c1f2a-110">この記事では、モデルをモデル ファイルにエクスポートし、モデル ファイルをインストールし、開発環境でモデルを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-110">This article describes how to export a model into a model file, install a model file, and delete a model in a development environment.</span></span>

<a name="export-a-model-into-a-model-file-for-distribution"></a><span data-ttu-id="c1f2a-111">モデルを配布用のモデル ファイルにエクスポート</span><span class="sxs-lookup"><span data-stu-id="c1f2a-111">Export a model into a model file for distribution</span></span>
-------------------------------------------------

<span data-ttu-id="c1f2a-112">既存のモデルをモデル ファイルにエクスポートするには、ModelUtil.exe ツールと **-export** ディレクティブを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-112">To export an existing model into a model file, use the ModelUtil.exe tool and the **-export** directive.</span></span> <span data-ttu-id="c1f2a-113">このツールは、パッケージの bin フォルダー (通常は、c:\\packages\\bin または i:\\AosService\\PackagesLocalDirectory\\bin) に配置されています。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-113">This tool is located in the packages bin folder (typically, c:\\packages\\bin or i:\\AosService\\PackagesLocalDirectory\\bin).</span></span>

    ModelUtil.exe -export -metadatastorepath=[path of the metadata store] -modelname=[name of the model to export] -outputpath=[path of the folder where the model file should be saved]

<span data-ttu-id="c1f2a-114">**例**</span><span class="sxs-lookup"><span data-stu-id="c1f2a-114">**Example**</span></span>

    ModelUtil.exe -export -metadatastorepath=c:\packages -modelname="FleetManagement" -outputpath=c:\temp

<span data-ttu-id="c1f2a-115">上記の例は、c: \\temp に .axmodel ファイルを作成します。通常、次に、顧客プロジェクトや Microsoft Dynamics Lifecycle Services (LCS) ソリューション プロジェクトの資産ライブラリにモデル ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-115">The preceding example creates an .axmodel file under c:\\temp. Typically, you then upload the model file to the Asset Library of the customer project or the Microsoft Dynamics Lifecycle Services (LCS) solution project.</span></span>

## <a name="install-a-model-in-a-development-environment"></a><span data-ttu-id="c1f2a-116">開発環境でのモデルのインストール</span><span class="sxs-lookup"><span data-stu-id="c1f2a-116">Install a model in a development environment</span></span>
<span data-ttu-id="c1f2a-117">開発環境でモデル ファイルをインストールするには、ModelUtil.exe ツールと **-import** ディレクティブを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-117">To install a model file in a development environment, use the ModelUtil.exe tool and the **-import** directive.</span></span>

    ModelUtil.exe -import -metadatastorepath=[path of the metadata store where model should be imported] -file=[full path of the file to import]

<span data-ttu-id="c1f2a-118">モデルが開発環境で既に存在する場合、**-削除**指令を使用し、それを最初に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-118">If the model already exists in your development environment, you must first delete it by using the **-delete** directive.</span></span>

    ModelUtil.exe -delete -metadatastorepath=[path of the metadata store] -modelname=[name of the model to delete]

## <a name="resolve-conflicts"></a><span data-ttu-id="c1f2a-119">競合を解決</span><span class="sxs-lookup"><span data-stu-id="c1f2a-119">Resolve conflicts</span></span>
<span data-ttu-id="c1f2a-120">モデルを開発環境にインストールするときに、環境開発にそのモデルへのカスタマイズが含まれている場合、コードまたはメタデータの競合を解決する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-120">If you install a model on a development environment that contains customizations to that model (in a higher-layer), you may have to resolve code or metadata conflicts.</span></span> <span data-ttu-id="c1f2a-121">開発ツールを使用すると、競合しているすべての品目をグループ化するプロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-121">You can use the development tools to create a project that groups all items that have conflicts.</span></span>

1. <span data-ttu-id="c1f2a-122"><strong>Dynamics 365 **&gt;**AddIns</strong> で、<strong>コンフリクトからプロジェクトを作成する</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-122">Under <strong>Dynamics 365 **&gt; **AddIns</strong>, click <strong>Create Project from Conflicts</strong>.</span></span>
2. <span data-ttu-id="c1f2a-123">ダイアログ ボックスで、モデルを選択して競合を確認します。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-123">In the dialog box, select the model to check for conflicts.</span></span> <span data-ttu-id="c1f2a-124">これは、新しくインストールされたベースライン モデルの要素に対するカスタマイズを含まれるモデルです。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-124">This is the model that contains customizations to elements in the newly installed baseline model.</span></span>
3. <span data-ttu-id="c1f2a-125">**プロジェクトの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-125">Click **Create project**.</span></span> <span data-ttu-id="c1f2a-126">競合するモデルの要素のみを含むプロジェクトが生成されます。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-126">A project is generated that contains only the elements in that model that have conflicts.</span></span> <span data-ttu-id="c1f2a-127">[![AddUpdate\_MetaHotfix](./media/addupdate_metahotfix.png)](./media/addupdate_metahotfix.png)</span><span class="sxs-lookup"><span data-stu-id="c1f2a-127">[![AddUpdate\_MetaHotfix](./media/addupdate_metahotfix.png)](./media/addupdate_metahotfix.png)</span></span>
4. <span data-ttu-id="c1f2a-128">競合する要素のデザイナーを開いて、表示されたツールを使って競合を表示し、解決します。</span><span class="sxs-lookup"><span data-stu-id="c1f2a-128">Open the designer for the conflicting element to view and resolve conflicts by using the tools that are provided.</span></span> 

<!--For an introduction to conflict resolution tools that are available in a development environment, see the [Resolve conflicts using Visual Studio tools](https://mix.office.com/watch/1rl75ei2cs6d7) Microsoft Office Mix.-->





