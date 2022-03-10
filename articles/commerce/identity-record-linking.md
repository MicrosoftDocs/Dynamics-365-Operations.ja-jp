---
title: ID レコードの顧客 ID への自動リンクを有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce で ID レコードと顧客 ID への自動リンクを有効にする方法について説明します。
author: BrianShook
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 068f9cd8d59c13c14990e9eb76040df3d30464be4a7b01d59e70a164bf2532b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738037"
---
# <a name="enable-automatic-linking-of-identity-records-to-customer-accounts"></a>ID レコードの顧客 ID への自動リンクを有効にする 

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で ID レコードと顧客 ID への自動リンクを有効にする方法について説明します。

このトピックでは、認証済みユーザーを既存の顧客 ID レコードに自動的にリンクする、ID レコード自動リンク機能について説明します。 この機能は、企業間 (B2B) および企業と顧客間 (B2C) サイト フローで使用され、承認済顧客が Azure Active Directory (Azure AD) B2C テナントにサインアップし、作成された顧客レコードにリンクできるようにします。 B2C サイト フローでは、ID レコード自動リンク機能を使用して、Azure AD テナントに登録したユーザーを、販売時点管理 (POS)、コール センター、または Commerce 本社で以前に作成した顧客 ID レコードに自動的にリンクできます。

> [!WARNING] 
> ID レコード自動リンク機能は、ID プロバイダーとして Azure AD B2C とともに使用する必要があります。 「サインアップとサインイン」 ユーザー フローでは、ローカル アカウントのサインアップ ページのレイアウトで、**電子メール アドレス** ユーザー属性の既定の設定を維持し、**検証を要求する** オプションを「はい」に設定する必要があります。 このコンフィギュレーションにより、自動リンク機能の使用時に、サインアップ フローで電子メールの検証機能を保持できます。

Commerce は、Azure AD B2C などの ID プロバイダー サービスと連携して、ユーザー名やパスワードなどのユーザー認証資格情報を格納します。 ユーザーの ID プロバイダー レコードは、Commerce のリンク テーブルによって参照され、認証済ユーザーを Commerce の顧客 ID に関連付けます。 

## <a name="enable-the-automatic-linking-feature-in-commerce-headquarters"></a>Commerce 本社で自動リンク機能を有効にする 

Commerce 本社の環境で自動リンク機能を有効にするには、次の手順を実行します。 

1. **システム管理\>ワークスペース\>機能管理** に移動し、**すべて** タブを選択します。 
1. **ローカル ID レコードと Commerce 顧客の自動リンク** という機能を検索します。
1. 機能を選択し、プロパティ ウィンドウで **今すぐ有効にする** を選択します。

> [!NOTE]
> 有効にすると、環境内のすべてのチャンネルに対して自動リンク機能が有効になります。 環境内で異なるタイプのサイトをホストしている場合は、この点に留意してください。

## <a name="automatic-linking-on-b2b-sites"></a>B2B サイトでの自動リンク 

B2B サイトは、チャネルの作成時に **顧客タイプ** プロパティが「B2B」に設定された、オンライン ストアに接続されている Commerce サイトです。 B2B サイトでは、顧客の承認やサインイン プロセスにおいて、ID レコードから顧客 ID への自動リンクが重要です。 顧客レコードは、B2B レコードが承認されたとき、または B2B 管理者がユーザー レコードを作成するときに作成されます。 顧客レコードが存在する場合、ユーザーは B2B サイトに移動してサインインします。 Azure AD B2C サインイン エクスペリエンスに転送されると、ユーザーはサインアップを続行できます。 サインアップが完了すると、ユーザーは B2B サイトにリダイレクトされます。 この返却コールで、Commerce は顧客の最初のサインインの自動リンク オプションを確認します。

ユーザーの Azure AD B2C ユーザー ID として使用される電子メール アドレスは、法人内のすべての B2B 顧客レコードで検索されます。 Commerce 自動リンク機能は、**個人** タイプで **isB2B** が「true」に設定されている顧客レコードを確認し、その顧客レコードに対して構成されている基本電子メール アドレスと照合します。

B2B サイトでは、自動リンクは次のチェックを実行します。

- 法人内の 1 つの顧客レコードのみが一致条件を満たす場合、サインアップしたユーザーは自動的にそのレコードにリンクされます。
- 法人内に一致条件を満たす顧客レコードがない場合、Commerce はエラー コード **Microsoft_Dynamics_CommerceIdentityNotFound** で **CommerceIdentityNotFound** エラーを生成します。
- 法人内の複数の顧客レコードで一致する条件が見つかった場合、Commerce はエラー コード **Microsoft_Dynamics_Commerce_Runtime_MultipleCustomerAccountsFoundWithSameEmailAddress** で **CustomerServiceMultipleCustomerAccountsFoundErrorOccurredWhenAutoLinking** エラーを生成します。

## <a name="automatic-linking-on-b2c-sites"></a>B2C サイトでの自動リンク

B2C サイトは、チャネルの作成時に **顧客タイプ** プロパティが「B2B」に設定された、オンライン ストアに接続されている Commerce サイトです。 B2C サイトでは、自動リンク機能は、サインアップに使用された電子メール アドレスを持つ単一の顧客 ID が法人内に存在するかどうかを確認します。

ユーザーの Azure AD B2C ユーザー ID として使用される電子メール アドレスは、法人内のすべての B2C 顧客レコードで検索されます。 Commerce 自動リンク機能は、**個人** タイプの顧客レコードを確認します。

B2C サイトでは、自動リンクは次のチェックを実行します。

- 法人内の 1 つの顧客レコードのみが一致条件を満たす場合、サインアップしたユーザーは自動的にそのレコードにリンクされます。
- 法人内に一致条件を満たす顧客レコードがない場合、Commerce は ID プロバイダー レコードにリンクされた新しい顧客レコードを生成します。 
- 法人内の複数の顧客レコードが一致条件を満たす場合、Commerce はエラー コード **Microsoft_Dynamics_Commerce_Runtime_MultipleCustomerAccountsFoundWithSameEmailAddress** で **CustomerServiceMultipleCustomerAccountsFoundErrorOccurredWhenAutoLinking** エラーを生成します。

> [!NOTE]
> - Commerce 通知モジュールを拡張して、エラー条件が満たされた場合にユーザーにエラー メッセージを表示することができます。
> - 1 つのレコードが見つかった場合、Azure AD B2C に設定されたソーシャル ID プロバイダー レコードも、条件が一致する同じ顧客レコードに自動的にリンクされます。 Commerce 顧客 ID は、ローカル ID レコードとソーシャル ID レコードの両方に同時にリンクできます。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい eコマース テナントの配置](deploy-ecommerce-site.md)

[E コマース サイトの作成](create-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
