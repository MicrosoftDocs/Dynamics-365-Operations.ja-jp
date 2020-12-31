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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abdd2fd543ce34a7d92ddabaa4f562c995e246f4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685653"
---
# <a name="application-lifecycle-management"></a><span data-ttu-id="9db1a-103">アプリケーション ライフサイクル管理</span><span class="sxs-lookup"><span data-stu-id="9db1a-103">Application lifecycle management</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9db1a-104">二重書き込みソリューションに対応することで、環境全体での二重書き込みテーブル マップの転送やバックアップ/復元など、基本的なアプリケーション ライフサイクル管理 (ALM) 機能を実現できます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-104">By making dual-write solution-aware, you enable basic application lifecycle management (ALM) capabilities, such as transportation and backup/restore of dual-write table maps across environments.</span></span> <span data-ttu-id="9db1a-105">また、AppSource から Microsoft または独立系ソフトウェア ベンダー (ISV) が公開するソリューションを入手できるシナリオも有効にします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-105">You also enable scenarios where you can get solutions that are published by Microsoft or an independent software vendor (ISV) from AppSource.</span></span>

## <a name="what-is-a-dual-write-solution"></a><span data-ttu-id="9db1a-106">二重書き込みソリューションとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="9db1a-106">What is a dual-write solution?</span></span>

<span data-ttu-id="9db1a-107">二重書き込みソリューションには、1 つ以上の二重書き込み テーブル マップを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-107">A dual-write solution can contain one or more dual-write table maps.</span></span> <span data-ttu-id="9db1a-108">これらのマップは、ご使用の環境 (Microsoft Power Apps の **ソリューション** を選択) にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-108">These maps can be imported into your environment (by selecting **Solutions** in Microsoft Power Apps).</span></span> <span data-ttu-id="9db1a-109">また、パッケージとして他の環境にエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-109">They can also be exported to other environments as a package.</span></span> <span data-ttu-id="9db1a-110">Microsoft 公開のテーブル マップまたは ISV 公開のテーブル マップを AppSource からインポートして、テスト環境で変更し、テストして、準備が整ったら、実稼働環境にエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-110">You can import Microsoft-published or ISV-published table maps from AppSource, modify them in your test environment, test them, and then, when they are ready, export them to your production environment.</span></span> <span data-ttu-id="9db1a-111">また、AppSource でソリューションを公開して、他のユーザーが使用できるようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-111">Additionally, you can publish your solution through AppSource, so that other people can use it.</span></span>

<span data-ttu-id="9db1a-112">ソリューションには、マネージドとアンマネージドの 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="9db1a-112">There two types of solutions: managed and unmanaged.</span></span>

<span data-ttu-id="9db1a-113">マネージド ソリューションを変更することはできませんが、インポート後にアンインストールできます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-113">A managed solution can't be modified, and it can be uninstalled after it's imported.</span></span> <span data-ttu-id="9db1a-114">アンマネージド ソリューションをインポートする場合は、そのソリューションのすべてのコンポーネントを環境に追加します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-114">When you import an unmanaged solution, you add all the components of that solution into your environment.</span></span> <span data-ttu-id="9db1a-115">既にカスタマイズしたコンポーネントを含むアンマネージド ソリューションをインポートすると、カスタマイズはインポート済みアンマネージド ソリューションのカスタマイズによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-115">When you import an unmanaged solution that contains components that you've already customized, your customizations are overwritten by the customizations in the imported unmanaged solution.</span></span>

<span data-ttu-id="9db1a-116">ソリューションの詳細については、[ソリューションの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9db1a-116">For more information about solutions, see the [solutions overview](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview).</span></span>

## <a name="install-the-dual-write-core-solution"></a><span data-ttu-id="9db1a-117">二重書き込みコア ソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="9db1a-117">Install the dual-write core solution</span></span>

<span data-ttu-id="9db1a-118">二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれており、環境にインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9db1a-118">The dual-write core solution contains metadata for your table maps and must be installed in your environments.</span></span>

1. <span data-ttu-id="9db1a-119">Power Apps の左ウィンドウで、**Solutions** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-119">In Power Apps, in the left pane, select **Solutions**.</span></span>
2. <span data-ttu-id="9db1a-120">**AppSource を開く** を選択し、**二重書き込みコア** という名前のソリューションを検索します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-120">Select **Open AppSource**, and search for the solution that is named **Dual Write Core**.</span></span>
3. <span data-ttu-id="9db1a-121">プロンプトに従ってソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-121">Follow the prompts to import the solution.</span></span>

    ![二重書き込みコア ソリューションのインポート](media/import-solution.png)

## <a name="install-the-dual-write-table-maps-solution"></a><a id="install-table-maps"></a> <span data-ttu-id="9db1a-123">二重書き込みテーブル マップ ソリューションのインストール</span><span class="sxs-lookup"><span data-stu-id="9db1a-123">Install the dual-write table maps solution</span></span>

1. <span data-ttu-id="9db1a-124">Power Apps の左ウィンドウで、**Solutions** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-124">In Power Apps, in the left pane, select **Solutions**.</span></span>
2. <span data-ttu-id="9db1a-125">**AppSource を開く** を選択し、**Finance and Operations パッケージ用 Dataverse アドイン** という名前のソリューションを検索します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-125">Select **Open AppSource**, and search for the solution that is named **Dataverse Add-in for Finance and Operations package**.</span></span>
3. <span data-ttu-id="9db1a-126">プロンプトに従ってソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-126">Follow the prompts to import the solution.</span></span>
4. <span data-ttu-id="9db1a-127">Finance and Operations アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたテーブル マップを適用します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-127">In the Finance and Operations app, on the **Dual-write** page, select **Apply Solution** to apply the table maps that you downloaded and installed.</span></span> <span data-ttu-id="9db1a-128">ソリューションを適用すると、既定のテーブル マップが公開されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-128">After you apply the solution, you will see that the default table maps are published.</span></span>

    ![二重書き込みテーブル マップの公開](media/default-entity-maps.png)

<span data-ttu-id="9db1a-130">Microsoft が公開した二重書き込みテーブル マップ ソリューションを環境に正常にインポートして適用しました。</span><span class="sxs-lookup"><span data-stu-id="9db1a-130">You've now successfully imported and applied a Microsoft-published dual-write table maps solution to your environment.</span></span>

## <a name="import-table-maps-through-a-dual-write-solution-and-apply-them-to-your-environment-new-environments"></a><span data-ttu-id="9db1a-131">二重書き込みソリューションを使用してテーブル マップをインポートし、環境に適用する (新しい環境)</span><span class="sxs-lookup"><span data-stu-id="9db1a-131">Import table maps through a dual-write solution and apply them to your environment (New environments)</span></span>

<span data-ttu-id="9db1a-132">このセクションでは、AppSource からテーブル マップをインポートし、環境に適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-132">This section explains how to import table maps from AppSource and apply them to your environment.</span></span>

![テーブル マップのインポートと適用](media/import-apply-entity-maps.png)

1. <span data-ttu-id="9db1a-134">二重書き込みコア ソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-134">Import the dual-write core solution.</span></span>

    1. <span data-ttu-id="9db1a-135">新しい二重書き込み環境 (Finance and Operations アプリ環境と Dataverse 環境) を作成します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-135">Create a new dual-write environment (a Finance and Operations app environment and a Dataverse environment).</span></span>
    2. <span data-ttu-id="9db1a-136">このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、AppSource の二重書き込みコア ソリューションを Power Apps にインストールします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-136">Follow the instructions in the [Install the dual-write core solution](#install-the-dual-write-core-solution) section earlier in this topic to install the dual-write core solution from AppSource in Power Apps.</span></span>
    3. <span data-ttu-id="9db1a-137">二重書き込みコア ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-137">Verify that the dual-write core solution is listed under **Solutions** in Power Apps.</span></span>

2. <span data-ttu-id="9db1a-138">Microsoft 公開、または ISV 公開のテーブル マップ ソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-138">Import the Microsoft-published or ISV-published table maps solution.</span></span>

    1. <span data-ttu-id="9db1a-139">[二重書き込みテーブル マップ ソリューションのインストール](#install-table-maps) の手順に従って、Power Apps の AppSource から Microsoft 公開、または ISV 公開のテーブル マップをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-139">Follow the instructions in the [Install the dual-write table maps solution](#install-table-maps) section to download and install the Microsoft-published or ISV-published table maps from AppSource in Power Apps.</span></span>
    2. <span data-ttu-id="9db1a-140">テーブル マップ ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-140">Verify that the table maps solution is listed under **Solutions** in Power Apps.</span></span>

3. <span data-ttu-id="9db1a-141">Finance and Operations アプリ環境に二重書き込みテーブル マップ ソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-141">Apply the dual-write table maps solution to your Finance and Operations app environment.</span></span>

    <span data-ttu-id="9db1a-142">[二重書き込みテーブル マップ ソリューションのインストール](#install-table-maps) セクションの説明に従って、Finance and Operations アプリの **二重書き込み** ページで **ソリューションの適用** を選択し、ダウンロードしたソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-142">Apply the solution that you downloaded by selecting **Apply Solutions** on the **Dual-write** page in the Finance and Operations app, as described in the [Install the dual-write table maps solution](#install-table-maps) section.</span></span>

## <a name="update-table-maps-and-export-them-to-other-environments-as-a-solution"></a><a id="update-table-maps"></a> <span data-ttu-id="9db1a-143">テーブル マップを更新し、ソリューションとして他の環境にエクスポートします</span><span class="sxs-lookup"><span data-stu-id="9db1a-143">Update table maps and export them to other environments as a solution</span></span>

<span data-ttu-id="9db1a-144">このセクションでは、カスタマイズ済みテーブル マップをソリューションとしてエクスポートし、それをバックアップとして使用して、環境間でアーティファクトを移動し、AppSource に発行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-144">This section explains how to export your customized table maps as a solution, use it as a backup, and move the artifacts across environments and/or publish them to AppSource.</span></span>

![カスタマイズされたマップをソリューションとしてエクスポート](media/export-maps-solution.png)

### <a name="customize-your-table-maps"></a><span data-ttu-id="9db1a-146">テーブル マップのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="9db1a-146">Customize your table maps</span></span>

<span data-ttu-id="9db1a-147">最初の手順では、既存のテーブル マップを変更し、新しいテーブル マップを追加することによって、テーブル マップをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-147">The first step is to customize your table maps by modifying existing table maps and adding a new table map.</span></span>

1. <span data-ttu-id="9db1a-148">Finance and Operations アプリの **テーブル マッピング** タブで、ソリューションを使用してインストールした既定のテーブル マップのマッピングをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-148">In the Finance and Operations app, on the **Table mappings** tab, customize the mappings for the default table map that you just installed by using a solution.</span></span> <span data-ttu-id="9db1a-149">新しいテーブル マップを追加するには、**テーブルの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-149">To add a new table map, select **Add Table**.</span></span> <span data-ttu-id="9db1a-150">どちらの場合も、テーブル マップを保存するときに、パブリッシャーとバージョン番号を指定するように求められます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-150">In both cases, when you save the table map, you're prompted to specify the publisher and the version number.</span></span>

    <span data-ttu-id="9db1a-151">次の図は、**生年月日** という名前の新しいフィールドを連絡先 - CDS 連絡先 V2 テーブル マップに追加して、既定のパブリッシャーを選択する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9db1a-151">The following figure shows how to add a new field that is named **birthday** to the contacts - CDS Contacts V2 table map and select the default publisher.</span></span>

    ![新しい生年月日フィールドの追加](media/add-new-birthday-field.png)

    > [!NOTE]
    > <span data-ttu-id="9db1a-153">これらの変更済みテーブル マップを使用して[新しいソリューションを作成する](#create-new-solution) 場合は、同じパブリッシャーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9db1a-153">When you [create a new solution](#create-new-solution) by using these modified table maps, you must specify the same publisher.</span></span>

    <span data-ttu-id="9db1a-154">次の図は、**アドレス帳** という名前の新しいテーブル マップを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9db1a-154">The following figure shows how to add a new table map that is named **Address books**.</span></span>

    ![新しいアドレス帳テーブル マップの追加](media/add-address-book.png)

2. <span data-ttu-id="9db1a-156">変更および追加したテーブル マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-156">Confirm the table maps that you just modified and added.</span></span> <span data-ttu-id="9db1a-157">それらを有効にしてテストし、期待どおりに機能することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9db1a-157">Be sure to enable and test them, to ensure that they work as you expect.</span></span>

    ![新しいテーブル マップの確認](media/confirm-new-entity-maps.png)

### <a name="create-a-new-dual-write-solution-and-add-your-components-customized-table-maps"></a><a id="create-new-solution"></a> <span data-ttu-id="9db1a-159">新しい二重書き込みソリューションを作成し、コンポーネントを追加する (カスタマイズ済みテーブル マップ)</span><span class="sxs-lookup"><span data-stu-id="9db1a-159">Create a new dual-write solution and add your components (Customized table maps)</span></span>

<span data-ttu-id="9db1a-160">マッピングをカスタマイズして新しいマッピングを追加したので、次の手順では、新しい二重書き込みソリューションを作成し、テーブル マップを追加します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-160">Now that you've customized your mappings and added new mappings, the next step is to create a new dual-write solution and add the table maps to it.</span></span>

1. <span data-ttu-id="9db1a-161">Power Apps の左ウィンドウで **ソリューション** を選択し、次に **新しいソリューション** を選択して、ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-161">In Power Apps, in the left pane, select **Solutions**, and then select **New solution** to create a solution.</span></span> <span data-ttu-id="9db1a-162">この例では、ソリューションの名前は **MyCustomTableMaps** です。</span><span class="sxs-lookup"><span data-stu-id="9db1a-162">For this example, the solution is named **MyCustomTableMaps**.</span></span> <span data-ttu-id="9db1a-163">前の手順で選択したのと同じパブリッシャーを選択してください。</span><span class="sxs-lookup"><span data-stu-id="9db1a-163">Be sure to select the same publisher that you selected in previous steps.</span></span>

    ![新しいソリューションの作成とテーブル マップの追加](media/add-map-to-solution.png)

2. <span data-ttu-id="9db1a-165">**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-165">Select **Create**.</span></span> <span data-ttu-id="9db1a-166">新しいソリューションが **ソリューション** 一覧ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-166">The new solution appears on the **Solutions** list page.</span></span>

    ![ソリューション 一覧ページの新しいソリューション](media/show-new-solution.png)

3. <span data-ttu-id="9db1a-168">二重書き込みソリューションを作成したので、前の手順で作成したカスタマイズ済みテーブル マップを追加できます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-168">Now that you've created your dual-write solution, you can add the customized table maps that you created in previous steps.</span></span> <span data-ttu-id="9db1a-169">作成した **MyCustomTableMaps** ソリューションを選択し、**既存の追加** を選択して、**その他** をポイントし、**二重書き込みテーブル マップ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-169">Select the **MyCustomTableMaps** solution that you just created, select **Add existing**, point to **Other**, and then select **Dual Write table map**.</span></span>

    ![カスタマイズ済みテーブル マップをソリューションに追加](media/add-customized-maps.png)

4. <span data-ttu-id="9db1a-171">一覧で、カスタマイズ済みテーブル マップを選択し、ソリューションに追加します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-171">In the list, select the customized table maps, and add them to the solution.</span></span> <span data-ttu-id="9db1a-172">ソリューションには、カスタマイズ済みテーブルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-172">The solution should now contain your customized tables.</span></span>

    ![新しいソリューションのカスタマイズ済みテーブル](media/entities-new-solution.png)

<span data-ttu-id="9db1a-174">これで、テーブルをカスタマイズし、ソリューションに追加しました。</span><span class="sxs-lookup"><span data-stu-id="9db1a-174">You've now customized your tables and put them into a solution.</span></span>

### <a name="export-and-publish-your-solution"></a><span data-ttu-id="9db1a-175">ソリューションのエクスポートと発行</span><span class="sxs-lookup"><span data-stu-id="9db1a-175">Export and publish your solution</span></span>

<span data-ttu-id="9db1a-176">ソリューション チェッカーを実行して問題がないことを確認したら、作成したソリューションをエクスポートし、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-176">After you run the solution checker and make sure that there are no issues, you export the solution that you created and publish the changes.</span></span>

1. <span data-ttu-id="9db1a-177">ソリューションの一覧でソリューションを選択し、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-177">In the list of solutions, select your solution, and then select **Export**.</span></span>
2. <span data-ttu-id="9db1a-178">バージョン番号を更新し、ソリューションをマネージドまたはアンマネージド ソリューションとしてエクスポートするかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-178">Update the version number, and select whether you want to export the solution as a managed or unmanaged solution.</span></span> <span data-ttu-id="9db1a-179">(マネージド ソリューションとしてエクスポートすることをお勧めします。) 次に **エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-179">(We recommend that you export it as a managed solution.) Then select **Export**.</span></span>

    ![バージョン番号の更新とエクスポート](media/update-version-number.png)

3. <span data-ttu-id="9db1a-181">エクスポートする前に、**すべての変更の公開** を選択し、**問題点を確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-181">Before you export, select **Publish all changes**, and then select **Check for issues**.</span></span> <span data-ttu-id="9db1a-182">完了したら、**次へ** を選択して、すべての変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-182">When you've finished, select **Next** to publish all your changes.</span></span>

    ![変更の公開](media/export-and-publish.png)

    <span data-ttu-id="9db1a-184">ソリューションは、そのすべてのコンポーネントと共に ZIP ファイルにエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-184">The solution, together with all its components, is exported to a zip file.</span></span>

    ![ZIP ファイルにエクスポートされたソリューション](media/components-to-zip.png)

<span data-ttu-id="9db1a-186">これで、テーブルをカスタマイズして、新しいソリューションに追加し、他の環境にインポートして適用できるソリューション ファイルを作成しました。</span><span class="sxs-lookup"><span data-stu-id="9db1a-186">You've now customized your tables, added them to a new solution, and created a solution file that can be imported and applied to other environments.</span></span> <span data-ttu-id="9db1a-187">(この機能は、テスト環境と実稼動環境の間でテーブル マップを移動する場合に役立ちます。) 同様に、すべてのテーブル マップのバックアップを、ソリューションに追加し、そのソリューションをパッケージとしてエクスポートすることによって作成できます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-187">(This capability can be useful if you want to move table maps between test and production environments.) In a similar way, you can create a backup of all your table maps by adding them to a solution and exporting the solution as a package.</span></span> <span data-ttu-id="9db1a-188">その後、そのパッケージを任意の環境にインポートして、テーブル マップを復元できます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-188">That package can then be imported into to any environment to restore the table maps.</span></span>

<span data-ttu-id="9db1a-189">AppSource にパッケージを公開する方法の詳細については、[AppSource でアプリを公開](https://docs.microsoft.com/powerapps/developer/common-data-service/publish-app-appsource) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9db1a-189">For information about how to publish the package to AppSource, see [Publish your app on AppSource](https://docs.microsoft.com/powerapps/developer/common-data-service/publish-app-appsource).</span></span>

### <a name="test-your-exported-solution-package"></a><span data-ttu-id="9db1a-190">エクスポート済みソリューション パッケージのテスト</span><span class="sxs-lookup"><span data-stu-id="9db1a-190">Test your exported solution package</span></span>

<span data-ttu-id="9db1a-191">エクスポート済みソリューション パッケージは、インポートして別の環境に適用することでテストできます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-191">You can test your exported solution package by importing and applying it to another environment.</span></span>

1. <span data-ttu-id="9db1a-192">Power Apps で、**インポート** を選択し、パッケージを新しい環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-192">In Power Apps, select **Import** to import the package into a new environment.</span></span>

    ![パッケージを新しい環境にインポート](media/import-package.png)

2. <span data-ttu-id="9db1a-194">環境にインポートしたばかりのソリューションを適用します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-194">Apply the solution that you just imported to the environment.</span></span>

    ![ソリューションを環境に適用](media/apply-solution-to-environment.png)

3. <span data-ttu-id="9db1a-196">2 つのカスタマイズ済みテーブル マップが、二重書き込みテーブル マップの一覧ページに表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-196">Verify that the two customized table maps appear on the dual-write table maps list page.</span></span>

    ![一覧ページの 2 つのカスタマイズ済みテーブル マップ](media/entity-maps-in-list.png)

4. <span data-ttu-id="9db1a-198">前の手順で行ったカスタマイズが保持されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-198">Make sure that the customizations from previous steps are preserved.</span></span>

    ![カスタマイズが保持されていることの確認](media/check-customizations.png)

### <a name="use-the-table-map-version"></a><span data-ttu-id="9db1a-200">テーブル マップ バージョンの使用</span><span class="sxs-lookup"><span data-stu-id="9db1a-200">Use the table map version</span></span>

<span data-ttu-id="9db1a-201">ソリューションには、テーブル マップの異なる実装が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9db1a-201">Sometimes, a solution might contain different implementations of an table map.</span></span> <span data-ttu-id="9db1a-202">たとえば、連絡先 - CDS 連絡先 V2 テーブル マップのバージョンには、異なるパブリッシャーまたはより新しいバージョン番号が含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9db1a-202">For example, the version of the contacts - CDS Contacts V2 table map might have a different publisher or a newer version number.</span></span> <span data-ttu-id="9db1a-203">このような場合、**テーブル マップ バージョン** ボタンを使用して、環境で使用するテーブル マップを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-203">In these cases, you can use the **Table Map version** button to select which table map you want to use in your environment.</span></span>

![環境で使用するテーブル マップの選択](media/select-entity-map.png)

## <a name="upgrade-existing-dual-write-environments-for-solution-awareness-existing-environments"></a><span data-ttu-id="9db1a-205">ソリューション認識の既存の二重書き込み環境をアップグレードする (既存の環境)</span><span class="sxs-lookup"><span data-stu-id="9db1a-205">Upgrade existing dual-write environments for solution awareness (Existing environments)</span></span>

1. <span data-ttu-id="9db1a-206">二重書き込みコア ソリューションをインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-206">Import the dual-write core solution.</span></span>

    1. <span data-ttu-id="9db1a-207">このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、二重書き込みコア ソリューションを AppSource から Power Apps にインポートします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-207">Follow the instructions in the [Install the dual-write core solution](#install-the-dual-write-core-solution) section earlier in this topic to import the dual-write core solution from AppSource into Power Apps.</span></span>
    2. <span data-ttu-id="9db1a-208">二重書き込みコア ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-208">Verify that the dual-write core solution is listed under **Solutions** in Power Apps.</span></span>

2. <span data-ttu-id="9db1a-209">テーブル マップをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="9db1a-209">Upgrade the table maps.</span></span>

    <span data-ttu-id="9db1a-210">アップグレードを促す通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-210">You'll see a notification prompting you to upgrade.</span></span>

    ![テーブル マップをアップグレードするプロンプト](media/upgrade-prompt.png)

    <span data-ttu-id="9db1a-212">ページ上部の **テーブル マップのアップグレード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9db1a-212">Select **Upgrade table maps** at the top of the page.</span></span>

    ![テーブル マップのアップグレード](media/upgrade-entity-maps.png)

<span data-ttu-id="9db1a-214">アップグレードには数分かかります。</span><span class="sxs-lookup"><span data-stu-id="9db1a-214">The upgrade takes a few minutes.</span></span> <span data-ttu-id="9db1a-215">完了すると、通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9db1a-215">When it's completed, you receive a notification.</span></span>
