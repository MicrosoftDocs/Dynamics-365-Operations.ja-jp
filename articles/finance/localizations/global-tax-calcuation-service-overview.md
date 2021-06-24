---
title: 税の計算 (プレビュー)
description: このトピックでは、税計算機能の全体的な範囲と機能について説明します。
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184104"
---
# <a name="tax-calculation-preview"></a>税の計算 (プレビュー)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

税計算は、Global Tax Engine によって税の決定と計算プロセスを自動化および簡素化できる、超スケーラブルなマルチテナント サービスです。 税エンジンは完全にコンフィギュレーション可能です。 設定できる要素には、課税対象データ モデル、税コード、課税適用マトリックス、および税金計算式が含まれますが、これに限定されません。 税エンジンは  Microsoft Azureコア サービス プラットフォームで実行され、最新のテクノロジと指数関数的なスケーラビリティを提供します。

税計算は、Dynamics 365 Finance および Dynamics 365 Supply Chain Management と統合されます。 最終的には、Dynamics 365 Project Operations、Dynamics 365 Commerce やその他のファースト パーティ アプリケーションとも統合されます。

> [!IMPORTANT]
> Tax Calculation サービスを有効にした場合、サービス データを管理するデータ センター以外のデータ センターで、関連データに対する一部の操作が実行される場合があります。 税計算サービスを有効にする前に、[条件](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) を確認してください。 Microsoft にとってお客様のプライバシーは重要です。 詳細については、Microsoft [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=521839)をお読みください。

税計算は、指数関数的なスケーラビリティを提供するマイクロサービス ベースの税エンジンです。 実行できるスケジューリング タスクは次のとおりです。

- Regulatory Configuration Service (RCS) を通じて税計算を構成します。 RCS は、電子レポート (ER) デザイナの拡張バージョンであり、スタンドアロンのサービスとして利用できます。
- 税マトリックスを構成して、税コードと税率を自動的に決定します。
- 税マトリックスを構成して、税登録番号を自動的に決定します。
- フォーミュラと条件を定義するには、税計算デザイナーを構成します。
- 税の決定および計算ソリューションを、複数の法人間で共有します。

税計算サービスを使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトから税計算サービス アドインをインストールします。 その後、RCS の設定を完了し、Finance および Supply Chain Management の税計算サービスを有効にしてください。 詳細については、[税サービスの使用を開始する](./global-get-started-with-tax-calculation-service.md)を参照してください。

## <a name="availability"></a>適用の対象

税計算は、パブリック プレビュー プログラムを通じて、選択した顧客および複数の税金環境でのみ使用できます。 最終的には、一般にすべての顧客および運用環境で使用できます。

引き続き新しい機能が提供されるため、サポートされる機能の補充と範囲について把握するために最新のドキュメントをチェックしてください。

税計算は、次の Azure 地域に配置されます。 また、顧客のニーズに基づいて、より多くの Azure 地域にもデプロイされます。

- 米国
- ヨーロッパ

> [!NOTE]
> 税計算は、Dynamics 365 のオンプレミス デプロイメントをサポートしません。 また、Dynamics 2012 AX などの以前のバージョンはサポートされていません。

## <a name="feature-highlights"></a>機能の特徴

- 税を自動的に決定する構成可能な税マトリックス
- 複数の税登録番号のサポート
- 税の決定と計算のための移動オーダーのサポート
- 複数の税登録番号の決定のための移動オーダーのサポート

## <a name="supported-transactions"></a>サポートされるトランザクション

税計算は、法人およびトランザクション別に有効にできます。 次のトランザクションがサポートされています。

- 販売プロセス

    - 販売見積
    - 販売注文
    - 確認書
    - ピッキング リスト
    - 梱包明細
    - 売上請求書
    - 訂正票
    - 返品注文
    - ヘッダー雑費
    - 明細行の雑費

- 購入プロセス

    - 発注書
    - 確認書
    - 入庫リスト
    - 製品受領書
    - 仕入請求書
    - ヘッダー雑費
    - 明細行の雑費
    - 訂正票
    - 返品注文
    - 購買要求
    - 購買要求明細行の雑費
    - 見積依頼
    - 見積依頼ヘッダーの雑費
    - 見積依頼行の雑費

- 在庫プロセス

    - 移動オーダー - 出荷
    - 移動オーダー - 入庫

## <a name="related-resources"></a>関連するリソース

[税サービスの使用を開始する](./global-get-started-with-tax-calculation-service.md)

[複数の VAT 登録番号](./emea-multiple-vat-registration-numbers.md)

[移動オーダーに対する税機能のサポート](./tasks/tax-feature-support-for-transfer-order.md)

[税サービスで拡張機能を作成する方法](./tax-service-add-data-fields-tax-integration-by-extension.md)
