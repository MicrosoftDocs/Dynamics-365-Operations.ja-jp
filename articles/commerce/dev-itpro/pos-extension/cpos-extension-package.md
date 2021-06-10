---
title: Cloud POS 拡張機能パッケージの作成
description: このトピックでは、Cloud POS 拡張機能パッケージの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 66b567b98cda98e44646af95b946a03b39a1ff0e
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093902"
---
# <a name="create-a-cloud-pos-extension-package"></a>Cloud POS 拡張機能パッケージの作成

[!include [banner](../../../includes/banner.md)]

このトピックでは、Cloud POS 拡張機能パッケージの作成方法について説明します。 Cloud POS 配置トポロジに基づいて、Cloud POS を Cloud スケール ユニット (CSU) または Cloud スケール ユニット (CSU) – セルフ ホストに配置できます。

## <a name="packaging-for-cloud-scale-unit-csu-cpos"></a>Cloud スケール ユニット (CSU) CPOS のパッケージング

CSU の配置パッケージは、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを消費することで作成できます。

パッケージを作成するには、これらの手順に従います。

1. Visual Studio 2017 を開き、**ターゲット フレームワーク** で **.NET Standard 2.0** を設定して新しい C\# クラス ライブラリー プロジェクトを作成し、プロジェクト名を **ScaleUnit** に変更します。

2. 生成された **クラス 1.cs** ファイルは削除します。

3. 依存関係として **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet パッケージをプロジェクトに追加します。

4. **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet バージョンを選択し、使用している SDK/アプリケーションのバージョンに一致させます。 `https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json` から、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを使用します。 パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加できます。

5. プロジェクト参照として、**POS.Extension** プロジェクトを **ScaleUnit** プロジェクトに追加します。

6. プロジェクトをコンパイル、およびビルドします。 このプロジェクトの出力には、CSU 配置パッケージが zip ファイルとして含まれています。

> [!NOTE]
> Commerce Runtime、Retail Server、またはデーターベース拡張機能がある場合は、すべての拡張機能のプロジェクトを参照として **ScaleUnit** プロジェクトに含みます。 これらのパッケージを追加すると、すべての拡張機能を含む複合配置パッケージが生成されます。

配置するには、[パッケージを CSU に配置](../retail-sdk/retail-sdk-packaging.md#deploy-the-package-to-csu) の手順に従います。

## <a name="packaging-for-cloud-scale-unit--self-hosted-cpos"></a>Cloud スケール ユニット – セルフ ホスト CPOS のパッケージング

CSU の配置パッケージは、**Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** パッケージを消費することで作成できます。

1. Visual Studio 2017 を開いて新しいコンソール アプリケーション (.NET Core) を作成し、**ScaleUnit.Installer** と名前を付けます。

2. .proj ファイルを編集し、**ターゲット フレームワーク** を **.NET Framework 4.6.1** へ変更します。 Xml は次のようになります。

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
        <PropertyGroup>
            <OutputType>Exe</OutputType>
            <TargetFramework>net461</TargetFramework>
        </PropertyGroup>
    </Project>
    ```

3. 生成された **Program.cs** ファイルは削除します。

4. Installer SDK NuGet パッケージへの参照を追加

    1. ソリューション エクスプローラーのプロジェクトを選択し、**NuGet パッケージの管理** を選択します。
    2. NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。
    3. **Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** を検索します。
    4. パッケージを選択し、**インストール** を選択します。
    5. Go-Live バージョンと一致するバージョンを選択します。

5. 上記のとおりに作成した POS.Extension プロジェクトへ、**ScaleUnit.Installer** プロジェクトから参照を追加します。

    1. Solution Explorer で **ScaleUnit.Installer** プロジェクトを右クリックして、**追加** から **参照** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. 上記で作成した POS.Extension プロジェクトを選択します。

6. **Extension.Config** ファイルをプロジェクトに追加します。

    1. プロジェクトを右クリックし、**追加** から **新しい項目** を選択します。
    2. **アプリケーション構成ファイル** を選択します。
    3. **Extension.Config** 名のファイルを作成し、追加します。

7. **Extension.Config** ファイルを Commerce Runtime 拡張機能で更新します。 Commerce Runtime 拡張機能が無い場合は、**合成** セクションを空白のままにします。 Xml は次のようになります。

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <add source="assembly" value="CommerceRuntime" />
          </composition>
    ```

8. プロジェクトをコンパイル、およびビルドします。 このプロジェクトの出力に、**ScaleUnit** インストーラー .exe ファイルが含まれています。

9. 拡張機能を手動でインストールするには、管理者モードで PowerShell を開き、拡張機能インストーラーのフォルダーに移動します。 install コマンドを実行して拡張機能をインストールします。

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ScaleUnit.Installer.exe install    
    ```

    拡張機能をアンインストールするには:

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ScaleUnit.Installer.exe uninstall
    ```

    > [!NOTE]
    > 拡張機能インストーラーをインストールする前に、シールドされた **ScaleUnit** パッケージを最初にインストールします。 Commerce Runtime、Retail Server、またはデーターベース拡張機能がある場合は、すべての拡張機能のプロジェクトを参照として **ScaleUnit.Installer** プロジェクトに含みます。 プロジェクトを追加すると、すべての拡張機能を含む複合配置パッケージが生成されます。
    > 拡張機能によって複数のスケール ユニット インストーラーを作成し、それらを個別に管理することもできます。 拡張機能をすべてパッケージで結合する必要はありません。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
