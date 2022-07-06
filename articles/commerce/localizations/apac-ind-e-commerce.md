---
title: インド向け e コマース サイト用の商品及びサービス税 (GST) 統合
description: この記事では、インドで使用可能な Microsoft Dynamics 365 Commerce e コマース 機能の概要を示します。 また、機能を設定するためのガイドラインを示します。
author: EvgenyPopovMBS
ms.date: 12/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: v-chgriffin
ms.search.region: India
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2021-12-10
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 78465b4daaf664e2b618b744686b7eeac00b7426
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892786"
---
# <a name="goods-and-services-tax-gst-integration-for-e-commerce-sites-for-india"></a>インド向け e コマース サイト用の商品及びサービス税 (GST) 統合

[!include [banner](../includes/banner.md)]

この記事では、インドで使用可能な Microsoft Dynamics 365 Commerce e コマース 機能の概要を示します。 また、機能を設定するためのガイドラインを示します。 

Dynamics 365 Commerce で使用可能な e コマースの機能に関する詳細については、[e コマース サイトの概要](../online-store-overview.md)を参照してください。 Commerce で商品及びサービス税 (GST) がサポートされる方法の詳細については、[インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合](apac-ind-cash-registers.md)を参照してください。

## <a name="e-commerce-capabilities-for-india"></a>インド向けの e コマースの機能

インド向けの Commerce e コマースの機能は、次の機能を提供します。

- GST は、注文で指定された配送情報および請求書情報に基づく e コマース注文に対しても計算できます。
- GST は、明細行レベルの e コマース注文に含められる出荷費用に対しても計算されます。
- 商品及びサービス税 ID 番号 (GSTIN) または固定勘定番号 (PAN) などの顧客登録番号は、e コマース サイトの顧客プロファイルで指定できます。

### <a name="gst-calculation-for-e-commerce-orders"></a>e コマース注文の GST 計算

e コマース注文の GST 計算は、e コマース サイトの **チェックアウト** ページで指定できる顧客の請求先住所に基づいています。 既定では、注文の出荷先住所が請求先住所として使用されます。 ただし、顧客の他の住所の一覧で請求先住所を選択したり、新しい住所を追加することもできます。

請求書情報に基づく e コマース注文に対する GST 計算を有効にするには、**インドの請求先住所** モジュールをチェックアウト ページに追加する必要があります。 コマース本部の **機能管理** ワークスペースで、**(インド) e コマースの請求先住所に基づいて GST を計算する** 機能を有効にする必要があります。 詳細については、この記事で後述する[インド向けの e コマースの設定](#setting-up-e-commerce-for-india)セクションを参照してください。

### <a name="gst-calculation-for-shipping-charges"></a>出荷費用に対する GST の計算

GST は、注文で選択された配送オプションに基づいて、e コマース注文に追加できる出荷費用に対して計算することもできます。 出荷費用に対する GST の計算も、e コマース注文で指定された請求先住所に基づいています。

> [!NOTE]
> GST の計算は現在、注文明細行レベルの出荷費用でのみサポートされます。 ただし、ヘッダー レベルの出荷費用での GST 計算は、今後の更新で追加される可能性があります。

### <a name="customer-registration-numbers"></a>顧客登録番号

顧客の登録番号および他の情報は、e コマース サイトの **マイ プロファイル** ページで指定できます。 次の登録情報を入力できます。

- PAN。
- GST 登録番号タイプ。 登録番号には、GSTIN、政府機関の固有 ID (GDI)、または固有 ID (UID) 番号があります。
- GST 登録番号。
- ビジネス業種。
- 付加価値税 (VAT) の登録番号。 この番号は、税 ID 番号 (TIN) と呼ばれています。

PAN は顧客プロファイル レベルで指定できます。 他の登録情報は、顧客の住所レベルで指定できます。

顧客プロファイルへの顧客登録情報の入力を有効にするには、**インドの税務登録番号** モジュールを **マイ プロファイル** ページに追加する必要があります。 詳細については、次の[インド向けの e コマースの設定](#setting-up-e-commerce-for-india)セクションを参照してください。

## <a name="setting-up-e-commerce-for-india"></a>インド向けの e コマースの設定

### <a name="prerequisites"></a>必要条件

インド向けの e コマースの機能を設定する前に、Retail Cloud Scale Unit (RCSU)、Commerce オンライン ソフトウェア開発キット (SDK)、および Commerce モジュール ライブラリを含む Commerce 環境を構成する必要があります。 Commerce SDK およびモジュール ライブラリのインストール方法については、[SDK およびモジュール ライブラリの更新プログラム](../e-commerce-extensibility/sdk-updates.md)を参照してください。

### <a name="install-modules"></a>モジュールのインストール

**dynamics365-commerce** フィードで使用可能な次のパッケージは、インド固有のモジュールを含んでいます。

- **@msdyn365-commerce-marketplace/address-extensions** – このパッケージは、**インドの請求先住所** モジュールを含んでいます。
- **@msdyn365-commerce-marketplace/tax-registration-numbers** – このパッケージは、**インド向け税登録番号** モジュールを含んでいます。

ただし、パッケージはそのフィードの一部ですが、異なる名前空間の下にあります。 したがって、名前空間のレジストリ エントリを追加するには、次の手順に従う必要があります。

1. **.npmrc** ファイルを更新して、次のレジストリ エントリが含まれるようにします (エントリの変更が含まれていない場合)。

    `@msdyn365-commerce-marketplace:registry=https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/`

1. **.yarnrc** ファイルを更新して、次のレジストリ エントリが含まれるようにします (エントリの変更が含まれていない場合)。

    `"@msdyn365-commerce-marketplace:registry" "https://pkgs.dev.azure.com/commerce-partner/Registry/_packaging/dynamics365-commerce/npm/registry/"`
    
ローカル環境にパッケージをインストールするには、コマンド プロンプトから次のコマンドを実行します。 このコマンドは、依存関係が含まれるように **package.json** ファイルを自動的に更新します。

```bash
yarn add @msdyn365-commerce-marketplace/address-extensions
yarn add @msdyn365-commerce-marketplace/tax-registration-numbers
```

**package.json** ファイルでは、パッケージのバージョンを特定のバージョンに更新します。

> [!IMPORTANT]
> - すべての機能が期待どおりに機能するように、パッケージのバージョンはモジュール ライブラリのバージョンと一致している必要があります。 
> - Commerce モジュール ライブラリと SDK の最小バージョンは 10.0.23 (9.33) である必要があります。 

### <a name="pull-updates-and-validate"></a>更新をプルして検証する

最新の SDK、モジュール ライブラリ、および他の依存関係の更新をプルする方法については、[更新をプルする](../e-commerce-extensibility/sdk-updates.md#pull-updates)を参照 してください。

最新の依存関係がプルダウンされたら、**yarn start** コマンドを実行して開発環境でノード サーバーを起動し、新しいモジュールをテストすることができます。 アプリケーションをローカルで参照します (たとえば、`https://localhost:4000`)。

### <a name="build-your-site"></a>サイトを構築します

インド固有のモジュールを、e コマース サイトの次のページに追加する必要があります。

- **インドの請求先住所** モジュールをチェックアウトのページに追加します。
- **インドの税務登録番号** モジュールを **マイ プロファイル** ページに追加します。

e コマース サイトを作成し、e コマース モジュールを使用する方法の詳細については、[e コマース サイトの作成](../create-ecommerce-site.md)と[モジュール ライブラリの概要](../starter-kit-overview.md)を参照してください。

### <a name="configure-gst-for-e-commerce"></a>e コマースの GSTを構成する

Commerce の GST を構成する方法の詳細については、[インドのキャッシュ レジスターの配置ガイドライン](apac-ind-loc-deployment-guidelines.md)を参照してください。

コマース本部の **機能管理** ワークスペースで、**(インド) e コマースの請求先住所に基づいて GST を計算する** 機能を有効にする必要があります。
