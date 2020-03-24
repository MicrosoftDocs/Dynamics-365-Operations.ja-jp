---
title: ドメイン名のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096823"
---
# <a name="configure-your-domain-name"></a>ドメイン名のコンフィギュレーション


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 E コマース サイトのドメイン名をコンフィギュレーションする方法について説明します。 

## <a name="add-domains-during-e-commerce-initialization"></a>E-コマースの初期化中にドメインを追加する

ドメインを E コマース環境に関連付けるには、[新しい E コマース サイトの配置](deploy-ecommerce-site.md) に記載され E コマースを初期化します。 初期化中、E コマース環境のプロビジョニングに使用する情報を提供するように求められます。 **サポートされるホスト名**フィールドに、この環境で使用する予定のすべてのドメインを追加します。 複数のドメインはセミコロンで区切る必要があります。 この方法で、全ての必要な E コーマース コンポーネントでドメインがコンフィギュレーションされ、それらは、コンテンツ配信ネットワーク (CDN) または Web サーバーからのトラフィックを切り替えて、それを E コマース フロント エンドにポイントする際に使用することができます。

## <a name="add-domains-after-e-commerce-initialization"></a>E-コマースの初期化後にドメインを追加する

E コマースの初期化後に新しいドメインを E コマース環境に関連付けるには、サービス要求を送信する必要があります。

## <a name="additional-resources"></a>追加リソース

[新しい E コマース サイトの配置](deploy-ecommerce-site.md)

[オンライン ストア チャネルのセットアップ](online-stores.md)

[E コマース サイトの作成](create-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
