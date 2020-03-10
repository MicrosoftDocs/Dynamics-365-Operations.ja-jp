---
title: 拡張イベントを Application Insights に記録する
description: このトピックでは、Commerce runtime (CRT) 拡張機能から顧客の Application Insights にイベントを記録する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: f5e84265cc2a5b14849a5bb47b0f492a0b0f2218
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057897"
---
# <a name="log-extension-events-to-application-insights"></a><span data-ttu-id="523c7-103">拡張イベントを Application Insights に記録する</span><span class="sxs-lookup"><span data-stu-id="523c7-103">Log extension events to Application Insights</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="523c7-104">このトピックでは、Commerce runtime (CRT) 拡張機能から [顧客の Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview) にイベントを記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="523c7-104">This topic explains how to log events to [Customer Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview) from Commerce runtime (CRT) extensions.</span></span>

## <a name="log-an-event-to-application-insights"></a><span data-ttu-id="523c7-105">イベントを Application Insights に記録します</span><span class="sxs-lookup"><span data-stu-id="523c7-105">Log an event to Application Insights</span></span>

1. <span data-ttu-id="523c7-106">[Microsoft Azureポータル](https://portal.azure.com) で Application Insights を設定し、インストルメンテーション キーを生成します。</span><span class="sxs-lookup"><span data-stu-id="523c7-106">Set up Application Insights in the [Microsoft Azure portal](https://portal.azure.com), and generate the instrumentation key.</span></span>
2. <span data-ttu-id="523c7-107">CRT を拡張して、生成した インストルメンテーション キー を使用して イベントを Application Insights に記録します。</span><span class="sxs-lookup"><span data-stu-id="523c7-107">Extend CRT to log events to Application Insights by using the instrumentation key that you generated.</span></span>

> [!NOTE]
> <span data-ttu-id="523c7-108">**RetailLogger** クラス はサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="523c7-108">The **RetailLogger** class is no longer supported.</span></span> <span data-ttu-id="523c7-109">このクラスを使用している既存の拡張機能は、新しいモデルに移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="523c7-109">Existing extensions that use this class must be migrated to the new model.</span></span>

## <a name="set-up-and-configure-application-insights-in-azure"></a><span data-ttu-id="523c7-110">Azureでの Application Insights の設定と構成</span><span class="sxs-lookup"><span data-stu-id="523c7-110">Set up and configure Application Insights in Azure</span></span>

1. <span data-ttu-id="523c7-111">[Azure ポータル](https://portal.azure.com) を開き、Azure の サブスクリプション資格情報を使用してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="523c7-111">Open the [Azure portal](https://portal.azure.com), and sign in by using your Azure subscription credentials.</span></span>
2. <span data-ttu-id="523c7-112">**リソースを作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="523c7-112">Select **Create a resource**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-113">![リソースの作成ボタン](media/NewResource.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-113">![Create a resource button](media/NewResource.png)</span></span>

3. <span data-ttu-id="523c7-114">**Application Insights** を検索します。</span><span class="sxs-lookup"><span data-stu-id="523c7-114">Search for **Application Insights**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-115">![検索フィールド](media/Search.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-115">![Search field](media/Search.png)</span></span>

4. <span data-ttu-id="523c7-116">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="523c7-116">Select **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-117">![作成 ボタン](media/Create.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-117">![Create button](media/Create.png)</span></span>

5. <span data-ttu-id="523c7-118">**基本** タブで、 **サブスクリプション**、 **リソース グループ** 、 **名前**、 **地域** の各フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="523c7-118">On the **Basic** tab, set the **Subscription**, **Resource group**, **Name**, and **Region** fields.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-119">![基本タブ](media/CreateNew.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-119">![Basic tab](media/CreateNew.png)</span></span>

6. <span data-ttu-id="523c7-120">**レビュー + 作成** タブで、 **作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="523c7-120">On the **Review + create** tab, select **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-121">![作成 ボタン](media/CreateConf.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-121">![Create button](media/CreateConf.png)</span></span>

7. <span data-ttu-id="523c7-122">展開処理が完了するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="523c7-122">Wait for the deployment to be completed.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-123">![作成されたリソース](media/Completed.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-123">![Resource created](media/Completed.png)</span></span>

8. <span data-ttu-id="523c7-124">リソースへと移動し、 **インストルメンテーション キー** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="523c7-124">Go to the resource, and copy the **Instrumentation Key** value.</span></span> <span data-ttu-id="523c7-125">この値は、 CRT コードまたは CRT 拡張機能の構成ファイルで使用します。</span><span class="sxs-lookup"><span data-stu-id="523c7-125">You will use this value in the CRT code or CRT extension configuration file.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-126">![インストルメンテーション キー フィールド](media/Resource.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-126">![Instrumentation Key field](media/Resource.png)</span></span>

## <a name="extend-the-crt-extension-project-to-log-events-to-application-insights"></a><span data-ttu-id="523c7-127">CRT 拡張プロジェクトを拡張して、イベントを Application Insights に記録します。</span><span class="sxs-lookup"><span data-stu-id="523c7-127">Extend the CRT extension project to log events to Application Insights</span></span>

1. <span data-ttu-id="523c7-128">新しい C\# クラス ライブラリ プロジェクトを作成し、 **Contoso.Diagnostic** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="523c7-128">Create a new C\# class library project, and name it **Contoso.Diagnostic**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-129">![新規 Contoso.Diagnostic プロジェクト](media/VSProject.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-129">![New Contoso.Diagnostic project](media/VSProject.png)</span></span>

2. <span data-ttu-id="523c7-130">次のライブラリへの参照を追加します:</span><span class="sxs-lookup"><span data-stu-id="523c7-130">Add references to the following libraries:</span></span>

    + <span data-ttu-id="523c7-131">Microsoft.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="523c7-131">Microsoft.ApplicationInsights</span></span>
    + <span data-ttu-id="523c7-132">Netstandard</span><span class="sxs-lookup"><span data-stu-id="523c7-132">Netstandard</span></span>
    + <span data-ttu-id="523c7-133">Microsoft.Dynamics.Commerce.Runtime.Framework</span><span class="sxs-lookup"><span data-stu-id="523c7-133">Microsoft.Dynamics.Commerce.Runtime.Framework</span></span>

    > [!NOTE]
    > <span data-ttu-id="523c7-134">**Microsoft.ApplicationInsights** アセンブリ参照をインストールするには、 [ASP.NET Core 用の Application Insights SDK](https://nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="523c7-134">To install the **Microsoft.ApplicationInsights** assembly reference, install the [Application Insights SDK for ASP.NET Core](https://nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore).</span></span> <span data-ttu-id="523c7-135">**Microsoft.Dynamics.Commerce.Runtime.Framework** への参照は、 **..\\RetailSDK\\参照** フォルダ から追加することができます。</span><span class="sxs-lookup"><span data-stu-id="523c7-135">The reference to **Microsoft.Dynamics.Commerce.Runtime.Framework** can be added from the **..\\RetailSDK\\Reference** folder.</span></span>

3. <span data-ttu-id="523c7-136">**ContosoLogger** という名前の新規クラス ファイルを追加し、次のコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="523c7-136">Add a new class file that is named **ContosoLogger**, and copy the following code into it.</span></span>

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
                            string key = context.Runtime.Configuration.GetSettingValue("ext.AppInsightsKey");
                            client = new TelemetryClient(new TelemetryConfiguration(key));
                        }
                    }
                }
                return client;
            }
        }
    }
    ```

4. <span data-ttu-id="523c7-137">プロジェクトを構築し、出力ライブラリと **Microsoft.ApplicationInsights.dll** ファイルを **..\\RetailServer\\webroot\\bin\\Ext** にコピーし、これを使用して配置とテストを手動で行います。</span><span class="sxs-lookup"><span data-stu-id="523c7-137">Build the project, and copy the output library and the **Microsoft.ApplicationInsights.dll** file to the **..\\RetailServer\\webroot\\bin\\Ext** folder for manual deployment and testing.</span></span>
5. <span data-ttu-id="523c7-138">**..\\RetailServer\\webroot\\bin\\Ext** フォルダで、 **CommerceRuntime.Ext.config** ファイルを開き、 **\<設定\>** セクションを事前に生成したアプリケーション 分析情報の インストルメンテーション キーで更新します。</span><span class="sxs-lookup"><span data-stu-id="523c7-138">In the **..\\RetailServer\\webroot\\bin\\Ext** folder, open the **CommerceRuntime.Ext.config** file, and update the **\<settings\>** section with the Applications Insights instrumentation key that you generated earlier.</span></span> <span data-ttu-id="523c7-139">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="523c7-139">Here is an example.</span></span>

    ```xml
    <add name="ext.AppInsightsKey" value="xxxxxxx"/>;
    ```

6. <span data-ttu-id="523c7-140">Commerce Scale Unit を再起動します。</span><span class="sxs-lookup"><span data-stu-id="523c7-140">Restart your Commerce Scale Unit.</span></span>

## <a name="consume-the-logger-in-the-crt-extension"></a><span data-ttu-id="523c7-141">CRT 拡張機能でロガーを使用する</span><span class="sxs-lookup"><span data-stu-id="523c7-141">Consume the logger in the CRT extension</span></span>

1. <span data-ttu-id="523c7-142">拡張機能で **ContosoLogger** を使用するには、 **ContosoDiagnostic** と **Microsoft.ApplicationInsights** のアセンブリ参照を拡張機能プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="523c7-142">To consume the **ContosoLogger** in the extension, add the **ContosoDiagnostic** and **Microsoft.ApplicationInsights** assembly references to the extension project.</span></span>
2. <span data-ttu-id="523c7-143">イベントを記録するには、 **TraceTelemetry** クラスを使用し、トレースを作成します。</span><span class="sxs-lookup"><span data-stu-id="523c7-143">To log events, use the **TraceTelemetry** class, and create the traces.</span></span> <span data-ttu-id="523c7-144">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="523c7-144">Here is an example.</span></span>

    ```C#
    using Contoso.Diagnostic;
    using Microsoft.ApplicationInsights.DataContracts;
    var trace = new TraceTelemetry("CRT executing request", SeverityLevel.Information);
    trace.Properties.Add("CustomDimensionColumn1", request.RequestContext.GetTerminalId().ToString());
    trace.Properties.Add("CustomDimensionColumn2", "CRT demo - Save Cart request");
    ContosoLogger.GetLogger(request.RequestContext).TrackTrace(trace);
    ```

    > [!NOTE]
    > <span data-ttu-id="523c7-145">トレースプロパティは、クエリをトレースするにあたって簡単に追加することができるユーザー定義の分析コードです。</span><span class="sxs-lookup"><span data-stu-id="523c7-145">Trace properties are custom dimensions that you can easily add to query the traces.</span></span>

## <a name="validate-the-trace-events"></a><span data-ttu-id="523c7-146">追跡イベントの検証</span><span class="sxs-lookup"><span data-stu-id="523c7-146">Validate the trace events</span></span>

1. <span data-ttu-id="523c7-147">[Azure ポータル](https://portal.azure.com) を開き、Azure の サブスクリプション資格情報を使用してサイン インします。</span><span class="sxs-lookup"><span data-stu-id="523c7-147">Open the [Azure portal](https://portal.azure.com), and sign in by using your Azure subscription credentials.</span></span>
2. <span data-ttu-id="523c7-148">Application Insights インスタンスに移動し、 **監視** 配下の **ログ (分析)** を選択して、新しいクエリ エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="523c7-148">Go to the Application Insights instance, and then, under **Monitoring**, select **Logs (Analytics)** to open a new query editor.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-149">![ログ分析オプション](media/AppInsightQuery.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-149">![Log Analytics option](media/AppInsightQuery.png)</span></span>

3. <span data-ttu-id="523c7-150">**スキーマ** タブで、 **追跡** をダブル クリックしてクエリ エディターに追加します。</span><span class="sxs-lookup"><span data-stu-id="523c7-150">On the **Schema** tab, double-click **traces** to add it to the query editor.</span></span> <span data-ttu-id="523c7-151">既定ては時間の範囲は、**直近の24時間** となっています。</span><span class="sxs-lookup"><span data-stu-id="523c7-151">The default time range is **Last 24 hours**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-152">![クエリ エディター に 追加されたトレース](media/Trace.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-152">![Traces added to the query editor](media/Trace.png)</span></span>

4. <span data-ttu-id="523c7-153">**実行** を選択してクエリを実行してください。</span><span class="sxs-lookup"><span data-stu-id="523c7-153">Select **Run** to run the query.</span></span> <span data-ttu-id="523c7-154">記録されたイベントが結果として表示されます。</span><span class="sxs-lookup"><span data-stu-id="523c7-154">The logged event will appear in the results.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="523c7-155">![ログ詳細](media/TraceDetails.png)</span><span class="sxs-lookup"><span data-stu-id="523c7-155">![Log details](media/TraceDetails.png)</span></span>

## <a name="build-the-deployable-package"></a><span data-ttu-id="523c7-156">配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="523c7-156">Build the deployable package</span></span>

<span data-ttu-id="523c7-157">配置可能パッケージの作成方法の詳細については、 [配置可能なパッケージを作成する](retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="523c7-157">For detailed information about how to build deployable packages, see [Create deployable packages](retail-sdk/retail-sdk-packaging.md).</span></span>

1. <span data-ttu-id="523c7-158">**Contoso.Diagnostic** と **Microsoft.ApplicationInsights** のアセンブリを **\\RetailSDK\\参照** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="523c7-158">Copy the **Contoso.Diagnostic** and **Microsoft.ApplicationInsights** assemblies to the **\\RetailSDK\\References** folder.</span></span>
2. <span data-ttu-id="523c7-159">**BuildTools\\Customization.settings** ファイルを更新し、 **\<ItemGroup\>** セクションに次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="523c7-159">Update the **BuildTools\\Customization.settings** file, and add the following entries in the **\<ItemGroup\>** section.</span></span>

    ```xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\\Contoso.Diagnostic.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\\Microsoft.ApplicationInsights.dll" />;
    ```

3. <span data-ttu-id="523c7-160">Microsoft Visual Studio 2015 の MSBuild **Command Prompt** ウィンドウを開いて、Retail SDK フォルダのルートにある **作成** コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="523c7-160">Open an MSBuild **Command Prompt** window for Microsoft Visual Studio 2015, and run the **build** command in the root of your Retail SDK folder.</span></span>
4. <span data-ttu-id="523c7-161">配備可能なパッケージを生成するには、次のコマンドを入力します。</span><span class="sxs-lookup"><span data-stu-id="523c7-161">Enter the following command to generate the deployable package.</span></span>

    ```Console
    msbuild /t:rebuild
    ```

5. <span data-ttu-id="523c7-162">**RetailSDK\\Packages\\RetailDeployablePackage** フォルダーで、配置可能パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="523c7-162">In the **RetailSDK\\Packages\\RetailDeployablePackage** folder, find the deployable package.</span></span> <span data-ttu-id="523c7-163">**content.folder** フォルダに移動して、3つのファイルがパッケージに含まれていることを確認します。(**Packages\\RetailDeployablePackage\\content.folder\\RetailServer\\Code\\bin\\ext**)</span><span class="sxs-lookup"><span data-stu-id="523c7-163">Go to the **content.folder** folder, and make sure that your three files are in the package (**Packages\\RetailDeployablePackage\\content.folder\\RetailServer\\Code\\bin\\ext**).</span></span>
6. <span data-ttu-id="523c7-164">展開可能パッケージを Microsoft Dynamics Lifecycle Services (LCS) の共有されたアセット ライブラリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="523c7-164">Upload the deployable package to your Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span>
7. <span data-ttu-id="523c7-165">LCS で、ご利用の環境のメイン ページを開き、**環境の機能** \> **Retail と Commerce** \> **管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="523c7-165">In LCS, open your environment's main page, and select **Environment Features** \> **Retail and Commerce** \> **Manage**.</span></span>
8. <span data-ttu-id="523c7-166">**拡張機能の適用** を選択し、ライブラリから拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="523c7-166">Select **Apply Extension**, and select the extension from your library.</span></span>
9. <span data-ttu-id="523c7-167">拡張機能が正常に展開された後、Commerce Scale Unit に対して有効化された Modern POS (MPOS) または POS (CPOS) のインスタンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="523c7-167">After the extension has been successfully deployed, open an instance of Modern POS (MPOS) or POS (CPOS) that has been activated against the Commerce Scale Unit.</span></span>
10. <span data-ttu-id="523c7-168">ユーザー定義の Application Insights 記録処理 を使用する拡張シナリオを実行します。</span><span class="sxs-lookup"><span data-stu-id="523c7-168">Run the extension scenario that that uses custom Application Insights logging.</span></span>
11. <span data-ttu-id="523c7-169">Application Insights のクエリを更新し、拡張機能からのトレースが正しく記録されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="523c7-169">Refresh the query in Application Insights to verify that the traces from the extension are logged correctly.</span></span>
