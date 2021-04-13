---
title: 拡張イベントを Application Insights に記録する
description: このトピックでは、Commerce runtime (CRT) 拡張機能から顧客の Application Insights にイベントを記録する方法について説明します。
author: mugunthanm
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 046288851361526861b46280222f5a3cd2f87717
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793029"
---
# <a name="log-extension-events-to-application-insights"></a><span data-ttu-id="8a587-103">拡張イベントを Application Insights に記録する</span><span class="sxs-lookup"><span data-stu-id="8a587-103">Log extension events to Application Insights</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a587-104">このトピックでは、Commerce Runtime (CRT) POS 拡張機能から[顧客の Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview) にイベントを記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a587-104">This topic explains how to log events to [Customer Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview) from Commerce runtime (CRT) and POS extensions.</span></span>

## <a name="log-an-event-to-application-insights"></a><span data-ttu-id="8a587-105">イベントを Application Insights に記録します</span><span class="sxs-lookup"><span data-stu-id="8a587-105">Log an event to Application Insights</span></span>

1. <span data-ttu-id="8a587-106">[Microsoft Azureポータル](https://portal.azure.com) で Application Insights を設定し、インストルメンテーション キーを生成します。</span><span class="sxs-lookup"><span data-stu-id="8a587-106">Set up Application Insights in the [Microsoft Azure portal](https://portal.azure.com), and generate the instrumentation key.</span></span>
2. <span data-ttu-id="8a587-107">CRT を拡張して、生成した インストルメンテーション キー を使用して イベントを Application Insights に記録します。</span><span class="sxs-lookup"><span data-stu-id="8a587-107">Extend CRT to log events to Application Insights by using the instrumentation key that you generated.</span></span>

> [!NOTE]
> <span data-ttu-id="8a587-108">**RetailLogger** クラス はサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8a587-108">The **RetailLogger** class is no longer supported.</span></span> <span data-ttu-id="8a587-109">このクラスを使用している既存の拡張機能は、新しいモデルに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a587-109">Existing extensions that use this class must be migrated to the new model.</span></span>

## <a name="set-up-and-configure-application-insights-in-azure"></a><span data-ttu-id="8a587-110">Azureでの Application Insights の設定と構成</span><span class="sxs-lookup"><span data-stu-id="8a587-110">Set up and configure Application Insights in Azure</span></span>

1. <span data-ttu-id="8a587-111">[Azure ポータル](https://portal.azure.com) を開き、Azure の サブスクリプション資格情報を使用してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="8a587-111">Open the [Azure portal](https://portal.azure.com), and sign in by using your Azure subscription credentials.</span></span>
2. <span data-ttu-id="8a587-112">**リソースを作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a587-112">Select **Create a resource**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-113">![リソースの作成ボタン](media/NewResource.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-113">![Create a resource button](media/NewResource.png)</span></span>

3. <span data-ttu-id="8a587-114">**Application Insights** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8a587-114">Search for **Application Insights**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-115">![検索フィールド](media/Search.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-115">![Search field](media/Search.png)</span></span>

4. <span data-ttu-id="8a587-116">Application Insights ページで **作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a587-116">Click **Create** in the Application Insights page.</span></span>

5. <span data-ttu-id="8a587-117">**基本** タブで、 **サブスクリプション**、 **リソース グループ** 、 **名前**、 **地域** の各フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="8a587-117">On the **Basic** tab, set the **Subscription**, **Resource group**, **Name**, and **Region** fields.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-118">![基本タブ](media/CreateNew.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-118">![Basic tab](media/CreateNew.png)</span></span>

6. <span data-ttu-id="8a587-119">**レビュー + 作成** タブで、 **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a587-119">On the **Review + create** tab, select **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-120">![作成 ボタン](media/CreateConf.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-120">![Create button](media/CreateConf.png)</span></span>

7. <span data-ttu-id="8a587-121">展開処理が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="8a587-121">Wait for the deployment to be completed.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-122">![作成されたリソース](media/Completed.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-122">![Resource created](media/Completed.png)</span></span>

8. <span data-ttu-id="8a587-123">リソースへと移動し、 **インストルメンテーション キー** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="8a587-123">Go to the resource, and copy the **Instrumentation Key** value.</span></span> <span data-ttu-id="8a587-124">この値は、 CRT コードまたは CRT 拡張機能の構成ファイルで使用します。</span><span class="sxs-lookup"><span data-stu-id="8a587-124">You will use this value in the CRT code or CRT extension configuration file.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-125">![インストルメンテーション キー フィールド](media/Resource.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-125">![Instrumentation Key field](media/Resource.png)</span></span>

## <a name="extend-the-crt-extension-project-to-log-events-to-application-insights"></a><span data-ttu-id="8a587-126">CRT 拡張プロジェクトを拡張して、イベントを Application Insights に記録します。</span><span class="sxs-lookup"><span data-stu-id="8a587-126">Extend the CRT extension project to log events to Application Insights</span></span>

1. <span data-ttu-id="8a587-127">新しい C\# クラス ライブラリ プロジェクトを作成し、 **Contoso.Diagnostic** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8a587-127">Create a new C\# class library project, and name it **Contoso.Diagnostic**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-128">![新規 Contoso.Diagnostic プロジェクト](media/VSProject.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-128">![New Contoso.Diagnostic project](media/VSProject.png)</span></span>

2. <span data-ttu-id="8a587-129">次のライブラリへの参照を追加します:</span><span class="sxs-lookup"><span data-stu-id="8a587-129">Add references to the following libraries:</span></span>

    + <span data-ttu-id="8a587-130">Microsoft.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8a587-130">Microsoft.ApplicationInsights</span></span>
    + <span data-ttu-id="8a587-131">Netstandard</span><span class="sxs-lookup"><span data-stu-id="8a587-131">Netstandard</span></span>
    + <span data-ttu-id="8a587-132">Microsoft.Dynamics.Commerce.Runtime.Framework</span><span class="sxs-lookup"><span data-stu-id="8a587-132">Microsoft.Dynamics.Commerce.Runtime.Framework</span></span>

    > [!NOTE]
    > <span data-ttu-id="8a587-133">**Microsoft.ApplicationInsights** アセンブリ参照をインストールするには、 [ASP.NET Core 用の Application Insights SDK](https://nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="8a587-133">To install the **Microsoft.ApplicationInsights** assembly reference, install the [Application Insights SDK for ASP.NET Core](https://nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore).</span></span> <span data-ttu-id="8a587-134">**Microsoft.Dynamics.Commerce.Runtime.Framework** への参照は、 **..\\RetailSDK\\参照** フォルダ から追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8a587-134">The reference to **Microsoft.Dynamics.Commerce.Runtime.Framework** can be added from the **..\\RetailSDK\\Reference** folder.</span></span>

3. <span data-ttu-id="8a587-135">**ContosoLogger** という名前の新規クラス ファイルを追加し、次のコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="8a587-135">Add a new class file that is named **ContosoLogger**, and copy the following code into it.</span></span>

    ```C#
    using Microsoft.ApplicationInsights;
    using Microsoft.ApplicationInsights.Extensibility;
    using Microsoft.Dynamics.Commerce.Runtime;
    using Microsoft.Dynamics.Commerce.Runtime.Extensions;
    namespace Contoso.Diagnostic
    {
        public static class ContosoLogger
        {
            private static readonly object lockObject = new object();
            private static TelemetryClient client = null;
            public static TelemetryClient GetLogger(RequestContext context)
            {
                if (client == null)
                {
                    lock (lockObject)
                    {
                        if (client == null)
                        {
                            string key = context.Runtime.Configuration.GetSettingValue("ext.AppInsightsKey") ?? string.Empty;
                            client = new TelemetryClient(new TelemetryConfiguration(key));
                        }
                    }
                }
                return client;
            }
        }
    }
    ```

4. <span data-ttu-id="8a587-136">プロジェクトを構築し、出力ライブラリと **Microsoft.ApplicationInsights.dll** ファイルを **..\\RetailServer\\webroot\\bin\\Ext** にコピーし、これを使用して配置とテストを手動で行います。</span><span class="sxs-lookup"><span data-stu-id="8a587-136">Build the project, and copy the output library and the **Microsoft.ApplicationInsights.dll** file to the **..\\RetailServer\\webroot\\bin\\Ext** folder for manual deployment and testing.</span></span>
5. <span data-ttu-id="8a587-137">**..\\RetailServer\\webroot\\bin\\Ext** フォルダで、**CommerceRuntime.Ext.config** ファイルを開き、事前に生成した Applications Insights のインストルメンテーション キーで **\<settings\>** セクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="8a587-137">In the **..\\RetailServer\\webroot\\bin\\Ext** folder, open the **CommerceRuntime.Ext.config** file, and update the **\<settings\>** section with the Applications Insights instrumentation key that you generated earlier.</span></span> <span data-ttu-id="8a587-138">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8a587-138">Here is an example.</span></span>

    ```xml
    <add name="ext.AppInsightsKey" value="xxxxxxx"/>
    ```

6. <span data-ttu-id="8a587-139">Commerce Scale Unit を再起動します。</span><span class="sxs-lookup"><span data-stu-id="8a587-139">Restart your Commerce Scale Unit.</span></span>

## <a name="consume-the-logger-in-the-crt-extension"></a><span data-ttu-id="8a587-140">CRT 拡張機能でロガーを使用する</span><span class="sxs-lookup"><span data-stu-id="8a587-140">Consume the logger in the CRT extension</span></span>

1. <span data-ttu-id="8a587-141">拡張機能で **ContosoLogger** を使用するには、 **ContosoDiagnostic** と **Microsoft.ApplicationInsights** のアセンブリ参照を拡張機能プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="8a587-141">To consume the **ContosoLogger** in the extension, add the **ContosoDiagnostic** and **Microsoft.ApplicationInsights** assembly references to the extension project.</span></span>
2. <span data-ttu-id="8a587-142">イベントを記録するには、 **TraceTelemetry** クラスを使用し、トレースを作成します。</span><span class="sxs-lookup"><span data-stu-id="8a587-142">To log events, use the **TraceTelemetry** class, and create the traces.</span></span> <span data-ttu-id="8a587-143">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="8a587-143">Here is an example.</span></span>

    ```C#
    using Contoso.Diagnostic;
    using Microsoft.ApplicationInsights.DataContracts;
    var trace = new TraceTelemetry("CRT executing request", SeverityLevel.Information);
    trace.Properties.Add("CustomDimensionColumn1", request.RequestContext.GetTerminalId().ToString());
    trace.Properties.Add("CustomDimensionColumn2", "CRT demo - Save Cart request");
    ContosoLogger.GetLogger(request.RequestContext).TrackTrace(trace);
    ```

    > [!NOTE]
    > <span data-ttu-id="8a587-144">トレースプロパティは、クエリをトレースするにあたって簡単に追加することができるユーザー定義の分析コードです。</span><span class="sxs-lookup"><span data-stu-id="8a587-144">Trace properties are custom dimensions that you can easily add to query the traces.</span></span>

## <a name="validate-the-trace-events"></a><span data-ttu-id="8a587-145">追跡イベントの検証</span><span class="sxs-lookup"><span data-stu-id="8a587-145">Validate the trace events</span></span>

1. <span data-ttu-id="8a587-146">[Azure ポータル](https://portal.azure.com) を開き、Azure の サブスクリプション資格情報を使用してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="8a587-146">Open the [Azure portal](https://portal.azure.com), and sign in by using your Azure subscription credentials.</span></span>
2. <span data-ttu-id="8a587-147">Application Insights インスタンスに移動し、 **監視** 配下の **ログ (分析)** を選択して、新しいクエリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a587-147">Go to the Application Insights instance, and then, under **Monitoring**, select **Logs (Analytics)** to open a new query editor.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-148">![ログ分析オプション](media/AppInsightQuery.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-148">![Log Analytics option](media/AppInsightQuery.png)</span></span>

3. <span data-ttu-id="8a587-149">**スキーマ** タブで、 **追跡** をダブル クリックしてクエリ エディターに追加します。</span><span class="sxs-lookup"><span data-stu-id="8a587-149">On the **Schema** tab, double-click **traces** to add it to the query editor.</span></span> <span data-ttu-id="8a587-150">既定ては時間の範囲は、**直近の24時間** となっています。</span><span class="sxs-lookup"><span data-stu-id="8a587-150">The default time range is **Last 24 hours**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-151">![クエリ エディター に 追加されたトレース](media/Trace.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-151">![Traces added to the query editor](media/Trace.png)</span></span>

4. <span data-ttu-id="8a587-152">**実行** を選択してクエリを実行してください。</span><span class="sxs-lookup"><span data-stu-id="8a587-152">Select **Run** to run the query.</span></span> <span data-ttu-id="8a587-153">記録されたイベントが結果として表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a587-153">The logged event will appear in the results.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="8a587-154">![ログ詳細](media/TraceDetails.png)</span><span class="sxs-lookup"><span data-stu-id="8a587-154">![Log details](media/TraceDetails.png)</span></span>

## <a name="build-the-deployable-package"></a><span data-ttu-id="8a587-155">配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="8a587-155">Build the deployable package</span></span>

<span data-ttu-id="8a587-156">配置可能パッケージの作成方法の詳細については、 [配置可能なパッケージを作成する](retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a587-156">For detailed information about how to build deployable packages, see [Create deployable packages](retail-sdk/retail-sdk-packaging.md).</span></span>

1. <span data-ttu-id="8a587-157">**Contoso.Diagnostic** と **Microsoft.ApplicationInsights** のアセンブリを **\\RetailSDK\\参照** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8a587-157">Copy the **Contoso.Diagnostic** and **Microsoft.ApplicationInsights** assemblies to the **\\RetailSDK\\References** folder.</span></span>
2. <span data-ttu-id="8a587-158">**BuildTools\\Customization.settings** ファイルを更新し、**\<ItemGroup\>** セクションに次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="8a587-158">Update the **BuildTools\\Customization.settings** file, and add the following entries in the **\<ItemGroup\>** section.</span></span>

    ```xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\\Contoso.Diagnostic.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\\Microsoft.ApplicationInsights.dll" />;
    ```

3. <span data-ttu-id="8a587-159">Microsoft Visual Studio 2015 の MSBuild **Command Prompt** ウィンドウを開いて、Retail SDK フォルダのルートにある **作成** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="8a587-159">Open an MSBuild **Command Prompt** window for Microsoft Visual Studio 2015, and run the **build** command in the root of your Retail SDK folder.</span></span>
4. <span data-ttu-id="8a587-160">配備可能なパッケージを生成するには、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="8a587-160">Enter the following command to generate the deployable package.</span></span>

    ```Console
    msbuild /t:rebuild
    ```

5. <span data-ttu-id="8a587-161">**RetailSDK\\Packages\\RetailDeployablePackage** フォルダーで、配置可能パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="8a587-161">In the **RetailSDK\\Packages\\RetailDeployablePackage** folder, find the deployable package.</span></span> <span data-ttu-id="8a587-162">**content.folder** フォルダに移動して、3つのファイルがパッケージに含まれていることを確認します。(**Packages\\RetailDeployablePackage\\content.folder\\RetailServer\\Code\\bin\\ext**)</span><span class="sxs-lookup"><span data-stu-id="8a587-162">Go to the **content.folder** folder, and make sure that your three files are in the package (**Packages\\RetailDeployablePackage\\content.folder\\RetailServer\\Code\\bin\\ext**).</span></span>
6. <span data-ttu-id="8a587-163">展開可能パッケージを Microsoft Dynamics Lifecycle Services (LCS) の共有されたアセット ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8a587-163">Upload the deployable package to your Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span>
7. <span data-ttu-id="8a587-164">LCS で、ご利用の環境のメイン ページを開き、**環境の機能** \> **Retail と Commerce** \> **管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a587-164">In LCS, open your environment's main page, and select **Environment Features** \> **Retail and Commerce** \> **Manage**.</span></span>
8. <span data-ttu-id="8a587-165">**拡張機能の適用** を選択し、ライブラリから拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a587-165">Select **Apply Extension**, and select the extension from your library.</span></span>
9. <span data-ttu-id="8a587-166">拡張機能が正常に展開された後、Commerce Scale Unit に対して有効化された Modern POS (MPOS) または POS (CPOS) のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a587-166">After the extension has been successfully deployed, open an instance of Modern POS (MPOS) or POS (CPOS) that has been activated against the Commerce Scale Unit.</span></span>
10. <span data-ttu-id="8a587-167">ユーザー定義の Application Insights 記録処理 を使用する拡張シナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="8a587-167">Run the extension scenario that that uses custom Application Insights logging.</span></span>
11. <span data-ttu-id="8a587-168">Application Insights のクエリを更新し、拡張機能からのトレースが正しく記録されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8a587-168">Refresh the query in Application Insights to verify that the traces from the extension are logged correctly.</span></span>

## <a name="log-events-to-application-insights-in-the-pos-extension-projects"></a><span data-ttu-id="8a587-169">POS 拡張プロジェクトで、イベントを Application Insights に記録する</span><span class="sxs-lookup"><span data-stu-id="8a587-169">Log events to Application Insights in the POS extension projects</span></span>

1. <span data-ttu-id="8a587-170">**RetailSDK\POS\Extensions** フォルダーに、**ライブラリ** という名前の新しいフォルダを作成します。</span><span class="sxs-lookup"><span data-stu-id="8a587-170">In the **RetailSDK\POS\Extensions** folder, create a new folder named  **Libraries**.</span></span>
2. <span data-ttu-id="8a587-171">コマンド プロンプトを開き、**ライブラリ** フォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="8a587-171">Open a command prompt and navigate to the **Libraries** folder.</span></span>
3. <span data-ttu-id="8a587-172">**Npm** をインストールします。</span><span class="sxs-lookup"><span data-stu-id="8a587-172">Install **npm**.</span></span> <span data-ttu-id="8a587-173">**Npm** パッケージは、[OpenJS](https://nodejs.org) からダウンロードしてインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="8a587-173">The **npm** package can be downloaded and installed from [OpenJS](https://nodejs.org).</span></span>
4. <span data-ttu-id="8a587-174">このコマンドを実行して、JavaScript Application Insights パッケージの **Npm** パッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="8a587-174">Run this command to install the **npm** package for the JavaScript Application Insights package.</span></span>

    ```console run the
    npm i --save @microsoft/applicationinsights-web
    ```

    <span data-ttu-id="8a587-175">パッケージをインストールした後に、**POS/Extensions/ライブラリ** フォルダに **node_modules** フォルダが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a587-175">After the package is installed, the **POS/Extensions/Libraries** folder should contain the **node_modules** folder.</span></span> <span data-ttu-id="8a587-176">**node_modules** フォルダには Application Insights ライブラリ ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8a587-176">The **node_modules** folder contains the Application Insights library files.</span></span>

5. <span data-ttu-id="8a587-177">**POS/Extensions/Libraries/node_modules/@microsoft/applicationinsights-web/dist/applicationinsights-web.js** ファイルがライブラリに存在することを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8a587-177">Check that the file **POS/Extensions/Libraries/node_modules/@microsoft/applicationinsights-web/dist/applicationinsights-web.js** exists in the library.</span></span>

    <span data-ttu-id="8a587-178">ファイル名は、Application Insights ライブラリの将来のバージョンで変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8a587-178">The file name might change in future versions of the Application Insights library.</span></span> <span data-ttu-id="8a587-179">パスが変更された場合は、手順 8 と 10 のライブラリ パスをメインの Application Insights ライブラリをポイントするパスに更新します。</span><span class="sxs-lookup"><span data-stu-id="8a587-179">If the path changes, update the library path in steps 8 and 10 to a path that points to the main Application Insights library.</span></span>

6. <span data-ttu-id="8a587-180">**RetailSDK\POS** から **ModernPOS.sln**、または **CloudPos.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="8a587-180">Open **ModernPOS.sln** or **CloudPos.sln** from **RetailSDK\POS**.</span></span>
7. <span data-ttu-id="8a587-181">**POS.Extensions** プロジェクトにある **tsconfig.json** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a587-181">Open the **tsconfig.json** file from the **POS.Extensions** project.</span></span> <span data-ttu-id="8a587-182">**除外** セクションで、エントリを **ライブラリ** フォルダに追加します。</span><span class="sxs-lookup"><span data-stu-id="8a587-182">Under the **exclude** section, add an entry to the **Libraries** folder.</span></span>

    ```typescript
    "exclude": [
        "Libraries"
      ],
    ```

8. <span data-ttu-id="8a587-183">**POS.Extensions** プロジェクトにある **tsconfig.json** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a587-183">Open the **tsconfig.json** file from the **POS.Extensions** project.</span></span> <span data-ttu-id="8a587-184">**compilerOptions** セクションで、次のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="8a587-184">Under the **compilerOptions** section, add the following properties.</span></span>

    ```typescript
    "baseUrl": "./",
    "paths": {
        "applicationinsights-web": [ "Libraries/node_modules/@microsoft/applicationinsights-web/dist/applicationinsights-web" ]
    }
    ```

9. <span data-ttu-id="8a587-185">**CopyPosExtensionsFiles** セクションで、**Pos.Extensions.csproj** を編集します。</span><span class="sxs-lookup"><span data-stu-id="8a587-185">Edit the **Pos.Extensions.csproj** file in the **CopyPosExtensionsFiles** section.</span></span> <span data-ttu-id="8a587-186">次のターゲットを追加して、Application Insights ライブラリを POS アプリケーションにコピーすることにより、ターゲットを拡張コードで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8a587-186">Add the following targets to copy the Application Insights library to the POS application, so that the targets can be consumed by the extension code.</span></span>

    ```typescript
    <JavaScriptFileList Include="Libraries\\**\\*.js">
        <InProject>false</InProject>
        <Visible>false</Visible>
    </JavaScriptFileList>
    ```

10. <span data-ttu-id="8a587-187">Application Insights ライブラリを消費している POS 拡張機能フォルダ (パッケージ) の **manifest.json** ファイルに次のノードを含めます。</span><span class="sxs-lookup"><span data-stu-id="8a587-187">Include the following node in the **manifest.json** file of the POS extension folder (package) that is consuming the Application Insights library.</span></span>

    ```typescript
    {
      "dependencies": [
        {
          "alias": "applicationinsights-web",
          "format": "amd",
          "modulePath": "../Libraries/node_modules/@microsoft/applicationinsights-web/dist/applicationinsights-web"
        }
      ]
    }
    ```

<span data-ttu-id="8a587-188">これで、Application Insights ライブラリを POS で使用する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="8a587-188">The Application Insights library is now ready to be consumed and used in POS.</span></span>

## <a name="consume-the-library-and-log-events"></a><span data-ttu-id="8a587-189">ライブラリ イベントとログ イベントの使用</span><span class="sxs-lookup"><span data-stu-id="8a587-189">Consume the library and log events</span></span>

1. <span data-ttu-id="8a587-190">**RetailSDK\POS** から **ModernPOS.sln**、または **CloudPos.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="8a587-190">Open the **ModernPOS.sln** or **CloudPos.sln** solution from **RetailSDK\POS**.</span></span>
2. <span data-ttu-id="8a587-191">POS 拡張機能フォルダ (パッケージ) 内に新しい TypeScript ファイルを作成し、そのファイルに **AppInsights.ts** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="8a587-191">Create a new TypeScript file inside the POS extension folder (package) and name it **AppInsights.ts**.</span></span>
3. <span data-ttu-id="8a587-192">次のコードをファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="8a587-192">Copy the following code to the file.</span></span> <span data-ttu-id="8a587-193">コードは、Application Insights を使用してイベントを追跡するために拡張機能によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="8a587-193">The code is used by the extensions to track events using Application Insights.</span></span> <span data-ttu-id="8a587-194">Azure App Insights で作成したインストルメンテーション キーを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a587-194">Use the instrumentation key created in Azure App Insights.</span></span>

    ```typescript
    import { ApplicationInsights } from "applicationinsights-web";

    /**
     * Example implementation of an Application Insights singleton that can be used to log events and metrics on Application Insights.
     */
    export class AppInsights {
        private static _instance: AppInsights = null;
        private _applicationInsights: ApplicationInsights = null;

        /**
         * Gets a global reference to an Application Insights reference that can be used by other extension code.
         * @returns {ApplicationInsights} The ApplicationInsights instance that can be used to log events.
         */
        public static get instance(): ApplicationInsights {
            if (AppInsights._instance === null) {
                AppInsights._instance = new AppInsights();
            }

            return AppInsights._instance._applicationInsights;
        }

        /**
         * Initializes a new instance of AppInsights.
         */
        constructor() {
            this._applicationInsights = new ApplicationInsights({
                config: {
                    instrumentationKey: 'YOUR_INSTRUMENTATION_KEY_GOES_HERE'
                    /* ...Other Configuration Options... */
                }
            });
            this._applicationInsights.loadAppInsights();
        }
    }
    ```

4. <span data-ttu-id="8a587-195">拡張機能コードで、次のコード例に示すように、AppInsights クラスを呼び出してイベントをログに記録します。</span><span class="sxs-lookup"><span data-stu-id="8a587-195">In the extension code, log the events by calling the AppInsights class as shown in the following code example.</span></span>

    ```typescript
    AppInsights.instance.trackEvent({
        name: "extensionTest",
        properties: {
            "property1": "value1",
            "property2": "value2",
        },
        measurements: {
            "measurement1": 1,
            "measurement2": 2,
        },
    });
    ```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]