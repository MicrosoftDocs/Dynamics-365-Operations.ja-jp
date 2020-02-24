---
title: E コマース サイトの作成
description: このトピックでは、Dynamics 365 Commerce サイト ビルダーで 新しい E コマース サイトを作成するために必要な手順と情報について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002016"
---
# <a name="create-an-e-commerce-site"></a>E コマース サイトの作成


[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce サイト ビルダーで 新しい E コマース サイトを作成するために必要な手順と情報について説明します。

E コマース サイトの開発を開始する前には、最初にサイト ビルダーで新しいサイトを開設する必要があります。 


E コマース サイトの開発を開始するには、最初にサイト作成環境で新しいサイトを開設する必要があります。 新しいサイトを作成する前に、少なくとも 1 つのオンライン ストアをコマースで作成する必要があります。 


## <a name="set-up-your-site"></a>サイトの設定

サイトを設定するには、次の操作を行います。

1. サイト ビルダーの環境を開きます。 コマースの環境機能ページには、Microsoft Lifecycle Services (LCS) のサイト ビルダーへのリンクが表示されます。
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

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい E コマース サイトの配置](deploy-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
