---
title: 展開の Cloud Scale Unit 拡張パッケージのマージ
description: この記事では、展開用 Microsoft Dynamics 365 Commerce Cloud Scale Unit (CSU) の拡張機能パッケージのマージ方法について説明します。
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-03-30
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 0a2d516cd6ff911623272c7a69a470163e45f578
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279623"
---
# <a name="merge-cloud-scale-unit-extension-packages-for-deployment"></a>展開の Cloud Scale Unit 拡張パッケージのマージ

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce Cloud Scale Unit (CSU) の拡張機能パッケージのマージ方法について説明します。

独立系ソフトウェア ベンダー (ISV)、パートナー、および顧客が CSU 用に生成する拡張機能パッケージは、[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) に展開する前に、単一のパッケージにマージする必要があります。 現在、LCS は複数の拡張機能パッケージの展開をサポートしていません。 最後に展開された拡張機能パッケージは、以前の拡張機能の展開を上書きします。

CSU 拡張機能パッケージをマージするための複数のオプションがあります。 この記事では、ISV CSU 拡張機能用 NuGet パッケージを生成してマージするプロセスについて説明します。

> [!NOTE]
> 拡張機能パッケージのマージは、オンプレミスの CSU 展開、Store Commerce、または共有のハードウェア ステーションには必要ありません。 オンプレミス コンポーネントは、複数の拡張配置をサポートします。

## <a name="scenario"></a>シナリオ

税 ISV と支払 ISV の両方から CSU 拡張機能パッケージが提供され、独自の拡張機能パッケージを所有しているので、すべてのパッケージを展開する必要があります。 LCS は複数のパッケージの展開をサポートしていないので、すべてのパッケージを 1 つのパッケージにマージする必要があります。

### <a name="merge-the-packages-by-generating-a-nuget-package-for-the-isv-extensions"></a>ISV 拡張機能の NuGet パッケージを生成してパッケージをマージする

ISV 拡張機能の NuGet パッケージを生成してパッケージをマージするには、以下の手順を実行します。

1. ISV に CSU 拡張機能の NuGet パッケージを生成するように求めます。
1. プロジェクトへの参照として追加することにより、CSU パッケージング プロジェクトで ISV NuGet パッケージを使用します。
1. CSU パッケージ プロジェクトを構築します。 出力 CSU 拡張機能パッケージには、ISV および自身の拡張機能からの拡張機能が含まれます。

### <a name="generate-a-nuget-package-for-the-isvs-extensions"></a>ISV 拡張機能用の NuGet パッケージを生成する

ISV 拡張プロジェクトがある場合は、以下の手順を実行して NuGet パッケージを生成します。 または、ISV にそれを実行するよう求めます。

1. ISV 拡張機能 CSU パッケージ プロジェクトを、Visual Studio Code または Visual Studio で開きます。
1. ISV CSU パッケージ プロジェクト ファイルを編集し、次のビルド プロパティ追加して[ビルドに NuGet パッケージを生成](/nuget/create-packages/creating-a-package-msbuild#automatically-generate-package-on-build)し、さらに CSU 拡張機能パッケージを生成します。

    ```XML
    <GeneratePackageOnBuild>true</GeneratePackageOnBuild>
    ```

1. ISV から CSU 拡張機能 NuGet パッケージを取得します。

### <a name="consume-the-nuget-package-in-your-csu-extension-package"></a>CSU 拡張パッケージで NuGet パッケージを使用する

CSU 拡張機能パッケージで NuGet パッケージを消費するには、次の手順に従います。

1. ISV から NuGet パッケージを消費する前に、次の XML を使用して **nuget.config** ファイルで ISV CSU 拡張機能 NuGet パッケージ用の[パッケージ フィード場所](/nuget/hosting-packages/local-feeds)を設定します。

    ```XML
    <packageSources>
        <add key="local" value="packages" />
    </packageSources>
    ```

1. 拡張機能 CSU パッケージ プロジェクトを、Visual Studio Code または Visual Studio で開きます。
1. 次の例に示すように、プロジェクト ファイルを編集し、ISV から受け取った CSU 拡張機能 NuGet パッケージを、CSU 拡張機能パッケージ プロジェクトの参照として追加します。

    ```XML
    <PackageReference Include="Contoso.Extension.Sample.Package" Version="2.0.*" />
    ```

    正確なパッケージ バージョンを指定するか、ワイルド カードを使用して更新されたバージョンを選択できます (使用可能な場合)。 ISV NuGet パッケージが複数ある場合は、必要に応じて手順 3 を繰り返します。

1. CSU パッケージ プロジェクトを構築します。 出力 CSU 拡張機能パッケージには、ISV および自身の拡張機能からの拡張機能が含まれます。

CSU 拡張機能パッケージを生成および配置する方法の詳細については、[Cloud Scale Unit 拡張機能パッケージの作成](csu-packaging.md)を参照してください。
