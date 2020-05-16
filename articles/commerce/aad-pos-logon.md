---
title: POS サインインの Azure Active Directory 認証を有効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce 販売時点管理 (POS) のサインイン エクスペリエンスを構成して、Azure Active Directory 認証を使用できるようにする方法について説明します。
author: boycezhu
manager: annbe
ms.date: 03/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: dfc49585434383385b6b993893d93b95ef888384
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248943"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a>POS サインインの Azure Active Directory 認証を有効にする
[!include [banner](includes/banner.md)]


Microsoft Dynamics 365 Commerce を使用する多くの顧客は、他の Microsoft クラウド サービスも使用しており、Azure Active Directory (Azure AD) を使用して、これらのサービスのユーザー資格情報を管理することができます。 そのような場合、顧客はアプリケーション間で同じ Azure AD アカウントを使用することができます。 このトピックでは、Commerce 販売時点管理 (POS) のサインイン エクスペリエンスを構成して、 Azure AD 認証を使用できるようにする方法について説明します。

## <a name="configure-azure-ad-authentication"></a>Azure AD 認証の構成

店舗の POS サインインの認証方法として Azure AD を使用できるようにするには、店舗の機能プロファイルの設定を構成してから、それらの設定を POS クライアントに適用する必要があります。

機能プロファイルを構成するには、次の手順に従います。

1. **Retail および Commerce** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **機能プロファイル**の順に移動します。
1. 変更する機能プロファイルを選択します。
1. **関数**クイック タブの、**POS スタッフ ログオン** セクションで、**ログオン認証方法**フィールドの値を**従業員 ID とパスワード**から **Azure Active Directory** に変更します。

既定では、すべての機能プロファイルは、POS 認証方法として**従業員 ID とパスワード**を使用します。 したがって、Azure AD を使用する場合は、**ログオン認証方法**フィールドの値を変更する必要があります。 選択した機能プロファイルにリンクされているすべての小売用店舗は、この変更によって影響を受けます。

POS クライアントにこの設定を適用するには、次の手順に従います。

1. **Retail と Commerce** \> **Retail と Commerce IT** \> **配送スケジュール**の順に移動します。
1. **1070** (**チャネル構成**) 配布スケジュールを実行します。

> [!NOTE]
> Azure AD 認証にはインターネット接続が必要です。 POS がオフライン モードの場合は機能しません。

## <a name="associate-an-azure-ad-account-with-a-worker"></a>Azure AD アカウントと作業者の関連付け

店舗の作業者が POS アプリケーションへのサインインに Azure AD アカウントを使用する前に、Azure AD アカウントがその作業者に関連付けられている必要があります。

Azure AD アカウントを作業者に関連付けるには、次の手順に従います。

1. **Retail と Commerce** \> **従業員** \> **作業者**の順に移動します。
1. 作業者の詳細ページを開きます。
1. アクション ウィンドウ、**Commerce** タブの、**外部 ID** グループで、**既存の ID の関連付け**を選択します。
1. **既存の外部 ID を使用する**ダイアログ ボックスで、**電子メールで検索**を選択し、Azure AD 電子メール アドレスを入力して、**検索**を選択します。
1. 返された Azure AD アカウントを選択し、**OK** を選択します。

**Commerce** タブの**エイリアス**、**UPN**、および**外部サブ ID** フィールドが入力されます。

## <a name="additional-resources"></a>追加リソース

[MPOS および Cloud POS の拡張ログオン機能の設定](extended-logon.md)

[小売機能プロファイルの作成](retail-functionality-profile.md)

[作業者のコンフィギュレーション](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
