---
title: パッケージのアンインストール
description: このトピックでは、配置可能パッケージを環境から削除する方法について説明します。
author: manado
manager: AnnBe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8e3e23d71481d1bdd5c2690619cd8d30530fcb3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191622"
---
# <a name="uninstall-a-package"></a><span data-ttu-id="00289-103">パッケージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="00289-103">Uninstall a package</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00289-104">場合によっては、配置可能パッケージをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00289-104">Occasionally, you might have to uninstall a deployable package.</span></span> <span data-ttu-id="00289-105">たとえば、ソース コードを再編成することができます。</span><span class="sxs-lookup"><span data-stu-id="00289-105">For example, you might be reorganizing your source code.</span></span> <span data-ttu-id="00289-106">また、独立系ソフトウェア ベンダー (ISV) 製品はすでに必要がなく、ライセンスを更新していません。</span><span class="sxs-lookup"><span data-stu-id="00289-106">Alternatively, you no longer require an independent software vendor (ISV) product and haven't renewed the license.</span></span> <span data-ttu-id="00289-107">したがって、パッケージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00289-107">Therefore, you must remove the package.</span></span>

## <a name="remove-a-model"></a><span data-ttu-id="00289-108">モデルの削除</span><span class="sxs-lookup"><span data-stu-id="00289-108">Remove a model</span></span>

<span data-ttu-id="00289-109">モデルは、パッケージの一部であるデザイン時の概念です。</span><span class="sxs-lookup"><span data-stu-id="00289-109">A model is a design-time concept that is part of a package.</span></span> <span data-ttu-id="00289-110">モジュール内の唯一のモデルでないモデルは、ソース コードからモデルを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="00289-110">When a model isn't the only model in a module, you can just remove it from the source code.</span></span> <span data-ttu-id="00289-111">更新されたモジュールを配置するときに古いモジュールが上書きされるため、その他の手順は行う必要がありません。</span><span class="sxs-lookup"><span data-stu-id="00289-111">No other steps are required, because when you deploy the updated module, the old module is overwritten.</span></span> <span data-ttu-id="00289-112">すべてのオーバーレイ モデルは、このカテゴリに分類されます。</span><span class="sxs-lookup"><span data-stu-id="00289-112">All overlayer models fall into this category.</span></span> <span data-ttu-id="00289-113">詳細については、[モデルの削除](../dev-tools/models.md#deleting-a-model)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00289-113">For more information, see [Deleting a model](../dev-tools/models.md#deleting-a-model).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="00289-114">前提条件</span><span class="sxs-lookup"><span data-stu-id="00289-114">Prerequisites</span></span>

- <span data-ttu-id="00289-115">いずれかのモデルが削除されるモジュールを参照している場合、そのモジュールから参照を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00289-115">If any models reference the module that will be removed, the references must be removed from them.</span></span> <span data-ttu-id="00289-116">削除する必要がある参照を検索する方法については、[モデルの依存関係の表示](../dev-tools/models.md#viewing-package-dependencies)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00289-116">For information about how to find the references that must be removed, see [Viewing model dependencies](../dev-tools/models.md#viewing-package-dependencies).</span></span>
- <span data-ttu-id="00289-117">参照が削除されたすべてのモジュールを構築し展開します。</span><span class="sxs-lookup"><span data-stu-id="00289-117">Build and deploy any modules that references were removed from.</span></span>
- <span data-ttu-id="00289-118">モジュールをアンインストールする前に、モジュールへの参照およびモジュールからの参照を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00289-118">All references to and from the modules must be removed before you begin to uninstall the module.</span></span> <span data-ttu-id="00289-119">モジュールのすべての参照を削除するには、モデルに 1 つのクラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="00289-119">To remove all a module's references, add a single class to the model.</span></span> <span data-ttu-id="00289-120">このクラスにコードを含むことはできません。</span><span class="sxs-lookup"><span data-stu-id="00289-120">This class should contain no code.</span></span> <span data-ttu-id="00289-121">これにはアプリケーション プラットフォームへの参照のみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00289-121">It should contain only a reference to the application platform.</span></span>

## <a name="uninstall-a-package"></a><span data-ttu-id="00289-122">パッケージのアンインストール</span><span class="sxs-lookup"><span data-stu-id="00289-122">Uninstall a package</span></span>

1. <span data-ttu-id="00289-123">**ModuleToRemove.txt** という名前のファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="00289-123">Create a file that is named **ModuleToRemove.txt**.</span></span>
2. <span data-ttu-id="00289-124">ファイルには、別の行で削除する各モジュールの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="00289-124">In the file, put the name of each module that you want to remove on a separate line.</span></span> <span data-ttu-id="00289-125">削除する各モジュールの前提条件が完了したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00289-125">Make sure that you've completed the prerequisites for each module that you're removing.</span></span>
3. <span data-ttu-id="00289-126">有効な配置可能なパッケージを作成して、**package\\AOSService\\Scripts** フォルダに ModuleToRemove.txt ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="00289-126">Create a valid deployable package, and put the ModuleToRemove.txt file in the **package\\AOSService\\Scripts** folder.</span></span>
4. <span data-ttu-id="00289-127">配置可能パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="00289-127">Install the deployable package.</span></span> <span data-ttu-id="00289-128">配置可能パッケージをインストールする方法の詳細については、[クラウド配置に更新プログラムを適用する](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00289-128">For more information about how to install deployable packages, see [Apply updates to a cloud deployment](apply-deployable-package-system.md).</span></span>
5. <span data-ttu-id="00289-129">実稼動環境で、この手順を実行する前に、パッケージがアンインストールされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="00289-129">Verify that the package was uninstalled before you complete this procedure in a production environment.</span></span>