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
ms.openlocfilehash: c28e23f973dc275cf2f13f12ee210dff1af2f6ac
ms.sourcegitcommit: 4c880b152e81350f023b944c2ab13e60498e2c7b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/25/2021
ms.locfileid: "6093894"
---
# <a name="create-a-modern-pos-extension-package"></a>Modern POS 拡張機能パッケージの作成

[!include [banner](../../../includes/banner.md)]

Modern POS 拡張機能用の拡張機能インストーラーを作成するには、次の手順に従います。

1. Visual studio 2017 を開いて新しいコンソール アプリケーション (.NET Core) を作成し、**ModernPos.Installer** と名前を付けます。

2. **.proj** ファイルを編集し、**ターゲット フレームワーク** を **.NET Framework 4.6.1** に変更します。 XML はここに表示されます。

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

    1. ソリューション エクスプローラーのプロジェクトを選択し、**NuGet パッケージの管理** を選択します。
    2. NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。
    3. **Microsoft.Dynamics.Commerce.Sdk.Installers.ModernPos** を検索します。
    4. パッケージを選択し、**インストール** を選択します。
    5. Go-Live バージョンと一致するバージョンを選択します。

5. 上記のとおりに作成した **ModernPos.Installer** プロジェクトへ Modern POS プロジェクト からの参照を追加します。

    1. ソリューション エクスプローラーで、Modern POS プロジェクトを右クリックし、**追加 -&gt; 参照** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. 上記の通りに作成した **ModernPos.Installer** プロジェクトを選択します。

6. \[オフライン チャンネル データベースの拡張スクリプト プロジェクトのみ\]: Modern POS プロジェクトからの参照をチャンネル データベース プロジェクトに追加します。

    1. ソリューション エクスプローラーで、Modern POS プロジェクトを右クリックし、**追加 -&gt; 参照** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. 上記のとおりに作成したチャネル データベース拡張機能プロジェクトを選択します。

7. プロジェクトをコンパイル、およびビルドします。 このプロジェクトの出力に、Modern POS 拡張機能インストーラーが含まれています。

8. 拡張機能を手動でインストールするには、管理者モードで PowerShell を開き、拡張機能インストーラーのフォルダーに移動します。 install コマンドを実行して拡張機能をインストールします。

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ModernPos.Installer.exe install
    ```

    拡張機能をアンインストールするには:

    ```powershell
    PS C:\ModernPos.Installer\bin\Debug\net461> .\ModernPos.Installer.exe uninstall
    ```

    > [!NOTE]
    > 拡張機能インストーラーをインストールする前に、シールドされた Modern POS を最初にインストールします。

9. 拡張機能をインストールした後、実行されている場合は Modern POS を閉じます。 **Modern POS のインストール/更新** のデスクトップ ショートカットから Modern POS Modern POS を起動し、拡張機能を読み込みます。 拡張子が .appx のファイルは、デスクトップ アイコンをクリックした後にインストールされます。 前の手順で .appx とファイルを正しい場所にコピーします。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
