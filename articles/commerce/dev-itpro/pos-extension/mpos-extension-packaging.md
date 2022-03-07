---
title: Modern POS 拡張機能パッケージの作成
description: このトピックでは、Modern POS 拡張機能パッケージの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: f93b17a530dae3ea8a9f2feb2ea1c4ce9ad76ef2a31d0830c798c68a9cbfd17a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741800"
---
# <a name="create-a-modern-pos-extension-package"></a>Modern POS 拡張機能パッケージの作成

[!include [banner](../../../includes/banner.md)]

Modern POS 拡張機能用の拡張機能インストーラーを作成するには、次の手順に従います。

1. Visual Studio 2017 で新しいコンソール アプリケーション (.NET Core) を作成し、**ModernPos.Installer** と名前を付けます。
2. .proj ファイルを編集し、次の XML に示すようにターゲット フレームワークを .NET Framework バージョン 4.6.1 に変更します。

    ```Javascript
    <Project Sdk="Microsoft.NET.Sdk">
        <PropertyGroup>
            <OutputType>Exe</OutputType>
            <TargetFramework>net461</TargetFramework>
        </PropertyGroup>
    </Project>
    ```

3. 生成された **Program.cs** ファイルは削除します。
4. **Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos** NuGet パッケージへの参照を追加します。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。
    2. **NuGet パッケージ マネージャー** ウィンドウの **参照** タブで、**Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos** を検索します。
    3. パッケージを選択し、**インストール** を選択します。
    4. Go-Live バージョンと一致するバージョンを選択します。

5. Modern POS プロジェクトから、既に作成した **ModernPos.Installer** プロジェクトへの参照を追加します。

    1. ソリューション エクスプローラーで、Modern POS を選択したまま (または右クリック) にして、**参照&gt;追加** を選択します。
    2. 参照マネージャーの左側の **プロジェクト** タブで、以前作成した **ModernPos.Installer** プロジェクトを選択します。

6. **オフライン チャネル データベースの拡張スクリプト プロジェクトのみ:** Modern POS プロジェクトからの参照をチャネル データベース プロジェクトに追加します。

    1. ソリューション エクスプローラーで、Modern POS を選択したまま (または右クリック) にして、**参照&gt;追加** を選択します。
    2. 参照マネージャーの左側の **プロジェクト** タブで、以前作成したチャネル データベース拡張プロジェクトを選択します。

7. プロジェクトをコンパイル、およびビルドします。 このプロジェクトの出力に、Modern POS 拡張機能インストーラーが含まれています。
8. 拡張機能を手動でインストールするには、管理者モードで Windows PowerShell を開き、拡張機能インストーラーのフォルダーに移動し、**インストール** コマンドを実行します。

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ModernPos.Installer.exe install
    ```

    **アンインストール** コマンドを実行して拡張機能をアンインストールします。

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ModernPos.Installer.exe uninstall
    ```

    > [!NOTE]
    > 拡張機能インストーラーをインストールする前に、シールドされた Modern POS をインストールします。

9. 拡張機能をインストールした後、実行されている場合は Modern POS を閉じます。 **Modern POS のインストール/更新** のデスクトップ アイコンを使用して、Modern POS を起動し、拡張機能を読み込みます。 拡張機能の .appx ファイルがインストールされます。 前の手順で .appx ファイルと他のファイルを正しい場所にコピーします。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
