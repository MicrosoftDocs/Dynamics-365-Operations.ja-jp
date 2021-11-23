---
title: Modern POS 拡張パッケージの .appx ファイルの作成
description: このトピックでは、Microsoft Visual Studio 2017 を使用して、Modern 販売時点管理 (MPOS) のパッケージ プロジェクトの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: fd6b1b28fa590a95bf64df5b13c86f03222da616
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783332"
---
# <a name="create-an-appx-file-for-a-modern-pos-extension-package"></a>Modern POS 拡張パッケージの .appx ファイルの作成

[!include [banner](../../includes/banner.md)]

このトピックでは、 Visual Studio 2017 を使用して、Modern 販売時点管理 (MPOS) のパッケージ プロジェクトの作成方法について説明します。 これらの手順は、MPOS の拡張機能を開発する場合にのみ必要です。 MPOS 拡張機能パッケージ プロジェクトは、MPOS アプリを拡張する[MSIX Windows アプリ パッケージ](/windows/msix/overview) を生成します。

1. 新しい JavaScript Universal Windows Platform (UWP) アプリ プロジェクトを作成します。

    1. ソリューション エクスプローラーで、ソリューションを保留 (または右クリック)し、**追加** から **新しいプロジェクト** を選択します。
    2. **Windows JavaScript** を検索し、**空白のアプリ (Universal Windows)** を選択します。
    3. プロジェクトに **ModernPos** と名前を付けます。
    4. **ターゲット バージョン** フィールドを **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。
    5. **ミニマム バージョン** フィールドを **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。

2. 生成される次のソース フォルダおよびファイルを削除します。

    + **js** フォルダー
    + **css** フォルダー
    + **index.html** ファイル
    + **package.appxmanifest** ファイル

    > [!NOTE]
    > 交換するロゴが含まれる場合に限り、アプリ パッケージのロゴとして使用する画像ファイル (**images\\StoreLogo.png**) は削除しないでください。

3. プロジェクトを編集し、カスタマイズ パッケージ用に作成されたプロパティ (.props) ファイルをインポートします。

    > [!NOTE]
    > **package.appxmanifest** ファイルの世代は、カスタマイズ パッケージの .props ファイルによって異なります。 .props ファイルをプロジェクトにインポートすることを確認してください。

4. POS SDK NuGet パッケージへの参照を追加します。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**NuGet パッケージの管理** を選択します。
    2. **NuGet パッケージ マネージャー** ウィンドウの **閲覧** タブで、**Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。
    3. パッケージを選択し、**インストール** を選択します。

5. ソリューション コンフィギュレーションを更新して、x86 プラットフォームのみをターゲットとします。

    1. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**プロパティ** を選択します。
    2. 構成マネージャーを開きます。
    3. **有効なソリューション プラットフォーム** メニューで、**編集** を選択します。
    4. **x86** を除くすべてのプラットフォームを削除します。

    ![プラットフォーム コンフィギュレーション。](media/platform.png)

6. サポートされていないプラットフォーム コンフィギュレーションを削除するには、JavaScript プロジェクト ファイル (.jsproj ファイル) を編集してください。

    1. プロジェクト ファイルを保存します。
    2. ソリューション エクスプローラを使用してプロジェクトをアンロードします。
    3. ソリューション エクスプローラーで、プロジェクトを保留 (または右クリック) し、**編集** を選択します。
    4. **x86** を除くすべてのプラットフォームが含まれる **ProjectConfiguration** を削除します。 完了すると、**ProjectConfiguration** エレメントは次の例のようになります。

        ```xml
        <ItemGroup Label="ProjectConfigurations">
            <ProjectConfiguration Include="Debug|x86">
                <Configuration>Debug</Configuration>
                <Platform>x86</Platform>
            </ProjectConfiguration>
            <ProjectConfiguration Include="Release|x86">
                <Configuration>Release</Configuration>
                <Platform>x86</Platform>
                <UseDotNetNativeToolchain>true</UseDotNetNativeToolchain>
            </ProjectConfiguration>
        </ItemGroup>
        ```

    5. プロジェクトをリロードします。

7. 参照を MPOS .jsproj ファイルから以前作成した **POS. 拡張機能パッケージ** プロジェクトに追加します。

    1. ソリューション エクスプローラーで、MPOS プロジェクトを保留 (または右クリック)し、**追加** から **参照** を選択します。
    2. 照会マネージャーの左側の **プロジェクト** タブで、以前作成した **POS 拡張機能パッケージ** プロジェクトを選択します。
    3. サポートされていない参照を確認するメッセージが表示されたら、**はい** を選択します。

8. ソリューションに Commerce Runtime (CRT) 拡張機能プロジェクトが含まれている場合、プロジェクト参照をソリューションの各 CRT 拡張機能プロジェクトに追加します。

    1. ソリューション エクスプローラーで、MPOS プロジェクトを保留 (または右クリック)し、**追加** から **参照** を選択します。
    2. 参照マネージャーの左側の **プロジェクト** タブで、CRT 拡張機能プロジェクトを選択します。

9. ソリューションに Hardware Station 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Hardware Station 拡張機能プロジェクトにプロジェクト参照を追加します。

    1. ソリューション エクスプローラーで、MPOS プロジェクトを保留 (または右クリック)し、**追加** から **参照** を選択します。
    2. 参照マネージャーの左側の **プロジェクト** タブで、Hardware Station 拡張機能プロジェクトを選択します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
