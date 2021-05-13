---
title: マスター データ検索用の環境の設定
description: このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。
author: kai-cloud
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 9f9b385df1db60b27698d90281c43fabb574af49
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924157"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>マスター データ検索用の環境の設定

[!include [banner](../includes/banner.md)]

このトピックでは、税計算マスター データ検索機能を使用するための環境の設定方法について説明します。

1. Lifecycle Services (LCS) の Power Platform 統合を設定します。 詳細については、[Microsoft Power Platform 統合 - アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。
2. Dynamics 365 Finance および Microsoft Dataverse を設定します。 詳細については、[ソリューションの入手](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution)および[認証と承認](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization)を参照してください。
3. 次のエンティティを設定します。 詳細については、[仮想エンティティの有効化](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#enabling-virtual-entities) を参照してください。
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
4. Dynamics 365 Regulatory Configuration Service (RCS) を設定します。 
5. Microsoft に対するサービス要求を作成して、次の機能のフライティングを有効にします:

      - ERCdsFeature
      - TaxServiceCDSFeature

6. **機能管理** ワークスペースに移動し、次の機能を有効にします。

      - (プレビュー) 電子申告 Dataverse データ ソース サポート
      - (プレビュー) 税サービス Dataverse のデータソース サポート
      - (プレビュー) グローバリゼーション機能

5. テナント管理者アカウントを使用して RCS にログインします。
6. **電子申告** > **接続アプリケーション** に移動します。 
7. **新規** を選択してレコードを追加し、次のフィールド情報を入力します。 

   - **名前** フィールドに、名前を入力します。
   - **タイプ** フィールドで、**Dataverse** を選択します。
   - **アプリケーション** フィールドに、Dataverse URL を入力します。
   - **テナント** フィールドに、テナントを入力します。
   - **カスタム URL** フィールドに、Dataverse URL を入力し、"/api/data/v9.1" を追加します。

8. **接続の確認** を選択し、接続プロセスを完了します。 

   [![接続の確認ボタン](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. **電子申告** > **税コンフィギュレーション** に移動し、[税コンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2158352)から税コンフィギュレーションをインポートします。

   [![税コンフィギュレーション ページ、税データ モデル ツリー](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. **課税対象ドキュメント モデル マッピング** または Microsoft コンフィギュレーションを使用している場合は **Dataverse モデル マッピング** に移動し、**接続アプリケーション** フィールドで、手順 7 で作成したレコードを選択します。
11. **モデル マッピングの既定値** を **はい** に設定します。

   [![モデル マッピング ページ](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
