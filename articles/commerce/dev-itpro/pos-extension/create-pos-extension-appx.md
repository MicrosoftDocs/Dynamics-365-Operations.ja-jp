---
title: Modern POS 拡張パッケージ appx ファイルの作成
description: このトピックでは、Visual Studio 2017 を使用した Modern POS のパッケージ プロジェクトの作成方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 68f77ab9a2c821828e3ec397b84da98aeb0bc104
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960155"
---
# <a name="create-a-modern-pos-extension-package-appx-file"></a>Modern POS 拡張パッケージ appx ファイルの作成

[!include [banner](../../includes/banner.md)]

次の手順では、Visual Studio 2017 を使用して Modern POS のパッケージ プロジェクトを作成する方法を示します。 これらの手順は、Modern POS の拡張機能を開発する場合にのみ必要です。 Modern POS 拡張機能パッケージ プロジェクトは、Modern POS アプリを拡張する[MSIX Windows アプリ パッケージ](https://docs.microsoft.com/windows/msix/overview) を生成します。

1. 次の手順に従って、新しい JavaScript Universal Windows Platform アプリ プロジェクトを作成します。

    1. ソリューション エクスプローラーで、ソリューションを右クリックし、**追加** を選択してから **新しいプロジェクト** を選択します。 **Windows JavaScript** を検索し、**空白のアプリ (Universal Windows)** を選択します。 プロジェクトに **ModernPos** と名前を付けます。
    2. **ターゲット バージョン** を **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。
    3. **最小 バージョン** を **Windows 10、バージョン 1809 (10.0; ビルド 17763)** に設定します。

2. 生成されたソース フォルダーおよびファイルを削除します。

    + **js** フォルダー。
    + **css** フォルダー。
    + **index.html** ファイル。
    + **package.appxmanifest** ファイル。

    > [!NOTE]
    > 交換するロゴが含まれる場合に限り、アプリ パッケージのロゴとして使用する画像ファイル (**images\\StoreLogo.png**) は削除しないでください。

3. プロジェクトを編集し、上記の手順で作成したカスタマイズ パッケージ **props** ファイルをインポートします。

    > [!NOTE]
    > **package.appxmanifest** ファイルの生成は、カスタマイズ パッケージ **props** ファイルのプロパティによって異なります。 プロジェクトにインポートする必要があります。**

4. POS SDK NuGet パッケージへの参照を追加します。

    1. プロジェクト ソリューション エクスプローラーを選択し、**NuGet パッケージの管理** を選択します。
    2. NuGet パッケージ マネージャー ウィンドウで **参照** を選択します。
    3. **Microsoft.Dynamics.Commerce.Sdk.Pos** を検索します。
    4. パッケージを選択し、**インストール** を選択します。

5. **x86** のみを対象とするようにソリューション コンフィギュレーションを更新します。

    1. プロジェクト ソリューション エクスプローラーを選択し、**プロパティ** を選択します。
    2. 構成マネージャーを開きます。
    3. **有効なソリューション プラットフォーム** ドロップダウンで、**編集** を選択します。
    4. **x86** を除く他のすべてのプラットフォームを削除します。

         ![プラットフォーム コンフィギュレーション](media/platform.png)

6. サポートされていないプラットフォーム コンフィギュレーションを削除するには、**jsproj** ファイルを編集してください。

    1. プロジェクト ファイルを保存します。
    2. ソリューション エクスプローラを使用してプロジェクトをアンロードします。
    3. ソリューション エクスプローラーでプロジェクトを選択し、**編集** を選択します。
    4. **x86** 以外のすべてのプラットフォームが含まれる **ProjectConfiguration** を削除します。 **ProjectConfigurations** は次の Xml のようになります。

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

7. 次の手順に従って、Modern POS **jsproj** から上記で作成した **POS.Extension パッケージ** プロジェクトへの参照を追加します。

    1. ソリューション エクスプローラーで、Modern POS プロジェクトを右クリックし、**追加** を選択してから、**参照** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. 上記で **作成した POS 拡張機能パッケージ** プロジェクトを選択します。 プロジェクトを選択すると、Visual Studio はサポートされていない参照を確認するように求めます。 **はい** を選択します。

8. ソリューションに Commerce Runtime 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Commerce Runtime 拡張機能プロジェクトをプロジェクト参照に追加します。

    1. ソリューション エクスプローラーで、Modern POS を右クリックします。 **追加** を選択してから **参照** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. Commerce Runtime 拡張機能プロジェクトを選択します。

9. ソリューションに Hardware Station 拡張機能プロジェクトが含まれている場合は、ソリューションで各 Hardware Station 拡張機能プロジェクトをプロジェクト参照に追加します。

    1. ソリューション エクスプローラーで、Modern POS を右クリックします。 **追加** を選択してから **参照** を選択します。
    2. 参照マネージャの左側にある **プロジェクト** タブを選択します。
    3. Hardware Station の拡張機能プロジェクトを選択します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
