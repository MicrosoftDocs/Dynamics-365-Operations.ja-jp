---
title: 独立したパッケージ モデルへの POS 拡張機能の移行
description: このトピックでは、POS 拡張機能を独立したパッケージ モデルに移行する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 8697827511f0d7247b934cc960faaa92757a9e90
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984292"
---
# <a name="migrate-a-pos-extension-to-the-independent-packaging-model"></a>独立したパッケージ モデルへの POS 拡張機能の移行

[!include [banner](../../../includes/banner.md)]

このトピックは、Retail SDK バージョン 10.0.18 以降に適用されます。

Retail SDK の独立したパッケージ モデルは、Dynamics 365 Commerce 拡張機能の開発のための更新および改善された開発者エクスペリエンスを提供します。 Retail SDK の独立したパッケージ モデルは、Retail SDK モデルと開発中の拡張機能との間に、より大きな分離を生じさせます。 SDK は、Commerce 開発を可能にするアーティファクトを含む一連の NuGet パッケージで構成されています。 独立したパッケージ モデルの変更範囲により、必要な変更がいくつかあります。 独立したパッケージ モデルを使用するようにカスタマイズを変更するには、標準のバージョン更新よりも少し手間のかかるコード移行が必要です。 このトピックでは、独立したパッケージ モデルの利点と変更について説明します。 また、既存の販売時点管理 (POS) 拡張機能を独立したパッケージ モデルに変換するための高レベルの一連の手順も示します。

## <a name="benefits-of-the-independent-packaging-model-in-the-retail-sdk"></a>Retail SDK の独立したパッケージ モデルの利点

### <a name="no-code-merge-required-when-updating-to-the-latest-version"></a>最新バージョンへの更新時のコード マージが不要

Retail SDK の以前のバージョンでは、デザインと配分方法を使用するために、コードをマージして最新バージョンの Commerce コンポーネントに更新する必要がありました。 コード マージは時間のかかるアップグレード プロセスであり、Retail SDK 全体をリポジトリに維持し、コア POS.App プロジェクトをコンパイルする必要があります。 独立したパッケージ モデルを使用する場合は、拡張機能のみを維持する必要があります。 最新の Retail SDK への更新は、プロジェクトが使用している NuGet パッケージ バージョンの更新のように簡単です。

### <a name="simplified-consumption-of-custom-headless-commerce-apis"></a>カスタム ヘッドレス Commerce API の消費の簡略化

Retail SDK の以前のバージョンの別の問題点は、販売時点管理でヘッドレス Commerce API を使用するために必要な TypeScript の生成でした。 独立したパッケージ モデルを使用すると、このプロセスが簡素化され、データ サービスの要求とエンティティの TypeScript コードが自動的に生成されます。 POS 用の TypeScript プロキシは、POS 拡張プロジェクトをビルドするときに自動的に作成されるため、CommerceProxyGenerator を手動で実行してファイルをコピーする必要がなくなります。

### <a name="automated-packaging-and-configuration-of-commerce-runtime-and-hardware-station-extensions-for-mpos"></a>MPOS 用 Commerce Runtime および Hardware Station 拡張機能の自動パッケージとコンフィギュレーション

独立したパッケージ モデルのもう 1 つの改善点は、コンフィギュレーションとパッケージの多くが自動化され、ソリューションのビルド時に自動的に生成されることです。 例として、オフライン用および専用ハードウェア ステーション用の拡張コンフィギュレーション ファイルの自動生成の 2 つがあげられます。 オフラインおよび専用ハードウェア ステーションのアセンブリも、ビルド中に自動的に MPOS パッケージに含まれるため、手動で **Customization.settings** ファイルを更新する必要はありません。

### <a name="improved-build-times"></a>ビルド時間の短縮

独立したパッケージ モデルを使用する場合、配置可能なパッケージを生成するには、Commerce 拡張ソリューションをビルドするだけで済みます。 この設計により、拡張機能の開発およびパッケージの際のビルド時間が大幅に短縮されます。

### <a name="modern-pos-framework-and-system-requirement-changes"></a>Modern POS フレームワークおよびシステム要件の変更

Modern POS が独立したパッケージ モデルをサポートするために、POS フレームワークは Microsoft Windows オプション パッケージ拡張モデルを使用するように拡張されています。 Modern POS とオプション パッケージは、一覧に示されている Windows バージョンでのみサポートされます。

+ Windows 10 バージョン 1809 以降
+ Windows Server 2019 またはそれ以降

## <a name="pos-api-and-sdk-changes"></a>POS API と SDK の変更

### <a name="removal-of-posuisdk-library"></a>Pos.UI.Sdk ライブラリの削除

独立したパッケージ モデルへの移行により、**Knockout.js** に依存していた **Pos.UI.Sdk** ライブラリが削除されました。 代わりに、拡張機能内で POS コントロールを使用するための、ライブラリに依存しないデザインがあります。 このモデルでは、アプリケーション全体で一貫した概観を維持しながら、拡張機能の開発時に使用する UI ライブラリを選択できます。 詳細については、[拡張機能での POS コントロール](controls-pos-extension.md)を参照してください。

### <a name="knockoutjs-changes"></a>Knockout.js の変更

シールドされた拡張性モデルの POS API に対する最大の変更の 1 つは、POS 契約の **Knockout.js** へのすべての参照を削除したことです。

+ POS UI SDK ライブラリは、**PosApi/Consume/Controls** 下の POS コントロール用の **消費** API に置き換えられます。 POS コントロールを使用する拡張機能の開発方法の詳細については、[拡張機能の POS コントロール](controls-pos-extension.md)を参照してください。
+ **knockout.d.ts** ファイルは SDK から削除されたため、グローバル **ko** 変数は、拡張機能で使用できません。 POS 拡張機能で **Knockout.js** を使用するには、[POS 拡張機能での knockout.js の使用](knockout-pos-extension.md)を参照してください。

### <a name="changes-when-creating-a-custom-view"></a><a id="custom-view"></a>カスタム ビュー作成時の変更

拡張ビューを作成する際に、より管理しやすく直感的な方法を提供するために、**ExtensionViewControllerBase** クラスを **CustomViewControllerBase** と呼ばれるカスタム ビューの新しい基本クラスに置き換えました。 新しいクラスは、より管理しやすい方法で同じ機能を提供します。 **ExtensionViewControllerBase** から派生した拡張ビューは、独立パッケージ モデルを使用してサポートされていないため、読み込まれません。 **ExtensionViewControllerBase** と新しい **CustomViewControllerBase** の主な違いは、新しいパッケージ モデルではヘッダーとナビゲーション バーが自動的に表示され、拡張機能の開発エクスペリエンスが簡略化されることです。 詳細については、[POS でのカスタム ビューの作成](custom-pos-view.md)を参照してください。

### <a name="extension-loading-changes"></a>拡張機能の読み込みの変更

個別に配布および提供される拡張パッケージの使用により、読み込むパッケージを検出する方法が変更されました。 POS は読み込むすべての拡張パッケージを一覧表示するために、単一の **extensions.json** ファイルに依存しなくなりました。 この方法は、独立したパッケージ モデルと互換性がありません。 独立したパッケージ モデルでは、POS はヘッドレス コマース エンジンを呼び出して、読み込む必要がある拡張パッケージの一覧を取得します。 詳細については、[拡張パッケージのコンフィギュレーション](pos-extension-basics.md#configuring-extension-packages)を参照してください

## <a name="code-migration-steps"></a>コードの移行手順

既存の POS 拡張機能を、Retail SDK の **Pos.Extensions** プロジェクトから独立したパッケージ モデルに移行するには、次の手順を実行します。

1. [拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md)の手順を完了します。

2. Retail SDK の **Pos.Extensions** プロジェクトから、前の手順で作成したプロジェクトのルート ディレクトリに、拡張機能パッケージ ディレクトリのコンテンツをコピーします。
    + 拡張機能パッケージのソース ファイルのみをコピーし、ソース ディレクトリに存在するビルド コンポーネントを除外します。
    + 完了すると、プロジェクトのルート ディレクトリに **manifest.json** ファイルが表示されます。

3. POS 拡張機能マニフェスト スキーマへの参照を変更します。 これを行うには、**manifest.json** の `$schema` 行 を次のように更新します。

    ```json
    "$schema": "./devDependencies/schemas/manifestSchema.json"
    ```

4. Pos.UI.Sdk を使用する場合にのみ必要: すべての参照を Pos.UI.Sdk ライブラリに変換します。 Pos.UI.Sdk ライブラリは、拡張機能での POS コントロールの使用方法が異なる独立したパッケージではサポートされていません。

    1. Visual Studio で、**PosUISdk** をグローバル検索します。
    2. **PosUISdk** への参照ごとに、POS UI SDK コントロールの使用を、**PosApi/Consume/Controls** からの POS コントロールを使用する新しいアプローチに置き換えます。 これらの更新を行う方法については、[拡張機能の POS コントロール](controls-pos-extension.md)を参照してください。
    3. **PosUISdk** のソリューションを再度検索して、すべての使用が更新されていることを確認します。

5. **Knockout.js** を使用する場合にのみ必要: POS で使用されるグローバル インスタンスに依存する代わりに、拡張機能パッケージに含まれるライブラリのコピーを使用するように、**Knockout.js** へのすべての参照を更新します。 詳細については、[POS 拡張機能での knockout.js の使用](knockout-pos-extension.md)を参照してください。

6. **ExtensionViewControllerBase** へのすべての参照を、**CustomViewControllerBase** に変換します。 詳細については、[カスタム ビュー作成時の変更](#custom-view)を参照してください。

7. POS 拡張機能プロジェクトをビルドし、正常にビルドされたことを確認します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
