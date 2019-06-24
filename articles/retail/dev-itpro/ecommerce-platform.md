---
title: E コマース プラットフォーム
description: このトピックでは、電子商取引の機能の概要を示します。
author: kfend
manager: AnnBe
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 18511
ms.assetid: 032233a8-dbc7-4946-a0cb-26db1b3e7d3f
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 56bf153ea1134e25312358d6326d720cbb2c7dba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569279"
---
# <a name="e-commerce-platform"></a>E コマース プラットフォーム

[!include [banner](../includes/banner.md)]

このトピックでは、電子商取引の機能の概要を示します。

Microsoft Dynamics 365 for Retail には、サード パーティのオンライン ストアがすべての機能を備えた E コマース サイトに容易にプラグインして作成できる完全に統合されたオムニチャネル E コマース プラットフォームが含まれています。 このプラットフォームには、リッチなショッピング カートと、クロス チャンネル シナリオをサポートするチェックアウト機能が含まれています。 さらに、プラットフォームは 1 つの顧客 ID を作成し、顧客口座、注文履歴、欲しい物のリスト、およびオンライン ストアを通じたロイヤルティの管理を可能にします。 E コマースの経験は、すべての必要なカスタマー エクスペリエンスを公開するスケーラビリティの高い Retail サーバーと統合されています。 このプラットフォームは、統合された支払と Open ID 統合をサポートして、シームレスなユーザー認証を提供します。 電子商取引のこのスイートを使用して、オンライン販売チャネルのあらゆる面に、製品、マーチャンダイジング、注文処理を中央管理できます。 次の図は、外部オンライン ストアを Dynamics 電子商取引プラットフォームと統合する方法を示しています。 

[![ECommerceUpdated](./media/ecommerceupdated-1024x545.png)](./media/ecommerceupdated.png) 

次のテーブルに、各コンポーネントについて説明します。

| **コンポーネント**          | **機能**                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 小売用バックオフィス    | オンライン ストア、製品、マーチャンダイジング、および注文フルフィルメントを小売用バックオフィスで集中管理し、構成します。 本社では、オンライン ストアを作成、設定、管理するための単一の場所を提供しています。 詳細については、[Retail の概要](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/index) を参照してください。                                                                                                                                                                                                                             |
| Commerce Data Exchange | Commerce Data Exchange には Microsoft Dynamics 365 for Retail とオンライン店舗間のデータ交換に使用されるいくつかのコンポーネントが含まれています。 これは、分散アーキテクチャをサポートします。 詳細については、[Commerce Data Exchange および Retail チャネル コミュニケーション](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/define-retail-channel-communications-cdx)を参照してください。                                                                                                                                                                                                                                                    |
| Retail サーバー          | Retail サーバーは、電子商取引に必要なすべての顧客サービスをサポートする商取引ランタイム上の OData Web API のセットです。 これには、ショッピング カート、注文管理、出荷価格、税金、欲しい物のリスト、顧客口座の管理、およびロイヤルティが含まれます。 Retail Server は、顧客認証用の Open ID 接続との統合もサポートしています。 支払の統合は、すぐに利用できるプロバイダーおよび外部プロバイダーの両方でサポートされます。 詳細については、[Retail サーバー アーキテクチャ](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-server-architecture)を参照してください。   |
| 公開しています             | Dynamics 電子商取引プラットフォームは、オンライン ストアの必要に応じて高度な検索機能をサポートする外部のオンライン固有のデータ ストアへのデータのエクスポートをサポートします。 これは、CMS で定期的に実行できるパブリッシャーに統合できる公開 API としてサポートされています。 これは、差分公開と完全公開の両方をサポートします。 詳細については、[Retail オンライン ストア公開アーキテクチャ](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-online-store-publishing-architecture)を参照してください。                                                                |
| プロキシ                  | プロキシは C\# で自動生成され、Retail Server と通信するために電子商取引プラットフォームにより使用されます。 詳細については、[Retail プロキシ](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/typescript-proxy-retail-pos) を参照してください。                                                                                                                                                                                                                                                                                                                                        |
| コントロール               | 一連の ASP.NET MVC コントロールは、チェック アウト、ショッピング カート、ミニ ショッピング カート、配送ピッカー、注文確認書に利用可能です。 コントロールは、顧客ログインと注文履歴にも利用できます。 ASP.NET オンライン ストアは、これらのコントロールを直接埋め込むことができます。 他の技術を使用するように実装されたオンライン ストアは、E コマース SDK で使用可能なコントローラ レイヤーと統合することができます。                                                       |
| サード パーティのストアフロント   | サンプル ASP.NET オンライン ストアは、デモと開発者の両方のトポロジが利用でき、SDK の一部です。 これは、サードパーティのストアフロントがプラットフォームにどのように統合できるかを示しています。                                                                                                                                                                                                                                                                      |





