---
title: Dataverse 仮想エンティティの構成
description: このトピックでは、Microsoft Dataverse で Finance and Operations アプリの仮想エンティティを構成する方法について説明します。
author: Sunil-Garg
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 2d727395db8f7c2cb8c12b2ece80be0ef1d8bfd0
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913766"
---
# <a name="configure-dataverse-virtual-entities"></a>Dataverse 仮想エンティティの構成

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dataverse で Finance and Operations アプリの仮想エンティティを構成する方法について説明します。

> [!IMPORTANT]
> このトピックに含まれる構成手順が必要となるのは、 Microsoft Power Platform 統合が有効に **なっていない** Finance and Operations アプリ環境に対してのみです。 Microsoft Power Platform 統合が有効になっている Finance and Operations アプリ環境のために、統合を有効にするプロセスの一部としてこのトピックで説明した仮想エンティティ構成が実行されます。 
> 
> Dataverse 仮想エンティティがを手動で構成された場合、Microsoft Power Platform 統合を有効にする前にこのトピックのガイダンスに従うと、Microsoft Power Platform 統合が有効にされた後、手動構成はリンクされた Power Platform 環境を使用しません。 仮想エンティティは、Microsoft Power Platform 統合によって提供される自動構成を使用して Dataverse 環境に接続します。 ただし、Finance and Operations アプリ環境を Microsoft Power Platform 統合が有効になっていない追加の Power Platform 環境に接続するには、仮想エンティティの手動構成が使用されます。
> 
> Finance and Operations アプリ環境の Microsoft Power Platform 統合を有効にする方法の詳細については、[Microsoft Power Platform 統合の有効化](enable-power-platform-integration.md) を参照してください。

## <a name="getting-the-virtual-entity-solution"></a><a name="get-virtual-entity-solution"></a> 仮想エンティティ ソリューションの取得

Finance and Operations 仮想エンティティの Dataverse ソリューションは、Microsoft AppSource 仮想エンティティ ソリューションからダウンロードする必要があります。 詳細については、[Finance and Operations 仮想エンティティ](https://appsource.microsoft.com/product/dynamics-crm/mscrm.finance_and_operations_virtual_entity) を参照してください。

次のソリューションが Dataverse にインストールされていることを確認します。

- **Dynamics365Company**: すべての Finance and Operations エンティティによって参照される **会社** エンティティを、PrimaryCompanyContext メタデータ値と共に追加します。

- **MicrosoftOperationsVESupport**: これにより、Finance and Operations 仮想エンティティ機能のコア サポートが提供されます。

- **MicrosoftOperationsERPCatalog**: これは、mserp_financeandoperationsentity 仮想エンティティを通じて使用できる Finance and Operations エンティティの一覧を提供します。

- **MicrosoftOperationsERPVE**: これは、表示されるときに生成された仮想エンティティを含む、API マネージド ソリューションです。

仮想エンティティ ソリューションで更新を使用できる場合は、Power Platform 管理センターで手動で適用できます。 仮想エンティティ ソリューションを手動でインストールおよび更新する方法の詳細については [Dynamics 365 アプリの管理](/power-platform/admin/manage-apps) を参照してください。 

> [!NOTE]
> Microsoft Power Platform 統合が有効になっている Finance and Operations アプリ環境では、仮想エンティティ ソリューションに対する更新可能な更新が自動的に適用されます。

## <a name="authentication-and-authorization"></a>認証と承認

ソリューションを Dataverse 環境にインポートした後は、両方の環境を相互に接続するように設定する必要があります。 Dataverse は、Azure Active Directory (Azure AD) アプリケーションに基づいて、サービス間 (S2S) 認証を使用して Finance and Operations アプリを呼び出します。 環境この新しい Azure AD アプリケーションは、Dataverse 環境の単一のインスタンスを表します。 Dataverse と Finance and Operations アプリ環境の組み合わせが複数存在する場合は、組み合わせごとに独立した Azure AD アプリケーションを作成して、 Finance and Operations アプリと Microsoft Power Platform 環境の正しい組み合わせの間で確実に接続が確立されるようにする必要があります。 

### <a name="register-the-app-in-the-azure-portal"></a>Azure ポータルでアプリを登録する

次の手順では、Azure AD アプリケーションの作成方法を説明します。

> [!IMPORTANT]
> Azure AD アプリケーションは、Finance and Operations アプリと同じテナントに作成する必要があります。

1.  <https://portal.azure.com> **\> Azure Active Directory \> アプリの登録** に移動します。

2.  **新規登録** を選択します。 次の情報を入力します。

    - **名前**: 一意の名前を入力します。

    - **アカウント タイプ**: **任意の Azure AD ディレクトリ** を入力します (単一またはマルチテナント)。

    - **リダイレクト URI**: 空白のままにします。

    - **登録** を選択します。

    - 後の手順で必要となるため、**アプリケーション (クライアント) ID** の値をメモしておきます。

3.  アプリケーションの対称キーを作成します。

    - 新しく作成されたアプリケーションで **証明書とシークレット** を選択します。

    - **新しいクライアント シークレット** を選択します。

    - 説明と有効期限を入力します。

    - **保存** を選択します。 キーが作成され、表示されます。 この値を後で使用するためにコピーします。

### <a name="grant-app-permissions-in-finance-and-operations-apps"></a>Finance and Operations アプリのアクセス許可を付与する

作成した Azure AD アプリケーションは、Dataverse によって Finance and Operations アプリを呼び出すために使用されます。 したがって、Finance and Operations アプリによって信頼され、 適切な権限を持つユーザー アカウントに関連付けられている必要があり ます。 仮想エンティティ機能への権限 **のみ** を持つ特殊サービス ユーザーは、Finance and Operations アプリで作成される必要があります。 このサービス ユーザーには、その他の権限が設定されている必要はありません。 この手順を完了した後、作成した Azure AD アプリケーションのシークレットを持つアプリケーションによって、この Finance and Operations アプリ環境を呼び出して仮想エンティティの機能にアクセスできるようになります。

1.  Finance and Operations で、**システム管理 \> ユーザー \> ユーザー** の順に移動します。

2.  **新規作成** を選択して、新しいユーザーを追加します。 次の情報を入力します。

    - **ユーザー ID**: **dataverseintegration** (または別の値) を入力します。

    - **ユーザー名** - **dataverse 統合** (または別の値) を入力します。

    - **プロバイダー** - **NonAAD** に設定します。

    - **電子メール**: **dataverseintegration** (または別の値) を入力します (有効な電子メール アカウントである必要は *ありません*)。

    - このユーザーにセキュリティ ロール **CDS 仮想エンティティ アプリケーション** を割り当てます。

    - **システム ユーザー** を含む他のすべてのロールを削除します。

3.  **システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動して Dataverse を登録します。 

    - 新しい行を追加します。

    - **クライアント ID**: 上で作成された **アプリケーション (クライアント) ID**

    - **名前** - **Dataverse 統合** (または別の名前) を入力します。

    - **ユーザー ID**: 上記で作成されたユーザー ID。

## <a name="configure-the-virtual-entity-data-source"></a>仮想エンティティ データ ソースの構成

プロセスの次の手順では、接続先の Finance and Operations インスタンスに Dataverse を提供します。 以下の手順では、プロセスのこの部分について説明します。

1.  Dataverse では、**詳細設定 \> 管理 \> 仮想エンティティ データ ソース** に移動します。

2.  「Finance and Operations」というデータ ソースを選択します。

3.  上記の手順に従って情報を入力します。

    - **ターゲット URL**: Finance and Operations にアクセスできる URL。

    - **OAuth URL** - https://login.windows.net/

    - **テナント ID**- 「contoso.com」などのテナント。

    - **AAD アプリケーション ID**: 上で作成された **アプリケーション (クライアント) ID**。

    - **AAD アプリケーション シークレット**: 上で生成されたシークレット。

    - **AAD リソース**- 00000015-0000-0000-c000-000000000000 と入力します (これは、Finance and Operations を表す Azure AD アプリケーションで、常に同じ値であることを表します)。

4.  変更を保存します。

仮想エンティティ の構成が完了したら、Dataverse で仮想エンティティを有効にできます。 詳細については、[Microsoft Dataverse 仮想エンティティの有効化](enable-virtual-entities.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
