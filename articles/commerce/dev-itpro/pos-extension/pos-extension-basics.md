---
title: POS 拡張機能の基本
description: この記事では、販売時点管理 (POS) 拡張機能の基本的な概念について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 3711f40c52521c325eabd594b8e783b5a2f9d735
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885568"
---
# <a name="pos-extension-basics"></a>POS 拡張機能の基本

[!include [banner](../../../includes/banner.md)]

この記事では、販売時点管理 (POS) 拡張機能の基本的な概念について説明します。 Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

拡張機能の開発者は POS API ライブラリを使用してカスタマイズを作成することができます。 POS API により、POS のビジネス ロジックおよびユーザー インターフェイス (UI) レイヤーの両方をカスタマイズできます。

## <a name="terminology"></a>用語

次の条件がこの記事で使用されます。

| 相談 | 定義 | 例 |
|---|---|---|
| 拡張ポイント | POS を拡張できる特定の場所、または POS に新しい機能を追加する技術。 | <p>**PreOperationTrigger** 呼び出しのポイント</p><p>新しいビューの追加</p> |
| 内線 | 特定の拡張ポイントを使用して POS をカスタマイズするのに役立つ個々のコンポーネント。 | <p>新しい操作</p><p>新しいビュー</p><p>**PreOperationTrigger** の実装</p> |
| 拡張パッケージ | 組み合わせた場合に、カスタマイズされたエンド ツー エンド POS シナリオを有効にする一連の拡張機能。 | 新しいビューを開く操作を含むパッケージ |

## <a name="types-of-extensions"></a>拡張機能のタイプ

POS 拡張機能は 2 つのタイプに分類できます。

+ 拡張機能の *拡張* とは、既存のページまたはワークフローを変更することにより POS の機能を変更することです。
+ 拡張機能の *作成* は POS を補完し、新しいページまたはワークフローを導入して新しい機能を作成します。

*拡張* 拡張機能と *作成* 拡張機能の違いは、POS 拡張機能フレームワークを通して組み込まれることです。 拡張機能を開発する場合、「既存の POS コンポーネントを拡張するか、または全く新しい機能を作成するか?」について考えることは役立ちます。

## <a name="pos-api-library"></a>POS API ライブラリ

POS API ライブラリには、拡張機能のモジュール使用方法に基づいて編成された一連のモジュールが含まれています。

+ **拡張**

    + これらのモジュールは、拡張機能が POS コンポーネントおよびワークフローを拡張するのに役立ちます。
    + サブディレクトリは、拡張するコンポーネントのタイプに基づいてまとめられた後、拡張する機能領域に基づいてまとめられます。
    + **PosApi/Extend/Views/CustomerDetailsView**、**PosApi/Extend/Triggers/ProductTriggers** などがその例です。

+ **新規**

    + 拡張機能を支援するモジュールにより、新しいコンポーネントおよび機能が作成されます。
    + サブディレクトリは、作成するコンポーネントのタイプに基づいて編成されます。
    + その一例として、**PosApi/Create/Views** が挙げられます。

+ **消費**

    + これらのモジュールにより、POS 機能を実行するための拡張機能が使用できるようになります。

POS API ライブラリの API の完全な一覧とモジュールのタイプの宣言については、**Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージと共に配布される **Pos.Api.d.ts** ファイルを参照してください。

## <a name="manifestjson-file"></a>Manifest.json ファイル

各拡張機能パッケージは、**manifest.json** ファイルを拡張機能パッケージのルート ディレクトリ内に格納している必要があります。 このマニフェスト ファイルには、拡張機能パッケージに関する重要な情報が含まれており、パッケージに含まれる拡張機能の一覧を定義しています。 マニフェスト ファイルは、**Microsoft.Dynamics.Commerce.Sdk.Pos** NuGet パッケージで提供されるマニフェスト スキーマに従う必要があります。 そうしない場合、POS は拡張機能を読み込めません。

### <a name="fields"></a>フィールド

マニフェスト ファイルには次のフィールドが含まれます。

+ **名前** – 拡張機能パッケージの名前です。
+ **説明** – 拡張機能パッケージの機能の説明です。
+ **発行元** – 拡張機能パッケージの発行元または組織の名前です。
+ **バージョン** – 拡張機能パッケージのバージョンです。 バージョンは、セマンティック バージョニング パターンに従う必要があります。
+ **minimumPosVersion** – 拡張機能パッケージを実行するために必要な最小 POS バージョンです。 バージョン番号は、消費している POS NuGet パッケージと、インストールされた POS アプリによって異なります。 たとえば、拡張機能プロジェクトでは、インストールされている POS アプリよりも古いバージョンから、POS API または 拡張機能アーティファクトを使用しないでください。 ランタイムに、POS アプリは拡張機能パッケージのバージョンを確認します。 インストールされた POS アプリよりも古いバージョンの場合、拡張機能パッケージは読み込まれません。
+ **supportedCountryRegions** – 拡張機能パッケージを読み込む国または地域コードのオプションのリスト。 このフィールドに値が指定されていない場合、POS の現在の国や地域に関係なく、拡張機能パッケージが読み込まれます。
+ **コンポーネント** – 拡張機能パッケージに含まれている拡張機能の一覧。

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

各 POS 拡張機能には、1 つ以上の TypeScript モジュールが含まれます。 拡張機能クラスは、POS API から公開され、適用される基本クラスから継承する必要があります。 POS API のコンポーネントとタイプは、次の例に示すように、POS API モジュールの相対的でないインポートを使用して、拡張モジュールにインポートできます。

```JavaScript
import { ApplicationStartTrigger } from "PosApi/Extend/Triggers/ApplicationTriggers";
```

次の例に示すように、各拡張モジュールには拡張クラスの既定のエクスポートを 1 つ含める必要があります。

```JavaScript
import { ApplicationStartTrigger } from "PosApi/Extend/Triggers/ApplicationTriggers";
export default class MyCustomApplicationStartTrigger extends ApplicationStartTrigger {
    public execute(options): Promise<void> {
        return Promise.resolve();
    }
}
```

### <a name="configuring-extension-packages"></a>拡張機能パッケージのコンフィギュレーション

POS は、**GetExtensionPackageDefinitions** API を呼び出すことにより、ヘッドレス Commerce エンジンから構成された拡張機能パッケージの定義の一覧を読み込みます。 **GetExtensionPackageDefinitions** API は、**GetExtensionPackageDefinitions** Commerce Runtime (CRT) 要求を実行します。 拡張機能パッケージを読み込むように POS を構成するには、次の例に示されているように、CRT トリガーを **GetExtensionPackageDefinitionsRequest** に追加し、拡張機能パッケージの定義を **GetExtensionPackageDefinitionsResponse** 内にある定義の一覧に追加します。

**ExtensionPackageDefinition** のフィールドは、POS 拡張機能パッケージを作成するときに使用した値と一致している必要があります。

+ **名前** – 名前を使用して、POS 拡張機能パッケージを検索して読み込みます。 したがって、拡張機能パッケージ プロジェクトの **PackageName** 値と完全に一致する必要があります。 
+ **発行元** – 発行元は、拡張機能パッケージの **manifest.json** ファイルで指定されている発行元と一致する必要があります。

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
