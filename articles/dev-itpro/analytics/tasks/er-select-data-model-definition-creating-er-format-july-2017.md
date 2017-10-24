--- 
title: "電子申告 (ER) の形式の作成中にデータ モデル定義を選択する"
description: "この手順にあるステップを完了するには、まず「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」にある手順を完了する必要があります。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 70d928b0f0807731a5f96ef5497fb6060fbfebf5
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="select-data-model-definition-while-creating-format-for-electronic-reporting-er"></a><span data-ttu-id="8bed9-103">電子申告 (ER) の形式の作成中にデータ モデル定義を選択する</span><span class="sxs-lookup"><span data-stu-id="8bed9-103">Select data model definition while creating format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8bed9-104">この手順にあるステップを完了するには、まず「ER コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」にある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bed9-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="8bed9-105">この手順では、電子ドキュメントを生成するために設計されている電子レポート (ER) 形式コンフィギュレーションを挿入するために、モデルのルート項目をデータ モデル定義として選択する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-105">This procedure shows how a model’s root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="8bed9-106">この手順では、サンプル会社 Litware、Inc. 用の新しい ER 形式コンフィギュレーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="8bed9-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="8bed9-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="8bed9-108">ステップは、どのデータ セットを使用しても完了することができます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="8bed9-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8bed9-110">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="8bed9-111">このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bed9-111">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="8bed9-112">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="8bed9-113">新しい ER データ モデル コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="8bed9-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="8bed9-114">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="8bed9-115">生成 ER レポートのデータ ソースとして使用するように設計されたデータ モデルを含む新しい ER モデル コンフィギュレーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="8bed9-116">[名前] フィールドに、「支払モデル (架空)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="8bed9-117">支払モデル (架空)</span><span class="sxs-lookup"><span data-stu-id="8bed9-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="8bed9-118">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-118">Click Create configuration.</span></span>
4. <span data-ttu-id="8bed9-119">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-119">Click Designer.</span></span>
    * <span data-ttu-id="8bed9-120">ER デザイナーを開いて、このコンフィギュレーションのデータ モデルの構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="8bed9-121">口座振替と口座引落という 2 つの支払方法をサポートするために、支払業務ドメインのデータ モデルを設計すると仮定します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="8bed9-122">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="8bed9-123">[名前] フィールドに、「支払 – 口座振替」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="8bed9-124">支払 – 口座振替</span><span class="sxs-lookup"><span data-stu-id="8bed9-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="8bed9-125">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-125">Click Add.</span></span>
8. <span data-ttu-id="8bed9-126">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="8bed9-127">[新しいノード] フィールドに、「モデル ルート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="8bed9-128">[名前] フィールドに、「支払 – 口座引落」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="8bed9-129">支払 – 口座引落</span><span class="sxs-lookup"><span data-stu-id="8bed9-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="8bed9-130">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-130">Click Add.</span></span>
12. <span data-ttu-id="8bed9-131">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-131">Click Save.</span></span>
13. <span data-ttu-id="8bed9-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-132">Close the page.</span></span>
14. <span data-ttu-id="8bed9-133">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-133">Click Change status.</span></span>
    * <span data-ttu-id="8bed9-134">モデルのドラフト バージョンを完了して、新しいモデル マッピングと形式で使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="8bed9-135">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-135">Click Complete.</span></span>
16. <span data-ttu-id="8bed9-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="8bed9-137">新しい ER 形式コンフィギュレーションの入力を開始する</span><span class="sxs-lookup"><span data-stu-id="8bed9-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="8bed9-138">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8bed9-139">[新規] フィールドで、「支払モデル (架空) のデータ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="8bed9-140">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8bed9-141">選択したデータ モデルのすべてのルート項目が、現在データ モデル定義として選択可能であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8bed9-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="8bed9-142">データ モデルの必要なルート項目のいずれかを使用して、形式の設計を続行することができます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="8bed9-143">選択したルート項目のモデル マッピングが存在しなくても、続行は妨げられません。</span><span class="sxs-lookup"><span data-stu-id="8bed9-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="8bed9-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="8bed9-145">新しい ER モデル マッピング コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="8bed9-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="8bed9-146">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="8bed9-147">[新規] フィールドで、「支払モデル (架空) のデータ モデルに基づいたモデル マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="8bed9-148">[名前] フィールドに、「支払モデル マッピング (架空)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="8bed9-149">支払モデル マッピング (架空)</span><span class="sxs-lookup"><span data-stu-id="8bed9-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="8bed9-150">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="8bed9-151">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="8bed9-152">ER モデル マッピングを設計する</span><span class="sxs-lookup"><span data-stu-id="8bed9-152">Design ER model mappings</span></span>
1. <span data-ttu-id="8bed9-153">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-153">Click Designer.</span></span>
    * <span data-ttu-id="8bed9-154">ER デザイナーを使用して、必要なルート項目のモデル マッピングを指定します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="8bed9-155">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-155">Click Designer.</span></span>
    * <span data-ttu-id="8bed9-156">選択したモデルのルート項目の選択したモデル マッピングの設定をシミュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-156">Simulate setting of selected model mapping for the selected model’s root item.</span></span>  
3. <span data-ttu-id="8bed9-157">ツリーで、[Dynamics 365 for Operations\Table records] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="8bed9-158">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-158">Click Add root.</span></span>
5. <span data-ttu-id="8bed9-159">[名前] フィールドに、「元帳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="8bed9-160">[テーブル] フィールドで、「LedgerJournalTrans」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="8bed9-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="8bed9-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="8bed9-162">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-162">Click OK.</span></span>
8. <span data-ttu-id="8bed9-163">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bed9-163">Click Save.</span></span>
9. <span data-ttu-id="8bed9-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-164">Close the page.</span></span>
10. <span data-ttu-id="8bed9-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="8bed9-166">別の新しい ER 形式コンフィギュレーションの入力を開始する</span><span class="sxs-lookup"><span data-stu-id="8bed9-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="8bed9-167">ツリーで、「支払モデル (架空)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="8bed9-168">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="8bed9-169">[新規] フィールドで、「支払モデル (架空) のデータ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="8bed9-170">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8bed9-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="8bed9-171">アプリケーション データ ソースにマップするのに、現在 1 つのみのルート項目が使用可能であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8bed9-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="8bed9-172">少なくとも 1 つのモデル マッピングが導入されると、アプリケーション データ ソースにマップされているモデルのルート項目のみが、ER 形式が追加されるときにモデル定義として選択できます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-172">When at least one model mapping is introduced, only the model’s root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="8bed9-173">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bed9-173">Close the page.</span></span>


