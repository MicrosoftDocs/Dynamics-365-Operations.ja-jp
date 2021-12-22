---
title: サウジアラビア向け QR コードの生成とレシートへの印刷
description: このトピックでは、Microsoft Dynamics 365 Commerce でサウジアラビアで使用できる QR コードを印刷するための機能の概要を説明します。
author: EvgenyPopovMBS
manager: annbe
ms.date: 11/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.region: Saudi Arabia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2021-11-04
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 621b2558e9347638bba63b96ddc7d08cb63e3e1f
ms.sourcegitcommit: 93cc9823016c9f2fd568ada0b670a52c8c3bfa33
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2021
ms.locfileid: "7864245"
---
# <a name="generate-qr-codes-and-print-them-on-receipts-for-saudi-arabia"></a>サウジアラビア向け QR コードの生成とレシートへの印刷

[!include[banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce でサウジアラビアで使用できる QR コードを印刷するための機能の概要を説明します。

サウジアラビアに通常の住所を持つ法人にリンクされている店舗では、ユーザーは現金払いトランザクションまたは販売注文トランザクションのレシートに QR コードを印刷できます。 QR コードには、次の情報が含まれます。

| 順番 | フィールド                                                    | データ ソース |
|----------| ---------------------------------------------------------|-------------|
| 1        | 会社名                                             | 法人の名前 |
| 2        | 会社の VAT 登録番号                          | 法人の税登録番号 |
| 3        | トランザクションの日時                             | 小売用店舗トランザクションの日時 |
| 4        | 合計受領額 (付加価値税 \[VAT\] を含む) | 小売店舗トランザクションの合計金額 |
| 5        | レシートに含まれる VAT の合計金額                  | 小売店舗トランザクションに係る税額の合計額 |

> [!NOTE]
> 顧客注文トランザクションの作成時に、合計受領額は、配送実行モードを使用するすべてのトランザクション明細行の合計金額を加算して計算されます。

QR コードは、base64 変換をタグ長値 (TLV) 形式でエンコードされたトランザクション情報に適用することによって生成されます。 ザカート・税・税関庁 (ZATCA) は、QR コードの検証に使用できるツールを提供します。 電子請求書発行の要件および QR コード検証機能の詳細については、[ZATCA の電子請求書ポータル](https://zatca.gov.sa/en/E-Invoicing/Pages/default.aspx)を参照してください。

## <a name="set-up-qr-codes"></a>QR コードの設定

QR コードを生成してサウジアラビア向けのレシートにを印刷するには、次のタスクを行う必要があります。

1. カスタム フィールドを設定して、販売レシートのレシート形式で使用できるようにします。
1. レシート形式を設定します。
1. コマース パラメーターで、QR コード分析コードを指定します。
1. Commerce runtime (CRT) 拡張機能を有効にします。

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>カスタム フィールドを設定して、販売レシートのレシート形式で使用できるようにする

販売時点管理 (POS) レシート形式で使用される言語テキストおよびカスタム フィールドを構成することができます。 **言語テキスト** ページで、レシート レイアウト用のカスタム フィールドのラベルに次のレコードを追加します。 テーブルに表示されている **言語 ID**、**テキスト ID**、および **テキスト** の値は、単なる例に過ぎません。 要件に合わせてそれらを変更できます。 ただし、使用する **テキスト ID** の値は一意である必要があり、900001 以上である必要があります。

| 言語 ID | テキスト ID | テキスト         |
|-------------|---------|--------------|
| ja       | 900001  | QR コード (SA) |

> [!NOTE]
> レシート設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。 または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。

**カスタム フィールド** ページで、レシート レイアウトのカスタム フィールドに次のレコードを追加します。 **キャプション テキスト ID** の値は、**言語テキスト** ページで指定した **テキスト ID** の値に対応している必要があることに注意してください。

| Name             | 種類    | キャプション テキスト ID |
|------------------|---------|-----------------|
| INVOICEQRCODE_SA | 受信 | 900001          |

### <a name="configure-receipt-formats"></a>レシート形式を設定する

必要なレシート形式ごとに、**印刷動作** フィールドを **常に印刷** にします。

レシート形式デザイナーで、レシートの **フッター** セクションに、次のカスタム フィールドを追加します。 フィールド名は、前のセクションで定義した言語テキストに対応していることに注意してください。

- **QR コード (SA)** – このフィールドは、QR コードをレシートに印刷します。

レシート形式の使用方法の詳細については、[レシート形式の設定とデザイン](../receipt-templates-printing.md)を参照してください。

### <a name="specify-qr-code-dimensions-in-commerce-parameters"></a>コマース パラメーターで、QR コード分析コードを指定する

コマース パラメーター ページの **コンフィギュレーション パラメーター** タブで、次のコンフィギュレーション パラメーターを追加します。

- **QrCodeWidth** - ピクセル単位の QR コード画像の幅。 パラメーターに適切な値を指定します。
- **QrCodeHeight** - ピクセル単位の QR コード画像の高さ。 パラメーターに適切な値を指定します。

> [!NOTE]
> レシートに QR コードを印刷するには、これらのコンフィギュレーション パラメーターの値を指定する必要があります。 パラメーターの既定値のサポートは、今後のアップデートで追加される可能性があります。

### <a name="enable-crt-extensions"></a>CRT 拡張機能の有効化

> [!WARNING]
> [新しい独立した梱包および拡張モデル](../dev-itpro/build-pipeline.md)の制限により、現在、このローカライズ機能は使用できません。 Microsoft Dynamics Lifecycle Services (LCS) の開発者仮想マシン (VM) で、Retailソフトウェア開発キット (SDK) の以前のバージョンを使用する必要があります。 (Microsoft は今後のバージョンの新しい独立した梱包および拡張機能モデルに、ローカライズ機能のサポートを追加する予定です。)

#### <a name="development-environment"></a>開発環境

次の手順に従って開発環境を設定し、ローカライズ機能をテストし、拡張できるようにします。

1. CRT 用拡張コンフィギュレーション ファイルを検索します。

    - **Retail サーバー:** ファイル名は **commerceruntime.ext.config** で、インターネット インフォメーション サービス (IIS) Retail サーバー サイトの場所にある **bin\\ext** フォルダーにあります。
    - **Modern POS 上のローカル CRT:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーがある場所にあります。

1. 次の例に示すように、拡張コンフィギュレーション ファイルに CRT 変更を登録します。

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSaudiArabia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
    ```

#### <a name="production-environment"></a>実稼働環境

以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。

1. **RetailSdk\\Assets** フォルダーの下の **commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** パッケージ コンフィギュレーション ファイルで、以下の行を **合成** セクションに追加します。

    ``` xml 
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSaudiArabia" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
    ```

1. Visual Studio ユーティリティ用の MSBuild コマンド プロンプトを起動し、Retail SDK フォルダーの下で **msbuild** を実行し、配置可能なパッケージを作成します。
1. LCS 経由または手動でパッケージを適用します。 詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。
