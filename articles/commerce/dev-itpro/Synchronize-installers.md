---
title: Dynamics 365 Commerce のセルフサービス インストーラーの同期
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Headquarters でアセット ライブラリと共用資産ライブラリを使用して、セルフサービス インストーラーをアップロードおよび同期し、標準セルフサービス ダウンロード メカニズムで使用できるようにする方法について説明します。
author: jashanno
manager: AnnBe
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.service: Dynamics-365-retail
ms.technology: ''
ms.search.form: SysAADClientTable, RetailTransactionServiceProfile
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail, Core
ms.custom: 44351
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 5e60f6cad72e277d95d89dc53fbc2c6ad9d93e9d
ms.sourcegitcommit: c30a9956d9c29a504856487a3a98090eef9aab2b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2020
ms.locfileid: "3266405"
---
# <a name="synchronize-self-service-installers-in-dynamics-365-commerce"></a><span data-ttu-id="72d89-103">Dynamics 365 Commerce のセルフサービス インストーラーの同期</span><span class="sxs-lookup"><span data-stu-id="72d89-103">Synchronize self-service installers in Dynamics 365 Commerce</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="72d89-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) と Dynamics 365 Headquarters でアセット ライブラリと共有アセット ライブラリを使用して、セルフサービス インストーラーをアップロードおよび同期し、標準セルフサービス ダウンロード メカニズムで使用できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72d89-104">This topic explains how to use the Asset library and Shared asset library in Microsoft Dynamics Lifecycle Services (LCS), and Dynamics 365 Headquarters, to upload and synchronize self-service installers so that they can be used with the standard self-service download mechanism.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72d89-105">セルフサービス パッケージをアップロードする以前の方法は、現在もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="72d89-105">The earlier method of uploading self-service packages is currently still supported.</span></span> <span data-ttu-id="72d89-106">ただし、これは廃止され、今後削除される予定です。</span><span class="sxs-lookup"><span data-stu-id="72d89-106">However, it's obsolete and will be removed in the future.</span></span>

## <a name="key-terms"></a><span data-ttu-id="72d89-107">重要な用語</span><span class="sxs-lookup"><span data-stu-id="72d89-107">Key terms</span></span>

| <span data-ttu-id="72d89-108">期間</span><span class="sxs-lookup"><span data-stu-id="72d89-108">Term</span></span> | <span data-ttu-id="72d89-109">説明</span><span class="sxs-lookup"><span data-stu-id="72d89-109">Description</span></span> |
|---|---|
| <span data-ttu-id="72d89-110">共有アセット ライブラリ</span><span class="sxs-lookup"><span data-stu-id="72d89-110">Shared asset library</span></span> | <span data-ttu-id="72d89-111">LCS では、共有アセット ライブラリとプロジェクト レベルのアセット ライブラリの 2 種類のアセット ライブラリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="72d89-111">In LCS, two types of asset libraries are available: the Shared asset library and the project-level Asset library.</span></span> <span data-ttu-id="72d89-112">これらのライブラリの詳細については、[Lifecycle Services (LCS) のアセット ライブラリ](../../fin-ops-core/dev-itpro/lifecycle-services/asset-library.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72d89-112">For more information about these libraries, see [Asset library in Lifecycle Services (LCS)](../../fin-ops-core/dev-itpro/lifecycle-services/asset-library.md).</span></span> |
| <span data-ttu-id="72d89-113">資産ライブラリ</span><span class="sxs-lookup"><span data-stu-id="72d89-113">Asset library</span></span> | <span data-ttu-id="72d89-114">詳細については、[Lifecycle Services (LCS) のアセット ライブラリ](../../fin-ops-core/dev-itpro/lifecycle-services/asset-library.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72d89-114">For more information, see [Asset library in Lifecycle Services (LCS)](../../fin-ops-core/dev-itpro/lifecycle-services/asset-library.md).</span></span> |
| <span data-ttu-id="72d89-115">セルフ サービス インストーラー</span><span class="sxs-lookup"><span data-stu-id="72d89-115">Self-service installers</span></span> | <span data-ttu-id="72d89-116">セルフサービス インストーラーは Dynamics 365 Commerce コンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="72d89-116">Self-service installers are the Dynamics 365 Commerce components.</span></span> <span data-ttu-id="72d89-117">インストーラーの詳細については、このトピックの最後にあるリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72d89-117">For more information about the installers, see the links at the end of this topic.</span></span> |

## <a name="overview"></a><span data-ttu-id="72d89-118">概要</span><span class="sxs-lookup"><span data-stu-id="72d89-118">Overview</span></span>

<span data-ttu-id="72d89-119">共有アセット ライブラリの **Retail セルフサービス パッケージ** サブセクションには、セルフサービス インストーラーのすべての月次リリースが格納されます。</span><span class="sxs-lookup"><span data-stu-id="72d89-119">The **Retail Self-service package** subsection in the Shared asset library stores all monthly releases for self-service installers.</span></span> <span data-ttu-id="72d89-120">これらのインストーラーには、Modern POS (オフライン バージョンを含む)、Commerce Scale Unit (旧 Retail Store Scale Unit \[RSSU\])、ハードウェア ステーションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="72d89-120">These installers include Modern POS (which includes the offline version), Commerce Scale Unit (which was formerly known as Retail Store Scale Unit \[RSSU\]), and hardware station.</span></span> <span data-ttu-id="72d89-121">また、カスタマイズされたインストーラーを、このライブラリとプロジェクト レベルのアセット ライブラリの両方にアップロードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="72d89-121">You can also upload customized installers into both this library and the project-level Asset library.</span></span> <span data-ttu-id="72d89-122">これらの場所を使用することで、Dynamics 365 Headquarters で 使用可能なインストーラーを同期できます。</span><span class="sxs-lookup"><span data-stu-id="72d89-122">By using these locations, you can then synchronize the available installers in Dynamics 365 Headquarters.</span></span> <span data-ttu-id="72d89-123">同期が完了すると、これら 2 つのライブラリ (および以前に環境に存在していたもの) 間で使用可能なすべてのインストーラーは、個別のトピック (このトピックで前述した用語の表のリンクを参照してください) で詳細に説明されている標準セルフサービス ダウンロード プロセスでアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="72d89-123">After synchronization is completed, all the installers that are available between these two libraries (and whatever previously existed in the environment) will be accessible for the standard self-service download processes that are described in detail in separate topics (see the links in the table of terms earlier in this topic).</span></span>

<span data-ttu-id="72d89-124">次の図は、共有アセット ライブラリ (またはアセット ライブラリ) の **Retail セルフサービス パッケージ** サブセクションの一般的な例を示しています。</span><span class="sxs-lookup"><span data-stu-id="72d89-124">The following illustration shows a generic example of the **Retail Self-service package** subsection in the Shared asset library (or Asset library).</span></span>

![共有アセット ライブラリの Retail セルフサービス パッケージ サブセクション](media/SharedAssets.jpg)

## <a name="synchronize-installers-in-dynamics-365-headquarters"></a><span data-ttu-id="72d89-126">Dynamics 365 Headquarters のインストーラーの同期</span><span class="sxs-lookup"><span data-stu-id="72d89-126">Synchronize installers in Dynamics 365 Headquarters</span></span>

1. <span data-ttu-id="72d89-127">**Retail とコマース** &gt; **バックオフィスの設定** &gt; **パラメーター** &gt; **コマース パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72d89-127">Go to **Retail and Commerce** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Commerce parameters**.</span></span>
2. <span data-ttu-id="72d89-128">**チャンネル配置** タブで **パッケージの更新の確認** を選択して、同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="72d89-128">On the **Channel deployment** tab, select **Check for package updates** to perform synchronization.</span></span> <span data-ttu-id="72d89-129">(標準セルフサービス プロセスを通じて) ダウンロード可能なインストーラーは、現在 LCS で利用可能などのインストーラーが環境に適用されるかに応じて、同期および更新されます。</span><span class="sxs-lookup"><span data-stu-id="72d89-129">The installers that are available for download (through standard self-service processes) are synchronized and updated, depending on which of the installers that are currently available in LCS apply to environment.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="72d89-130">以前は、RetailSelfService テーブルは、すべてのインストーラー情報が取得されるソースとして使用されていました。</span><span class="sxs-lookup"><span data-stu-id="72d89-130">Previously, the RetailSelfService table was used as the source that all installer information was pulled from.</span></span> <span data-ttu-id="72d89-131">このテーブルには、以前のパッケージ アプリケーション メソッドを使用して Headquarters にアップロードされたインストーラーに基づいて情報が入力されています。</span><span class="sxs-lookup"><span data-stu-id="72d89-131">Information was entered in this table, based on the installers that had been uploaded into headquarters through the earlier package application method.</span></span> <span data-ttu-id="72d89-132">新しいセルフサービスの作成方法では、RetailSelfService テーブル (以前のセルフサービス パッケージのアップロード方法) のすべての値を、LCS 共有アセット ライブラリで使用可能なすべてのインストーラーと結合します。</span><span class="sxs-lookup"><span data-stu-id="72d89-132">The new self-service population methodology combines all values in the RetailSelfService table (the earlier self-service package upload method) with all available installers in the LCS Shared asset library.</span></span> <span data-ttu-id="72d89-133">セルフサービス ドロップダウン パッケージ セレクターには、この新しく同期された結合ソースからオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72d89-133">The self-service drop-down package selectors will show the options from this newly synchronized, combined source.</span></span>
    >
    > <span data-ttu-id="72d89-134">このトピックの冒頭で説明したように、以前のセルフサービス パッケージのアップロード方法は廃止されましたが、今後削除されるまで引き続きサポートされます。</span><span class="sxs-lookup"><span data-stu-id="72d89-134">As was stated at the beginning of this topic, the earlier self-service package upload method is obsolete, but it will continue to be supported until it's removed in the future.</span></span>

4. <span data-ttu-id="72d89-135">同じページで、関連する場所 (**デバイス**、**すべての店舗**、および **チャネル データベース**) の Headquarters 全体で使用される既定のパッケージを選択できます。</span><span class="sxs-lookup"><span data-stu-id="72d89-135">On the same page, you can select default packages that will be used throughout headquarters in their relevant locations (**Devices**, **All stores**, and **Channel database**).</span></span>
5. <span data-ttu-id="72d89-136">次のテーブルのリンクを使用して、Modern POS、ハードウェア ステーション、または Commerce Scale Unit の標準コンフィギュレーション フローとインストール フローを実行します。</span><span class="sxs-lookup"><span data-stu-id="72d89-136">Perform standard configuration and installation flows for Modern POS, hardware station, or Commerce Scale Unit by using the links in the following table.</span></span>

    | <span data-ttu-id="72d89-137">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="72d89-137">Component</span></span> | <span data-ttu-id="72d89-138">リンク</span><span class="sxs-lookup"><span data-stu-id="72d89-138">Link</span></span> |
    |---|---|
    | <span data-ttu-id="72d89-139">Modern POS</span><span class="sxs-lookup"><span data-stu-id="72d89-139">Modern POS</span></span> | [<span data-ttu-id="72d89-140">Modern POS (MPOS) のコンフィギュレーション、インストール、および有効化</span><span class="sxs-lookup"><span data-stu-id="72d89-140">Configure, install, and activate Modern POS (MPOS)</span></span>](../retail-modern-pos-device-activation.md) |
    | <span data-ttu-id="72d89-141">Hardware station</span><span class="sxs-lookup"><span data-stu-id="72d89-141">Hardware station</span></span> | [<span data-ttu-id="72d89-142">Retail Hardware Station のコンフィギュレーションおよびインストール</span><span class="sxs-lookup"><span data-stu-id="72d89-142">Configure and install Retail hardware station</span></span>](../retail-hardware-station-configuration-installation.md) |
    | <span data-ttu-id="72d89-143">Commerce Scale Unit (旧 Retail Store Scale Unit)</span><span class="sxs-lookup"><span data-stu-id="72d89-143">Commerce Scale Unit (formerly known as Retail Store Scale Unit)</span></span> | [<span data-ttu-id="72d89-144">Commerce Scale Unit のコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="72d89-144">Configure and install Commerce Scale Unit</span></span>](retail-store-scale-unit-configuration-installation.md) |