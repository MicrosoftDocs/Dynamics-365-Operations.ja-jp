---
title: アプリケーション クラスのメソッドを呼び出す ER 式の設計
description: このガイドは、ER の式で必要なアプリケーション クラスのメソッドを呼び出すことによって、電子申告 (ER) コンフィギュレーションで既存のアプリケーション ロジックを再利用する方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f61228d328521d0c6fe8e0ae704001a65d03151f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249230"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="e5a07-103">アプリケーション クラスのメソッドを呼び出す ER 式の設計</span><span class="sxs-lookup"><span data-stu-id="e5a07-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e5a07-104">このガイドは、ER の式で必要なアプリケーション クラスのメソッドを呼び出すことによって、電子申告 (ER) コンフィギュレーションで既存のアプリケーション ロジックを再利用する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="e5a07-105">呼び出しクラスの引数の値は、実行時に動的に定義することができます。たとえば、解析文書内の情報に基づいて、その正確性を確保します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="e5a07-106">このガイドでは、サンプル会社 Litware, Inc. に必要な ER コンフィギュレーションを作成します。この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="e5a07-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="e5a07-107">これらのステップは、任意のデータ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="e5a07-108">次のファイルもローカルでダウンロードして保存する必要があります: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt。</span><span class="sxs-lookup"><span data-stu-id="e5a07-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="e5a07-109">これらの手順を完了するには、まず手順の「ER はコンフィギュレーションプロバイダーを作成し、それを有効としてマークする」にある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a07-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="e5a07-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e5a07-111">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="e5a07-112">このコンフィギュレーション プロバイダーが表示されない場合は、「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a07-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="e5a07-113">アプリケーション データ更新のために受取口座取引明細書を解析するプロセスを設計しているとしましょう。</span><span class="sxs-lookup"><span data-stu-id="e5a07-113">Uou are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="e5a07-114">受取口座取引明細書が、IBAN コードを含んだテキスト ファイルとして届きます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="e5a07-115">口座取引明細書のインポート プロセスの一部として、すでに利用可能なロジックを使用して、この IBAN コードの正確性を検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5a07-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="e5a07-116">新しい ER モデル コンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="e5a07-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="e5a07-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e5a07-118">Microsoft プロバイダー タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="e5a07-119">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-119">Click Repositories.</span></span>
3. <span data-ttu-id="e5a07-120">[フィルターの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-120">Click Show filters.</span></span>
4. <span data-ttu-id="e5a07-121">[タイプ名] フィルター フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="e5a07-122">[名前] フィールドでは、値「リソース」を入力し、「次の値を含む」フィールド オペレーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="e5a07-123">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-123">Click Open.</span></span>
6. <span data-ttu-id="e5a07-124">ツリーで、「支払モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="e5a07-125">[バージョン] クイック タブの [インポート] ボタンが有効でない場合は、ER コンフィギュレーション [支払モデル] のひとつである、「バージョン 1」がすでにインポートされています。</span><span class="sxs-lookup"><span data-stu-id="e5a07-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="e5a07-126">この下位タスクの残りの手順はスキップできます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="e5a07-127">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-127">Click Import.</span></span>
8. <span data-ttu-id="e5a07-128">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-128">Click Yes.</span></span>
9. <span data-ttu-id="e5a07-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-129">Close the page.</span></span>
10. <span data-ttu-id="e5a07-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="e5a07-131">新しい ER 形式コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="e5a07-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="e5a07-132">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="e5a07-133">新しい ER 形式を追加して、受取口座取引明細書を TXT 形式で解析します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="e5a07-134">ツリーで、「支払モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="e5a07-135">[コンフィギュレーションの作成] をクリックすると、ダイアログ メニューが開きます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="e5a07-136">[新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="e5a07-137">[名前] フィールドに「口座取引明細書のインポート形式 (サンプル)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="e5a07-138">口座取引明細書のインポート形式 (サンプル)</span><span class="sxs-lookup"><span data-stu-id="e5a07-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="e5a07-139">[データのインポートのサポート] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="e5a07-140">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="e5a07-141">ER 形式のコンフィギュレーションをデザイン- 形式</span><span class="sxs-lookup"><span data-stu-id="e5a07-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="e5a07-142">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-142">Click Designer.</span></span>
    * <span data-ttu-id="e5a07-143">設計された形式は、TXT 形式の外部ファイルの予想構造を表します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="e5a07-144">[ルートの追加] をクリックして、ダイアログ メニューを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="e5a07-145">ツリーで、「Text\Sequence」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="e5a07-146">[名称] のフィールドに、「Root」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="e5a07-147">ルート</span><span class="sxs-lookup"><span data-stu-id="e5a07-147">Root</span></span>  
5. <span data-ttu-id="e5a07-148">[特殊文字] フィールドでは、「New line - Windows (CR LF)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="e5a07-149">「New line - Windows (CR LF)」オプションが、「特殊文字」フィールドで選択されています。</span><span class="sxs-lookup"><span data-stu-id="e5a07-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="e5a07-150">この設定に基づいて、解析ファイル内の各明細行は別々のレコードとみなします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="e5a07-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-151">Click OK.</span></span>
7. <span data-ttu-id="e5a07-152">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="e5a07-153">ツリーで、「Text\Sequence」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="e5a07-154">[名前] フィールドに、「行」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="e5a07-155">行</span><span class="sxs-lookup"><span data-stu-id="e5a07-155">Rows</span></span>  
10. <span data-ttu-id="e5a07-156">[多様性] フィールドで、「1 つ、多数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="e5a07-157">[多様性] フィールドで、「1 つ、多数」オプションが選択されています。</span><span class="sxs-lookup"><span data-stu-id="e5a07-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="e5a07-158">この設定に基づいて、解析ファイルに少なくとも 1 つの明細行が表示されることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="e5a07-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-159">Click OK.</span></span>
12. <span data-ttu-id="e5a07-160">ツリーで、[ルート\行] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="e5a07-161">[順番の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="e5a07-162">[名前] フィールドに、「フィールド」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="e5a07-163">フィールド</span><span class="sxs-lookup"><span data-stu-id="e5a07-163">Fields</span></span>  
15. <span data-ttu-id="e5a07-164">[多様性] フィールドで、「1 つのみ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="e5a07-165">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-165">Click OK.</span></span>
17. <span data-ttu-id="e5a07-166">ツリーで、[ルート\行\フィールド] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="e5a07-167">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="e5a07-168">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="e5a07-169">[名前] フィールドに、「IBAN」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="e5a07-170">IBAN</span><span class="sxs-lookup"><span data-stu-id="e5a07-170">IBAN</span></span>  
21. <span data-ttu-id="e5a07-171">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-171">Click OK.</span></span>
    * <span data-ttu-id="e5a07-172">解析ファイルの各明細行に IBAN コードのみが含まれるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e5a07-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="e5a07-173">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="e5a07-174">ER 形式のコンフィギュレーションをデザイン- データ モデルへのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5a07-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="e5a07-175">[形式をモデルにマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-175">Click Map format to model.</span></span>
2. <span data-ttu-id="e5a07-176">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-176">Click New.</span></span>
3. <span data-ttu-id="e5a07-177">[定義] フィールドに、「BankToCustomerDebitCreditNotificationInitiation」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="e5a07-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="e5a07-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="e5a07-179">[定義の変更] を解決します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="e5a07-180">[名前] フィールドで、「データモデルのマッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="e5a07-181">データ モデルへのマッピング</span><span class="sxs-lookup"><span data-stu-id="e5a07-181">Mapping to data model</span></span>  
6. <span data-ttu-id="e5a07-182">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-182">Click Save.</span></span>
7. <span data-ttu-id="e5a07-183">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-183">Click Designer.</span></span>
8. <span data-ttu-id="e5a07-184">ツリーで、「Dynamics 365 for Operations\Class」を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="e5a07-185">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-185">Click Add root.</span></span>
    * <span data-ttu-id="e5a07-186">IBAN コード検証のために既存のアプリケーション ロジックを呼び出すための新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="e5a07-187">[名称] フィールドで、「check_codes」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="e5a07-188">check_codes</span><span class="sxs-lookup"><span data-stu-id="e5a07-188">check_codes</span></span>  
11. <span data-ttu-id="e5a07-189">[クラス] フィールドに「ISO7064」と入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="e5a07-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="e5a07-190">ISO7064</span></span>  
12. <span data-ttu-id="e5a07-191">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-191">Click OK.</span></span>
13. <span data-ttu-id="e5a07-192">ツリーで、「形式」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="e5a07-193">ツリーで、[形式\ルート: 順番 (ルート)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="e5a07-194">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="e5a07-195">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-195">Click Bind.</span></span>
17. <span data-ttu-id="e5a07-196">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="e5a07-197">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)\フィールド: 順番 1..1 (フィールド)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="e5a07-198">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)\フィールド: 順番 1..1 (フィールド)\IBAN: 文字列 (IBAN)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="e5a07-199">ツリーで、[支払い = format.Root.Row] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="e5a07-200">ツリーで、[支払い = format.Root.Rows\債権者勘定 (CreditorAccount)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="e5a07-201">ツリーで、[支払い = format.Root.Rows\債権者勘定 (CreditorAccount)\ID] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="e5a07-202">ツリーで、[支払い = format.Root.Rows\債権者勘定 (CreditorAccount)\ID\IBAN] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="e5a07-203">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-203">Click Bind.</span></span>
25. <span data-ttu-id="e5a07-204">[検証] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="e5a07-205">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-205">Click New.</span></span>
    * <span data-ttu-id="e5a07-206">無効な IBAN コードを含む解析ファイルで任意の明細行のエラーを表示する新しい検証ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="e5a07-207">[条件の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-207">Click Edit condition.</span></span>
28. <span data-ttu-id="e5a07-208">ツリーで、[check_codes] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="e5a07-209">ツリーで、[check_codes\verifyMOD1271_36] を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="e5a07-210">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-210">Click Add data source.</span></span>
31. <span data-ttu-id="e5a07-211">[式] フィールドに、「check_codes.verifyMOD1271_36(」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="e5a07-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="e5a07-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="e5a07-213">ツリーで、「形式」を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="e5a07-214">ツリーで、[形式\ルート: 順番 (ルート)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="e5a07-215">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="e5a07-216">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)\フィールド: 順番 1..1 (フィールド)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="e5a07-217">ツリーで、[形式\ルート: 順番 (ルート)\行: 順番 1..\* (行)\フィールド: 順番 1..1 (フィールド)\IBAN: 文字列 (IBAN)] を展開します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="e5a07-218">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-218">Click Add data source.</span></span>
38. <span data-ttu-id="e5a07-219">[式] フィールドに、「check_codes.verifyMOD1271_36 (format.Root.Rows.Fields.IBAN)」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="e5a07-220">check_codes.verifyMOD1271_36 (形式です。Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="e5a07-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="e5a07-221">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-221">Click Save.</span></span>
40. <span data-ttu-id="e5a07-222">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-222">Close the page.</span></span>
    * <span data-ttu-id="e5a07-223">検証条件は、アプリケーション クラス 「ISO7064」の既存のメソッド 「verifyMOD1271_36」を呼び出すことによって、無効な IBAN コードに対して FALSE を返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e5a07-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="e5a07-224">IBAN コードの値は、解析中の TXT ファイルの内容に基づいて、呼び出しメソッドの引数として実行時に動的に定義されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e5a07-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="e5a07-225">メッセージの編集をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-225">Click Edit message.</span></span>
42. <span data-ttu-id="e5a07-226">[式] フィールドに、「CONCATENATE("無効な IBAN コードが検出されました:  ", format.Root.Rows.Fields.IBAN)」を入力します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="e5a07-227">CONCATENATE("無効な IBAN コードが検出されました:  "、書式設定します.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="e5a07-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="e5a07-228">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-228">Click Save.</span></span>
44. <span data-ttu-id="e5a07-229">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-229">Close the page.</span></span>
45. <span data-ttu-id="e5a07-230">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-230">Click Save.</span></span>
46. <span data-ttu-id="e5a07-231">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="e5a07-232">形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="e5a07-232">Run the format mapping</span></span>
<span data-ttu-id="e5a07-233">テストのために、ダウンロードした SampleIncomingMessage.txt ファイルを使用して形式マッピングを実行します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="e5a07-234">生成された出力は選択された TXT ファイルからインポートされ、実際のインポート中にカスタム データ モデルに読み込まれるデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="e5a07-235">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-235">Click Run.</span></span>
    * <span data-ttu-id="e5a07-236">[参照] をクリックし、以前ダウンロードした SampleIncomingMessage.txt ファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="e5a07-237">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e5a07-237">Click OK.</span></span>
    * <span data-ttu-id="e5a07-238">選択ファイルからインポートされてデータ モデルにポートされたデータを表すXML 書式の出力を確認します。</span><span class="sxs-lookup"><span data-stu-id="e5a07-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="e5a07-239">インポートされた TXT ファイルの 3 つの行のみが処理されたことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e5a07-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="e5a07-240">有効でない明細行 4 の IBAN コードはスキップされ、情報ログにエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5a07-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  
