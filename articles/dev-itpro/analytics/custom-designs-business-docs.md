---
title: "ビジネス ドキュメントのカスタム デザインを作成する"
description: "このトピックでは、純粋な拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを作成する方法について説明します。"
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 266574
ms.assetid: fba7faa3-716b-4adf-ab3e-8573f3614894
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 9f350a3d6233c534d7103e5c4cd7acd60dd51b6c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="create-custom-designs-for-business-documents"></a><span data-ttu-id="e0287-103">ビジネス ドキュメントのカスタム デザインを作成する</span><span class="sxs-lookup"><span data-stu-id="e0287-103">Create custom designs for business documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0287-104">このトピックでは、純粋な拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e0287-104">This topic shows how to create a custom report design for an existing application business document by using a pure extension model.</span></span> 

<span data-ttu-id="e0287-105">Microsoft Dynamics 365 for Finance and Operations には、カスタム ソリューションをサポートするためのツールの拡張セットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0287-105">Microsoft Dynamics 365 for Finance and Operations includes an expanded set of tools to support custom solutions.</span></span> <span data-ttu-id="e0287-106">このトピックでは、純粋な拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを作成する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="e0287-106">This topic focuses on the steps for creating a custom report design for an existing application business document by using a pure extension model.</span></span> <span data-ttu-id="e0287-107">カスタム レポート デザインをアプリケーション ドキュメントのインスタンスに関連付けるには、このトピックで後述する手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e0287-107">Follow the steps later in this topic to associate a custom report design with an instance of an application document.</span></span> <span data-ttu-id="e0287-108">完了したら、ユーザーは印刷管理設定を構成して、 該当するときはいつでも、カスタムのデザインを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0287-108">When you've finished, users can configure Print management settings to select the custom design whenever it's appropriate, based on transaction details.</span></span> <span data-ttu-id="e0287-109">次の図は、一般的なアプリケーションのカスタマイズを示しています。[![extendingprintmgt](./media/extendingprintmgt1.png)](./media/extendingprintmgt1.png)</span><span class="sxs-lookup"><span data-stu-id="e0287-109">The following illustration shows a typical application customization.[![extendingprintmgt](./media/extendingprintmgt1.png)](./media/extendingprintmgt1.png)</span></span>  

## <a name="whats-important-to-know"></a><span data-ttu-id="e0287-110">知っている必要がある重要なこと</span><span class="sxs-lookup"><span data-stu-id="e0287-110">What's important to know?</span></span>
<span data-ttu-id="e0287-111">このソリューションを適用する前に注意すべき重要な点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e0287-111">Here are some important points that you should be aware of before you apply this solution:</span></span>

-   <span data-ttu-id="e0287-112">印刷管理設定は、有効な法人に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e0287-112">Print management settings are scoped to the active legal entity.</span></span> <span data-ttu-id="e0287-113">カスタム デザインは、1 つ以上の印刷管理設定を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e0287-113">Custom designs can be associated with one or more Print management settings.</span></span>
-   <span data-ttu-id="e0287-114">標準レポート デザインは、カスタム ソリューションと共に引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="e0287-114">Standard report designs continue to be available alongside custom solutions.</span></span> <span data-ttu-id="e0287-115">印刷管理設定を使用して、トランザクションの詳細に基づいて適切なデザインを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0287-115">Use Print management settings to select the appropriate design, based on transaction details.</span></span>
-   <span data-ttu-id="e0287-116">カスタム ビジネス プロセスのビジネス ドキュメントを導入する場合は、多くの作業が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0287-116">If you introduce a business document for a custom business process, more work is required.</span></span> <span data-ttu-id="e0287-117">カスタム ビジネス ドキュメント ソリューションの作成方法の詳細については、[印刷管理の統合ガイド](https://www.microsoft.com/en-us/download/details.aspx?id=36049) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0287-117">For more information about how to create a custom business document solution, see the [Print Management Integration Guide](https://www.microsoft.com/en-us/download/details.aspx?id=36049).</span></span>

## <a name="customize-a-business-document"></a><span data-ttu-id="e0287-118">ビジネス ドキュメントのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e0287-118">Customize a business document</span></span>
<span data-ttu-id="e0287-119">次のチュートリアルでは、既存のアプリケーション ビジネス ドキュメントのカスタム レポート デザインを導入し、次に印刷管理を使用して新しいデザインを選択するプロセスを示します。</span><span class="sxs-lookup"><span data-stu-id="e0287-119">The following walkthrough shows the process of introducing a custom report design for an existing application business document and then using Print management to select the new design.</span></span> <span data-ttu-id="e0287-120">このソリューションには、Application Suite モデルの一部として標準アプリケーションで提供される**販売の確認**レポートのカスタム設計定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e0287-120">The solution includes a custom design definition for the **Sales confirmation** report that is provided in the standard application as part of the Application Suite model.</span></span> <span data-ttu-id="e0287-121">アプリケーションのカスタマイズ内容は、拡張モデルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="e0287-121">The application customizations will be defined in an extension model.</span></span>

1.  <span data-ttu-id="e0287-122">**アプリケーション カスタマイズの新しいモデルを作成します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-122">**Create a new model for your application customizations.**</span></span> <span data-ttu-id="e0287-123">拡張モデルに関する詳細については、[カスタマイズ: オーバーレイおよび拡張機能](../extensibility/customization-overlayering-extensions.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e0287-123">For more information about extension models, see [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span> <span data-ttu-id="e0287-124">この例では、**アプリケーション スイート拡張子**というモデルを追加し、それはアプリケーション スイート、アプリケーション プラットフォーム、およびアプリケーション基盤パッケージを参照します。</span><span class="sxs-lookup"><span data-stu-id="e0287-124">For this example, you add a model that is named **Application Suite Extensions**, and that references the Application Suite, Application Platform, and Application Foundation packages.</span></span>
2.  <span data-ttu-id="e0287-125">**Microsoft Visual Studio で新しいプロジェクトを作成します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-125">**Create a new project in Microsoft Visual Studio.**</span></span> <span data-ttu-id="e0287-126">プロジェクトが拡張モデルに関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0287-126">Make sure that the project is associated with your extension model.</span></span> <span data-ttu-id="e0287-127">次の図はプロジェクト設定を示します。</span><span class="sxs-lookup"><span data-stu-id="e0287-127">The following illustration shows the project settings.</span></span> <span data-ttu-id="e0287-128">[![Visual Studio のプロジェクト設定](./media/app-extension-vs-project-settings.png)](./media/app-extension-vs-project-settings.png)</span><span class="sxs-lookup"><span data-stu-id="e0287-128">[![Project settings in Visual Studio](./media/app-extension-vs-project-settings.png)](./media/app-extension-vs-project-settings.png)</span></span>
3.  <span data-ttu-id="e0287-129">**ビジネス ドキュメントのカスタム レポートのデザインを作成します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-129">**Create a custom report design for the business document.**</span></span> <span data-ttu-id="e0287-130">カスタム ソリューションが正しいレポート データ コントラクトを消費することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0287-130">You must make sure that your custom solution consumes the correct report data contract.</span></span> <span data-ttu-id="e0287-131">アプリケーション エクスプ ローラーで、既存のアプリケーション スイート レポートを検索します。</span><span class="sxs-lookup"><span data-stu-id="e0287-131">Find the existing Application Suite report in Application Explorer.</span></span> <span data-ttu-id="e0287-132">このレポートの名前は **SalesConfirm** です。</span><span class="sxs-lookup"><span data-stu-id="e0287-132">This report is named **SalesConfirm**.</span></span> <span data-ttu-id="e0287-133">右クリックし、**プロジェクトで複製** をクリックしてカスタム ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="e0287-133">Right-click it, and then click **Duplicate in project** to create the custom solution.</span></span>
4.  <span data-ttu-id="e0287-134">**レポートの名前を変更して、わかりやすい名前にします。**</span><span class="sxs-lookup"><span data-stu-id="e0287-134">**Rename the report so that it has a meaningful name.**</span></span> <span data-ttu-id="e0287-135">この例では、カスタム レポートの **SalesConfirmExt** を名前付けし、標準のソリューションと区別します。</span><span class="sxs-lookup"><span data-stu-id="e0287-135">For this example, name the custom report **SalesConfirmExt** to distinguish it from the standard solution.</span></span> <span data-ttu-id="e0287-136">プロジェクトをコンパイルしてレポートを展開し、変更にエラーがないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0287-136">Compile the project, and deploy the report to verify that the changes have no errors.</span></span>
5.  <span data-ttu-id="e0287-137">**自由形式デザイナーを使用して、レポートのデザインをカスタマイズします。**</span><span class="sxs-lookup"><span data-stu-id="e0287-137">**Use the free-form designer to customize the report design.**</span></span> <span data-ttu-id="e0287-138">**レポート** という名前のレポート デザインを選択し、右クリックして、精度デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0287-138">Select the report design that is named **Report**, right-click it, and open the precision designer.</span></span> <span data-ttu-id="e0287-139">組織の業務要件を満たすように設計をカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="e0287-139">Customize the design to satisfy the organization’s business requirements.</span></span> <span data-ttu-id="e0287-140">次の図は、**Sales confirmation** レポートのカスタム設計定義を示しています。</span><span class="sxs-lookup"><span data-stu-id="e0287-140">The following illustration shows a custom design definition for the **Sales confirmation** report.</span></span> <span data-ttu-id="e0287-141">[![販売確認レポートのカスタム デザイン定義](./media/app-extension-report-designer-1024x613.png)](./media/app-extension-report-designer.png)</span><span class="sxs-lookup"><span data-stu-id="e0287-141">[![Custom design definition for the Sales confirmation report](./media/app-extension-report-designer-1024x613.png)](./media/app-extension-report-designer.png)</span></span>
6.  <span data-ttu-id="e0287-142">**標準のレポート コントローラーを拡張する新しい X++ クラスを追加します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-142">**Add a new X++ class that extends the standard report controller.**</span></span> <span data-ttu-id="e0287-143">クラスに、それが既存のアプリケーション レポートのハンドラーであることを適切に表す名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e0287-143">Give the class a name that appropriately describes that it's a handler for an existing application report.</span></span> <span data-ttu-id="e0287-144">この例では、クラスの **SalesConfirmControllerExt** の名前を変更し、他のレポート コントローラーと区別します。</span><span class="sxs-lookup"><span data-stu-id="e0287-144">For this example, rename the class **SalesConfirmControllerExt** to distinguish it from other report controllers.</span></span>
7.  <span data-ttu-id="e0287-145">**拡張クラスを使用して、カスタム デザインを読み込みます。**</span><span class="sxs-lookup"><span data-stu-id="e0287-145">**Use the extended class to load the custom design.**</span></span> <span data-ttu-id="e0287-146">カスタム レポート デザインを参照する**メイン**メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="e0287-146">Add a **main** method that refers to the custom report design.</span></span> <span data-ttu-id="e0287-147">(標準的なソリューションから**主要な**メソッドをコピーし、新しい**コントローラー**クラスへの参照を追加することができます。) 次に、標準的なソリューションを拡張するコードを示します。</span><span class="sxs-lookup"><span data-stu-id="e0287-147">(You can just copy the **main** method from the standard solution and add references to the new **Controller** class.) Here is the code that extends the standard solution.</span></span>

        class SalesConfirmControllerExt extends SalesConfirmController
        {
            public static SalesConfirmControllerExt construct()
            {
                return new SalesConfirmControllerExt();
            }
            public static void main(Args _args)
            {
                SrsReportRunController formLetterController = SalesConfirmControllerExt::construct();
                SalesConfirmControllerExt controller = formLetterController;controller.initArgs(_args, ssrsReportStr(SalesConfirmExt, Report));
                if (classIdGet(_args.caller()) == classNum(SalesConfirmJournalPrint))
                {
                    formLetterController.renderingCompleted += eventhandler(SalesConfirmJournalPrint::renderingCompleted);
                }
                formLetterController.startOperation();
            }
        }

8.  <span data-ttu-id="e0287-148">**新しいレポート ハンドラー (X++) クラスをプロジェクトに追加します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-148">**Add a new report handler (X++) class to the project.**</span></span> <span data-ttu-id="e0287-149">クラスに、それが印刷管理に基づくドキュメントのハンドラーであることを適切に表す名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="e0287-149">Give the class a name that appropriately describes that it's a handler for Print management–based documents.</span></span> <span data-ttu-id="e0287-150">この例では、クラスの **PrintMgtDocTypeHandlerExt** の名前を変更し、他のオブジェクト ハンドラーと区別します。</span><span class="sxs-lookup"><span data-stu-id="e0287-150">For this example, rename the class **PrintMgtDocTypeHandlerExt** to distinguish it from other object handlers.</span></span>
9.  <span data-ttu-id="e0287-151">**デリゲート ハンドラー メソッドを追加して、カスタム レポートの使用を開始します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-151">**Add a delegate handler method to start to use your custom report.**</span></span> <span data-ttu-id="e0287-152">この例では、次のコードを使用して **PrintMgtDocTypeHandlerExt** クラスの **getDefaultReportFormatDelegate** メソッドを展開します。</span><span class="sxs-lookup"><span data-stu-id="e0287-152">In this example, extend the **getDefaultReportFormatDelegate** method in the **PrintMgtDocTypeHandlerExt** class by using the following code.</span></span>

        class PrintMgtDocTypeHandlersExt
        {
            [SubscribesTo(classstr(PrintMgmtDocType), delegatestr(PrintMgmtDocType, getDefaultReportFormatDelegate))]
            public static void getDefaultReportFormatDelegate(PrintMgmtDocumentType _docType, EventHandlerResult _result)
            {
                switch (_docType)
                {
                    case PrintMgmtDocumentType::SalesOrderConfirmation:
                        _result.result(ssrsReportStr(SalesConfirmExt, Report));
                        break;
                }
            }
        }

10. <span data-ttu-id="e0287-153">**アプリケーションのレポートのメニュー項目を拡張します。**</span><span class="sxs-lookup"><span data-stu-id="e0287-153">**Extend the menu item for the application report.**</span></span> <span data-ttu-id="e0287-154">アプリケーション エクスプ ローラーで、既存のアプリケーション スイート メニュー項目を検索します。</span><span class="sxs-lookup"><span data-stu-id="e0287-154">Find the existing Application Suite menu item in Application Explorer.</span></span> <span data-ttu-id="e0287-155">このメニュー項目の名前は **SalesConfirmation** です。</span><span class="sxs-lookup"><span data-stu-id="e0287-155">This menu item is named **SalesConfirmation**.</span></span> <span data-ttu-id="e0287-156">右クリックし、**拡張子の作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0287-156">Right-click it, and then click **Create extension**.</span></span> <span data-ttu-id="e0287-157">デザイナーで新しい拡張オブジェクトを開いて、**オブジェクト**プロパティの値を **SalesConfirmControllerExt** に設定し、ユーザー ナビゲーションを拡張されたソリューションにリダイレクトします。</span><span class="sxs-lookup"><span data-stu-id="e0287-157">Open the new extension object in the designer, and set the value of the **Object** property to **SalesConfirmControllerExt** to redirect user navigations to the extended solution.</span></span>
11. <span data-ttu-id="e0287-158">**カスタム ビジネス ドキュメントを使用するため、印刷管理設定を更新してください。**</span><span class="sxs-lookup"><span data-stu-id="e0287-158">**Update the Print management settings to use the custom business document.**</span></span> <span data-ttu-id="e0287-159">この例では、**売掛金勘定** &gt; **セッテイ** &gt; **フォーム** &gt; **フォーム設定**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0287-159">For this example, go to **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span> <span data-ttu-id="e0287-160">**印刷管理**をクリックし、ドキュメントの構成設定を検索し、カスタム デザインを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0287-160">Click **Print Management**, find the document configuration settings, and then select the custom design.</span></span> <span data-ttu-id="e0287-161">次の図は、変更がコンパイルされた後の印刷管理設定を示しています。</span><span class="sxs-lookup"><span data-stu-id="e0287-161">The following illustration shows the Print management settings after the changes have been compiled.</span></span> <span data-ttu-id="e0287-162">[![コンパイル後の印刷管理設定](./media/app-extension-print-mgt-after-1024x608.png)](./media/app-extension-print-mgt-after.png)</span><span class="sxs-lookup"><span data-stu-id="e0287-162">[![Print Management settings after compilation](./media/app-extension-print-mgt-after-1024x608.png)](./media/app-extension-print-mgt-after.png)</span></span>

<span data-ttu-id="e0287-163">これで、ビジネス ドキュメントのカスタマイズが完了しました。</span><span class="sxs-lookup"><span data-stu-id="e0287-163">You’ve now finished customizing the business document.</span></span> <span data-ttu-id="e0287-164">アプリケーションでトランザクションを処理するとき、ビジネス ドキュメントのカスタム レポート デザインがユーザーに提示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="e0287-164">Users will now be presented with the custom report design for the business document when they process transactions in the application.</span></span>




