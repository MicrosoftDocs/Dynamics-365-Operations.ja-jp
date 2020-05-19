---
title: 在庫エイジング レポート ストレージ
description: このトピックでは、在庫エイジング レポートを実行し、その出力をフォームおよびグラフとして使用できるようにする機能について説明します。
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e68833cc2b4430f66419a67b1cba5f6c8c209f4
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323626"
---
# <a name="inventory-aging-report-storage"></a><span data-ttu-id="285e8-103">在庫エイジング レポート ストレージ</span><span class="sxs-lookup"><span data-stu-id="285e8-103">Inventory aging report storage</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="285e8-104">Microsoft Dynamics 365 Supply Chain Management では、**在庫のエイジング レポート ストレージ** を実行して、フォームとグラフとして出力できるようにします。</span><span class="sxs-lookup"><span data-stu-id="285e8-104">In Microsoft Dynamics 365 Supply Chain Management, you can run an **Inventory aging report storage** report and make the output available as a form and a chart.</span></span> <span data-ttu-id="285e8-105">フォームでは、コンフィギュレーションされているレイアウトに応じて、列と集計残高が動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="285e8-105">In the form, columns and aggregate balances are dynamically adjusted, depending on the layout that is configured.</span></span> <span data-ttu-id="285e8-106">チャートは、フィルター処理をサポートする視覚概要を提供します。詳細にドリルダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="285e8-106">The chart provides a visual overview that supports filtering and lets you drill down into details.</span></span> <span data-ttu-id="285e8-107">さらに、**在庫エイジング レポート** という名前のデータ エンティティを使用すると、実行された**在庫エイジング レポート ストレージ** レポートの結果を Microsoft Excel ファイルや PDF ファイルなどの形式でエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="285e8-107">Additionally, a data entity that is named **Inventory aging report** lets you export the results of an **Inventory aging report storage** report run to a format such as a Microsoft Excel file or a PDF file.</span></span>

<span data-ttu-id="285e8-108">**在庫エイジング レポート ストレージ** レポートを実行するこの方法は、出力に多数の行が含まれている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="285e8-108">This method of running an **Inventory aging report storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="285e8-109">たとえば、倉庫として作成された 50,000 個の品目と 300 軒の店舗がある場合、出力には多くの明細行が含まれ、在庫エイジングは、品目、サイト、および倉庫ごとに要求します。</span><span class="sxs-lookup"><span data-stu-id="285e8-109">For example, the output will contain many lines if you have 50,000 items and 300 stores that are created as warehouses, and you request inventory aging by item, site, and warehouse.</span></span>

## <a name="enable-the-inventory-value-storage-report-feature"></a><span data-ttu-id="285e8-110">在庫評価額ストレージ レポート機能を有効にします</span><span class="sxs-lookup"><span data-stu-id="285e8-110">Enable the Inventory value storage report feature</span></span>

<span data-ttu-id="285e8-111">この機能を使用するには、事前にシステム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="285e8-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="285e8-112">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して機能状態を確認し、必要に応じてそれを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="285e8-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="285e8-113">この機能は次のように一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="285e8-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="285e8-114">**モジュール** - 原価管理</span><span class="sxs-lookup"><span data-stu-id="285e8-114">**Module** - Cost management</span></span>
- <span data-ttu-id="285e8-115">**機能名称** - 在庫エイジング レポート ストレージ</span><span class="sxs-lookup"><span data-stu-id="285e8-115">**Feature name** - Inventory aging report storage</span></span>

## <a name="run-an-inventory-aging-report-storage"></a><span data-ttu-id="285e8-116">在庫評価額レポート ストレージを実行する</span><span class="sxs-lookup"><span data-stu-id="285e8-116">Run an Inventory aging report storage</span></span>

1. <span data-ttu-id="285e8-117">**原価管理 \> 照会およびレポート \> 在庫エイジング レポート ストレージ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="285e8-117">Go to **Cost management \> Inquiries and reports \> Inventory aging report storage**.</span></span>
1. <span data-ttu-id="285e8-118">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="285e8-118">Select **New**.</span></span>
1. <span data-ttu-id="285e8-119">**プロセス ID – 名前**フィールドに、レポートの固有の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="285e8-119">In the **Process Identifier – Name** field, enter a unique name for the report.</span></span>
1. <span data-ttu-id="285e8-120">**ID – ID** レポートを選択し、必要に応じてフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="285e8-120">Select the **Identification – ID** report, and filter it as you require.</span></span>

    <span data-ttu-id="285e8-121">レポートの実行は、常にバッチ ジョブで行われます。</span><span class="sxs-lookup"><span data-stu-id="285e8-121">Report execution is always done in a batch job.</span></span>

1. <span data-ttu-id="285e8-122">バッチ ジョブが完了すると、出力は**在庫エイジング レポート ストレージ** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="285e8-122">After the batch job is completed, the output is shown on the **Inventory aging report storage** page.</span></span>
1. <span data-ttu-id="285e8-123">従来のグリッド レイアウトを持つフォームとして出力を表示するには、**詳細の表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="285e8-123">To view the output as a form that has a traditional grid layout, select **View details**.</span></span> <span data-ttu-id="285e8-124">集計グラフとして出力を表示するには、**グラフの表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="285e8-124">To view the output as an aggregated chart, select **View chart**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="285e8-125">フォームには、レポート レイアウトで定義されている小計は含まれません。</span><span class="sxs-lookup"><span data-stu-id="285e8-125">The form won't include subtotals that are defined in the report layout.</span></span>

<span data-ttu-id="285e8-126">**在庫エイジング レポート** データ エンティティを使用すると、**プロセス ID – 名前** フィールドのフィルターを、データ管理がサポートする形式に適用することにより、**在庫エイジング レポート ストレージ** レポートをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="285e8-126">The **Inventory aging report** data entity lets you export the output of an **Inventory aging report storage** report by applying a filter for the **Process Identifier – Name** field to any format that Data management supports.</span></span>
