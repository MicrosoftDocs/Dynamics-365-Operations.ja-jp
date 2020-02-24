---
title: ER 設計ドメイン固有のデータ モデル
description: 次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子支払ドキュメントのデータ モデルを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe08b30977b8515ffd8d0acc1fd8f4b3085de93
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026089"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="af3b1-103">ER 設計ドメイン固有のデータ モデル</span><span class="sxs-lookup"><span data-stu-id="af3b1-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af3b1-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子支払ドキュメントのデータ モデルを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="af3b1-105">このデータ モデルは、支払ドキュメントの形式を作成するときに後でデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="af3b1-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="af3b1-107">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af3b1-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="af3b1-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="af3b1-109">サンプル会社、「Litware、Inc.」のコンフィギュレーション プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="af3b1-110">このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順の最初のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af3b1-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="af3b1-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="af3b1-112">電子支払ドキュメントのデータ モデルを含むコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="af3b1-113">このデータ モデルは支払ドキュメントの形式を作成するするときに後でデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="af3b1-114">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="af3b1-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="af3b1-115">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="af3b1-116">[名前] フィールドに、「支払 (単純化モデル)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="af3b1-117">支払 (単純化モデル)</span><span class="sxs-lookup"><span data-stu-id="af3b1-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="af3b1-118">[説明] フィールドに、「支払モデル コンフィギュレーション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="af3b1-119">支払モデル構成</span><span class="sxs-lookup"><span data-stu-id="af3b1-119">Payment model configuration</span></span>  
    * <span data-ttu-id="af3b1-120">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="af3b1-121">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="af3b1-122">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="af3b1-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="af3b1-123">コンフィギュレーション作成タスクを実行するのは、[コンフィギュレーションの作成] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="af3b1-124">データ モデルの作成</span><span class="sxs-lookup"><span data-stu-id="af3b1-124">Create a data model</span></span>
<span data-ttu-id="af3b1-125">選択したコンフィギュレーションの新しいデータ モデルを作成しています。</span><span class="sxs-lookup"><span data-stu-id="af3b1-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="af3b1-126">このコンフィギュレーション バージョンにはドラフトのステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="af3b1-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="af3b1-127">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="af3b1-128">支払プロセスに関与している当事者の構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="af3b1-129">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="af3b1-130">[名前] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="af3b1-131">関係者</span><span class="sxs-lookup"><span data-stu-id="af3b1-131">Party</span></span>  
3. <span data-ttu-id="af3b1-132">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-132">Click Add.</span></span>
4. <span data-ttu-id="af3b1-133">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="af3b1-134">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="af3b1-135">氏名</span><span class="sxs-lookup"><span data-stu-id="af3b1-135">Name</span></span>  
6. <span data-ttu-id="af3b1-136">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="af3b1-137">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-137">Click Add.</span></span>
8. <span data-ttu-id="af3b1-138">[検索] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="af3b1-139">関係者</span><span class="sxs-lookup"><span data-stu-id="af3b1-139">Party</span></span>  
9. <span data-ttu-id="af3b1-140">[前を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="af3b1-141">このモデルの銀行構造の定義</span><span class="sxs-lookup"><span data-stu-id="af3b1-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="af3b1-142">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="af3b1-143">[名前] フィールドに、「代理店」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="af3b1-144">代理店</span><span class="sxs-lookup"><span data-stu-id="af3b1-144">Agent</span></span>  
3. <span data-ttu-id="af3b1-145">[品目タイプ] フィールドで、「レコード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="af3b1-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-146">Click Add.</span></span>
5. <span data-ttu-id="af3b1-147">[説明] フィールドで、「当事者 (債務者/債権者) の口座を提供する金融機関 (例: 銀行)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="af3b1-148">当事者 (債務者/債権者) の口座を提供する金融機関 (例: 銀行)。</span><span class="sxs-lookup"><span data-stu-id="af3b1-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="af3b1-149">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="af3b1-150">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="af3b1-151">氏名</span><span class="sxs-lookup"><span data-stu-id="af3b1-151">Name</span></span>  
8. <span data-ttu-id="af3b1-152">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="af3b1-153">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-153">Click Add.</span></span>
10. <span data-ttu-id="af3b1-154">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="af3b1-155">[名前] フィールドに、「SWIFT」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="af3b1-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="af3b1-156">SWIFT</span></span>  
12. <span data-ttu-id="af3b1-157">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-157">Click Add.</span></span>
13. <span data-ttu-id="af3b1-158">[説明] フィールドに、「銀行 ID コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="af3b1-159">銀行 ID コード</span><span class="sxs-lookup"><span data-stu-id="af3b1-159">Bank identification code</span></span>  
14. <span data-ttu-id="af3b1-160">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="af3b1-161">[名前] フィールドに、「RoutingNumber」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="af3b1-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="af3b1-162">RoutingNumber</span></span>  
16. <span data-ttu-id="af3b1-163">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-163">Click Add.</span></span>
17. <span data-ttu-id="af3b1-164">[説明] フィールドに、「銀行支店コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="af3b1-165">銀行支店コード</span><span class="sxs-lookup"><span data-stu-id="af3b1-165">Routing number</span></span>  
18. <span data-ttu-id="af3b1-166">[前を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="af3b1-167">このモデルの銀行口座構造の定義</span><span class="sxs-lookup"><span data-stu-id="af3b1-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="af3b1-168">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="af3b1-169">[名前] フィールドに、「口座」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="af3b1-170">アカウント</span><span class="sxs-lookup"><span data-stu-id="af3b1-170">Account</span></span>  
3. <span data-ttu-id="af3b1-171">[品目タイプ] フィールドで、「レコード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="af3b1-172">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-172">Click Add.</span></span>
5. <span data-ttu-id="af3b1-173">[説明] フィールドに、「当事者の金融機関 (たとえば、銀行) の口座の ID」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="af3b1-174">当事者の金融機関 (たとえば、銀行) の口座の ID。</span><span class="sxs-lookup"><span data-stu-id="af3b1-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="af3b1-175">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="af3b1-176">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="af3b1-177">通貨</span><span class="sxs-lookup"><span data-stu-id="af3b1-177">Currency</span></span>  
8. <span data-ttu-id="af3b1-178">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="af3b1-179">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-179">Click Add.</span></span>
10. <span data-ttu-id="af3b1-180">[説明] フィールドに、「通貨コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="af3b1-181">通貨コード</span><span class="sxs-lookup"><span data-stu-id="af3b1-181">Currency code</span></span>  
11. <span data-ttu-id="af3b1-182">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="af3b1-183">[名前] フィールドに、「番号」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="af3b1-184">数値</span><span class="sxs-lookup"><span data-stu-id="af3b1-184">Number</span></span>  
13. <span data-ttu-id="af3b1-185">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-185">Click Add.</span></span>
14. <span data-ttu-id="af3b1-186">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="af3b1-187">[名前] フィールドに、「IBAN」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="af3b1-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="af3b1-188">IBAN</span></span>  
16. <span data-ttu-id="af3b1-189">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-189">Click Add.</span></span>
17. <span data-ttu-id="af3b1-190">[説明] フィールドに、「会社の国際銀行番号」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="af3b1-191">国際銀行番号</span><span class="sxs-lookup"><span data-stu-id="af3b1-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="af3b1-192">口座振替の支払タイプの支払メッセージ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="af3b1-193">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="af3b1-194">[新しいノード] フィールドに、「モデル ルート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="af3b1-195">[名前] フィールドに「CustomerCreditTransferInitiatio」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="af3b1-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="af3b1-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="af3b1-197">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-197">Click Add.</span></span>
5. <span data-ttu-id="af3b1-198">[検索] フィールドに「CustomerCreditTransferInitiation」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="af3b1-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="af3b1-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="af3b1-200">[前を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-200">Click Find previous.</span></span>
7. <span data-ttu-id="af3b1-201">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="af3b1-202">[名前] フィールドで、「MessageIdentification」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="af3b1-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="af3b1-203">MessageIdentification</span></span>  
9. <span data-ttu-id="af3b1-204">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-204">Click Add.</span></span>
10. <span data-ttu-id="af3b1-205">[説明] フィールドに、「メッセージを明確に識別するために、指示者によって割り当てられる (および次の当事者に送信される) ポイント ツー ポイントの参照」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="af3b1-206">メッセージを明確に識別するために、指示者によって割り当てられる (および次の当事者に送信される) ポイント ツー ポイントの参照です。</span><span class="sxs-lookup"><span data-stu-id="af3b1-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="af3b1-207">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="af3b1-208">[名前] フィールドに、「ProcessingDateTime」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="af3b1-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="af3b1-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="af3b1-210">[品目タイプ] フィールドで、「DateTime」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="af3b1-211">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-211">Click Add.</span></span>
15. <span data-ttu-id="af3b1-212">[説明] フィールドに、「支払メッセージが作成された日時」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="af3b1-213">支払メッセージが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="af3b1-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="af3b1-214">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="af3b1-215">このモデルの支払トランザクション構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="af3b1-216">[名前] フィールドに、「支払」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="af3b1-217">支払利息</span><span class="sxs-lookup"><span data-stu-id="af3b1-217">Payments</span></span>  
18. <span data-ttu-id="af3b1-218">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="af3b1-219">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-219">Click Add.</span></span>
20. <span data-ttu-id="af3b1-220">[説明] フィールドに、「現在のメッセージの支払明細行」と入力とします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="af3b1-221">現在のメッセージの支払明細行</span><span class="sxs-lookup"><span data-stu-id="af3b1-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="af3b1-222">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="af3b1-223">[名前] フィールドに、「債権者」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="af3b1-224">作成者</span><span class="sxs-lookup"><span data-stu-id="af3b1-224">Creditor</span></span>  
23. <span data-ttu-id="af3b1-225">[品目タイプ] フィールドで、「レコード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="af3b1-226">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-226">Click Add.</span></span>
25. <span data-ttu-id="af3b1-227">[説明] フィールドに、「金銭が支払われる当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="af3b1-228">金銭が支払われる当事者。</span><span class="sxs-lookup"><span data-stu-id="af3b1-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="af3b1-229">[品目参照の切り替え] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="af3b1-230">[検索] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="af3b1-231">関係者</span><span class="sxs-lookup"><span data-stu-id="af3b1-231">Party</span></span>  
28. <span data-ttu-id="af3b1-232">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-232">Click Find next.</span></span>
29. <span data-ttu-id="af3b1-233">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-233">Click OK.</span></span>
30. <span data-ttu-id="af3b1-234">[検索] フィールドに、「支払」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="af3b1-235">支払利息</span><span class="sxs-lookup"><span data-stu-id="af3b1-235">Payments</span></span>  
31. <span data-ttu-id="af3b1-236">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-236">Click Find next.</span></span>
32. <span data-ttu-id="af3b1-237">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="af3b1-238">[名前] フィールドに、「債務者」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="af3b1-239">債務者</span><span class="sxs-lookup"><span data-stu-id="af3b1-239">Debtor</span></span>  
34. <span data-ttu-id="af3b1-240">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-240">Click Add.</span></span>
35. <span data-ttu-id="af3b1-241">[説明] フィールドに、「(最終的な) 債権者に金銭を支払う義務を負う当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="af3b1-242">(最終的な) 債権者に金銭を支払う義務を負う当事者。</span><span class="sxs-lookup"><span data-stu-id="af3b1-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="af3b1-243">[品目参照の切り替え] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="af3b1-244">[検索] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="af3b1-245">関係者</span><span class="sxs-lookup"><span data-stu-id="af3b1-245">Party</span></span>  
38. <span data-ttu-id="af3b1-246">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-246">Click Find next.</span></span>
39. <span data-ttu-id="af3b1-247">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-247">Click OK.</span></span>
40. <span data-ttu-id="af3b1-248">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-248">Click Find next.</span></span>
41. <span data-ttu-id="af3b1-249">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="af3b1-250">[名前] フィールドに、「説明」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="af3b1-251">説明</span><span class="sxs-lookup"><span data-stu-id="af3b1-251">Description</span></span>  
43. <span data-ttu-id="af3b1-252">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="af3b1-253">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-253">Click Add.</span></span>
45. <span data-ttu-id="af3b1-254">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="af3b1-255">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="af3b1-256">通貨</span><span class="sxs-lookup"><span data-stu-id="af3b1-256">Currency</span></span>  
47. <span data-ttu-id="af3b1-257">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-257">Click Add.</span></span>
48. <span data-ttu-id="af3b1-258">[説明] フィールドに、「通貨コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="af3b1-259">通貨コード</span><span class="sxs-lookup"><span data-stu-id="af3b1-259">Currency code</span></span>  
49. <span data-ttu-id="af3b1-260">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="af3b1-261">[名前] フィールドに、「TransactionDate」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="af3b1-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="af3b1-262">TransactionDate</span></span>  
51. <span data-ttu-id="af3b1-263">[品目タイプ] フィールドで、「日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="af3b1-264">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-264">Click Add.</span></span>
53. <span data-ttu-id="af3b1-265">[説明] フィールドに、「トランザクション日付」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="af3b1-266">取引日付</span><span class="sxs-lookup"><span data-stu-id="af3b1-266">Transaction date</span></span>  
54. <span data-ttu-id="af3b1-267">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="af3b1-268">[名前] フィールドに、「InstructedAmount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="af3b1-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="af3b1-269">InstructedAmount</span></span>  
56. <span data-ttu-id="af3b1-270">[品目タイプ] フィールドで、「実数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="af3b1-271">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-271">Click Add.</span></span>
58. <span data-ttu-id="af3b1-272">[説明] フィールドに、「手数料を控除する前の、債務者と債権者の間を移動する金額」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="af3b1-273">金額は開始側の指示通りの通貨で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af3b1-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="af3b1-274">手数料を控除する前に債務者と債権者の間を移動する金額です。</span><span class="sxs-lookup"><span data-stu-id="af3b1-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="af3b1-275">金額は開始側の指示通りの通貨で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af3b1-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="af3b1-276">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="af3b1-277">[名前] フィールドに、「End2EndID」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="af3b1-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="af3b1-278">End2EndID</span></span>  
61. <span data-ttu-id="af3b1-279">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="af3b1-280">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-280">Click Add.</span></span>
63. <span data-ttu-id="af3b1-281">[説明] フィールドに、「開始側が割り当てる固有 ID」を入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="af3b1-282">この ID は、エンド ツー エンド チェーン全体に渡され、不変のものです。</span><span class="sxs-lookup"><span data-stu-id="af3b1-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="af3b1-283">開始側が割り当てる固有 ID です。</span><span class="sxs-lookup"><span data-stu-id="af3b1-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="af3b1-284">この ID は、エンド ツー エンド チェーン全体に渡され、不変のものです。</span><span class="sxs-lookup"><span data-stu-id="af3b1-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="af3b1-285">[名前] フィールドに「PaymentModel」と入力します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="af3b1-286">「PaymentModel」の名前は支払形式の定義済インターフェイスに対応します。</span><span class="sxs-lookup"><span data-stu-id="af3b1-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="af3b1-287">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="af3b1-287">Click Save.</span></span>
66. <span data-ttu-id="af3b1-288">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="af3b1-288">Close the page.</span></span>

