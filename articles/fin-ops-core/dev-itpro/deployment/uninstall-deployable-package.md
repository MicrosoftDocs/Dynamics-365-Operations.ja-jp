---
title: パッケージのアンインストール
description: このトピックでは、配置可能パッケージを環境から削除する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac77f92ae947571dda5ee3ff2cf0aa97381b9b6f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685453"
---
# <a name="uninstall-a-package"></a><span data-ttu-id="b9631-103">パッケージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="b9631-103">Uninstall a package</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9631-104">場合によっては、配置可能パッケージをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9631-104">Occasionally, you might have to uninstall a deployable package.</span></span> <span data-ttu-id="b9631-105">たとえば、ソース コードを再編成することができます。</span><span class="sxs-lookup"><span data-stu-id="b9631-105">For example, you might be reorganizing your source code.</span></span> <span data-ttu-id="b9631-106">また、独立系ソフトウェア ベンダー (ISV) 製品はすでに必要がなく、ライセンスを更新していません。</span><span class="sxs-lookup"><span data-stu-id="b9631-106">Alternatively, you no longer require an independent software vendor (ISV) product and haven't renewed the license.</span></span> <span data-ttu-id="b9631-107">したがって、パッケージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9631-107">Therefore, you must remove the package.</span></span>

## <a name="remove-a-model"></a><span data-ttu-id="b9631-108">モデルの削除</span><span class="sxs-lookup"><span data-stu-id="b9631-108">Remove a model</span></span>

<span data-ttu-id="b9631-109">モデルは、パッケージの一部であるデザイン時の概念です。</span><span class="sxs-lookup"><span data-stu-id="b9631-109">A model is a design-time concept that is part of a package.</span></span> <span data-ttu-id="b9631-110">モジュール内の唯一のモデルでないモデルは、ソース コードからモデルを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="b9631-110">When a model isn't the only model in a module, you can just remove it from the source code.</span></span> <span data-ttu-id="b9631-111">更新されたモジュールを配置するときに古いモジュールが上書きされるため、その他の手順は行う必要がありません。</span><span class="sxs-lookup"><span data-stu-id="b9631-111">No other steps are required, because when you deploy the updated module, the old module is overwritten.</span></span> <span data-ttu-id="b9631-112">すべてのオーバーレイ モデルは、このカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="b9631-112">All overlayer models fall into this category.</span></span> <span data-ttu-id="b9631-113">詳細については、[モデルの削除](../dev-tools/models.md#deleting-a-model)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9631-113">For more information, see [Deleting a model](../dev-tools/models.md#deleting-a-model).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b9631-114">前提条件</span><span class="sxs-lookup"><span data-stu-id="b9631-114">Prerequisites</span></span>

- <span data-ttu-id="b9631-115">いずれかのモデルが削除されるモジュールを参照している場合、そのモジュールから参照を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9631-115">If any models reference the module that will be removed, the references must be removed from them.</span></span> <span data-ttu-id="b9631-116">削除する必要がある参照を検索する方法については、[モデルの依存関係の表示](../dev-tools/models.md#viewing-package-dependencies)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9631-116">For information about how to find the references that must be removed, see [Viewing model dependencies](../dev-tools/models.md#viewing-package-dependencies).</span></span>
- <span data-ttu-id="b9631-117">参照が削除されたすべてのモジュールを構築し展開します。</span><span class="sxs-lookup"><span data-stu-id="b9631-117">Build and deploy any modules that references were removed from.</span></span>
- <span data-ttu-id="b9631-118">モジュールをアンインストールする前に、モジュールへの参照およびモジュールからの参照を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9631-118">All references to and from the modules must be removed before you begin to uninstall the module.</span></span> <span data-ttu-id="b9631-119">モジュールのすべての参照を削除するには、モデルに 1 つのクラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="b9631-119">To remove all a module's references, add a single class to the model.</span></span> <span data-ttu-id="b9631-120">このクラスにコードを含むことはできません。</span><span class="sxs-lookup"><span data-stu-id="b9631-120">This class should contain no code.</span></span> <span data-ttu-id="b9631-121">これにはアプリケーション プラットフォームへの参照のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9631-121">It should contain only a reference to the application platform.</span></span>
- <span data-ttu-id="b9631-122">Microsoft モジュールは削除できません。</span><span class="sxs-lookup"><span data-stu-id="b9631-122">A Microsoft module cannot be removed.</span></span>  <span data-ttu-id="b9631-123">試行する場合、検証エラーが Lifecycle Services のパッケージに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b9631-123">If this is attempted, a validation error will be shown on the package in Lifecycle Services.</span></span>
- <span data-ttu-id="b9631-124">AOT の展開可能なパッケージの一部がインストールされている場合、モジュールは削除できません。</span><span class="sxs-lookup"><span data-stu-id="b9631-124">A module cannot be removed if it is part of the AOT deployable package being installed.</span></span>  <span data-ttu-id="b9631-125">モジュールを削除したい場合、ModuleToRemove.txt ファイルにファイル名を追加する前に、パッケージの一部ではないかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="b9631-125">If you want to remove a module, be sure that it is not part of the package before adding the name to the ModuleToRemove.txt file.</span></span>

## <a name="uninstall-a-package"></a><span data-ttu-id="b9631-126">パッケージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="b9631-126">Uninstall a package</span></span>

1. <span data-ttu-id="b9631-127">**ModuleToRemove.txt** という名前のファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="b9631-127">Create a file that is named **ModuleToRemove.txt**.</span></span>
2. <span data-ttu-id="b9631-128">ファイルには、別の行で削除する各モジュールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9631-128">In the file, put the name of each module that you want to remove on a separate line.</span></span> <span data-ttu-id="b9631-129">削除する各モジュールの前提条件が完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9631-129">Make sure that you've completed the prerequisites for each module that you're removing.</span></span>
3. <span data-ttu-id="b9631-130">有効な配置可能なパッケージを作成して、**package\\AOSService\\Scripts** フォルダに ModuleToRemove.txt ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="b9631-130">Create a valid deployable package, and put the ModuleToRemove.txt file in the **package\\AOSService\\Scripts** folder.</span></span>
4. <span data-ttu-id="b9631-131">パッケージを Lifecycle Services アセット ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="b9631-131">Upload the package to the Lifecycle Services asset library.</span></span> <span data-ttu-id="b9631-132">アセットが検証を終了するのを待ち、ページの右側にあるアセットの詳細パネルに表示される任意の警告を確認します。</span><span class="sxs-lookup"><span data-stu-id="b9631-132">Wait for the asset to finish validation, and review any warnings that are shown on the Asset Details panel on the right side of the page.</span></span>
5. <span data-ttu-id="b9631-133">配置可能パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="b9631-133">Install the deployable package.</span></span> <span data-ttu-id="b9631-134">配置可能パッケージをインストールする方法の詳細については、[クラウド配置に更新プログラムを適用する](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b9631-134">For more information about how to install deployable packages, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>
6. <span data-ttu-id="b9631-135">実稼動環境で、この手順を実行する前に、パッケージがアンインストールされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="b9631-135">Verify that the package was uninstalled before you complete this procedure in a production environment.</span></span>
