---
title: 電子申告 (ER) のモデル マッピング コンフィギュレーションの作成
description: 新しい電子申告 (ER) モデル マッピング コンフィギュレーションをデザインして、効率的な集計計算の組み込み ER 機能を使用するには、この手順を使用します。
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a614ce0f055691e36c1aab5d84d4fc3355026f1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752559"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a><span data-ttu-id="a3429-103">電子申告 (ER) のモデル マッピング コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="a3429-103">Create Electronic reporting (ER) model mapping configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3429-104">新しい電子申告 (ER) モデル マッピング コンフィギュレーションをデザインして、効率的な集計計算の組み込み ER 機能を使用するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3429-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="a3429-105">この手順では、サンプル会社 Litware、Inc. のコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a3429-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="a3429-106">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられている使用のために作成されています。</span><span class="sxs-lookup"><span data-stu-id="a3429-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="a3429-107">これらのステップは、任意のデータ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="a3429-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="a3429-108">これらの手順を完了するには、まず "コンフィギュレーション プロバイダーを作成し、有効としてマークする" の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3429-108">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>

1. <span data-ttu-id="a3429-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3429-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="a3429-110">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3429-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="a3429-111">このコンフィギュレーション プロバイダーが表示されない場合は、"コンフィギュレーション プロバイダーを作成し、有効としてマークする" の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3429-111">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>  
2. <span data-ttu-id="a3429-112">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a3429-113">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-113">Click Show filters.</span></span>
4. <span data-ttu-id="a3429-114">[名前] フィールドでは、フィルター値「イントラスタット」を入力し、フィールド オペレーター「次の値で始まる」を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3429-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="a3429-115">"イントラスタット データ モデル コンフィギュレーションを検索するには、このフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="a3429-115">Apply this filter to find the 'Intrastat' data model configuration.</span></span> <span data-ttu-id="a3429-116">このモデルは、既にコンフィギュレーション ツリー内に存在します。</span><span class="sxs-lookup"><span data-stu-id="a3429-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="a3429-117">存在する場合は、下位の次のタスクをスキップします。</span><span class="sxs-lookup"><span data-stu-id="a3429-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="a3429-118">Microsoft 提供のイントラスタットのモデル コンフィギュレーションを取得</span><span class="sxs-lookup"><span data-stu-id="a3429-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="a3429-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3429-119">Close the page.</span></span>
2. <span data-ttu-id="a3429-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3429-120">Close the page.</span></span>
3. <span data-ttu-id="a3429-121">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3429-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="a3429-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a3429-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a3429-123">Microsoft プロバイダー タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a3429-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="a3429-124">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-124">Click Repositories.</span></span>
    * <span data-ttu-id="a3429-125">Microsoft プロバイダー タイルで [リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="a3429-126">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-126">Click Show filters.</span></span>
7. <span data-ttu-id="a3429-127">"タイプ名" フィールドでは、フィルター値 "リソース" を入力し、フィルター演算子 "部分一致" を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3429-127">In the "Type name" field, enter the filter value, "resources" and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="a3429-128">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-128">Click Open.</span></span>
9. <span data-ttu-id="a3429-129">ツリーで、[イントラスタット モデル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3429-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="a3429-130">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-130">Click Import.</span></span>
11. <span data-ttu-id="a3429-131">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-131">Click Yes.</span></span>
    * <span data-ttu-id="a3429-132">新しい ER 機能の使用方法を調べるために、使用するデータ モデルを含む ER モデルのコンフィギュレーションがインポートされます。</span><span class="sxs-lookup"><span data-stu-id="a3429-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="a3429-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3429-133">Close the page.</span></span>
13. <span data-ttu-id="a3429-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a3429-134">Close the page.</span></span>
14. <span data-ttu-id="a3429-135">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="a3429-136">新しいモデル マッピング コンフィギュレーションを追加</span><span class="sxs-lookup"><span data-stu-id="a3429-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="a3429-137">ツリーで、[イントラスタット モデル] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3429-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="a3429-138">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="a3429-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="a3429-139">[新規] フィールドで、「データ モデル イントラスタットに基づいたモデル マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a3429-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="a3429-140">[名前] フィールドで、「イントラスタットのサンプル マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a3429-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="a3429-141">イントラスタットのサンプル マッピング</span><span class="sxs-lookup"><span data-stu-id="a3429-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="a3429-142">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3429-142">Click Create configuration.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]