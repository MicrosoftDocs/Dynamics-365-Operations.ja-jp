---
title: Retail Cloud Scale Unit への更新プログラムと拡張機能の適用
description: このトピックでは、クラウドでホストされているコマース チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 04/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7a48b5296318ee957fb7a9a398754cb803cda48b
ms.sourcegitcommit: 4254acb3cf8c6299fc2f3818ea6c499f058320d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/09/2020
ms.locfileid: "3254737"
---
# <a name="apply-updates-and-extensions-to-retail-cloud-scale-unit"></a><span data-ttu-id="a3132-103">Retail Cloud Scale Unit への更新プログラムと拡張機能の適用</span><span class="sxs-lookup"><span data-stu-id="a3132-103">Apply updates and extensions to Retail Cloud Scale Unit</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a3132-104">アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、Commerce Scale Unit を初期化した場合は、チャネル コンポーネントも更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3132-104">If you are updating a Tier-2 sandbox or production environment on application version 8.1.2 or newer and have initialized Commerce Scale Unit, you will also need to update channel components.</span></span> <span data-ttu-id="a3132-105">このトピックでは、Commerce Scale Unit に更新と拡張を適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a3132-105">This topic shows how to apply updates and extensions to Commerce Scale Unit.</span></span>

<span data-ttu-id="a3132-106">Commerce Scale Unit の更新プログラムは累積的なものです。</span><span class="sxs-lookup"><span data-stu-id="a3132-106">Updates to Commerce Scale Unit are cumulative.</span></span> <span data-ttu-id="a3132-107">つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3132-107">This means that any update that you apply will include all previously released changes.</span></span> <span data-ttu-id="a3132-108">配置可能なコマースの拡張用パッケージを適用することも累積的なプロセスであり、以前に配置された拡張機能のバージョンが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a3132-108">Applying a Commerce deployable package for extensions is also a cumulative process and will replace the previously deployed version of the extension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a3132-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="a3132-109">Prerequisites</span></span>

<span data-ttu-id="a3132-110">続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a3132-110">Before you proceed, you must first apply updates and extensions (if applicable) to the environment.</span></span> <span data-ttu-id="a3132-111">詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3132-111">For more information, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

<span data-ttu-id="a3132-112">Commerce Scale Unit を更新するには、それぞれについて次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a3132-112">To update Commerce Scale Unit, run the following steps for each:</span></span>

1. <span data-ttu-id="a3132-113">**環境の詳細**ページで、**環境機能 > Retail およびコマース**に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3132-113">On the **Environment details** page, go to **Environment features > Retail and Commerce**.</span></span>
2. <span data-ttu-id="a3132-114">**コマース配置設定**ページで、**更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3132-114">On the **Commerce deployment setup** page, select **Update**.</span></span>
3. <span data-ttu-id="a3132-115">選択パネルで、更新先のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a3132-115">In the selection panel, select the version to update to.</span></span>
4. <span data-ttu-id="a3132-116">最新のサービス更新プログラムを適用して最新の機能にアクセスすることも、最新の品質更新プログラムに更新して、現在展開されているサービス更新プログラムの品質改善を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a3132-116">You can choose to update to the newest service update to access the latest features, or you can update to the latest quality update to apply quality improvements for the currently deployed service update.</span></span> <span data-ttu-id="a3132-117">詳細については、[Lifecycle Services (LCS) から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3132-117">For more information, see [Download updates from Lifecycle Services (LCS)](../migration-upgrade/download-hotfix-lcs.md).</span></span>
5. <span data-ttu-id="a3132-118">また、同時に拡張機能を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a3132-118">You can choose to apply an extension at the same time.</span></span> 

<span data-ttu-id="a3132-119">Commerce Scale Unit に拡張機能を適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a3132-119">To apply an extension to a Commerce Scale Unit, run the following steps:</span></span>

1. <span data-ttu-id="a3132-120">**コマース配置設定**ページで、**拡張機能の適用**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3132-120">On the **Commerce deployment setup** page, select **Apply Extension**.</span></span>
2. <span data-ttu-id="a3132-121">選択パネルで、適用する拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3132-121">In the selection panel, select the extension to apply.</span></span>

> [!NOTE]
> <span data-ttu-id="a3132-122">まず、Lifecycle Services (LCS) で Commerce の配置可能なパッケージをプロジェクト資産ライブラリにアップロードしてください。すると、LCS の **Commerce の配置設定ページ**でパッケージの配置を選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a3132-122">You must first upload the Commerce deployable package to the project asset library in Lifecycle Services (LCS), before you can select to deploy it on the **Commerce deployment setup page** in LCS.</span></span>

<span data-ttu-id="a3132-123">**更新の適用**と**拡張機能の適用**の両方の操作には、最大 1 時間のダウンタイムが必要です。</span><span class="sxs-lookup"><span data-stu-id="a3132-123">Both **Apply updates** and **Apply extension** operations will involve a downtime of up to 1 hour.</span></span> <span data-ttu-id="a3132-124">この時間中、次のことが発生します。</span><span class="sxs-lookup"><span data-stu-id="a3132-124">During this time, the following will occur:</span></span>

- <span data-ttu-id="a3132-125">クラウドでホストされている Commerce チャネルは機能しません (POS オフライン機能が有効な場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="a3132-125">Cloud-hosted Commerce channels will not function (unless POS offline capability is enabled).</span></span>
- <span data-ttu-id="a3132-126">オフライン機能が有効になっている POS デバイスの機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="a3132-126">POS devices that have the offline capability feature enabled will have reduced functionality.</span></span>
- <span data-ttu-id="a3132-127">Commerce Scale Unit に依存しているすべてのE コマース クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="a3132-127">Any e-Commerce clients that are dependent on Commerce Scale Unit will be disrupted.</span></span>
- <span data-ttu-id="a3132-128">Commerce Scale Units でホストされているチャネルは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="a3132-128">Channels hosted on Commerce Scale Units will remain unaffected.</span></span>
- <span data-ttu-id="a3132-129">本社機能も影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="a3132-129">Head office functionality will remain unaffected.</span></span>

> [!NOTE]
> <span data-ttu-id="a3132-130">拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。</span><span class="sxs-lookup"><span data-stu-id="a3132-130">Applying an extension and an update at the same time requires a single downtime, and can be an effective way of averting multiple downtimes.</span></span>

## <a name="view-history"></a><span data-ttu-id="a3132-131">履歴の表示</span><span class="sxs-lookup"><span data-stu-id="a3132-131">View history</span></span>
<span data-ttu-id="a3132-132">最新の操作履歴をスケールユニットで表示するには、**アクション** タブの **履歴** を選択し、**スケール ユニットの履歴**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a3132-132">To view the history of recent operations on a Scale Unit, select **History** on the **Action** tab to open the **Scale Unit History** page.</span></span> <span data-ttu-id="a3132-133">このページでは、初期化、サービス更新、品質更新、バージョン、拡張機能の詳細、その他の関連情報など、最近の操作を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a3132-133">On this page, you can view recent operations such as initialize, service update, quality update, version, extension details, and other relevant information.</span></span>

