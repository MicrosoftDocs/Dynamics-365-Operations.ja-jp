---
title: 電子請求管理コンポーネント
description: このトピックでは、電子請求の管理に関連するコンポーネントについて説明します。
author: gionoder
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463884"
---
# <a name="electronic-invoicing-administration-components"></a>電子請求管理コンポーネント

[!include [banner](../includes/banner.md)]


このトピックでは、電子請求の管理に関連するコンポーネントについて説明します。 また、電子請求サービスの設定方法についても説明しています。

## <a name="azure"></a>Azure

Microsoft Azure を使用して、Key Vault のシークレットを作成し、ストレージ アカウントを設定します。 その後、電子請求の構成で、Key Vault シークレットとストレージ アカウントの SAS トークンを使用します。

## <a name="lifecycle-services"></a>Lifecycle Services

Microsoft Dynamics Lifecycle Services (LCS) を使用して、LCS 配置プロジェクトの電子請求アドインを有効にします。

> [!NOTE]
> LCS にアドインをインストールするには、少なくとも **Tier 2 以上の環境** が必要です。 環境計画に関する詳細については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) は、電子請求の構成に使用します。 環境や電子請求書機能などのリソースは、RCSで作成、管理、ホストされます。 リソースの準備が整うと、電子請求サービスにリソースが公開されます。

RCS の登録については、[Regulatory services](https://marketing.configure.global.dynamics.com/) を参照してください。

RCS の詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください

### <a name="integration-with-electronic-invoicing"></a>電子請求との統合 

RCS を使用して電子請求書を構成するには、電子請求との通信を許可するために、RCS を構成する必要があります。 **電子申告パラメーター** ページの **電子請求** タブでこの構成を完了します。

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>サービス エンドポイント

電子請求は、いくつかの Azure データセンターの地域で使用できます。 次の表に、地域ごとの可用性の一覧を示します。


| Azure geography データ センター | サービス エンドポイント URI                                                       |
|----------------------------|----------------------------------------------------------------------------|
| 米国              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| ヨーロッパ                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| 英国             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| アジア                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>サービス環境

サービス環境は、電子請求におけるグローバリゼーション機能の実行をサポートするために作成される論理パーティションです。 セキュリティのシークレットや電子証明書、ガバナンス (アクセス権限) は、サービス環境レベルで構成する必要があります。

顧客は、必要な数のサービス環境を作成できます。 顧客が作成するサービス環境は互いに依存するものではありません。

サービス環境は、RCS で作成・管理する必要があります。 サービス環境の準備が整うと、電子請求にリソースが公開されます。

#### <a name="service-environment-status"></a>サービス環境の状態

サービス環境は、状態を介して管理できます。 想定できるオプションは次のとおりです。

- **未公開** - 環境は作成済ですが、まだ公開されていません。
- **公開済** - 環境が電子請求に公開されました。
- **変更済** - 公開された環境の属性は変更されましたが、まだ公開されていません。

#### <a name="customer-secrets"></a>顧客のシークレット

電子請求サービスは、企業が所有する Azure リソースにすべてのビジネス データを保存する役割を果たします。 サービスが正常に動作し、電子請求で必要とされ生成されるすべてのビジネス データに適切にアクセスできるようにするためには、2 つの主要な Azure リソースを作成する必要があります。

- 電子請求書、ドキュメント変換の結果、および外部 Web サービスからの応答を含め、電子ドキュメントを格納する Azure ストレージ アカウント (Blob ストレージ)。
- 証明書とストレージ アカウントの Uniform Resource Identifier (URI) を格納する Azure Key Vault (SAS トークン)。


電子請求で使用するには、専用の Key Vault のリソースと顧客のストレージ アカウントを特別に割り当てる必要があります。 詳細については、[Azure ストレージ アカウント と Key Vault の作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。

Key Vault の正常性を監視し、警告を受信するには、Key Vault の Azure Monitor を構成します。 Key Vault ログを有効にすると、Key Vault がどのように、また、いつ、だれにアクセスされたかを監視することができます。 詳細については、[Azure Key Vault の監視と警告](/azure/key-vault/general/alert)および [Key Vault ログを有効にする方法](/azure/key-vault/general/howto-logging?tabs=azure-cli) を参照してください。

ベスト プラクティスとして、定期的にシークレットのローテーションを行います。 詳細については、[シークレット ドキュメント](/azure/key-vault/secrets/) を参照してください。

#### <a name="users"></a>ユーザー

各サービス環境では、電子請求で Dynamics 365 Finance と Dynamics 365 Supply Chain Management から接続できるユーザーの一覧を作成する必要があります。

#### <a name="publication"></a>公開

サービス環境は、電子請求に公開した後で使用する必要があります。 公開された環境のみが、 Finance および Supply Chain Management からアクセスできます。 また、電子請求書発行サービスで属性の更新が有効になる前に、サービス環境を公開する必要があります。

### <a name="connected-applications"></a>接続した申請

接続されたアプリケーションは、RCS によって利用できる Finance および Supply Chain Management のインスタンスです。 アプリケーションの URL とそのテナントに加え、接続されたアプリケーションには、RCS が環境に接続できる資格情報が含まれています。

接続されたアプリケーションを通じて、Finance および Supply Chain Management の電子請求書機能の一部を構成することで、電子請求書の機能全体を機能させることができます。

## <a name="finance-and-supply-chain-management"></a>Finance および Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>電子請求との統合

Finance および Supply Chain Management を使用して電子請求書アドオンを介した電子請求書を発行するには、サービスと通信ができるように構成する必要があります。

#### <a name="electronic-invoicing-integration-feature"></a>電子請求統合機能

Finance および Supply Chain Management と電子請求の間の通信を有効にするには、**機能管理** ワークスペースで **電子請求の統合** 機能を有効にする必要 があります。

#### <a name="service-endpoint"></a>サービス エンドポイント

サービス エンドポイントは、電子請求が位置する URL です。 サービスとの通信を可能にするには、電子請求書を発行する前にサービスのエンドポイントを Finance と Supply Chain Management に構成する必要があります。

サービス エンドポイントを構成するには、**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動し、**電子請求** タブの **エンドポイント URL** フィールドに、このトピックで前述した[サービス エンドポイント](#svc-endpoint-uris)のセクションにある表から適切な URL を入力します。

#### <a name="environments"></a>環境

Finance および Supply Chain Management に入力された環境名は、RCS で作成され、電子請求に公開されている環境名を指します。

**電子ドキュメント パラメーター** ページの **電子請求** タブで環境を構成する必要があります。 このように、すべての電子請求書発行の要求には、要求を処理する必要がある電子請求を決定する電子請求の環境が含まれています。

## <a name="additional-resources"></a>追加リソース

- [RCS で電子請求書を構成する](e-invoicing-configuration-rcs.md)
- [Finance および Supply Chain Management で電子請求書を発行する](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
