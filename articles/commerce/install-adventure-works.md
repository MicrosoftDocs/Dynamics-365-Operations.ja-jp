---
title: Adventure Works テーマのインストール
description: このトピックでは、Microsoft Dynamics 365 Commerce で Adventure Works テーマをインストールする方法について説明します。
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9c94dd8ead32f58a25a396376840101d9c2c9b08
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655851"
---
# <a name="install-the-adventure-works-theme"></a>Adventure Works テーマのインストール

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で Adventure Works テーマをインストールする方法について説明します。 

> [!IMPORTANT]
> Adventure Works テーマおよびモジュールは、Dynamics 365 Commerce バージョン 10.0.20 リリースの時点で使用できます。 これらは Microsoft AppSource から入手できます。

## <a name="prerequisites"></a>必要条件

Adventure Works テーマをインストールする前に、Retail Cloud Scale Unit (RCSU)、Commerce オンライン ソフトウェア開発キット (SDK)、および Commerce モジュール ライブラリを含む Dynamics 365 Commerce 環境 (Commerce Version 10.0.20 以降) が必要です。 Commerce SDK およびモジュール ライブラリのインストール方法については、[SDK およびモジュール ライブラリの更新プログラム](e-commerce-extensibility/sdk-updates.md)を参照してください。 

## <a name="installation-steps"></a>インストール手順

### <a name="install-the-adventure-works-theme-in-your-application"></a>アプリケーションに Adventure Works テーマをインストールする

Adventure Works テーマ パッケージは、**dynamics365-commerce** フィードで利用可能です。これは、**@msdyn365-commerce-theme/adventureworks-theme-kit** として利用できます。 ただし、Adventure Works のテーマ パッケージは、そのフィードの一部ですが、異なる名前空間の下です。 したがって、名前空間のレジストリ エントリを追加するには、次の手順に従う必要があります。

1. **.npmrc** ファイルを更新して、次のレジストリ エントリが含まれるようにします (エントリの変更が含まれていない場合)。

    `@msdyn365-commerce-theme:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. **.yarnrc** ファイルを更新して、次のレジストリ エントリが含まれるようにします (エントリの変更が含まれていない場合)。

    `"@msdyn365-commerce-theme:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`  
    
ローカル環境にパッケージをインストールするには、コマンド プロンプトから次のコマンドを実行します。 このコマンドは、依存関係が含まれるように package.json ファイルを自動的に更新します。

`yarn add @msdyn365-commerce-theme/adventureworks-theme-kit`

**package.json** ファイルでは、テーマのバージョンを特定のバージョンに更新します。

> [!IMPORTANT]
> - すべての機能が期待どおりに機能するように、テーマのバージョンはモジュール ライブラリのバージョンと一致している必要があります。 
> - Commerce モジュール ライブラリと SDK の最小バージョンは 10.0.20 (9.31) である必要があります。 

### <a name="add-the-font-files-for-the-adventure-works-theme"></a>Adventure Works テーマのフォント ファイルの追加

アプリケーションに Adventure Works テーマがインストールされた後、必要なフォント ファイルを追加する必要があります。 この手順を完了するには、すべてのフォント ファイルを **\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\public\webfonts** からパートナー アプリケーションのパブリック ディレクトリ パス **\public\webfonts** にコピーします。

### <a name="set-up-the-resources-for-the-adventure-works-theme"></a>Adventure Works テーマのリソースの設定

次に、テーマに必要な既定のリソースを更新します。 この手順を完了するには、**\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks\resources\modules** の下にある global.json ファイルから、**\src\resources\modules** の下にあるパートナー アプリケーション global.json ファイルにコンテンツをコピーします。 **\src\resources** のターゲット・ディレクトリが存在しない場合は、**\node_modules@msdyn365-commerce-theme\adventureworks-theme-kit\src\modules\adventureworks** ソース ディレクトリから **\src** ターゲット ディレクトリに全体をコピーすることができます。

### <a name="pull-updates-and-validate-the-theme"></a>更新をプルしてテーマを検証する

最新の SDK、モジュール ライブラリ、およびその他の依存関係の更新をプルする方法については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#pull-updates)の「プル更新」セクションを参照してください。

最新の依存関係がプルダウンされたら、**yarn start** コマンドを実行して、開発環境でノード サーバーを起動し、新しい Adventure Works テーマをテストできます。 クエリ文字列パラメータ `?theme=adventureworks` (例えば、 `https://localhost:4000/?theme=adventureworks`) を使用してアプリケーションをローカルで参照します。

## <a name="additional-resources"></a>追加リソース

[Adventure Works テーマ](adventure-works-theme.md)

[モジュール ライブラリの概要](starter-kit-overview.md)

[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
