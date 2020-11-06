---
title: ウェーブ ラベル印刷の設定と使用
description: このトピックでは、ウェーブ ラベル印刷についての説明と、設定方法について解説します。
author: GarmMSFT
manager: PJacobse
ms.date: 05/01/2020
ms.topic: configure-wave-label-printing
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 1f51ed9f05caede3d4f320ddb6b705e67df9aa1f
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016958"
---
# <a name="set-up-and-use-wave-label-printing"></a><span data-ttu-id="f8bda-103">ウェーブ ラベル印刷の設定と使用</span><span class="sxs-lookup"><span data-stu-id="f8bda-103">Set up and use wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8bda-104">ウェーブ ラベル印刷では、ウェーブの実行中にウェーブのテンプレートから直接ラベルを作成して印刷できる新しいウェーブ ステップ メソッドが導入され、ラベル印刷に代わるアプローチを提供します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="f8bda-105">そのため、作業者がモバイル デバイス上で作業指示を実行する前に、ラベルは既に利用可能となっています。</span><span class="sxs-lookup"><span data-stu-id="f8bda-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="f8bda-106">作業者は、ピッキング後ではなく、ピッキング中に必要なラベルを貼ることができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="f8bda-107">ウェーブ ラベル印刷では、Zebra プログラム言語 (ZPL) を使用してラベル レイアウトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="f8bda-108">ラベルのレイアウトは、ヘッダー、本文、フッターの3つのセクションに分かれており、重複した構造を持つラベルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="f8bda-109">ウェーブ ラベルのテンプレートは、システムに使用するラベルのレイアウトの指示を出します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="f8bda-110">使用するプリンターはユーザーが指定できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-110">Users can specify which printer is used.</span></span> <span data-ttu-id="f8bda-111">また、必要に応じて、複数のプリンターで同時にラベルを印刷することもできます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="f8bda-112">**ウェーブ ラベルの履歴** ページには、この設定を使用して作成されたすべてのラベルのレコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="f8bda-113">作業ヘッダーに基づいたラベルの印刷と照合、作業ヘッダーごとの区切りラベルの印刷、コンテナー内容のラベル、ケースのラベル、その他のラベルを印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="f8bda-114">この機能は、ドキュメント ルーティングに基づく既存のラベル印刷機能を置き換えるものではありません。</span><span class="sxs-lookup"><span data-stu-id="f8bda-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="f8bda-115">ウェーブ ラベル印刷では、次の機能拡張が提供されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="f8bda-116">コンテナ化を使用せずに、単一の作業ラインにカートン数に応じたラベルを印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="f8bda-117">("カートン" とは、出荷単位の順序グループライン上で指定された出荷単位を意味します。)</span><span class="sxs-lookup"><span data-stu-id="f8bda-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="f8bda-118">複数の異なるラベル シーケンスを印刷します (たとえば、カートンとパレット ラベル)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="f8bda-119">ラベル リストを含有し (たとえば、1/124、2/124、...124/124) 、リストの範囲を定義します (たとえば、作業ライン、積荷ライン、出荷)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="f8bda-120">船荷証券を生成する前に、ラベルに船荷証券 ID を作成して印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="f8bda-121">それぞれのカートンに対して固有のシリアル出荷コンテナー コード (SSCC) を作成し、各ラベルに含めます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="f8bda-122">船荷証券 ID と SSCC で使用する、GS1 に準拠したシーケンス番号を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="f8bda-123">モバイル デバイスとリッチ クライアントの両方からラベルを再印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="f8bda-124">ラベルを無効化し (例 : 小口ピックのシナリオなど)、再印刷を行います。</span><span class="sxs-lookup"><span data-stu-id="f8bda-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="f8bda-125">ウェーブ ラベル履歴をクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="f8bda-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="f8bda-126">ドキュメント ルーティング レイアウトに対して行われた改善は、ドキュメント ルーティング レイアウトとウェーブ ラベル レイアウト間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="f8bda-127">(詳細については、 [ライセンス プレート向けドキュメント ルーティング レイアウト ](../warehousing/document-routing-layout-for-license-plates.md)を参照してください。)</span><span class="sxs-lookup"><span data-stu-id="f8bda-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="f8bda-128">これらの機能強化により、パレット積みのカートンへのラベル付けがより効率的になります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="f8bda-129">カートンを個別にスキャンすることで自動的に受注確認を行う大手の小売店に出荷している企業には、特に有用となります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="f8bda-130">このトピックで説明する構成シナリオは、業務上の要件に応じて個別に、または組み合わせて実装することができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="f8bda-131">連続して動作する複数のウェーブ ラベルのテンプレートを設計することができます (シナリオ3を参照のこと)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="f8bda-132">たとえば、シナリオ１でカートン ラベルを印刷し、シナリオ２でパレット ラベルを印刷することができます (在庫のパレットのサイズや構成が異なる場合)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="f8bda-133">ウェーブ ラベルの印刷機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="f8bda-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="f8bda-134">*ウェーブ ラベルの印刷* 機能を使用するには、システム上で有効になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="f8bda-135">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="f8bda-136">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f8bda-137">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="f8bda-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="f8bda-138">**機能名 :** *ウェーブ ラベルの印刷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="f8bda-139">シナリオ1 : 1つのウェーブ ラベルを生成するウェーブ ラベルの印刷</span><span class="sxs-lookup"><span data-stu-id="f8bda-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="f8bda-140">このシナリオでは、各カートンを個別にスキャンすることで、受注を自動的に確認する大手の小売業者向けの出荷ラベルの印刷方法を解説しています。</span><span class="sxs-lookup"><span data-stu-id="f8bda-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="f8bda-141">このシナリオでは、エンドツーエンドのフローを説明します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="f8bda-142">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="f8bda-142">Make demo data available</span></span>

<span data-ttu-id="f8bda-143">このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="f8bda-144">ウェーブ ラベルのメソッドが使用可能であることを確認します</span><span class="sxs-lookup"><span data-stu-id="f8bda-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="f8bda-145">場合によっては、ウェーブ ラベルの印刷メソッドを利用するには、ウェーブ プロセスのメソッドを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="f8bda-146">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="f8bda-147">**WaveLabelPrinting** がリストに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="f8bda-148">表示されない場合は、アクション ウィンドウで **メソッドの再生成** を選択して追加します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="f8bda-149">ウェーブのテンプレートを構成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-149">Configure a wave template</span></span>

<span data-ttu-id="f8bda-150">ウェーブのテンプレートを使用すると、特定のウェーブ メソッドのインスタンスをこれに対応するウェーブ ラベルのテンプレートにリンクさせることができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="f8bda-151">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="f8bda-152">**62 出荷の既定** などのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="f8bda-153">**メソッド** クイックタブで、 **ウェーブ ラベルの印刷** メソッドを **選択したメソッド** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="f8bda-154">**選択したメソッド** 列で、 **ウェーブ ラベルの印刷** メソッドを選択し、 **ウェーブ ステップ コード** フィールドを *PrintLabel* に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="f8bda-155">ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="f8bda-156">ウェーブ ラベルのレイアウトを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-156">Create a wave label layout</span></span>

<span data-ttu-id="f8bda-157">ラベル レイアウトでは、ラベルに印刷される情報と、ラベルのレイアウトを制御します。ここでは、プリンターに送信される ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="f8bda-158">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ドキュメント ルーティング レイアウト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="f8bda-159">以下の設定をしたレコードを作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-160">**ラベルのレイアウト ID :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-161">**説明 :** *カートン (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="f8bda-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="f8bda-162">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-163">アクション ウィンドウで、 **ウェーブ ラベル行の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="f8bda-164">**ウェーブ ラベル行の設定** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="f8bda-165">ここでは、ラベルの動的な部分を構成できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="f8bda-166">以下の設定を持つ行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-167">**行 Id:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="f8bda-168">**行テーブル名 :** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="f8bda-169">**行の開始位置 :** *0*</span><span class="sxs-lookup"><span data-stu-id="f8bda-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="f8bda-170">このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="f8bda-171">**行の高さ :** *0*</span><span class="sxs-lookup"><span data-stu-id="f8bda-171">**Row height:** *0*</span></span>

        <span data-ttu-id="f8bda-172">このフィールドでは、ZPL 標準に従って、各行の高さをポイント数を使用して定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="f8bda-173">行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="f8bda-174">この例では行が1つしか存在しないため、この値を *0* (ゼロ) に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="f8bda-175">**ページごとの行数 :** *1*</span><span class="sxs-lookup"><span data-stu-id="f8bda-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="f8bda-176">このフィールドでは、各ラベルに印刷できる行の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f8bda-177">この設定により、ウェーブ ラベル テーブルの各レコードに対して個別の ZPL ラベルが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="f8bda-178">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-178">Close the page.</span></span>
1. <span data-ttu-id="f8bda-179">アクション ウィンドウで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f8bda-180">クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-181">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-182">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-183">**フィールド:** *作業タイプ*</span><span class="sxs-lookup"><span data-stu-id="f8bda-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="f8bda-184">**基準:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="f8bda-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="f8bda-185">このクエリを実行することで、ラベルにはピックタイプの作業行のみが印刷され、プットタイプの作業行は印刷されません。</span><span class="sxs-lookup"><span data-stu-id="f8bda-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="f8bda-186">船荷証券 ID を印刷できるようにするには、 **結合** タブで **作業ライン** テーブルを選択し、 **出荷** テーブルを結合します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="f8bda-187">クエリ エディター ダイアログボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-188">**印刷テキストレイアウト** クイック タブには、 **ヘッダー セクション** 、 **ボディ セクション** 、 **フッター セクション** の3つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="f8bda-189">**ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="f8bda-190">たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="f8bda-191">**ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="f8bda-192">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="f8bda-193">**ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="f8bda-194">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="f8bda-195">この設定では、ラベルを1部ずつ印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="f8bda-196">さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="f8bda-197">たとえば、各ラベルを4部印刷するには、 **\^PQ4** を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="f8bda-198">以上でラベルを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="f8bda-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="f8bda-199">ウェーブ ラベルのタイプを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-199">Create a wave label type</span></span>

<span data-ttu-id="f8bda-200">ウェーブ ラベルのタイプは、ウェーブ ラベル テンプレートを出荷単位の順序グループ ライン上の出荷単位にリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="f8bda-201">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="f8bda-202">以下の設定のあるウェーブ ラベル タイプを追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-203">**ラベル タイプ :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-204">**説明 :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="f8bda-205">単位順序グループを設定します</span><span class="sxs-lookup"><span data-stu-id="f8bda-205">Set up unit sequence groups</span></span>

<span data-ttu-id="f8bda-206">次に、ウェーブ ラベル タイプの出荷単位順序グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="f8bda-207">**倉庫管理 \> 設定 \> 倉庫 \> 出荷単位の順序グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="f8bda-208">**Ea Box PL** グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="f8bda-209">**ボックス** 明細行では 、 **ウェーブ レベル タイプ** フィールドに *カートン* を設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="f8bda-210">ウェーブ ラベルのテンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-210">Create a wave label template</span></span>

<span data-ttu-id="f8bda-211">次は、ウェーブ ラベルタイプのウェーブ ラベル テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="f8bda-212">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="f8bda-213">ウェーブ レベル テンプレートを追加し、ヘッダーに以下の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="f8bda-214">**ラベル テンプレート名 :** *カートン ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="f8bda-215">**説明 :** *カートン ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="f8bda-216">**ウェーブ ステップ コード :** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="f8bda-217">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="f8bda-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f8bda-218">**一般** クイックタブで、 **ウェーブ ラベル タイプ** フィールドを *カートン* に設定し ます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="f8bda-219">**ウェーブ ラベル テンプレートの詳細** クイック タブで、次の設定を含む新たな行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-220">**ラベルのレイアウト ID :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-221">**プリンター名** 適切な ZPL プリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="f8bda-222">**クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="f8bda-223">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-224">オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="f8bda-225">**ウェーブ ラベル テンプレートの詳細** クイックタブで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="f8bda-226">続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-227">**テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-228">**派生テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-229">**フィールド :** *アカウント番号*</span><span class="sxs-lookup"><span data-stu-id="f8bda-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="f8bda-230">**条件 :** 関連する顧客アカウント番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="f8bda-231">完了後は、 **OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="f8bda-232">アクション ウィンドウで **クエリの編集** を選択して、全体のラベル テンプレートで使用するクエリ エディター ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="f8bda-233">クエリ エディター ダイアログ ボックスの **ソート** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-234">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-235">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-236">**フィールド :** *参照読み込み行の Id (レコード ID)*</span><span class="sxs-lookup"><span data-stu-id="f8bda-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="f8bda-237">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="f8bda-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="f8bda-238">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-239">グループのリセット操作の確認を促すメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="f8bda-240">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="f8bda-241">アクション ウィンドウで、 **ウェーブ ラベル テンプレート グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="f8bda-242">**ウェーブ ラベル テンプレート グループ** ダイアログ ボックスで、 **参照フィールド名** フィールドが *参照積荷行 ID* に設定されている行を選択し、この行の **ラベルのビルド ID** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id* , and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-243">この設定では、作業グループの設定に関係なく、ウェーブ全体で各積荷ラインごとに 1 つのラベル シーケンス（"カートン X のうちの 1"）を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="f8bda-244">このラベル番号は、ラベルのレイアウトに印刷できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="f8bda-245">シーケンス番号の拡張機能を構成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-245">Configure number sequence extensions</span></span>

<span data-ttu-id="f8bda-246">シーケンス番号の拡張機能は、特定のシーケンス番号の GS1 コンプライアンスを制御します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="f8bda-247">この構成は、こののシナリオでは任意となります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="f8bda-248">詳細情報と構成についての手順については、[シーケンス番号拡張機能の構成](../warehousing/configure-number-sequence-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="f8bda-249">販売注文を作成して倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="f8bda-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="f8bda-250">**販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="f8bda-251">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-252">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f8bda-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f8bda-253">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="f8bda-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f8bda-254">次の設定を持つ 2 つの販売明細行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="f8bda-255">販売注文明細行 1:</span><span class="sxs-lookup"><span data-stu-id="f8bda-255">Sales order line 1:</span></span>

        - <span data-ttu-id="f8bda-256">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f8bda-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="f8bda-257">**数量:** *9024*</span><span class="sxs-lookup"><span data-stu-id="f8bda-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="f8bda-258">**出荷単位 :** *ea* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="f8bda-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="f8bda-259">販売注文明細行 2:</span><span class="sxs-lookup"><span data-stu-id="f8bda-259">Sales order line 2:</span></span>

        - <span data-ttu-id="f8bda-260">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f8bda-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="f8bda-261">**数量:** *9016*</span><span class="sxs-lookup"><span data-stu-id="f8bda-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="f8bda-262">**出荷単位 :** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="f8bda-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-263">ここで扱っている項目や数量はあくまでも一例です。</span><span class="sxs-lookup"><span data-stu-id="f8bda-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="f8bda-264">前述の手順で定義した出荷単位のシーケンス グループを使用し、 *ea* から *Box* および *PL* への適切な単位変換を定義し、倉庫 *62* に在庫がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="f8bda-265">詳細については、[測定単位と在庫のポリシー](unit-measure-stocking-policies.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="f8bda-266">販売注文明細行 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-266">Select sales order line 1.</span></span> <span data-ttu-id="f8bda-267">続いて、 **在庫** メニューの **販売注文明細行** セクションで、 **引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="f8bda-268">**引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-268">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="f8bda-269">販売注文明細行 2 については、手順 4 と 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="f8bda-270">アクション ウィンドウの **倉庫** タブで、 **倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f8bda-271">以下のイベントが発生します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-271">The following events occur:</span></span>

    - <span data-ttu-id="f8bda-272">システムは、ラベル印刷の手順を含むテンプレートを使用して、作成された出荷を処理します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="f8bda-273">ラベルのレイアウトはラベル フォーマットの定義に使用され、ラベル テンプレートで選択されたプリンタで印刷されるラベルとなります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="f8bda-274">ウェーブ ラベルが生成され、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="f8bda-275">ラベルの数は、カートンの数と等しくなります (この例では、1 行目の 376 ボックスラベルと 2 行目の 322 ボックスラベル)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="f8bda-276">出荷に対して新たな船荷証券 ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="f8bda-277">シーケンス番号の拡張機能を構成した場合、ウェーブ ラベル ID は **SSCC-18** の番号形式に従います。</span><span class="sxs-lookup"><span data-stu-id="f8bda-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="f8bda-278">次のページから、ウェーブ ラベルを表示および再印刷できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="f8bda-279">各ページのアクション ペインにある **出荷** タブの **関連情報** グループで、 **ウェーブ ラベル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="f8bda-280">すべての出荷 \> 出荷詳細</span><span class="sxs-lookup"><span data-stu-id="f8bda-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="f8bda-281">すべての貨物 \> 貨物の詳細</span><span class="sxs-lookup"><span data-stu-id="f8bda-281">All loads \> Load details</span></span>
- <span data-ttu-id="f8bda-282">すべてのウェーブ</span><span class="sxs-lookup"><span data-stu-id="f8bda-282">All waves</span></span>
- <span data-ttu-id="f8bda-283">ウェーブ ラベル</span><span class="sxs-lookup"><span data-stu-id="f8bda-283">Wave labels</span></span>
- <span data-ttu-id="f8bda-284">ウェーブ ラベル履歴</span><span class="sxs-lookup"><span data-stu-id="f8bda-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="f8bda-285">シナリオ 2 : コンテナ化に使用するウェーブ ラベル印刷 (ウェーブ ラベル レコードなし)</span><span class="sxs-lookup"><span data-stu-id="f8bda-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="f8bda-286">このシナリオでは、コンテナ化を利用して品目を自動的にカートンに分割し、ウェーブ ラベルのレコードが必要とされない場合に、ウェーブ ラベルを印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="f8bda-287">この場合、コンテナー IDは、SSCC のプレースホルダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="f8bda-288">このシナリオとシナリオ 1 の主な相違点は次のとおりです :</span><span class="sxs-lookup"><span data-stu-id="f8bda-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="f8bda-289">**ウェーブ ラベル テンプレート :** ウェーブ ラベル テンプレートでウェーブ ラベルのタイプを選択する必要はなく、ラベル ビルドのグループ化も必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f8bda-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="f8bda-290">それ以外の場合は、シナリオ1での解説と同じ方法で、ウェーブ ラベル テンプレートを構成し、ウェーブ テンプレートにリンクします。</span><span class="sxs-lookup"><span data-stu-id="f8bda-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="f8bda-291">ウェーブ ラベルが生成されないようにするには、ウェーブ ラベル タイプを空白のままにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="f8bda-292">**ウェーブ ラベル レイアウト :** ウェーブ ラベル レコードではなく、作業明細行のウェーブ ラベル レイアウト行を構成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="f8bda-293">ラベル レイアウトの行設定は、 **WHSWorkLine** テーブルではなく、 **WHSWaveLabel** テーブルを使用して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="f8bda-294">**ページあたりの行数** 設定は、ボディ セクションに含まれる行数を制御します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="f8bda-295">この構成は、複数の異なるアイテムを1つのラベル付きボックスやパレットに梱包する業務シナリオにも適しており、この梱包プロセスは作業を作成することで定義できます (例 : 出荷ごとにグループ化された作業など)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="f8bda-296">このシナリオでは、エンドツーエンドのフローを説明します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="f8bda-297">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="f8bda-297">Make demo data available</span></span>

<span data-ttu-id="f8bda-298">このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="f8bda-299">ウェーブ ラベルのメソッドが使用可能であることを確認します</span><span class="sxs-lookup"><span data-stu-id="f8bda-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="f8bda-300">場合によっては、ウェーブ ラベルの印刷メソッドを利用するには、ウェーブ プロセスのメソッドを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="f8bda-301">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="f8bda-302">**WaveLabelPrinting** がリストに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="f8bda-303">表示されない場合は、アクション ウィンドウで **メソッドの再生成** を選択して追加します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="f8bda-304">ウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="f8bda-304">Set up a wave template</span></span>

<span data-ttu-id="f8bda-305">ウェーブのテンプレートを使用すると、特定のウェーブ メソッドのインスタンスをこれに対応するウェーブ ラベルのテンプレートにリンクさせることができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="f8bda-306">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="f8bda-307">**63 コンテナ化** などのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="f8bda-308">**メソッド** クイックタブで、 **ウェーブ ラベルの印刷** メソッドを **選択したメソッド** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="f8bda-309">**選択したメソッド** 列で、 **ウェーブ ラベルの印刷** メソッドを選択し、 **ウェーブ ステップ コード** フィールドを *PrintLabel* に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="f8bda-310">ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="f8bda-311">ウェーブ ラベルのレイアウトを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-311">Create a wave label layout</span></span>

1. <span data-ttu-id="f8bda-312">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ドキュメント ルーティング レイアウト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="f8bda-313">以下の設定をしたレコードを作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-314">**ラベルのレイアウト ID :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-315">**説明 :** *カートン (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="f8bda-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="f8bda-316">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-317">アクション ウィンドウで、 **ウェーブ ラベル行の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="f8bda-318">**ウェーブ ラベル行の設定** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="f8bda-319">ここでは、ラベルの動的な部分を構成できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="f8bda-320">以下の設定を持つ行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-321">**行 Id:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="f8bda-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="f8bda-322">**行テーブル名 :** *WHSWorkLine*</span><span class="sxs-lookup"><span data-stu-id="f8bda-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="f8bda-323">**行の開始位置 :** *500*</span><span class="sxs-lookup"><span data-stu-id="f8bda-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="f8bda-324">このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="f8bda-325">**行の高さ :** *-50*</span><span class="sxs-lookup"><span data-stu-id="f8bda-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="f8bda-326">このフィールドは、各行の高さを定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-326">This field defines the height of each row.</span></span> <span data-ttu-id="f8bda-327">行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="f8bda-328">**ページごとの行数 :** *5*</span><span class="sxs-lookup"><span data-stu-id="f8bda-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="f8bda-329">このフィールドでは、各ラベルに印刷できる行の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f8bda-330">この設定により、作業ごとに複数の ZPL ラベルが印刷され、各ページには最大5行までの作業明細行を保存できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="f8bda-331">たとえば、12行のコンテナーに対してラベルを印刷すると、3部のラベルが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="f8bda-332">ピッキング ラインごとに個別のラベルを印刷する場合は、この値を *1* に設定してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="f8bda-333">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-333">Close the page.</span></span>
1. <span data-ttu-id="f8bda-334">アクション ウィンドウで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f8bda-335">クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-336">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-337">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-338">**フィールド:** *作業タイプ*</span><span class="sxs-lookup"><span data-stu-id="f8bda-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="f8bda-339">**基準:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="f8bda-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="f8bda-340">船荷証券 ID を印刷できるようにするには、 **結合** タブで **作業ライン** テーブルを選択し、 **出荷** テーブルを結合します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="f8bda-341">クエリ エディター ダイアログボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-342">**印刷テキストレイアウト** クイック タブには、 **ヘッダー セクション** 、 **ボディ セクション** 、 **フッター セクション** の3つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="f8bda-343">**ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="f8bda-344">たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="f8bda-345">**ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="f8bda-346">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="f8bda-347">**ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="f8bda-348">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="f8bda-349">この設定では、ラベルを1部ずつ印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="f8bda-350">さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="f8bda-351">たとえば、各ラベルを4部印刷するには、 **\^PQ4** を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="f8bda-352">以上でラベルを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="f8bda-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="f8bda-353">ウェーブ ラベルのテンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-353">Create a wave label template</span></span>

1. <span data-ttu-id="f8bda-354">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="f8bda-355">ウェーブ レベル テンプレートを追加し、ヘッダーに以下の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="f8bda-356">**ラベル テンプレート名 :** *コンテナー ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="f8bda-357">**説明 :** *コンテナー ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="f8bda-358">**ウェーブ ステップ コード :** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="f8bda-359">**倉庫:** *63*</span><span class="sxs-lookup"><span data-stu-id="f8bda-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="f8bda-360">**ウェーブ ラベル テンプレートの詳細** クイック タブで、以下の設定を含む新たな行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-361">**ラベルのレイアウト ID :** *コンテナー*</span><span class="sxs-lookup"><span data-stu-id="f8bda-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="f8bda-362">**プリンター名** 適切な ZPL プリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="f8bda-363">**クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="f8bda-364">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-365">オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="f8bda-366">**ウェーブ ラベル テンプレートの詳細** クイックタブで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="f8bda-367">続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-368">**テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-369">**派生テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-370">**フィールド :** *アカウント番号*</span><span class="sxs-lookup"><span data-stu-id="f8bda-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="f8bda-371">**条件 :** 関連する顧客アカウント番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="f8bda-372">完了後は、 **OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="f8bda-373">シーケンス番号の拡張機能を構成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-373">Configure number sequence extensions</span></span>

<span data-ttu-id="f8bda-374">シーケンス番号の拡張機能は、特定のシーケンス番号の GS1 コンプライアンスを制御します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="f8bda-375">この構成は、こののシナリオでは任意となります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="f8bda-376">詳細情報と構成についての手順については、[シーケンス番号拡張機能の構成](../warehousing/configure-number-sequence-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="f8bda-377">販売注文を作成して倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="f8bda-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="f8bda-378">**販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="f8bda-379">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-380">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f8bda-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f8bda-381">**倉庫:** *63*</span><span class="sxs-lookup"><span data-stu-id="f8bda-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="f8bda-382">販売注文明細行を5行追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="f8bda-383">販売注文明細行 1:</span><span class="sxs-lookup"><span data-stu-id="f8bda-383">Sales order line 1:</span></span>

        - <span data-ttu-id="f8bda-384">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f8bda-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="f8bda-385">**数量:** *10*</span><span class="sxs-lookup"><span data-stu-id="f8bda-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="f8bda-386">販売注文明細行 2:</span><span class="sxs-lookup"><span data-stu-id="f8bda-386">Sales order line 2:</span></span>

        - <span data-ttu-id="f8bda-387">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f8bda-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="f8bda-388">**数量:** *20*</span><span class="sxs-lookup"><span data-stu-id="f8bda-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="f8bda-389">販売注文明細行 3:</span><span class="sxs-lookup"><span data-stu-id="f8bda-389">Sales order line 3:</span></span>

        - <span data-ttu-id="f8bda-390">**品目番号:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="f8bda-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="f8bda-391">**数量:** *20*</span><span class="sxs-lookup"><span data-stu-id="f8bda-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="f8bda-392">販売注文明細行 4:</span><span class="sxs-lookup"><span data-stu-id="f8bda-392">Sales order line 4:</span></span>

        - <span data-ttu-id="f8bda-393">**品目番号:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="f8bda-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="f8bda-394">**数量:** *40*</span><span class="sxs-lookup"><span data-stu-id="f8bda-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="f8bda-395">販売注文明細行 5:</span><span class="sxs-lookup"><span data-stu-id="f8bda-395">Sales order line 5:</span></span>

        - <span data-ttu-id="f8bda-396">**品目番号:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="f8bda-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="f8bda-397">**数量:** *50*</span><span class="sxs-lookup"><span data-stu-id="f8bda-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-398">ここで扱っている項目や数量はあくまでも一例です。</span><span class="sxs-lookup"><span data-stu-id="f8bda-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="f8bda-399">これらには、指定された倉庫の在庫が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="f8bda-400">販売注文明細行 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-400">Select sales order line 1.</span></span> <span data-ttu-id="f8bda-401">続いて、 **在庫** メニューの **販売注文明細行** セクションで、 **引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="f8bda-402">**引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-402">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="f8bda-403">追加の販売注文明細行については、手順 4 と 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="f8bda-404">アクション ウィンドウの **倉庫** タブで、 **倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f8bda-405">以下のイベントが発生します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-405">The following events occur:</span></span>

    - <span data-ttu-id="f8bda-406">システムは、ラベル印刷の手順を含むテンプレートを使用して、作成された出荷を処理します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="f8bda-407">ラベルのレイアウトは、ラベル フォーマットの定義に使用され、結果として 5つの行を含むのラベルとなり、ラベル テンプレートで選択したプリンタで印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="f8bda-408">出荷に対して新たな船荷証券 ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="f8bda-409">シーケンス番号の拡張機能を構成した場合、ウェーブ ラベル ID は **SSCC-18** の番号形式に従います。</span><span class="sxs-lookup"><span data-stu-id="f8bda-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="f8bda-410">これらのウェーブ ラベルを再印刷するには、 **倉庫管理 \> 照会とレポート \> ウェーブラベル履歴** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="f8bda-411">シナリオ 3 : 複数層のラベルのウェーブ ラベル印刷</span><span class="sxs-lookup"><span data-stu-id="f8bda-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="f8bda-412">このシナリオでは、倉庫管理プロセスで複数の階層階層の出荷ラベルが必要な場合の、ウェーブ ラベル印刷機能の使用方法を解説します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="f8bda-413">たとえば、カートンとパレットに対して別々のラベルの印刷を行い、改ラベルを出荷全体で印刷する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="f8bda-414">改ラベルとは、出荷 ID のラベルやバーコードなど、ロールとコンテナーの間の仕切りとして使用できるセパレート タイプのラベルを意味し、印刷後のラベルの仕分けが簡単になります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="f8bda-415">このシナリオとシナリオ１における構成の主な相違点は、改ラベルが有効になっていることを除いて、複数のウェーブ ラベル タイプをウェーブ ラベル テンプレートと出荷単位シーケンス グループ ラインに関連付ける必要があるという点です。</span><span class="sxs-lookup"><span data-stu-id="f8bda-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="f8bda-416">この構成を実行するには、このシナリオで次の要素を設定します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="f8bda-417">**ウェーブの処理方法 :** ウェーブ ラベル メソッドを「繰り返し可能」に設定し、ウェーブのテンプレートに2回以上 (またはそれ以上) を追加し、異なるウェーブのステップ コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="f8bda-418">**ウェーブ ラベル テンプレート :** ウェーブ ラベルのテンプレートを設定し、ウェーブ テンプレートとリンクさせます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="f8bda-419">それぞれのウェーブ ラベル テンプレートには、独自のウェーブ ラベル タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="f8bda-420">**ウェーブ ラベル レイアウト :** 複数のウェーブ ラベル レイアウトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="f8bda-421">ラベルの「層」ごとに独立したラベル レイアウトがあり、ラベル破断のレイアウトも用意されています。</span><span class="sxs-lookup"><span data-stu-id="f8bda-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="f8bda-422">このシナリオでは、エンドツーエンドのフローを説明します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="f8bda-423">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="f8bda-423">Make demo data available</span></span>

<span data-ttu-id="f8bda-424">このシナリオを実行するには、デモ データがインストールされている必要があり、法人として **USMF** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="f8bda-425">ウェーブ プロセス メソッドの設定</span><span class="sxs-lookup"><span data-stu-id="f8bda-425">Set up a wave process method</span></span>

1. <span data-ttu-id="f8bda-426">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブのプロセス メソッド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="f8bda-427">**WaveLabelPrinting** がリストに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="f8bda-428">表示されない場合は、アクション ウィンドウで **メソッドの再生成** を選択して追加します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="f8bda-429">**waveLabelPrinting** メソッドに、 **メソッドを繰り返し可能にする** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="f8bda-430">ウェーブ テンプレートの設定</span><span class="sxs-lookup"><span data-stu-id="f8bda-430">Set up a wave template</span></span>

1. <span data-ttu-id="f8bda-431">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="f8bda-432">**62 出荷の既定** などのテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="f8bda-433">**メソッド** クイックタブで、 **ウェーブ ラベルの印刷** メソッドを **選択したメソッド** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="f8bda-434">**選択した方法** 列で、 *カートン* などの **ウェーブ ステップ コード** 値を **ウェーブ ラベルの印刷** メソッドに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton* , to the **Wave label printing** method.</span></span> <span data-ttu-id="f8bda-435">ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="f8bda-436">**ウェーブ ラベルの印刷** メソッドを再度 **選択したメソッド** 列に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="f8bda-437">**選択されたメソッド** の列で、2 番目の **ウェーブ ラベルの印刷** メソッドに、 *パレット* などの別の **ウェーブ ステップ コード** の値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet* , to the second **Wave label printing** method.</span></span> <span data-ttu-id="f8bda-438">ウェーブ ステップ コードの詳細については、[ウェーブ ステップ コード](wave-step-codes.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="f8bda-439">3 つのウェーブ ラベルのレイアウトを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="f8bda-440">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ドキュメント ルーティング レイアウト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="f8bda-441">以下の設定をしたレコードを作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-442">**ラベルのレイアウト ID :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-443">**説明 :** *カートン (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="f8bda-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="f8bda-444">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-445">アクション ウィンドウで、 **ウェーブ ラベル行の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="f8bda-446">**ウェーブ ラベル行の設定** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="f8bda-447">ここでは、ラベルの動的な部分を構成できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="f8bda-448">以下の設定を持つ行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-449">**行 Id:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="f8bda-450">**行テーブル名 :** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="f8bda-451">**行の開始位置 :** *0*</span><span class="sxs-lookup"><span data-stu-id="f8bda-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="f8bda-452">このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="f8bda-453">**行の高さ :** *0*</span><span class="sxs-lookup"><span data-stu-id="f8bda-453">**Row height:** *0*</span></span>

        <span data-ttu-id="f8bda-454">このフィールドでは、ZPL 標準に従って、各行の高さをポイント数を使用して定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="f8bda-455">行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="f8bda-456">この例では行が1つしか存在しないため、この値を *0* (ゼロ) に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="f8bda-457">**ページごとの行数 :** *1*</span><span class="sxs-lookup"><span data-stu-id="f8bda-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="f8bda-458">このフィールドでは、各ラベルに印刷できる行の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f8bda-459">この設定により、ウェーブ ラベル テーブルの各レコードに対して個別の ZPL ラベルが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="f8bda-460">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-460">Close the page.</span></span>
1. <span data-ttu-id="f8bda-461">アクション ウィンドウで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f8bda-462">クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-463">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-464">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-465">**フィールド:** *作業タイプ*</span><span class="sxs-lookup"><span data-stu-id="f8bda-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="f8bda-466">**基準:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="f8bda-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="f8bda-467">このクエリを実行することで、ラベルにはピックタイプの作業行のみが印刷され、プットタイプの作業行は印刷されません。</span><span class="sxs-lookup"><span data-stu-id="f8bda-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="f8bda-468">船荷証券 ID を印刷できるようにするには、 **結合** タブで **作業ライン** テーブルを選択し、 **出荷** テーブルを結合します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="f8bda-469">クエリ エディター ダイアログボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-470">**印刷テキストレイアウト** クイック タブには、 **ヘッダー セクション** 、 **ボディ セクション** 、 **フッター セクション** の3つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="f8bda-471">**ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="f8bda-472">たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="f8bda-473">**ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="f8bda-474">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="f8bda-475">**ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="f8bda-476">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="f8bda-477">この設定では、ラベルを1部ずつ印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="f8bda-478">さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="f8bda-479">たとえば、各ラベルを4部印刷するには、 **\^PQ4** を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="f8bda-480">1番目のラベルを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="f8bda-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="f8bda-481">以下の設定を持つ 2 番目のレイアウト レコードを作成します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-482">**ラベルのレイアウト ID :** *パレット*</span><span class="sxs-lookup"><span data-stu-id="f8bda-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="f8bda-483">**説明 :** *パレット*</span><span class="sxs-lookup"><span data-stu-id="f8bda-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="f8bda-484">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-485">アクション ウィンドウで、 **ウェーブ ラベル行の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="f8bda-486">**ウェーブ ラベル行の設定** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="f8bda-487">ここでは、ラベルの動的な部分を構成できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="f8bda-488">以下の設定を持つ行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-489">**行 Id:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="f8bda-490">**行テーブル名 :** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="f8bda-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="f8bda-491">**行の開始位置 :** *0*</span><span class="sxs-lookup"><span data-stu-id="f8bda-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="f8bda-492">このフィールドでは、ラベル上で行が開始される縦方向の位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="f8bda-493">**行の高さ :** *0*</span><span class="sxs-lookup"><span data-stu-id="f8bda-493">**Row height:** *0*</span></span>

        <span data-ttu-id="f8bda-494">このフィールドでは、ZPL 標準に従って、各行の高さをポイント数を使用して定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="f8bda-495">行の高さに使用する値は、水平ラベルの場合は正、縦方向のラベルの場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="f8bda-496">この例では行が1つしか存在しないため、この値を *0* (ゼロ) に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="f8bda-497">**ページごとの行数 :** *1*</span><span class="sxs-lookup"><span data-stu-id="f8bda-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="f8bda-498">このフィールドでは、各ラベルに印刷できる行の数を定義します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f8bda-499">この設定により、ウェーブ ラベル テーブルの各レコードに対して個別の ZPL ラベルが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="f8bda-500">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-500">Close the page.</span></span>
1. <span data-ttu-id="f8bda-501">アクション ウィンドウで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="f8bda-502">クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-503">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-504">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-505">**フィールド:** *作業タイプ*</span><span class="sxs-lookup"><span data-stu-id="f8bda-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="f8bda-506">**基準:** *ピッキング*</span><span class="sxs-lookup"><span data-stu-id="f8bda-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="f8bda-507">このクエリを実行することで、ラベルにはピックタイプの作業行のみが印刷され、プットタイプの作業行は印刷されません。</span><span class="sxs-lookup"><span data-stu-id="f8bda-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="f8bda-508">船荷証券 ID を印刷できるようにするには、 **結合** タブで **作業ライン** テーブルを選択し、 **出荷** テーブルを結合します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="f8bda-509">クエリ エディター ダイアログボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-510">**印刷テキストレイアウト** クイック タブには、 **ヘッダー セクション** 、 **ボディ セクション** 、 **フッター セクション** の3つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="f8bda-511">**ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーのコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="f8bda-512">たとえば、Zebra プリンターを使用している場合は、次のコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="f8bda-513">**ボディ セクション** セクションの **ラベル ボディ** フィールドに、必要なボディの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="f8bda-514">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="f8bda-515">**ボディ セクション** セクションの **ラベル フター** フィールドに、必要なフッターの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="f8bda-516">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="f8bda-517">この設定では、ラベルを1部ずつ印刷します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="f8bda-518">さらに多くのコピーが必要な場合 (パレットの両側に1つずつコピーする場合など) は、フッターの **\^PQn** セクションの **n** 値を必要なコピー数に設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="f8bda-519">たとえば、各ラベルを4部印刷するには、 **\^PQ4** を指定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="f8bda-520">2番目のラベルを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="f8bda-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="f8bda-521">以下の設定を持つ 3 番目のレイアウト レコードを作成します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-522">**ラベルのレイアウト ID :** *ブレイク*</span><span class="sxs-lookup"><span data-stu-id="f8bda-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="f8bda-523">**説明 :** *改ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="f8bda-524">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-525">**印刷テキストレイアウト** クイック タブには、 **ヘッダー セクション** 、 **ボディ セクション** 、 **フッター セクション** の3つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section** , **Body section** , and **Footer section**.</span></span> <span data-ttu-id="f8bda-526">**ヘッダー セクション** セクションの **ラベル ヘッダー** フィールドに必要なヘッダーの ZPL コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="f8bda-527">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="f8bda-528">今回は、ボディは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f8bda-528">This time, no body is required.</span></span> <span data-ttu-id="f8bda-529">そのため、 **フッター セクション** セクションに必要なテキストを入力するだけです。</span><span class="sxs-lookup"><span data-stu-id="f8bda-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="f8bda-530">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="f8bda-531">3番目のラベルを使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="f8bda-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-532">この 3 番目のラベルは、ラベル ロール間の区切り線として使用される改ラベルです。</span><span class="sxs-lookup"><span data-stu-id="f8bda-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="f8bda-533">2 つのウェーブ ラベル タイプを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-533">Create two wave label types</span></span>

1. <span data-ttu-id="f8bda-534">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="f8bda-535">以下の設定をしたレコードを作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-536">**ラベル タイプ :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-537">**説明 :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="f8bda-538">以下の設定を持つ 2 番目のレコードを作成します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-539">**ラベルタイプ :** *パレット*</span><span class="sxs-lookup"><span data-stu-id="f8bda-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="f8bda-540">**説明 :** *パレット*</span><span class="sxs-lookup"><span data-stu-id="f8bda-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="f8bda-541">単位順序グループを設定します</span><span class="sxs-lookup"><span data-stu-id="f8bda-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="f8bda-542">**倉庫管理 \> 設定 \> 倉庫 \> 出荷単位の順序グループ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="f8bda-543">**Ea Box PL** グループを選択、または作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="f8bda-544">**ボックス** 明細行では 、 **ウェーブ レベル タイプ** フィールドに *カートン* を設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="f8bda-545">**PL** 明細行では 、 **ウェーブ レベル タイプ** フィールドに *パレット* を設定します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="f8bda-546">ウェーブ ラベルのテンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-546">Create wave label templates</span></span>

1. <span data-ttu-id="f8bda-547">**倉庫管理 \> 設定 \> ドキュメント ルーティング \> ウェーブ ラベル テンプレート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="f8bda-548">以下の設定を持つラベル テンプレートを作成します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-549">**ラベル テンプレート名 :** *カートン ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="f8bda-550">**説明 :** *カートン ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="f8bda-551">**ウェーブ ステップ コード :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-552">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="f8bda-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f8bda-553">**一般** クイック タブの **ウェーブ ラベル タイプ** フィールドで、 *カートン* などの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="f8bda-554">**ウェーブ ラベル テンプレートの詳細** クイック タブで、以下の設定を含む新たな行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-555">**ラベルのレイアウト ID :** *カートン*</span><span class="sxs-lookup"><span data-stu-id="f8bda-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="f8bda-556">**プリンター名** 適切な ZPL プリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="f8bda-557">**クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="f8bda-558">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-559">オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="f8bda-560">**ウェーブ ラベル テンプレートの詳細** クイックタブで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="f8bda-561">続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-562">**テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-563">**派生テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-564">**フィールド :** *アカウント番号*</span><span class="sxs-lookup"><span data-stu-id="f8bda-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="f8bda-565">**条件 :** 関連する顧客アカウント番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="f8bda-566">完了後は、 **OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="f8bda-567">アクション ウィンドウで **クエリの編集** を選択して、全体のラベル テンプレートで使用するクエリ エディター ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="f8bda-568">クエリ エディター ダイアログ ボックスの **ソート** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-569">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-570">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-571">**フィールド :** *参照読み込み行の Id (レコード ID)*</span><span class="sxs-lookup"><span data-stu-id="f8bda-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="f8bda-572">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="f8bda-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="f8bda-573">以下の設定を持つ2つ目の行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-574">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-575">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-576">**フィールド:** *出荷 ID*</span><span class="sxs-lookup"><span data-stu-id="f8bda-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="f8bda-577">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="f8bda-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="f8bda-578">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-579">グループのリセット操作の確認を促すメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="f8bda-580">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="f8bda-581">アクション ウィンドウで、 **ウェーブ ラベル テンプレート グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="f8bda-582">**ウェーブ ラベル テンプレート グループ** ダイアログ ボックスで、 **参照フィールド名** フィールドが *出荷 ID* に設定されている行では、以下の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="f8bda-583">**改ラベルの印刷 :** このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f8bda-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="f8bda-584">**ラベルのレイアウト ID :** 改ラベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="f8bda-585">(たとえば、このシナリオで既に作成した *改ラベル* のレイアウトを作成します。)</span><span class="sxs-lookup"><span data-stu-id="f8bda-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="f8bda-586">**プリンター名 :** 改ラベルで使用するプリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="f8bda-587">(通常、ラベル ロールを分割する目的で、 **ウェーブ ラベル テンプレートの詳細** クイックタブで選択されているものと同じプリンタを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="f8bda-588">しかし、他のシナリオにも適用可能です。)</span><span class="sxs-lookup"><span data-stu-id="f8bda-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="f8bda-589">**参照フィールド名** フィールドが、 *参照積荷行 ID*  に設定されている行では、 **ラベルビルド ID** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-589">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-590">この設定では、作業グループの設定に関係なく、ウェーブ全体で各積荷ラインごとに 1 つのラベル シーケンス（"カートン X のうちの 1"）を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="f8bda-591">このラベル シーケンスは、ラベル レイアウトに印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="f8bda-592">また、異なる出荷のラベルは、選択された改ラベルで区切られます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="f8bda-593">**OK** を選択して、 **ウェーブ ラベル テンプレート グループ** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="f8bda-594">以下の設定を持つ 2 つ目のラベル テンプレートを作成します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-595">**ラベル テンプレート名 :** *パレット ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="f8bda-596">**説明 :** *パレット ラベル*</span><span class="sxs-lookup"><span data-stu-id="f8bda-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="f8bda-597">**ウェーブ ステップ コード :** *パレット*</span><span class="sxs-lookup"><span data-stu-id="f8bda-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="f8bda-598">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="f8bda-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f8bda-599">**一般** クイック タブの **ウェーブ ラベル タイプ** フィールドで、 *パレット* などの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="f8bda-600">**ウェーブ ラベル テンプレートの詳細** クイック タブで、以下の設定を含む新たな行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-601">**ラベルのレイアウト ID :** *パレット*</span><span class="sxs-lookup"><span data-stu-id="f8bda-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="f8bda-602">**プリンター名** 適切な ZPL プリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="f8bda-603">**クエリの実行 :** *はい* (この設定はオプションですが、最適なパフォーマンスを実現するにあたって推奨します)。</span><span class="sxs-lookup"><span data-stu-id="f8bda-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="f8bda-604">アクション ウィンドウで、 **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="f8bda-605">オプション : 顧客固有のラベル デザインを設定している場合は、顧客のアカウントを検索するクエリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="f8bda-606">**ウェーブ ラベル テンプレートの詳細** クイックタブで、 **クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="f8bda-607">続いて、クエリ エディター ダイアログ ボックスの **範囲** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-608">**テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-609">**派生テーブル:** *出荷*</span><span class="sxs-lookup"><span data-stu-id="f8bda-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="f8bda-610">**フィールド :** *アカウント番号*</span><span class="sxs-lookup"><span data-stu-id="f8bda-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="f8bda-611">**条件 :** 関連する顧客アカウント番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="f8bda-612">完了後は、 **OK** を選択して、クエリ エディタ ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="f8bda-613">アクション ウィンドウで **クエリの編集** を選択して、全体のラベル テンプレートで使用するクエリ エディター ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="f8bda-614">クエリ エディター ダイアログ ボックスの **ソート** タブで、以下の設定のある行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-615">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-616">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-617">**フィールド :** *参照読み込み行の Id (レコード ID)*</span><span class="sxs-lookup"><span data-stu-id="f8bda-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="f8bda-618">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="f8bda-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="f8bda-619">以下の設定を持つ2つ目の行を追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-620">**表:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-621">**派生テーブル:** *作業明細行*</span><span class="sxs-lookup"><span data-stu-id="f8bda-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="f8bda-622">**フィールド:** *出荷 ID*</span><span class="sxs-lookup"><span data-stu-id="f8bda-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="f8bda-623">**検索の方法:** *昇順*</span><span class="sxs-lookup"><span data-stu-id="f8bda-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="f8bda-624">**OK** を選択してクエリ エディター ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="f8bda-625">グループのリセット操作の確認を促すメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="f8bda-626">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="f8bda-627">アクション ウィンドウで、 **ウェーブ ラベル テンプレート グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="f8bda-628">**ウェーブ ラベル テンプレート グループ** ダイアログ ボックスで、 **参照フィールド名** フィールドが *出荷 ID* に設定されている行では、以下の値を設定します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID* , set the following values:</span></span>

    - <span data-ttu-id="f8bda-629">**改ラベルの印刷 :** このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="f8bda-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="f8bda-630">**ラベルのレイアウト ID :** 改ラベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="f8bda-631">(たとえば、このシナリオで既に作成した *改ラベル* のレイアウトを作成します。)</span><span class="sxs-lookup"><span data-stu-id="f8bda-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="f8bda-632">**プリンター名 :** 改ラベルで使用するプリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="f8bda-633">(通常、ラベル ロールを分割する目的で、 **ウェーブ ラベル テンプレートの詳細** クイックタブで選択されているものと同じプリンタを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="f8bda-634">しかし、他のシナリオにも適用可能です。)</span><span class="sxs-lookup"><span data-stu-id="f8bda-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="f8bda-635">**参照フィールド名** フィールドが、 *参照積荷行 ID*  に設定されている行では、 **ラベルビルド ID** チェックボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-635">For the row where the **Reference field name** field is set to *Reference load line id* , select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-636">この設定では、作業グループの設定に関係なく、ウェーブ全体で各積荷ラインごとに 1 つのラベル シーケンス（"カートン X のうちの 1"）を作成します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="f8bda-637">このラベル シーケンスは、ラベル レイアウトに印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="f8bda-638">また、異なる出荷のラベルは、選択された改ラベルで区切られます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="f8bda-639">シーケンス番号の拡張機能を構成する</span><span class="sxs-lookup"><span data-stu-id="f8bda-639">Configure number sequence extensions</span></span>

<span data-ttu-id="f8bda-640">シーケンス番号の拡張機能は、特定のシーケンス番号の GS1 コンプライアンスを制御します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="f8bda-641">この構成は、こののシナリオでは任意となります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="f8bda-642">詳細情報と構成についての手順については、[シーケンス番号拡張機能の構成](../warehousing/configure-number-sequence-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="f8bda-643">販売注文を作成して倉庫にリリースする</span><span class="sxs-lookup"><span data-stu-id="f8bda-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="f8bda-644">**販売とマーケティング \> 販売注文 \> すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="f8bda-645">以下の設定で販売注文を作成します:</span><span class="sxs-lookup"><span data-stu-id="f8bda-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="f8bda-646">**顧客アカウント:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="f8bda-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="f8bda-647">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="f8bda-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="f8bda-648">販売注文明細行を2行追加します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="f8bda-649">販売注文明細行 1:</span><span class="sxs-lookup"><span data-stu-id="f8bda-649">Sales order line 1:</span></span>

        - <span data-ttu-id="f8bda-650">**品目番号:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="f8bda-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="f8bda-651">**数量:** *9024*</span><span class="sxs-lookup"><span data-stu-id="f8bda-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="f8bda-652">**出荷単位 :** *ea* (9024 ea = 376 Box = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="f8bda-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="f8bda-653">販売注文明細行 2:</span><span class="sxs-lookup"><span data-stu-id="f8bda-653">Sales order line 2:</span></span>

        - <span data-ttu-id="f8bda-654">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="f8bda-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="f8bda-655">**数量:** *9016*</span><span class="sxs-lookup"><span data-stu-id="f8bda-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="f8bda-656">**出荷単位 :** *ea* (9016 ea = 322 Box = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="f8bda-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8bda-657">ここで扱っている項目や数量はあくまでも一例です。</span><span class="sxs-lookup"><span data-stu-id="f8bda-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="f8bda-658">前述の手順で定義した出荷単位のシーケンス グループを使用し、 *ea* から *Box* および *PL* への適切な単位変換を定義し、倉庫 *62* に在庫がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="f8bda-659">詳細については、[測定単位と在庫のポリシー](unit-measure-stocking-policies.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8bda-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="f8bda-660">販売注文明細行 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-660">Select sales order line 1.</span></span> <span data-ttu-id="f8bda-661">続いて、 **在庫** メニューの **販売注文明細行** セクションで、 **引当** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="f8bda-662">**引当** ページの、アクション ウィンドウで **ロットの引当** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-662">On the **Reservation** page, on the Action Pane, select **Reserve lot** , and then close the page.</span></span>
1. <span data-ttu-id="f8bda-663">販売注文明細行 2 については、手順 4 と 5 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="f8bda-664">アクション ウィンドウの **倉庫** タブで、 **倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="f8bda-665">以下のイベントが発生します :</span><span class="sxs-lookup"><span data-stu-id="f8bda-665">The following events occur:</span></span> 

    - <span data-ttu-id="f8bda-666">システムは、ラベル印刷の手順を含むテンプレートを使用して、作成された出荷を処理します。</span><span class="sxs-lookup"><span data-stu-id="f8bda-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="f8bda-667">ラベルのレイアウトはラベル フォーマットの定義に使用され、ラベル テンプレートで選択されたプリンタで印刷されるラベルとなります。</span><span class="sxs-lookup"><span data-stu-id="f8bda-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="f8bda-668">ウェーブ ラベルが生成され、印刷されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="f8bda-669">ラベルの数は、カートンの数と等しくなります (例 : 1行目の 376 ボック スラベル、2行目の 322 ボックス ラベル、1行目の 47 PL ラベル、2行目の 47 PLラベル、出荷 ID を持つ2つの改ラベル) 。</span><span class="sxs-lookup"><span data-stu-id="f8bda-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="f8bda-670">出荷に対して新たな船荷証券 ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="f8bda-671">シーケンス番号の拡張機能を構成した場合、ウェーブ ラベル ID は **SSCC-18** の番号形式に従います。</span><span class="sxs-lookup"><span data-stu-id="f8bda-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="f8bda-672">以下のページでは、ウェーブ ラベルを表示、再印刷ができます :</span><span class="sxs-lookup"><span data-stu-id="f8bda-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="f8bda-673">すべての出荷 \> 出荷詳細</span><span class="sxs-lookup"><span data-stu-id="f8bda-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="f8bda-674">すべての貨物 \> 貨物の詳細</span><span class="sxs-lookup"><span data-stu-id="f8bda-674">All loads \> Load details</span></span>
- <span data-ttu-id="f8bda-675">すべてのウェーブ</span><span class="sxs-lookup"><span data-stu-id="f8bda-675">All waves</span></span>
- <span data-ttu-id="f8bda-676">ウェーブ ラベル</span><span class="sxs-lookup"><span data-stu-id="f8bda-676">Wave labels</span></span>
- <span data-ttu-id="f8bda-677">ウェーブ ラベル履歴</span><span class="sxs-lookup"><span data-stu-id="f8bda-677">Wave label history</span></span>

<span data-ttu-id="f8bda-678">これらのほとんどのページでは、アクションウィンドウの **出荷** タブにある **関連情報** グループの **ウェーブラベル** を選択することにより、関連する機能を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f8bda-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>
