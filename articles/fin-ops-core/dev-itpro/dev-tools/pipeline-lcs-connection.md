---
title: Azure Pipelines で LCS 接続を作成する
description: このトピックでは、Microsoft Azure DevOps から LCS への接続を設定する方法について説明します。
author: jorisdg
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f80b28ceb25249f199764e70e68a7d592dfdb46
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765092"
---
# <a name="create-a-lifecycle-services-lcs-connection-in-azure-pipelines"></a>Azure Pipelines での Lifecycle Services (LCS)  接続の作成

Azure DevOps 用 [Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能には、Dynamics Lifecycle Services (LCS) でアクションを実行できるパイプライン タスクがいくつか用意されています。 たとえば、資産のアップロードとダウンロード、または環境のサービスを行うことができます。 LCS を正常に機能させるには、接続に必要な認証の詳細を含む Azure DevOps の新しい **サービス接続** を設定する必要があります。 Azure DevOps の **サービス接続** の詳細については、[サービス接続](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops) を参照してください。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension?view=azure-devops&tabs=browser)を参照してください。

## <a name="prerequisites"></a>必要条件

対話する 1 つ以上の LCS プロジェクトへのアクセス許可を持つユーザーの資格情報が必要です。 ユーザーが事前に LCS にログインしていることを確認し、Azure DevOps から通信元となるプロジェクトのダッシュボードを開きました。

> [!NOTE]
> LCS はサービス間認証をサポートしていません。 その結果、通常のユーザーの資格情報 (ユーザー名/パスワード) のみを使用できます。 パイプラインは対話的に実行されないため、使用するアカウントでは多要素認証を設定することはできません。 セキュリティ上の目的で定期的にを回転させることができる、限定アクセスと強力な資格情報を持つ別のユーザーアカウントを設定することをお勧めします。

Azure DevOps からの接続をユーザーの代わりに直接 LCS に接続できるようにするには、アプリケーションを自分の Azure Active Directory (AAD) に登録する必要があります。

1. [クイックスタート: Microsoft ID プラットフォームを持つアプリケーションを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) の指示に従い、新しい **リダイレクト URI** を追加します。

    - **パブリック クライアント/ネイティブ (モバイル & デスクトップ)** を選択します
    - 有効な URI を入力します (このURIは、たとえば、`http://localhost` など何でも構いません)

2. LCS web Api にアクセスするためのアクセス許可をアプリケーション登録に追加します。 [Web API にアクセスするためのアクセス許可の追加](https://docs.microsoft.com/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis) の手順に従ってください。 API のアクセス許可を要求する場合は、**自分の組織で使用する API** を選択し、**Dynamics Lifecycle Services** を検索します。

3. 使用するアカウントに、Azure AD でアプリケーション登録の同意が付与されていることを確認します。 [Azure Active Directory でエンドユーザーがアプリケーションに対して同意する方法を構成する](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-user-consent#grant-admin-consent-to-enterprise-apps-in-the-azure-portal) の指示に従います。 特定のユーザーを有効にするか、[テナント全体に対して管理者の同意を付与する](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-user-consent#grant-admin-consent-to-enterprise-apps-in-the-azure-portal) ことができます。

## <a name="create-the-dynamics-lifecycle-services-service-connection"></a>Dynamics Lifecycle Services (LCS) へのサービス接続を作成する

パイプライン タスクから直接、またはプロジェクトの設定ページから、新しい接続を作成することができます。 サービス接続の詳細は、[サービス接続の作成](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints?view=azure-devops) を参照してください。 **Dynamics Lifecycle Services** のサービス接続ダイアログで、次の情報を入力します。

- 認証エンドポイント: Azure クラウドのすべての Azure Active Directory (AAD) テナントに対して既定値が適用されます。 AAD が国内クラウドに配置されている場合は、[国内クラウド](https://docs.microsoft.com/azure/active-directory/develop/authentication-national-cloud) を参照して、正しい認証エンドポイントを見つけます。
- Lifecycle Services API エンドポイント: エンドポイントを提供します。
- ユーザー名: ユーザーの資格情報のメール エイリアスを指定します。
- パスワード: ユーザーの資格情報のパスワードを入力します。
- アプリケーション (クライアント) ID: アプリケーション登録用に作成した ID を AAD で事前に用意します。
- サービス接続名: 接続に意味のある名前を指定します。 この名前は、LCS 接続を必要とするパイプライン タスクの接続ドロップダウンで表示されます。
- 説明: この接続の説明を入力します (オプション)。

