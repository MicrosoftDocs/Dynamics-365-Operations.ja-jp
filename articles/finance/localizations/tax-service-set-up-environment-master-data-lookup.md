---
title: マスター データ検索用の環境の設定
description: このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。
author: kai-cloud
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 901f8bcb0220355866952b68e92bc2dd906bb430
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700407"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>マスター データ検索用の環境の設定

[!include [banner](../includes/banner.md)]

このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。

1. Microsoft Dynamics Lifecycle Services (LCS) の Microsoft Power Platform 統合を設定します。 詳細については、[Microsoft Power Platform 統合 - アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。 この手順を完了すると、Microsoft Power Platform 環境の名前が **Power Platform 統合** セクションに表示されます。
2. [Microsoft Power Platform 管理センター](https://admin.powerplatform.microsoft.com/environments) に移動し、環境名を選択します。 環境 URL が提供されていません。
3. Dynamics 365 Finance および Dataverse を設定します。 詳細については、[仮想エンティティ ソリューションの入手](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#get-virtual-entity-solution) と [認証と承認](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization) を参照してください。
4. 次のエンティティを設定します。 詳細については、[Microsoft Dataverse 仮想エンティティの有効化](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md) を参照してください。

    - CompanyInfoEntity
    - CurrencyEntity
    - CustCustomerV3Entity
    - DeliveryTermsEntity
    - EcoResProductCategoryEntity
    - EcoResReleasedProductV2Entity
    - LogisticsAddressCityEntity
    - LogisticsAddressCountryRegionTranslationEntity
    - LogisticsAddressStateEntity
    - PurchProcurementChargeCDSEntity
    - SalesChargeCDSEntity
    - TaxGroupEntity
    - TaxItemGroupHeadingEntity
    - VendVendorV2Entity

5. Regulatory Configuration Service (RCS) を設定します。 **機能管理** ワークスペースを開き、次の機能を有効にします。

    - 電子報告 Dataverse データ ソース サポート
    - 税サービス Dataverse のデータソースのサポート
    - グローバリゼーション機能

6. テナント管理者アカウントを使用して RCS にログインします。
7. **電子申告** > **接続アプリケーション** に移動します。 
8. **新規** を選択してレコードを追加し、次のフィールド情報を入力します。 

    - **名前** フィールドに、名前を入力します。
    - **タイプ** フィールドで、**Dataverse** を選択します。
    - **アプリケーション** フィールドに、Dataverse URL を入力します。
    - **テナント** フィールドに、テナントを入力します。
    - **カスタム URL** フィールドに、Dataverse URL を入力し、"/api/data/v9.1" を追加します。

9. **接続の確認** を選択し、接続プロセスを完了します。 

    [![接続の確認ボタン。](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

10. **電子申告** > **税コンフィギュレーション** に移動し、[税コンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2158352)から税コンフィギュレーションをインポートします。

    [![税コンフィギュレーション ページ、税データ モデル ツリー。](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

11. **課税対象ドキュメント モデル マッピング** または Microsoft コンフィギュレーションを使用している場合は **Dataverse モデル マッピング** に移動し、**接続アプリケーション** フィールドで、手順 7 で作成したレコードを選択します。
12. **モデル マッピングの既定値** を **はい** に設定します。

    [![モデル マッピング ページ。](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
