---
title: Store Commerce 拡張機能インストーラー パッケージの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce Store Commerce 拡張機能インストーラー パッケージを作成する方法について説明します。
author: mugunthanm
ms.date: 04/21/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 03-30-2022
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 311c87560d522223e430af9c01f359399b557fa7
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629724"
---
# <a name="create-a-store-commerce-extension-installer-package"></a>Store Commerce 拡張機能インストーラー パッケージの作成

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce Store Commerce 拡張機能インストーラー パッケージを作成する方法について説明します。

> [!NOTE]
> 完全なコード サンプルは、[Store Commerce 拡張機能サンプルの GitHub リポジトリ (リポジトリ)](https://github.com/microsoft/Dynamics365Commerce.InStore) にあります。

Store Commerce 拡張機能用の拡張機能インストーラーを作成するには、次の手順に従います。

1. Visual Studio 2017 で、**StoreCommerce.ExtInstaller** と名前を付けた新しいコンソール アプリケーション (.NET Core) を作成します。
1. **.proj** ファイルで、次の XML サンプルに示すようにターゲット フレームワークを .NET Framework バージョン 4.6.1 に変更します。

    ```XML
    <Project Sdk="Microsoft.NET.Sdk">
        <PropertyGroup>
            <OutputType>Exe</OutputType>
            <TargetFramework>net461</TargetFramework>
        </PropertyGroup>
    </Project>
    ```

1. 生成された **Program.cs** ファイルは削除します。
1. **Microsoft.Dynamics.Commerce.Sdk.Installers.StoreCommerce** NuGet パッケージへの参照を追加します:

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。
    1. **NuGet パッケージ マネージャー** ウィンドウの **参照** タブで、**Microsoft.Dynamics.Commerce.Sdk.Installers.StoreCommerce** を検索します。
    1. パッケージを選択し、**インストール** を選択します。
    1. Go-Live バージョンと一致するバージョンを選択します。

1. Store Commerce 拡張 .csproj プロジェクト、Commerce runtime (CRT)、およびデータベース スクリプト プロジェクト拡張機能への参照を追加します。

    1. ソリューション エクスプローラーで、プロジェクトを選択したまま (または右クリックして) 、**追加\>参照** を選択します。
    1. 参照マネージャーの左側の **プロジェクト** タブで、以前作成した拡張機能プロジェクトを選択します。

1. プロジェクトをコンパイル、およびビルドします。 このプロジェクトの出力には、Store Commerce 拡張機能インストーラーが含まれています。 **F5** キーを選択してプロジェクトを構築すると、インストーラーは自動的に配置されます。
1. 拡張機能を手動でインストールするには、管理者モードで Windows PowerShell を開き、拡張機能インストーラーのフォルダーに移動し、次の **インストール** コマンドを実行します。

    ```PowerShell
    PS C:\StoreCommerce.ExtInstaller\bin\Debug\net461> .\ StoreCommerce.ExtInstaller.exe install
    ```

    > [!NOTE]
    > 拡張機能インストーラーをインストールする前に、Store Commerce アプリをインストールします。

    **uninstall** コマンドを実行して拡張機能をアンインストールします。

    ```PowerShell
    PS C:\StoreCommerce.ExtInstaller\bin\Debug\net461> .\ StoreCommerce.ExtInstaller.exe uninstall
    ```

1. 拡張機能をインストールした後、実行されている場合は Store Commerce を閉じます。 次に、拡張機能を読み込むには、デスクトップ上の Store Commerce ショートカットを使用して Store Commerce を開きます。

## <a name="sample-code"></a>サンプル コード

```XML
<Project Sdk="Microsoft.NET.Sdk">
    <Import Project="..\CustomizationPackage.props " />
    <PropertyGroup>
        <OutputType>Exe</OutputType>
        <TargetFramework>net461</TargetFramework>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Dynamics.Commerce.Sdk.Installers.StoreCommerce" Version="$(CommerceSdkPackagesVersion)" />
    </ItemGroup>
    <ItemGroup>
        <ProjectReference Include="..\CommerceRuntime\Contoso.GasStationSample.CommerceRuntime.csproj">
            <ReferenceOutputAssembly>false</ReferenceOutputAssembly>
        </ProjectReference>
        <ProjectReference Include="..\Pos\Contoso.GasStationSample.Pos.csproj">
            <ReferenceOutputAssembly>false</ReferenceOutputAssembly>
        </ProjectReference>
    </ItemGroup>
    <ItemGroup>
        <!-- Settings included in the CommerceRuntimeExtensionSettings item group will be added to the generated CommerceRuntime config file and available at runtime in the CommerceRuntime extension. -->
        <CommerceRuntimeExtensionSettings Include="ext.Contoso.GasolineItemId">
            <Value>gasoline</Value>
        </CommerceRuntimeExtensionSettings>
    </ItemGroup>
</Project>
```
