---
title: Dynamics 365 Commerce のドメイン
description: この記事では、Microsoft Dynamics 365 Commerce でのドメインの処理方法について説明します。
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750683"
---
# <a name="domains-in-dynamics-365-commerce"></a>Dynamics 365 Commerce のドメイン

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce でのドメインの処理方法について説明します。

ドメインは Web ブラウザーで Dynamics 365 Commerce サイトに移動するために使用される Web アドレスです。 選択したドメイン ネーム サーバー (DNS) プロバイダーを使用して、ドメインの管理を制御します。 ドメインは、Dynamics 365 Commerce サイト ビルダー全体で参照され、公開時のサイトへのアクセス方法を調整します。 この記事では、Commerce サイトの開発と立ち上げのライフサイクルを通じてドメインがどのように処理および参照されるかを確認します。

> [!NOTE]
> 2022 年 5 月 6 日現在、Dynamics 365 Commerce で作成されたすべての環境は、以前の `.commerce.dynamics.com` のパターンに代わり、`.dynamics365commerce.ms` ドメインでプロビジョニングされます。 `.commerce.dynamics.com` ドメインでプロビジョニングされた既存の環境は引き続き機能します。

## <a name="provisioning-and-supported-host-names"></a>プロビジョニングおよびサポートされているホスト名

[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) で e コマース環境をプロビジョニングする場合 、e コマース プロビジョニング画面の **サポートされているホスト名** ボックスを使用して、展開された Commerce 環境に関連付けられるドメインを入力します。 これらのドメインは、e コマース Web サイトがホストされる顧客向けドメイン ネーム サーバー (DNS) 名になります。 この段階でドメインを入力しても、ドメインのトラフィックを Dynamics 365 Commerce に振り向けることはありません。 ドメインのトラフィックは、ドメインで Commerce エンドポイントを使用するように DNS CNAME レコードが更新された場合にのみ、Commerce エンドポイントにルーティングされます。

> [!NOTE]
> 複数のドメインをセミコロンで区切ることによって、**サポートされているホスト名** ボックスに入力できます。

次の図は、**サポートされているホスト名** ボックスが強調表示された LCS E コマース プロビジョニング画面を示しています。 

![**サポートされているホスト名** ボックスが強調表示された LCS E コマース プロビジョニング画面。](./media/Domains_ProvisioningeCommerceScreen_publish.png)

プロビジョニングが既に行われている場合は、サービス要求を作成して環境にドメインを追加できます。 LCS でサービス要求を作成するには、環境内で **サポート \> サポートの問題** に移動し、**インシデントの送信** を選択します。

## <a name="commerce-generated-urls"></a>Commerce 生成の URL

Dynamics 365 Commerce e コマース環境をプロビジョニングする際、Commerce は環境の作業用アドレスとなる URL を生成します。 この URL は、環境のプロビジョニング後に、LCS に表示されている e コマース サイトのリンクで参照されます。 Commerce 生成の URL は、`https://<e-commerce tenant name>.dynamics365commerce.ms` の形式で、e コマース テナント名は、Commerce 環境に対して LCS に入力された名前です。

サンドボックス環境では、実稼働環境サイトのホスト名を使用することもできます。 このオプションは、サンドボックス環境から運用環境にサイトをコピーする場合に最も適しています。

## <a name="site-setup"></a>サイトの設定

e コマース環境のプロビジョニング後、サイトを作業用 URL に関連付けるように、サイトを Commerce サイト ビルダーで設定する必要があります。

サイト ビルダーで初めてサイトを設定すると、**サイトの設定** ダイアログ ボックスが表示されます。

次の図は、サイト ビルダーで初めてサイトにアクセスするときの、"default" という名前のサイトの **サイトの設定** ダイアログ ボックスを示しています。

![**サイトの設定** ダイアログ ボックス。](./media/Domains_SetupyoursiteScreen.png)

**ドメインの選択** ボックスを使用すると、LCS でサイトに用意されている、サポートされているホスト名の 1 つをサイト ビルダーでサイトに関連付けることができます。

**パス** ボックスは空白のままにするか、作業 URL に反映される追加のパス文字列を追加できます。 **パス** ボックスを空白のままにすると、Commerce 生成のベース URL が、サイト ビルダーで設定されているサイトに関連付けられます。 パスは、サイト/ドメインのペアごとに一意である必要があります。 選択したサイトおよびドメイン内では、環境内の 1 つのサイトのみが空白のパスを使用するか、一意のパス文字列に関連付けることができます。 サイトのセットアップ時に **パス** フィールドに追加された文字列は、Web ブラウザーでサイトにアクセスするために使用される Commerce 生成のベース URL のサブパスになります。

> [!NOTE]
> パスは、サイト ビルダーの **サイトの設定 \> チャネル** コンフィギュレーション セクションでチャネルを追加するときに、**一致パス** とも呼ばれます。

たとえば、"xyz" という名前の e コマース テナントでサイト ビルダーに "fabrikam" というサイトがあり、空白のパスでサイトを設定した場合、次の Commerce 生成のベース URL に直接アクセスすることによって、Web ブラウザーで公開サイトのコンテンツにアクセスします:

`https://xyz.dynamics365commerce.ms`

また、この同じサイトのセットアップ時に "fabrikam" のパスを追加した場合は、次の URL を使用して、Web ブラウザーで公開サイトのコンテンツにアクセスします:

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>ページと URL

サイトがパスで設定されると、サイト ビルダーのページに関連付けられているすべての URL が、サイトの作業 URL (Commerce 生成の URL または Commerce 生成の URLとパス) に基づいてビルドされます。 **新しい URL** ダイアログ ボックスの一覧からページを選択し、そのページの URL パスを入力することによって、サイト ビルダー (**URL /> + 新規**) で新しい URL を作成すると、その URL が選択したページに関連付けられます。 URL パス値は、そのページにアクセスするためにサイトの作業 URL に追加され、サイト ビルダーの **URL** ページの URL リストで `./<URL path>` のラベルが付けられます。

次の図は、URL パスの例が強調表示されたサイト ビルダーの **新しい URL** ダイアログ ボックスを示しています。 

![サイト ビルダーの **新しい URL** ダイアログ ボックス。](./media/Domains_PageSetup2a.png)

次の図は、URL の例が一覧で強調表示されたサイト ビルダーの **URL** ページを示しています。

![ポリシー フローでのユーザー フロー オプションの実行。](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>サイト ビルダーのドメイン

サポートされているホスト名の値は、サイトの設定時にドメインとして関連付けることができます。 サポートされているホスト名の値をドメインとして選択すると、サイト ビルダー全体で参照されている選択されたドメインが表示されます。 このドメインは、Commerce 環境内の参照にすぎず、そのドメインのライブ トラフィックはまだ Dynamics 365 Commerce に転送されません。

サイト ビルダーでサイトを操作するときに、2 つの異なるドメインで 2 つのサイトを設定している場合、**?domain=** 属性を作業 URL に追加して、ブラウザーで公開サイトのコンテンツにアクセスできます。

たとえば、環境 "xyz" がプロビジョニングされ、サイト ビルダーに 2 つのサイトが作成されて、1 つはドメイン `www.fabrikam.com` で、もう 1 つはドメイン `www.constoso.com` に関連付けられています。 各サイトは空白のパスを使用して設定されました。 この 2 つのサイトは、**?domain=** 属性を使用して、次のように Web ブラウザーでアクセスできます:
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

複数のドメインが提供されている環境でドメインのクエリ文字列が指定されていない場合、Commerce は提供された最初のドメインを使用します。 たとえば、サイトの設定中に最初にパス "fabrikam" が提供された場合、その URL `https://xyz.dynamics365commerce.ms` を使用して、`www.fabrikam.com` の公開サイトのコンテンツ サイトにアクセスできます。

カスタム ドメインを追加することも可能です。 これを行うには、プロジェクトの環境の Commerce 管理ページの **E コマース** サブヘッダーで、**+ カスタム ドメインの追加** を選択します。 スライダーは既存のカスタム ドメインを示し、新しいカスタム ドメインを追加するオプションを提供します。

## <a name="update-which-commerce-scale-unit-is-used"></a>使用する Commerce Scale Unit の更新

Commerce で使用される Commerce Scale Unit (CSU) は、環境を最初に作成するときに選択されるのが一般的です。 Commerce では、環境で使用する CSU インスタンスを変更できるため、セルフサービス機能によりアーキテクチャの保守を向上させ、サポートへの問い合わせを減らすることができます。 CSU インスタンスを更新するには、プロジェクトの環境の Commerce 管理ページに移動し、**Scale Unit を更新する** を選択します。 **新しい Commerce Scale Unit** スライダーを使用して、環境で使用できる CSU の一覧から新しい CSU インスタンスを選択します。

## <a name="traffic-forwarding-in-production"></a>実稼働環境でのトラフィックの転送

Commerce.dynamics.com エンドポイント自体でドメインのクエリ文字列パラメータを使用して、複数のドメインをシミュレートできます。 ただし、実稼働環境で稼働させる必要がある場合は、カスタム ドメインのトラフィックを `<e-commerce tenant name>.dynamics365commerce.ms` エンドポイントに転送する必要があります。

`<e-commerce tenant name>.dynamics365commerce.ms` エンドポイントは、カスタム ドメイン Secure Sockets Layer (SSL) をサポートしていないため、フロント ドア サービスまたは Content Delivery Network (CDN) を使用してカスタム ドメインを設定する必要があります。 

フロント ドア サービスまたは CDN を使用してカスタム ドメインを設定するには、次の 2 つのオプションがあります:

- Azure Front Door のようなフロント ドア サービスを設定して、フロントエンドのトラフィックを処理し、Commerce 環境に接続することで、ドメインと証明書の管理をより詳細に制御し、きめ細かなセキュリティ ポリシーを提供します。

- Commerce が提供する Azure Front Door インスタンスを使用することで、ドメイン検証のために Dynamics 365 Commerce チームとアクションを調整し、運用環境ドメインの SSL 証明書を取得する必要があります。

> [!NOTE]
> 外部の URL または前もったサービスを使用している場合は、Commerce が提供するリポートを使用して Commerce プラットフォームに上陸し、X-Forwarded-Host (XFH) ヘッダー \<custom-domain\> が設定された Commerce プラットフォームに要求が上陸する必要があります。 たとえば、Commerce エンドポイント `xyz.dynamics365commerce.ms` で、カスタム ドメインが `www.fabrikam.com` である場合は、転送される要求のホスト ヘッダーは、`xyz.dynamics365commerce.ms` である必要があり、XFH ヘッダーも `www.fabrikam.com` である必要があります。

CDN サービスを直接設定する方法の詳細については、[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md) を参照してください。

Commerce 提供の Azure Front Door インスタンスを使用するには、Commerce オンボード チームから CDN 設定支援のサービス要求を作成する必要があります。 

- 会社名、運用環境ドメイン、環境 ID、および運用環境の eコマース テナント名を入力する必要があります。 
- このサービス要求が既存のドメイン (現在アクティブなサイトに使用されている) か、新しいドメインであるかを確認する必要があります。 
- 新しいドメインの場合、ドメイン検証と SSL 証明書は 1 つのステップで実行できます。 
- 既存の Web サイトに提供するドメインの場合、ドメイン検証と SSL 証明書を確立するために必要ないくつかのステップ プロセスがあります。 このプロセスには、複数の連続したステップが含まれているため、ドメインが稼働するために 7 営業日のサービス レベル契約 (SLA) があります。

LCS でサービス要求を作成するには、環境内で **サポート \> サポートの問題** に移動し、**インシデントの送信** を選択します。

> [!NOTE]
> SSL を使用したカスタム ドメインは、運用環境でのみサポートされます。 サンドボックスやユーザー受け入れテスト (UAT) などの非運用環境の場合、Commerce 生成の URL を使用して、Web ブラウザーで公開されたコンテンツにアクセスします。

## <a name="ssl-certificate-process"></a>SSL 証明書プロセス

サービス要求が提出されると、Commerce チームは次の手順をユーザーと調整します。

新しいドメインの場合:
- Commerce チームは Azure Front Door インスタンス (Commerce ホスト) を設定します。
- その後、Commerce チームは、カスタム ドメインをポイントする CNAME レコードを提供します。
- CNAME レコードが更新されると、Commerce ホストの Azure Front Door インスタンスは、ドメインの所有権を確認して SSL 証明書を取得できるようになります。

既存/アクティブ ドメインの場合:
- Commerce チームは、ドメイン DNS プロバイダーに提供する `afdverify.<custom-domain>` CNAME レコードを追加するように指示します。
- 完了すると、Commerce チームは、ドメインを Azure Front Door インスタンスに追加し、ドメインの DNS に追加する追加の DNS TXT レコードを提供します。
- TXT レコードが完了すると、Commerce チームは、SSL 証明書を設定するドメインに対して Azure Front Door の更新を完了します。

## <a name="apex-domains"></a>Apex ドメイン

Commerce 提供の Azure Front Door インスタンスは、apex ドメイン (サブドメインを含まないルート ドメイン) をサポートしていません。 Apex ドメインは解決するために IP アドレスを必要とし、Commerce Azure Front Door インスタンスは仮想エンドポイントでのみ存在します。 Apex ドメインを使用するには、次のオプションがあります。

- **オプション 1** - DNS プロバイダーを使用して、apex ドメインを "www" ドメインにリダイレクトします。 たとえば、fabrikam.com は `www.fabrikam.com` にリダイレクトし、`www.fabrikam.com` は、Commerce ホストの Azure Front Door インスタンスをポイントする CNAME レコードです。

- **オプション 2** - DNS プロバイダーが ALIAS レコードをサポートしている場合、Apex ドメインを Azure Front Door エンドポイントにポイントできます。これにより、エンドポイントによる IP 変更が確実に反映されます。 Azure Front Door インスタンスを自分でホストする必要があります。
  
- **オプション 3** - DNS プロバイダーが ALIAS レコードをサポートしていない場合は、DNS プロバイダーを Azure DNS に変更し、Azure DNS と Azure Front Door インスタンスの両方を自分でホストする必要があります。

> [!NOTE]
> Azure Front Door を使用している場合は、同じサブスクリプションで Azure DNS も設定する必要があります。 Azure DNS でホストされている apex ドメインは、Azure Front Door をエイリアス レコードとしてポイントできます。 Apex ドメインは常に IP アドレスをポイントする必要があるため、これが唯一の回避策です。
  
複数のドメインについて不明な点がある場合は、[Microsoft サポート](https://support.microsoft.com/) に問い合わせください。

  ## <a name="additional-resources"></a>追加リソース

  [新しい eコマース テナントの配置](deploy-ecommerce-site.md)

  [オンライン ストア チャネルのセットアップ](./channel-setup-online.md)

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
