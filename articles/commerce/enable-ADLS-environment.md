---
title: Dynamics 365 Commerce 環境での Azure Data Lake Storage の有効化
description: このトピックでは、Dynamics 365 Commerce 環境に対して、製品推奨事項を有効にする前提条件である Azure Data Lake Storage を有効化し、テストする方法について説明します。
author: bebeale
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ac440362379475b05c6a37019c25e3a96be3739
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349499"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Dynamics 365 Commerce 環境での Azure Data Lake Storage の有効化

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce 環境に対して、製品推奨事項を有効にする前提条件である Azure Data Lake Storage を有効化し、テストする方法について説明します。

Dynamics 365 Commerce ソリューションにおいて、すべての製品およびトランザクションの情報は環境のエンティティ格納で追跡されます。 このデータを、データ分析、ビジネス インテリジェンス、パーソナライズされた推奨事項などの他の Dynamics 365 サービスからアクセスできるようにするには、顧客所有の Azure Data Lake Storage Gen 2 ソリューションに環境を接続する必要があります。

Azure Data Lake Storage が環境でコンフィギュレーションされている場合、まだ保護が行われていて、顧客のコントロール下にある間、すべての必要なデータはエンティティ格納からミラーリングされます。

製品の推奨事項または個人用設定の推奨事項が環境でも有効になっている場合、製品の推奨事項スタックに Azure Data Lake Storage の専用フォルダーへのアクセス許可が付与され、顧客のデータを取得し、それに基づいた推奨事項を計算することができるようになります。

## <a name="prerequisites"></a>必要条件

顧客は、所有する Azure サブスクリプションで Azure Data Lake Storage をコンフィギュレーションする必要があります。 このトピックでは、Azure サブスクリプションの購入または Azure Data Lake Storage が有効なストレージ アカウントの設定については扱いません。

Azure Data Lake Storage の詳細については、[Azure Data Lake Storage Gen2 公式ドキュメント](https://azure.microsoft.com/pricing/details/storage/data-lake) を参照してください。
  
## <a name="configuration-steps"></a>コンフィギュレーションの手順

このセクションでは、製品の推奨事項に関連する環境で Azure Data Lake Storage を有効にするために必要なコンフィギュレーション手順について説明します。
Azure Data Lake Storage を有効にするために必要な手順の詳しい概要については、[エンティティ格納を Data Lake として使用可能にする](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md) を参照してください。

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>環境での Azure Data Lake Storage の有効化

1. 環境のバック オフィス ポータルにログインします。
1. **システム パラメーター** を検索し、**データ接続** タブに移動します。 
1. **Data Lake 統合の有効化** を **はい** に設定します。
1. **Data Lake のトリクル更新** を **はい** に設定します。
1. 次に、次の必要な情報を入力します。
    1. **アプリケーション ID** // **アプリケーション シークレット** // **DNS 名** - Azure Data Lake Storage シークレットが保存されている KeyVault に接続する必要があります。
    1. **シークレット名** - KeyVault に格納されていて、Azure Data Lake Storage の認証に使用されるシークレット名。
1. ページ左上隅の変更を保存します。

次の図は、Azure Data Lake Storage コンフィギュレーションの例を示しています。

![Azure Data Lake Storage コンフィギュレーションの例。](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>Azure Data Lake Storage 接続のテスト

1. **Azure Key Vault のテスト** のリンクを使用して KeyVault への接続をテストします。
1. **Azure Storage のテスト** のリンクを使用して Azure Data Lake Storage への接続をテストします。

> [!NOTE]
> テストに失敗した場合、上記の手順で追加した KeyVault 情報がすべて正しいことを確認してから、再試行してください。

接続テストが成功したら、エンティティ格納の自動更新を有効にする必要があります。

エンティティ格納の自動更新を有効にするには、以下の手順に従います。

1. **エンティティ格納** を検索します。
1. 左のリストで、**RetailSales** エントリに移動し、**編集** を選択します。
1. **自動更新の有効化** が **はい** に設定されていることを確認してから **更新** を選択し、**保存** を選択します。

次の図は、自動更新が有効になっているエンティティ格納の例を示しています。

![自動更新が有効になっているエンティティ格納の例。](./media/exampleADLSConfig2.png)

Azure Data Lake Storage が環境に対してコンフィギュレーションされました。 

まだ完了していない場合、環境に対する [製品推奨事項および個人用設定の有効化](enable-product-recommendations.md) の手順に従います。

## <a name="additional-resources"></a>追加リソース

[エンティティ格納を Data Lake として使用可能にする](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[製品推奨事項の概要](product-recommendations.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨事項の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[収集された推奨事項の手動作成](create-editorial-recommendation-lists.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
