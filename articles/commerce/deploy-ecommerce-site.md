---
title: 新しい E コマース テナントの配置
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい E コマース テナントを配置する方法について説明します。
author: psimolin
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945516"
---
# <a name="deploy-a-new-e-commerce-tenant"></a>新しい E コマース テナントの配置

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい E コマース テナントを配置する方法について説明します。

## <a name="overview"></a>概要
    
Microsoft Dynamics Lifecycle Services (LCS) は、パートナーや顧客がプロジェクト環境を管理したり、Microsoft Dynamics 製品や機能に関する最新情報を表示したり、サポート インシデントを作成、追跡、参照したりするために使用できる、クラウドベースのコラボレーション ワークスペースです。 E コマースの管理機能は LCS に統合されています。

LCS の詳細については、[Lifecycle Services ユーザー ガイド](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)を参照してください。
    
## <a name="get-started"></a>はじめに

E コマースを初期化する前に、プロジェクト、環境、および Retail Cloud Scale Unit (RCSU) を初期化する必要があります。 LCS で初期化を行うには、プロジェクト所有者ロールまたは環境マネージャ ロールのいずれかのアクセス許可が必要です。 実稼働環境とサンドボックス環境のトポロジがサポートされています。

環境に関する詳細については、[環境計画](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)を参照してください。 RCSU の詳細については、[Retail Cloud Scale Unit の初期化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)を参照してください。

## <a name="initialize-e-commerce"></a>E コマースの初期化

この手順を使用して、既存環境で E コマースを初期化します。

開始する前に、次の必要な情報があることを確認してください。

- 使用される RCSU。
- E コマース システムで使用される Microsoft Azure Active Directory セキュリティ グループ。
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

[!NOTE]
この情報は、サービス要求を介して後から追加できます。

必要な情報を収集したら、次の手順に従って E コマースを初期化します。

1. [LCS](https://lcs.dynamics.com) にサインインします。
1. E コマースを初期化する環境を含むプロジェクトを開きます。
1. **環境**セクションで、環境を選択します。
1. **環境機能**で、**小売管理**のリンクを選択します。
1. **E コマース** タブで、**設定**を選択します。 ダイアログ ボックスが表示されるので、プロビジョニングに必要な情報を入力します。
1. 必要な情報を入力し、次のページに進みます。
1. 次のページで必要な情報を入力し、フォームを送信します。 **E コマース** タブに戻り、初期化が開始されていることを確認します。
1. 初期化の状態を表示するには、**更新**もしくは後で **E コマース** タブに戻ります。
    
E コマースが LCS から初期化されると、システムは E コマースに必要な複数のコンポーネントをプロビジョニングし、それらを環境に関連付けます。 プロビジョニングが完了すると、**小売管理**ページの **E コマース** タブが更新されて、プロビジョニングが反映されます。 このページには、最新のカスタマイズ配置と、進行中の他の配置状態が表示されます。 また、E コマース サイトおよび E コマース サイト管理ツール (オーサリング ツール) へのリンクも含まれています。

## <a name="access-the-authoring-environment"></a>作成環境へのアクセス

作成環境にアクセスするには、**小売管理**ページの **E コマース** タブに移動します。 そこに、E コマース サイトとサイト管理ツールへのリンクが表示されます。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[E コマース サイトの作成](create-ecommerce-site.md)

[チャンネルとオンライン サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)

[場所に基づく店舗検出の有効化](enable-store-detection.md)
