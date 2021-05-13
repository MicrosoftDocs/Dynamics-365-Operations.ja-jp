---
title: 新しい NuGet パッケージ用にホストされる Azure Pipeline の更新
description: このトピックでは、新しい NuGet パッケージを使用するために Azure パイプラインを更新する方法について説明します。
author: jorisdg
ms.date: 03/04/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53ae0068b9acfd4f330183d49a7267a8686963be
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866236"
---
# <a name="update-the-hosted-azure-pipeline-for-new-nuget-packages"></a><span data-ttu-id="00d0a-103">新しい NuGet パッケージ用にホストされる Azure Pipeline の更新</span><span class="sxs-lookup"><span data-stu-id="00d0a-103">Update the hosted Azure Pipeline for new NuGet packages</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="00d0a-104">このトピックは、バージョン 10.0.17 以前に設定したパイプラインに適用されます。</span><span class="sxs-lookup"><span data-stu-id="00d0a-104">This topic applies to pipelines that were set up for versions 10.0.17 or earlier.</span></span> <span data-ttu-id="00d0a-105">これは、ビルド仮想マシンを使用するレガシ ビルド パイプラインには適用されません。</span><span class="sxs-lookup"><span data-stu-id="00d0a-105">This does not apply to the legacy build pipeline that uses the build virtual machine.</span></span>

<span data-ttu-id="00d0a-106">[バージョン 10.0.18](../get-started/whats-new-platform-updates-10-0-18.md) のプラットフォーム更新により、新しい NuGet パッケージが導入されます。</span><span class="sxs-lookup"><span data-stu-id="00d0a-106">Platform updates for [version 10.0.18](../get-started/whats-new-platform-updates-10-0-18.md) introduce a new NuGet package.</span></span> <span data-ttu-id="00d0a-107">新しいパッケージは、アプリケーション ビルド参照コードのパッケージ分割の結果です。</span><span class="sxs-lookup"><span data-stu-id="00d0a-107">The new package is a result of a package split for the Application Build Reference code.</span></span> <span data-ttu-id="00d0a-108">このため、10.0.17 以前のバージョンで作成されたパイプラインに変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="00d0a-108">As a result, you have to make changes to pipelines created for 10.0.17 or earlier versions.</span></span>

## <a name="add-the-new-package-to-packagesconfig-list"></a><span data-ttu-id="00d0a-109">新しいパッケージを packages.config リストに追加する</span><span class="sxs-lookup"><span data-stu-id="00d0a-109">Add the new package to packages.config list</span></span>

<span data-ttu-id="00d0a-110">ビルドで使用される **packages.config** ファイルには、既に 3 つのパッケージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="00d0a-110">The **packages.config** file used for your build already includes three packages:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
    <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5934.35741" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.761.10019" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5934.35741" targetFramework="net40" />
</packages>
```

<span data-ttu-id="00d0a-111">リストに 4 つ目のパッケージ **Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp** を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00d0a-111">You need to add a fourth package to the list, **Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp**.</span></span> <span data-ttu-id="00d0a-112">結果の **packages.config** ファイルは次の例のようになり、バージョン番号がパイプラインで使用されているバージョン番号に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="00d0a-112">The resulting **packages.config** file should look like the following example, replacing the version number with the version number that your pipeline uses.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<packages>
    <package id="Microsoft.Dynamics.AX.Platform.DevALM.BuildXpp" version="7.0.5968.16973" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Application.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp" version="10.0.793.16" targetFramework="net40" />
    <package id="Microsoft.Dynamics.AX.Platform.CompilerPackage" version="7.0.5968.16973" targetFramework="net40" />
</packages>
```

## <a name="add-a-pipeline-variable"></a><span data-ttu-id="00d0a-113">パイプライン変数を追加する</span><span class="sxs-lookup"><span data-stu-id="00d0a-113">Add a pipeline variable</span></span>

<span data-ttu-id="00d0a-114">パイプラインは変数を使用して、パイプライン タスクで使用されるパラメーターを単純化および一元化します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-114">The pipeline uses variables to simplify and centralize parameters used in the pipeline tasks.</span></span> <span data-ttu-id="00d0a-115">NuGet パッケージ名ごとに既に変数があります。</span><span class="sxs-lookup"><span data-stu-id="00d0a-115">There are already variables for each of the NuGet package names.</span></span> <span data-ttu-id="00d0a-116">新しい NuGet パッケージの名前の変数を追加するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="00d0a-116">To add a variable for the name of the new NuGet package, do the following:</span></span>

1. <span data-ttu-id="00d0a-117">パイプラインの **変数** タブで、変数リストの下にある **追加** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-117">On the **Variables** tab of the pipeline, select the **Add** link at the bottom of the list of variables.</span></span>
2. <span data-ttu-id="00d0a-118">**名前** 列に、`AppSuitePackage` と入力します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-118">In the **Name** column, type `AppSuitePackage`.</span></span>
3. <span data-ttu-id="00d0a-119">**値** 列に、`Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp` と入力します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-119">In the **Value** column, type `Microsoft.Dynamics.AX.ApplicationSuite.DevALM.BuildXpp`.</span></span>

## <a name="update-the-build-solution-step"></a><span data-ttu-id="00d0a-120">**ソリューションのビルド** ステップを更新する</span><span class="sxs-lookup"><span data-stu-id="00d0a-120">Update the **Build solution** step</span></span>

<span data-ttu-id="00d0a-121">パイプラインの **ソリューションのビルド** ステップでは、すべての NuGet パッケージのパスおよび名前は、コマンド ライン パラメーターとして **MSBuild** に提供されます。</span><span class="sxs-lookup"><span data-stu-id="00d0a-121">In the **Build solution** step in the pipeline, the path and names to all the NuGet packages are supplied as command-line parameters to **MSBuild**.</span></span> <span data-ttu-id="00d0a-122">新しい NuGet パッケージを **ReferenceFolder** パスのセミコロンで区切られたリストに追加するには、次のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-122">To add the new NuGet package to the semi-colon separated list of **ReferenceFolder** paths, do either of the following:</span></span>

- <span data-ttu-id="00d0a-123">既存のテンプレートを変更せずに使用した場合、新しい **MSBuild 引数** は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="00d0a-123">If you used the existing template without modifying it, the new **MSBuild Arguments** will be:</span></span>

    `/p:BuildTasksDirectory="$(NugetsPath)\$(ToolsPackage)\DevAlm" /p:MetadataDirectory="$(MetadataPath)" /p:FrameworkDirectory="$(NuGetsPath)\$(ToolsPackage)" /p:ReferenceFolder="$(NuGetsPath)\$(PlatPackage)\ref\net40;$(NuGetsPath)\$(AppPackage)\ref\net40;$(MetadataPath);$(Build.BinariesDirectory);$(NuGetsPath)\$(AppSuitePackage)\ref\net40" /p:ReferencePath="$(NuGetsPath)\$(ToolsPackage)" /p:OutputDirectory="$(Build.BinariesDirectory)"`

- <span data-ttu-id="00d0a-124">引数リストを変更した場合は、**ReferenceFolder** プロパティ引数を見つけて、セミコロンで区切られたリストに `$(NuGetsPath)\$(AppSuitePackage)\ref\net40` を追加します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-124">If you've modified the arguments list, find the **ReferenceFolder** property argument and add `$(NuGetsPath)\$(AppSuitePackage)\ref\net40` to the semi-colon separated list.</span></span> <span data-ttu-id="00d0a-125">セミコロンを追加して、この新しいエントリをリスト内の他のパスから分離します。</span><span class="sxs-lookup"><span data-stu-id="00d0a-125">Add a semi-colon to separate this new entry from other paths in the list.</span></span>

## <a name="use-the-updated-templates-on-github-as-an-alternative"></a><span data-ttu-id="00d0a-126">代わりに GitHub で更新されたテンプレートを使用する</span><span class="sxs-lookup"><span data-stu-id="00d0a-126">Use the updated templates on GitHub as an alternative</span></span>

<span data-ttu-id="00d0a-127">これらの変更を行う代わりに、または変更を確認するために、[Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub リポジトリで更新されたテンプレートを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00d0a-127">As an alternative to making these changes, or as a way to verify your changes, review the updated templates in the [Dynamics365-Xpp-Samples-Tools](https://github.com/microsoft/Dynamics365-Xpp-Samples-Tools/tree/master/CI-CD/Pipeline-Samples) GitHub repository.</span></span>
