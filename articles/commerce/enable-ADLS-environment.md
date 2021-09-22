---
title: Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効にする
description: このトピックでは、Dynamics 365 Commerce 環境のエンティティ格納に Azure Data Lake Storage Gen 2 ソリューションを接続する方法について説明します。 製品推奨事項の有効化の前に、この手順を実行する必要があります。
author: bebeale
ms.date: 08/31/2020
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
ms.openlocfilehash: c96c29a4d9639b02e6a60ad938b7e06f7d500c68
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466295"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効にする

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce 環境のエンティティ格納に Azure Data Lake Storage Gen2 ソリューションを接続する方法について説明します。 製品推奨事項の有効化の前に、この手順を実行する必要があります。

Dynamics 365 Commerce ソリューションにおいて、推奨事項、製品、およびトランザクションの計算に必要なデータは、環境のエンティティ格納で集計されます。 このデータを、データ分析、ビジネス インテリジェンス、パーソナライズされた推奨事項などの他の Dynamics 365 サービスからアクセスできるようにするには、顧客所有の Azure Data Lake Storage Gen2 ソリューションに環境を接続する必要があります。

上記の手順が完了した後、環境のエンティティ格納内の顧客データすべては、自動的に顧客の Azure Data Lake Storage Gen 2 ソリューションにミラーリングされます。 Commerce 本社の機能管理ワークスペースを介して推奨事項機能が有効にされた場合、推奨事項スタックに同じ Azure Data Lake Storage Gen2 ソリューションへのアクセス許可が付与されます。

プロセス全体において顧客のデータは保護され、管理されたままです。

## <a name="prerequisites"></a>必要条件

Dynamics 365 Commerce 環境のエンティティ格納は、Azure Data Lake Gen Storage Gen2 アカウントおよび付属するサービスに接続されている必要があります。

Azure Data Lake Storage Gen2 およびその設定方法の詳細については、[Azure Data Lake Storage Gen2 公式ドキュメント](https://azure.microsoft.com/pricing/details/storage/data-lake)を参照してください。
  
## <a name="configuration-steps"></a>コンフィギュレーションの手順

このセクションでは、製品の推奨事項に関連する環境で Azure Data Lake Storage Gen2 を有効にするために必要な構成手順について説明します。
Azure Data Lake Storage Gen2 を有効にするために必要な手順の詳しい概要については、[エンティティ格納を Data Lake として使用可能にする](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)を参照してください。

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>環境での Azure Data Lake Storage の有効化

1. 環境のバック オフィス ポータルにログインします。
1. **システム パラメーター** を検索し、**データ接続** タブに移動します。 
1. **Data Lake 統合の有効化** を **はい** に設定します。
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
> 上記のテストのいずれかに失敗した場合、上記の手順で追加した KeyVault 情報がすべて正しいことを確認してから、再試行してください。

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
