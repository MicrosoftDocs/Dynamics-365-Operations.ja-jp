---
title: ドメイン名のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796054"
---
# <a name="configure-your-domain-name"></a>ドメイン名のコンフィギュレーション


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。 

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