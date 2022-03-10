---
title: Cloud POS 拡張機能パッケージの作成
description: このトピックでは、Cloud POS 拡張機能パッケージの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: cb79b1270fd6d941897423d7c3f813e237097504
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781807"
---
# <a name="create-a-cloud-pos-extension-package"></a>Cloud POS 拡張機能パッケージの作成

[!include [banner](../../../includes/banner.md)]

このトピックでは、Cloud POS 拡張機能パッケージの作成方法について説明します。 Cloud POS 配置トポロジに基づいて、Cloud POS を Cloud スケール ユニット (CSU) または CSU – セルフ ホストに配置できます。

## <a name="packaging-for-csu-cloud-pos"></a>CSU Cloud POS のパッケージ

CSU の配置パッケージは、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを消費することで作成できます。

パッケージを作成するには、これらの手順に従います。

1. Microsoft Visual Studio 2017 では、**ターゲット フレームワーク** プロパティが **.NET Standard 2.0** に設定されている新しい C\# クラス ライブラリ プロジェクトを作成します。 プロジェクト名を **ScaleUnit** に変更します。
2. 生成された **Class1.cs** ファイルは削除します。
3. **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet パッケージを依存関係としてプロジェクトに追加します。
4. **Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** NuGet パッケージを選択し、使用している SDK/アプリケーションのバージョンに一致させます。 `https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/nuget/v3/index.json` から、**Microsoft.Dynamics.Commerce.Sdk.ScaleUnit** パッケージを使用します。 パッケージのソースの場所を拡張機能プロジェクト ファイルの **nuget.config** ファイルに追加できます。
5. プロジェクト参照として、**POS.Extension** プロジェクトを **ScaleUnit** プロジェクトに追加します。
6. プロジェクトをコンパイル、およびビルドします。 プロジェクトの出力には、CSU 配置パッケージが zip ファイルとして含まれています。

> [!NOTE]
> Commerce Runtime (CRT) または Retail Server 拡張子、またはデータベース 拡張がある場合、すべての拡張子プロジェクトを参照として **ScaleUnit** プロジェクトに追加する必要があります。 すべての拡張子を含む複合配置パッケージが生成されます。

このパッケージを配置するには、[パッケージを CSU に配置](../retail-sdk/retail-sdk-packaging.md#deploy-the-package-to-csu) の手順に従います。

## <a name="packaging-for-csu--self-hosted-cloud-pos"></a>CSU パッケージ – セルフ ホステッド Cloud POS

CSU の配置パッケージは、**Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** パッケージを消費することで作成できます。

1. Visual Studio 2017 で、新しいコンソール アプリケーション (.NET Core) を作成し、**ScaleUnit.Installer** と名前を付けます。
2. .proj ファイルを編集し、次の XML に示すようにターゲット フレームワークを Microsoft .NET Framework バージョン 4.6.1 に変更します。

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">
        <PropertyGroup>
            <OutputType>Exe</OutputType>
            <TargetFramework>net461</TargetFramework>
        </PropertyGroup>
    </Project>
    ```

3. 生成された **Program.cs** ファイルは削除します。
4. Installer SDK NuGet パッケージへの参照を追加。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。
    2. **NuGet パッケージ マネージャー** ウィンドウの **参照** タブで、**Microsoft.Dynamics.Commerce.Sdk.Installers.ScaleUnit** を検索します。
    3. パッケージを選択し、**インストール** を選択します。
    4. Go-Live バージョンと一致するバージョンを選択します。

5. **ScaleUnit.Installer** プロジェクトから、以前作成した **POS.Extension** プロジェクトへ参照を追加します。

    1. ソリューション エクスプローラーで、**ScaleUnit.Installer** プロジェクトを保留し (または右クリック)、**追加** を選び、**参照** を選択します。
    2. 参照マネージャーの左側の **プロジェクト** タブで、以前作成した **POS.Extension** プロジェクトを選択します。

6. **Extension.Config** ファイルをプロジェクトに追加します。

    1. プロジェクトを選択および保留し (または右クリック)、**追加** から **新しい項目** を選択します。
    2. **アプリケーション構成ファイル** を選択します。
    3. **Extension.Config** のファイル名を作成し、追加します。

7. 次の XML で示すように、CRT 拡張子で **Extension.Config** ファイルを更新します。 CRT 拡張機能が無い場合は、**合成** セクションを空白のままにします。

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <commerceRuntimeExtensions>
        <composition>
            <add source="assembly" value="CommerceRuntime" />
        </composition>
    ```

8. プロジェクトをコンパイル、およびビルドします。 このプロジェクトの出力に、**ScaleUnit** インストーラーの .exe ファイルが含まれています。
9. 拡張機能を手動でインストールするには、管理者モードで Windows PowerShell を開き、拡張機能インストーラーのフォルダーに移動し、**インストール** コマンドを実行します。

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ScaleUnit.Installer.exe install
    ```

    拡張子をアンインストールし、次のコマンドを実行します。

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ScaleUnit.Installer.exe
    ```

    > [!NOTE]
    > 拡張機能インストーラーをインストールする前に、シールドされた **ScaleUnit** パッケージを最初にインストールします。 CRT または Retail Server 拡張子、またはデータベース 拡張子がある場合、すべての拡張子プロジェクトを参照として **ScaleUnit.Installer** プロジェクトに追加する必要があります。 すべての拡張子を含む複合配置パッケージが生成されます。
    >
    > 拡張機能に基づいて、複数のスケール ユニット インストーラーを作成し、それらを個別に管理することもできます。 拡張機能をすべてパッケージで結合する必要はありません。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
