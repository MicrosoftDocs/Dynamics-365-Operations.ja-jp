---
title: Azure Pipelines で LCS 接続を作成する
description: このトピックでは、Azure DevOps から Microsoft Dynamics Lifecycle Services (LCS) への接続を設定する方法について説明します。
author: jorisdg
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65b0248add7ea7c5cf24f6aca90402b59a0f93e1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744813"
---
# <a name="create-an-lcs-connection-in-azure-pipelines"></a>Azure Pipelines で LCS 接続を作成する

Microsoft Azure DevOps の [Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) 拡張機能には、Microsoft Dynamics Lifecycle Services (LCS) でアクションを実行できるパイプライン タスクがいくつか用意されています。 たとえば、資産のアップロード、資産のダウンロード、および環境のサービスを行うことができます。 LCS を正常に機能させるには、Azure DevOps で新しいサービス接続を設定する必要があります。 このサービス接続は、LCS に接続するために必要な認証の詳細を提供します。 Azure DevOps のサービス接続の詳細については、[サービス接続](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints) を参照してください。

このトピックは、[Azure Pipelines](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識を持っていることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加するには、[Dynamics 365 Finance and Operations ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントで Azure DevOps が有効化およびインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](https://docs.microsoft.com/azure/devops/marketplace/install-extension)を参照してください。

## <a name="prerequisites"></a>必要条件

Azure DevOps から対話する 1 つ以上の LCS プロジェクトへのアクセス許可を持つユーザー資格情報が必要です。 このユーザーが以前に LCS に正常にサインインし、対話するプロジェクトのダッシュボードを開いたことを確認します。

> [!NOTE]
> LCS はサービス間認証をサポートしていません。 したがって、通常のユーザー資格情報 (ユーザー名およびパスワード) のみを使用できます。 パイプラインは対話的に実行されないため、使用するアカウントでは多要素認証を設定してはいけません。 セキュリティ上の目的で定期的にローテーションできる制限付きアクセスおよび強力な資格情報を持つ別のユーザー アカウントを設定することをお勧めします。

ユーザーの代わりに Azure DevOps から LCS に直接接続できるようにするには、Azure Active Directory (Azure AD) にアプリケーションを登録する必要があります。

1. [クイックスタート: Microsoft ID プラットフォームにアプリケーションを登録する](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) の指示に従い、新しいリダイレクト URI を追加します。

    1. **パブリック クライアント/ネイティブ (モバイル & デスクトップ)** を選択します。
    2. `http://localhost` などの有効な URI を入力します。

2. LCS web Api にアクセスするためのアクセス許可をアプリケーション登録に追加します。 [Web API にアクセスするためのアクセス許可の追加](https://docs.microsoft.com/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-your-web-api) の手順に従ってください。 API のアクセス許可を要求する場合は、**自分の組織で使用する API** を選択し、**Dynamics Lifecycle Services** を検索します。
3. 使用するアカウントに、Azure AD でのアプリケーション登録に対して同意が付与されていることを確認します。 [Azure Active Directory でエンドユーザーがアプリケーションに対して同意する方法を構成する](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-user-consent) の指示に従います。 特定のユーザーを有効にするか、テナント全体に対して管理者の同意を付与する ことができます。

## <a name="create-the-dynamics-lifecycle-services-service-connection"></a>Dynamics Lifecycle Services (LCS) へのサービス接続を作成する

パイプライン タスクから直接、またはプロジェクト設定ページから、新しいサービス接続を作成することができます。 サービス接続を作成する方法の詳細については、[サービス接続の作成](https://docs.microsoft.com/azure/devops/pipelines/library/service-endpoints#create-a-service-connection) を参照してください。 **Dynamics Lifecycle Services** へのサービス接続のダイアログ ボックスで、次の情報が提供されます。

- **認証エンドポイント** – 規定値は Azure クラウドのすべての Azure AD テナントで機能します。 Azure AD が国内クラウドにある場合は、[国内クラウド](https://docs.microsoft.com/azure/active-directory/develop/authentication-national-cloud) を参照して、正しい認証エンドポイントを検索します。
- **Lifecycle Services API エンドポイント** – エンドポイントを提供します。
- **ユーザー名** – ユーザー資格情報の電子メール エイリアスを提供します。
- **パスワード** – ユーザー資格情報のパスワードを提供します。
- **アプリケーション (クライアント) ID** – Azure AD でのアプリケーション登録用に以前に作成した ID を提供します。
- **サービス接続名** – 接続に意味のある名前を提供します。 この名前は、LCS 接続を必要とするパイプライン タスクの接続フィールドで表示されます。
- **説明** – この接続のオプションの説明を提供します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]