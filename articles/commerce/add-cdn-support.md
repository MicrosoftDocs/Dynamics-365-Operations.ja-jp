---
title: コンテンツ配信ネットワーク (CDN) のサポートの追加
description: この記事では、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。
author: brianshook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2177eeb6497269d580d2baea87ebb4fcd395223b
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069671"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a>コンテンツ配信ネットワーク (CDN) のサポートの追加

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce 環境にコンテンツ配信ネットワーク (CDN) を追加する方法について説明します。

Dynamics 365 Commerce の E コマース環境を設定すると、CDN サービスと連携するようにコンフィギュレーションできます。 

カスタム ドメインは、E コマース環境のプロビジョニング プロセス中に有効にできます。 また、プロビジョニング プロセスが完了した後に、サービス要求を使用して設定することもできます。 E コマース環境のプロビジョニング プロセスでは、環境に関連付けられたホスト名が生成されます。 \<*e-commerce-tenant-name*\> が環境の名称となっている場合、このホスト名の形式は次のとおりです :

&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com

プロビジョニング プロセス中に生成されるホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ Secure Sockets Layer (SSL) 証明書をサポートします。 カスタム ドメインに対する SSL はサポートしません。 したがって、CDN のカスタム ドメインの SSL を終了し、CDN からコマースが生成したホスト名またはエンドポイントへトラフィックを転送する必要があります。 

さらに、コマースからの *静的* (JavaScript または カスケード スタイル シート \[CSS\] ファイル) は、コマースが生成したエンドポイント (\*.commerce.dynamics.com) から提供されます。 静的は、コマースが生成したホスト名またはエンドポイントが CDN の後に配置される場合にのみキャッシュできます。

## <a name="set-up-ssl"></a>SSL を設定する

指定されたカスタム ドメインを使用してコマース環境をプロビジョニングした後、またはサービス要求を使用して環境のカスタム ドメインを指定した後は、コマースのオンボーディング チームと協力してDNS の変更を計画する必要があります。

前述のように、生成したホスト名またはエンドポイントは、\*.commerce.dynamics.com に対してのみ SSL 証明書をサポートします。 カスタム ドメインに対する SSL はサポートしません。

## <a name="cdn-services"></a>CDN サービス

任意の CDN サービスは、コマース環境で使用できます。 次に 2 つの例を挙げます。

- **Microsoft Azure Front Door Service** – Azure CDN ソリューション。 Azure Front Door Service の詳細については、[Azure Front Door Service のドキュメント](/azure/frontdoor/) を参照してください。
- **Akamai 動的サイト アクセラレータ** – 詳細については、[動的サイト アクセラレータ](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp) を参照してください。

## <a name="cdn-setup"></a>CDN の設定

CDN の設定プロセスは、次の一般的な手順で構成されています。

1. フロント エンド ホストを追加します。
1. バック エンド プールを構成します。
1. ルーティング規則を設定する。

### <a name="add-a-front-end-host"></a>フロント エンド ホストを追加する

任意の CDN サービスを使用できますが、この記事の例では、Azure Front Door Service を使用します。 

Azure Front Door Service の設定方法の詳細については、[クイックスタート: 高可用性グローバル Web アプリケーションに対する Front Door を作成する](/azure/frontdoor/quickstart-create-front-door) を参照してください。

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a>Azure Front Door Service のバック エンド プールを構成する

Azure Front Door Service のバック エンド プールを構成するには、次の手順を実行してください。

1. **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** と同じバックエンドホスト ヘッダを持つカスタムホストとして、**&lt;ecom-tenant-name&gt;.commerce.dynamics.com** をバックエンドプールに追加します。
1. **負荷分散** では、既定値のままにします。
1. バックエンド プールの正常性チェックを無効にします。

次の図は、バック エンド ホスト名が入力された Azure Front Door Service の **バックエンドの追加** ダイアログ ボックスを示します。

![バックエンド プール ダイアログ ボックスを追加します。](./media/CDN_BackendPool.png)

次の図は、既定の負荷分散値が入力された Azure Front Door Service の **バックエンド プール の追加** ダイアログ ボックスを示します。

![バックエンド プールのダイアログ ボックスを継続して追加します。](./media/CDN_BackendPool_2.png)

> [!NOTE]
> Commerce に対して独自の Azure Front Door Service サービスを設定する際は、 **正常性の検査** を無効にしてください。


### <a name="set-up-rules-in-azure-front-door-service"></a>Azure Front Door Service でルールを設定する

Azure Front Door Service でルート指定ルールを設定するには、次の手順を実行します。

1. ルート指定ルールを追加します。
1. **名前** フィールドに、**既定** と入力します。
1. **承認済プロトコル** フィールドで、**HTTP と HTTPS** を選択します。
1. **フロントエンド ホスト** フィールドで、**dynamics-ecom-tenant-name.azurefd.net** を入力します。
1. **照合するパターン** の、上のフィールドで、**/\*** と入力します。
1. **工順の詳細** で、**工順タイプ** オプションを **転送** に設定します。
1. **バックエンド プール** フィールドで、**ecom-backend** を選択します。
1. **転送プロトコル** フィールド グループで、**照合要求** オプションを選択します。 
1. **URL Rewrite** オプションを **無効** に設定します。
1. **キャッシュ** オプションを **無効** に設定します。


> [!WARNING]
> 使用するドメインが既に有効化されている場合は、[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) の **サポート** タイルからサポートチケットを作成して、次の手順についてのサポートを受けてください。 詳細については、[財務と運用アプリまたは Lifecycle Services (LCS) のサポート情報](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照してください。

ご利用のドメインが新しく、かつ既存のドメインではない場合は、Azure Front Door Service の構成にカスタム ドメインを追加することができます。 これにより、web トラフィックが Azure Front Door インスタンスを介してサイトに誘導されるようになります。 カスタム ドメイン (たとえば、`www.fabrikam.com`) を追加するには、ドメインの正規名 (CNAME) をコンフィギュレーションする必要があります。

次の図は、Azure Front Door Service の **CNAME コンフィギュレーション** ダイアログ ボックスを示します。

![CNAME コンフィギュレーション ダイアログ ボックス。](./media/CNAME_Configuration.png)

Azure Front Door Service を使用して証明書を管理したり、カスタム ドメインに対して独自の証明書を使用したりできます。

次の図は、Azure Front Door Service の **カスタム ドメイン HTTPS** ダイアログ ボックスを示します。

![カスタム ドメイン HTTPS ダイアログ ボックス。](./media/Custom_Domain_HTTPS.png)

Azure Front Door にカスタムドメインを追加する方法の詳細については、[フロント ドアにカスタム ドメインを追加する](/azure/frontdoor/front-door-custom-domain)を参照してください。

これにより、CDN を正しくコンフィギュレーションして、コマース サイトで使用できるようになります。

## <a name="additional-resources"></a>追加リソース

[コンテンツ配信ネットワークの実装オプション](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
