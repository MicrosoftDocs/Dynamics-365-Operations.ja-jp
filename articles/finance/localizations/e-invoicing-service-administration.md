---
title: 電子請求書アドオン管理コンポーネント
description: このトピックでは、電子請求書アドオンの管理に関連するコンポーネントについて説明します。
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592577"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>電子請求書アドオン管理コンポーネント

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

このトピックでは、電子請求書アドオンの管理に関連するコンポーネントについて説明します。 また、電子請求アドオン サービスの設定方法についても説明しています。

## <a name="azure"></a>Azure

Microsoft Azure を使用して、key vault およびストレージ アカウントのシークレットを作成します。 このシークレットを、電子請求書アドオンの構成で使用します。

## <a name="lifecycle-services"></a>Lifecycle Services

Microsoft Dynamics Lifecycle Services (LCS) を使用して、LCS デプロイ プロジェクトのマイクロサービスに対するアドオンを有効にします。

> [!NOTE]
> LCS にマイクロサービス アドオンをインストールするには、少なくとも Tier 2 以上の仮想マシンが必要です。 環境計画に関する詳細については、[環境計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) は、電子請求書のアドオンの構成に使用します。 環境や電子請求書機能などのリソースは、RCSで作成、管理、ホストされます。 リソースの準備が整うと、電子請求アドオン サービスにリソースが公開されます。

RCS の登録については、[Regulatory services](https://marketing.configure.global.dynamics.com/) を参照してください。

RCS の詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください

### <a name="integration-with-the-electronic-invoicing-add-on"></a>電子請求書アドオンとの統合

RCS を使用して電子請求書を構成するには、電子請求アドオンとの通信を許可するために、RCS を構成する必要があります。 **電子申告パラメーター** ページの **電子請求書アドオン** タブでこの構成を完了します。

#### <a name="service-endpoint"></a>サービス エンドポイント

電子請求のアドオンは、いくつかの Azure データセンターの地域で使用できます。 次の表に、地域ごとの可用性の一覧を示します。

| Azure データ センターの地域 |
|----------------------------|
| 米国東部                    |
| 米国西部                    |
| 北ヨーロッパ                   |
| 西ヨーロッパ                    |

### <a name="service-environments"></a>サービス環境

サービス環境は、電子請求書アドオンにおける電子請求機能の実行をサポートするために作成される論理パーティションです。 セキュリティのシークレットや電子証明書、ガバナンス (アクセス権限) は、サービス環境レベルで構成する必要があります。

顧客は、必要な数のサービス環境を作成できます。 顧客が作成するサービス環境は互いに依存するものではありません。

サービス環境は、RCS で作成・管理する必要があります。 サービス環境の準備が整うと、電子請求アドオンにリソースが公開されます。

#### <a name="service-environment-status"></a>サービス環境の状態

サービス環境は、状態を介して管理できます。 想定できるオプションは次のとおりです。

- **未公開** - 環境は作成済ですが、まだ公開されていません。
- **公開済** - 環境が電子請求書アドオンに公開されました。
- **変更済** - 公開された環境の属性は変更されましたが、まだ公開されていません。

#### <a name="customer-secrets"></a>顧客のシークレット

電子請求アドオンサービスは、企業が所有する Azure リソースにすべてのビジネス データを保存する役割を果たします。 サービスが正常に動作し、電子請求書アドオンで必要とされ、生成されるすべてのビジネス データにアクセスできるようにするためには、2 つの主要な Azure リソースを作成する必要があります。

- 電子請求書を格納する Azure ストレージ アカウント (Blob ストレージ)
- 証明書とストレージ アカウントの Uniform Resource Identifier (URI) を格納する Azure key vault

> [!NOTE]
> 電子請求書作成アドオンで使用するには、専用の Key Vault のリソースと顧客の Blob ストレージを特別に割り当てる必要があります。

詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。

#### <a name="users"></a>ユーザー

各サービス環境では、電子請求書アドオンで Dynamics 365 Finance と Dynamics 365 Supply Chain Management から接続できるユーザーの一覧を作成する必要があります。

#### <a name="publication"></a>公開

サービス環境は、電子請求書アドオンに公開した後で使用する必要があります。 公開された環境のみが、 Finance および Supply Chain Management からアクセスできます。 また、電子請求書発行サービスで属性の更新が有効になる前に、サービス環境を公開する必要があります。

### <a name="connected-applications"></a>接続した申請

接続されたアプリケーションは、RCS によって利用できる Finance および Supply Chain Management のインスタンスです。 アプリケーションの URL とそのテナントに加え、接続されたアプリケーションには、RCS が環境に接続できる資格情報が含まれています。

接続されたアプリケーションを通じて、Finance および Supply Chain Management の電子請求書機能の一部を構成することで、電子請求書の機能全体を機能させることができます。

## <a name="finance-and-supply-chain-management"></a>Finance および Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>電子請求書アドオンとの統合

Finance および Supply Chain Management を使用して電子請求書アドオンを介した電子請求書を発行するには、サービスと通信ができるようにアドオンを構成する必要があります。

#### <a name="electronic-invoicing-add-on-integration-feature"></a>電子請求書のアドオン統合機能

Finance および Supply Chain Management と電子請求アドオンの間の通信を有効にするには、**機能管理** ワークスペースで **電子請求アドオンの統合** 機能を有効にする必要 があります。

#### <a name="service-endpoint"></a>サービス エンドポイント

サービス エンドポイントは、電子請求書アドオンが位置する URL です。 サービスとの通信を可能にするには、電子請求書を発行する前にサービスのエンドポイントを Finance と Supply Chain Management に構成する必要があります。

サービス エンドポイントを構成するには、**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動し、**送信サービス** タブの **電子請求アドオン URL** フィールドに、**サービス エンドポイント** のセクションで説明されている表に従って URL を入力します。

#### <a name="environments"></a>環境

Finance および Supply Chain Management に入力された環境名は、RCS で作成され、電子請求書アドオンに公開されている環境名を指します。

環境は、電子請求書を発行するすべての要求に、電子請求アドオンがどの電子請求機能が要求を処理する必要があるかどうかを決定できる環境を含むように、**電子ドキュメント パラメータ** ページの **送信サービス** タブで構成する必要があります。

## <a name="additional-resources"></a>追加リソース

- [RCS で電子請求書を構成する](e-invoicing-configuration-rcs.md)
- [Finance および Supply Chain Management で電子請求書を発行する](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
