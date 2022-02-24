---
title: e コマース サイトの作成
description: このトピックでは、Dynamics 365 Commerce サイト ビルダーで新しい e コマース サイトを作成するために必要な手順と情報について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf084f90d203d84c91ddf7c0d963780b895ef23d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963038"
---
# <a name="create-an-e-commerce-site"></a>e コマース サイトの作成

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce サイト ビルダーで新しい e コマース サイトを作成するために必要な手順と情報について説明します。

Dynamics 365 Commerce 機能のライセンスを取得すると、サイト ビルダーには、独自のサイトの基礎として使用できるスターター サイトがプロビジョニングされます。 ただし、最初から開始する場合、または 2 つめのサイトを作成する場合は、サイト作成環境で新しいサイトを作成する必要があります。 

## <a name="set-up-your-site"></a>サイトの設定

サイトを設定するには、次の操作を行います。

1. サイト ビルダーの環境を開きます。 コマースの環境機能ページには、Microsoft Lifecycle Services (LCS) のサイト ビルダーへのリンクが表示されます。
1. サイト作成環境のホームページで、**新しいサイト** を選択します。
1. **新しいサイト** ダイアログ ボックスで、次の情報を入力してください。

| フィールド                               | 説明 |
|-------------------------------------|-------------|
| サイト名                           | サイト作成環境で、サイトに使用する表示名を入力します。 この名前は、作成環境でのみ表示され、顧客には表示されません。 |
| サイト管理者のセキュリティ グループ | このサイトで管理者ロールを持つユーザーを管理する Microsoft Azure Active Directory (Azure AD) セキュリティ グループを指定します。 |
| 既定のチャネル (作業単位番号) | このサイトが Web ストア フロントとして使用されるオンライン ストアを選択します。 e コマース サイトで複数のオンライン ストアをサポートする場合は、サイトを設定した後で、**サイトの設定** でストアをサイトに関連付ける必要があります。 |
| 既定の言語                            | このオンライン ストアおよびマーケットの既定の言語を指定します。 オンライン ストアは複数の言語をサポートできます。 このオンライン ストアまたは別のオンライン ストアに対して、複数の言語をサポートする場合は、サイトを設定した後に、**サイトの設定** で構成することができます。  |
| ドメイン                              | このオンライン ストアでドメインとして使用されるドメイン名を選択します。 LCS でドメインをコンフィグレーションしていない場合は、このフィールドを空白のままにしておくことができます。 ドメインを LCS でコンフィグレーションしたら、**サイトの設定** でそのドメインをオンライン ストアに追加する必要があります。  |
| パス                              | サイトが、特定のドメイン名に対して複数の言語をサポートしている場合は、パス フィールドを使用して、そのドメインと言語の組み合わせに固有のサイト URL を作成します。 **既定の言語** フィールドに指定した言語のみ、このドメインに対してサポートされる場合、またはサイトを他の言語にローカライズした後も、その言語を既定の言語として使用する場合は、このフィールドを空白のままにすることをお勧めします。 |


サイトが作成されると、**製品** タブを選択することにより、そのサイトがオンライン ストアに関連付けられていることを確認できます。そこでは、オンライン ストアに割り当てられた製品の品揃えが表示されます。 ページの左上にあるドロップダウン メニューを使用して、割り当てられた製品にカテゴリ別にアクセスすることもできます。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい eコマース テナントのデプロイ](deploy-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
