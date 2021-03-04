---
title: Commerce 環境での複数の B2C テナントのコンフィギュレーション
description: このトピックでは、専用の Dynamics 365 Commerce 環境で、複数のチャネルごとの Microsoft Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントの設定時期と方法について説明します。
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: da27e3ed0a0e50126590609d09575befe17a7aa2
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517129"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Commerce 環境での複数の B2C テナントのコンフィギュレーション

[!include [banner](includes/banner.md)]

このトピックでは、専用の Dynamics 365 Commerce 環境で、複数の Microsoft Azure Active Directory (Azure AD) 企業と顧客間 (B2C) テナントをチャネルごとに設定する時期と方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce では Azure AD B2C クラウド ID サービスを使用して、ユーザーの資格情報と認証フローをサポートします。 ユーザーは認証フローを使用して、パスワードの登録、ログイン、およびリセットを行うことができます。 Azure AD B2C では、ユーザー名やパスワードなどの機密性の高い認証情報を保存します。 ユーザー レコードは、各 B2C テナントに固有であり、ユーザー名 (電子メールアドレス) またはソーシャル ID プロバイダーの資格情報を使用します。

多くの場合、単一の Azure AD B2C テナントは Commerce 環境で使用されます。 その後、Commerce の顧客は同じ Commerce 環境で複数のサイトを作成および公開することができ、それらのサイトで同じ顧客の資格情報が使用されます。 ただし環境内のサイトを別のブランドとして扱う必要があり、ユーザーには別のビジネスとして表示される場合、B2C テナントはサイトまたはブランドの分離に使用されるチャネルに対してコンフィギュレーションされます。

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>チャネルごとに複数の B2C テナントを設定する場合の考慮事項

各チャネルまたはサイトが個別のビジネスとして扱われる場合、Commerce のユーザー認証フローに関する最適なオプションは異なる法人エンティティを使用することです。 ただし、同じ環境と法人各チャネルまたはサイトを保持しながら各サイトの個別ユーザー認証を使用する場合は、先に進む前に次の点を考慮する必要があります。

- ユーザーは、チャネルまたはサイトごとに個別の資格情報を持つことになります。

    各アカウントはそれぞれ別の B2C テナントに一意のエントリになるので、同じ人がチャネルまたはサイトごとに 2 つのアカウントを持つことができます。

- Microsoft Dynamics 環境では、グローバル レコードの検索に対して個別の顧客レコードが返されます。

    ユーザーがチャネルまたはサイト間で同じ電子メールアドレスを使用している場合、グローバル顧客検索ではチャネルまたはサイトごとに結果が返されます。 (チャネル インジケータが表示されます。)

- アドレス帳を使用して、ユーザーをグループ化し、チャネルごとに追跡できるようにすることができます。
- チャンネルごとの顧客レコード数が増加し、この増加がグローバル顧客検索のパフォーマンスに影響を与える可能性があります。
- B2C テナントは顧客が誤ったテナントにサイン アップする状況を防止するために、チャネルに注意深くマップする必要があります。 そうしないと、混乱や追跡の問題が発生する可能性があります。

次の図は、Commerce 環境における複数の B2C テナントを示しています。

![Commerce 環境での B2C テナントを複数化](media/MultiB2C_In_Environment.png)

同じ Commerce 環境にあるチャネルごとに個別の B2C テナントが必要であると判断した場合は、次のセクションの手順を実行し、この機能を要求します。

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>お客様の環境でチャネルごとの B2C を有効にすることを要求

現在、チャネルごとに個別の B2C テナントを同じ Commerce 環境で使用できるようにするには、Dynamics 365 Commerce に要求を提出する必要があります。 詳細については、[Lifecycle Services (LCS) のサポートを受ける](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md) を参照するか、または Commerce ソリューションへ連絡し相談してください。

## <a name="configure-b2c-tenants-in-your-environment"></a>お客様の環境での B2C テナントのコンフィギュレーション

使用している環境で B2C テナントをコンフィギュレーションするには、このセクションの該当する手順を実行します。

### <a name="add-an-azure-ad-b2c-tenant"></a>Azure AD B2C テナントの追加

Azure AD B2C テナントをお客様の環境に追加するには、次の手順を実行します。

1. システム管理者として使用環境の Commerce サイト ビルダーにログインします。Azure AD B2C テナントをコンフィギュレーションするには、Commerce 環境のシステム管理者である必要があります。
1. 左のナビゲーション ウィンドウで、**テナント設定** を選択して展開します。
1. **B2C 設定** を選択し、**管理** を選択します。
1. **B2C アプリケーションを追加** を選択し、以下の情報を入力します。

    - **アプリケーション名**: Commerce で管理するコンテキストのアプリケーションで使用する名前を入力します。 Azure ポータルの Azure AD B2C アプリケーションを設定する際に、選択したアプリケーション名の使用をお勧めします。 このようにして、Commerce の B2C テナントを管理する際に混乱を避けることができます。
    - **テナント名**: Azure ポータルに表示される B2C テナント名を入力します。
    - **Password Policy ID 忘れた**: ポリシー ID (Azure ポータルのポリシーの名前) を入力します。
    - **Signin Policy ID をサインアップ**: ポリシー ID (Azure ポータルのポリシーの名前) を入力します。
    - **クライアント GUID**: Azure ポータルに表示されるとおりに Azure AD B2C テナント ID (B2C テナントのアプリケーション ID ではない) を入力します。
    - **Profile Policy ID を編集**: ポリシー ID (Azure ポータルのポリシーの名前) を入力します。

1. 情報の入力が完了したら、**承認** を選択して変更を保存します。

> [!NOTE]
> Dynamics 365 Commerce チームがそれらを設定するよう指示しない限り、**スコープ**、**Non Interactive Policy ID**、**Non Interactive Client ID**、**Custom Domain をログイン** および **Policy ID をサインアップ** ブランクなどのフィールドを残す必要があります。
新しい Azure AD B2C テナントが、**B2C Applications の管理** 下の一覧に表示されるようになります。

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Azure AD B2C テナントの管理または削除

1. システム管理者として使用環境の Commerce サイト ビルダーにログインします。Azure AD B2C テナントをコンフィギュレーションするには、Commerce 環境のシステム管理者である必要があります。
1. 左のナビゲーション ウィンドウで、**テナント設定** を選択して展開します。
1. **B2C 設定** を選択し、**管理** を選択します。
1. B2C テナントを編集するには、その横にある鉛筆の記号を選択します。 B2C テナントを削除するには、その横のごみ箱アイコンを選択します。
1. **保存** を選び、**発行** を選択して変更をアクティブにします。

> [!WARNING]
> ライブまたは公開サイトに対して B2C テナントをコンフィギュレーションすると、ユーザーはテナントに存在するアカウントを使用してサインアップした可能性があります。 **テナントの設定 \> B2C テナント** メニュー上でコンフィギュレーションされたテナントを削除する場合、テナントのチャネルに関連付けられているサイトから B2C テナントのアソシエーションを削除することになります。 この場合、ユーザーは自分のアカウントにログインできなくなる場合があります。 したがって、コンフィギュレーション済のテナントを削除する場合は細心の注意を払ってください。
>
> コンフィギュレーションされたテナントを削除すると、B2C テナントとレコードが引き続き維持されますが、そのテナントの Commerce システム コンフィギュレーションは変更または削除されます。 サイトへサイン アップまたはサイト インを試みるユーザーは、サイトのチャネルに対してコンフィギュレーションされた既定または新しく関連付けられた B2C テナントに新しいアカウント レコードが作成されます。
## <a name="configure-your-channel-with-a-b2c-tenant"></a>B2C テナントでのチャネルのコンフィギュレーション

1. システム管理者として使用環境の Commerce サイト ビルダーにログインします。Azure AD B2C テナントをコンフィギュレーションするには、Commerce 環境のシステム管理者である必要があります。
1. 左のナビゲーション ウィンドウで、**サイト設定** を選択して展開します。
1. **チャネル** を選択し、コンフィギュレーションするチャネルを選択します。
1. 右側のプロパティ ウィンドウの **B2C アプリケーションの選択** フィールドで、このチャネルに使用されるコンフィギュレーション済み Azure AD B2C テナントを選択します。
1. コマンド バーで **保存と発行** を選択し、新規または更新されたコンフィギュレーションをコミットします。

> [!WARNING]
> チャネルに割り当てられている B2C アプリケーションを変更すると、その環境に既にサイン アップしているすべてのユーザーに対して確立されている現在の参照を削除することになります。 この場合、現在割り当てられている B2C アプリケーションに関連付けられている資格情報は、ユーザーに使用できません。 したがって、チャネルを初めて設定するときにユーザーが登録できなかった場合にのみ、チャネル Azure AD B2C コンフィギュレーションを変更してください。 そうしないと、新しい Azure AD B2C テナントのレコードを確立するために、ユーザーが再度サイン アップする必要があります。
## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい eコマース テナントのデプロイ](deploy-ecommerce-site.md)

[eコマース サイトの作成](create-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]