---
title: 拡張イベントを Application Insights に記録する
description: このトピックでは、Commerce runtime (CRT) 拡張機能から顧客の Application Insights にイベントを記録する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 3bfac7da1ad0b585e7a86e5e595b6080f3052611
ms.sourcegitcommit: 7537aa8ef619eea6c48467a3ca86e3372415f8a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/18/2020
ms.locfileid: "3823443"
---
# <a name="log-extension-events-to-application-insights"></a>拡張イベントを Application Insights に記録する

[!include [banner](../includes/banner.md)]

このトピックでは、Commerce Runtime (CRT) POS 拡張機能から[顧客の Application Insights](https://docs.microsoft.com/azure/azure-monitor/app/app-insights-overview) にイベントを記録する方法について説明します。

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

4. Application Insights ページで **作成** をクリックします。

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

4. プロジェクトを構築し、出力ライブラリと **Microsoft.ApplicationInsights.dll** ファイルを **..\\RetailServer\\webroot\\bin\\Ext** にコピーし、これを使用して配置とテストを手動で行います。
5. **..\\RetailServer\\webroot\\bin\\Ext** フォルダで、**CommerceRuntime.Ext.config** ファイルを開き、事前に生成した Applications Insights のインストルメンテーション キーで **\<settings\>** セクションを更新します。 次に例を示します。

    ```xml
    <add name="ext.AppInsightsKey" value="xxxxxxx"/>
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
2. **BuildTools\\Customization.settings** ファイルを更新し、**\<ItemGroup\>** セクションに次のエントリを追加します。

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

## <a name="log-events-to-application-insights-in-the-pos-extension-projects"></a>POS 拡張プロジェクトで、イベントを Application Insights に記録する

1. **RetailSDK\POS\Extensions** フォルダーに、**ライブラリ**という名前の新しいフォルダを作成します。
2. コマンド プロンプトを開き、**ライブラリ** フォルダーに移動します。
3. **Npm** をインストールします。 **Npm** パッケージは、[OpenJS](https://nodejs.org) からダウンロードしてインストールすることができます。
4. このコマンドを実行して、JavaScript Application Insights パッケージの **Npm** パッケージをインストールします。

    ```console run the
    npm i --save @microsoft/applicationinsights-web
    ```

    パッケージをインストールした後に、**POS/Extensions/ライブラリ** フォルダに **node_modules** フォルダが含まれている必要があります。 **node_modules** フォルダには Application Insights ライブラリ ファイルが含まれています。

5. **POS/Extensions/Libraries/node_modules/@microsoft/applicationinsights-web/dist/applicationinsights-web.js** ファイルがライブラリに存在することを確認してください。

    ファイル名は、Application Insights ライブラリの将来のバージョンで変更される可能性があります。 パスが変更された場合は、手順 8 と 10 のライブラリ パスをメインの Application Insights ライブラリをポイントするパスに更新します。

6. **RetailSDK\POS** から **ModernPOS.sln**、または **CloudPos.sln** を開きます。
7. **POS.Extensions** プロジェクトにある **tsconfig.json** ファイルを開きます。 **除外**セクションで、エントリを**ライブラリ** フォルダに追加します。

    ```typescript
    "exclude": [
        "Libraries"
      ],
    ```

8. **POS.Extensions** プロジェクトにある **tsconfig.json** ファイルを開きます。 **compilerOptions** セクションで、次のプロパティを追加します。

    ```typescript
    "baseUrl": "./",
    "paths": {
        "applicationinsights-web": [ "Libraries/node_modules/@microsoft/applicationinsights-web/dist/applicationinsights-web" ]
    }
    ```

9. **CopyPosExtensionsFiles** セクションで、**Pos.Extensions.csproj** を編集します。 次のターゲットを追加して、Application Insights ライブラリを POS アプリケーションにコピーすることにより、ターゲットを拡張コードで使用できるようにします。

    ```typescript
    <JavaScriptFileList Include="Libraries\\**\\*.js">
        <InProject>false</InProject>
        <Visible>false</Visible>
    </JavaScriptFileList>
    ```

10. Application Insights ライブラリを消費している POS 拡張機能フォルダ (パッケージ) の **manifest.json** ファイルに次のノードを含めます。

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

これで、Application Insights ライブラリを POS で使用する準備が整いました。

## <a name="consume-the-library-and-log-events"></a>ライブラリ イベントとログ イベントの使用

1. **RetailSDK\POS** から **ModernPOS.sln**、または **CloudPos.sln** を開きます。
2. POS 拡張機能フォルダ (パッケージ) 内に新しい TypeScript ファイルを作成し、そのファイルに **AppInsights.ts** という名前を付けます。
3. 次のコードをファイルに貼り付けます。 コードは、Application Insights を使用してイベントを追跡するために拡張機能によって使用されます。 Azure App Insights で作成したインストルメンテーション キーを使用します。

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

4. 拡張機能コードで、次のコード例に示すように、AppInsights クラスを呼び出してイベントをログに記録します。

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
