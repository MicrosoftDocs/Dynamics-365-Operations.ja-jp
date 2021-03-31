---
title: Cookie のコンプライアンス
description: このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10a58cf7197d2a8596107a42174b35350e72ae11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215700"
---
# <a name="cookie-compliance"></a>Cookie のコンプライアンス

[!include [banner](includes/banner.md)]

このトピックでは、Cookie のコンプライアンスおよび Microsoft Dynamics 365 Commerce に含まれる既定のポリシーに関する考慮事項について説明します。

## <a name="overview"></a>概要

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