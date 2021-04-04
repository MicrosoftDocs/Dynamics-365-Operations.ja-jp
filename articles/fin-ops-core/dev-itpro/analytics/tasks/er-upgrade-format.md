---
title: ER 形式の新しい基準バージョンを採用してその形式をアップグレードする
description: このトピックでは、電子申告 (ER) 形式のコンフィギュレーションを管理する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 336551f4e9858269010ec7debd1750a8d8453163
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564245"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a><span data-ttu-id="98d61-103">ER 形式の新しい基準バージョンを採用してその形式をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="98d61-103">ER Upgrade your format by adopting a new, base version of that format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98d61-104">次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションを維持管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="98d61-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can maintain an Electronic reporting (ER) format configuration.</span></span> <span data-ttu-id="98d61-105">この手順では、コンフィギュレーション プロバイダー (CP) から受領した形式を基にカスタム バージョンの形式を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="98d61-105">This procedure explains how a custom version of a format can be created based on the format received from a configuration provider (CP).</span></span> <span data-ttu-id="98d61-106">また、その形式の新しい基準バージョンの採用方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="98d61-106">It also explains how to adopt a new, base version of that format.</span></span>

<span data-ttu-id="98d61-107">これらのステップを完了するには、まず 「構成プロバイダーを作成し、有効としてマークする 」 に記載の手順、および 「作成済みの形式を使用して支払用の電子ドキュメントを生成する」 に記載の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d61-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" and "Use created format to generate electronic documents for payments" procedures.</span></span> <span data-ttu-id="98d61-108">これらのステップは GBSI 会社で実行できます。</span><span class="sxs-lookup"><span data-stu-id="98d61-108">These steps can be performed in the GBSI company.</span></span>

## <a name="select-format-configuration-for-customization"></a><span data-ttu-id="98d61-109">カスタマイズする形式のコンフィギュレーションを選択</span><span class="sxs-lookup"><span data-stu-id="98d61-109">Select format configuration for customization</span></span>
1. <span data-ttu-id="98d61-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="98d61-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="98d61-111">この例では、サンプル会社 Litware, Inc. (https://www.litware.com) が特定の国に対する電子支払の形式コンフィギュレーションをサポートするコンフィギュレーション プロバイダーとして機能します。</span><span class="sxs-lookup"><span data-stu-id="98d61-111">In this example, sample company Litware, Inc. (https://www.litware.com) will act as a configuration provider that supports format configurations for electronic payments for a particular country.</span></span>    <span data-ttu-id="98d61-112">サンプル会社 Proseware, Inc. (http://www.proseware.com) は、Liteware, Inc. が提供した形式コンフィギュレーションの消費者として機能します。</span><span class="sxs-lookup"><span data-stu-id="98d61-112">Sample company Proseware, Inc. (http://www.proseware.com) will act as a consumer of the format configuration that Litware, Inc. provided.</span></span> <span data-ttu-id="98d61-113">Proseware, Inc. はその国の特定の地域の形式を使用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-113">Proseware, Inc. uses formats in certain regions of that country.</span></span>  
2. <span data-ttu-id="98d61-114">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-114">Click Reporting configurations.</span></span>
3. <span data-ttu-id="98d61-115">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-115">Click Show filters.</span></span>
4. <span data-ttu-id="98d61-116">「名前」フィールドで「次の値で始まる」フィルター演算子を使用して、値「BACS (英国企業)」でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-116">Apply the following filters: Enter a filter value of "BACS (UK fictitious)" on the "Name" field using the "begins with" filter operator.</span></span>
  
    <span data-ttu-id="98d61-117">選択された形式のコンフィギュレーション BACS (英国企業) は、プロバイダーである Litware, Inc. が所有しています。</span><span class="sxs-lookup"><span data-stu-id="98d61-117">The selected format configuration BACS (UK fictitious) is owned by provider Litware, Inc.</span></span>  

5. <span data-ttu-id="98d61-118">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-118">Click Show filters.</span></span>
6. <span data-ttu-id="98d61-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-119">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="98d61-120">[完了] 状態の形式のバージョンは、カスタマイズ用に Proseware Inc. で使用されます 。</span><span class="sxs-lookup"><span data-stu-id="98d61-120">The version of the format with the status of Completed will be used by Proseware, Inc. for customization.</span></span>  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a><span data-ttu-id="98d61-121">電子ドキュメントのカスタム形式の新規コンフィギュレーションを作成</span><span class="sxs-lookup"><span data-stu-id="98d61-121">Create a new configuration for your custom format of electronic document</span></span>
<span data-ttu-id="98d61-122">Proseware、Inc. は、自身のサービスの定期売買に従って電子支払ドキュメントを生成するための初期形式が含まれている BACS (英国企業) コンフィギュレーションの バージョン 1.1 を受領済です。</span><span class="sxs-lookup"><span data-stu-id="98d61-122">Proseware, Inc. received version 1.1 of BACS (UK fictitious) configuration that contains the initial format to generate electronic payment documents from Litware, Inc. in accordance to their service subscription.</span></span> <span data-ttu-id="98d61-123">Proseware, Inc. は、これを自身の国の標準として使い始めようとしますが、特定の地域の要件をサポートするためのカスタマイズが必要です。</span><span class="sxs-lookup"><span data-stu-id="98d61-123">Proseware, Inc. wants to start using this as a standard for their country but some customization is required to support specific regional requirements.</span></span> <span data-ttu-id="98d61-124">Proseware, Inc. は、その新しいバージョン (新しい国固有の要件をサポートするための変更を含む) が Litware, Inc. からリリースされ次第、カスタム形式をアップグレードする能力も維持したいと考えています。さらに、このアップグレードを最低限の費用で実行したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="98d61-124">Proseware, Inc. also wants to keep the ability to upgrade a custom format as soon as a new version of it (with changes to support new country-specific requirements) comes from Litware, Inc. and they want to perform this upgrade with the lowest cost.</span></span>  

<span data-ttu-id="98d61-125">これを実現するため Proseware, Inc. は、基準として Litware, Inc. のコンフィギュレーション BACS (英国企業) を使用してコンフィギュレーションを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d61-125">To do this, Proseware, Inc. needs to create a configuration using the Litware, Inc. configuration BACS (UK fictitious) as a base.</span></span>  

1. <span data-ttu-id="98d61-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="98d61-126">Close the page.</span></span>
2. <span data-ttu-id="98d61-127">Proseware, Inc を選択して 有効なプロバイダーとします。</span><span class="sxs-lookup"><span data-stu-id="98d61-127">Select Proseware, Inc. to make it an active provider.</span></span>
3. <span data-ttu-id="98d61-128">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-128">Click Set active.</span></span>
4. <span data-ttu-id="98d61-129">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-129">Click Reporting configurations.</span></span>
5. <span data-ttu-id="98d61-130">ツリーで、「支払 (単純化モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-130">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="98d61-131">ツリーで、「支払 (単純化モデル)」 \BACS (英国の企業) を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-131">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="98d61-132">Litware, Inc. から BACS (英国企業) 構成を選択します。Proseware, Inc. は、バージョン 1.1 をカスタム バージョンの基準として使用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-132">Select the BACS (UK fictitious) configuration from Litware, Inc. Proseware, Inc. will use version 1.1 as a base for the custom version.</span></span>  

7. <span data-ttu-id="98d61-133">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="98d61-133">Click Create configuration to open the drop dialog.</span></span>

    <span data-ttu-id="98d61-134">これにより、カスタムの支払形式用の新しいコンフィギュレーションを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="98d61-134">This lets you create a new configuration for a custom payment format.</span></span>  

8. <span data-ttu-id="98d61-135">[新規] フィールドに「Derive from Name: BACS (英国の企業)、Litware, Inc.」と入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-135">In the New field, enter 'Derive from Name: BACS (UK fictitious), Litware, Inc.'.</span></span>

    <span data-ttu-id="98d61-136">[派生] オプションを選択して、カスタム バージョンを作成する基準として BACS (英国企業) の使用を確認します。</span><span class="sxs-lookup"><span data-stu-id="98d61-136">Select the Derive option to confirm the usage of BACS (UK fictitious) as the base for creating the custom version.</span></span>  

9. <span data-ttu-id="98d61-137">[名前] フィールドに、「BACS (英国関税)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-137">In the Name field, type 'BACS (UK fictitious custom)'.</span></span>
10. <span data-ttu-id="98d61-138">[説明] フィールドに、「BACS の仕入先支払 (英国関税) 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-138">In the Description field, type 'BACS vendor payment (UK fictitious custom)'.</span></span>

    <span data-ttu-id="98d61-139">ここでは、有効なコンフィギュレーション プロバイダー (Proseware, Inc.) が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="98d61-139">The active configuration provider (Proseware, Inc.) is automatically entered here.</span></span> <span data-ttu-id="98d61-140">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="98d61-140">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="98d61-141">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="98d61-141">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

11. <span data-ttu-id="98d61-142">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-142">Click Create configuration.</span></span>

## <a name="customize-your-format-for-the-electronic-document"></a><span data-ttu-id="98d61-143">電子ドキュメントの形式のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="98d61-143">Customize your format for the electronic document</span></span>
1. <span data-ttu-id="98d61-144">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-144">Click Designer.</span></span>
2. <span data-ttu-id="98d61-145">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-145">Click Expand/collapse.</span></span>
3. <span data-ttu-id="98d61-146">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-146">Click Expand/collapse.</span></span>
4. <span data-ttu-id="98d61-147">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="98d61-148">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="98d61-148">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="98d61-149">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-149">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="98d61-150">[名前] フィールドに、「IBAN」と入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-150">In the Name field, type 'IBAN'.</span></span>
8. <span data-ttu-id="98d61-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-151">Click OK.</span></span>
9. <span data-ttu-id="98d61-152">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\IBAN」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-152">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\IBAN'.</span></span>
10. <span data-ttu-id="98d61-153">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="98d61-153">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="98d61-154">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-154">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="98d61-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-155">Click OK.</span></span>
13. <span data-ttu-id="98d61-156">ツリーで、「Xml\Message\Payments\Item\Vendor\Name\String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-156">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="98d61-157">[最大の長さ] フィールドに「60」を入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-157">In the Maximum length field, enter '60'.</span></span>
15. <span data-ttu-id="98d61-158">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-158">Click the Mapping tab.</span></span>
16. <span data-ttu-id="98d61-159">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-159">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="98d61-160">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-160">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="98d61-161">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-161">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="98d61-162">ツリーで、[model\Payments\Creditor\Account] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-162">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
20. <span data-ttu-id="98d61-163">ツリーで、「model\Payments\Creditor\Account\IBAN」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-163">In the tree, select 'model\Payments\Creditor\Account\IBAN'.</span></span>
21. <span data-ttu-id="98d61-164">ツリーで、「Xml\Message\Payments\Item = model.Payments\Vendor\Bank\IBAN\String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-164">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\IBAN\String'.</span></span>
22. <span data-ttu-id="98d61-165">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-165">Click Bind.</span></span>
23. <span data-ttu-id="98d61-166">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-166">Click Save.</span></span>

## <a name="validate-the-customized-format"></a><span data-ttu-id="98d61-167">カスタマイズされた形式の検証</span><span class="sxs-lookup"><span data-stu-id="98d61-167">Validate the customized format</span></span>
1. <span data-ttu-id="98d61-168">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-168">Click Validate.</span></span>

    <span data-ttu-id="98d61-169">すべてのバインディングに問題がないことを確認するために、カスタマイズされた形式レイアウトおよびデータ マッピングの変更を検証します。</span><span class="sxs-lookup"><span data-stu-id="98d61-169">Validate the customized format layout and data mapping changes to make sure that all bindings are okay.</span></span>  

2. <span data-ttu-id="98d61-170">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="98d61-170">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a><span data-ttu-id="98d61-171">カスタム形式のコンフィギュレーションの現行バージョンの状態を変更</span><span class="sxs-lookup"><span data-stu-id="98d61-171">Change the status of the current version of the custom format configuration</span></span>
<span data-ttu-id="98d61-172">支払ドキュメントの生成に使用できるように、指定の形式のコンフィギュレーションの状態を [ドラフト] から [完了] に変更します。</span><span class="sxs-lookup"><span data-stu-id="98d61-172">Change the status of the designed format configuration from Draft to Completed to make it available for payment document generation.</span></span>  

1. <span data-ttu-id="98d61-173">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-173">Click Change status.</span></span>

    <span data-ttu-id="98d61-174">選択したコンフィギュレーションの現在のバージョンが [ドラフト] 状態であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-174">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="98d61-175">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-175">Click Complete.</span></span>
3. <span data-ttu-id="98d61-176">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-176">In the Description field, type a value.</span></span>
4. <span data-ttu-id="98d61-177">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-177">Click OK.</span></span>
5. <span data-ttu-id="98d61-178">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-178">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="98d61-179">作成したコンフィギュレーションが完了したバージョン 1.1.1 として保存されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-179">Note that the created configuration is saved as completed version 1.1.1.</span></span> <span data-ttu-id="98d61-180">これは、BACS の関税 (英国企業の関税) 形式のバージョン 1 であることを意味します。これは BACS (英国企業) 形式のバージョン 1、および支払 (単純化モデル) データ モデルのバージョン 1 に基づきます。</span><span class="sxs-lookup"><span data-stu-id="98d61-180">This means it is version 1 of the custom BACS (UK fictitious custom) format, which is based on version 1 of the BACS (UK fictitious) format, which is based on version 1 of the Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-to-generate-payment-files"></a><span data-ttu-id="98d61-181">カスタマイズされた形式の支払ファイル生成テストの実行</span><span class="sxs-lookup"><span data-stu-id="98d61-181">Test the customized format to generate payment files</span></span>
<span data-ttu-id="98d61-182">並列する Finance and Operations のセッションで 「作成した形式を使用して支払い用の電子文書を生成する」 の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="98d61-182">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in a parallel Finance and Operations session.</span></span> <span data-ttu-id="98d61-183">電子支払方法のパラメーターで BACS (英国関税) 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-183">Select the BACS (UK fictitious custom) format in electronic payment method parameters.</span></span> <span data-ttu-id="98d61-184">作成した支払ファイルに、地域要件に対応した IBAN コードを表す最新の XML ノードが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="98d61-184">Make sure that the created payment file contains the recently introduced XML node presenting IBAN code in accordance to regional requirements.</span></span>  

## <a name="update-the-existing-country-specific-configuration"></a><span data-ttu-id="98d61-185">既存の国固有のコンフィギュレーションの更新</span><span class="sxs-lookup"><span data-stu-id="98d61-185">Update the existing country-specific configuration</span></span>
<span data-ttu-id="98d61-186">電子ドキュメントの形式を管理するために、Litware, Inc. は BACS (英国の企業) コンフィギュレーションを更新し、新しい国要件を採用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d61-186">Litware, Inc. needs to update the BACS (UK fictitious) configuration and adopt new country requirements for managing the format of the electronic document.</span></span> <span data-ttu-id="98d61-187">これは後に、Proseware, Inc. を含むサービスのサブスクライバーに提供される、このコンフィギュレーションの新しいバージョンに取り入れられます。</span><span class="sxs-lookup"><span data-stu-id="98d61-187">Later, this will be enclosed in a new version of this configuration that will be offered for service subscribers, including Proseware, Inc.</span></span>  

<span data-ttu-id="98d61-188">実際のサービス提供に関連するプロセスにおいては、BACS（イギリスの架空の企業） のそれぞれの新たなバージョンを、Litware, Inc. 構成の LCS レポジトリからインポートできます。</span><span class="sxs-lookup"><span data-stu-id="98d61-188">In real service provision related processes, each new version of BACS (UK fictitious) can be imported by Proseware, Inc. from Litware, Inc. configurations' LCS repository.</span></span> <span data-ttu-id="98d61-189">本手順では、サービス プロバイダーに代わり BACS (英国の企業) を更新してこれをシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="98d61-189">In this procedure we will simulate this by updating BACS (UK fictitious) on behalf of a service provider.</span></span>  

1. <span data-ttu-id="98d61-190">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="98d61-190">Close the page.</span></span>
2. <span data-ttu-id="98d61-191">Litware, Inc. の選択 プロバイダー</span><span class="sxs-lookup"><span data-stu-id="98d61-191">Select Litware, inc. provider.</span></span>
3. <span data-ttu-id="98d61-192">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-192">Click Set active.</span></span>
4. <span data-ttu-id="98d61-193">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-193">Click Reporting configurations.</span></span>
5. <span data-ttu-id="98d61-194">ツリーで、「支払 (単純化モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-194">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="98d61-195">ツリーで、「支払 (単純化モデル)」 \BACS (英国の企業) を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-195">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>

    <span data-ttu-id="98d61-196">Litware、Inc. が所有する プロバイダー BACKS (英国企業) のドラフト バージョンは、国固有の新しい要件をサポートする変更点を取り入れるため選択されます。</span><span class="sxs-lookup"><span data-stu-id="98d61-196">The draft version owned by Litware, Inc. provider BACS (UK fictitious) is selected to bring in changes to support new country-specific requirements.</span></span>  

## <a name="localize-the-base-format-of-the-electronic-document"></a><span data-ttu-id="98d61-197">電子ドキュメントの基準形式のローカライズ</span><span class="sxs-lookup"><span data-stu-id="98d61-197">Localize the base format of the electronic document</span></span>
<span data-ttu-id="98d61-198">Litware, Inc. によりサポートされる国固有の新しい要件があると想定します。</span><span class="sxs-lookup"><span data-stu-id="98d61-198">Assume that there are new country-specific requirements to be supported by Litware, Inc.:</span></span>  

- <span data-ttu-id="98d61-199">各支払取引における債権者の銀行の SWIFT コードの値。</span><span class="sxs-lookup"><span data-stu-id="98d61-199">A value for the creditor's bank SWIFT code in each payment transaction.</span></span>
- <span data-ttu-id="98d61-200">生成ファイルでの仕入先名のテキストの長さは 100 文字以内に制限されます。</span><span class="sxs-lookup"><span data-stu-id="98d61-200">A limit of 100 characters for the length of text for the vendor's name in a generating file.</span></span>  
- <span data-ttu-id="98d61-201">国固有の新しい要件</span><span class="sxs-lookup"><span data-stu-id="98d61-201">New country-specific requirements</span></span>  
- <span data-ttu-id="98d61-202">必要な変更を取り入れるため、必要なコンフィギュレーションのドラフト バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-202">Select the draft version of the desired configuration to introduce required changes.</span></span>  


1. <span data-ttu-id="98d61-203">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-203">Click Designer.</span></span>
2. <span data-ttu-id="98d61-204">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-204">Click Expand/collapse.</span></span>
3. <span data-ttu-id="98d61-205">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-205">Click Expand/collapse.</span></span>
4. <span data-ttu-id="98d61-206">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-206">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
5. <span data-ttu-id="98d61-207">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="98d61-207">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="98d61-208">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-208">In the tree, select 'XML\Element'.</span></span>
7. <span data-ttu-id="98d61-209">[名前] フィールドに、「SWIFT」と入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-209">In the Name field, type 'SWIFT'.</span></span>
8. <span data-ttu-id="98d61-210">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-210">Click OK.</span></span>
9. <span data-ttu-id="98d61-211">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\SWIFT」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-211">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\SWIFT'.</span></span>
10. <span data-ttu-id="98d61-212">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="98d61-212">Click Add to open the drop dialog.</span></span>
11. <span data-ttu-id="98d61-213">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-213">In the tree, select 'Text\String'.</span></span>
12. <span data-ttu-id="98d61-214">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-214">Click OK.</span></span>
13. <span data-ttu-id="98d61-215">ツリーで、「Xml\Message\Payments\Item\Vendor\Name\String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-215">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
14. <span data-ttu-id="98d61-216">[最大の長さ] フィールドに「100」を入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-216">In the Maximum length field, enter '100'.</span></span>
15. <span data-ttu-id="98d61-217">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-217">Click the Mapping tab.</span></span>
16. <span data-ttu-id="98d61-218">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-218">In the tree, expand 'model'.</span></span>
17. <span data-ttu-id="98d61-219">ツリーで、[model\Payments] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-219">In the tree, expand 'model\Payments'.</span></span>
18. <span data-ttu-id="98d61-220">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-220">In the tree, expand 'model\Payments\Creditor'.</span></span>
19. <span data-ttu-id="98d61-221">ツリーで、[model\Payments\Creditor\Agent] を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-221">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
20. <span data-ttu-id="98d61-222">ツリーで、「model\Payments\Creditor\Agent\SWIFT」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-222">In the tree, select 'model\Payments\Creditor\Agent\SWIFT'.</span></span>
21. <span data-ttu-id="98d61-223">ツリーで、「Xml\Message\Payments\Item = model.Payments\Vendor\Bank\SWIFT\String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-223">In the tree, select 'Xml\Message\Payments\Item =  model.Payments\Vendor\Bank\SWIFT\String'.</span></span>
22. <span data-ttu-id="98d61-224">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-224">Click Bind.</span></span>
23. <span data-ttu-id="98d61-225">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-225">Click Save.</span></span>

## <a name="validate-the-localized-format"></a><span data-ttu-id="98d61-226">ローカライズされた形式の検証</span><span class="sxs-lookup"><span data-stu-id="98d61-226">Validate the localized format</span></span>
1. <span data-ttu-id="98d61-227">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-227">Click Validate.</span></span>
2. <span data-ttu-id="98d61-228">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="98d61-228">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a><span data-ttu-id="98d61-229">基準形式のコンフィギュレーションの現行バージョンの状態を変更</span><span class="sxs-lookup"><span data-stu-id="98d61-229">Change the status of the current version of the base format configuration</span></span>
<span data-ttu-id="98d61-230">支払ドキュメントの生成および、そこから派生する形式のコンフィギュレーションの更新に使用できるよう、更新された基準形式のコンフィギュレーションの状態を [ドラフト] から [完了] に変更します。</span><span class="sxs-lookup"><span data-stu-id="98d61-230">Change the status of the updated base format configuration from Draft to Completed to make it available for generation of payment documents and updates of format configurations derived from it.</span></span>  

1. <span data-ttu-id="98d61-231">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-231">Click Change status.</span></span>

    <span data-ttu-id="98d61-232">選択したコンフィギュレーションの現在のバージョンが [ドラフト] 状態であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-232">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="98d61-233">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-233">Click Complete.</span></span>
3. <span data-ttu-id="98d61-234">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-234">In the Description field, type a value.</span></span>
4. <span data-ttu-id="98d61-235">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-235">Click OK.</span></span>
5. <span data-ttu-id="98d61-236">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-236">In the list, find and select the desired record.</span></span>

## <a name="change-the-base-version-for-the-custom-format-configuration"></a><span data-ttu-id="98d61-237">カスタム形式のコンフィギュレーションの基準バージョンの変更</span><span class="sxs-lookup"><span data-stu-id="98d61-237">Change the base version for the custom format configuration</span></span>

<span data-ttu-id="98d61-238">Proseware, Inc. は最近発表された国固有の要件に従った電子支払ドキュメントの生成に使用できる BACS (英国の企業) コンフィギュレーションの新しいバージョン 1.2 が使用できることを通知されています。</span><span class="sxs-lookup"><span data-stu-id="98d61-238">Proseware, Inc. is informed that a new version 1.2 of BACS (UK fictitious) configuration is available to generate electronic payment documents in accordance to recently announced country-specific requirements.</span></span> <span data-ttu-id="98d61-239">Proseware, Inc. は国の標準としてこの使用を開始することを考えています。</span><span class="sxs-lookup"><span data-stu-id="98d61-239">Proseware, Inc. wants to start using it as a standard for the country.</span></span>  

<span data-ttu-id="98d61-240">これを実現するには、Proseware, Inc. はカスタム コンフィギュレーション BACS (英国関税) の基準コンフィギュレーション バージョンを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d61-240">To do this, Proseware, Inc. needs to change the base configuration version for the custom configuration BACS (UK fictitious custom).</span></span> <span data-ttu-id="98d61-241">BACS (英国の企業) のバージョン 1.1 の代わりに 1.2 を使用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-241">Instead of version 1.1 of BACS (UK fictitious) use new version 1.2.</span></span>  

1. <span data-ttu-id="98d61-242">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="98d61-242">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="98d61-243">Proseware, Inc. プロバイダーを選択し、有効なプロバイダーとしてマーク付けします。</span><span class="sxs-lookup"><span data-stu-id="98d61-243">Select the Proseware, Inc. provider to mark it as active.</span></span>
3. <span data-ttu-id="98d61-244">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-244">Click Set active.</span></span>
4. <span data-ttu-id="98d61-245">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-245">Click Reporting configurations.</span></span>
5. <span data-ttu-id="98d61-246">ツリーで、「支払 (単純化モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-246">In the tree, expand 'Payments (simplified model)'.</span></span>
6. <span data-ttu-id="98d61-247">ツリーで、「支払 (単純化モデル)」 \BACS (英国の企業)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="98d61-247">In the tree, expand 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
7. <span data-ttu-id="98d61-248">ツリーで、「支払 (単純化モデル)\BACS (英国の企業)\BACS (英国関税)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-248">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.</span></span>

    <span data-ttu-id="98d61-249">Proseware, Inc. が所有する BACS (英国関税) コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-249">Select the BACS (UK fictitious custom) configuration, which is owned by Proseware, Inc.</span></span>  

    <span data-ttu-id="98d61-250">必要な変更を取り入れるため、選択したコンフィギュレーションのドラフト バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-250">Use the draft version of the selected configuration to introduce required changes.</span></span>  

8. <span data-ttu-id="98d61-251">[再ベース] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-251">Click Rebase.</span></span>

    <span data-ttu-id="98d61-252">コンフィギュレーションを更新する新しい基準として適用されるよう、基準コンフィギュレーションの新しいバージョン 1.2 を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-252">Select the new version 1.2 of the base configuration to be applied as a new base for updating the configuration.</span></span>  

9. <span data-ttu-id="98d61-253">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-253">Click OK.</span></span>

    <span data-ttu-id="98d61-254">カスタム バージョンをマージすると、自動的にマージできない一部のフォーマット変更を表す新しいベース バージョンとの間で競合が検出されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-254">Note that some conflicts have been discovered between merging the custom version and a new base version representing some format changes that can't be merged automatically.</span></span>  

## <a name="resolve-rebase-conflicts"></a><span data-ttu-id="98d61-255">再ベースの競合の解決</span><span class="sxs-lookup"><span data-stu-id="98d61-255">Resolve rebase conflicts</span></span>
1. <span data-ttu-id="98d61-256">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-256">Click Designer.</span></span>
    
    <span data-ttu-id="98d61-257">仕入先名のテキストの長さ制限の変更を自動的に解決できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-257">Note that changes to the vendor's name text length limit couldn't be resolved automatically.</span></span> <span data-ttu-id="98d61-258">したがって、これは競合の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="98d61-258">Therefore, this is presented in a conflicts list.</span></span> <span data-ttu-id="98d61-259">タイプの更新の各競合に対して、次のオプションが使用できます: - 前の基準値を適用して (グリッド上部にあるボタンを使用)、前の基準バージョンの値 (このケースでは 0) を用いる。</span><span class="sxs-lookup"><span data-stu-id="98d61-259">For each conflict of type Update, the following options are available:  - Apply a prior base value (button on top of the grid) to bring in the previous base version value (0 in our case).</span></span>  <span data-ttu-id="98d61-260">- 基準値を適用して (グリッド上部にあるボタンを使用)、新しいバージョンの値 (このケースでは 100) を用いる。</span><span class="sxs-lookup"><span data-stu-id="98d61-260">- Apply a base value (button on top of the grid) to bring in the new base version value (100 in our case).</span></span>  <span data-ttu-id="98d61-261">- 独自 (カスタム) の値 (ここでは 60) を保持します。</span><span class="sxs-lookup"><span data-stu-id="98d61-261">- Keep your own (custom) value (60 in our case).</span></span>  <span data-ttu-id="98d61-262">[基準値の適用] をクリックし、仕入先名のテキストの長さに国固有の 100 文字の制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-262">Click Apply base value to apply a country-specific limit of 100 characters for vendor's name text length.</span></span>  

    <span data-ttu-id="98d61-263">Proseware, Inc. および Litware, Inc. には、 管理形式に自動的にマージされる関連コンポーネントを含む IBAN および SWIFT コードを使用したこの形式のカスタムおよびローカル バージョンがあることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-263">Note that Proseware, Inc. and Litware, Inc. have custom and local versions of this format using IBAN and SWIFT codes with related components that are automatically merged in the managing format.</span></span>  

2. <span data-ttu-id="98d61-264">[基準値の適用] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-264">Click Apply base value.</span></span>

    <span data-ttu-id="98d61-265">[基準値の適用] をクリックして仕入先名の国固有の 100 文字の制限を適用します。</span><span class="sxs-lookup"><span data-stu-id="98d61-265">Click Apply base value to apply the country-specific limit of 100 characters for vendor names.</span></span>  

3. <span data-ttu-id="98d61-266">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-266">Click Save.</span></span>

    <span data-ttu-id="98d61-267">形式を保存すると、競合の一覧から解決済の競合が削除されます。</span><span class="sxs-lookup"><span data-stu-id="98d61-267">Saving the format will remove resolved conflicts from the conflicts list.</span></span>  

4. <span data-ttu-id="98d61-268">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="98d61-268">Close the page.</span></span>

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a><span data-ttu-id="98d61-269">カスタム形式のコンフィギュレーションの新規バージョンの状態を変更</span><span class="sxs-lookup"><span data-stu-id="98d61-269">Change the status of the new version of the custom format configuration</span></span>
1. <span data-ttu-id="98d61-270">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-270">Click Change status.</span></span>

    <span data-ttu-id="98d61-271">更新されたカスタム形式のコンフィギュレーションの状態を [ドラフト] から [完了] に変更します。</span><span class="sxs-lookup"><span data-stu-id="98d61-271">Change the status of the updated, custom format configuration from Draft to Completed.</span></span> <span data-ttu-id="98d61-272">この結果、支払ドキュメントの生成に形式のコンフィギュレーションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="98d61-272">This will make the format configuration available for generating payment documents.</span></span> <span data-ttu-id="98d61-273">選択したコンフィギュレーションの現在のバージョンが [ドラフト] 状態であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="98d61-273">Note that the current version of the selected configuration is in Draft status.</span></span>  

2. <span data-ttu-id="98d61-274">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-274">Click Complete.</span></span>
3. <span data-ttu-id="98d61-275">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="98d61-275">In the Description field, type a value.</span></span>
4. <span data-ttu-id="98d61-276">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98d61-276">Click OK.</span></span>

    <span data-ttu-id="98d61-277">作成したコンフィギュレーションが完了済のバージョン 1.2.2 として保存されていることに注意してください: 支払 (単純化モデル) データ モデルのバージョン 1 に基づく基準 BACS (英国関税) 形式のバージョン 2 に基づく基準 BACS (英国の企業) 形式のバージョン 2。</span><span class="sxs-lookup"><span data-stu-id="98d61-277">Note that the created configuration is saved as completed version 1.2.2: version 2 of base BACS (UK fictitious custom) format, which is based on version 2 of base BACS (UK fictitious) format, which is based on version 1 of Payments (simplified model) data model.</span></span>  

## <a name="test-the-customized-format-for-payment-files-generation"></a><span data-ttu-id="98d61-278">カスタマイズされた形式の支払ファイル生成テストの実行</span><span class="sxs-lookup"><span data-stu-id="98d61-278">Test the customized format for payment files generation</span></span>
<span data-ttu-id="98d61-279">並列する Finance and Operations セッションで 「作成されたフォーマットを使用して支払い用の電子文書を生成する」 の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="98d61-279">Complete the steps in the "Use created format to generate electronic documents for payments" procedure in parallel Finance and Operations session.</span></span> <span data-ttu-id="98d61-280">電子支払方法のパラメーターで作成した 「BACS (英国関税)」 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="98d61-280">Select the created 'BACS (UK fictitious custom)' format in electronic payment method parameters.</span></span> <span data-ttu-id="98d61-281">Proseware, Inc. が最近導入した、地域要件に対応した IBAN 口座コードを表す XML ノードが作成した支払ファイルに含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="98d61-281">Make sure that the created payment file contains recently introduced by Proseware, Inc. XML node presenting IBAN account code in accordance to regional requirements.</span></span> <span data-ttu-id="98d61-282">ファイルには Litware, Inc. が最近導入した、国要件に沿った SWIFT 銀行コードを表す XML ノードも含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="98d61-282">The file also should contain the recently introduced by Litware, Inc. XML node presenting SWIFT bank code in accordance to country requirements.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]