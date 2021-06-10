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
# <a name="pos-extension-basics"></a>POS 拡張機能の基本

[!include [banner](../../../includes/banner.md)]

このトピックでは、POS 拡張機能の基本的な概念について説明します。 Retail SDK バージョン 10.0.18 以降に適用されます。

POS により、拡張機能の開発者は POS API ライブラリを使用してカスタマイズを作成することができます。  POS API により、POS のビジネス ロジックおよび UI レイヤーの両方をカスタマイズできます。

## <a name="terminology"></a>用語

これらの用語がこのトピックで使用されます。

相談 | 定義 | 例
---|---|---
拡張ポイント | POS を拡張できる特定の場所、または POS に新しい機能を追加する技術。 | **PreOperationTrigger** 呼び出しのポイント。<br>新しいビューの追加。
内線 | 特定の拡張ポイントを使用して POS をカスタマイズするのに役立つ個々のコンポーネント。 | 新しい操作<br>新しいビュー<br>**PreOperationTrigger** の実装
拡張パッケージ | 組み合わせた場合にカスタマイズされたエンド ツー エンド POS シナリオを有効にする一連の拡張機能。 | 新しいビューに移動する操作を含むパッケージ。

## <a name="types-of-extensions"></a>拡張機能のタイプ

POS 拡張機能は 2 つのタイプに分類できます。

+ 拡張機能の *拡張* とは、既存のページまたはワークフローを変更することにより POS の機能を変更することです。
+ 拡張機能の *作成* とは、POS を補い、の機能拡張を作成し、既成には存在しない新しいページまたはワークフローを導入して新しい機能を作成することです。

*拡張* 拡張機能と *作成* 拡張機能の違いは、POS 拡張機能フレームワークを通して組み込まれることです。 拡張機能を開発する場合、「既存の POS コンポーネントを拡張するか、または全く新しい機能を作成するか」を考えることは役立ちます。

## <a name="pos-api"></a>POS API

POS API ライブラリには、拡張機能がモジュールを使用する方法に基づいてまとめられた一連のモジュールが含まれています。

+ **拡張**
    + 拡張機能が POS コンポーネントおよびワークフローを拡張するのに役立つモジュール。
    + サブディレクトリは、拡張するコンポーネントのタイプに基づいてまとめられた後、拡張する機能領域に基づいてまとめられます。
    + 例: **PosApi/Extend/Views/CustomerDetailsView**、**PosApi/Extend/Triggers/ProductTriggers**

+ **新規**
    + 拡張機能を支援するモジュールにより、新しいコンポーネントおよび機能が作成されます。
    + このノードの下のサブディレクトリは、作成するコンポーネントのタイプに基づいてまとめられます。
    + 例: **PosApi/Create/Views**

+ **消費**
    + 拡張機能で POS 機能を実行できるようにするモジュール。

POS API ライブラリの API の完全な一覧とモジュールの型宣言は、**Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージと共に配布される **Pos.Api.d.ts** 内で見つけることができます。

## <a name="manifestjson"></a>Manifest.json

各拡張機能パッケージは、**manifest.json** ファイルを拡張機能パッケージのルート ディレクトリ内に格納している必要があります。 このマニフェスト ファイルには、拡張機能パッケージに関する重要な情報が含まれており、パッケージに含まれる拡張機能の一覧を定義しています。 マニフェスト ファイルは、POS 用の **Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージで提供されているマニフェスト スキーマに従って、拡張機能を読み込む必要があります。

### <a name="fields"></a>フィールド

これらのフィールドは、マニフェスト ファイルに含まれています。

+ **名前** - 拡張パッケージの名前。
+ **説明** - 拡張機能パッケージの機能の説明。
+ **発行元** - 拡張機能パッケージの発行元または組織の名前。
+ **バージョン** - 拡張機能パッケージのバージョン。 バージョンは、セマンティック バージョニング パターンに従う必要があります。
+ **minimumPosVersion** - 拡張機能パッケージを実行するために必要な最小 POS バージョン。 バージョン番号は、消費している POS NuGet パッケージと、インストールされた POS アプリによって異なります。 たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンから、POS API または 拡張機能アーティファクトを使用しないでください。 ランタイムに、POS アプリは拡張機能パッケージのバージョンを確認します。 インストールされた POS アプリよりも古いバージョンの場合、拡張機能パッケージは読み込まれません。
+ **supportedCountryRegions** - 拡張機能パッケージを読み込む国または地域コードのオプションのリスト。 この値が指定されていない場合、POS の現在の国や地域に関係なく、拡張機能パッケージが読み込まれます。
+ **components** - 拡張機能パッケージに含まれている拡張機能の一覧。

こちらは、マニフェスト ファイルの例です。

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

### <a name="extension-structure"></a>拡張機能の構造

各 POS 拡張機能には、1 つ以上の TypeScript モジュールが含まれます。 拡張機能クラスは、POS API から公開され、適用される基本クラスから継承する必要があります。 POS API のコンポーネントとタイプは、次のコード例に示すように、POS API モジュールの相対的でないインポートを使用して、拡張モジュールにインポートできます。

```JavaScript
import { ApplicationStartTrigger } from “PosApi/Extend/Triggers/ApplicationTriggers”;
```

次のコード例に示すように、各拡張モジュールには拡張クラスの既定のエクスポートを 1 つ含める必要があります。

```JavaScript
import { ApplicationStartTrigger } from “PosApi/Extend/Triggers/ApplicationTriggers”;
export default class MyCustomApplicationStartTrigger extends ApplicationStartTrigger {
    public execute(options): Promise<void> {
        return Promise.resolve();
    }
}
```

### <a name="configuring-extension-packages"></a>拡張機能パッケージの構成

POS は、**GetExtensionPackageDefinitions** API を呼び出すことにより、ヘッドレス Commerce エンジンから構成された拡張機能パッケージの定義の一覧を読み込みます。 **GetExtensionPackageDefinitions** API は、**GetExtensionPackageDefinitions** Commerce Runtime 要求を実行します。 拡張機能パッケージを読み込むように POS を構成するには、次のコード例に示されているように、Commerce Runtime トリガーを **GetExtensionPackageDefinitionsRequest** に追加し、拡張機能パッケージの定義を **GetExtensionPackageDefinitionsResponse** 内にある定義の一覧に追加します。
**ExtensionPackageDefinition** のフィールドは、POS 拡張機能パッケージを作成するときに使用した値と一致している必要があります。

+ **名前** - 名前は、拡張機能パッケージ プロジェクトの **PackageName** と一致している必要があります。 名前は、POS 拡張機能パッケージの検索および読み込みのために使用され、値は正確に一致している必要があります。
+ **発行元** - 発行元は、拡張機能パッケージの manifest.json で指定されている発行元と一致している必要があります。

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
