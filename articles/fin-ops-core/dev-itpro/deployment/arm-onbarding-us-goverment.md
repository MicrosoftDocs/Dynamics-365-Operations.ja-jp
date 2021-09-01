---
title: 米国政府の Lifecycle Services プロジェクトに対する Azure Resource Manager オンボード プロセスの実行
description: このトピックでは、コネクタの Microsoft Azure Resource Manager オンボード プロセスを実施する方法について説明します。 このトピックは、Azure US government に適用されます。
author: saurabhsurana
ms.date: 08/12/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sasurana
ms.search.validFrom: 2021-07-31
ms.openlocfilehash: a1f296ab4c46c4e4ea1dff93830b3b12ae30d8f4
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386755"
---
# <a name="complete-the-azure-resource-manager-onboarding-process-for-us-government-lifecycle-services-projects"></a>米国政府の Lifecycle Services プロジェクトに対する Azure Resource Manager オンボード プロセスの実行

[!include [banner](../includes/banner.md)]

このトピックでは、コネクタの Microsoft Azure Resource Manager オンボード プロセスを実施する方法について説明します。

Azure Resource Manager トポロジをデプロイするには、コネクタに対して Resource Manager オンボード プロセスを実行する必要があります。 オンボード プロセスを開始するには、次の項目が必要です。

- 展開する Azure サブスクリプション ID

    > [!NOTE]
    > 米国政府機関向け Microsoft Dynamics Lifecycle Services (LCS) プロジェクトでは、Azure US government 固有の Azure サブスクリプションのみサポートされます。

- Azure サブスクリプションの所有権、またはサブスクリプション所有者へのアクセス。共同作成者ワークフローを追加し、管理証明書をアップロードできるようにする
- テナント管理者。管理者の同意ワークフローを介して作業を行えるようにする

## <a name="resource-manager-onboarding-process"></a>Resource Manager オンボード プロセス

Resource Manager オンボードは、各ステップに独自のサブ手順がある、2 ステップ手順とみなすことができます。 LCS プロジェクトに追加するすべてのサブスクリプションに対して、これらすべてのサブ手順を実施する必要があります。

1. Azure サブスクリプションで作業を行う LCS 配置サービスを承認します。

    1. ワークフローを認証します。
    2. 投稿者ワークフローを設定します。

2. Resource Manager リソースをデプロイする Azure サブスクリプションを有効にします。

    1. Azure コネクタを有効にし、LCS ユーザーを追加にします。
    2. 管理証明書のアップロード。
    3. 配置設定をコンフィギュレーションします。

### <a name="authorize-the-lcs-deployment-service-to-work-on-the-azure-subscription"></a>Azure サブスクリプションで作業を行う LCS 配置サービスを承認する

Azure サブスクリプションで動作するよう LCS 配置サービスを承認するには、次の手順を実行します。

#### <a name="authorize-the-workflow"></a>ワークフローを認証する

Azure Active Directory (Azure AD) PowerShell コマンドレットがインストールされていることを確認してください。 詳細については [Graph 用 Azure Active Directory PowerShell のインストール](/powershell/azure/active-directory/install-adv2?view=azureadps-2.0)を参照してください。

次の 2 つのアプリ ID が Azure AD テナントで承認されている必要があります。

- 68fdae24-7da6-4d2d-82b6-fd78a0f38eb7
- 913c6de4-2a4a-4a61-a9ce-945d2b2ce2e0

テナントでアプリ ID を承認するには、次の手順に従います。 各アプリケーションについてこの手順を実行します。

1. Azure AD PowerShell コマンドレットからサインインします。 テナント管理者アカウントを使用してサインインします。

    ```powershell
    Connect-AzureAD 
    ```

2. サービス プリンシパルがインストールされていないことを確認します。

    ```powershell
    Get-AzureADServicePrincipal -Filter "AppId eq '<AppId>'"
    ```

3. サービス プリンシパルを追加します。

    ```powershell
    New-AzureADServicePrincipal -AppId <AppId>
    ```

4. 各アプリケーション ID が正常に追加されたことを確認します。

    ```powershell
    $sp = Get-AzureADServicePrincipal -Filter "AppId eq '<AppId>'"
    ```

#### <a name="set-the-contributor-workflow"></a>投稿者ワークフローを設定

**寄稿者** ロールを **Dynamics 配置サービス \[wsfed 有効 \]** アプリケーションに割り当てるため、これらの手順に従います。

1. [Azure ポータル](https://portal.azure.com)の **サブスクリプション** タブで、Azure サブスクリプションを選択してから、ナビゲーション メニューで **アクセス制御 (IAM)** の項目をクリックします。
2. **追加** を選択し、**ロール割り当ての追加** を選択します。
3. **ロール割り当ての追加** ダイアログ ボックスで、**ロール** フィールドを **共同作成者** に、**アクセス権の割り当て先** フィールドを **Azure AD** ユーザー、グループ、サービス プリンシパルに設定します。 **選択** フィールドで **Dynamics 配置サービス \[wsfed 有効\]** を検索して選択します。 その後、**保存** を選択します。

    > [!NOTE]
    > 一部の Azure サブスクリプションでは、ナビゲーション メニューに **アクセス制御 (IAM)** 項目ではなく、**ユーザー** 項目があります。 この場合、**ユーザーの追加** ダイアログ ボックスの **選択** フィールドに、**Dynamics 配置サービス \[wsfed 有効\]** と入力して選択をクリックします。 **選択する** を選択します。

    [![ロール割り当ての追加ダイアログ ボックスで Dynamics 配置サービス \[wsfed 有効\]を選択する](./media/arm_redo_02.png)](./media/arm_redo_02.png)

3. **ロールの割り当て** タブで、アプリは共同作成者として割り当てられます。

    > [!NOTE]
    > **Dynamics 配置サービス \[wsfed 有効\]** が表示されない場合、承認プロセスは完了していないか、別の Azure サブスクリプションで完了しています。

### <a name="enable-the-azure-subscription-to-deploy-resource-manager-resources"></a>Resource Manager リソースをデプロイする Azure サブスクリプションを有効にする

Azure サブスクリプションを有効にして Resource Manager リソースをデプロイできるようにするには、次の手順を実行します。

#### <a name="enable-the-azure-connector-and-add-an-lcs-user"></a>Azure コネクタを有効、および LCS ユーザーを追加

Azure コネクタを有効にし、必要に応じて LCS ユーザーを追加するには、以下の手順に従います。

1. LCS で、**プロジェクト** ページの **環境** セクションにある、**Microsoft Azure 設定** を選択します。
2. **プロジェクト設定** ページでは、**Azure コネクタ** タブの、**Azure コネクタ** の下で **追加** を選択します。

    > [!NOTE]
    > 既存のコネクタに対して Resource Manager を有効にする場合は、**追加** ではなく **編集** を選択します 。

3. コネクタ名および配置する Azure サブスクリプション ID を入力し、**Azure Resource Manager を使用するコンフィギュレーション** オプションを **はい** に設定します。
4. **Azure サブスクリプション AAD テナント ドメイン** フィールドで、Azure サブスクリプション アカウント管理者のドメイン名を入力し、**次へ** を選択します。
5. **Microsoft Azure 設定** ページで、**ダウンロード** を選択します。 証明書ファイルをダウンロードした場所をメモしておきます。 この情報を使用して、証明書を Azure サブスクリプションにアップロードします。
6. [Azure ポータル](https://portal.azure.com)で、対象のサブスクリプションにアクセスします。 左ペインで、**管理証明書** を選択します。
7. 使用する Azure サブスクリプションへフィルター処理をし、次に、**管理証明書** タブで、**アップロード** を選択します。
8. 手順 5 でダウンロードした管理証明書を選択し、**OK** を選択します。

#### <a name="configure-deployment-settings"></a>配置設定のコンフィギュレーション

1. LCS で、**プロジェクト** ページの **環境** セクションにある、**Microsoft Azure 設定** を選択します。
2. **プロジェクト設定** ページが表示されます。 **Azure コネクタ** エリアで、**追加** をクリックします。
3. **Microsoft Azure 設定** ページで、デプロイする地域を選択し、**接続** を選択します。 これで Resource Manager オンボード フローは完了です。 **Azure コネクタ** リストにサブスクリプションが追加されたのが確認できるはずです。 また、チェック マークは **ARM 有効** で表示されます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
