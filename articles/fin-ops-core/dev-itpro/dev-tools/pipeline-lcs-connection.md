---
title: Azure Pipelines での Dynamics Lifecycle Services 接続の作成
description: この記事では、Azure DevOps から Microsoft Dynamics Lifecycle Services への接続を設定する方法について説明します。
author: gianugo
ms.date: 03/05/2020
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2020-08-19
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.openlocfilehash: bbb8967c3145ebe44eff4455fc59ebba4128a3d9
ms.sourcegitcommit: a3b1ed5b8ee0d99459b60a7082eb8fc75bcee687
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/04/2022
ms.locfileid: "9742691"
---
# <a name="create-a-dynamics-lifecycle-services-connection-in-azure-pipelines"></a>Azure Pipelines での Dynamics Lifecycle Services 接続の作成

Microsoft Azure DevOps 用 [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) 拡張機能には、Microsoft Dynamics Lifecycle Services でアクションを実行できるパイプライン タスクがいくつか用意されています。 たとえば、資産のアップロード、資産のダウンロード、および環境のサービスを行うことができます。 Dynamics Lifecycle Services を正常に機能させるには、Azure DevOps で新しいサービス接続を設定する必要があります。 このサービス接続により、Dynamics Lifecycle Services に接続するために必要な認証の詳細が提供されます。 Azure DevOps のサービス接続の詳細については、[サービス接続](/azure/devops/pipelines/library/service-endpoints) を参照してください。

この記事は、[Azure Pipelines](/azure/devops/pipelines/get-started/pipelines-get-started) の実用的な知識があることを前提としています。

> [!NOTE]
> これらのステップをパイプラインに追加する前に、Azure DevOps の [Dynamics 365 Finance and Operations Tools](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools)拡張機能が有効になっていて、Azure DevOps アカウントにインストールされている必要があります。 組織に拡張機能をインストールする方法の詳細については、[拡張機能のインストール](/azure/devops/marketplace/install-extension)を参照してください。

## <a name="prerequisites"></a>必要条件

Azure DevOps から関わりのある 1 つ以上の Dynamics Lifecycle Services プロジェクトへのアクセス許可を持つユーザー資格情報が必要です。 このユーザーが以前に Dynamics Lifecycle Services に正常にサインインし、関わりのあるプロジェクトのダッシュボードを開いたことを確認します。

> [!NOTE]
> Dynamics Lifecycle Services はサービス間認証をサポートしていません。 したがって、通常のユーザー資格情報 (ユーザー名およびパスワード) のみを使用できます。 パイプラインは対話的に実行されないため、使用するアカウントでは多要素認証を設定してはいけません。 セキュリティ上の目的で定期的にローテーションできる制限付きアクセスおよび強力な資格情報を持つ別のユーザー アカウントを設定することをお勧めします。

ユーザーの代わりに Azure DevOps から Dynamics Lifecycle Services に直接接続できるようにするには、Azure Active Directory (Azure AD) にアプリケーションを登録する必要があります。

1. [クイックスタート: Microsoft ID プラットフォームにアプリケーションを登録する](/azure/active-directory/develop/quickstart-register-app) の指示に従い、新しいリダイレクト URI を追加します。

    1. **パブリック クライアント/ネイティブ (モバイル & デスクトップ)** を選択します。
    2. `http://localhost` などの有効な URI を入力します。

2. アプリケーションの登録へのアクセス許可を追加して、Dynamics Lifecycle Services の Web API にアクセスします。 [Web API にアクセスするためのアクセス許可の追加](/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-your-web-api) の手順に従ってください。 API のアクセス許可を要求する場合は、**自分の組織で使用する API** を選択し、**Dynamics Lifecycle Services** を検索します。
3. 使用するアカウントに、Azure AD でのアプリケーション登録に対して同意が付与されていることを確認します。 [Azure Active Directory でエンドユーザーがアプリケーションに対して同意する方法を構成する](/azure/active-directory/manage-apps/configure-user-consent) の指示に従います。 特定のユーザーを有効にするか、テナント全体に対して管理者の同意を付与する ことができます。
4. パブリック クライアント アプリケーションとして登録を構成します。
    1. Azure ポータルで、**アプリの登録** でアプリを選択してから、**認証** を選択します。
    2. **詳細設定** > **パブリック クライアント フローを許可する** > **次のモバイル およびデスクトップ フローを有効にする:** で、**はい** を選択します。

## <a name="create-the-dynamics-lifecycle-services-service-connection"></a>Dynamics Lifecycle Services (LCS) へのサービス接続を作成する

パイプライン タスクから直接、またはプロジェクト設定ページから、新しいサービス接続を作成することができます。 サービス接続を作成する方法の詳細については、[サービス接続の作成](/azure/devops/pipelines/library/service-endpoints#create-a-service-connection) を参照してください。 **Dynamics Lifecycle Services** へのサービス接続のダイアログ ボックスで、次の情報が提供されます。

- **認証エンドポイント** – 規定値は Azure クラウドのすべての Azure AD テナントで機能します。 Azure AD が国内クラウドにある場合は、[国内クラウド](/azure/active-directory/develop/authentication-national-cloud) を参照して、正しい認証エンドポイントを検索します。
- **Dynamics Lifecycle Services API エンドポイント** – エンドポイントを提供します。 Dynamics Lifecycle Services プロジェクトがローカルの地域に配置されている場合は、正しい Dynamics Lifecycle Services API のエンドポイント アドレスを使用しているかを確認してください。 [ローカル展開オプションとエンドポイント](../deployment/deployment-options-geo.md#supported-local-geographies-and-endpoints) 記事を参照して、正しい API エンドポイントを検索してください。
- **ユーザー名** – ユーザー資格情報の電子メール エイリアスを提供します。
- **パスワード** – ユーザー資格情報のパスワードを提供します。
- **アプリケーション (クライアント) ID** – Azure AD でのアプリケーション登録用に以前に作成した ID を提供します。
- **サービス接続名** – 接続に意味のある名前を提供します。 この名前は、Dynamics Lifecycle Services 接続が必要なパイプライン タスクの接続フィールドに表示されます。
- **説明** – この接続のオプションの説明を提供します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
