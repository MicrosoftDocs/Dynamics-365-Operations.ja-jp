---
title: カスタム Azure AD アプリを使用するための CPOS の構成
description: この記事では、カスタム Azure Active Directory (Azure AD) アプリを使用するために クラウド POS (CPOS) を構成する方法について説明します。
author: boycez
ms.date: 11/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 5e4ff797410e1e94869cc37684e7622ec0d97842
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746263"
---
# <a name="configure-cpos-to-use-a-custom-azure-ad-app"></a>カスタム Azure AD アプリを使用するための CPOS の構成

[!include [banner](includes/banner.md)]

既定では、Microsoft Dynamics 365 Commerce のクラウドPOS (CPOS) は、Azure Active Directory (Azure AD) に登録されているファースト パーティの Microsoft アプリを指します。 そのため、Azure AD に変更を加えることなく CPOS を使用できます。 ただし、CPOS のインスタンスを自分で制御するカスタム Azure AD アプリに指定することもできます。 この記事では、カスタム Azure AD アプリを使用するために CPOS を構成する方法について説明します。

## <a name="set-up-a-custom-retail-server-app-in-azure-ad"></a>Azure AD でカスタム Retail Server アプリを設定する

Azure AD でカスタム Retail Server アプリを作成および構成するには、以下の手順に従います。

1. Azure AD ユーザー アカウントを使用して [Azure Active Directory 管理センター](https://aad.portal.azure.com) にサインインします。 ユーザー アカウントに管理者のアクセス許可は必要ありません。
1. **Azure Active Directory** を選択します。
1. **アプリの登録** を選択し、**新規登録** を選択して、**アプリケーションの登録** ダイアログ ボックスを開きます。
1. 次のフィールドを設定します。

    - **名前** - アプリのカスタム名を入力します。 たとえば、**カスタム Retail Server** を入力します。
    - **サポート アカウントの種類** – 既定のオプション **この組織ディレクトリのアカウントのみ (Microsoft のみ、単一テナント)** を選択します。
    - **リダイレクト URL** - このフィールドはオプションです。 空欄のままにしてください。
    - **サービス ツリー ID** - このフィールドはオプションです。 空欄のままにしてください。
    
1. **登録** を選択します。 新しく登録されたアプリの構成ページが表示されます。
1. **概要 \> Essentials** セクションで **アプリケーション ID URI の追加** を選択し、**アプリケーション ID URI** の横にある **設定** を選択します。 提案された値をメモし、**保存** を選択してその値を受け入れます。 
1. **スコープの追加** を選択して、次のフィールドを設定します:

    - **スコープ名** - スコープのカスタム名を入力します。 たとえば、**Legacy.Access.Full** などと入力します。
    - **同意できるユーザー** – 組織のセキュリティ ポリシーに基づいて、管理者とユーザーの両方、または管理者のみが同意できるかどうかを指定します。
    - **管理者の同意の表示名** – 表示名を入力します。 たとえば、**Retail Server へのアクセス** を入力します。
    - **管理者の同意の説明** – 説明を入力します。 たとえば、**Retail Server API へのアクセス許可を与えます** を入力します。

1. **スコープの追加** を選択し、スコープ作成プロセスを完了します。

## <a name="set-up-a-custom-cpos-app-in-azure-ad"></a>Azure AD でカスタム CPOS アプリを設定する

> [!IMPORTANT]
> Commerce バージョン 10.0.21 より前に作成した既存のカスタムCPOS Azure AD アプリをアップグレードする場合は、[Commerce バージョン 10.0.21 より前に作成した既存のカスタム CPOS Azure AD アプリをアップグレードする](#upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021) の手順に従ってください。

Azure AD でカスタム CPOS アプリを作成および構成するには、以下の手順に従います。

1. Azure AD ユーザー アカウントを使用して [Azure Active Directory 管理センター](https://aad.portal.azure.com) にサインインします。 ユーザー アカウントに管理者のアクセス許可は必要ありません。
1. **Azure Active Directory** を選択します。
1. **アプリの登録** を選択し、**新規登録** を選択して、**アプリケーションの登録** ダイアログ ボックスを開きます。
1. 次のフィールドを設定します。

    - **名前** – アプリの名前を入力します。 たとえば、**カスタム クラウド POS** と入力します。
    - **サポート アカウントの種類** – 既定のオプション **この組織ディレクトリのアカウントのみ (Microsoft のみ、単一テナント)** を選択します。
    - **リダイレクト URI** – ドロップダウン リストで **シングル ページ アプリケーション (SPA)** を選択し、CPOS URI を入力します。
    - **サービス ツリー ID** - このフィールドはオプションです。 空欄のままにしてください。

1. **登録** を選択します。 新しく登録されたアプリの構成ページが表示されます。
1. **マニフェスト** セクションで **oauth2AllowIdTokenImplicitFlow** と **oauth2AllowImplicitFlow** のパラメーターを **true** に設定し、**保存** を選択します。
1. **トークンの構成** セクションで、以下の手順に従って 2 つの要求を追加します:

    1. **オプション要求の追加** を選択します。 **トークン タイプ** フィールドを **ID** に設定し、**sid** 要求を選択します。 **追加** を選択します。
    1. **オプション要求の追加** を選択します。 **トークン タイプ** フィールドを **アクセス** に設定し、**sid** 要求を選択します。 **追加** を選択します。

1. **API アクセス許可** セクションで **アクセス許可の追加** を選択します。
1. **組織が使用する API** タブで、[Azure AD でカスタム Retail Server アプリを設定する](#set-up-a-custom-retail-server-app-in-azure-ad) セクションで作成した Retail Server アプリを検索します。 次に、**アクセス許可の追加** を選択します。
1. **概要** セクションで **アプリケーション (クライアント) ID** フィールドの値をメモします。

### <a name="upgrade-an-existing-custom-cpos-azure-ad-app-created-before-commerce-version-10021"></a>Commerce バージョン 10.0.21 より前に作成した既存のカスタム CPOS Azure AD アプリをアップグレードする

Commerce バージョン 10.0.21 より前に作成した既存のカスタム CPOS Azure AD アプリをアップグレードするには、以下の手順を実行します。 

1. Azure portal でカスタム CPOS Azure AD アプリを開きます。
1. **認証** タブを選択します。
1. 後で使用するために **Web** タイプから元のリダイレクト URI をコピーして保存してから、削除します。
1. **プラットフォームの追加** を選択し、**シングル ページ アプリケーション (SPA)** を選択します。
1. 上記でコピーした元の Web リダイレクト URI を SPA プラットフォームに追加します。
1. **トークンの構成** セクションで、以下の手順に従って 2 つの要求を追加します:
    1. **オプション要求の追加** を選択します。 **トークン タイプ** フィールドを **ID** に設定し、**sid** 要求を選択します。 **追加** を選択します。
    1. **オプション要求の追加** を選択します。 **トークン タイプ** フィールドを **アクセス** に設定し、**sid** 要求を選択します。 **追加** を選択します。

## <a name="update-the-cpos-configuration-file"></a>CPOS 構成ファイルを更新する

CPOS config.json ファイルを開いて、次の更新を行います。

1. **AADClientId** キー値を、[Azure AD でカスタム CPOS アプリを設定する](#set-up-a-custom-cpos-app-in-azure-ad) セクションで作成したカスタム CPOS アプリの **アプリケーション (クライアント) ID** の値に置き換えます。
1. **AADRetailServerResourceId** キー値を、[Azure AD でカスタム Retail Server アプリを設定する](#set-up-a-custom-retail-server-app-in-azure-ad) セクションで作成したカスタム Retail Serve アプリの **アプリケーション ID URI** の値に置き換えます。

CPOS は、Azure AD に要求を送信してセキュリティ トークンを取得するときに両方のパラメーターを使用します。

## <a name="update-identity-providers-settings-in-commerce-headquarters"></a>Commerce headquarters で ID プロバイダーの設定を更新する

次に、Commerce headquarters で ID プロバイダーの設定を更新する必要があります。

1. Commerce headquarters で **Commerce 共有パラメーター** ページを開きます。
1. **ID プロバイダー** タブの **ID プロバイダー** セクションで、**タイプ** フィールドが **Azure Active Directory** に設定され、**発行者** フィールドが Azure AD テナントを指定している行を選択します。 この設定では、Azure AD テナントに対応する ID プロバイダーに関連するデータを含む子グリッドを使用することを宣言します。
1. **依存する関係者** セクションで **追加** を選択して、行を追加します。
1. 次のフィールドを設定します。

    - **ClientId** – [Azure AD でカスタム CPOS アプリを設定する](#set-up-a-custom-cpos-app-in-azure-ad) セクションで作成したカスタム CPOS アプリの **アプリケーション (クライアント) ID** の値を入力します。
    - **タイプ** – **パブリック** を選択します。
    - **UserType** – **作業者** を選択します。

1. 追加した行を選択します。 **依存する関係者** セクションの下の **サーバー リソース ID** セクションには、**依存する関係者** グリッドで選択したアプリからアクセスできる Retail Server アプリ ID が表示されます。
1. **サーバー リソース ID** セクションで **追加** を選択して、行を追加します。
1. **サーバー リソース ID** フィールドで、[Azure AD でカスタム Retail Server アプリを設定する](#set-up-a-custom-retail-server-app-in-azure-ad) セクションで作成したカスタム Retail Serve アプリの **アプリケーション ID URI** の値を入力します。

    > [!IMPORTANT]
    > これまでの手順で説明したすべてのフィールドでは、大文字と小文字が区別されます。 入力する値は、Azure AD 管理センターで構成された値と完全に一致する必要があります。

1. **小売とコマース IT \> 配送スケジュール** に移動し、**1110** (**グローバル構成**) ジョブを実行します。

これで、独自の Azure AD アプリを使用して CPOS デバイスを有効化できるようになりました。

## <a name="additional-resources"></a>追加リソース

[販売時点管理 (POS) デバイスのライセンス認証](dev-itpro/retail-device-activation.md)

[アクティベーション アカウントの管理とデバイスの検証](set-up-activation-accounts-validate-devices-hq.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
