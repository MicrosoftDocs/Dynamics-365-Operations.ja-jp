---
title: フランス向け電子請求のアドオンの使用を開始する
description: この記事では、フランス向け電子請求書作成アドオンの使用を開始するにあたっての情報を提供します。
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573281"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>フランス向け電子請求のアドオンの使用を開始する

[!include [banner](../includes/banner.md)]

この記事では、フランス向けの電子請求を使い始めるための情報を提供します。 Regulatory Configuration Service (RCS) における、国ごとに異なる構成手順について説明します。 これらの手順は、[電子請求アドオンの使用を開始する](e-invoicing-get-started.md) で説明した手順を補完します。

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>フランス Chorus Pro 申請 (FR) 電子請求機能の国別コンフィギュレーション

**フランス Chorus Pro 申請 (FR)** の電子請求機能を構成するには、いくつかの手順が必要です。 構成の一部のパラメーターは、既定値で公開されます。 これらの値は、事業運営をより反映するように見直し、更新する必要があります。

### <a name="prerequisites"></a>必要条件

この記事の手順を開始する前に、以下の前提条件を完了します:

- 電子請求について理解していること。 詳細については、[電子請求の概要](e-invoicing-service-overview.md) を参照してください。
- RCS に登録し、電子請求を設定します。 詳細については、次の記事を参照してください。

    - [電子請求サービスへの登録およびインストール](e-invoicing-sign-up-install.md)
    - [電子請求のための Azure リソースの設定](e-invoicing-set-up-azure-resources.md)
    - [Lifecycle Services にマイクロサービス向けのアドインをインストールします](e-invoicing-install-add-in-microservices-lcs.md)
    - [電子請求との統合のアクティブ化と設定](e-invoicing-activate-setup-integration.md) – この記事の情報を使用して、Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management アプリと電子請求サービス間の統合をアクティブにします。
    - [NAF コードと Siret 番号](emea-fra-naf-codes-siret-numbers.md) と [NAF コードと Siret 番号の設定](tasks/fr-00003-naf-codes-siret-numbers.md) – これらの記事の情報を使用して、法人に NAF コードと Siret 番号を設定します。 

- Chorus Pro を使用するには、組織の登録が必要です。 Microsoft では、アプリケーション プログラミング インターフェイス (API) を経由して、OAuth2 Mode で Chorus pro との統合を提供しています。 Chorus Pro の登録とアプリケーションのアクティブ化の詳細については、[公式ドキュメント](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/) を参照してください。

    以下の手順で、Chorus Pro に登録します。

    1. [PISTE ポータル](https://piste.gouv.fr/en/component/apiportal/registration) に移動して登録を開始します。 
    2. アプリケーションを登録し、Open Authorization (OAuth) 資格情報をアクティブにします。
    3. OAuth 資格情報のクライアント ID とシークレット キーをコピーして保存します。 この情報は、後の手順で使用します。
    4. [Chorus Pro ポータル](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) に移動して登録します。 
    5. API アクセス用の技術アカウントを作成します。 詳細については、[運用環境での API アクセス用技術アカウントの作成](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/) を参照してください。
    6. 技術アカウントのユーザー ID とパスワードをコピーします。 この情報は、後の手順で使用します。

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>フランス Chorus Pro 申請 (FR) 電子請求機能のアプリケーション設定の国別コンフィギュレーション

**フランス Chorus Pro 申請 (FR)** 電子請求機能のパラメーターの一部は、既定値で公開されます。 電子請求機能をサービス環境に配置する前に、必要に応じて既定値を確認および更新し、事業運営がより適切に反映されるようにします。

1. Azure Key Vault で、シークレットとそれに対応する参照を作成します。 詳細については、[顧客の証明書とシークレット](e-invoicing-customer-certificates-secrets.md) を参照してください。
2. [グローバル リポジトリからの機能のインポート](e-invoicing-import-feature-global-repository.md) に記載の **フランス Chorus Pro 申請 (FR)** グローバリゼーション機能の最新バージョンをインポートします。
3. インポートされたグローバリゼーション機能のコピーを作成し、構成プロバイダーを選択します。 詳細については、[グローバリゼーション機能の作成](e-invoicing-create-new-globalization-feature.md) を参照してください。
4. **バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。
5. **設定** タブのグリッドで、**UBL 売上請求書派生** 機能の設定を選択します。
6. **編集** を選択し、**処理中のパイプライン** タブの **処理中のパイプライン** セクションで、アクション名 **フランス Chorus Pro 申請** の **(プレビュー) フランスの Chorus Pro と統合する** を選択します。
7. **パラメーター** セクションの **クライアント ID シークレット名** フィールドで、キー コンテナーのクライアント ID に対して作成したシークレット名を選択します。
8. **クライアント シークレットのシークレット名** セクションで、キー コンテナーのクライアント シークレットに対して作成したシークレット名を選択します。
9. **技術ログイン シークレット名** フィールドで、キー コンテナーの技術アカウント サインインに対して作成したシークレット名を選択します。
10. **技術パスワード シークレット名** フィールドで、キー コンテナーの技術アカウント パスワードに対して作成したシークレット名を選択します。
11. **処理中のパイプライン** タブの **処理中のパイプライン** セクションで、アクション名 **フランス Chorus Pro リクエスト ステータス** の **フランスの Chorus Pro と統合する** を選択します。
12. **パラメーター** セクションの **クライアント ID シークレット名** フィールドで、キー コンテナーのクライアント ID に対して作成したシークレット名を選択します。
13. **クライアント シークレットのシークレット名** セクションで、キー コンテナーのクライアント シークレットに対して作成したシークレット名を選択します。
14. **技術ログイン シークレット名** フィールドで、キー コンテナーの技術アカウント サインインに対して作成したシークレット名を選択します。
15. **技術パスワード シークレット名** フィールドで、キー コンテナーの技術アカウント パスワードに対して作成したシークレット名を選択します。
16. **保存** を選択し、ページを閉じます。
17. **UBL プロジェクト請求書派生** 機能の設定、**UBL 売上訂正票派生** 機能の設定、および **UBL プロジェクト訂正票派生** 機能の設定について、手順 6 から手順 16 を繰り返します。

## <a name="additional-resources"></a>追加リソース

- [電子請求アドオンの概要](e-invoicing-service-overview.md)
- [電子請求アドオン サービス管理の使用を開始する](e-invoicing-get-started-service-administration.md)
- [電子請求アドオンの使用を開始する](e-invoicing-get-started.md)
