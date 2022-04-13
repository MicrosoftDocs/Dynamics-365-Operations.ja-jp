---
title: 電子商取引サイトの概要
description: このトピックでは、Microsoft Dynamics 365 Commerce における eコマース サイトのサポートの概要について説明します。
author: bicyclingfool
ms.date: 11/05/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 90f0f01115b00f231af8d4ae11be1d18d379399b
ms.sourcegitcommit: 6f6ec4f4ff595bf81f0b8b83f66442d5456efa87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2022
ms.locfileid: "8487771"
---
# <a name="e-commerce-site-overview"></a>eコマース サイトの概要

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce における eコマース サイトのサポートの概要について説明します。 これには、Dynamics 365 Commerce で電子商取引オンライン ストアが初期化および管理される方法に関する情報が含まれています。 また、オンラインストア、および電子商取引サイトの設定と構成の方法に関する詳細情報へのリンクも提供します。 このトピックでは、多くの基本的な概念について説明しますが、生産的な電子商取引サイトの設定に必要なものすべてについては説明しません。 詳細なトピックについては、Dynamics 365 Commerce ドキュメントを参照してください。

## <a name="online-store-channel"></a>オンライン ストア チャネル

Dynamics 365 Commerce で新しいサイトを構築する前に、少なくとも 1 つのオンライン ストア チャネルを設定する必要があります。 詳細については、[オンライン チャンネルの設定](channel-setup-online.md)を参照してください。 

Dynamics 365 Commerce では、オンライン ストア チャネルを使用して、製品、価格決定、言語、支払方法、出荷方法、補充センターなど、顧客が利用できるオンライン エクスペリエンスの側面を確立します。

Dynamics 365 Commerce の使用を開始する前に、設定する必要があるオンライン ストア チャネルは 1 つだけです。 ただし、1 つの電子商取引サイトは、複数のオンライン ストアにオンライン エクスペリエンスを提供できます。 たとえば、異なる地理的地域をサポートするように複数のオンライン ストアが設定されている場合、単一の電子商取引ページ セットを使用して、各ストアで定義されている固有のエクスペリエンスを提供できます。 複数のオンライン ストアをサポートするようにサイトを構成する方法の詳細については、[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)を参照してください。

オンライン ストアが設定されると、オンライン ストアフロントとして機能する Dynamics 365 Commerce サイトに関連付けることができます。 オンライン ストアとその設定方法の詳細については、[オンライン ストアの設定](/dynamics365/unified-operations/retail/online-stores)を参照してください。

## <a name="deploy-a-new-e-commerce-tenant"></a>新しい eコマース テナントのデプロイ

電子商取引サイトの初期化中に、ドメイン名の入力を求めるメッセージが表示されます。 Commerce のドメインの詳細については、[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)[Dynamics 365 Commerce のドメイン](domains-commerce.md)を参照してください。 [Microsoft Dynamics Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide) を使用して新しい電子商取引のテナントを配置するには、[新しい電子商取引テナントの配置](deploy-ecommerce-site.md)を参照してください。 電子商取引のテナントが LCS で設定された後に、Commerce サイト ビルダーへのリンクが提供されます。 その後、Commerce サイト ビルダーを使用して、電子商取引サイトを初期化および構成することができます。

## <a name="initialize-your-e-commerce-site"></a>電子商取引サイトの初期化

LC から Commerce サイト ビルダーを起動すると、**サイト** ページが表示されます。 このページには、次の図の例に示すように、**既定** と **fabrikam** の 2 つの事前構成されたサイトが含まれています。

![Commerce サイト ビルダーのサイト ページ。](media/e-commerce-site-01.png)

これらのサイトのいずれかを選択すると、ドメイン名、既定のオンライン チャンネル、選択したチャンネルでサポートされている言語、およびパスを選択するように求められます。 1 つのチャネルだけを使用する場合は、パスを空白のままにしておくことができます。 後で、オンラインの店舗のチャネルまたは言語を Commerce サイト ビルダーで構成できます。 追加のチャネルまたは言語ごとに、固有のパスが必要です。 たとえば、1 つのサイトに関連付けられている 2 つのオンライン チャネルがあり、そのサイトのドメイン名は `www.fabrikam.com` であるとします。 この場合、1つのチャネルのパスをパスのない既定値 (`https://www.fabrikam.com`) にすることができ、2 番目のチャネルを **site2** などの新しいパスに設定できます。URL は `https://www.fabrikam.com/site2` になります。 次の図は、Commerce サイト ビルダーのサイトの初期化ダイアログ ボックスの例を示しています。

![Commerce サイト ビルダーのサイトの初期化ダイアログ ボックス。](media/e-commerce-site-02.png)

**サイト** ページには、**新しいサイト** ボタンも含まれています。 このボタンを選択したときに表示されるダイアログ ボックスは、サイトの初期化ダイアログ ボックスに似ていますが、新しいサイトを作成するために使用されます。 新しいサイトは空白になっています。 これには、**既定の** サイトと **fabrikam** サイトに用意されている既定のテンプレート、フラグメント、ページ、およびイメージは含まれません。 ただし、必要に応じて、サポート チケットを開いて、新しい空のサイトに既定のコンテンツのコピーを追加するように要求することができます。 詳細については、[E コマース サイトの作成](create-ecommerce-site.md)を参照してください。

新しいサイトが初期化されると、Commerce サイト ビルダーの **ホーム** ページが表示されます。 このページには、次の図の例に示すように、一般的なアクションとガイダンスのコンテンツへのリンクが含まれています。

![Commerce サイト ビルダーのホーム ページにあるリンク。](media/e-commerce-site-03.png)

## <a name="modify-online-store-channels-or-add-online-store-channels-to-an-e-commerce-site"></a>オンライン ストア チャネルの変更、または電子商取引サイトへのオンライン ストア チャネルの追加

電子商取引サイトを作成した後、そのサイトに関連付けられているチャネルを変更するには、[電子商取引サイトをオンライン チャネルに関連付ける](associate-site-online-store.md)の手順に従ってください。 次の図の例は、**チャネル** ページ (**サイト設定 \> チャンネル**) でチャンネルの作業単位番号 (OUN) を変更する方法を示しています。 変更が完了したら、**保存して発行** をクリックします。 これにより、変更が確実に発行されます。

![Commerce サイト ビルダーのチャネル ページ。](media/e-commerce-site-04.png)

新しいチャネルを追加するには、**チャンネルの追加** を選択します。 チャネルに新しい言語を追加するには、チャネルを選択し、表示されるチャネル ダイアログ ボックスで **ロケールの追加** を選択します。 ダイアログ ボックスにロケールを表示するには、あらかじめロケールを設定しておく必要があります。

![Commerce サイト ビルダーのチャネル ダイアログ ボックス。](media/e-commerce-site-05.png)

## <a name="set-up-an-azure-b2c-tenant"></a>Azure B2C テナントの設定

Dynamics 365 Commerce は Azure Active Directory (Azure AD) 企業と顧客間 (B2C) を使用して、ユーザーの資格情報と認証フローをサポートします。 Azure B2C テナントの設定方法の詳細については、[Commerce での B2C テナントの設定](set-up-b2c-tenant.md)、[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)、[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-b2c-tenants.md)を参照してください。

## <a name="overview-of-the-default-site-pages"></a>既定のサイト ページの概要

**既定の** サイトと **fabrikam** のサイトには、開始するのに役立つコンフィギュレーション済みテンプレート、フラグメント、およびページが用意されています。 詳細については、次のトピックを参照してください。

- [ホーム ページの概要](quick-tour-home-page.md)
- [製品詳細ページの概要](quick-tour-pdp.md)
- [買い物カゴとチェック アウト ページの概要](quick-tour-cart-checkout.md)
- [アカウント管理ページの概要](quick-tour-account-management.md)

## <a name="manage-site-settings"></a>サイト設定の管理

サイト設定を管理する方法については、次のトピックを参照してください。

- [E コマース ユーザーとロールの管理](manage-ecommerce-users-roles.md)
- [サイトにおける検索エンジンの最適化 (SEO) の考慮事項](search-engine-optimization-considerations.md)
- [コンテンツ セキュリティ ポリシー (CSP) の管理](manage-csp.md)
- [サイト テーマの選択](select-site-theme.md)

## <a name="manage-site-content"></a>サイト コンテンツの管理

サイトのコンテンツを管理する方法については、次のトピックを参照してください。

- [ページ モデルの用語集](page-elements-overview.md)
- [ドキュメントの状態とライフサイクル](document-states-overview.md)
- [テンプレートとレイアウト](templates-layouts-overview.md)
- [フラグメントで動作](work-with-fragments.md)
- [モジュールで動作](work-with-modules.md)
- [デジタル資産管理の概要](dam-overview.md)
- [モジュール ライブラリの概要](starter-kit-overview.md)

## <a name="additional-resources"></a>追加リソース

[eコマース サイトの作成](create-ecommerce-site.md)

[新しい E コマース サイトの配置](deploy-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]