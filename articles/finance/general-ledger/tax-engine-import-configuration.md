---
title: 税エンジン インポート コンフィギュレーション
description: このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。
author: yijialuan
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, GTE
audience: IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 31e5b9e6c142d6ba04485e69ff23c912b242fdcc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408685"
---
# <a name="tax-engine-import-configuration"></a><span data-ttu-id="c32d6-103">税エンジン インポート コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c32d6-103">Tax engine import configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c32d6-104">このトピックでは、輸入税エンジンのコンフィギュレーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-104">This topic provides information about import tax engine configuration.</span></span>

### <a name="create-a-lifecycle-services-lcs-configuration-repository"></a><span data-ttu-id="c32d6-105">Lifecycle Services (LCS) のコンフィギュレーション リポジトリの作成</span><span class="sxs-lookup"><span data-stu-id="c32d6-105">Create a Lifecycle Services (LCS) configuration repository</span></span>
1. <span data-ttu-id="c32d6-106">**組織管理** > **ワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-106">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="c32d6-107">**コンフィギュレーション プロバイダー** セクションで、**Microsoft** プロバイダー タイルの **リポジトリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c32d6-107">In the **Configuration providers** section, click **Repositories** on the **Microsoft** provider tile.</span></span>

![コンフィギュレーションの読み込み](media/gte-extension-repositories.png)

3. <span data-ttu-id="c32d6-109">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c32d6-109">Click **Add**.</span></span> 
4. <span data-ttu-id="c32d6-110">**LCS** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-110">Select the **LCS** option.</span></span> 
5. <span data-ttu-id="c32d6-111">**リポジトリの作成** をクリックして、LCS コンフィギュレーション リポジトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-111">Click **Create repository** to create an LCS configuration repository.</span></span>
6. <span data-ttu-id="c32d6-112">リポジトリの名前と説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c32d6-112">Enter a name and description for the repository and then click **OK**.</span></span>

### <a name="import-configurations-from-lcs"></a><span data-ttu-id="c32d6-113">LCS からコンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="c32d6-113">Import configurations from LCS</span></span>
1. <span data-ttu-id="c32d6-114">**組織管理** > **ワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-114">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="c32d6-115">**コンフィギュレーション プロバイダー** セクションで、**Microsoft** プロバイダー タイルの **リポジトリ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c32d6-115">In the **Configuration providers** section, click **Repositories** on the **Microsoft** provider tile.</span></span>
3. <span data-ttu-id="c32d6-116">作成したコンフィギュレーション リポジトリを選択します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-116">Select the configuration repository that you just created.</span></span> 
4. <span data-ttu-id="c32d6-117">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c32d6-117">Click **Open**.</span></span>
5. <span data-ttu-id="c32d6-118">ツリーで、最新の税務書類を選択します (たとえば、**税 (インド GST)** を選択)。</span><span class="sxs-lookup"><span data-stu-id="c32d6-118">In the tree, select the latest tax document (for example, select **Tax (India GST)**).</span></span>
6. <span data-ttu-id="c32d6-119">**バージョン** セクションで、**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c32d6-119">In the **Versions** section, click **Import**.</span></span>

![コンフィギュレーションの読み込み](media/gte-extension-import-configurations.png)

7. <span data-ttu-id="c32d6-121">**はい** をクリックして、インポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="c32d6-121">Click **Yes** to confirm the import.</span></span>
