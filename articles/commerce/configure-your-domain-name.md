---
title: ドメイン名の構成
description: この記事では、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。
author: josaw1
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 298ce84008e60cc82a494320b6a41f35338508c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278627"
---
# <a name="configure-your-domain-name"></a>ドメイン名の構成


[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。 

## <a name="add-domains-during-e-commerce-initialization"></a>eコマースの初期化中にドメインを追加する

ドメインを Dynamics 365 Commerce e コマース環境に関連付けるには、[新しい e コマース テナントのデプロイ](deploy-ecommerce-site.md).に記載されている通り、e コマースを初期化します。 初期化中、e コマース環境のプロビジョニングに使用する情報を提供するように求められます。 **サポートされるホスト名** フィールドに、この環境で使用する予定のすべてのドメインを追加します。 複数のドメインはセミコロンで区切る必要があります。 この方法で、全ての必要な e コーマース コンポーネントでドメインがコンフィギュレーションされ、それらは、コンテンツ配信ネットワーク (CDN) または Web サーバーからのトラフィックを切り替え、それを e コマース フロント エンドにポイントする際に使用する準備が整います。

## <a name="add-domains-after-e-commerce-initialization"></a>e-コマースの初期化後にドメインを追加する

e コマースの初期化後に新しいドメインを e コマース環境に関連付けるには、サービス要求を送信する必要があります。

## <a name="additional-resources"></a>追加リソース

[新しい eコマース テナントのデプロイ](deploy-ecommerce-site.md)

[eコマース サイトの作成](create-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
