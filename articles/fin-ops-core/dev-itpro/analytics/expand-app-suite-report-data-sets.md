---
title: アプリケーション スイート レポート データ セットを展開する
description: このトピックでは、レポート データ プロバイダー (RDP) クラスで X++ ビジネス ロジックを使用して作成された既存のレポート データ セットを拡張する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 266594
ms.assetid: 7810ee2c-e012-4a0f-992c-840e626bf437
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 94b4646344d519742de33e2e9aaf0704fc6c10fb
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026148"
---
# <a name="expand-application-suite-report-data-sets"></a><span data-ttu-id="d19b5-103">アプリケーション スイート レポート データ セットを展開する</span><span class="sxs-lookup"><span data-stu-id="d19b5-103">Expand Application Suite report data sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d19b5-104">このトピックでは、レポート データ プロバイダー (RDP) クラスで X++ ビジネス ロジックを使用して作成された既存のレポート データ セットを拡張する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-104">This topic shows how to expand an existing report data set that is produced by using X++ business logic in a report data provider (RDP) class.</span></span>

<span data-ttu-id="d19b5-105">このトピックでは、レポート データ プロバイダー (RDP) クラスで X++ ビジネス ロジックを使用して作成された既存のレポート データ セットの拡張について説明します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-105">This topic focuses on the expansion of an existing report data set that is produced by using X++ business logic in a report data provider (RDP) class.</span></span> <span data-ttu-id="d19b5-106">カスタムのデリゲート ハンドラーおよびテーブル拡張機能を使用して、追加のフィールド データと計算の両方またはいずれかを含めます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-106">You use custom delegate handlers and table extensions to include additional field data and/or calculations.</span></span> <span data-ttu-id="d19b5-107">アプリケーション スイートを重層化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d19b5-107">You don't have to over-layer the Application Suite.</span></span> <span data-ttu-id="d19b5-108">次に、標準のアプリケーション ソリューションを置き換えてデータをユーザーに提供する、カスタムのデザインを作成します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-108">You then create custom designs that replace the standard application solutions and present the data to users.</span></span> <span data-ttu-id="d19b5-109">次の図は、このトピックで説明されている一般的なアプリケーションのカスタマイズを示しています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-109">The following illustration shows a typical application customization, as described in this topic.</span></span>

<span data-ttu-id="d19b5-110">[![extendingdatasets](./media/extendingdatasets.png)](./media/extendingdatasets.png)</span><span class="sxs-lookup"><span data-stu-id="d19b5-110">[![extendingdatasets](./media/extendingdatasets.png)](./media/extendingdatasets.png)</span></span>

## <a name="whats-important-to-know"></a><span data-ttu-id="d19b5-111">知っている必要がある重要なこと</span><span class="sxs-lookup"><span data-stu-id="d19b5-111">What's important to know?</span></span>
<span data-ttu-id="d19b5-112">このソリューションを適用する前に知っておくべき基本的な前提がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="d19b5-112">There are a few basic assumptions that you should be aware of before you apply this solution.</span></span>

- <span data-ttu-id="d19b5-113">**RDP クラスを直接拡張することはできません。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-113">**You can't directly extend RDP classes.**</span></span> <span data-ttu-id="d19b5-114">ただし、プラットフォームは、標準のアプリケーションのビジネス ロジックを複製せずにデータ セットの拡張を有効にする拡張ポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-114">However, the platform provides extension points that enable data set expansion without duplicating business logic in the standard application.</span></span>
- <span data-ttu-id="d19b5-115">**レポート データ セットを展開するために使用できる 2 つの方法があります。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-115">**There are two methods that can be used to expand report data sets.**</span></span> <span data-ttu-id="d19b5-116">ソリューションに適した戦略を使用します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-116">Use the strategy that is appropriate for your solution:</span></span>

    - <span data-ttu-id="d19b5-117">**データ処理ポストハンドラー** - このメソッドは、**ProcessReport** メソッドが完了して、データ セットがレポート サーバーに返される前に、1 回だけ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-117">**Data processing post-handler** – This method is called only one time, after the **ProcessReport** method is completed and before the data set is returned to the report server.</span></span> <span data-ttu-id="d19b5-118">このポスト ハンドラーを登録し、標準アプリケーション ソリューションによって生成される一時的なデータ セットに対して一括更新を実行します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-118">Register for this post-handler to perform bulk updates on the temporary data set that is produced by the standard application solution.</span></span>
    - <span data-ttu-id="d19b5-119">**イベントを挿入する一時テーブル** – このメソッドは、一時テーブルに追加される各行に対して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-119">**Temp table inserting event** – This method is called for each row that is added to the temporary table.</span></span> <span data-ttu-id="d19b5-120">これは計算およびインラインの評価により適しています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-120">It's more suitable for calculations and inline evaluations.</span></span> <span data-ttu-id="d19b5-121">ジョイン操作やルックアップ操作が多い負担のかかるクエリは避けてください。</span><span class="sxs-lookup"><span data-stu-id="d19b5-121">Try to avoid expensive queries that have many joins and look-up operations.</span></span>

- <span data-ttu-id="d19b5-122">**イベントハンドラーを使用して、メニュー項目を新しいレポート デザインにリダイレクトします。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-122">**Use event handlers to redirect menu items to your new report design.**</span></span> <span data-ttu-id="d19b5-123">イベント ハンドラーを使用して、アプリケーション レポート ソリューションのすべての側面をカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-123">You can customize all aspects of an application reporting solution by using event handlers.</span></span> <span data-ttu-id="d19b5-124">コントローラー クラスの **PostHandler** イベントを追加して、ユーザー ナビゲーションをカスタム レポート デザインに再ルーティングします。</span><span class="sxs-lookup"><span data-stu-id="d19b5-124">Add a **PostHandler** event for the controller class to reroute user navigations to a custom report design.</span></span>

## <a name="expand-a-report-data-set"></a><span data-ttu-id="d19b5-125">レポート データ セットを展開</span><span class="sxs-lookup"><span data-stu-id="d19b5-125">Expand a report data set</span></span>
<span data-ttu-id="d19b5-126">次のチュートリアルでは、「純粋な」拡張機能ベースのソリューションを使用して既存のアプリケーション データ セットを拡張するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-126">The following walkthrough shows the process of expanding an existing application data set by using a "pure" extension-based solution.</span></span> <span data-ttu-id="d19b5-127">このソリューションには、Fleet Management アプリケーション用のカスタム **レンタル リスト** レポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-127">The solution includes a custom **Rentals list** report for the Fleet Management application.</span></span> <span data-ttu-id="d19b5-128">新しいレポートには、レンタルの詳細に追加のレンタル料金データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-128">The new report includes additional rental charge data in the rental details.</span></span> <span data-ttu-id="d19b5-129">アプリケーションのカスタマイズ内容は、拡張モデルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-129">The application customizations are defined in an extension model.</span></span> <span data-ttu-id="d19b5-130">次の図は、標準デザインとカスタム ソリューションを示しています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-130">The following illustrations show the standard design and the custom solution.</span></span>

### <a name="before-standard-design"></a><span data-ttu-id="d19b5-131">(標準デザイン) の前に</span><span class="sxs-lookup"><span data-stu-id="d19b5-131">Before (standard design)</span></span>

<span data-ttu-id="d19b5-132">[![標準デザイン (カスタマイズ前)](./media/fleet-extension-rentals-list-before-1024x673.png)](./media/fleet-extension-rentals-list-before.png)</span><span class="sxs-lookup"><span data-stu-id="d19b5-132">[![Standard design (before customization)](./media/fleet-extension-rentals-list-before-1024x673.png)](./media/fleet-extension-rentals-list-before.png)</span></span>

### <a name="after-custom-solution"></a><span data-ttu-id="d19b5-133">変更後 (カスタム ソリューション)</span><span class="sxs-lookup"><span data-stu-id="d19b5-133">After (custom solution)</span></span>

<span data-ttu-id="d19b5-134">[![カスタム ソリューション (カスタマイズ後)](./media/fleet-extension-rentals-list-after-1024x672.png)](./media/fleet-extension-rentals-list-after.png)</span><span class="sxs-lookup"><span data-stu-id="d19b5-134">[![Custom solution (after customization)](./media/fleet-extension-rentals-list-after-1024x672.png)](./media/fleet-extension-rentals-list-after.png)</span></span>

1. <span data-ttu-id="d19b5-135">**アプリケーション カスタマイズの新しいモデルを作成します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-135">**Create a new model for your application customizations.**</span></span> <span data-ttu-id="d19b5-136">拡張モデルに関する詳細については、 [拡張機能およびオーバーレイによるカスタマイズ](../extensibility/customization-overlayering-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d19b5-136">For more information about extension models, see [Customize through extension and overlayering](../extensibility/customization-overlayering-extensions.md).</span></span> <span data-ttu-id="d19b5-137">この例では、**フリート管理拡張**モデルにカスタム レポートを追加します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-137">For this example, add a custom report to the **Fleet Management Extensions** model.</span></span>
2. <span data-ttu-id="d19b5-138">**Microsoft Visual Studio で、新しいプロジェクトを作成します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-138">**Create a new project in Microsoft Visual Studio.**</span></span> <span data-ttu-id="d19b5-139">プロジェクトが拡張モデルに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-139">Make sure that the project is associated with your extension model.</span></span> <span data-ttu-id="d19b5-140">次の図はプロジェクト設定を示します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-140">The following illustration shows the project settings.</span></span>

    <span data-ttu-id="d19b5-141">[![Visual Studio でのプロジェクト設定](./media/fleet-extension-vs-project-settings.png)](./media/fleet-extension-vs-project-settings.png)</span><span class="sxs-lookup"><span data-stu-id="d19b5-141">[![Project settings in Visual Studio](./media/fleet-extension-vs-project-settings.png)](./media/fleet-extension-vs-project-settings.png)</span></span>

3. <span data-ttu-id="d19b5-142">**カスタム レポート データを格納するテーブル拡張機能を追加します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-142">**Add a table extension to store the custom report data.**</span></span> <span data-ttu-id="d19b5-143">RDP クラスによって設定される **TmpFMRentalsByCust** データ セットの一時的キャッシュを検索し、モデルで拡張を作成します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-143">Find the temporary cache for the **TmpFMRentalsByCust** data set that is populated by the RDP class, and create an extension in your model.</span></span> <span data-ttu-id="d19b5-144">レポート サーバーのデータの格納に使用するフィールドを定義し、**保存**をクリックして変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-144">Define the fields that will be used to store the data for the report server, and then click **Save** to save your changes.</span></span> <span data-ttu-id="d19b5-145">次の図は、この例で必要なテーブル拡張機能を示しています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-145">The following illustration shows the table extension that is required for this example.</span></span>

    <span data-ttu-id="d19b5-146">[![この例の拡張テーブル](./media/fleet-extension-table-extension.png)](./media/fleet-extension-table-extension.png)</span><span class="sxs-lookup"><span data-stu-id="d19b5-146">[![Table extension for this example](./media/fleet-extension-table-extension.png)](./media/fleet-extension-table-extension.png)</span></span>

4. <span data-ttu-id="d19b5-147">**プロジェクトに、カスタム レポートを追加します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-147">**Add your custom report to the project.**</span></span> <span data-ttu-id="d19b5-148">カスタム デザインは、標準的なソリューションによく似ています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-148">The custom design closely resembles the standard solution.</span></span> <span data-ttu-id="d19b5-149">したがって、**フリート管理拡張**モデルで既存のアプリケーション レポートを複製してから、レンタル料金コンテナーにカスタム タイトルと追加テキスト ボックスが含まれるようにレポート デザインを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-149">Therefore, you can just duplicate the existing application report in the **Fleet Management Extension** model, and then update the report design so that it includes the custom title and additional text box in the Rental Charges container.</span></span>
5. <span data-ttu-id="d19b5-150">**レポートの名前を変更して、わかりやすい名前にします。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-150">**Rename the report so that it has a meaningful name.**</span></span> <span data-ttu-id="d19b5-151">この例では、カスタム レポートの **FERentalsByCustomer** の名前を変更し、標準のソリューションと区別します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-151">For this example, rename the custom report **FERentalsByCustomer** to distinguish it from the standard solution.</span></span>
6. <span data-ttu-id="d19b5-152">**レポート データ セットの参照を復元します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-152">**Restore the report data set references.**</span></span> <span data-ttu-id="d19b5-153">レポート デザイナーを開いて、**データセット**コレクションを展開し、**FMRentalsByCustDS** と名付けられたデータ セットを右クリックし、それから**復元**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d19b5-153">Open the report designer, expand the **Datasets** collection, right-click the data set that is named **FMRentalsByCustDS**, and then click **Restore**.</span></span> <span data-ttu-id="d19b5-154">データ セットは、新しく導入された列を含むように拡張されます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-154">The data set is expanded so that it includes the newly introduced columns.</span></span> <span data-ttu-id="d19b5-155">したがって、これらの列は、レポート デザイナーで使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d19b5-155">Therefore, these columns are now available in the report designer.</span></span>
7. <span data-ttu-id="d19b5-156">**レポート デザインのカスタマイズ**</span><span class="sxs-lookup"><span data-stu-id="d19b5-156">**Customize the report design.**</span></span> <span data-ttu-id="d19b5-157">デザイナーは、カスタム ソリューションを作成するために使用できる自由形式のデザイン サーフェスを提供します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-157">The designer offers a free-form design surface that you can use to create the custom solution.</span></span> <span data-ttu-id="d19b5-158">次の図は、この例で使用されるカスタム デザインを示しています。</span><span class="sxs-lookup"><span data-stu-id="d19b5-158">The following illustration shows the custom design that is used for this example.</span></span>

    <span data-ttu-id="d19b5-159">[![この例のカスタム デザイン](./media/fleet-extension-custom-design.png)](./media/fleet-extension-custom-design.png)</span><span class="sxs-lookup"><span data-stu-id="d19b5-159">[![Custom design for this example](./media/fleet-extension-custom-design.png)](./media/fleet-extension-custom-design.png)</span></span>

8. <span data-ttu-id="d19b5-160">**新しいレポート ハンドラー (X++) クラスをプロジェクトに追加します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-160">**Add a new report handler (X++) class to the project.**</span></span> <span data-ttu-id="d19b5-161">クラスに、それが既存のアプリケーション レポートのハンドラーであることを適切に表す名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-161">Give the class a name that appropriately describes that it's a handler for an existing application report.</span></span> <span data-ttu-id="d19b5-162">この例では、クラスの **FERentalsByCustomerHandler** の名前を変更し、他のレポート ハンドラーと区別します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-162">For this example, rename the class **FERentalsByCustomerHandler** to distinguish it from other report handlers.</span></span>
9. <span data-ttu-id="d19b5-163">**PostHandler メソッドを追加して、カスタム レポートの使用を開始します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-163">**Add a PostHandler method to begin to use your custom report.**</span></span> <span data-ttu-id="d19b5-164">この例では、次のコードを使用して標準ソリューション **FMRentalsByCustController** のコントローラー クラスを展開します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-164">In this example, extend the controller class in the standard solution, **FMRentalsByCustController**, by using the following code.</span></span>

    ```xpp
    class FERentalsByCustomerHandler
    {
        [PostHandlerFor(classStr(FMRentalsByCustController), staticMethodStr(FMRentalsByCustController, construct))]
        public static void ReportNamePostHandler(XppPrePostArgs arguments)
        {
            FMRentalsByCustController controller = arguments.getReturnValue();
            controller.parmReportName(ssrsreportstr(FERentalsByCustomer, Report));
        }
    }
    ```

    <span data-ttu-id="d19b5-165">アプリケーションのユーザー ナビゲーションは、カスタム レポート ソリューションに再ルーティングされるようになります。</span><span class="sxs-lookup"><span data-stu-id="d19b5-165">User navigations in the application will now be rerouted to the custom reporting solution.</span></span> <span data-ttu-id="d19b5-166">レポート サーバーにカスタム レポートを配置し、アプリケーションがそれを使用していることを確認するには少し時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="d19b5-166">Take some time to deploy the custom report to the report server and verify that the application is using it.</span></span> <span data-ttu-id="d19b5-167">この時点では、ステップ 3 で導入したカスタム フィールドを作成するために使用されるビジネス ロジックを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d19b5-167">At this point, you just have to add the business logic that is used to populate the custom fields that you introduced in step 3.</span></span> <span data-ttu-id="d19b5-168">次の手順では、ソリューションに該当するデータ セット拡張のメソッドを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d19b5-168">In the next step, you must select the method of data set expansion that is appropriate for your solution.</span></span>

10. <span data-ttu-id="d19b5-169">**X++ ビジネス ロジックを追加して、カスタム フィールド データを設定します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-169">**Add X++ business logic to populate the custom field data.**</span></span> <span data-ttu-id="d19b5-170">ソリューションを必要とする変換のタイプに適したデータの処理方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-170">Select the data processing technique that makes sense for the type of transformation that you require for the solution.</span></span>

    - <span data-ttu-id="d19b5-171">**オプション 1: データ処理ポストハンドラーを追加します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-171">**Option 1: Add a data processing post-handler.**</span></span> <span data-ttu-id="d19b5-172">標準ソリューションの結果セットに対して 1 つのパスを使用する一括挿入操作にはこの手法を適用します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-172">Apply this technique for bulk insert operations that use a single pass over the result set of the standard solution.</span></span> <span data-ttu-id="d19b5-173">テーブル ルックアップを使用してデータ セットを展開するコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-173">Here is the code that expands the data set by using a table lookup.</span></span>

        ```xpp
        class FERentalsByCustomerHandler
        {
            [PostHandlerFor(classStr(FMRentalsByCustDP), methodstr(FMRentalsByCustDP, processReport))]
            public static void TmpTablePostHandler(XppPrePostArgs arguments)
            {
                FMRentalsByCustDP dpInstance = arguments.getThis() as FMRentalsByCustDP;
                TmpFMRentalsByCust tmpTable = dpInstance.getTmpFMRentalsByCust();
                FMRentalCharge chargeTable;
                ttsbegin;
                while select forUpdate tmpTable
                {
                    select * from chargeTable where chargeTable.RentalId == tmpTable.RentalId;
                    tmpTable.ChargeDesc = chargeTable.Description;
                    tmpTable.update();
                }
                ttscommit;
            }
        }
        ```

    - <span data-ttu-id="d19b5-174">**オプション 2: イベントを挿入する一時テーブルを追加します。**</span><span class="sxs-lookup"><span data-stu-id="d19b5-174">**Option 2: Add a temp table Inserting event.**</span></span> <span data-ttu-id="d19b5-175">この手法を行ごとの計算に適用します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-175">Apply this technique for row-by-row calculations.</span></span> <span data-ttu-id="d19b5-176">テーブル ルックアップを使用してデータ セットを展開するコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="d19b5-176">Here is the code that expands the data set by using a table lookup.</span></span>

        ```xpp
        class FERentalsByCustomerHandler
        {
            [DataEventHandlerAttribute(tableStr(TmpFMRentalsByCust), DataEventType::Inserting)]
            public static void TmpFMRentalsByCustInsertEvent(Common c, DataEventArgs e)
            {
                TmpFMRentalsByCust tempTable = c;
                FMRentalCharge chargeTable;
                // update the value of the 'ChargeDesc' column during 'insert' operation
                select * from chargeTable where chargeTable.RentalId == tempTable.RentalId
                && chargeTable.ChargeType == tempTable.ChargeType;
                tempTable.ChargeDesc = chargeTable.Description;
            }
        }
        ```

<span data-ttu-id="d19b5-177">これで、レポート データ セットの拡張が完了しました。</span><span class="sxs-lookup"><span data-stu-id="d19b5-177">You've now finished expanding the report data set.</span></span> <span data-ttu-id="d19b5-178">アプリケーションをコンパイルした後、拡張モデルで定義されているレポート クラス ハンドラーで定義したカスタム X++ ビジネス ロジックを使用して、新しいレポート デザインにユーザー ナビゲーションを再ルーティングし始めます。</span><span class="sxs-lookup"><span data-stu-id="d19b5-178">After the application is compiled, it will begin to reroute user navigations to the new report design by using the custom X++ business logic that you defined in the report class handler that is defined in the extension model.</span></span>
