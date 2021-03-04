---
title: 構成マネージャーを使用して構成をコピーする
description: 構成マネージャー (ベータ) 機能を使用すると、Microsoft Dynamics AX 2012 R3 の 1 つのインスタンスから他のインスタンスに構成をコピーすることができます。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 15541
ms.assetid: 54283db7-6f1a-46e8-b74d-c67d54e6e5fb
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 5e99a08413462b3c2459d0be685e4c180ee42bd7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128865"
---
# <a name="copy-configurations-by-using-configuration-manager"></a><span data-ttu-id="ac229-103">構成マネージャーを使用して構成をコピーする</span><span class="sxs-lookup"><span data-stu-id="ac229-103">Copy configurations by using Configuration manager</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac229-104">開始する前に、構成マネージャー (ベータ) を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac229-104">Before you begin, you must set up Configuration manager (beta).</span></span> <span data-ttu-id="ac229-105">詳細については、 [構成マネージャーの設定](set-up-configuration-manager-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac229-105">For more information, see [Set up Configuration manager](set-up-configuration-manager-lcs.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac229-106">この機能は、運用上の用途ではサポートされて **いません**。</span><span class="sxs-lookup"><span data-stu-id="ac229-106">This feature is **not** supported for production use.</span></span> <span data-ttu-id="ac229-107">構成マネージャー (ベータ) は、環境内のデータのインポート/エクスポート フレームワークからのエンティティに依存します。</span><span class="sxs-lookup"><span data-stu-id="ac229-107">Configuration manager (beta) relies on entities from the Data Import Export Framework in your environment.</span></span> <span data-ttu-id="ac229-108">これらのエンティティには現在 AX 2012 R3 のすべての機能が含まれていないため、一部の構成データは環境間でコピーされません。</span><span class="sxs-lookup"><span data-stu-id="ac229-108">Because these entities do not currently include all the functionality in AX 2012 R3, some configuration data is not copied between environments.</span></span>


## <a name="export-a-configuration"></a><span data-ttu-id="ac229-109">コンフィギュレーションのエクスポート</span><span class="sxs-lookup"><span data-stu-id="ac229-109">Export a configuration</span></span>
<span data-ttu-id="ac229-110">特定の法人およびエンティティからエクスポートすることにより、保存済みの構成を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ac229-110">You can create a stored configuration by exporting it from a specified legal entity and entities.</span></span>
1.  <span data-ttu-id="ac229-111">**エクスポートするコンフィギュレーション** リストで、プラス記号 (+) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-111">In the **Configurations to export** list, click the plus sign (+).</span></span>
2.  <span data-ttu-id="ac229-112">コンフィギュレーション名を入力し、**開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-112">Enter a name for the configuration, and then click **Start**.</span></span>
3.  <span data-ttu-id="ac229-113">保管場所を選択し、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-113">Select a storage location, and then click **Continue**.</span></span> <span data-ttu-id="ac229-114">ローカル、クラウド内、または両方の場所に、構成を保管することができます。</span><span class="sxs-lookup"><span data-stu-id="ac229-114">You can store your configuration locally, in the cloud, or in both locations.</span></span>
4.  <span data-ttu-id="ac229-115">接続先の環境を選択し、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-115">Select an environment to connect to, and then click **Continue**.</span></span>
5.  <span data-ttu-id="ac229-116">環境内のパーティションで使用できる法人を確認します。</span><span class="sxs-lookup"><span data-stu-id="ac229-116">Review the legal entities that are available in the partitions in your environment.</span></span> <span data-ttu-id="ac229-117">処理する法人を選択し、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-117">Select the legal entities to work with, and then click **Continue**.</span></span>
6.  <span data-ttu-id="ac229-118">保存されているコンフィギュレーションにコピーするエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="ac229-118">Select the entities to copy to a stored configuration.</span></span>
7.  <span data-ttu-id="ac229-119">オプション: コンフィギュレーション データが含まれるがエンティティにはないテーブルは、保存されているコンフィギュレーションにコピーできません。</span><span class="sxs-lookup"><span data-stu-id="ac229-119">Optional: Tables that contain configuration data but are not in entities can't be copied to a stored configuration.</span></span> <span data-ttu-id="ac229-120">これらのテーブルを表示するには、**見つからないテーブル** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-120">To see these tables, click the **Missing tables** tab.</span></span>
8.  <span data-ttu-id="ac229-121">保存された構成を作成するには、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-121">Click **Continue** to create your stored configuration.</span></span> <span data-ttu-id="ac229-122">コンフィギュレーションが作成された後、その内容を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="ac229-122">After a configuration has been created, you can review what it contains.</span></span>

## <a name="import-a-configuration"></a><span data-ttu-id="ac229-123">コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="ac229-123">Import a configuration</span></span>
1.  <span data-ttu-id="ac229-124">**インポートするコンフィギュレーション** リストで、既存のコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ac229-124">In the **Configurations to import** list, select an existing configuration.</span></span>
2.  <span data-ttu-id="ac229-125">既定の名前を使用するか、新しい名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac229-125">Use the default name, or enter a new name.</span></span> <span data-ttu-id="ac229-126">コンフィギュレーションは、ローカルおよびクラウドの両方に格納されている場合、保存されているコンフィギュレーションのインポート元を選択できます。</span><span class="sxs-lookup"><span data-stu-id="ac229-126">If the configuration was stored both locally and in the cloud, you can select which location to import the stored configuration from.</span></span> <span data-ttu-id="ac229-127">**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-127">Click **Continue**.</span></span>
3.  <span data-ttu-id="ac229-128">コンフィギュレーションをインポートする環境を選択し、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-128">Select the environment to import the configuration to, and then click **Continue**.</span></span>
4.  <span data-ttu-id="ac229-129">環境内のパーティションで使用できる会社を確認します。</span><span class="sxs-lookup"><span data-stu-id="ac229-129">Review the companies that are available in the partitions in your environment.</span></span> <span data-ttu-id="ac229-130">インポート元の会社の場所 (たとえば、initialDAT) を選択することによってと連携する会社を選択し、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-130">Select the companies to work with by selecting the location of the company that you are importing from (for example, initialDAT), and then click **Continue**.</span></span>
5.  <span data-ttu-id="ac229-131">保存されているコンフィギュレーションにコピーするエンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="ac229-131">Select the entities to copy to a stored configuration.</span></span>
6.  <span data-ttu-id="ac229-132">保存された構成をインポートするには、**続行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac229-132">Click **Continue** to import your stored configuration.</span></span> <span data-ttu-id="ac229-133">コンフィギュレーションが作成された後、その内容を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="ac229-133">After a configuration has been created, you can review what it contains.</span></span>


