---
title: POS と新しいハードウェア デバイスの統合
description: このトピックでは、新しいハードウェア デバイスに販売時点管理 (POS) を統合する方法について説明します。
author: mugunthanm
ms.date: 07/27/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 7.3.0, Retail July 2017 update, AX 10.0.11
ms.openlocfilehash: 308eaa6ee1bd96a84cb8bba752ad446507b19d93
ms.sourcegitcommit: f1ef61ee3d731f68e11a5bebc154ed33a7b8eda5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383814"
---
# <a name="integrate-the-pos-with-a-new-hardware-device"></a>POS と新しいハードウェア デバイスの統合

[!include [banner](../../includes/banner.md)]

このトピックでは、新しいハードウェア デバイスに販売時点管理 (POS) を統合する方法について説明します。 

POS からハードウェア ステーションを呼び出すには、要求と応答を使用する必要があります。

+ **HardwareStationDeviceActionRequest** – POS からハードウェア ステーションに送信される要求。
+ **HardwareStationDeviceActionResponse** – ハードウェア ステーションから POS が受信した要求。

拡張するクラスは、使用している Retail ソフトウェア開発キット (SDK) のバージョンによって異なります。

+ Retail SDK バージョン 10.0.11 以降では、**IController** インターフェイスを拡張します。
+ バージョン 10.0.11 以前の Retail SDK バージョンでは、**HardwareStationController** および **IHardwareStationController** のクラスを拡張します。

## <a name="hardwarestationdeviceactionrequest"></a>HardwareStationDeviceActionRequest

次のコード例は、**HardwareStationDeviceActionRequest** の定義を示します。

```TypeScript
class HardwareStationDeviceActionRequest<TResponse extends HardwareStationDeviceActionResponse> extends Request<TResponse> {
    readonly device: string;
    readonly action: string;
    readonly actionData: any;
    constructor(device: string, action: string, actionData: any, correlationId?: string);
}
```

次の表では、パラメーターについて説明します。

| パラメーター  | データ型 | 説明 |
|------------|-----------|-------------|
| デバイス     | 文字列    | ハードウェア ステーションの要求に渡されるデバイス名は、ハードウェア ステーションのデバイス拡張機能コントローラー クラスに追加される **エクスポート** 属性と一致している必要があります。 |
| アクション     | 文字列    | ハードウェア ステーション拡張機能で呼び出す必要があるメソッド。 メソッド名は、文字列値として渡される必要があります。 コア POS ハードウェア ステーションの層レイヤーは、ハードウェア ステーション拡張機能コードから対応するメソッドを呼び出します。 このメソッドは、ハードウェア ステーション拡張機能のメソッド名と完全に一致する必要があります。 ハードウェア ステーション拡張機能は、パラメータとして渡す必要があります。 |
| actionData | any       | 拡張機能を渡すためのカスタム パラメーター。 |

### <a name="sample-code"></a>サンプル コード

次のコードの例は､**HardwareStationDeviceActionRequest** オブジェクトを作成します。

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("Export attribute in Hardware station controller class",
        "extension method name in Hardware station", "Custom parameters/you can also pass custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="hardwarestationdeviceactionresponse"></a>HardwareStationDeviceActionResponse

次のコード例は、**HardwareStationDeviceActionResponse** の定義を示します。

```TypeScript
class HardwareStationDeviceActionResponse extends Response {
    readonly response: any;
    constructor(response: any);
}
```

次の表では、パラメーターについて説明します。

| パラメーター  | データ型 | 説明 |
|------------|-----------|-------------|
| 応答   | any       | ハードウェア ステーションから POS に送信される要求。 |

## <a name="end-to-end-flow"></a>エンド ツー エンド フロー

次の図は、POS、ハードウェア ステーション、およびハードウェア デバイス間のフローを示しています。

![フロー図。](./media/POSDeviceExtension.png)

## <a name="hardware-station-extension"></a>ハードウェア ステーション拡張機能

新しいハードウェア デバイスを呼び出すには、ハードウェア ステーション コードを実装する必要があります。 そのコードからハードウェア デバイスを呼び出します。

Retail SDK バージョン10.0.11 以降の Hardware station 拡張機能を実装するには、次の手順を実行します。

1. Microsoft .NET Framework バージョン 4.6.1を使用して、新しい C# クラス ライブラリ プロジェクトを作成します。 または、Retail SDK に含まれているサンプルのいずれかをテンプレートとして使用します。 (サンプルは **...\\RetailSDK\\SampleExtensions\\HardwareStation\\** で見つけることができます)。テンプレートとしてサンプルを使用することをお勧めします。
2. 拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** パッケージを追加します。 NuGet パッケージは、**RetailSDK\\pkgs** フォルダで見つけることができます。
3. **IController** インターフェイスを拡張する新しいコントローラ クラスを追加します。
4. コントローラ クラスをクライアントに公開するには、コントローラ クラスに **RoutePrefix** 属性を追加します。

    ```csharp
    [RoutePrefix("ISVEXTENSIONDEVICE")]
    ```

5. ハードウェア デバイスを呼び出すためのカスタム ロジックを実装するために、**HttpPost** 属性を持つメソッドをコントローラー クラスに追加します。 このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。 拡張機能メソッドから、この拡張機能では、印刷やキャッシュ ドロワー要求などの他の要求を呼び出すことができます。 Retail SDK から関連する NuGet パッケージのみを含めます。

    ```C#
    [HttpPost]
    public async Task<bool> IsReady(IEndpointContext context)
    {
    }
    ```

6. プロジェクトを構築します。

Retail SDK バージョン10.0.11 の Hardware station 拡張機能を実装するには、次の手順を実行します。

1. 新しい C# クラス ライブラリ プロジェクトの作成
2. **HardwareStationController** と **IHardwareStationController** を拡張する新しいコントローラー クラスを追加します。
3. コントローラー クラスに **エクスポート** 属性を追加します。 **エクスポート** 属性は、すべて大文字で指定する必要があり、値をパラメーターとして POS 拡張機能から渡す必要があります。 POS **HardwareStationDeviceActionRequest** から渡されるデバイス パラメータは、この値と一致している必要があります。
4. ハードウェア デバイスを呼び出すためのカスタム ロジックを実装するために、メソッドをコントローラ クラスに追加します。 このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。
5. プロジェクトを構築します。

Modern POS にハードウェア ステーション拡張機能を配置し、ローカル ハードウェア ステーションを使用してテストするには、次の手順を実行します。

1. 出力ライブラリを **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにコピーします。
2. **HardwareStation.Extension.config** ファイルを開きます。
3. **合成** セクションで、拡張機能ライブラリの詳細を追加します。

    ```Xml
    <add source="assembly" value="your extension library name" />
    ```
 
4. ファイル保存します。
5. 現在実行中の場合は、Modern POS を閉じます。
6. タスク マネージャーを開いて、**dllhost.exe** タスクを終了します。
7. Modern POS を開いて、ローカル ハードウェア ステーションを使用するように構成します。
8. シナリオを検証します。

Cloud POS を使用してテストするには、ハードウェア ステーション拡張機能のダイナミクス リンク ライブラリ (DLL) を、共有ハードウェア ステーションの **ext** フォルダに配置します。 次に、共有ハードウェア ステーション フォルダのカスタム ライブラリを使用して、**HardwareStation.Extension.config** ファイルを更新します。

## <a name="retail-sdk-samples"></a>Retail SDK サンプル

Retail SDK には、参照用に使用できるサンプルがいくつか含まれています。

+ **POS:** \\RetailSDK\\POS\\Extensions\\FiscalRegisterSample
+ **ハードウェア ステーション:** \\RetailSDK\\SampleExtensions\\HardwareStation\\Extension.FiscalRegisterSample

## <a name="sample-code-for-retail-sdk-version-10011-or-later"></a>Retail SDK バージョン 10.0.11 以降のサンプル コード

```csharp
namespace Contoso
{
    namespace Commerce.HardwareStation.ISVExtensionDevice
    {
        using Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts;
        using System;
        using System.Threading.Tasks;

        /// <summary>;
        /// Sample hardware station extension
        /// </summary>

        [RoutePrefix("ISVEXTENSIONDEVICE")]
        public class ISVExtensionDeviceController : IController
        {
            /// <summary>
            /// Sample.
            /// </summary>

            /// <param name="request">Custom request.<param>
            /// <returns>Result of Custom response.</returns>

            [HttpPost]
            public async Task<CustomResponse> Sample(CustomRequest request, IEndpointContext context)
            {
                CustomResponse response;
                try
                {
                    response = new CustomResponse();
                }
                catch (Exception ex)
                {
                    throw ex;
                }
                return await Task.FromResult(response);
            }
        }
        public class CustomResponse
        {
            public string sampleProp { get; set; }
            public CustomResponse()
            {
                this.sampleProp = "sampleValue";
            }
        }
    }
}
```

## <a name="sample-code-for-retail-sdk-versions-before-version-10011"></a>Retail SDK バージョン 10.0.11 以前のサンプル コード

```csharp
namespace Contoso
{
    namespace Commerce.HardwareStation.ISVExtensionDevice
    {
        using System;
        using System.Composition;
        using System.Web.Http;
        using Microsoft.Dynamics.Commerce.HardwareStation;

        /// <summary>;
        /// Fiscal register peripheral web API controller class.
        /// </summary>

        [Export("ISVEXTENSIONDEVICE", typeof(IHardwareStationController))]
        [Authorize]
        public class ISVExtensionDeviceController : HardwareStationController, IHardwareStationController
        {
            /// <summary>
            /// Sample.
            /// </summary>
            /// <param name="request">Custom request.<param>
            /// <returns>Result of Custom response.</returns>

            [HttpPost]
            public CustomResponse Sample(CustomRequest request)
            {
                ThrowIf.Null(request, "request");
                try
                {
                    return null;
                }
                catch (Exception ex)
                {
                    throw ex;
                }
            }
        }
    }
}
```

## <a name="sample-pos-code-to-call-the-hardware-station-extension"></a>ハードウェア ステーション拡張機能を呼び出すためのサンプル POS コード

POS 拡張機能から、次のパターンを使用してハードウェア ステーションを呼び出します。

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("ISVEXTENSIONDEVICE",
        "Sample", "Custom parameters or custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="generate-an-extension-installer-for-the-shared-hardware-station-for-application-release-10018-or-later"></a>アプリケーション リリース 10.0.18 以降で使用する共有ハードウェア ステーションの拡張機能インストーラーの生成

Dynamics 365 Commerce 10.0.18 以降では、シールド インストーラーがサポートされます。 拡張機能インストーラーは基本インストーラーとは別に生成できます。また、インストーラーは個別にインストールしてサービスを提供できます。 この機能は[シールド セルフサービス インストーラー](enhanced-mass-deployment.md)を使用している場合にのみ機能します。

共有ハードウェア ステーションのシールド拡張機能インストーラーを生成するには、次の手順に従います。

1. GitHub から [サンプル ハードウェア ステーション インストーラー プロジェクト](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.31/src/HardwareStationSample/HardwareStation.Installer)をダウンロードして、Visual Studio で **HardwareStation.Installer.csproj** プロジェクトを開きます。
2. ハードウェア ステーション拡張機能プロジェクトを、プロジェクト参照として **HardwareStation.Installer.csproj** インストーラー プロジェクトに追加します。 既存のサンプルのプロジェクト参照を **HardwareStation.Installer.csproj** プロジェクトから削除します。

    インストーラー プロジェクトは、**Microsoft.Dynamics.Commerce.Sdk.Installers.HardwareStation** パッケージを使用して拡張機能インストーラーを生成します。 サンプル インストーラー プロジェクト クラスでは **ExtensionPackageInstallerSetup** クラスが拡張され、インストール手順が実装されます。

3. インストーラー名を更新するには、サンプル コードの **InstallerName** 変数を設定します。
4. サンプル インストーラー プロジェクトを更新して、インストール中に追加のロジックを実行できます。 たとえば、サーバーに対して ping を実行できます。 ロジックを追加するには、**HardwareStation.Installer.csproj** の **HardwareStationExtensionPackageInstallerSetup.cs** ファイルを使用します。
5. **IExtensionInstallerStep** インターフェイスを実装すると、インストーラーに前後の手順を追加することもできます。 **TestExtensionInstallerPreInstallStep.cs** ファイル、および **HardwareStation.Installer.csproj** サンプル インストーラー プロジェクトの **TestExtensionInstallerPostInstallStep.cs** を使用して、ステップを追加します。
6. 拡張機能 **HardwareStation.Installer.csproj** プロジェクトを構築して、共有ハードウェア ステーション拡張機能インストーラーを生成します。 プロジェクトの出力は、拡張機能インストーラーです。 ビルドの完了後、生成された拡張機能インストーラーのパスが Visual Studio 出力ウィンドウに表示されます。
7. 販売時点管理 (POS) 用の共有ハードウェア ステーション拡張機能を配置し、シナリオでテストします。

    > [!NOTE]
    > 拡張機能インストーラーを実行する前に、シールド共有ハードウェア サーバー インストーラーをインストールする必要があります。

8. コマンド プロンプトを使用して生成された拡張機能インストーラーを実行します。 管理者モードでコマンド プロンプトを開き、**install** パラメーターを指定してインストーラーを実行します。 アンインストールするには、**uninstall** パラメーターを使用して拡張機能インストーラーを実行します。 例:

    ```dos
    C:\HardwareStation.Installer\bin\Debug\net461> .\HardwareStation.Installer.exe install
    ```

9. 現在実行中の場合は、POS を閉じます。
10. POS を開いて、共有ハードウェア ステーションを使用するように構成します。
11. 拡張機能ハードウェア ステーションのシナリオを検証します。

## <a name="generate-an-extension-installer-for-the-shared-hardware-station-for-dynamics-365-commerce-10017-or-earlier"></a>Dynamics 365 Commerce 10.0.17 またはそれ以前で使用する共有ハードウェア ステーションの拡張機能インストーラーの生成

Dynamics 365 Commerce 10.0.17 またはそれ以前の共有ハードウェア ステーションに拡張機能インストーラーを生成するには、[配置可能パッケージの作成](retail-sdk/retail-sdk-packaging.md)の手順に従います。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
