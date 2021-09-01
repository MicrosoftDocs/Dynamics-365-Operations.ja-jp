---
title: 独立したパッケージ モデルへの POS 拡張機能の移行
description: このトピックでは、販売時点管理 (POS) 拡張機能を独立したパッケージ モデルに移行する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 89ac3bce7b1a6fd45b7c6708869f67746a83be834cd5d28faa25dcf3a94e7e07
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762314"
---
# <a name="migrate-a-pos-extension-to-the-independent-packaging-model"></a>独立したパッケージ モデルへの POS 拡張機能の移行

[!include [banner](../../../includes/banner.md)]

このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。

Retail SDK の独立したパッケージ モデルは、Microsoft Dynamics 365 Commerce 拡張機能の開発のための更新および改善された開発者エクスペリエンスを提供します。 独立したパッケージ モデルは、Retail SDK と開発中の拡張機能との間に、より大きな分離を生じさせます。 Retail SDK は、一連の NuGet パッケージで構成されています。 これらのパッケージには、コマース開発を可能にするコンポーネントが含まれています。 独立したパッケージ モデルの変更範囲により、必要な変更がいくつかあります。 独立したパッケージ モデルを使用するようにカスタマイズを変更するには、標準のバージョン更新よりも少し手間のかかるコード移行が必要です。

このトピックでは、独立したパッケージ モデルの利点と変更について説明します。 また、既存の販売時点管理 (POS) 拡張機能を独立したパッケージ モデルに変換するための高レベルの一連の手順も示します。

## <a name="benefits-of-the-independent-packaging-model-in-the-retail-sdk"></a>Retail SDK の独立したパッケージ モデルの利点

### <a name="no-code-merge-is-required-when-you-update-to-the-latest-version"></a>最新バージョンへの更新時のコード マージが不要

Retail SDK の以前のバージョンでは、デザインと配分方法を使用するために、コードをマージして最新バージョンの Commerce コンポーネントに更新する必要がありました。 コード マージは時間のかかるアップグレード プロセスであり、Retail SDK 全体をリポジトリに維持し、コア **POS.App** プロジェクトをコンパイルする必要があります。 独立したパッケージ モデルを使用して、拡張機能のみを維持する必要があります。 Retail SDK 最新バージョンに更新するプロセスは、プロジェクトで消費する NuGet パッケージのバージョン更新と同様に簡単です。

### <a name="simplified-consumption-of-custom-headless-commerce-apis"></a>カスタム ヘッドレス Commerce API の消費の簡略化

Retail SDK の以前のバージョンでは、TypeScript プロキシの生成には POS でヘッドレス コマース API を使用する必要がありました。 独立したパッケージ モデルを使用すると、データ サービス要求とエンティティの TypeScript コードが自動的に生成されます。 そのため、このプロセスの方が簡単です。 POS 用の TypeScript プロキシは、POS 拡張プロジェクトをビルドするときに自動的に作成されるため、CommerceProxyGenerator を手動で実行してファイルをコピーする必要がなくなります。

### <a name="automated-packaging-and-configuration-of-commerce-runtime-and-hardware-station-extensions-for-modern-pos"></a>Modern POS 用 Commerce runtime および Hardware station 拡張機能の自動パッケージとコンフィギュレーション

独立したパッケージ モデルでは、コンフィギュレーションとパッケージの多くが自動化され、ソリューションのビルド時に自動的に生成されます。 たとえば、オフライン用および専用ハードウェア ステーション用の拡張コンフィギュレーション ファイルは自動的に生成されます。 また、ビルドの際には、オフライン用および専用のハードウェア ステーションのアセンブリが自動的に Modern POS パッケージに含まれます。 したがって、手動で **Customization.settings** ファイルを更新する必要はありません。

### <a name="improved-build-times"></a>ビルド時間の短縮

独立したパッケージ モデルでは、配置可能パッケージを生成するには、Commerce 拡張ソリューションをビルドするだけで済みます。 この設計により、拡張機能の開発およびパッケージの際のビルド時間が大幅に短縮されます。

### <a name="modern-pos-framework-and-system-requirement-changes"></a>Modern POS フレームワークおよびシステム要件の変更

Modern POS が独立したパッケージ モデルをサポートするために、POS フレームワークは Windows オプション パッケージ拡張モデルを使用するように拡張されています。 Modern POS とオプション パッケージは、次に示す Windows バージョンでのみサポートされます。

+ Windows 10 バージョン 1809 以降
+ Windows Server 2019 またはそれ以降

## <a name="pos-api-and-sdk-changes"></a>POS API と SDK の変更

### <a name="removal-of-the-posuisdk-library"></a>Pos.UI.Sdk ライブラリの削除

独立したパッケージ モデルへの移行中に、Microsoft は **Knockout.js** に依存していた **Pos.UI.Sdk** ライブラリが削除されました。 代わりに、拡張機能内で POS コントロールを使用するための、ライブラリに依存しないデザインがあります。 拡張機能を開発する際に、使用するユーザー インターフェイス (UI) ライブラリを選択できます。 同時に、アプリケーション全体で一貫した概観を維持できます。 詳細については、[拡張機能での POS コントロールの使用](controls-pos-extension.md)を参照してください。

### <a name="knockoutjs-changes"></a>Knockout.js の変更

シールドされた拡張性モデルの POS API に対する最大の変更の 1 つは、POS 契約の **Knockout.js** へのすべての参照を削除したことです。

+ POS UI SDK ライブラリは、POS コントロール用の **消費** API に置き換えられます。 これらの API は、**PosApi/Consume/Controls** で確認できます。 POS コントロールを使用する拡張機能の開発方法の詳細については、[拡張機能の POS コントロールの使用](controls-pos-extension.md)を参照してください。
+ **knockout.d.ts** ファイルは、SDK から削除されました。 そのため、グローバル **ko** 変数は、拡張機能で使用できません。 POS 拡張機能で **Knockout.js** を使用する方法については、[POS 拡張機能で Knockout.js を使用する](knockout-pos-extension.md)を参照してください。

### <a name="changes-when-you-create-a-custom-view"></a><a id="custom-view"></a>カスタム ビュー作成時の変更

拡張ビューの作成プロセスを、より管理しやすく直感的な方法にするために、Microsoft は **ExtensionViewControllerBase** クラスを **CustomViewControllerBase** と呼ばれるカスタム ビューの新しい基本クラスに置き換えました。 新しいクラスは、同じ機能を、より管理しやすい方法で提供します。 独立パッケージモデルでは、**ExtensionViewControllerBase** から派生した拡張ビューはサポートされていないため、読み込まれません。 新しい **CustomViewControllerBase** と **ExtensionViewControllerBase** クラスの主な違いは、独立したパッケージモデルを使用すると、ヘッダーとナビゲーション バーが自動的に表示されることです。 そのため、拡張機能の開発エクスペリエンスが簡略化されます。 詳細については、[POS でのカスタム ビューの作成](custom-pos-view.md)を参照してください。

### <a name="extension-loading-changes"></a>拡張機能の読み込みの変更

個別に配布および提供される拡張パッケージを使用すると、POS は単一の **extensions.json** ファイルに依存して、読み込む必要のあるすべての拡張パッケージを一覧表示します。 ただし、この方法は、独立したパッケージ モデルと互換性がありません。 独立したパッケージ モデルでは、POS はヘッドレス コマース エンジンを呼び出して、読み込む必要がある拡張パッケージの一覧を取得します。 詳細については、[拡張パッケージのコンフィギュレーション](pos-extension-basics.md#configuring-extension-packages)を参照してください。

## <a name="code-migration-steps"></a>コードの移行手順

既存の POS 拡張機能を、Retail SDK の **Pos.Extensions** プロジェクトから独立したパッケージ モデルに移行するには、次の手順を実行します。

1. [拡張機能パッケージ プロジェクトの作成](create-pos-extension-package.md)の手順に従います。
2. Retail SDK の **Pos.Extensions** プロジェクトから、前の手順で作成したプロジェクトのルート ディレクトリに、拡張機能パッケージ ディレクトリのコンテンツをコピーします。

    + 拡張機能パッケージのソース ファイルのみをコピーします。 ソース ディレクトリに存在する可能性があるビルド コンポーネントを除外します。
    + 完了すると、プロジェクトのルート ディレクトリに **manifest.json** ファイルが表示されます。

3. **manifest.json** ファイルで、次に示すように `$schema` 行を更新して、POS 拡張機能マニフェスト スキーマの参照を変更します。

    ```json
    "$schema": "./devDependencies/schemas/manifestSchema.json"
    ```

4. **Pos.UI.Sdk を使用する場合にのみ必要:** すべての参照を **Pos.UI.Sdk** ライブラリに変換します。 独立したパッケージ モデルは **Pos.UI.Sdk** ライブラリをサポートしていませんが、拡張機能で POS コントロールを使用する別の方法があります。

    1. Visual Studio で、ソリューションの **PosUISdk** をグローバル検索します。
    2. **PosUISdk** への参照ごとに、POS UI SDK コントロールの使用を、**PosApi/Consume/Controls** からの POS コントロールを使用する新しいアプローチに置き換えます。 この手順を完了する方法については、[拡張機能で POS コントロールを使用する](controls-pos-extension.md)を参照してください。
    3. **PosUISdk** をもう一度グローバル検索して、POS UI SDK コントロールの全ての使用が置き換えられたことを確認します。

5. **Knockout.js を使用する場合にのみ必要:** **Knockout.js** へのすべての参照を更新して、POS で使用されるグローバル インスタンスの代わりに、拡張機能パッケージに含まれるライブラリのコピーを使用するようにします。 詳細については、[POS 拡張機能での Knockout.js の使用](knockout-pos-extension.md)を参照してください。
6. **ExtensionViewControllerBase** へのすべての参照を、**CustomViewControllerBase** に変換します。 詳細については、このトピックで前述の[カスタム ビュー作成時の変更](#custom-view)セクションを参照してください。
7. POS 拡張機能プロジェクトをビルドし、正常にビルドされたことを確認します。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
