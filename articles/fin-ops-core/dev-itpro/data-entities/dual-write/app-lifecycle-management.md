---
title: アプリケーション ライフサイクル管理
description: このトピックでは、二重書き込みソリューションに対応することの利点について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 971fedb5f059bce5eefb9abc9ae5419ab227750a
ms.sourcegitcommit: e9fadf6f6dafdcefaff8e23eaa3c85f53437db3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3279120"
---
# <a name="application-lifecycle-management"></a><span data-ttu-id="1e7e1-103">アプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="1e7e1-103">Application lifecycle management</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1e7e1-104">二重書き込みソリューションに対応することで、環境全体での二重書き込みエンティティ マップの転送やバックアップ/復元など、基本的なアプリケーション ライフサイクル管理 (ALM) 機能を実現できます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-104">By making dual-write solution-aware, you enable basic application lifecycle management (ALM) capabilities, such as transportation and backup/restore of dual-write entity maps across environments.</span></span> <span data-ttu-id="1e7e1-105">また、AppSource から Microsoft または独立系ソフトウェア ベンダー (ISV) が公開するソリューションを入手できるシナリオも有効にします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-105">You also enable scenarios where you can get solutions that are published by Microsoft or an independent software vendor (ISV) from AppSource.</span></span>

## <a name="what-is-a-dual-write-solution"></a><span data-ttu-id="1e7e1-106">二重書き込みソリューションとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="1e7e1-106">What is a dual-write solution?</span></span>

<span data-ttu-id="1e7e1-107">二重書き込みソリューションには、1 つ以上の二重書き込みエンティティ マップを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-107">A dual-write solution can contain one or more dual-write entity maps.</span></span> <span data-ttu-id="1e7e1-108">これらのマップは、ご使用の環境 (Microsoft Power Apps の **ソリューション** を選択) にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-108">These maps can be imported into your environment (by selecting **Solutions** in Microsoft Power Apps).</span></span> <span data-ttu-id="1e7e1-109">また、パッケージとして他の環境にエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-109">They can also be exported to other environments as a package.</span></span> <span data-ttu-id="1e7e1-110">Microsoft 公開のエンティティ マップまたは ISV 公開のエンティティ マップを AppSource からインポートして、テスト環境で変更し、テストして、準備が整ったら、実稼働環境にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-110">You can import Microsoft-published or ISV-published entity maps from AppSource, modify them in your test environment, test them, and then, when they are ready, export them to your production environment.</span></span> <span data-ttu-id="1e7e1-111">また、AppSource でソリューションを公開して、他のユーザーが使用できるようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-111">Additionally, you can publish your solution through AppSource, so that other people can use it.</span></span>

<span data-ttu-id="1e7e1-112">ソリューションには、マネージドとアンマネージドの 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-112">There two types of solutions: managed and unmanaged.</span></span>

<span data-ttu-id="1e7e1-113">マネージド ソリューションを変更することはできませんが、インポート後にアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-113">A managed solution can't be modified, and it can be uninstalled after it's imported.</span></span> <span data-ttu-id="1e7e1-114">アンマネージド ソリューションをインポートする場合は、そのソリューションのすべてのコンポーネントを環境に追加します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-114">When you import an unmanaged solution, you add all the components of that solution into your environment.</span></span> <span data-ttu-id="1e7e1-115">既にカスタマイズしたコンポーネントを含むアンマネージド ソリューションをインポートすると、カスタマイズはインポート済みアンマネージド ソリューションのカスタマイズによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-115">When you import an unmanaged solution that contains components that you've already customized, your customizations are overwritten by the customizations in the imported unmanaged solution.</span></span>

<span data-ttu-id="1e7e1-116">ソリューションの詳細については、[ソリューションの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-116">For more information about solutions, see the [solutions overview](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview).</span></span>

## <a name="install-the-dual-write-core-solution"></a><span data-ttu-id="1e7e1-117">二重書き込みコア ソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="1e7e1-117">Install the dual-write core solution</span></span>

<span data-ttu-id="1e7e1-118">二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-118">The dual-write core solution contains metadata for your entity maps and must be installed in your environments.</span></span>

1. <span data-ttu-id="1e7e1-119">Power Apps の左ウィンドウで、**ソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-119">In Power Apps, in the left pane, select **Solutions**.</span></span>
2. <span data-ttu-id="1e7e1-120">**AppSource を開く** を選択し、**二重書き込みコア** という名前のソリューションを検索します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-120">Select **Open AppSource**, and search for the solution that is named **Dual Write Core**.</span></span>
3. <span data-ttu-id="1e7e1-121">プロンプトに従ってソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-121">Follow the prompts to import the solution.</span></span>

    ![二重書き込みコア ソリューションのインポート](media/import-solution.png)

## <a name="install-the-dual-write-entity-maps-solution"></a><span data-ttu-id="1e7e1-123">二重書き込みエンティティ マップ ソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="1e7e1-123">Install the dual-write entity maps solution</span></span>

1. <span data-ttu-id="1e7e1-124">Power Apps の左ウィンドウで、**ソリューション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-124">In Power Apps, in the left pane, select **Solutions**.</span></span>
2. <span data-ttu-id="1e7e1-125">**AppSource を開く** を選択し、**Finance and Operations パッケージ用 Common Data Service アドイン** という名前のソリューションを検索します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-125">Select **Open AppSource**, and search for the solution that is named **Common Data Service Add-in for Finance and Operations package**.</span></span>
3. <span data-ttu-id="1e7e1-126">プロンプトに従ってソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-126">Follow the prompts to import the solution.</span></span>
4. <span data-ttu-id="1e7e1-127">Finance and Operations アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたエンティティ マップを適用します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-127">In the Finance and Operations app, on the **Dual-write** page, select **Apply Solution** to apply the entity maps that you downloaded and installed.</span></span> <span data-ttu-id="1e7e1-128">ソリューションを適用すると、既定のエンティティ マップが公開されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-128">After you apply the solution, you will see that the default entity maps are published.</span></span>

    ![二重書き込みエンティティ マップの公開](media/default-entity-maps.png)

<span data-ttu-id="1e7e1-130">Microsoft が発行した二重書き込みエンティティ マップ ソリューションを環境に正常にインポートして適用しました。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-130">You've now successfully imported and applied a Microsoft-published dual-write entity maps solution to your environment.</span></span>

## <a name="import-entity-maps-through-a-dual-write-solution-and-apply-them-to-your-environment-new-environments"></a><span data-ttu-id="1e7e1-131">二重書き込みソリューションを使用してエンティティ マップをインポートし、環境に適用する (新しい環境)</span><span class="sxs-lookup"><span data-stu-id="1e7e1-131">Import entity maps through a dual-write solution and apply them to your environment (New environments)</span></span>

<span data-ttu-id="1e7e1-132">このセクションでは、AppSource からエンティティ マップをインポートし、環境に適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-132">This section explains how to import entity maps from AppSource and apply them to your environment.</span></span>

![エンティティマップのインポートと適用](media/import-apply-entity-maps.png)
    
1. <span data-ttu-id="1e7e1-134">二重書き込みコア ソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-134">Import the dual-write core solution.</span></span>

    1. <span data-ttu-id="1e7e1-135">新しい二重書き込み環境 (Finance and Operations アプリ環境と Common Data Service 環境) を作成します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-135">Create a new dual-write environment (a Finance and Operations app environment and a Common Data Service environment).</span></span>
    2. <span data-ttu-id="1e7e1-136">このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、AppSource の二重書き込みコア ソリューションを Power Apps にインストールします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-136">Follow the instructions in the [Install the dual-write core solution](#install-the-dual-write-core-solution) section earlier in this topic to install the dual-write core solution from AppSource in Power Apps.</span></span>
    3. <span data-ttu-id="1e7e1-137">二重書き込みコア ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-137">Verify that the dual-write core solution is listed under **Solutions** in Power Apps.</span></span>

2. <span data-ttu-id="1e7e1-138">Microsoft 公開、または ISV 公開のエンティティー マップ ソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-138">Import the Microsoft-published or ISV-published entity maps solution.</span></span>

    1. <span data-ttu-id="1e7e1-139">[二重書き込みエンティティ マップ ソリューションのインストール](#install-the-dual-write-entity-maps-solution) の手順に従って、Power Apps の AppSource から Microsoft 公開、または ISV 公開のエンティティー マップをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-139">Follow the instructions in the [Install the dual-write entity maps solution](#install-the-dual-write-entity-maps-solution) section to download and install the Microsoft-published or ISV-published entity maps from AppSource in Power Apps.</span></span>
    2. <span data-ttu-id="1e7e1-140">エンティティー マップ ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-140">Verify that the entity maps solution is listed under **Solutions** in Power Apps.</span></span>

3. <span data-ttu-id="1e7e1-141">Finance and Operations アプリ環境に二重書き込みエンティティ マップ ソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-141">Apply the dual-write entity maps solution to your Finance and Operations app environment.</span></span>

    <span data-ttu-id="1e7e1-142">[二重書き込みエンティティ マップ ソリューションのインストール](#install-the-dual-write-entity-maps-solution) セクションの説明に従って、Finance and Operations アプリの **二重書き込み** ページで **ソリューションの適用** を選択し、ダウンロードしたソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-142">Apply the solution that you downloaded by selecting **Apply Solutions** on the **Dual-write** page in the Finance and Operations app, as described in the [Install the dual-write entity maps solution](#install-the-dual-write-entity-maps-solution) section.</span></span>

## <a name="update-entity-maps-and-export-them-to-other-environments-as-a-solution"></a><span data-ttu-id="1e7e1-143">エンティティ マップを更新し、ソリューションとして他の環境にエクスポートします</span><span class="sxs-lookup"><span data-stu-id="1e7e1-143">Update entity maps and export them to other environments as a solution</span></span>

<span data-ttu-id="1e7e1-144">このセクションでは、カスタマイズ済みエンティティ マップをソリューションとしてエクスポートし、それをバックアップとして使用して、環境間でアーティファクトを移動し、AppSource に発行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-144">This section explains how to export your customized entity maps as a solution, use it as a backup, and move the artifacts across environments and/or publish them to AppSource.</span></span>

![カスタマイズされたマップをソリューションとしてエクスポート](media/export-maps-solution.png)

### <a name="customize-your-entity-maps"></a><span data-ttu-id="1e7e1-146">エンティティ マップのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="1e7e1-146">Customize your entity maps</span></span>

<span data-ttu-id="1e7e1-147">最初の手順では、既存のエンティティ マップを変更し、新しいエンティティ マップを追加することによって、エンティティ マップをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-147">The first step is to customize your entity maps by modifying existing entity maps and adding a new entity map.</span></span>

1. <span data-ttu-id="1e7e1-148">Finance and Operations アプリの **エンティティ マッピング** タブで、ソリューションを使用してインストールした既定のエンティティ マップのマッピングをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-148">In the Finance and Operations app, on the **Entity mappings** tab, customize the mappings for the default entity map that you just installed by using a solution.</span></span> <span data-ttu-id="1e7e1-149">新しいエンティティ マップを追加するには、**エンティティの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-149">To add a new entity map, select **Add Entity**.</span></span> <span data-ttu-id="1e7e1-150">どちらの場合も、エンティティ マップを保存するときに、パブリッシャーとバージョン番号を指定するように求められます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-150">In both cases, when you save the entity map, you're prompted to specify the publisher and the version number.</span></span>

    <span data-ttu-id="1e7e1-151">次の図は、**生年月日** という名前の新しいフィールドを連絡先 - CDS 連絡先 V2 エンティティ マップに追加して、既定のパブリッシャーを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-151">The following figure shows how to add a new field that is named **birthday** to the contacts - CDS Contacts V2 entity map and select the default publisher.</span></span>

    ![新しい生年月日フィールドの追加](media/add-new-birthday-field.png)

    > [!NOTE]
    > <span data-ttu-id="1e7e1-153">これらの変更済みエンティティ マップを使用して [新しいソリューションを作成する](#create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps) 場合は、同じパブリッシャーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-153">When you [create a new solution](#create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps) by using these modified entity maps, you must specify the same publisher.</span></span>

    <span data-ttu-id="1e7e1-154">次の図は、**アドレス帳** という名前の新しいエンティティ マップを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-154">The following figure shows how to add a new entity map that is named **Address books**.</span></span>

    ![新しいアドレス帳エンティティ マップの追加](media/add-address-book.png)

2. <span data-ttu-id="1e7e1-156">変更および追加したエンティティ マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-156">Confirm the entity maps that you just modified and added.</span></span> <span data-ttu-id="1e7e1-157">それらを有効にしてテストし、期待どおりに機能することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-157">Be sure to enable and test them, to ensure that they work as you expect.</span></span>

    ![新しいアドレス帳エンティティ マップの追加](media/confirm-new-entity-maps.png)

### <a name="create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps"></a><span data-ttu-id="1e7e1-159">新しい二重書き込みソリューションを作成し、コンポーネントを追加する (カスタマイズ済みエンティティ マップ)</span><span class="sxs-lookup"><span data-stu-id="1e7e1-159">Create a new dual-write solution and add your components (Customized entity maps)</span></span>

<span data-ttu-id="1e7e1-160">マッピングをカスタマイズして新しいマッピングを追加したので、次の手順では、新しい二重書き込みソリューションを作成し、エンティティ マップを追加します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-160">Now that you've customized your mappings and added new mappings, the next step is to create a new dual-write solution and add the entity maps to it.</span></span>

1. <span data-ttu-id="1e7e1-161">Power Apps の左ウィンドウで **ソリューション** を選択し、次に **新しいソリューション** を選択して、ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-161">In Power Apps, in the left pane, select **Solutions**, and then select **New solution** to create a solution.</span></span> <span data-ttu-id="1e7e1-162">この例では、ソリューションの名前は **MyCustomEntityMaps** です。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-162">For this example, the solution is named **MyCustomEntityMaps**.</span></span> <span data-ttu-id="1e7e1-163">前の手順で選択したのと同じパブリッシャーを選択してください。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-163">Be sure to select the same publisher that you selected in previous steps.</span></span>

    ![新しいソリューションの作成とエンティティ マップの追加](media/add-map-to-solution.png)

2. <span data-ttu-id="1e7e1-165">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-165">Select **Create**.</span></span> <span data-ttu-id="1e7e1-166">新しいソリューションが **ソリューション** 一覧ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-166">The new solution appears on the **Solutions** list page.</span></span>

    ![ソリューション 一覧ページの新しいソリューション](media/show-new-solution.png)

3. <span data-ttu-id="1e7e1-168">二重書き込みソリューションを作成したので、前の手順で作成したカスタマイズ済みエンティティ マップを追加できます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-168">Now that you've created your dual-write solution, you can add the customized entity maps that you created in previous steps.</span></span> <span data-ttu-id="1e7e1-169">作成した **MyCustomEntityMaps** ソリューションを選択し、**既存の追加** を選択して、**その他** をポイントし、**二重書き込みエンティティ マップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-169">Select the **MyCustomEntityMaps** solution that you just created, select **Add existing**, point to **Other**, and then select **Dual Write entity map**.</span></span>

    ![カスタマイズ済みエンティティ マップをソリューションに追加](media/add-customized-maps.png)

4. <span data-ttu-id="1e7e1-171">一覧で、カスタマイズ済みエンティティ マップを選択し、ソリューションに追加します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-171">In the list, select the customized entity maps, and add them to the solution.</span></span> <span data-ttu-id="1e7e1-172">ソリューションには、カスタマイズ済みエンティティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-172">The solution should now contain your customized entities.</span></span>

    ![新しいソリューションのカスタマイズ済みエンティティ](media/entities-new-solution.png)

<span data-ttu-id="1e7e1-174">これで、エンティティをカスタマイズし、ソリューションに追加しました。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-174">You've now customized your entities and put them into a solution.</span></span>

### <a name="export-and-publish-your-solution"></a><span data-ttu-id="1e7e1-175">ソリューションのエクスポートと発行</span><span class="sxs-lookup"><span data-stu-id="1e7e1-175">Export and publish your solution</span></span>

<span data-ttu-id="1e7e1-176">ソリューション チェッカーを実行して問題がないことを確認したら、作成したソリューションをエクスポートし、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-176">After you run the solution checker and make sure that there are no issues, you export the solution that you created and publish the changes.</span></span>

1. <span data-ttu-id="1e7e1-177">ソリューションの一覧でソリューションを選択し、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-177">In the list of solutions, select your solution, and then select **Export**.</span></span>
2. <span data-ttu-id="1e7e1-178">バージョン番号を更新し、ソリューションをマネージドまたはアンマネージド ソリューションとしてエクスポートするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-178">Update the version number, and select whether you want to export the solution as a managed or unmanaged solution.</span></span> <span data-ttu-id="1e7e1-179">(マネージド ソリューションとしてエクスポートすることをお勧めします。) 次に **エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-179">(We recommend that you export it as a managed solution.) Then select **Export**.</span></span>

    ![バージョン番号の更新とエクスポート](media/update-version-number.png)

3. <span data-ttu-id="1e7e1-181">エクスポートする前に、**すべての変更の公開** を選択し、**問題点を確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-181">Before you export, select **Publish all changes**, and then select **Check for issues**.</span></span> <span data-ttu-id="1e7e1-182">完了したら、**次へ** を選択して、すべての変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-182">When you've finished, select **Next** to publish all your changes.</span></span>

    ![変更の公開](media/export-and-publish.png)

    <span data-ttu-id="1e7e1-184">ソリューションは、そのすべてのコンポーネントと共に ZIP ファイルにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-184">The solution, together with all its components, is exported to a zip file.</span></span>

    ![ZIP ファイルにエクスポートされたソリューション](media/components-to-zip.png)
    
<span data-ttu-id="1e7e1-186">これで、エンティティをカスタマイズして、新しいソリューションに追加し、他の環境にインポートして適用できるソリューション ファイルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-186">You've now customized your entities, added them to a new solution, and created a solution file that can be imported and applied to other environments.</span></span> <span data-ttu-id="1e7e1-187">(この機能は、テスト環境と実稼動環境の間でエンティティ マップを移動する場合に役立ちます。) 同様に、すべてのエンティティ マップのバックアップを、ソリューションに追加し、そのソリューションをパッケージとしてエクスポートすることによって作成できます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-187">(This capability can be useful if you want to move entity maps between test and production environments.) In a similar way, you can create a backup of all your entity maps by adding them to a solution and exporting the solution as a package.</span></span> <span data-ttu-id="1e7e1-188">その後、そのパッケージを任意の環境にインポートして、エンティティ マップを復元できます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-188">That package can then be imported into to any environment to restore the entity maps.</span></span>

<span data-ttu-id="1e7e1-189">AppSource にパッケージを公開する方法の詳細については、[AppSource でアプリを公開](https://docs.microsoft.com/powerapps/developer/common-data-service/publish-app-appsource) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-189">For information about how to publish the package to AppSource, see [Publish your app on AppSource](https://docs.microsoft.com/powerapps/developer/common-data-service/publish-app-appsource).</span></span>

### <a name="test-your-exported-solution-package"></a><span data-ttu-id="1e7e1-190">エクスポート済みソリューション パッケージのテスト</span><span class="sxs-lookup"><span data-stu-id="1e7e1-190">Test your exported solution package</span></span>

<span data-ttu-id="1e7e1-191">エクスポート済みソリューション パッケージは、インポートして別の環境に適用することでテストできます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-191">You can test your exported solution package by importing and applying it to another environment.</span></span>

1. <span data-ttu-id="1e7e1-192">Power Apps で、**インポート** を選択し、パッケージを新しい環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-192">In Power Apps, select **Import** to import the package into a new environment.</span></span>

    ![パッケージを新しい環境にインポート](media/import-package.png)

2. <span data-ttu-id="1e7e1-194">環境にインポートしたばかりのソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-194">Apply the solution that you just imported to the environment.</span></span>

    ![ソリューションを環境に適用](media/apply-solution-to-environment.png)

3. <span data-ttu-id="1e7e1-196">2 つのカスタマイズ済みエンティティ マップが、[二重書き込みエンティティ マップ] 一覧ページに表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-196">Verify that the two customized entity maps appear on the dual-write entity maps list page.</span></span>

    ![[リスト] ページの 2 つのカスタマイズ済みエンティティ マップ](media/entity-maps-in-list.png)

4. <span data-ttu-id="1e7e1-198">前の手順で行ったカスタマイズが保持されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-198">Make sure that the customizations from previous steps are preserved.</span></span>

    ![カスタマイズが保持されていることの確認](media/check-customizations.png)

### <a name="use-the-entity-map-version"></a><span data-ttu-id="1e7e1-200">エンティティ マップ バージョンの使用</span><span class="sxs-lookup"><span data-stu-id="1e7e1-200">Use the entity map version</span></span>

<span data-ttu-id="1e7e1-201">ソリューションには、エンティティ マップの異なる実装が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-201">Sometimes, a solution might contain different implementations of an entity map.</span></span> <span data-ttu-id="1e7e1-202">たとえば、連絡先 - CDS 連絡先 V2 エンティティ マップのバージョンには、異なるパブリッシャーまたはより新しいバージョン番号が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-202">For example, the version of the contacts - CDS Contacts V2 entity map might have a different publisher or a newer version number.</span></span> <span data-ttu-id="1e7e1-203">このような場合、**エンティティ マップ バージョン** ボタンを使用して、環境で使用するエンティティ マップを選択できます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-203">In these cases, you can use the **Entity Map version** button to select which entity map you want to use in your environment.</span></span>

![環境で使用するエンティティ マップの選択](media/select-entity-map.png)

## <a name="upgrade-existing-dual-write-environments-for-solution-awareness-existing-environments"></a><span data-ttu-id="1e7e1-205">ソリューション認識の既存の二重書き込み環境をアップグレードする (既存の環境)</span><span class="sxs-lookup"><span data-stu-id="1e7e1-205">Upgrade existing dual-write environments for solution awareness (Existing environments)</span></span>

1. <span data-ttu-id="1e7e1-206">二重書き込みコア ソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-206">Import the dual-write core solution.</span></span>

    1. <span data-ttu-id="1e7e1-207">このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、二重書き込みコア ソリューションを AppSource から Power Apps にインポートします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-207">Follow the instructions in the [Install the dual-write core solution](#install-the-dual-write-core-solution) section earlier in this topic to import the dual-write core solution from AppSource into Power Apps.</span></span>
    2. <span data-ttu-id="1e7e1-208">二重書き込みコア ソリューションが PowerApps の **ソリューション** の下に一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-208">Verify that the dual-write core solution is listed under **Solutions** in PowerApps.</span></span>

2. <span data-ttu-id="1e7e1-209">エンティティ マップをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-209">Upgrade the entity maps.</span></span>

    <span data-ttu-id="1e7e1-210">アップグレードを促す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-210">You'll see a notification prompting you to upgrade.</span></span>

    ![エンティティ マップをアップグレードするプロンプト](media/upgrade-prompt.png)

    <span data-ttu-id="1e7e1-212">ページ上部の **エンティティ マップのアップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-212">Select **Upgrade entity maps** at the top of the page.</span></span>

    ![エンティティ マップのアップグレード](media/upgrade-entity-maps.png)

<span data-ttu-id="1e7e1-214">アップグレードには数分かかります。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-214">The upgrade takes a few minutes.</span></span> <span data-ttu-id="1e7e1-215">完了すると、通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="1e7e1-215">When it's completed, you receive a notification.</span></span>
