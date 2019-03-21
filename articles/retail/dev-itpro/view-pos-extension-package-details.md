---
title: POS 拡張パッケージ情報の表示
description: このトピックでは、販売時点管理 (POS) の設定ビューの拡張パッケージ セクションに関する情報を提供します。 この新しいセクションは、コア POS の一部として含まれる拡張パッケージを一覧表示するとともに、ステータス情報やその他の詳細を表示できます。
author: mumani
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-02-25
ms.dyn365.ops.version: AX 10.0.1
ms.openlocfilehash: 8e13b1415f66be999e90fe94acdaae57b07dc112
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2019
ms.locfileid: "790317"
---
# <a name="view-pos-extension-package-information"></a><span data-ttu-id="efbbe-104">POS 拡張パッケージ情報の表示</span><span class="sxs-lookup"><span data-stu-id="efbbe-104">View POS extension package information</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="efbbe-105">このトピックは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0.1 以降、および Microsoft Dynamics 365 for Retail バージョン 10.0.1 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-105">This topic applies to Microsoft Dynamics 365 for Finance and Operations version 10.0.1 or later, and Microsoft Dynamics 365 for Retail version 10.0.1 or later.</span></span>

<span data-ttu-id="efbbe-106">販売時点管理 (POS) の **設定** ビューでは、**拡張パッケージ** セクションにコア POS の一部として含まれている POS 拡張パッケージのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-106">In the **Settings** view in the point of sale (POS), the **Extension packages** section shows the list of POS extension packages that are included as part of the core POS.</span></span> <span data-ttu-id="efbbe-107">各パッケージのタイルには、そのパッケージの状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-107">The tile for each package shows the status of that package.</span></span> <span data-ttu-id="efbbe-108">パッケージの状態は、拡張機能がロードされたのか、ロードできなかったのか、またはスキップされたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="efbbe-108">The package status indicates whether the extension was loaded, could not be loaded, or was skipped.</span></span>

## <a name="extension-package-status"></a><span data-ttu-id="efbbe-109">拡張パッケージの状態</span><span class="sxs-lookup"><span data-stu-id="efbbe-109">Extension package status</span></span>

<span data-ttu-id="efbbe-110">このセクションでは各パッケージ状態の意味を説明します。</span><span class="sxs-lookup"><span data-stu-id="efbbe-110">This section describes what each package status means.</span></span>

- <span data-ttu-id="efbbe-111">**読み込み済** – 拡張パッケージが正常に読み込まれました。</span><span class="sxs-lookup"><span data-stu-id="efbbe-111">**Loaded** – The extension package was successfully loaded.</span></span>
- <span data-ttu-id="efbbe-112">**失敗** – 拡張パッケージが正常に読み込まれませんでした。</span><span class="sxs-lookup"><span data-stu-id="efbbe-112">**Failed** – The extension package wasn't successfully loaded.</span></span>
- <span data-ttu-id="efbbe-113">**スキップ** – パッケージはスキップされ、読み込まれませんでした。</span><span class="sxs-lookup"><span data-stu-id="efbbe-113">**Skipped** – The package was skipped and wasn't loaded.</span></span> <span data-ttu-id="efbbe-114">拡張マニフェストでパッケージが **en-fr** など特定のロケールに対して読み込まれ、他のすべてのロケールに対してはスキップするよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-114">In the extension manifest, you can specify that a package should be loaded for a specific locale, such as **en-fr**, but skipped for all the other locales.</span></span>

<span data-ttu-id="efbbe-115">[![POS 設定ビューの拡張パッケージ セクション](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)</span><span class="sxs-lookup"><span data-stu-id="efbbe-115">[![Extension packages section in the POS Settings view](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)</span></span>

## <a name="extension-package-details"></a><span data-ttu-id="efbbe-116">拡張パッケージの詳細</span><span class="sxs-lookup"><span data-stu-id="efbbe-116">Extension package details</span></span>

<span data-ttu-id="efbbe-117">拡張機能のロードで問題が発生した場合、または競合する拡張機能が存在する場合は、それぞれの拡張機能パッケージに提供されている詳細を使用して、どの拡張機能ファイルが問題の原因かを特定できます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-117">If an issue occurs when an extension is loaded, or if there is a conflicting extension, you can use the details that are provided for each extension package to determine which extension file is causing the issue.</span></span> <span data-ttu-id="efbbe-118">この方法により、問題をトラブルシューティングすることができます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-118">In this way, you can troubleshoot the issue.</span></span>

<span data-ttu-id="efbbe-119">拡張パッケージの詳細を表示するには、そのパッケージのタイルで **詳細の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="efbbe-119">To view the details of an extension package, select **View details** on the tile for that package.</span></span> <span data-ttu-id="efbbe-120">POS は新しいビューを開き、そこにパッケージの個々の拡張機能すべての詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-120">The POS opens a new view, where you can see the details of all the individual extensions in the package.</span></span> <span data-ttu-id="efbbe-121">任意の拡張機能が正しく読み込まれなかった場合や、スキップされた場合は、その詳細が右側のペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-121">If any extensions weren't successfully loaded or were skipped, the details appear in the right pane.</span></span>

<span data-ttu-id="efbbe-122">**状態** 列はパッケージの各拡張機能の状態を示し、**名前** 列は拡張の種類名を示し、**パス** 列はパッケージの実装ファイルのパスを示します。</span><span class="sxs-lookup"><span data-stu-id="efbbe-122">The **Status** column shows the status of each extension in the package, the **Name** column shows the name of the extension type, and the **Path** column shows the path of the implementation file in the package.</span></span> <span data-ttu-id="efbbe-123">特定の行項目を選択すると、右側のウィンドウにも拡張機能の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="efbbe-123">When you select a specific line item, the right pane also shows a description of the extension.</span></span>

<span data-ttu-id="efbbe-124">このビューの情報は拡張パッケージに含まれるマニフェスト ファイルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="efbbe-124">The information in this view is based on the manifest file that is included in the extension package.</span></span> <span data-ttu-id="efbbe-125">POS 拡張ローダーはすべての拡張パッケージを読み込んで状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="efbbe-125">The POS extension loader loads all the extension packages and updates the status.</span></span> <span data-ttu-id="efbbe-126">状態の情報には記録されたエラーがすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="efbbe-126">The status information includes any errors that have been logged.</span></span>
