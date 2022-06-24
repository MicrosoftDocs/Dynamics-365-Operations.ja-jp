---
title: POS サインインの Azure Active Directory 認証のコンフィギュレーション
description: この記事では、Azure Active Directory を Microsoft Dynamics 365 Commerce 販売時点管理の認証方法として構成する方法について説明します。
author: boycezhu
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 47da2c78cef2bbee324fbc2202898fbabd927c4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853931"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a>POS サインインの Azure Active Directory 認証のコンフィギュレーション

[!include [banner](includes/banner.md)]

この記事では、Azure Active Directory (Azure AD) を Microsoft Dynamics 365 Commerce 販売時点管理 (POS) の認証方法として構成する方法について説明します。

Microsoft Azure、Microsoft 365、および Microsoft Teams など、他の Microsoft クラウド サービスと共に Dynamics 365 Commerce を使用している小売業者は、通常、アプリケーション間での安全でシームレスなサインイン エクスペリエンスのため、ユーザー資格情報の集中管理に Azure AD を使用します。 Commerce POS に Azure AD 認証を使用するには、最初に Azure AD を Commerce 本社の認証方法として構成する必要があります。

## <a name="configure-pos-authentication-method"></a>POS 認証方法の構成

Commerce 本社の POS 認証方法を構成するには、次の手順に従います。
    
1. **Retail と Commerce \> チャネル設定 \> POS の設定 \> POS プロファイル \> 機能プロファイル** の順に移動し、機能プロファイルを選択して変更します。
1. **機能** クイックタブの **POS スタッフ ログオン** セクションで、**ログオン認証方法** ドロップダウン リストから目的の認証方法を選択します。

    **ログオン認証方法** には 3 つのオプションがあります。
    
    - **個人 ID とパスワード** - この既定のオプションの場合、POS ユーザーが POS にサインインしてマネージャーの上書き機能にアクセスするために、個人 ID とパスワードを入力する必要があります。
    - **シングル サインオンなしの Azure AD** - このオプションの場合、POS ユーザーが Azure AD 資格情報を使用して POS にサインインし、マネージャー上書き機能にアクセスすることが必要です。 POS クライアントが更新されるか再度開いた場合、POS ユーザーは再度サインインするために Azure AD 資格情報を指定する必要があります。
    - **シングル サインオン 付きの Azure AD** - このオプションを選択した場合、POS ユーザーは、他の Web アプリケーションによって使用されている有効な Azure AD 資格情報を使用してクラウド POS (CPOS) にサインインするか、または Windows にサインインしている Azure AD 資格情報を使用して Modern POS (MPOS) にサインインすることができます。 両方の方法により、POS のサインイン画面で Azure AD 資格情報を入力する必要なくサインインできるようになります。 ただし、POS マネージャー上書き機能にアクセスするには、Azure AD 資格情報を使用してサインインする必要があります。

1. **Retail と Commerce > Retail および Commerce IT > 配送スケジュール** に移動し、**1070 (チャネル コンフィギュレーション)** ジョブを実行して、最新の機能プロファイル設定を POS クライアントに同期させます。

> [!NOTE]
> - **シングル サインオンなしの Azure AD** の認証方法オプションは、Commerce バージョン 10.0.18 以前の **Azure Active Directory** オプションに代わります。
> - Azure AD 認証には有効なインターネット接続が必要で、POS がオフラインの場合は機能しません。

## <a name="associate-azure-ad-accounts-with-pos-users"></a>Azure AD アカウントを POS ユーザーに関連付ける

Azure AD を POS 認証方法として使用するには、Azure AD アカウントを Commerce 本社の POS ユーザーと関連付ける必要があります。 

Azure AD アカウントを Commerce 本社の POS ユーザーに関連付けるには、次の手順を実行します。
    
1. **Retail と Commerce > 従業員 > 作業者** に移動し、作業者レコードを開きます。
1. アクション ウィンドウで **Commerce** タブを選択し、**外部 ID** の下で、**既存の ID の関連付け** を選択します。 
1. **既存の外部 ID を使用する** ダイアログ ボックスで、**電子メールで検索** を選択し、Azure AD 電子メール アドレスを入力して、**検索** を選択します。
1. 返された Azure AD アカウントを選択し、**OK** を選択します。

上記の構成手順の後、**Commerce** タブの **エイリアス**、**UPN**、および **外部サブ ID** フィールドが入力されます。

**Retail と Commerce > Retail と Commerce IT > 配送スケジュール** で **1060 (スタッフ)** ジョブを実行して、最新の POS ユーザーと Azure AD アカント データをチャネルに同期させる必要があります。

> [!NOTE]
> ベスト プラクティスとして、パスワード、POS のアクセス許可、関連付けられている Azure AD アカウント、または従業員のアドレス帳などの作業者情報が Commerce 本社に更新された後、**1060 (スタッフ)** ジョブを実行して、最新の作業者情報とチャネルを同期することを強くお勧めします。 POS クライアントはユーザーの認証および承認のチェックに使用する正しいデータを取得できます。

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a>Azure AD 認証を使用した POS のレジスター ロックとサインアウト

POS が Azure AD 認証方法を使用するように構成されている場合、次のようになります。

- POS アプリケーションで、**レジスターのロック** 機能は使用できません。 
- **自動ロック** 機能は、**自動ログオフ** 機能と同じように動作します。
- POS ユーザーが **ログオフ** を選択すると、シングル サインインが有効になっているかどうかにかかわらず、次回 POS を起動する場合にユーザーは Azure AD 資格情報を使用してサインインするよう求められます。

## <a name="manager-override-functionality-with-azure-ad-authentication"></a>Azure AD 認証を使用したマネージャー上書き機能

POS が Azure AD 認証を使用するように構成されている場合、マネージャーの上書き機能は、マネージャーのユーザーの Azure AD 資格情報を求めるダイアログ ボックスを開きます。 マネージャーのサインインが承認されると、マネージャーの Azure AD 資格情報が削除され、以前のユーザーの Azure AD 資格情報がそれ以降の POS 操作に使用されます。

> [!NOTE]
> - Commerce のバージョン 10.0.18 以前では、マネージャーの上書き機能は Azure AD をサポートしません。 POS が Azure AD 認証方法を使用するよう構成されている場合でも、個人 ID とパスワードを入力する必要があります。
> - Apple iOS デバイス上の Safari Web ブラウザーで CPOS を使用する場合、Azure AD 認証でマネージャー上書き機能を使用するには、Safari の設定の **ポップアップをブロック** をオフにする必要があります。 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a>共有デバイスでの Azure AD ベースの POS 認証のセキュリティ ベスト プラクティス

多くの小売業者は、複数のユーザーが共有の物理デバイスから POS アプリケーションにアクセスすることが必要な方法で小売店舗の環境を設定します。 このコンテキストでは、シングル サインインは便利でシームレスな認証エクスペリエンスを提供しますが、現在の POS ユーザーが、別のユーザーの資格情報が使用されて POS のトランザクションまたは操作が実行されていることを認識しないことがあるというセキュリティ ループホールが作成されることがあります。 Azure AD 認証方法を使用するように POS を構成する前に、セキュリティ ポリシーと共有デバイスのサインイン設定を確認して、最も適合するオプションを決定することを強くお勧めします。

- 小売環境で物理的なデバイスのサインインに共有アカウント (ローカル アカウントなど) を使用する場合は、**シングル サインオンなしの Azure AD** オプションを使用することをお勧めします。 これにより、POS にサインインするのに各 POS ユーザーは明示的に Azure AD 資格情報を提供することになります。
- 小売環境で従業員が POS および物理的なホスティング デバイスにサインインするのに自分の Azure AD アカウントを使用する必要がある場合、**シングル サインオン 付きの Azure AD** オプションを使用することをお勧めします。

## <a name="additional-resources"></a>追加リソース

[作業者のコンフィギュレーション](tasks/worker.md)

[小売機能プロファイルの作成](retail-functionality-profile.md)


[MPOS および Cloud POS の拡張ログオン機能の設定](extended-logon.md)

[共有環境におけるクラウド POS のセキュリティ ベスト プラクティス](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
