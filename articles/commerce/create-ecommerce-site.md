---
title: E コマース サイトの作成
description: このトピックでは、Dynamics 365 Commerce における新しい E コマース サイトの作成に関連する作業について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697132"
---
# <a name="create-an-e-commerce-site"></a>E コマース サイトの作成

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce における新しい E コマース サイトの作成に関連する作業について説明します。

## <a name="overview"></a>概要

E コマース サイトの開発を開始するには、最初にサイト作成環境で新しいサイトを開設する必要があります。 新しいサイトを作成する前に、少なくとも 1 つのオンライン ストアを Dynamics 365 Retail で作成する必要があります。 

## <a name="set-up-your-site"></a>サイトの設定

サイトを設定するには、次の操作を行います。

1. Microsoft Lifecycle Services (LCS) で、サイト作成環境のリンクを選択します。 
1. サイト作成環境のホームページで、**新しいサイト**を選択します。
1. **新しいサイト** ダイアログ ボックスで、次の情報を入力してください。

| フィールド                               | 説明 |
|-------------------------------------|-------------|
| サイト名                           | サイト作成環境で、サイトに使用する表示名を入力します。 この名前は、作成環境でのみ表示され、顧客には表示されません。 |
| サイト管理者のセキュリティ グループ | このサイトで管理者ロールを持つユーザーを管理する Microsoft Azure Active Directory (Azure AD) セキュリティ グループを指定します。 |
| 既定のチャネル (作業単位番号) | このサイトが Web ストア フロントとして使用されるオンライン ストアを選択します。 E コマース サイトで複数のオンライン ストアをサポートする場合は、サイトを設定した後で、**サイトの設定**でストアをサイトに関連付ける必要があります。 |
| 既定の言語                            | このオンライン ストアおよびマーケットの既定の言語を指定します。 オンライン ストアは複数の言語をサポートできます。 このオンライン ストアまたは別のオンライン ストアに対して、複数の言語をサポートする場合は、サイトを設定した後に、**サイトの設定**で構成することができます。  |
| ドメイン                              | このオンライン ストアでドメインとして使用されるドメイン名を選択します。 LCS でドメインをコンフィグレーションしていない場合は、このフィールドを空白のままにしておくことができます。 ドメインを LCS でコンフィグレーションしたら、**サイトの設定**でそのドメインをオンライン ストアに追加する必要があります。  |
| パス                              | サイトが、特定のドメイン名に対して複数の言語をサポートしている場合は、パス フィールドを使用して、そのドメインと言語の組み合わせに固有のサイト URL を作成します。 **既定の言語**フィールドに指定した言語のみ、このドメインに対してサポートされる場合、またはサイトを他の言語にローカライズした後も、その言語を既定の言語として使用する場合は、このフィールドを空白のままにすることをお勧めします。 |


サイトが作成されると、**製品**タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。 ページの左上にあるドロップダウン メニューを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。

## <a name="additional-resources"></a>追加リソース

[オンライン ストアの概要](online-store-overview.md)

[新しい E コマース サイトの配置](deploy-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[ホーム ページの概要の作成](authoring-home-overview.md)

[新しいサイト ページの追加](add-new-page.md)
