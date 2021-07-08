---
title: モデルのエクスポートとインポート
description: この記事では、モデルをモデル ファイルにエクスポートし、モデル ファイルをインストールし、開発環境でモデルを削除する方法について説明します。
author: RobinARH
ms.date: 10/01/2018
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 20451
ms.assetid: 9eb3be56-6382-43df-a247-eae0dcaf46b8
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a749bb30b946a7545abeaede83738953489ed5d2
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189238"
---
# <a name="export-and-import-models"></a><span data-ttu-id="bf78c-103">モデルのエクスポートとインポート</span><span class="sxs-lookup"><span data-stu-id="bf78c-103">Export and import models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf78c-104">モデル ファイルは顧客およびパートナーにモデルを配布して、開発環境にインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="bf78c-104">Model files let you distribute models to customers and partners, and can be installed in development environments.</span></span> <span data-ttu-id="bf78c-105">これらは Lifecycle Services (LCS) ソリューションの主要なコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="bf78c-105">They are key components of a Lifecycle Services (LCS) solution.</span></span> <span data-ttu-id="bf78c-106">モデル ファイルには、モデル記述子ファイル、メタデータ、ソース コード、および参照先の .NET アセンブリ (ある場合) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="bf78c-106">Model files contain a model descriptor file, metadata, source code, and referenced .NET assemblies (when applicable).</span></span> <span data-ttu-id="bf78c-107">この記事では、モデルをモデル ファイルにエクスポートし、モデル ファイルをインストールし、開発環境でモデルを削除する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bf78c-107">This article describes how to export a model into a model file, install a model file, and delete a model in a development environment.</span></span>


## <a name="export-a-model-into-a-model-file-for-distribution"></a><span data-ttu-id="bf78c-108">モデルを配布用のモデル ファイルにエクスポート</span><span class="sxs-lookup"><span data-stu-id="bf78c-108">Export a model into a model file for distribution</span></span>

<span data-ttu-id="bf78c-109">既存のモデルをモデル ファイルにエクスポートするには、ModelUtil.exe ツールと **-export** ディレクティブを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf78c-109">To export an existing model into a model file, use the ModelUtil.exe tool and the **-export** directive.</span></span> <span data-ttu-id="bf78c-110">このツールは、パッケージの bin フォルダー (通常は、c:\\packages\\bin または i:\\AosService\\PackagesLocalDirectory\\bin) に配置されています。</span><span class="sxs-lookup"><span data-stu-id="bf78c-110">This tool is located in the packages bin folder (typically, c:\\packages\\bin or i:\\AosService\\PackagesLocalDirectory\\bin).</span></span>

```Console
ModelUtil.exe -export -metadatastorepath=[path of the metadata store] -modelname=[name of the model to export] -outputpath=[path of the folder where the model file should be saved]
```

<span data-ttu-id="bf78c-111">**例**</span><span class="sxs-lookup"><span data-stu-id="bf78c-111">**Example**</span></span>

```Console
ModelUtil.exe -export -metadatastorepath=c:\packages -modelname="FleetManagement" -outputpath=c:\temp
```

<span data-ttu-id="bf78c-112">上記の例は、c:\\temp に .axmodel ファイルを作成します。通常、次に、顧客プロジェクトや Microsoft Dynamics Lifecycle Services (LCS) ソリューション プロジェクトの資産ライブラリにモデル ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="bf78c-112">The preceding example creates an .axmodel file under c:\\temp. Typically, you then upload the model file to the Asset Library of the customer project or the Microsoft Dynamics Lifecycle Services (LCS) solution project.</span></span>

## <a name="install-a-model-in-a-development-environment"></a><span data-ttu-id="bf78c-113">開発環境でのモデルのインストール</span><span class="sxs-lookup"><span data-stu-id="bf78c-113">Install a model in a development environment</span></span>
<span data-ttu-id="bf78c-114">開発環境でモデル ファイルをインストールするには、ModelUtil.exe ツールと **-import** ディレクティブを使用します。</span><span class="sxs-lookup"><span data-stu-id="bf78c-114">To install a model file in a development environment, use the ModelUtil.exe tool and the **-import** directive.</span></span>

```Console
ModelUtil.exe -import -metadatastorepath=[path of the metadata store where model should be imported] -file=[full path of the file to import]
```

<span data-ttu-id="bf78c-115">モデルが開発環境で既に存在する場合、**-削除** 指令を使用し、それを最初に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf78c-115">If the model already exists in your development environment, you must first delete it by using the **-delete** directive.</span></span>

```Console
ModelUtil.exe -delete -metadatastorepath=[path of the metadata store] -modelname=[name of the model to delete]
```
    
> [!NOTE]
> <span data-ttu-id="bf78c-116">以前のバージョンを使用している場合、-replace パラメーターを使用して、オーバーレイヤー用の標準モデル (Foundation など) を置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="bf78c-116">If you're using an older version, you can use the -replace parameter to replace standard models (like Foundation) for overlayering.</span></span>    

## <a name="resolve-conflicts"></a><span data-ttu-id="bf78c-117">競合を解決</span><span class="sxs-lookup"><span data-stu-id="bf78c-117">Resolve conflicts</span></span>
<span data-ttu-id="bf78c-118">モデルを開発環境にインストールするときに、環境開発にそのモデルへのカスタマイズが含まれている場合、コードまたはメタデータの競合を解決する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="bf78c-118">If you install a model on a development environment that contains customizations to that model (in a higher-layer), you may have to resolve code or metadata conflicts.</span></span> <span data-ttu-id="bf78c-119">開発ツールを使用すると、競合しているすべての品目をグループ化するプロジェクトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="bf78c-119">You can use the development tools to create a project that groups all items that have conflicts.</span></span>

1. <span data-ttu-id="bf78c-120"><strong>Dynamics 365 &gt; AddIns</strong> で、<strong>コンフリクトからプロジェクトを作成する</strong>をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf78c-120">Under <strong>Dynamics 365 &gt; AddIns</strong>, click <strong>Create Project from Conflicts</strong>.</span></span>
2. <span data-ttu-id="bf78c-121">ダイアログ ボックスで、モデルを選択して競合を確認します。</span><span class="sxs-lookup"><span data-stu-id="bf78c-121">In the dialog box, select the model to check for conflicts.</span></span> <span data-ttu-id="bf78c-122">これは、新しくインストールされたベースライン モデルの要素に対するカスタマイズを含まれるモデルです。</span><span class="sxs-lookup"><span data-stu-id="bf78c-122">This is the model that contains customizations to elements in the newly installed baseline model.</span></span>
3. <span data-ttu-id="bf78c-123">**プロジェクトの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf78c-123">Click **Create project**.</span></span> <span data-ttu-id="bf78c-124">競合するモデルの要素のみを含むプロジェクトが生成されます。</span><span class="sxs-lookup"><span data-stu-id="bf78c-124">A project is generated that contains only the elements in that model that have conflicts.</span></span> 

    <span data-ttu-id="bf78c-125">[![AddUpdate\_MetaHotfix](./media/addupdate_metahotfix.png)](./media/addupdate_metahotfix.png)</span><span class="sxs-lookup"><span data-stu-id="bf78c-125">[![AddUpdate\_MetaHotfix](./media/addupdate_metahotfix.png)](./media/addupdate_metahotfix.png)</span></span>

4. <span data-ttu-id="bf78c-126">競合する要素のデザイナーを開いて、表示されたツールを使って競合を表示し、解決します。</span><span class="sxs-lookup"><span data-stu-id="bf78c-126">Open the designer for the conflicting element to view and resolve conflicts by using the tools that are provided.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]