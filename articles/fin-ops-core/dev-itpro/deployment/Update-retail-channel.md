---
title: クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能の適用
description: このトピックでは、クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 09/03/2019
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
ms.openlocfilehash: 9ca7a814982aaac462a298082b2ca04cec65a0a9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183409"
---
# <a name="apply-updates-and-extensions-to-cloud-hosted-retail-channel-components"></a><span data-ttu-id="0c0c1-103">クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能の適用</span><span class="sxs-lookup"><span data-stu-id="0c0c1-103">Apply updates and extensions to cloud hosted Retail channel components</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0c0c1-104">アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、クラウドで Retail チャンル コンポーネントの短縮ダウンタイム更新を有効にした場合は、Retail チャネル コンポーネントも更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-104">If you are updating a Tier-2 sandbox or production environment on application version 8.1.2 or newer and have enabled reduced downtime updates for Retail channel components in the cloud, you will also need to update Retail channel components.</span></span> <span data-ttu-id="0c0c1-105">このトピックでは、クラウドでホストされている Retail チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-105">This topic shows how to apply updates and extensions to cloud-hosted Retail channel components.</span></span>

<span data-ttu-id="0c0c1-106">Retail チャネル コンポーネントの更新は累積的です。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-106">Updates to Retail channel components are cumulative.</span></span> <span data-ttu-id="0c0c1-107">つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-107">This means that any update that you apply will include all previously released changes.</span></span> <span data-ttu-id="0c0c1-108">Retail の配置可能パッケージを適用することも累積的なプロセスであり、拡張機能の以前に配置されたバージョンが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-108">Applying a Retail deployable package is also a cumulative process and will replace the previously deployed version of the extension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0c0c1-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="0c0c1-109">Prerequisites</span></span>

<span data-ttu-id="0c0c1-110">続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-110">Before you proceed, you must first apply updates and extensions (if applicable) to the environment.</span></span> <span data-ttu-id="0c0c1-111">詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-111">For more information, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

<span data-ttu-id="0c0c1-112">クラウドでホストされている Retail チャネル コンポーネントを更新するには、以下を行います。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-112">To update cloud-hosted Retail channel components, do the following:</span></span>

1. <span data-ttu-id="0c0c1-113">**環境の詳細** ページで、**環境機能 > Retail** に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-113">On the **Environment details** page, go to **Environment features > Retail**.</span></span>
2. <span data-ttu-id="0c0c1-114">**Retail 配置設定** ページで、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-114">On the **Retail deployment setup** page, select **Update**.</span></span>
3. <span data-ttu-id="0c0c1-115">選択パネルで、更新先のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-115">In the selection panel, select the version to update to.</span></span>
4. <span data-ttu-id="0c0c1-116">同時に、拡張機能を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-116">You can also choose to apply an extension at the same time.</span></span> 

<span data-ttu-id="0c0c1-117">クラウドでホストされている Retail チャネルに拡張機能を適用するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-117">To apply an extension to a cloud-hosted Retail channel, do the following:</span></span>

1. <span data-ttu-id="0c0c1-118">**Retail 配置設定** ページで、**拡張機能の適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-118">On the **Retail deployment setup** page, select **Apply Extension**.</span></span>
2. <span data-ttu-id="0c0c1-119">選択パネルで、適用する拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-119">In the selection panel, select the extension to apply.</span></span>

> [!NOTE]
> <span data-ttu-id="0c0c1-120">LCS の **Retail の配置設定ページ** で配置を選択する前に、まず、Lifecycle Services (LCS) で Retail の配置可能なパッケージをプロジェクト資産ライブラリにアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-120">You must first upload the Retail deployable package to the project asset library in Lifecycle Services (LCS), before you can select to deploy it on the **Retail deployment setup page** in LCS.</span></span>

<span data-ttu-id="0c0c1-121">更新適用と拡張機能適用の両方の操作には、最大 1 時間のダウンタイムが必要です。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-121">Both Apply updates and Apply extension operations will involve a downtime of up to 1 hour.</span></span> <span data-ttu-id="0c0c1-122">この時間中、次のことが発生します。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-122">During this time, the following will occur:</span></span>

- <span data-ttu-id="0c0c1-123">クラウドでホストされている Retail チャンネルは機能しません (POS オフライン機能が有効な場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-123">Cloud-hosted Retail channels will not function (unless POS offline capability is enabled).</span></span>
- <span data-ttu-id="0c0c1-124">オフライン機能が有効になっている POS デバイスの機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-124">POS devices that have the offline capability feature enabled will have reduced functionality.</span></span>
- <span data-ttu-id="0c0c1-125">Retail サーバーに依存しているすべての電子商取引クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-125">Any e-Commerce clients that are dependent on Retail Server will be disrupted.</span></span>
- <span data-ttu-id="0c0c1-126">Retail Store Scale Unit でホストされているチャネルも影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-126">Channels hosted on Retail Store Scale Units will remain unaffected.</span></span>
- <span data-ttu-id="0c0c1-127">本社機能も影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-127">Head office functionality will remain unaffected.</span></span>

> [!NOTE]
> <span data-ttu-id="0c0c1-128">拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。</span><span class="sxs-lookup"><span data-stu-id="0c0c1-128">Applying an extension and an update at the same time requires a single downtime, and can be an effective way of averting multiple downtimes.</span></span>
