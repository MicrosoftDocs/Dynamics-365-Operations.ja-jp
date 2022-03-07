---
title: Dynamics 365 Commerce 認証フロー
description: このトピックでは、Microsoft Dynamics 365 Commerce のさまざまな認証フローの概要を示します。
author: samjarawan
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: samjar
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 2e7f4d2c06e60cc14b32d5aa9b8c4167d8304b52c67d6ff1a39cdea462682460
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735692"
---
# <a name="dynamics-365-commerce-authentication-flows"></a>Dynamics 365 Commerce 認証フロー

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のさまざまな認証フローの概要を示します。 Dynamics 365 Commerce ソリューションは現在、複数の認証シナリオとフローをサポートしていますが、Commerce Scale Unit (ヘッドレス コマース エンジンとも呼ばれる) のコア認証インフラストラクチャは、完全に [OpenID connect](https://openid.net/connect/) に基づいています。

## <a name="authentication-methods"></a>認証方法

Commerce Scale Unit の各アプリケーション プログラミング インターフェイス (API) へのアクセスは、次の 1 つ以上の役割によってネイティブに制限されます。

- **従業員** – このロールに関連付けられている API にアクセスするには、販売時点管理 (POS) デバイスの有効化 (デバイス トークン) と認証済従業員が必要です。
- **顧客** – このロールに関連付けられている API へのアクセスには、認証済顧客が必要です。 通常、E コマース サイトでは、これらの API を使用して、注文履歴の取得や顧客の詳細の変更などの操作を実行します。
- **アプリケーション** – このロールに関連付けられている API にアクセスするには、Azure Active Directory (Azure AD) サービスとサービス間認証などのアプリケーション レベルの認証が必要です。
- **匿名** – このロールに関連付けられている API は、主にユーザー認証を行わずに E コマース サイトによって使用されます。
- **カスタムされた API** – このロールに関連付けられている API へのアクセスを制限するには、POS デバイスの有効化、顧客認証、匿名認証などの方法を使用します。

Commerce Scale Unit API とそのアクセス制限の完全な一覧については、[Commerce Scale Unit 顧客およびコンシューマー API](/dev-itpro/retail-server-customer-consumer-api) を参照してください。

### <a name="supported-authentication-methods"></a>サポートされている認証方法

次の表では、デバイス トークンを生成する POS デバイスの有効化、またはユーザー トークンを生成するユーザー認証のいずれかを必要とする API に対して、サポートされている認証方法のセットについて説明します。

| API カテゴリ | シナリオ | サポートされている認証方法 | 必要な設定 | 追加の詳細 |
|----------|-----------|------------|------------|------------|
| 従業員 | Dynamics 365 POS 認証フロー\* | 単純レジ担当者のユーザー名とパスワード | Dynamics 365 Commerce 本社で、作業者のユーザー名とパスワードをコンフィギュレーションします。 | [作業者を作成](retail-modern-pos-device-activation.md#create-a-worker) |
| 従業員 | Dynamics 365 POS 認証フロー\* | Azure AD 資格情報 | Commerce 本社で、Azure AD の資格情報にマップされる作業者をコンフィギュレーションします。 | [POS サインインの Azure Active Directory 認証を有効にする](aad-pos-logon.md) |
| 従業員 | Dynamics 365 POS 認証フロー\* | 拡張サインイン資格情報 (たとえば、バーコードまたは磁気ストライプリーダー \[MSR\] を使用) | Commerce 本社で、拡張サインインの作業者をコンフィギュレーションします。 | [MPOS および Cloud POS の拡張ログオン機能の設定](extended-logon.md) |
| 顧客 | Dynamics 365 Commerce 認証フロー | Azure AD B2C を使用したサイトユーザー認証 | <ol><li>Azure AD 企業と顧客間 (B2C) アプリケーションを作成します。</li><li>Commerce 本社で、Azure AD B2C アプリケーションを、ID プロバイダーの承認済みリストに追加します。</li><li>Commerce サイト ビルダー で Azure AD B2C アプリケーションをコンフィギュレーションします。</li></ol> | [Commerce での B2C テナントの設定](set-up-b2c-tenant.md)<p>[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)</p> |
| 顧客 | Dynamics 365 Commerce 認証フロー | OpenID Connect をサポートする外部 ID プロバイダーを使用したサイト ユーザー認証 | <ol><li>Azure AD B2C アプリケーションを作成し、外部 ID プロバイダーをサポートするようにコンフィギュレーションします。</li><li>Commerce 本社で、Azure AD B2C アプリケーションを、ID プロバイダーの承認済みリストに追加します。</li><li>Commerce サイト ビルダー で Azure AD B2C アプリケーションをコンフィギュレーションします。</li></ol> | [Commerce での B2C テナントの設定](set-up-b2c-tenant.md)<p>[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)</p> |
| 顧客 | サード パーティ E コマースの認証フロー | OpenID Connect をサポートする外部 ID プロバイダーを使用したサイト ユーザー認証 | Commerce 本社で、外部 ID プロバイダーを ID プロバイダーの承認済みリストに追加します。 | [認証プロバイダーのコンフィギュレーション](/dev-itpro/configure-authentication-providers.md) |
| 応募 | サード パーティ アプリまたはサービスの認証フロー | Azure AD サービス間認証/アプリケーション認証 | Commerce 本社で、外部 ID プロバイダーを ID プロバイダーの承認済みリストに追加します。 | |

\* POS にサインインするには、デバイスごとにライセンス認証が必要です。 詳細については、[販売時点管理 (POS) デバイスのライセンス認証](/dev-itpro/retail-device-activation.md) を参照してください。

### <a name="unsupported-authentication-flows"></a>サポートされていない認証フロー

| シナリオ | サポートされていない認証方法 | 詳細情報 |
|----------|-----------|------------|
| Dynamics 365 POS 認証フロー | デバイスのライセンス認証を行わない (つまり、デバイストークンなし) 認証 | POS 関連の Commerce Scale Unit API では、認証のためのデバイス ライセンス認証トークンが必要です。 |

## <a name="dynamics-365-pos-employee-authentication-flows"></a>Dynamics 365 POS 従業員認証フロー

次の図は、Commerce の POS 従業員認証フローを示しています。

<a href="/dynamics365/commerce/media/arch-auth-flow-1.jpg" target="_blank">![Dynamics 365 POS 従業員認証フロー。](./media/arch-auth-flow-1.jpg)</a>

## <a name="dynamics-365-e-commerce-customer-authentication-flows"></a>Dynamics 365 E コマース顧客認証フロー

次の図は、Commerce の E コマース フローを示しています。

<a href="/dynamics365/commerce/media/arch-auth-flow-2.jpg" target="_blank">![Dynamics 365 E コマース顧客認証フロー。](./media/arch-auth-flow-2.jpg)</a>

## <a name="third-party-e-commerce-customer-authentication-flows"></a>サード パーティ E コマースの顧客認証フロー

次の図は、Commerce のサード パーティ E コマースの顧客認証フローを示しています。

<a href="/dynamics365/commerce/media/arch-auth-flow-3.jpg" target="_blank">![サード パーティ E コマースの顧客認証フロー。](./media/arch-auth-flow-3.jpg)</a>

## <a name="third-party-application-authentication-flows"></a>サード パーティ製アプリケーションの認証フロー

次の図は、Commerce のサード パーティ製アプリケーションの認証フローを示しています。

<a href="/dynamics365/commerce/media/arch-auth-flow-4.jpg" target="_blank">![サード パーティ製アプリケーションの認証フロー。](./media/arch-auth-flow-4.jpg)</a>

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce アーキテクチャの概要](commerce-architecture.md)

[Commerce Scale Unit の顧客およびコンシューマー API](/dev-itpro/retail-server-customer-consumer-api.md)

[POS 作業者 ログオン](retail-modern-pos-device-activation.md#create-a-worker)

[POS サインインの Azure Active Directory 認証を有効にする](aad-pos-logon.md)

[MPOS および Cloud POS の拡張ログオン機能の設定](extended-logon.md)

[Commerce での B2C テナントの設定](set-up-b2c-tenant.md)

[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)

[認証プロバイダーのコンフィギュレーション](/dev-itpro/configure-authentication-providers.md)

[販売時点管理 (POS) デバイスのライセンス認証](/dev-itpro/retail-device-activation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]