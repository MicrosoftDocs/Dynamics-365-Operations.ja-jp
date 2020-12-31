---
title: Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用
description: このトピックでは、クラウドでホストされているコマース チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 0e5f6e738cf0d4b051405053bed0069d6ffd2103
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681074"
---
# <a name="apply-updates-and-extensions-to-commerce-scale-unit-cloud"></a><span data-ttu-id="8d9b6-103">Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用</span><span class="sxs-lookup"><span data-stu-id="8d9b6-103">Apply updates and extensions to Commerce Scale Unit (cloud)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8d9b6-104">アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、Commerce Scale Unit を初期化した場合は、チャネル コンポーネントも更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-104">If you are updating a Tier-2 sandbox or production environment on application version 8.1.2 or newer and have initialized Commerce Scale Unit, you will also need to update channel components.</span></span> <span data-ttu-id="8d9b6-105">このトピックでは、Commerce Scale Unit に更新と拡張を適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-105">This topic shows how to apply updates and extensions to Commerce Scale Unit.</span></span>

<span data-ttu-id="8d9b6-106">Commerce Scale Unit の更新プログラムは累積的なものです。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-106">Updates to Commerce Scale Unit are cumulative.</span></span> <span data-ttu-id="8d9b6-107">つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-107">This means that any update that you apply will include all previously released changes.</span></span> <span data-ttu-id="8d9b6-108">配置可能なコマースの拡張用パッケージを適用することも累積的なプロセスであり、以前に配置された拡張機能のバージョンが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-108">Applying a Commerce deployable package for extensions is also a cumulative process and will replace the previously deployed version of the extension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d9b6-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="8d9b6-109">Prerequisites</span></span>

<span data-ttu-id="8d9b6-110">続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-110">Before you proceed, you must first apply updates and extensions (if applicable) to the environment.</span></span> <span data-ttu-id="8d9b6-111">詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-111">For more information, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

<span data-ttu-id="8d9b6-112">Commerce Scale Unit を更新するには、それぞれについて次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-112">To update Commerce Scale Unit, run the following steps for each:</span></span>

1. <span data-ttu-id="8d9b6-113">**環境の詳細** ページで、**環境機能 > Retail およびコマース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-113">On the **Environment details** page, go to **Environment features > Retail and Commerce**.</span></span>
2. <span data-ttu-id="8d9b6-114">**コマース配置設定** ページで、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-114">On the **Commerce deployment setup** page, select **Update**.</span></span>
3. <span data-ttu-id="8d9b6-115">選択パネルで、更新先のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-115">In the selection panel, select the version to update to.</span></span>
4. <span data-ttu-id="8d9b6-116">最新のサービス更新プログラムを適用して最新の機能にアクセスすることも、最新の品質更新プログラムに更新して、現在展開されているサービス更新プログラムの品質改善を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-116">You can choose to update to the newest service update to access the latest features, or you can update to the latest quality update to apply quality improvements for the currently deployed service update.</span></span> <span data-ttu-id="8d9b6-117">詳細については、[Lifecycle Services (LCS) から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-117">For more information, see [Download updates from Lifecycle Services (LCS)](../migration-upgrade/download-hotfix-lcs.md).</span></span>
5. <span data-ttu-id="8d9b6-118">また、同時に拡張機能を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-118">You can choose to apply an extension at the same time.</span></span> 

<span data-ttu-id="8d9b6-119">Commerce Scale Unit に拡張機能を適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-119">To apply an extension to a Commerce Scale Unit, run the following steps:</span></span>

1. <span data-ttu-id="8d9b6-120">**コマース配置設定** ページで、**拡張機能の適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-120">On the **Commerce deployment setup** page, select **Apply Extension**.</span></span>
2. <span data-ttu-id="8d9b6-121">選択パネルで、適用する拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-121">In the selection panel, select the extension to apply.</span></span>

> [!NOTE]
> <span data-ttu-id="8d9b6-122">まず、Lifecycle Services (LCS) で Commerce の配置可能なパッケージをプロジェクト資産ライブラリにアップロードしてください。すると、LCS の **Commerce の配置設定ページ** でパッケージの配置を選択できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-122">You must first upload the Commerce deployable package to the project asset library in Lifecycle Services (LCS), before you can select to deploy it on the **Commerce deployment setup page** in LCS.</span></span>

<span data-ttu-id="8d9b6-123">**更新プログラムの適用** および **拡張機能の適用** 操作の両方はダウンタイム (最大 1 時間) を伴い、場合によっては最大 2 時間以上になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-123">Both **Apply updates** and **Apply extension** operations will involve a downtime, which may last up to 1 hour, or in some cases up to 2 hours or more.</span></span> <span data-ttu-id="8d9b6-124">たとえば、Commerce Scale Unit の米国以外の場所を更新する場合、大量のデータ、または複雑なスキーマの更新が行われます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-124">For example, when updating non-US locations of Commerce Scale Unit, large data volumes, or complex schema updates.</span></span> <span data-ttu-id="8d9b6-125">ダウンタイム期間の現実的な予測については、運用環境で使用する予定のものと同等の更新およびデータセットに対するサンドボックス UAT のダウンタイム期間を記録します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-125">For a realistic estimate of the downtime duration, note the downtime duration in Sandbox UAT for an equivalent update and dataset that you plan to use in your production environment.</span></span> <span data-ttu-id="8d9b6-126">この時間中、次のことが発生します。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-126">During this time, the following will occur:</span></span>

- <span data-ttu-id="8d9b6-127">クラウドでホストされている Commerce チャネルは機能しません (POS オフライン機能が有効な場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-127">Cloud-hosted Commerce channels will not function (unless POS offline capability is enabled).</span></span>
- <span data-ttu-id="8d9b6-128">オフライン機能が有効になっている POS デバイスの機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-128">POS devices that have the offline capability feature enabled will have reduced functionality.</span></span>
- <span data-ttu-id="8d9b6-129">Commerce Scale Unit に依存しているすべてのE コマース クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-129">Any e-Commerce clients that are dependent on Commerce Scale Unit will be disrupted.</span></span>
- <span data-ttu-id="8d9b6-130">Commerce Scale Units でホストされているチャネルは影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-130">Channels hosted on Commerce Scale Units will remain unaffected.</span></span>
- <span data-ttu-id="8d9b6-131">本社機能も影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-131">Head office functionality will remain unaffected.</span></span>

> [!NOTE]
> <span data-ttu-id="8d9b6-132">拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-132">Applying an extension and an update at the same time requires a single downtime, and can be an effective way of averting multiple downtimes.</span></span>

## <a name="view-history"></a><span data-ttu-id="8d9b6-133">履歴の表示</span><span class="sxs-lookup"><span data-stu-id="8d9b6-133">View history</span></span>
<span data-ttu-id="8d9b6-134">最新の操作履歴をスケールユニットで表示するには、**アクション** タブの **履歴** を選択し、**スケール ユニットの履歴** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-134">To view the history of recent operations on a Scale Unit, select **History** on the **Action** tab to open the **Scale Unit History** page.</span></span> <span data-ttu-id="8d9b6-135">このページでは、初期化、サービス更新、品質更新、バージョン、拡張機能の詳細、その他の関連情報など、最近の操作を表示できます。</span><span class="sxs-lookup"><span data-stu-id="8d9b6-135">On this page, you can view recent operations such as initialize, service update, quality update, version, extension details, and other relevant information.</span></span>

