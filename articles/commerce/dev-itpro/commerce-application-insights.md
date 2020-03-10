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
# <a name="log-extension-events-to-application-insights"></a>拡張イベントを Application Insights に記録する

[!include [banner](../includes/banner.md)]

このトピックでは、Commerce runtime (CRT) 拡張機能から [顧客の Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview) にイベントを記録する方法について説明します。

## <a name="log-an-event-to-application-insights"></a>イベントを Application Insights に記録します

1. [Microsoft Azureポータル](https://portal.azure.com) で Application Insights を設定し、インストルメンテーション キーを生成します。
2. CRT を拡張して、生成した インストルメンテーション キー を使用して イベントを Application Insights に記録します。

> [!NOTE]
> **RetailLogger** クラス はサポートされなくなりました。 このクラスを使用している既存の拡張機能は、新しいモデルに移行する必要があります。

## <a name="set-up-and-configure-application-insights-in-azure"></a>Azureでの Application Insights の設定と構成

1. [Azure ポータル](https://portal.azure.com) を開き、Azure の サブスクリプション資格情報を使用してサイン インします。
2. **リソースを作成する** を選択します。

    > [!div class="mx-imgBorder"]
    > ![リソースの作成ボタン](media/NewResource.png)

3. **Application Insights** を検索します。

    > [!div class="mx-imgBorder"]
    > ![検索フィールド](media/Search.png)

4. **作成**を選択します。

    > [!div class="mx-imgBorder"]
    > ![作成 ボタン](media/Create.png)

5. **基本** タブで、 **サブスクリプション**、 **リソース グループ** 、 **名前**、 **地域** の各フィールドを設定します。

    > [!div class="mx-imgBorder"]
    > ![基本タブ](media/CreateNew.png)

6. **レビュー + 作成** タブで、 **作成**を選択します。

    > [!div class="mx-imgBorder"]
    > ![作成 ボタン](media/CreateConf.png)

7. 展開処理が完了するまで待機します。

    > [!div class="mx-imgBorder"]
    > ![作成されたリソース](media/Completed.png)

8. リソースへと移動し、 **インストルメンテーション キー** の値をコピーします。 この値は、 CRT コードまたは CRT 拡張機能の構成ファイルで使用します。

    > [!div class="mx-imgBorder"]
    > ![インストルメンテーション キー フィールド](media/Resource.png)

## <a name="extend-the-crt-extension-project-to-log-events-to-application-insights"></a>CRT 拡張プロジェクトを拡張して、イベントを Application Insights に記録します。

1. 新しい C\# クラス ライブラリ プロジェクトを作成し、 **Contoso.Diagnostic** という名前を付けます。

    > [!div class="mx-imgBorder"]
    > ![新規 Contoso.Diagnostic プロジェクト](media/VSProject.png)

2. 次のライブラリへの参照を追加します:

    + Microsoft.ApplicationInsights
    + Netstandard
    + Microsoft.Dynamics.Commerce.Runtime.Framework

    > [!NOTE]
    > **Microsoft.ApplicationInsights** アセンブリ参照をインストールするには、 [ASP.NET Core 用の Application Insights SDK](https://nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore) をインストールします。 **Microsoft.Dynamics.Commerce.Runtime.Framework** への参照は、 **..\\RetailSDK\\参照** フォルダ から追加することができます。

3. **ContosoLogger** という名前の新規クラス ファイルを追加し、次のコードをコピーします。

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

4. プロジェクトを構築し、出力ライブラリと **Microsoft.ApplicationInsights.dll** ファイルを **..\\RetailServer\\webroot\\bin\\Ext** にコピーし、これを使用して配置とテストを手動で行います。
5. **..\\RetailServer\\webroot\\bin\\Ext** フォルダで、 **CommerceRuntime.Ext.config** ファイルを開き、 **\<設定\>** セクションを事前に生成したアプリケーション 分析情報の インストルメンテーション キーで更新します。 次に例を示します。

    ```xml
    <add name="ext.AppInsightsKey" value="xxxxxxx"/>;
    ```

6. Commerce Scale Unit を再起動します。

## <a name="consume-the-logger-in-the-crt-extension"></a>CRT 拡張機能でロガーを使用する

1. 拡張機能で **ContosoLogger** を使用するには、 **ContosoDiagnostic** と **Microsoft.ApplicationInsights** のアセンブリ参照を拡張機能プロジェクトに追加します。
2. イベントを記録するには、 **TraceTelemetry** クラスを使用し、トレースを作成します。 次に例を示します。

    ```C#
    using Contoso.Diagnostic;
    using Microsoft.ApplicationInsights.DataContracts;
    var trace = new TraceTelemetry("CRT executing request", SeverityLevel.Information);
    trace.Properties.Add("CustomDimensionColumn1", request.RequestContext.GetTerminalId().ToString());
    trace.Properties.Add("CustomDimensionColumn2", "CRT demo - Save Cart request");
    ContosoLogger.GetLogger(request.RequestContext).TrackTrace(trace);
    ```

    > [!NOTE]
    > トレースプロパティは、クエリをトレースするにあたって簡単に追加することができるユーザー定義の分析コードです。

## <a name="validate-the-trace-events"></a>追跡イベントの検証

1. [Azure ポータル](https://portal.azure.com) を開き、Azure の サブスクリプション資格情報を使用してサイン インします。
2. Application Insights インスタンスに移動し、 **監視** 配下の **ログ (分析)** を選択して、新しいクエリ エディターを開きます。

    > [!div class="mx-imgBorder"]
    > ![ログ分析オプション](media/AppInsightQuery.png)

3. **スキーマ** タブで、 **追跡** をダブル クリックしてクエリ エディターに追加します。 既定ては時間の範囲は、**直近の24時間** となっています。

    > [!div class="mx-imgBorder"]
    > ![クエリ エディター に 追加されたトレース](media/Trace.png)

4. **実行** を選択してクエリを実行してください。 記録されたイベントが結果として表示されます。

    > [!div class="mx-imgBorder"]
    > ![ログ詳細](media/TraceDetails.png)

## <a name="build-the-deployable-package"></a>配置可能なパッケージを作成します。

配置可能パッケージの作成方法の詳細については、 [配置可能なパッケージを作成する](retail-sdk/retail-sdk-packaging.md) を参照してください。

1. **Contoso.Diagnostic** と **Microsoft.ApplicationInsights** のアセンブリを **\\RetailSDK\\参照** フォルダーにコピーします。
2. **BuildTools\\Customization.settings** ファイルを更新し、 **\<ItemGroup\>** セクションに次のエントリを追加します。

    ```xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\\Contoso.Diagnostic.dll" />
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\\Microsoft.ApplicationInsights.dll" />;
    ```

3. Microsoft Visual Studio 2015 の MSBuild **Command Prompt** ウィンドウを開いて、Retail SDK フォルダのルートにある **作成** コマンドを実行します。
4. 配備可能なパッケージを生成するには、次のコマンドを入力します。

    ```Console
    msbuild /t:rebuild
    ```

5. **RetailSDK\\Packages\\RetailDeployablePackage** フォルダーで、配置可能パッケージを検索します。 **content.folder** フォルダに移動して、3つのファイルがパッケージに含まれていることを確認します。(**Packages\\RetailDeployablePackage\\content.folder\\RetailServer\\Code\\bin\\ext**)
6. 展開可能パッケージを Microsoft Dynamics Lifecycle Services (LCS) の共有されたアセット ライブラリにアップロードします。
7. LCS で、ご利用の環境のメイン ページを開き、**環境の機能** \> **Retail と Commerce** \> **管理**を選択します。
8. **拡張機能の適用** を選択し、ライブラリから拡張機能を選択します。
9. 拡張機能が正常に展開された後、Commerce Scale Unit に対して有効化された Modern POS (MPOS) または POS (CPOS) のインスタンスを開きます。
10. ユーザー定義の Application Insights 記録処理 を使用する拡張シナリオを実行します。
11. Application Insights のクエリを更新し、拡張機能からのトレースが正しく記録されていることを確認します。
