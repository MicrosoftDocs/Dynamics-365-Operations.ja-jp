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
ms.openlocfilehash: f2b93f74a121de4c23eb5dddfb94c6596b78544d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142665"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="b1ac8-103">ER 設計ドメイン固有のデータ モデル</span><span class="sxs-lookup"><span data-stu-id="b1ac8-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1ac8-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子支払ドキュメントのデータ モデルを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b1ac8-105">このデータ モデルは、支払ドキュメントの形式を作成するときに後でデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="b1ac8-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="b1ac8-107">この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="b1ac8-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="b1ac8-109">サンプル会社、「Litware、Inc.」 の構成プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="b1ac8-110">この構成プロバイダーが表示されない場合は、「構成プロバイダを作成し、アクティブとしてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="b1ac8-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="b1ac8-112">電子支払ドキュメントのデータ モデルを含むコンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="b1ac8-113">このデータ モデルは支払ドキュメントの形式を作成するするときに後でデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b1ac8-114">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="b1ac8-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="b1ac8-115">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="b1ac8-116">[名前] フィールドに、「支払 (単純化モデル)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="b1ac8-117">[説明] フィールドに、「支払モデル コンフィギュレーション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="b1ac8-118">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="b1ac8-119">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="b1ac8-120">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="b1ac8-121">構成の作成タスクを実行するには、[構成の作成] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="b1ac8-122">データ モデルの作成</span><span class="sxs-lookup"><span data-stu-id="b1ac8-122">Create a data model</span></span>
<span data-ttu-id="b1ac8-123">選択したコンフィギュレーションの新しいデータ モデルを作成しています。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="b1ac8-124">このコンフィギュレーション バージョンにはドラフトのステータスがあります。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="b1ac8-125">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="b1ac8-126">支払プロセスに関与している当事者の構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="b1ac8-127">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b1ac8-128">[名前] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="b1ac8-129">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-129">Click Add.</span></span>
4. <span data-ttu-id="b1ac8-130">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="b1ac8-131">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="b1ac8-132">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="b1ac8-133">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-133">Click Add.</span></span>
8. <span data-ttu-id="b1ac8-134">[検索] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="b1ac8-135">[前を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="b1ac8-136">このモデルの銀行構造の定義</span><span class="sxs-lookup"><span data-stu-id="b1ac8-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="b1ac8-137">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b1ac8-138">[名前] フィールドに、「代理店」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="b1ac8-139">[品目タイプ] フィールドで、「レコード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b1ac8-140">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-140">Click Add.</span></span>
5. <span data-ttu-id="b1ac8-141">[説明] フィールドで、「当事者 (債務者/債権者) の口座を提供する金融機関 (例: 銀行)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="b1ac8-142">当事者 (債務者/債権者) の口座を提供する金融機関 (例: 銀行)。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="b1ac8-143">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b1ac8-144">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="b1ac8-145">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b1ac8-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-146">Click Add.</span></span>
10. <span data-ttu-id="b1ac8-147">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="b1ac8-148">[名前] フィールドに、「SWIFT」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="b1ac8-149">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-149">Click Add.</span></span>
13. <span data-ttu-id="b1ac8-150">[説明] フィールドに、「銀行 ID コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="b1ac8-151">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b1ac8-152">[名前] フィールドに、「RoutingNumber」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="b1ac8-153">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-153">Click Add.</span></span>
17. <span data-ttu-id="b1ac8-154">[説明] フィールドに、「銀行支店コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="b1ac8-155">[前を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="b1ac8-156">このモデルの銀行口座構造の定義</span><span class="sxs-lookup"><span data-stu-id="b1ac8-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="b1ac8-157">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b1ac8-158">[名前] フィールドに、「口座」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="b1ac8-159">[品目タイプ] フィールドで、「レコード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="b1ac8-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-160">Click Add.</span></span>
5. <span data-ttu-id="b1ac8-161">[説明] フィールドに、「当事者の金融機関 (たとえば、銀行) の口座の ID」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="b1ac8-162">当事者の金融機関 (たとえば、銀行) の口座の ID。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="b1ac8-163">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="b1ac8-164">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="b1ac8-165">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="b1ac8-166">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-166">Click Add.</span></span>
10. <span data-ttu-id="b1ac8-167">[説明] フィールドに、「通貨コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="b1ac8-168">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b1ac8-169">[名前] フィールドに、「番号」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="b1ac8-170">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-170">Click Add.</span></span>
14. <span data-ttu-id="b1ac8-171">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="b1ac8-172">[名前] フィールドに、「IBAN」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="b1ac8-173">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-173">Click Add.</span></span>
17. <span data-ttu-id="b1ac8-174">[説明] フィールドに、「会社の国際銀行番号」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="b1ac8-175">口座振替の支払タイプの支払メッセージ構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="b1ac8-176">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="b1ac8-177">[新しいノード] フィールドに、「モデル ルート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="b1ac8-178">[名前] フィールドに「CustomerCreditTransferInitiatio」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="b1ac8-179">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-179">Click Add.</span></span>
5. <span data-ttu-id="b1ac8-180">[検索] フィールドに「CustomerCreditTransferInitiation」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="b1ac8-181">[前を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-181">Click Find previous.</span></span>
7. <span data-ttu-id="b1ac8-182">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b1ac8-183">[名前] フィールドで、「MessageIdentification」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="b1ac8-184">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-184">Click Add.</span></span>
10. <span data-ttu-id="b1ac8-185">[説明] フィールドに、「メッセージを明確に識別するために、指示者によって割り当てられる (および次の当事者に送信される) ポイント ツー ポイントの参照」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="b1ac8-186">メッセージを明確に識別するために、指示者によって割り当てられる (および次の当事者に送信される) ポイント ツー ポイントの参照です。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="b1ac8-187">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b1ac8-188">[名前] フィールドに、「ProcessingDateTime」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="b1ac8-189">[品目タイプ] フィールドで、「DateTime」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="b1ac8-190">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-190">Click Add.</span></span>
15. <span data-ttu-id="b1ac8-191">[説明] フィールドに、「支払メッセージが作成された日時」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="b1ac8-192">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="b1ac8-193">このモデルの支払トランザクション構造を定義します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="b1ac8-194">[名前] フィールドに、「支払」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="b1ac8-195">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="b1ac8-196">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-196">Click Add.</span></span>
20. <span data-ttu-id="b1ac8-197">[説明] フィールドに、「現在のメッセージの支払明細行」と入力とします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="b1ac8-198">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b1ac8-199">[名前] フィールドに、「債権者」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="b1ac8-200">[品目タイプ] フィールドで、「レコード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="b1ac8-201">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-201">Click Add.</span></span>
25. <span data-ttu-id="b1ac8-202">[説明] フィールドに、「金銭が支払われる当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="b1ac8-203">[品目参照の切り替え] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="b1ac8-204">[検索] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="b1ac8-205">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-205">Click Find next.</span></span>
29. <span data-ttu-id="b1ac8-206">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-206">Click OK.</span></span>
30. <span data-ttu-id="b1ac8-207">[検索] フィールドに、「支払」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="b1ac8-208">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-208">Click Find next.</span></span>
32. <span data-ttu-id="b1ac8-209">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="b1ac8-210">[名前] フィールドに、「債務者」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="b1ac8-211">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-211">Click Add.</span></span>
35. <span data-ttu-id="b1ac8-212">[説明] フィールドに、「(最終的な) 債権者に金銭を支払う義務を負う当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="b1ac8-213">[品目参照の切り替え] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="b1ac8-214">[検索] フィールドに、「当事者」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="b1ac8-215">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-215">Click Find next.</span></span>
39. <span data-ttu-id="b1ac8-216">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-216">Click OK.</span></span>
40. <span data-ttu-id="b1ac8-217">[次を検索] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-217">Click Find next.</span></span>
41. <span data-ttu-id="b1ac8-218">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="b1ac8-219">[名前] フィールドに、「説明」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="b1ac8-220">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="b1ac8-221">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-221">Click Add.</span></span>
45. <span data-ttu-id="b1ac8-222">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="b1ac8-223">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="b1ac8-224">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-224">Click Add.</span></span>
48. <span data-ttu-id="b1ac8-225">[説明] フィールドに、「通貨コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="b1ac8-226">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="b1ac8-227">[名前] フィールドに、「TransactionDate」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="b1ac8-228">[品目タイプ] フィールドで、「日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="b1ac8-229">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-229">Click Add.</span></span>
53. <span data-ttu-id="b1ac8-230">[説明] フィールドに、「トランザクション日付」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="b1ac8-231">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="b1ac8-232">[名前] フィールドに、「InstructedAmount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="b1ac8-233">[品目タイプ] フィールドで、「実数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="b1ac8-234">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-234">Click Add.</span></span>
58. <span data-ttu-id="b1ac8-235">[説明] フィールドに、「手数料を控除する前の、債務者と債権者の間を移動する金額」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b1ac8-236">金額は開始側の指示通りの通貨で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="b1ac8-237">手数料を控除する前に債務者と債権者の間を移動する金額です。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="b1ac8-238">金額は開始側の指示通りの通貨で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="b1ac8-239">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="b1ac8-240">[名前] フィールドに、「End2EndID」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="b1ac8-241">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="b1ac8-242">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-242">Click Add.</span></span>
63. <span data-ttu-id="b1ac8-243">[説明] フィールドに、「開始側が割り当てる固有 ID」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="b1ac8-244">この ID は、エンド ツー エンド チェーン全体に渡され、不変のものです。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="b1ac8-245">[名前] フィールドに「PaymentModel」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="b1ac8-246">「PaymentModel」の名前は支払形式の定義済インターフェイスに対応します。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="b1ac8-247">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-247">Click Save.</span></span>
66. <span data-ttu-id="b1ac8-248">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b1ac8-248">Close the page.</span></span>

