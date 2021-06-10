---
title: Cookie のコンプライアンス
description: このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。
author: BrianShook
ms.date: 05/21/2021
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
ms.openlocfilehash: 8eb610eb819dee09a30368257e36dc88f855e985
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088390"
---
# <a name="cookie-compliance"></a>Cookie のコンプライアンス

[!include [banner](includes/banner.md)]

このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。

eコマースの顧客に影響を与える追跡技術が使用される場合は、プライバシーが重要な要素になります。 欧州連合 (EU) の一般データ保護規則 (GDPR) などのプライバシー コンプライアンス基準により、現在有効な任意のサイトでは電子プライバシー ガイドラインを考慮する必要があります。 多くの E コマース サイトは既定でグローバルにアクセスできるため、E コマース サイトのコンプライアンス基準を確認することが重要です。

Microsoft が Cookie のコンプライアンスに使用する基本原則の詳細については、[Microsoft Trust Center](https://www.microsoft.com/trust-center) を参照してください。 そのサイトでは、コンプライアンスおよびプライバシーの領域に関する詳細情報も取得できます。

次の表に、Dynamics 365 Commerce サイトによって配置された Cookie の現在の参照一覧を示します。

| Cookie 名                               | 使用状況                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| .AspNet.Cookies                             | シングルサインオン (SSO) 用の Microsoft Azure Active Directory (Azure AD) の認証 Cookie を保存します。 暗号化されたユーザー プリンシパル情報 (名前、姓、メール) を保存します。 |
| &#95;msdyn365___cart&#95;                           | カート インスタンスに追加された製品の一覧を取得するために使用される店舗カート ID。 |
| &#95;msdyn365___ucc&#95;                            | Cookie 準拠の承認追跡。                          |
| ai_session                                  | アプリの特定のページと機能を含むユーザー アクティビティのセッション数が検出されます。 |
| ai_user                                     | アプリとその機能を使用した人の数が検出されます。 ユーザーは匿名 ID を使用してカウントされます。 |
| b2cru                                       | リダイレクト URL を動的に格納します。                              |
| JSESSIONID                                  | ユーザー セッションを保存するために支払コネクタ Adyen によって使用されます。       |
| OpenIdConnect.nonce.&#42;                       | 認証                                               |
| x-ms-cpim-cache:.&#42;                          | 要求の状態を維持するために使用されます。                      |
| x-ms-cpim-csrf                              | CRSF から保護するためにクロスサイト リクエスト フォージェリ (CRSF) トークンが使用されています。     |
| x-ms-cpim-dc                                | 適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。 |
| x-ms-cpim-rc.&#42;                              | 適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。 |
| x-ms-cpim-slice                             | 適切なプロダクション認証サーバー インスタンスに要求を転送するために使用されます。 |
| x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0 | SSO セッションを維持するために使用されます。                        |
| x-ms-cpim-trans                             | 現在のトランザクションなど、トランザクションを追跡するために使用されます (企業からコンシューマー (B2C) サイトに対して認証されている開いたタブの数)。 |
| \_msdyn365___muid_                            | 環境で実験が有効になっている場合に使用され、実験のための userId として利用されます。 |
| \_msdyn365___exp_                             | 環境で実験が有効になっている場合に使用され、パフォーマンスの負荷分散を測定するために使用されます。         |
| d365mkt                                       | **サイト設定 > 一般 > 位置情報に基づく店舗の検出** の Commerce site builder で、ユーザーの IP アドレスを追跡して店舗の位置情報を提案する位置情報検出が有効になっている場合に使用します。      |

サイト ユーザーがサイト内のソーシャル メディア リンクを選択した場合、次の表の Cookie もユーザーのブラウザーで追跡されます。


| ドメイン                      | Cookie               | 説明                                                  | 配賦元                                          |
| --------------------------- | ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| .linkedin.com                | UserMatchHistory         | LinkedIn 広告 ID の同期                                      | LinkedIn フィードと分析情報タグ                                |
| .linkedin.com               | li_sugr                  | ブラウザーの識別子                                           | 指定した国に IP アドレスがない場合の LinkedIn 分析情報タグ |
| .linkedin.com               | BizographicsOptOut       | サード パーティの追跡のオプトアウト ステータスを決定します。              | LinkedIn ゲスト コントロールと業界のオプトアウト ページ           |
| .linkedin.com               | \_guid                    | Google 広告のブラウザーの識別子。                            | LinkedIn フィード                                                |
| .linkedin.com               | li_oatml                 | 変換の追跡、リターゲット、および分析のメンバーの間接識別子。 | LinkedIn 広告と分析情報タグ                                |
| 各種ファースト パーティのドメイン | li_fat_id                | 変換の追跡、リターゲット、および分析のメンバーの間接識別子。 | LinkedIn 広告と分析情報タグ                                |
| .adsymptotic.com            | U                        | ブラウザーの識別子                                           | 指定した国に IP アドレスがない場合の LinkedIn 分析情報タグ |
| .linkedin.com                | bcookie                  | ブラウザ ID Cookie                                            | LinkedIn への要求                                         |
| .linkedin.com                | bscookie                 | セキュア ブラウザ Cookie                                        | LinkedIn への要求                                         |
| .linkedin.com               | lang                     | 既定のロケールと言語を設定します。                                 | LinkedIn への要求                                         |
| .linkedin.com                | lidc                     | ルート指定に使用されます。                                             | LinkedIn への要求                                         |
| .linkedin.com               | aam_uuid                 | Adobe オーディエンス マネージャー Cookie                                                     | ID 同期の設定                                              |
| .linkedin.com               | \_ga                      | Google アナリティクス Cookie                                            | Google アナリティクス                                             |
| .linkedin.com               | \_gat                     | Google アナリティクス Cookie                                             | Google アナリティクス                                             |
| .linkedin.com               | liap                     | Google アナリティクス Cookie                                             | Google アナリティクス                                             |
| .linkedin.com               | lissc                    |                                                              |                                                              |
| .facebook.com               | c_user                   | Cookie には、現在サインインしているユーザーのユーザー ID が含まれます。  |   Facebook                                                           |
| .facebook.com               | datr                     | サインインしたユーザーとは別に、Facebook への接続に使用された Web ブラウザーを識別するために使用されます。 | Facebook                                                             |
| .facebook.com               | wd                       | ブラウザーのウィンドウ分析コードを保存し、Facebook がページのレンダリングを最適化するために使用されます。 | Facebook                                                             |
| .facebook.com               | xs                       | セッション番号を表す 2 桁の番号。 値の 2 番目の部分は、セッション シークレットです。 |  Facebook                                                            |
| .facebook.com               | fr                       | 固有のブラウザーおよびユーザー ID を含み、ターゲット広告に使用されます。 |  Facebook                                                            |
| .facebook.com               | sb                       | Facebook の友達提案を改善するために使用されます。                                |  Facebook                                                            |
| .facebook.com               | spin                     |                                                              |  Facebook                                                            |
| .twitter.com                | guest_id                 |                                                              |  Twitter                                                            |
| .twitter.com                | kdt                      |                                                              |  Twitter                                                             |
| .twitter.com                | personalization_id       | Cookie には、現在サインインしているユーザーのユーザー ID が含まれます。  |  Twitter                                                             |
| .twitter.com                | remember_checked_on      |                                                              | Twitter                                                              |
| .twitter.com                | twid                     |                                                              |  Twitter                                                             |
| .pinterest.com              | \_auth                    | Cookie には、現在サインインしているユーザーのユーザー ID が含まれます。  |   Pinterest                                                           |
| .pinterest.com              | \_b                       |                                                              |   Pinterest                                                           |
| .pinterest.com              | \_pinterest_pfob          |                                                              |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_referrer      | Cookie には、ユーザーが Pinterest ボタンを選択した場合のページが含まれます。      |  Pinterest                                                            |
| .pinterest.com              | \_pinterest_sess          | Cookie には、ユーザーが Pinterest ボタンを選択した場合のページが含まれます。      |  Pinterest                                                            |
| .pinterest.com              | \_routing_id              |                                                              |  Pinterest                                                            |
| .pinterest.com              | bei                      |                                                              |  Pinterest                                                            |
| .pinterest.com              | cm_sub                   | ユーザー ID と、Cookie が作成されたタイムスタンプが含まれます。 |  Pinterest                                                            |
| .pinterest.com              | csrftoken                | Cookie には、ユーザーが Pinterest ボタンを選択した場合のページが含まれます。      | Pinterest                                                             |
| .pinterest.com              | sessionFunnelEventLogged | Cookie には、ユーザーが Pinterest ボタンを選択した場合のページが含まれます。      | Pinterest                                                             |
| .pinterest.com              | ローカル ストレージ            |                                                              |  Pinterest                                                            |
| .pinterest.com              | サービス作業員          |                                                              |  Pinterest                                                            |


## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a>電子商取引サイトにおけるサイト利用者向け cookie の同意 

電子商取引サイトの機能、またはモジュールが必須ではない Cookie を使用している場合は、サイト利用者の同意を取得してから、cookie を追跡する必要があります。 サイト利用者が電子商取引サイトで cookie の同意を得られるようにするには、サイトの作成者が、ページのヘッダーモジュールに cookie の同意モジュールを追加および構成して、cookie の同意を要求し、同意を得られたことを確認する必要があります。 イト利用者の同意は、非必須の cookie を使用した機能、またはモジュールがサイトのページに表示される前に得なければなりません。

## <a name="additional-resources"></a>追加リソース

[ユーザー補助機能](accessibility.md)

[コンプライアンスの概要](compliance-overview.md)

[プライバシー ポリシー ページの追加](add-privacy-page.md)

[追跡しているコンテンツの変更に関連付いたユーザー ID の置換](replace-IDs-tracked-changes.md)

[Cookie の同意モジュール](cookie-consent-module.md) 
 
[ヘッダー モジュール](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
