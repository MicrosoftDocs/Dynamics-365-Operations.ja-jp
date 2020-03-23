---
title: POS と新しいハードウェア デバイスの統合
description: このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/03/2019
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
ms.dyn365.ops.version: AX 7.3.0, Retail July 2017 update
ms.openlocfilehash: d9252e4771bd6292407e8f9c2491f4eb3bbe718a
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117255"
---
# <a name="integrate-pos-with-a-new-hardware-device"></a>POS と新しいハードウェア デバイスの統合

[!include [banner](../../includes/banner.md)]

このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。 


POS からハードウェア ステーションを呼び出すには、要求と応答を使用する必要があります。

+ **HardwareStationDeviceActionRequest** - POS からハードウェア ステーションに送信された要求。
+ **HardwareStationDeviceActionResponse** - ハードウェア ステーションから POS に受信した要求。

## <a name="hardwarestationdeviceactionrequest"></a>HardwareStationDeviceActionRequest

**HardwareStationDeviceActionRequest** の定義を次のコード例に示します。

```TypeScript
class HardwareStationDeviceActionRequest<TResponse extends HardwareStationDeviceActionResponse> extends Request<TResponse> {

  readonly device: string;
  readonly action: string;
  readonly actionData: any;
  constructor(device: string, action: string, actionData: any, correlationId?: string);

}
```

次の表で、このパラメーターについて説明します。

| パラメーター | データ型 | 説明                     |
|------------|-----------|---------------------------------|
| デバイス     | 文字列    | ハードウェア ステーションの要求に渡されるデバイス名は、ハードウェア ステーションのデバイス拡張コントローラー クラスに追加された**エクスポート**属性と同じである必要があります。                                          |
| アクション     | 文字列    | ハードウェア ステーション拡張機能で呼び出すメソッド。 メソッド名は文字列値として渡され、コア POS ハードウェア ステーション層は、ハードウェア ステーション拡張コードから対応するメソッドを呼び出します。 このメソッドは、ハードウェア ステーション拡張機能のメソッド名と完全に一致する必要があります。 ハードウェア ステーション拡張機能は、パラメーターとして渡される必要があります。 |
| actionData | any       | 拡張機能に渡すカスタム パラメーター。  |

### <a name="sample-code"></a>サンプル コード

次のコード例では、**HardwareStationDeviceActionRequest** オブジェクトを作成します。

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("Export attribute in Hardware station controller class",
    "extension method name in Hardware station", "Custom parameters/you can also pass custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="hardwarestationdeviceactionresponse"></a>HardwareStationDeviceActionResponse

**HardwareStationDeviceActionResponse** の定義を次のコード例に示します。

```TypeScript
class HardwareStationDeviceActionResponse extends Response {
  readonly response: any;
  constructor(response: any);
}
```
次の表で、このパラメーターについて説明します。

| パラメーター | データ型 | 説明                                       |
|------------|-----------|---------------------------------------------------|
| 応答   | any       | ハードウェア ステーション拡張コードから POS に送信された応答。 |

## <a name="end-to-end-flow"></a>エンド ツー エンド フロー

次の図は、POS、ハードウェア ステーション、ハードウェア デバイスのフローを示しています。

![POS-HWS デバイス シーケンス図](./media/POSDeviceExtension.png)

## <a name="hardware-station-extension"></a>ハードウェア ステーション拡張機能

新しいハードウェア デバイスを呼び出すには、ハードウェア ステーション コードを実装する必要があります。 ハードウェア ステーション コードから、ハードウェア デバイスを呼び出します。

ハードウェア ステーション拡張機能を実装するには、次の手順を実行します。

1.  新しい C# クラス ライブラリ プロジェクトの作成
2.  **HardwareStationController** と **IHardwareStationController** を拡張する新しいコントローラー クラスを追加します。
3.  コントローラー クラスに**エクスポート**属性を追加します。 **エクスポート**属性は、すべて大文字で指定する必要があります。また、この値は POS 拡張機能のパラメーターとして渡す必要があります。 POS **HardwareStationDeviceActionRequest** から渡されたデバイス パラメーターは、この値と一致する必要があります。
4.  このメソッドをコントローラー クラスに追加して、ハードウェア デバイスを呼び出すカスタム ロジックを実装します。 このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。
5.  プロジェクトを構築します。

MPOS にハードウェア ステーション拡張機能を展開し、ローカル ハードウェア ステーションを使用してテストするには、次の操作を行います。

1. 出力ライブラリを **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにコピーします。
2. **HardwareStation.Extension.config** を開きます。
3. 合成セクションに拡張ライブラリの詳細を追加します。

  ```Xml
  <add source="assembly" value="your extension library name" />
  ```
 
4. ファイル保存します。
5. モダン POS を閉じます (実行中の場合)。
6. タスク マネージャーを開いて、**dllhost.exe** タスクを終了します。
7. MPOS を起動して、ローカル ハードウェア ステーションを使用するように構成します。
8. シナリオを検証します。

クラウド POS を使用してテストするには、共有ハードウェア ステーションの **ext** フォルダーにハードウェア ステーション拡張 dll を配置し、共有ハードウェア ステーション フォルダーのカスタム ライブラリを使用して **HardwareStation.Extension.config** ファイルを更新します。

## <a name="retail-sdk-samples"></a>Retail SDK サンプル
次に、参照用の Retail SDK のサンプルをいくつか示します。

+ **POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample
+ **ハードウェア ステーション**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample

## <a name="sample-hardware-station-code"></a>ハードウェア ステーション コードのサンプル

```C#
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

## <a name="sample-pos-code-on-how-to-call-the-above-hardware-station-extension"></a>上記のハードウェア ステーション拡張機能の呼び出し方法に関するサンプル POS コード

POS 拡張機能から、このパターンを使用してハードウェア ステーションを呼び出します。

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("ISVEXTENSIONDEVICE",
     "Sample", "Custom parameters or custom object");
 return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
 ```
