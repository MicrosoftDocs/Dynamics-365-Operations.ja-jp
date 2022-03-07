---
title: 新しい eコマース テナントのデプロイ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい Dynamics 365 Commerce e コマース サイトをデプロイする方法について説明します。
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b4b54e10cb4bd897b4c0706a13eeaf32f8892a05f7a09f3b27dbdd3dcdad1606
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750717"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>新しい eコマース テナントのデプロイ

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい Dynamics 365 Commerce e コマース サイトをデプロイする方法について説明します。

Microsoft Dynamics Lifecycle Services (LCS) は、パートナーや顧客がプロジェクト環境を管理したり、Microsoft Dynamics 製品や機能に関する最新情報を表示したり、サポート インシデントを作成、追跡、参照したりするために使用できる、クラウドベースのコラボレーション ワークスペースです。 e コマースの管理機能は LCS に統合されています。

LCS の詳細については、[Lifecycle Services ユーザー ガイド](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)を参照してください。
    
## <a name="get-started"></a>開始する

e コマースを初期化する前に、プロジェクト、環境、Retail Cloud Scale Unit (RCSU) を初期化する必要があります。 LCS で初期化を行うには、プロジェクト所有者ロールまたは環境マネージャ ロールのいずれかのアクセス許可が必要です。 実稼働環境とサンドボックス環境のトポロジがサポートされています。

環境に関する詳細については、[環境計画](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)を参照してください。 RCSU の詳細については、[Retail Cloud Scale Unit の初期化](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)を参照してください。

## <a name="initialize-e-commerce"></a>e コマースの初期化

この手順を使用して、既存環境で e コマース機能を初期化します。

開始する前に、次の必要な情報があることを確認してください。

- 使用される RCSU。
- e コマース システムで使用される Microsoft Azure Active Directory セキュリティ グループ。
- 評価およびレビュー モデレーターで使用される Microsoft Azure Active Directory セキュリティ グループ。
- 環境に関連付けられるドメイン。

さらに、次のオプション情報を収集できます。

- Azure AD 企業と顧客間 (B2C) 情報:

    - テナント名。
    - クライアント ID。
    - ログイン カスタム ドメイン。
    - 返信 URL。
    - ポリシー ID のサインアップ サインイン。
    - リセット パスワード ポリシー ID。
    - プロファイル ポリシー 編集 ID。

> [!NOTE]
> この情報は、サービス要求を介して後から追加できます。

必要な情報を収集したら、次の手順に従って e コマースを初期化します。

1. [LCS](https://lcs.dynamics.com) にサインインします。
1. e コマースを初期化する環境を含むプロジェクトを開きます。
1. **環境** セクションで、環境を選択します。
1. **環境機能** で、**小売管理** のリンクを選択します。
1. **E コマース** タブで、**設定** を選択します。 ダイアログ ボックスが表示されるので、プロビジョニングに必要な情報を入力します。
1. 必要な情報を入力し、次のページに進みます。
1. 次のページで必要な情報を入力し、フォームを送信します。 **E コマース** タブに戻り、初期化が開始されていることを確認します。
1. 初期化の状態を表示するには、**更新** もしくは後で **E コマース** タブに戻ります。
    
e コマースが LCS から初期化されると、システムは e コマースに必要な複数のコンポーネントをプロビジョニングし、それらを環境に関連付けます。 プロビジョニングが完了すると、**小売管理** ページの **E コマース** タブが更新されて、プロビジョニングが反映されます。 このページには、最新のカスタマイズ配置と、進行中の他の配置状態が表示されます。 また、e コマース サイトと作成されるサイトの e コマース サイト ビルダーへのリンクも含まれています。

## <a name="access-commerce-site-builder"></a>Commerce のサイト ビルダーへのアクセス

Commerce サイト ビルダーにアクセスするには、LCS の **小売管理** ページの **e コマース** タブに移動し、**e コマース サイトの管理ツール** リンクを選択します。 サイト ビルダー ランディング ページには、テナント レベルのビューが表示されます。 このページから次の操作を実行できます。

- テナント レベルの設定を変更します。
- 作成したサイトで、表示するためのアクセス許可を持っているサイトに移動します。 
- 管理および報告などのレビュー機能にアクセスします。
- 新しいサイトを作成します。 新しいサイトを作成する方法の詳細については、[新しい e コマース サイトの作成](create-ecommerce-site.md) を参照してください。 

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[eコマース サイトの作成](create-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]