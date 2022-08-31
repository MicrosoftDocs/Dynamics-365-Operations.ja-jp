---
title: ID 管理ページとモジュール
description: この記事では、Microsoft Dynamics 365 Commerce の ID 管理ページおよびモジュールについて説明します。
author: BrianShook
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 75d50d5c07c685b374537887bd5c67d84e7efad7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273488"
---
# <a name="identity-management-pages-and-modules"></a>ID 管理ページとモジュール

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の ID 管理ページおよびモジュールについて説明します。

ID 管理モジュールは、eコマース サイトのユーザーが Dynamics 365 Commerce 環境に関連付けられている ID 管理システムと対話するために使用する ID 管理ページの要素を表示します。 特に、ID 管理モジュールは、サインイン、サインアップ、パスワードのリセット、およびアカウント プロフィール編集ページで使用されます。 既定では、Commerce モジュールは、ID プロバイダーとして Azure Active Directory B2C (Azure AD B2C) を使用するように構成されています。

> [!WARNING]
> Azure AD B2C は、2021 年 8 月 1 日までに古い (レガシ) ユーザー フローを破棄します。 したがって、ユーザー フローを新しい推奨バージョンに移行する必要があります。 新しいバージョンでは、機能パリティと新しい機能が提供されます。 詳細については、[Azure Active Directory B2C のユーザー フロー](/azure/active-directory-b2c/user-flow-overview) を参照してください。

## <a name="identity-management-pages"></a>ID 管理ページ

ID 管理ページは、Commerce サイト ビルダーを使用して作成されます。 ただし、セキュリティ上の理由から、Commerce サイトからではなく Azure AD B2C サーバーでホストされ、提供されます。 ベスト プラクティスとして、ID 管理ページ用に個別の Azure AD ヘッダー フラグメントとフッター フラグメントを作成し、それらに最小限のページ要素を含める必要があります。 相対リンクを持つフラグメントや、Commerce 固有の呼び出し (お気に入りボタンやショッピング カート モジュールからの呼び出しなど) を行うフラグメントは、Azure AD B2C サーバーからは機能しません。 Commerce のインスタンスと共にリリースされるスターター サイトには、参照のために Azure AD のヘッダーとフッターのサンプルが含まれています。

Azure AD B2C で ID 管理ページを設定する方法については、「[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)」を参照してください。

### <a name="associate-published-identity-management-pages-with-the-azure-ad-b2c-user-flow"></a>発行された ID 管理ページと Azure AD B2C ユーザー フローの関連付け

ID 管理ページでは、Azure AD B2C サーバーから初期化された JavaScriptが使用されます。 多くの場合、サイト ビルダーや eコマース サイトからページをプレビューすると、ページの中央に白い読み込みバーが表示されますが、初期化されることはありません。 ページが発行されたら、[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md) の説明に従って、そのページを Azure AD B2C ユーザー フローに関連付ける必要があります。その後、Azure AD B2C から提供されるページを表示すると、ページ要素がレンダリングされるときに JavaScript が初期化されます。

## <a name="identity-management-modules"></a>ID 管理モジュール

Commerce の ID 管理ページで使用されるモジュールは次のとおりです。

### <a name="sign-up-module"></a>サインアップ モジュール

サインアップ モジュールは、サインアップ ページで使用されます。 これには、サイト ユーザーがサインアップ フローを完了するために使用するフォーム要素が含まれます。 ユーザーは、ユーザー名として使用するメール アドレスを提供します。 その後、このモジュールによって Azure AD B2C メール検証フローが実行されます。 このフローでは「コードを送信」がトリガされ、ユーザーが入力したセキュリティ個人識別番号 (PIN) が検証されます。 サインアップ ページで収集された情報は、Azure AD B2C でレコードを作成し、Commerce で顧客レコードを作成するために使用されます。

### <a name="sign-in-module"></a>サインイン モジュール

サインイン モジュールは、サインイン ページで使用されます。 これには、ユーザーが自分のアカウントにサインインするために使用するフォーム要素が含まれます。 サインイン ページには、ユーザーがサインアップ ページを開く時に使用できるボタンも表示されます。 この方法で、このページは Azure AD B2Cの「サインアップしてサインインする」ユーザーフローと直接ペアリングされます。

### <a name="password-reset-modules"></a>パスワードのリセット モジュール

パスワードのリセット フローに関連付けられているモジュールは次の 2 種類です。

- **パスワードのリセット検証** – このモジュールは、パスワードのリセット検証ページで使用されます。 これにより、ユーザーはユーザー アカウントに関連付けられているメール アドレスにセキュリティ PIN のメールを送信します。 パスワードのリセットの検証ページでは、ユーザーが受け取ったセキュリティ PIN を入力してアカウントの所有権を確認することもできます。
- **パスワードのリセット** – このモジュールは、パスワードのリセット ページで使用されます。 パスワード リセットの確認ページでアカウントのメール アドレスが確認された後、ユーザーは新しいパスワードを設定して確認できます。

### <a name="account-profile-edit-module"></a>アカウント プロフィール編集モジュール

アカウント プロフィールの編集モジュールは、プロフィール編集ページで使用されます。 これにより、ユーザーが名および姓を更新できます。 これら 2 つの値は Azure AD B2C と Commerce 間で共有されます。 ユーザーがアカウント プロフィール編集ページを通じて更新を行う場合、値は Azure AD B2C システムと Commerce システムの両方で更新されます。

Commerce eコマース サイトでは、ユーザーは **マイ アカウント \> マイ プロフィール \> 詳細の表示 \> 名前** に移動することで自分のアカウント プロフィール編集ページにアクセスできます。 ユーザーは、**編集** を選択して情報を更新できます。

### <a name="azure-ad-generic-module"></a>Azure AD 汎用モジュール

Azure AD 汎用モジュールは Azure AD B2C の推奨パターンに従い、専用の **\<div\>** 要素が設定され、Azure AD B2C がサイトページ上で要素をレンダリングするために使用できます。 汎用モジュールは柔軟であり、そのモジュールを含むページをすべての Azure AD B2C ユーザー フローのページ レイアウトに使用できます。

Azure AD B2C は、ページ上のモジュールに異なるユーザー フロー要素をレンダリングします。 したがって、ページのレンダリング時に視覚的要素に対する制御がわずかに少なくなります。 カスケード スタイル シート (CSS) スタイルが適用されますが、他の ID 管理モジュールのようにページ要素の複雑な配置を行うことはできません。

汎用モジュールを含むページは、Azure AD B2C 設定 (たとえば、サインインおよびサインアップ用の ソーシャル ID プロバイダを追加する場合) を変更したり、将来の Azure AD B2C 機能を使用する場合にモジュールの拡張性調整が必要ないため、より効率的に使用できます。

## <a name="additional-resources"></a>追加リソース

[ユーザーのサインインに対するカスタム ページの設定](custom-pages-user-logins.md)
