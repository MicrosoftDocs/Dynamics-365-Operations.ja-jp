---
title: Azure Logic アプリを使用した定期的なデータ エクスポート
description: このチュートリアルでは Dynamics 365 for Talent から定期的なスケジュールでデータをエクスポートする Azure ロジック アプリを作成する方法を説明します。
author: gregboyko
manager: AnnBe
ms.date: 02/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: gboyko
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Talent January 2019 update
ms.openlocfilehash: 72481e47058b9e8b108369d48c14cb4cce6bb4d1
ms.sourcegitcommit: 0bd0215d0735ed47b1b8af93a80bcdbf7ca2cc49
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2019
ms.locfileid: "789834"
---
# <a name="recurring-data-export-using-azure-logic-apps"></a><span data-ttu-id="ea860-103">Azure Logic アプリを使用した定期的なデータ エクスポート</span><span class="sxs-lookup"><span data-stu-id="ea860-103">Recurring data export using Azure Logic apps</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ea860-104">このチュートリアルでは Microsoft Dynamics 365 for Talent Core HR から定期的なスケジュールでデータをエクスポートする Microsoft Azure ロジック アプリを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ea860-104">This tutorial shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 for Talent Core HR on a recurring schedule.</span></span> <span data-ttu-id="ea860-105">このチュートリアルでは Core HR の DMF パッケージ REST アプリケーション プログラミング インターフェイス (API) を利用して、データをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="ea860-105">The tutorial takes advantage of Core HR's DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="ea860-106">データがエクスポートされた後、ロジック アプリはエクスポートされたデータ パッケージを Microsoft OneDrive for Business のフォルダーに保存します。</span><span class="sxs-lookup"><span data-stu-id="ea860-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="ea860-107">ビジネス シナリオ</span><span class="sxs-lookup"><span data-stu-id="ea860-107">Business scenario</span></span>

<span data-ttu-id="ea860-108">Microsoft Dynamics 365 統合のひとつの典型的なビジネス シナリオでは、データは定期的なスケジュールで下流システムにエクスポートされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea860-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="ea860-109">このチュートリアルでは Microsoft Dynamics 365 for Talent からすべての作業者レコードをエクスポートし、OneDrive for Business のフォルダーに作業者のリストを保存する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ea860-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 for Talent and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="ea860-110">このチュートリアルでエクスポートされる特定のデータと、エクスポートされたデータの宛先は単なる例です。</span><span class="sxs-lookup"><span data-stu-id="ea860-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="ea860-111">ビジネスのニーズに合わせてそれらを簡単に変更できます。</span><span class="sxs-lookup"><span data-stu-id="ea860-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="ea860-112">使用されるテクノロジ</span><span class="sxs-lookup"><span data-stu-id="ea860-112">Technologies used</span></span>

<span data-ttu-id="ea860-113">このチュートリアルでは下記のテクノロジを使用します:</span><span class="sxs-lookup"><span data-stu-id="ea860-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="ea860-114">**[Dynamics 365 for Talent Core HR](https://dynamics.microsoft.com/en-us/talent/overview/)** – エクスポートされる作業者のマスター データ ソース。</span><span class="sxs-lookup"><span data-stu-id="ea860-114">**[Dynamics 365 for Talent Core HR](https://dynamics.microsoft.com/en-us/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="ea860-115">**[Azure ロジック アプリ](https://azure.microsoft.com/services/logic-apps/)** – 定期的なエクスポートのオーケストレーションとスケジュールを提供するテクノロジ。</span><span class="sxs-lookup"><span data-stu-id="ea860-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="ea860-116">**[コネクタ](https://docs.microsoft.com/en-us/azure/connectors/apis-list)** – ロジック アプリを必要なエンドポイントに接続するために使用されるテクノロジ。</span><span class="sxs-lookup"><span data-stu-id="ea860-116">**[Connectors](https://docs.microsoft.com/en-us/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="ea860-117">[Azure AD の HTTP](https://docs.microsoft.com/connectors/webcontents/) コネクタ</span><span class="sxs-lookup"><span data-stu-id="ea860-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="ea860-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) コネクタ</span><span class="sxs-lookup"><span data-stu-id="ea860-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="ea860-119">**[DMF パッケージ REST API](../dev-itpro/data-entities/data-management-api.md)** – エクスポートをトリガーし、その進捗を監視するために使用されるテクノロジ。</span><span class="sxs-lookup"><span data-stu-id="ea860-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="ea860-120">**[OneDrive for Business](https://onedrive.live.com/about/en-us/business/)** – エクスポートされた作業者の宛先。</span><span class="sxs-lookup"><span data-stu-id="ea860-120">**[OneDrive for Business](https://onedrive.live.com/about/en-us/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ea860-121">必要条件</span><span class="sxs-lookup"><span data-stu-id="ea860-121">Prerequisites</span></span>

<span data-ttu-id="ea860-122">このチュートリアルで手順を開始する前に、次の項目が必要です:</span><span class="sxs-lookup"><span data-stu-id="ea860-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="ea860-123">その環境で管理者レベルの権限を持つ Core HR 環境</span><span class="sxs-lookup"><span data-stu-id="ea860-123">A Core HR environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="ea860-124">ロジック アプリをホストする [Azure サブスクリプション](https://azure.microsoft.com/free/)</span><span class="sxs-lookup"><span data-stu-id="ea860-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="ea860-125">演習</span><span class="sxs-lookup"><span data-stu-id="ea860-125">The exercise</span></span>

<span data-ttu-id="ea860-126">この演習の最後には、Core HR 環境と OneDrive for Business アカウントに接続されているロジック アプリを取得できます。</span><span class="sxs-lookup"><span data-stu-id="ea860-126">At the end of this exercise, you will have a logic app that is connected to your Core HR environment and your OneDrive for Business account.</span></span> <span data-ttu-id="ea860-127">ロジック アプリは Core HR からデータ パッケージをエクスポートし、そのエクスポートが完了するのを待ち、エクスポートされたデータ パッケージをダウンロードして、指定した OneDrive for Business フォルダーにデータ パッケージを保存します。</span><span class="sxs-lookup"><span data-stu-id="ea860-127">The logic app will export a data package from Core HR, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="ea860-128">完成したロジック アプリは、次の図のようになります。</span><span class="sxs-lookup"><span data-stu-id="ea860-128">The completed logic app will resemble the following illustration.</span></span>

![ロジック アプリの概要](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-core-hr"></a><span data-ttu-id="ea860-130">ステップ 1: Core HR でデータ エクスポート プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="ea860-130">Step 1: Create a data export project in Core HR</span></span>

<span data-ttu-id="ea860-131">Core HR で、作業者をエクスポートするデータ エクスポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ea860-131">In Core HR, create a data export project that exports workers.</span></span> <span data-ttu-id="ea860-132">プロジェクトに **作業者のエクスポート** という名前を付け、**データ パッケージの生成** オプションが **はい** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea860-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="ea860-133">プロジェクトに単一のエンティティ (**作業者**) を追加して、エクスポートする形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="ea860-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="ea860-134">(このチュートリアルは Microsoft Excel 形式を使用します。)</span><span class="sxs-lookup"><span data-stu-id="ea860-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![作業者データ プロジェクトをエクスポート](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="ea860-136">データ エクスポート プロジェクトの名前を記憶します。</span><span class="sxs-lookup"><span data-stu-id="ea860-136">Remember the name of the data export project.</span></span> <span data-ttu-id="ea860-137">次のステップでロジック アプリを作成するときに必要です。</span><span class="sxs-lookup"><span data-stu-id="ea860-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="ea860-138">ステップ 2: ロジック アプリの作成</span><span class="sxs-lookup"><span data-stu-id="ea860-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="ea860-139">演習の大部分はロジック アプリの作成に関するものです。</span><span class="sxs-lookup"><span data-stu-id="ea860-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="ea860-140">Azure ポータルで、ロジック アプリを作成します。</span><span class="sxs-lookup"><span data-stu-id="ea860-140">In the Azure portal, create a logic app.</span></span>

    ![ロジック アプリ作成ページ](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="ea860-142">ロジック アプリ デザイナーで、空白のロジック アプリから始めます。</span><span class="sxs-lookup"><span data-stu-id="ea860-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="ea860-143">24 時間ごとに (または選択したスケジュールに従って) ロジック アプリを実行するために [定期スケジュール トリガー](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) を追加します。</span><span class="sxs-lookup"><span data-stu-id="ea860-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![定期ダイアログ ボックス](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="ea860-145">[ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API を呼び出して、データ パッケージのエクスポートをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="ea860-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="ea860-146">Azure AD コネクタで HTTP から **HTTP 要求を呼び出す** アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="ea860-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="ea860-147">**基本リソース URL:** Talent 環境の URL (パス / 名前空間情報を含めないでください。)</span><span class="sxs-lookup"><span data-stu-id="ea860-147">**Base Resource URL:** The URL of your Talent environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="ea860-148">**Azure AD リソース URI:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="ea860-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="ea860-149">**ExportToPackage** のような DMF パッケージ REST API を構成するすべての API を公開するコネクタを、Core HR サービスはまだ提供していません。</span><span class="sxs-lookup"><span data-stu-id="ea860-149">The Core HR service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="ea860-150">代わりに、Azure AD コネクタで HTTP を経由して、未加工の HTTPS 要求を使用して API を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea860-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="ea860-151">このコネクターは Talent に対する認証および承認に Azure Active Directory (Azure AD) を使用します。</span><span class="sxs-lookup"><span data-stu-id="ea860-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Talent.</span></span>

        ![Azure AD コネクタの HTTP](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="ea860-153">Azure AD コネクタの HTTP 経由で Talent 環境にサインインします。</span><span class="sxs-lookup"><span data-stu-id="ea860-153">Sign in to your Talent environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="ea860-154">HTTP **POST** 要求をセットアップして **ExportToPackage** DMF REST API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea860-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="ea860-155">**メソッド:** POST</span><span class="sxs-lookup"><span data-stu-id="ea860-155">**Method:** POST</span></span>
        - <span data-ttu-id="ea860-156">**要求のUrl:** https://\<ホスト名\>/名前空間/\<名前空間\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="ea860-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="ea860-157">**B要求の本文:**</span><span class="sxs-lookup"><span data-stu-id="ea860-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![HTTP 要求アクションの呼び出し](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="ea860-159">既定の名前より意味があるように各ステップの名前を変更したい場合は、**HTTP 要求を呼び出します**。</span><span class="sxs-lookup"><span data-stu-id="ea860-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="ea860-160">たとえば、このステップの名前を **ExportToPackage** に変更できます。</span><span class="sxs-lookup"><span data-stu-id="ea860-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="ea860-161">[変数を初期化](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) して **ExportToPackage** 要求の実行状態を格納します。</span><span class="sxs-lookup"><span data-stu-id="ea860-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![変数のアクションを初期化](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="ea860-163">データ エクスポートの実行状態が **成功** になるまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="ea860-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="ea860-164">**ExecutionStatus** 変数が **成功** になるまで繰り返す [Until ループ](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) を追加します。</span><span class="sxs-lookup"><span data-stu-id="ea860-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="ea860-165">エクスポートの現在の実行状態のポーリング前に 5 秒間待機する **遅延** アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="ea860-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Until ループ コンテナー](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="ea860-167">エクスポートが完了するまで最大 75 秒 (15 イテレーション × 5 秒) 待つには、制限カウントを **15** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ea860-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="ea860-168">さらにエクスポートに時間がかかる場合は、必要に応じて制限カウントを調整してください。</span><span class="sxs-lookup"><span data-stu-id="ea860-168">If your export takes more time, adjust the limit count as appropriate.</span></span>

        > <span data-ttu-id="ea860-169">このサンプルはエラー チェックを実行しません。</span><span class="sxs-lookup"><span data-stu-id="ea860-169">This sample doesn't do error checking.</span></span> <span data-ttu-id="ea860-170">**GetExecutionSummaryStatus** API は成功しなかった端末状態 (つまり、**"成功"** 以外の状態) を返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ea860-170">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="ea860-171">詳細については [API のドキュメント](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea860-171">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

    3. <span data-ttu-id="ea860-172">**HTTP 要求の呼び出し** アクションを追加して [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API を呼び出し、 **ExecutionStatus** 変数を **GetExecutionSummaryStatus** 応答の結果に設定します。</span><span class="sxs-lookup"><span data-stu-id="ea860-172">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="ea860-173">![NOTE] エクスポートが完了するまで最大 75 秒 (15 イテレーション × 5 秒) 待つには、制限カウントを **15** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ea860-173">![NOTE] Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="ea860-174">さらにエクスポートに時間がかかる場合は、必要に応じて制限カウントを調整してください。</span><span class="sxs-lookup"><span data-stu-id="ea860-174">If your export takes more time, adjust the limit count as appropriate.</span></span>

        > <span data-ttu-id="ea860-175">このサンプルはエラー チェックを実行しません。</span><span class="sxs-lookup"><span data-stu-id="ea860-175">This sample doesn't do error checking.</span></span> <span data-ttu-id="ea860-176">**GetExecutionSummaryStatus** API は成功しなかった端末状態 (つまり、**"成功"** 以外の状態) を返す可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ea860-176">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="ea860-177">詳細については [API のドキュメント](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ea860-177">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

    3. <span data-ttu-id="ea860-178">**HTTP 要求の呼び出し** アクションを追加して [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API を呼び出し、 **ExecutionStatus** 変数を **GetExecutionSummaryStatus** 応答の結果に設定します。</span><span class="sxs-lookup"><span data-stu-id="ea860-178">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>


        - <span data-ttu-id="ea860-179">**メソッド:** POST</span><span class="sxs-lookup"><span data-stu-id="ea860-179">**Method:** POST</span></span>
        - <span data-ttu-id="ea860-180">**要求のUrl:** https://\<ホスト名\>/名前空間/\<名前空間\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="ea860-180">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="ea860-181">**要求の本文:** body('Invoke\_an\_HTTP\_request').value</span><span class="sxs-lookup"><span data-stu-id="ea860-181">**Body of the request:** body('Invoke\_an\_HTTP\_request').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="ea860-182">コード ビューまたはデザイナーの機能エディターで **要求の本文** 値を入力する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="ea860-182">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP 要求 2 アクションの呼び出し](media/integration-logic-app-get-execution-status-step.png)

        ![変数アクションの設定](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="ea860-185">デザイナーが同じ方法で値を表示するとしても、**変数を設定** アクション (**body('Invoke\_an\_HTTP\_request\_2').value**) の値は **HTTP request 2 の呼び出し** 本文値の値とは異なります。</span><span class="sxs-lookup"><span data-stu-id="ea860-185">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2').value**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="ea860-186">エクスポートしたパッケージのダウンロード URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="ea860-186">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="ea860-187">**HTTP 要求の呼び出し** アクションを追加して [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ea860-187">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="ea860-188">**メソッド:** POST</span><span class="sxs-lookup"><span data-stu-id="ea860-188">**Method:** POST</span></span>
        - <span data-ttu-id="ea860-189">**要求のUrl:** https://\<ホスト名\>/名前空間/\<名前空間\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="ea860-189">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="ea860-190">**要求の本文:**{"executionId": body('GetExportedPackageURL').value}</span><span class="sxs-lookup"><span data-stu-id="ea860-190">**Body of the request:** {"executionId": body('GetExportedPackageURL').value}</span></span>

        ![GetExportedPackageURL action](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="ea860-192">エクスポートしたパッケージのダウンロード</span><span class="sxs-lookup"><span data-stu-id="ea860-192">Download the exported package.</span></span>

    - <span data-ttu-id="ea860-193">前のステップで返された URL からパッケージをダウンロードするための HTTP **GET** 要求 (組み込み [HTTP コネクタ アクション](https://docs.microsoft.com/azure/connectors/connectors-native-http)) を追加します。</span><span class="sxs-lookup"><span data-stu-id="ea860-193">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="ea860-194">**メソッド:** GET</span><span class="sxs-lookup"><span data-stu-id="ea860-194">**Method:** GET</span></span>
        - <span data-ttu-id="ea860-195">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="ea860-195">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="ea860-196">コード ビューまたはデザイナーの機能エディターで **URI** 値を入力する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="ea860-196">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GET アクション](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="ea860-198">**GetExportedPackageUrl** API が返す URL には、ファイルをダウンロードするアクセスを許可する共有アクセス署名トークンが含まれているため、この要求は追加の認証を必要としません。</span><span class="sxs-lookup"><span data-stu-id="ea860-198">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="ea860-199">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) コネクタを使用してダウンロードしたパッケージを保存する。</span><span class="sxs-lookup"><span data-stu-id="ea860-199">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="ea860-200">OneDrive for Business の [ファイルの作成](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) アクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="ea860-200">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="ea860-201">必要に応じて OneDrive for Business アカウントを接続します。</span><span class="sxs-lookup"><span data-stu-id="ea860-201">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="ea860-202">**フォルダーのパス:** 選択したフォルダー</span><span class="sxs-lookup"><span data-stu-id="ea860-202">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="ea860-203">**ファイル名:** 作業者\_package.zip</span><span class="sxs-lookup"><span data-stu-id="ea860-203">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="ea860-204">**ファイルのコンテンツ:** 前のステップからの本文 (動的コンテンツ)</span><span class="sxs-lookup"><span data-stu-id="ea860-204">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![ファイルのアクションの作成](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="ea860-206">ステップ 3: ロジック アプリのテスト</span><span class="sxs-lookup"><span data-stu-id="ea860-206">Step 3: Test the logic app</span></span>

<span data-ttu-id="ea860-207">ロジック アプリをテストするには、デザイナーで **実行** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="ea860-207">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="ea860-208">ロジック アプリのステップが実行を開始することを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea860-208">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="ea860-209">30 から 40 秒後、ロジック アプリの実行が終了し、OneDrive for Business フォルダにエクスポートされた作業者を含む新しいパッケージ ファイルが含まれるはずです。</span><span class="sxs-lookup"><span data-stu-id="ea860-209">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="ea860-210">どこかのステップで失敗が報告された場合、デザイナーから失敗したステップを選択し、その **入力** フィールドと **出力** フィールドを確認します。</span><span class="sxs-lookup"><span data-stu-id="ea860-210">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="ea860-211">エラーを修正するため必要に応じてステップをデバッグおよび調整します。</span><span class="sxs-lookup"><span data-stu-id="ea860-211">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="ea860-212">次の図はロジック アプリのすべてのステップが正常に実行された場合のロジック アプリ デザイナーの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="ea860-212">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![成功したロジック アプリの実行](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="ea860-214">集計</span><span class="sxs-lookup"><span data-stu-id="ea860-214">Summary</span></span>

<span data-ttu-id="ea860-215">このチュートリアルではロジック アプリを使用して Core HR からデータをエクスポートして、そのエクスポートしたデータを OneDrive for Business フォルダーに保存する方法を学びました。</span><span class="sxs-lookup"><span data-stu-id="ea860-215">In this tutorial, you learned how to use a logic app to export data from Core HR and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="ea860-216">ビジネスのニーズに合わせて、このチュートリアルの手順を必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="ea860-216">You can modify the steps of this tutorial as required to suit your business needs.</span></span>
