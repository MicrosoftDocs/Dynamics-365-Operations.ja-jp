---
title: POS 拡張パッケージ情報の表示
description: このトピックでは、販売時点管理 (POS) の設定ビューの拡張パッケージ セクションに関する情報を提供します。
author: mugunthanm
ms.date: 04/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-02-25
ms.dyn365.ops.version: AX 10.0.1
ms.openlocfilehash: aaa3e9e4f9bd2ad030a247154e9a4631c83c4099
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792909"
---
# <a name="view-pos-extension-package-information"></a><span data-ttu-id="88eaf-103">POS 拡張パッケージ情報の表示</span><span class="sxs-lookup"><span data-stu-id="88eaf-103">View POS extension package information</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88eaf-104">販売時点管理 (POS) の **設定** ビューでは、**拡張パッケージ** セクションにコア POS の一部として含まれている POS 拡張パッケージのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-104">In the **Settings** view in the point of sale (POS), the **Extension packages** section shows the list of POS extension packages that are included as part of the core POS.</span></span> <span data-ttu-id="88eaf-105">各パッケージのタイルには、そのパッケージの状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-105">The tile for each package shows the status of that package.</span></span> <span data-ttu-id="88eaf-106">パッケージの状態は、拡張機能がロードされたのか、ロードできなかったのか、またはスキップされたのかを示します。</span><span class="sxs-lookup"><span data-stu-id="88eaf-106">The package status indicates whether the extension was loaded, could not be loaded, or was skipped.</span></span>

## <a name="extension-package-status"></a><span data-ttu-id="88eaf-107">拡張パッケージの状態</span><span class="sxs-lookup"><span data-stu-id="88eaf-107">Extension package status</span></span>

<span data-ttu-id="88eaf-108">このセクションでは各パッケージ状態の意味を説明します。</span><span class="sxs-lookup"><span data-stu-id="88eaf-108">This section describes what each package status means.</span></span>

- <span data-ttu-id="88eaf-109">**読み込み済** – 拡張パッケージが正常に読み込まれました。</span><span class="sxs-lookup"><span data-stu-id="88eaf-109">**Loaded** – The extension package was successfully loaded.</span></span>
- <span data-ttu-id="88eaf-110">**失敗** – 拡張パッケージが正常に読み込まれませんでした。</span><span class="sxs-lookup"><span data-stu-id="88eaf-110">**Failed** – The extension package wasn't successfully loaded.</span></span>
- <span data-ttu-id="88eaf-111">**スキップ** – パッケージはスキップされ、読み込まれませんでした。</span><span class="sxs-lookup"><span data-stu-id="88eaf-111">**Skipped** – The package was skipped and wasn't loaded.</span></span> <span data-ttu-id="88eaf-112">拡張マニフェストでパッケージが **en-fr** など特定のロケールに対して読み込まれ、他のすべてのロケールに対してはスキップするよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-112">In the extension manifest, you can specify that a package should be loaded for a specific locale, such as **en-fr**, but skipped for all the other locales.</span></span>

<span data-ttu-id="88eaf-113">[![POS 設定ビューの拡張パッケージ セクション](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)</span><span class="sxs-lookup"><span data-stu-id="88eaf-113">[![Extension packages section in the POS Settings view](./media/ExtensionPackage.png)](./media/ExtensionPackage.png)</span></span>

> [!NOTE]
> <span data-ttu-id="88eaf-114">クラウド POS は **POS 設定** ページの **情報** セクションの下の Customization.settings ファイルに拡張機能のバージョンを表示せず、Microsoft アプリ パッケージのバージョンのみを表示します。</span><span class="sxs-lookup"><span data-stu-id="88eaf-114">Cloud POS will not display the extension version in the Customization.settings file under the **About** section on the **POS settings** page, it will only show the Microsoft app package version.</span></span> <span data-ttu-id="88eaf-115">拡張機能パッケージのバージョンは **拡張機能の詳細** セクションからのみ表示できます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-115">Extension package versions can only be viewed from the **Extension details** section.</span></span>

## <a name="extension-package-details"></a><span data-ttu-id="88eaf-116">拡張パッケージの詳細</span><span class="sxs-lookup"><span data-stu-id="88eaf-116">Extension package details</span></span>

<span data-ttu-id="88eaf-117">拡張機能のロードで問題が発生した場合、または競合する拡張機能が存在する場合は、それぞれの拡張機能パッケージに提供されている詳細を使用して、どの拡張機能ファイルが問題の原因かを特定できます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-117">If an issue occurs when an extension is loaded, or if there is a conflicting extension, you can use the details that are provided for each extension package to determine which extension file is causing the issue.</span></span> <span data-ttu-id="88eaf-118">この方法により、問題をトラブルシューティングすることができます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-118">In this way, you can troubleshoot the issue.</span></span>

<span data-ttu-id="88eaf-119">拡張パッケージの詳細を表示するには、そのパッケージのタイルで **詳細の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88eaf-119">To view the details of an extension package, select **View details** on the tile for that package.</span></span> <span data-ttu-id="88eaf-120">POS は新しいビューを開き、そこにパッケージの個々の拡張機能すべての詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-120">The POS opens a new view, where you can see the details of all the individual extensions in the package.</span></span> <span data-ttu-id="88eaf-121">任意の拡張機能が正しく読み込まれなかった場合や、スキップされた場合は、その詳細が右側のペインに表示されます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-121">If any extensions weren't successfully loaded or were skipped, the details appear in the right pane.</span></span>

<span data-ttu-id="88eaf-122">**状態** 列はパッケージの各拡張機能の状態を示し、**名前** 列は拡張の種類名を示し、**パス** 列はパッケージの実装ファイルのパスを示します。</span><span class="sxs-lookup"><span data-stu-id="88eaf-122">The **Status** column shows the status of each extension in the package, the **Name** column shows the name of the extension type, and the **Path** column shows the path of the implementation file in the package.</span></span> <span data-ttu-id="88eaf-123">特定の行項目を選択すると、右側のウィンドウにも拡張機能の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88eaf-123">When you select a specific line item, the right pane also shows a description of the extension.</span></span>

<span data-ttu-id="88eaf-124">このビューの情報は拡張パッケージに含まれるマニフェスト ファイルに基づいています。</span><span class="sxs-lookup"><span data-stu-id="88eaf-124">The information in this view is based on the manifest file that is included in the extension package.</span></span> <span data-ttu-id="88eaf-125">POS 拡張ローダーはすべての拡張パッケージを読み込んで状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="88eaf-125">The POS extension loader loads all the extension packages and updates the status.</span></span> <span data-ttu-id="88eaf-126">状態の情報には記録されたエラーがすべて含まれています。</span><span class="sxs-lookup"><span data-stu-id="88eaf-126">The status information includes any errors that have been logged.</span></span>

> [!NOTE]
> <span data-ttu-id="88eaf-127">デュアル ディスプレイ カスタム コントロールとデュアル ディスプレイに関連するその他の拡張機能の詳細情報は、拡張機能の詳細ビューには表示されません。</span><span class="sxs-lookup"><span data-stu-id="88eaf-127">Dual display custom control and other extension details information related to dual display will not be shown in the extension details view.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]