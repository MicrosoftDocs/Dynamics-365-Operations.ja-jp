---
title: 新しい NuGet パッケージ用にホストされる Azure Pipeline の更新
description: この記事では、新しい NuGet パッケージを使用するために Azure パイプラインを更新する方法について説明します。
author: jorisdg
ms.date: 03/04/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cfbb0f3562280538ed9e815e49047e5866e9822
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867003"
---
# <a name="update-the-hosted-azure-pipeline-for-new-nuget-packages"></a>新しい NuGet パッケージ用にホストされる Azure Pipeline の更新

[!include [banner](../includes/banner.md)]

> [!NOTE]
> この記事は、バージョン 10.0.17 以前に設定したパイプラインに適用されます。 これは、ビルド仮想マシンを使用するレガシ ビルド パイプラインには適用されません。

[バージョン 10.0.18](../get-started/whats-new-platform-updates-10-0-18.md) のプラットフォーム更新により、新しい NuGet パッケージが導入されます。 新しいパッケージは、アプリケーション ビルド参照コードのパッケージ分割の結果です。 このため、10.0.17 以前のバージョンで作成されたパイプラインに変更を加える必要があります。

## <a name="add-the-new-package-to-packagesconfig-list"></a>新しいパッケージを packages.config リストに追加する

ビルドで使用される **packages.config** ファイルには、既に 3 つのパッケージが含まれています。

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
    <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5934.35741" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.761.10019" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5934.35741" targetFramework="net40" />
</packages>
```

リストに 4 つ目のパッケージ **Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp** を追加する必要があります。 結果の **packages.config** ファイルは次の例のようになり、バージョン番号がパイプラインで使用されているバージョン番号に置き換えられます。

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
    <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5968.16973" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5968.16973" targetFramework="net40" />
</packages>
```

## <a name="add-a-pipeline-variable"></a>パイプライン変数を追加する

パイプラインは変数を使用して、パイプライン タスクで使用されるパラメーターを単純化および一元化します。 NuGet パッケージ名ごとに既に変数があります。 新しい NuGet パッケージの名前の変数を追加するには、次の操作を行います。

1. パイプラインの **変数** タブで、変数リストの下にある **追加** リンクを選択します。
2. **名前** 列に、`AppSuitePackage` と入力します。
3. **値** 列に、`Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp` と入力します。

## <a name="update-the-build-solution-step"></a>**ソリューションのビルド** ステップを更新する

パイプラインの **ソリューションのビルド** ステップでは、すべての NuGet パッケージのパスおよび名前は、コマンド ライン パラメーターとして **MSBuild** に提供されます。 新しい NuGet パッケージを **ReferenceFolder** パスのセミコロンで区切られたリストに追加するには、次のいずれかを実行します。

- 既存のテンプレートを変更せずに使用した場合、新しい **MSBuild 引数** は次のようになります。

    `/p:BuildTasksDirectory="$(NugetsPath)\$(ToolsPackage)\DevAlm" /p:MetadataDirectory="$(MetadataPath)" /p:FrameworkDirectory="$(NuGetsPath)\$(ToolsPackage)" /p:ReferenceFolder="$(NuGetsPath)\$(PlatPackage)\ref\net40;$(NuGetsPath)\$(AppPackage)\ref\net40;$(MetadataPath);$(Build.BinariesDirectory);$(NuGetsPath)\$(AppSuitePackage)\ref\net40" /p:ReferencePath="$(NuGetsPath)\$(ToolsPackage)" /p:OutputDirectory="$(Build.BinariesDirectory)"`

- 引数リストを変更した場合は、**ReferenceFolder** プロパティ引数を見つけて、セミコロンで区切られたリストに `$(NuGetsPath)\$(AppSuitePackage)\ref\net40` を追加します。 セミコロンを追加して、この新しいエントリをリスト内の他のパスから分離します。

## <a name="use-the-updated-templates-on-github-as-an-alternative"></a>代わりに GitHub で更新されたテンプレートを使用する

これらの変更を行う代わりに、または変更を確認するために、[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリで更新されたテンプレートを確認してください。
