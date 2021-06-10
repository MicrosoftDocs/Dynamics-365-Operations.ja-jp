---
title: POS 拡張機能の基本
description: このトピックでは、POS 拡張機能の基本的な概念について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 5d88f07bf32bfcd46798ea0d218ae9fc0e98d3d7
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984293"
---
# <a name="pos-extension-basics"></a><span data-ttu-id="37752-103">POS 拡張機能の基本</span><span class="sxs-lookup"><span data-stu-id="37752-103">POS extension basics</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="37752-104">このトピックでは、POS 拡張機能の基本的な概念について説明します。</span><span class="sxs-lookup"><span data-stu-id="37752-104">This topic describes the basic POS extension concepts.</span></span> <span data-ttu-id="37752-105">Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="37752-105">It applies to the Retail SDK version 10.0.18 and later.</span></span>

<span data-ttu-id="37752-106">POS により、拡張機能の開発者は POS API ライブラリを使用してカスタマイズを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="37752-106">POS lets extension developers create customizations by using the POS API library.</span></span>  <span data-ttu-id="37752-107">POS API により、POS のビジネス ロジックおよび UI レイヤーの両方をカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="37752-107">The POS APIs let you customize both business logic and UI layers of POS.</span></span>

## <a name="terminology"></a><span data-ttu-id="37752-108">用語</span><span class="sxs-lookup"><span data-stu-id="37752-108">Terminology</span></span>

<span data-ttu-id="37752-109">これらの用語がこのトピックで使用されます。</span><span class="sxs-lookup"><span data-stu-id="37752-109">These terms are used in this topic.</span></span>

<span data-ttu-id="37752-110">相談</span><span class="sxs-lookup"><span data-stu-id="37752-110">Term</span></span> | <span data-ttu-id="37752-111">定義</span><span class="sxs-lookup"><span data-stu-id="37752-111">Definition</span></span> | <span data-ttu-id="37752-112">例</span><span class="sxs-lookup"><span data-stu-id="37752-112">Examples</span></span>
---|---|---
<span data-ttu-id="37752-113">拡張ポイント</span><span class="sxs-lookup"><span data-stu-id="37752-113">Extension point</span></span> | <span data-ttu-id="37752-114">POS を拡張できる特定の場所、または POS に新しい機能を追加する技術。</span><span class="sxs-lookup"><span data-stu-id="37752-114">A specific location at which POS can be extended, or a technique through which new functionality can be added to POS.</span></span> | <span data-ttu-id="37752-115">**PreOperationTrigger** 呼び出しのポイント。</span><span class="sxs-lookup"><span data-stu-id="37752-115">**PreOperationTrigger** invocation point.</span></span><br><span data-ttu-id="37752-116">新しいビューの追加。</span><span class="sxs-lookup"><span data-stu-id="37752-116">Adding a new view.</span></span>
<span data-ttu-id="37752-117">内線</span><span class="sxs-lookup"><span data-stu-id="37752-117">Extension</span></span> | <span data-ttu-id="37752-118">特定の拡張ポイントを使用して POS をカスタマイズするのに役立つ個々のコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="37752-118">An individual component that helps to customize POS by utilizing a specific extension point.</span></span> | <span data-ttu-id="37752-119">新しい操作</span><span class="sxs-lookup"><span data-stu-id="37752-119">New operation</span></span><br><span data-ttu-id="37752-120">新しいビュー</span><span class="sxs-lookup"><span data-stu-id="37752-120">New view</span></span><br><span data-ttu-id="37752-121">**PreOperationTrigger** の実装</span><span class="sxs-lookup"><span data-stu-id="37752-121">**PreOperationTrigger** implementation</span></span>
<span data-ttu-id="37752-122">拡張パッケージ</span><span class="sxs-lookup"><span data-stu-id="37752-122">Extension package</span></span> | <span data-ttu-id="37752-123">組み合わせた場合にカスタマイズされたエンド ツー エンド POS シナリオを有効にする一連の拡張機能。</span><span class="sxs-lookup"><span data-stu-id="37752-123">A set of extensions that when combined enable a custom end-to-end POS scenario.</span></span> | <span data-ttu-id="37752-124">新しいビューに移動する操作を含むパッケージ。</span><span class="sxs-lookup"><span data-stu-id="37752-124">A package that contains an operation that navigates to a new view.</span></span>

## <a name="types-of-extensions"></a><span data-ttu-id="37752-125">拡張機能のタイプ</span><span class="sxs-lookup"><span data-stu-id="37752-125">Types of Extensions</span></span>

<span data-ttu-id="37752-126">POS 拡張機能は 2 つのタイプに分類できます。</span><span class="sxs-lookup"><span data-stu-id="37752-126">POS extensions can be classified into two types.</span></span>

+ <span data-ttu-id="37752-127">拡張機能の *拡張* とは、既存のページまたはワークフローを変更することにより POS の機能を変更することです。</span><span class="sxs-lookup"><span data-stu-id="37752-127">*Extend* extensions modify POS functionality by modifying existing pages or workflows.</span></span>
+ <span data-ttu-id="37752-128">拡張機能の *作成* とは、POS を補い、の機能拡張を作成し、既成には存在しない新しいページまたはワークフローを導入して新しい機能を作成することです。</span><span class="sxs-lookup"><span data-stu-id="37752-128">*Create* extensions supplement POS and create new functionality by introducing new pages or workflows that do not exist out of the box.</span></span>

<span data-ttu-id="37752-129">*拡張* 拡張機能と *作成* 拡張機能の違いは、POS 拡張機能フレームワークを通して組み込まれることです。</span><span class="sxs-lookup"><span data-stu-id="37752-129">The distinction between *extend* and *create* extensions is incorporated throughout the POS extensibility framework.</span></span> <span data-ttu-id="37752-130">拡張機能を開発する場合、「既存の POS コンポーネントを拡張するか、または全く新しい機能を作成するか」を考えることは役立ちます。</span><span class="sxs-lookup"><span data-stu-id="37752-130">When you are developing an extension, it can be helpful to think: “Am I extending an existing POS component or creating entirely new functionality?”</span></span>

## <a name="pos-api"></a><span data-ttu-id="37752-131">POS API</span><span class="sxs-lookup"><span data-stu-id="37752-131">POS API</span></span>

<span data-ttu-id="37752-132">POS API ライブラリには、拡張機能がモジュールを使用する方法に基づいてまとめられた一連のモジュールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="37752-132">The POS API library contains a set of modules that are organized based on how the module will be used by the extension.</span></span>

+ <span data-ttu-id="37752-133">**拡張**</span><span class="sxs-lookup"><span data-stu-id="37752-133">**Extend**</span></span>
    + <span data-ttu-id="37752-134">拡張機能が POS コンポーネントおよびワークフローを拡張するのに役立つモジュール。</span><span class="sxs-lookup"><span data-stu-id="37752-134">Modules that help extensions extend POS components and workflows.</span></span>
    + <span data-ttu-id="37752-135">サブディレクトリは、拡張するコンポーネントのタイプに基づいてまとめられた後、拡張する機能領域に基づいてまとめられます。</span><span class="sxs-lookup"><span data-stu-id="37752-135">Subdirectories are organized based on the type of component to be extended and then the feature area to be extended.</span></span>
    + <span data-ttu-id="37752-136">例: **PosApi/Extend/Views/CustomerDetailsView**、**PosApi/Extend/Triggers/ProductTriggers**</span><span class="sxs-lookup"><span data-stu-id="37752-136">Examples: **PosApi/Extend/Views/CustomerDetailsView**, **PosApi/Extend/Triggers/ProductTriggers**</span></span>

+ <span data-ttu-id="37752-137">**新規**</span><span class="sxs-lookup"><span data-stu-id="37752-137">**Create**</span></span>
    + <span data-ttu-id="37752-138">拡張機能を支援するモジュールにより、新しいコンポーネントおよび機能が作成されます。</span><span class="sxs-lookup"><span data-stu-id="37752-138">Modules that help extensions create new components and functionality.</span></span>
    + <span data-ttu-id="37752-139">このノードの下のサブディレクトリは、作成するコンポーネントのタイプに基づいてまとめられます。</span><span class="sxs-lookup"><span data-stu-id="37752-139">Subdirectories under this node are organized based on the type of component to be created.</span></span>
    + <span data-ttu-id="37752-140">例: **PosApi/Create/Views**</span><span class="sxs-lookup"><span data-stu-id="37752-140">Example: **PosApi/Create/Views**</span></span>

+ <span data-ttu-id="37752-141">**消費**</span><span class="sxs-lookup"><span data-stu-id="37752-141">**Consume**</span></span>
    + <span data-ttu-id="37752-142">拡張機能で POS 機能を実行できるようにするモジュール。</span><span class="sxs-lookup"><span data-stu-id="37752-142">Modules that allow extensions to execute POS functionality.</span></span>

<span data-ttu-id="37752-143">POS API ライブラリの API の完全な一覧とモジュールの型宣言は、**Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージと共に配布される **Pos.Api.d.ts** 内で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="37752-143">The complete list of APIs and the type declarations for the modules in the POS API library can be found in **Pos.Api.d.ts**, which is distributed with the **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet package.</span></span>

## <a name="manifestjson"></a><span data-ttu-id="37752-144">Manifest.json</span><span class="sxs-lookup"><span data-stu-id="37752-144">Manifest.json</span></span>

<span data-ttu-id="37752-145">各拡張機能パッケージは、**manifest.json** ファイルを拡張機能パッケージのルート ディレクトリ内に格納している必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-145">Each extension package must have a **manifest.json** file in the extension package's root directory.</span></span> <span data-ttu-id="37752-146">このマニフェスト ファイルには、拡張機能パッケージに関する重要な情報が含まれており、パッケージに含まれる拡張機能の一覧を定義しています。</span><span class="sxs-lookup"><span data-stu-id="37752-146">This manifest file contains important information about the extension package and defines the list of extensions contained in the package.</span></span> <span data-ttu-id="37752-147">マニフェスト ファイルは、POS 用の **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージで提供されているマニフェスト スキーマに従って、拡張機能を読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-147">The manifest file must follow the manifest schema that is provided in the **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet package for POS to load the extensions.</span></span>

### <a name="fields"></a><span data-ttu-id="37752-148">フィールド</span><span class="sxs-lookup"><span data-stu-id="37752-148">Fields</span></span>

<span data-ttu-id="37752-149">これらのフィールドは、マニフェスト ファイルに含まれています。</span><span class="sxs-lookup"><span data-stu-id="37752-149">These fields are contained in the manifest file.</span></span>

+ <span data-ttu-id="37752-150">**名前** - 拡張パッケージの名前。</span><span class="sxs-lookup"><span data-stu-id="37752-150">**name** - The name of the extension package.</span></span>
+ <span data-ttu-id="37752-151">**説明** - 拡張機能パッケージの機能の説明。</span><span class="sxs-lookup"><span data-stu-id="37752-151">**description** - A description of the extension package's functionality.</span></span>
+ <span data-ttu-id="37752-152">**発行元** - 拡張機能パッケージの発行元または組織の名前。</span><span class="sxs-lookup"><span data-stu-id="37752-152">**publisher** - The name of the extension package's publisher or organization.</span></span>
+ <span data-ttu-id="37752-153">**バージョン** - 拡張機能パッケージのバージョン。</span><span class="sxs-lookup"><span data-stu-id="37752-153">**version** - The extension package version.</span></span> <span data-ttu-id="37752-154">バージョンは、セマンティック バージョニング パターンに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-154">The version must follow semantic versioning pattern.</span></span>
+ <span data-ttu-id="37752-155">**minimumPosVersion** - 拡張機能パッケージを実行するために必要な最小 POS バージョン。</span><span class="sxs-lookup"><span data-stu-id="37752-155">**minimumPosVersion** - The minimum POS version that is required to run the extension package.</span></span> <span data-ttu-id="37752-156">バージョン番号は、消費している POS NuGet パッケージと、インストールされた POS アプリによって異なります。</span><span class="sxs-lookup"><span data-stu-id="37752-156">The version number depends on the POS NuGet package that you're consuming and the POS app that is installed.</span></span> <span data-ttu-id="37752-157">たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンから、POS API または 拡張機能アーティファクトを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="37752-157">For example, the extension project should not use POS APIs or extension artifacts from a version that is later than the version of the POS app that is installed.</span></span> <span data-ttu-id="37752-158">ランタイムに、POS アプリは拡張機能パッケージのバージョンを確認します。</span><span class="sxs-lookup"><span data-stu-id="37752-158">At runtime, the POS app checks the version of the extension package.</span></span> <span data-ttu-id="37752-159">インストールされた POS アプリよりも古いバージョンの場合、拡張機能パッケージは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="37752-159">If it's later than the version of the installed POS app, the extension package won't be loaded.</span></span>
+ <span data-ttu-id="37752-160">**supportedCountryRegions** - 拡張機能パッケージを読み込む国または地域コードのオプションのリスト。</span><span class="sxs-lookup"><span data-stu-id="37752-160">**supportedCountryRegions** - The optional list of country region codes in which to load the extension package.</span></span> <span data-ttu-id="37752-161">この値が指定されていない場合、POS の現在の国や地域に関係なく、拡張機能パッケージが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="37752-161">If this value is not specified, then the extension package will be loaded regardless of the current POS country region.</span></span>
+ <span data-ttu-id="37752-162">**components** - 拡張機能パッケージに含まれている拡張機能の一覧。</span><span class="sxs-lookup"><span data-stu-id="37752-162">**components** - The list of extensions contained in the extension package.</span></span>

<span data-ttu-id="37752-163">こちらは、マニフェスト ファイルの例です。</span><span class="sxs-lookup"><span data-stu-id="37752-163">Here is an example of a manifest file.</span></span>

```json
{
    "$schema": "./devDependencies/schemas/manifestSchema.json",
    "name": "Contoso.Pos.Developer.Samples",
    "publisher": "Contoso",
    "version": "1.0.0",
    "minimumPosVersion": "9.28.0.0",
    "description": "An extension package containing POS developer samples to showcase various types of POS extensions.",
}
```

### <a name="extension-structure"></a><span data-ttu-id="37752-164">拡張機能の構造</span><span class="sxs-lookup"><span data-stu-id="37752-164">Extension structure</span></span>

<span data-ttu-id="37752-165">各 POS 拡張機能には、1 つ以上の TypeScript モジュールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="37752-165">Each POS extension contains one or more TypeScript modules.</span></span> <span data-ttu-id="37752-166">拡張機能クラスは、POS API から公開され、適用される基本クラスから継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-166">Extension classes must inherit from the applicable base class exposed from the POS API.</span></span> <span data-ttu-id="37752-167">POS API のコンポーネントとタイプは、次のコード例に示すように、POS API モジュールの相対的でないインポートを使用して、拡張モジュールにインポートできます。</span><span class="sxs-lookup"><span data-stu-id="37752-167">The components and types in the POS API can be imported into the extension module using a non-relative import of a POS API module, as shown in the following code example.</span></span>

```JavaScript
import { ApplicationStartTrigger } from “PosApi/Extend/Triggers/ApplicationTriggers”;
```

<span data-ttu-id="37752-168">次のコード例に示すように、各拡張モジュールには拡張クラスの既定のエクスポートを 1 つ含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-168">Each extension module should contain a single, default export of the extension class as shown in the following code example.</span></span>

```JavaScript
import { ApplicationStartTrigger } from “PosApi/Extend/Triggers/ApplicationTriggers”;
export default class MyCustomApplicationStartTrigger extends ApplicationStartTrigger {
    public execute(options): Promise<void> {
        return Promise.resolve();
    }
}
```

### <a name="configuring-extension-packages"></a><span data-ttu-id="37752-169">拡張機能パッケージの構成</span><span class="sxs-lookup"><span data-stu-id="37752-169">Configuring Extension Packages</span></span>

<span data-ttu-id="37752-170">POS は、**GetExtensionPackageDefinitions** API を呼び出すことにより、ヘッドレス Commerce エンジンから構成された拡張機能パッケージの定義の一覧を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="37752-170">POS loads the list of configured extension package definitions from the headless Commerce engine by calling the **GetExtensionPackageDefinitions** API.</span></span> <span data-ttu-id="37752-171">**GetExtensionPackageDefinitions** API は、**GetExtensionPackageDefinitions** Commerce Runtime 要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="37752-171">The **GetExtensionPackageDefinitions** API runs the **GetExtensionPackageDefinitions** Commerce Runtime request.</span></span> <span data-ttu-id="37752-172">拡張機能パッケージを読み込むように POS を構成するには、次のコード例に示されているように、Commerce Runtime トリガーを **GetExtensionPackageDefinitionsRequest** に追加し、拡張機能パッケージの定義を **GetExtensionPackageDefinitionsResponse** 内にある定義の一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="37752-172">To configure POS to load your extension package, add a Commerce Runtime trigger for the **GetExtensionPackageDefinitionsRequest** and add your extension package definition to the list of definitions in the **GetExtensionPackageDefinitionsResponse** as shown in the following code example.</span></span>
<span data-ttu-id="37752-173">**ExtensionPackageDefinition** のフィールドは、POS 拡張機能パッケージを作成するときに使用した値と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-173">The fields in **ExtensionPackageDefinition** must match the values used when creating the POS extension package.</span></span>

+ <span data-ttu-id="37752-174">**名前** - 名前は、拡張機能パッケージ プロジェクトの **PackageName** と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-174">**Name** - The name must match the **PackageName** for the extension package project.</span></span> <span data-ttu-id="37752-175">名前は、POS 拡張機能パッケージの検索および読み込みのために使用され、値は正確に一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-175">The name is used to locate and load the POS extension package so the values must match exactly.</span></span>
+ <span data-ttu-id="37752-176">**発行元** - 発行元は、拡張機能パッケージの manifest.json で指定されている発行元と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="37752-176">**Publisher** - The publisher must match the publisher specified in the extension package’s manifest.json.</span></span>

```CSharp
/// <summary>
/// Class that implements a post trigger for the GetExtensionPackageDefinitionsRequest request type.
/// </summary>
public class DefinePosExtensionPackageTrigger : IRequestTrigger
{
    /// <summary>
    /// Gets the supported requests for this trigger.
    /// </summary>
    public IEnumerable<Type> SupportedRequestTypes
    {
        get
        {
            return new[] { typeof(GetExtensionPackageDefinitionsRequest) };
        }
    }

    /// <summary>
    /// Post trigger to retrieve extension package.
    /// </summary>
    /// <param name="request">The request.</param>
    /// <param name="response">The response.</param>
    public void OnExecuted(Request request, Response response)
    {
        var getExtensionsResponse = (GetExtensionPackageDefinitionsResponse)response;
        var extensionPackageDefinition = new ExtensionPackageDefinition();

        // Should match the PackageName used when packaging the customization package.
        extensionPackageDefinition.Name = "Contoso.Commerce";
        extensionPackageDefinition.Publisher = "Contoso";
        extensionPackageDefinition.IsEnabled = true;

        getExtensionsResponse.ExtensionPackageDefinitions.Add(extensionPackageDefinition);
    }

    public void OnExecuting(Request request)
    {
    }
}
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
