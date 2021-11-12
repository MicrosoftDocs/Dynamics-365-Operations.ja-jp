---
title: 税の計算の概要
description: このトピックでは、税計算機能の全体的な範囲と機能について説明します。
author: wangchen
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: caa7e458763b6ba6b2b85ab016a1aa2e53cee89a
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647060"
---
# <a name="tax-calculation-overview"></a>税の計算の概要

[!include [banner](../includes/banner.md)]

税計算は、Global Tax Engine によって税の決定と計算プロセスを自動化および簡素化できる、超スケーラブルなマルチテナント サービスです。 税エンジンは完全にコンフィギュレーション可能です。 設定できる要素には、課税対象データ モデル、税コード、課税適用マトリックス、および税金計算式が含まれますが、これに限定されません。 税エンジンは  Microsoft Azureコア サービス プラットフォームで実行され、最新のテクノロジと指数関数的なスケーラビリティを提供します。

税計算は、Dynamics 365 Finance および Dynamics 365 Supply Chain Management と統合されます。 最終的には、Dynamics 365 Project Operations、Dynamics 365 Commerce やその他のファースト パーティ アプリケーションとも統合されます。

> [!IMPORTANT]
> 税計算を有効にした場合、サービス データを管理するデータ センター以外のデータ センターで、関連データに対する一部の操作が実行される場合があります。 税計算を有効にする前に、[条件](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) を確認してください。 Microsoft にとってお客様のプライバシーは重要です。 詳細については、Microsoft [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=521839)をお読みください。

税計算は、指数関数的なスケーラビリティを提供し、次のタスクの実行に役立つマイクロサービス ベースの税エンジンです。

- 拡張決定メカニズムを介して、正しい消費税グループ、品目消費税グループ、および税コードを自動的に決定します。
- 1 つの法人で複数の税登録番号をサポートし、課税対象取引の正しい税登録番号を自動的に決定します。
- 移動オーダーの税金の決定、計算、転記、および決済をサポートします。
- 特定の業務要件に対してコンフィギュレーション可能な税計算式および条件を定義します。
- 税金決定および計算ソリューションを法人間で共有して、管理作業を保存し、エラーを回避します。
- 顧客および仕入先の税登録番号の決定をサポートします。
- リスト コードの決定をサポートします。
- 税務署レベルでの税計算パラメータをサポートします。

税計算を使用するには、Microsoft Dynamics Lifecycle Services のプロジェクトから税計算アドインをインストールします。 その後、[Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) の設定を完了し、Finance および Supply Chain Management の税計算を有効にしてください。 詳細については、[税サービスの使用を開始する](global-get-started-with-tax-calculation-service.md)を参照してください。

## <a name="availability"></a>適用の対象

税計算は、バージョン 10.0.21 以降、すべての顧客が運用環境で一般的に利用できます。

新しい機能は、引き続き提供されます。 サポートされる機能の補充と範囲について把握するために最新のリリース計画をチェックしてください。

税計算は、次の Azure 地域に配置されます。 顧客のニーズに基づいて、Azure の地域がさらに追加されます。

- アジア太平洋
- オーストラリア
- カナダ
- ヨーロッパ
- 日本
- 英国
- 米国

> [!NOTE]
> 税計算は、Dynamics AX 2012 などの以前のバージョンの Dynamics 365、または Dynamics 365 のオンプレミス配置をサポートしていません。

## <a name="data-flow"></a>データ フロー

次に、税計算のデータ フロー プロセスの概要を示します。 

1. RCS では、課税対象ドキュメント モデル コンフィギュレーションとモデル マッピング コンフィギュレーションを表示およびインポートします。 より高度なシナリオに対してコンフィギュレーションを拡張する必要がある場合は、[税コンフィギュレーションのデータ フィールドの追加](tax-service-add-data-fields-tax-configurations.md) を参照してください。
2. RCS で、税機能を作成または管理します。 税機能を使用して、税率および税の適用性ルールを管理できます。
3. 税機能の設定が完了したら、RCS の税コンフィギュレーションと税機能をグローバル レポジトリに公開します。
4. Finance で、特定の法人に対して使用する税機能設定のバージョンを選択します。
5. Finance および Supply Chain Management では、トランザクションを通常どおり操作します。 税計算が必要な場合、クライアントはトランザクションから販売注文や発注書などの情報を収集し、情報をペイロードとしてパッケージ化します。 その後、税金を計算する要求が送信されます。
6. 税計算要求がクライアントから受信され、計算が完了します。 税の結果がクライアントに返されます。
7. Dynamics 365 クライアントは税の結果を受け取り、消費税ページに税計算結果を表示します。

## <a name="supported-transactions"></a>サポートされるトランザクション

税計算はトランザクションによって有効にできます。 

次のトランザクションは、バージョン 10.0.21 でサポートされています: 

- 販売注文

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

- 購買

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

- 在庫

    - 移動オーダー - 出荷
    - 移動オーダー - 入庫

次のトランザクションは、バージョン 10.0.23 でサポートされています: 

- 自由書式の請求書

## <a name="supported-countriesregions"></a>サポートされる国/地域

税計算は法人によって有効にできます。 

法人の基本住所に対する次の国/地域は、バージョン 10.0.21 でサポートされています:

- オーストリア
- ベルギー
- デンマーク
- エストニア
- フィンランド
- フランス
- ドイツ
- ハンガリー
- アイスランド
- イタリア
- ラトビア
- リトアニア
- オランダ
- ノルウェー
- ポーランド
- スウェーデン
- スイス
- イギリス
- 米国

法人の基本住所に対する次の国/地域は、バージョン 10.0.22 でサポートされています:

- オーストラリア
- バーレーン
- カナダ
- エジプト
- 香港特別行政区
- クウェート
- ニュージーランド
- オマーン
- カタール
- サウジアラビア語
- 南アフリカ
- アラブ首長国連邦

法人の基本住所に対する次の国/地域は、バージョン 10.0.23 でサポートされています:

- タイ
- 日本
- マレーシア
- シンガポール

## <a name="related-resources"></a>関連するリソース

[税サービスの使用を開始する](./global-get-started-with-tax-calculation-service.md)

[複数の VAT 登録番号](./emea-multiple-vat-registration-numbers.md)

[移動オーダーに対する税機能のサポート](./tasks/tax-feature-support-for-transfer-order.md)

[税サービスで拡張機能を作成する方法](./tax-service-add-data-fields-tax-integration-by-extension.md)
