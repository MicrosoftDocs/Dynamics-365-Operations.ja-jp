---
title: コンテンツ配信ネットワーク (CDN) のサポートの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646042"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>コンテンツ配信ネットワーク (CDN) のサポートの追加


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce の E コマース環境を設定すると、CDN サービスと連携するようにコンフィギュレーションできます。 

カスタム ドメインは、E コマース環境のプロビジョニング プロセス中に有効にできます。 また、プロビジョニング プロセスが完了した後に、サービス要求を使用して設定することもできます。 E コマース環境のプロビジョニング プロセスでは、環境に関連付けられたホスト名が生成されます。 \<*e-commerce-tenant-name*\> が環境の名称となっている場合、このホスト名の形式は次のとおりです :

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

プロビジョニング プロセス中に生成されるホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ Secure Sockets Layer (SSL) 証明書をサポートします。 カスタム ドメインに対する SSL はサポートしません。 したがって、CDN のカスタム ドメインの SSL を終了し、CDN からコマースが生成したホスト名またはエンドポイントへトラフィックを転送する必要があります。 

さらに、コマースからの *静的* (JavaScript または カスケード スタイル シート \[CSS\] ファイル) は、コマースが生成したエンドポイント (\*.commerce.dynamics.com) から提供されます。 静的は、コマースが生成したホスト名またはエンドポイントが CDN の後に配置される場合にのみキャッシュできます。

## <a name="set-up-ssl"></a>SSL のセットアップ

SSL が設定され、その静的が確実にキャッシュされるようにするには、環境に対してコマースが生成したホスト名に関連付けられるよう CDN をコンフィギュレーションする必要があります。 また、次のパターンを静的に対してのみキャッシュする必要があります。 

/\_msdyn365/\_scnr/\*

指定されたカスタム ドメインを使用してコマース環境をプロビジョニングした後、またはサービス要求を使用して環境のカスタム ドメインを指定した後、カスタム ドメインをコマースが生成したホスト名またはエンドポイントに向けます。

前述のように、生成したホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ SSL 証明書をサポートします。 カスタム ドメインに対する SSL はサポートしません。

## <a name="cdn-services"></a>CDN サービス

任意の CDN サービスは、コマース環境で使用できます。 次に 2 つの例を挙げます。

- **Microsoft Azure Front Door Service** – Azure CDN ソリューション。 Azure Front Door Service の詳細については、[Azure Front Door Service のドキュメント](https://docs.microsoft.com/azure/frontdoor/) を参照してください。
- **Akamai 動的サイト アクセラレータ** – 詳細については、[動的サイト アクセラレータ](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp) を参照してください。

## <a name="cdn-setup"></a>CDN の設定

CDN の設定プロセスは、次の一般的な手順で構成されています。

1. フロント エンド ホストを追加します。
1. バック エンド プールを構成します。
1. ルート指定とキャッシュのルールを設定します。

### <a name="add-a-front-end-host"></a>フロント エンド ホストを追加する

任意の CDN サービスを使用できますが、このトピックの例では、 Azure Front Door Service を使用します。 

Azure Front Door Service の設定方法の詳細については、[クイックスタート: 高可用性グローバル Web アプリケーションに対する Front Door を作成する](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door) を参照してください。

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Azure Front Door Service のバック エンド プールを構成する

Azure Front Door Service のバック エンド プールを構成するには、次の手順を実行してください。

1. **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** を、空のバック エンド ホスト ヘッダーを持つカスタム ホストとして、バック エンド プールに追加します。
1. **負荷分散**では、既定値のままにします。

次の図は、バック エンド ホスト名が入力された Azure Front Door Service の**バックエンドの追加**ダイアログ ボックスを示します。

![バックエンド プール ダイアログ ボックスを追加する](./media/CDN_BackendPool.png)

次の図は、既定の負荷分散値が入力された Azure Front Door Service の**バックエンド プール の追加**ダイアログ ボックスを示します。

![バックエンド プールのダイアログ ボックスを継続して追加する](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a>Azure Front Door Service でルールを設定する

Azure Front Door Service でルート指定ルールを設定するには、次の手順を実行します。

1. ルート指定ルールを追加します。
1. **名前**フィールドに、**既定**と入力します。
1. **承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。
1. **フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。
1. **照合するパターン**の、上のフィールドで、**/\*** と入力します。
1. **工順の詳細**で、**工順タイプ** オプションを**転送**に設定します。
1. **バックエンド プール** フィールドで、**ecom-backend** を選択します。
1. **転送プロトコル** フィールド グループで、**照合要求**オプションを選択します。 
1. **URL Rewrite** オプションを**無効**に設定します。
1. **キャッシュ** オプションを**無効**に設定します。

Azure Front Door Service でキャッシュ ルールを設定するには、次の手順を実行します。

1. キャッシュ ルールを追加します。
1. **名前**フィールドに、**静的**と入力します。
1. **承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。
1. **フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。
1. **照合するパターン**の、上のフィールドで、**/\_msdyn365/\_scnr/\*** と入力します。
1. **工順の詳細**で、**工順タイプ** オプションを**転送**に設定します。
1. **バックエンド プール** フィールドで、**ecom-backend** を選択します。
1. **転送プロトコル** フィールド グループで、**照合要求**オプションを選択します。
1. **URL Rewrite** オプションを**無効**に設定します。
1. **キャッシュ** オプションを**無効**に設定します。
1. **クエリ文字列のキャッシュ動作**フィールドで、**一意の URL ごとキャッシュする**を選択します。
1. **動的な圧縮**フィールド グループで、**有効化**オプションを選択します。

次の図は、Azure Front Door Service の**ルールの追加**ダイアログ ボックスを示します。

![ルールの追加ダイアログ ボックス](./media/CDN_CachingRule.png)

> [!WARNING]
> 使用するドメインが既に有効化されている場合は、[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) の **サポート**タイルからサポートチケットを作成して、次の手順についてのサポートを受けてください。 詳細については、[Finance and Operations アプまたは Lifecycle Services (LCS) のサポートを得る](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。

ご利用のドメインが新しく、かつ既存のドメインではない場合は、Azure Front Door Service の構成にカスタム ドメインを追加することができます。 これにより、web トラフィックが Azure Front Door インスタンスを介してサイトに誘導されるようになります。 カスタム ドメイン (たとえば、`www.fabrikam.com`) を追加するには、ドメインの正規名 (CNAME) をコンフィギュレーションする必要があります。

次の図は、Azure Front Door Service の**CNAME コンフィギュレーション** ダイアログ ボックスを示します。

![CNAME コンフィギュレーション ダイアログ ボックス](./media/CNAME_Configuration.png)

Azure Front Door Service を使用して証明書を管理したり、カスタム ドメインに対して独自の証明書を使用したりできます。

次の図は、Azure Front Door Service の**カスタム ドメイン HTTPS** ダイアログ ボックスを示します。

![カスタム ドメイン HTTPS ダイアログ ボックス](./media/Custom_Domain_HTTPS.png)

Azure Front Door にカスタムドメインを追加する方法の詳細については、[フロント ドアにカスタム ドメインを追加する](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain)を参照してください。

これにより、CDN を正しくコンフィギュレーションして、コマース サイトで使用できるようになります。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい E コマース サイトの配置](deploy-ecommerce-site.md)

[E コマース サイトの作成](create-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
