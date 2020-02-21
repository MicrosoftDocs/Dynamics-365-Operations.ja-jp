---
title: POS 拡張パッケージ情報の表示
description: このトピックでは、販売時点管理 (POS) の設定ビューの拡張パッケージ セクションに関する情報を提供します。 この新しいセクションは、コア POS の一部として含まれる拡張パッケージを一覧表示するとともに、ステータス情報やその他の詳細を表示できます。
author: mumani
manager: AnnBe
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-02-25
ms.dyn365.ops.version: AX 10.0.1
ms.openlocfilehash: a13b4dbd0c01b1d20885a1f25e115cf166a607c3
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004621"
---
# <a name="view-pos-extension-package-information"></a><span data-ttu-id="7af0d-104">POS 拡張パッケージ情報の表示</span><span class="sxs-lookup"><span data-stu-id="7af0d-104">View POS extension package information</span></span>


[!include [banner](../includes/banner.md)]




<span data-ttu-id="7af0d-105">販売時点管理 (POS) の **設定** ビューでは、**拡張パッケージ** セクションにコア POS の一部として含まれている POS 拡張パッケージのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-105">In the **Settings** view in the point of sale (POS), the **Extension packages** section shows the list of POS extension packages that are included as part of the core POS.</span></span> <span data-ttu-id="7af0d-106">各パッケージのタイルには、そのパッケージの状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-106">The tile for each package shows the status of that package.</span></span> <span data-ttu-id="7af0d-107">パッケージの状態は、拡張機能がロードされたのか、ロードできなかったのか、またはスキップされたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="7af0d-107">The package status indicates whether the extension was loaded, could not be loaded, or was skipped.</span></span>

## <a name="extension-package-status"></a><span data-ttu-id="7af0d-108">拡張パッケージの状態</span><span class="sxs-lookup"><span data-stu-id="7af0d-108">Extension package status</span></span>

<span data-ttu-id="7af0d-109">このセクションでは各パッケージ状態の意味を説明します。</span><span class="sxs-lookup"><span data-stu-id="7af0d-109">This section describes what each package status means.</span></span>

- <span data-ttu-id="7af0d-110">**読み込み済** – 拡張パッケージが正常に読み込まれました。</span><span class="sxs-lookup"><span data-stu-id="7af0d-110">**Loaded** – The extension package was successfully loaded.</span></span>
- <span data-ttu-id="7af0d-111">**失敗** – 拡張パッケージが正常に読み込まれませんでした。</span><span class="sxs-lookup"><span data-stu-id="7af0d-111">**Failed** – The extension package wasn't successfully loaded.</span></span>
- <span data-ttu-id="7af0d-112">**スキップ** – パッケージはスキップされ、読み込まれませんでした。</span><span class="sxs-lookup"><span data-stu-id="7af0d-112">**Skipped** – The package was skipped and wasn't loaded.</span></span> <span data-ttu-id="7af0d-113">拡張マニフェストでパッケージが **en-fr** など特定のロケールに対して読み込まれ、他のすべてのロケールに対してはスキップするよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-113">In the extension manifest, you can specify that a package should be loaded for a specific locale, such as **en-fr**, but skipped for all the other locales.</span></span>

<span data-ttu-id="7af0d-114">[![POS 設定ビューの拡張パッケージ セクション](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)</span><span class="sxs-lookup"><span data-stu-id="7af0d-114">[![Extension packages section in the POS Settings view](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)</span></span>

> [!NOTE]
> <span data-ttu-id="7af0d-115">クラウド POS は **POS 設定** ページの **情報** セクションの下の Customization.settings ファイルに拡張機能のバージョンを表示せず、Microsoft アプリ パッケージのバージョンのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="7af0d-115">Cloud POS will not display the extension version in the Customization.settings file under the **About** section on the **POS settings** page, it will only show the Microsoft app package version.</span></span> <span data-ttu-id="7af0d-116">拡張機能パッケージのバージョンは **拡張機能の詳細** セクションからのみ表示できます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-116">Extension package versions can only be viewed from the **Extension details** section.</span></span>

## <a name="extension-package-details"></a><span data-ttu-id="7af0d-117">拡張パッケージの詳細</span><span class="sxs-lookup"><span data-stu-id="7af0d-117">Extension package details</span></span>

<span data-ttu-id="7af0d-118">拡張機能のロードで問題が発生した場合、または競合する拡張機能が存在する場合は、それぞれの拡張機能パッケージに提供されている詳細を使用して、どの拡張機能ファイルが問題の原因かを特定できます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-118">If an issue occurs when an extension is loaded, or if there is a conflicting extension, you can use the details that are provided for each extension package to determine which extension file is causing the issue.</span></span> <span data-ttu-id="7af0d-119">この方法により、問題をトラブルシューティングすることができます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-119">In this way, you can troubleshoot the issue.</span></span>

<span data-ttu-id="7af0d-120">拡張パッケージの詳細を表示するには、そのパッケージのタイルで **詳細の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7af0d-120">To view the details of an extension package, select **View details** on the tile for that package.</span></span> <span data-ttu-id="7af0d-121">POS は新しいビューを開き、そこにパッケージの個々の拡張機能すべての詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-121">The POS opens a new view, where you can see the details of all the individual extensions in the package.</span></span> <span data-ttu-id="7af0d-122">任意の拡張機能が正しく読み込まれなかった場合や、スキップされた場合は、その詳細が右側のペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-122">If any extensions weren't successfully loaded or were skipped, the details appear in the right pane.</span></span>

<span data-ttu-id="7af0d-123">**状態** 列はパッケージの各拡張機能の状態を示し、**名前** 列は拡張の種類名を示し、**パス** 列はパッケージの実装ファイルのパスを示します。</span><span class="sxs-lookup"><span data-stu-id="7af0d-123">The **Status** column shows the status of each extension in the package, the **Name** column shows the name of the extension type, and the **Path** column shows the path of the implementation file in the package.</span></span> <span data-ttu-id="7af0d-124">特定の行項目を選択すると、右側のウィンドウにも拡張機能の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="7af0d-124">When you select a specific line item, the right pane also shows a description of the extension.</span></span>

<span data-ttu-id="7af0d-125">このビューの情報は拡張パッケージに含まれるマニフェスト ファイルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="7af0d-125">The information in this view is based on the manifest file that is included in the extension package.</span></span> <span data-ttu-id="7af0d-126">POS 拡張ローダーはすべての拡張パッケージを読み込んで状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="7af0d-126">The POS extension loader loads all the extension packages and updates the status.</span></span> <span data-ttu-id="7af0d-127">状態の情報には記録されたエラーがすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="7af0d-127">The status information includes any errors that have been logged.</span></span>
