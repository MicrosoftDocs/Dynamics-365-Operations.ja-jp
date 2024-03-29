---
title: 財務と運用アプリの技術サポートの設定
description: この記事では、クラウドおよびオンプレミス配置のサポートについて説明します。
author: sericks007
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 29531
ms.assetid: 3734bd06-6d4c-42f5-8f2b-30a451189002
ms.openlocfilehash: d5d0b9942ca19225c9472ce686bbaa1441b8e0dc
ms.sourcegitcommit: 29af4c9d9968bbfa4c19fee9de34fed309f6d38b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2022
ms.locfileid: "9388464"
---
# <a name="set-up-technical-support-for-finance-and-operations-apps"></a>財務と運用アプリの技術サポートの設定 
[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>必要条件

テクニカル サポートの設定をする前に、Microsoft Azure Active Directory (Azure AD) アカウントを取得する必要があります。 このアカウントは、財務と運用アプリのいずれかのサブスクリプションを設定すると作成されます。

## <a name="create-an-azure-devops-project"></a>Azure DevOps プロジェクトの作成
Lifecycle Services (LCS) プロジェクトの **サポート** タイルは、Azure DevOps を使用し、クライアントを通して送信された問題と、LCS の **サポート** タイルから手動で作成された問題を格納します。 この機能を使用するには、サポートに使用する LCS プロジェクトで Azure DevOps プロジェクトを設定する必要があります。 **サポート** タイルを使用して問題を提出する必要があるすべてのユーザーは、Azure DevOps プロジェクトにアクセスできる必要があり、LCS が Azure DevOps に自身が代わってアクセスを承認する必要があります。 ほとんどのユーザーは、LCS または Azure DevOps へのアクセス権がありません。 したがって、Azure DevOps プロジェクトでは、問題を提出するために使用できる特別なシステム アカウントを作成する必要があります。

### <a name="create-a-new-azure-devops-project"></a>新しい Azure DevOps プロジェクトの作成

1.  <https://www.visualstudio.com/> に移動します。
2.  右上隅にある **サインイン** をクリックします。
3.  サブスクリプションがリンクされているテナントに含まれる AAD アカウントを使用してサインインします。 ブラウザーにすでに資格情報が割り当てられている場合は、サインイン ページは表示されず、右上隅にあるユーザーの名前をクリックする必要があります。
4.  ページの右側の、**アカウント** で、**今すぐ無料のアカウントを作成** をクリックします。
5.  アカウント URL を指定し、**アカウントの作成** をクリックします。
6.  プロジェクトに名前を付け、プロセス テンプレートを指定します。 これで、プロジェクトが作成されます。

### <a name="add-users-to-the-azure-devops-project"></a>Azure DevOps プロジェクトへのユーザーの追加

1.  左上にある **Team Services** をクリックします。
2.  **ユーザー** タブで、**追加** をクリックし、サポート エクスペリエンスを使用するユーザーを Azure DevOps アカウントに招待します。 招待する各ユーザーについては、**基本** または **利害関係者** のいずれかを選択します。
3.  左上にある **Team Services** をクリックします。
4.  **参照** をクリックし、以前の手順で作成されたプロジェクトを参照します。
5.  プロジェクト ホーム ページの **メンバー** セクションで、**追加** をクリックして手順 2 で招待したユーザーを追加します。

### <a name="create-the-support-system-user"></a>サポート システム ユーザーを作成する

1.  Azure AD テナントで新しいユーザーを作成し、**LcsCpsSystemAccount** などの内容を示す名前を入力します。
2.  左上にある **Team Services** をクリックします。
3.  **ユーザー** タブで、**追加** をクリックし、手順 1 で作成したシステム ユーザーを招待します。 このユーザーについては、**利害関係者** を選択します。
4.  左上にある **Team Services** を再度クリックします。
5.  **参照** をクリックし、以前に作成したプロジェクトを参照します。
6.  プロジェクト ホーム ページの **メンバー** セクションで、**追加** をクリックしてシステム ユーザーを追加します。

### <a name="retrieve-the-personal-access-token-for-the-support-system-user"></a>サポート システム ユーザーの個人用アクセス トークンを取得

1.  右上隅にあるユーザー名をクリックして **サインアウト** をクリックすることで、Team Services からサインアウトします。
2.  前の手順で作成したサポート システム アカウントを使用して Team Services にサインインします。
3.  右上隅でユーザー名をクリックしてから、**自分のプロファイル** をクリックします。
4.  **セキュリティ** タブの、**個人用アクセス トークン** タブで、**追加** をクリックします。
5.  **LCS サポート システム アカウント** のような説明を入力します。
6.  1 年の有効期限を選択します。
7.  **選択されているスコープ** をクリックし、**作業項目 (読み取り/書き込み)** を選択します。
8.  **トークンの作成** をクリックします。
9.  ページから移動した後にアクセスできなくするため、トークンをコピーして、安全な場所に貼り付けます。

## <a name="configure-lcs"></a>LCS の構成
1.  アプリケーションが配置された LCS プロジェクトの **所有者** ロールを持っているアカウントを使用して、LCS にサインインします。
2.  LCS でプロジェクトを開きます。
3.  **プロジェクト設定** をクリックし、**Azure DevOps** リンクをクリックします。

    [![LCS-Project-Tiles.](./media/lcs-project-tiles-237x300.png)](./media/lcs-project-tiles.png)
    
    [![LCS-Project-Settings-VSO.](./media/lcs-project-settings-vso-1024x320.png)](./media/lcs-project-settings-vso.png)

4.  **Azure DevOps の設定** をクリックします。
5.  **Azure DevOps サイトの URL** フィールドに、前のセクションで作成した Azure DevOps プロジェクトの URL を入力します。

    > [!NOTE]
    > LCS では、Azure DevOps のルート URL をレガシー形式で入力する必要があります。 レガシ形式は `https://ACCOUNT.visualstudio.com` と `https://contoso.visualstudio.com` です。

6.  **個人用アクセス トークン** フィールドに、前のセクションで作成した個人用アクセス トークンを入力します。 

    [![前のセクションで作成した個人用アクセス トークンを入力します。](./media/lcs-project-settings-vso-setup-1.png)](./media/lcs-project-settings-vso-setup-1.png)

7.  **続行** をクリックします。
8.  使用する VSO プロジェクトを選択し、**続行** をクリックします。
9.  **保存** をクリックします。
10. **承認** をクリックします。
11. 確認メッセージ ボックスで、**OK** をクリックします。
12. Visual Studio Online へサインインします。
13. **承認** をクリックします。

## <a name="create-an-issue"></a>問題の作成 
Microsoft によって公開されている更新プログラムを表示するため、サポート エクスペリエンスが更新されました。 クライアントの上部バーで、**?** をクリックしてから **サポート** をクリックします。 

> [!WARNING]
> オンプレミスで配置している場合、既存の問題を検索してオンプレミス クライアントから Azure DevOps プロジェクトにサポート インシデントを送信することはできません。

[![wiki1.](./media/wiki1-1024x518.png)](./media/wiki1.png) 

> [!NOTE]
> Lifecycle Services (LCS) にまだ接続していない場合は、ダイアログ ボックスに接続できる場所が表示されます。 続行する前に、接続するリンクをクリックしてください。 
    [![クリックして Lifecycle Services に接続する。](./media/wiki2.png)](./media/wiki2.png)


### <a name="search-for-a-fix"></a>修正プログラムの検索

LCS に接続した後は、既存の Microsoft 更新プログラムおよび修正を検索できます。 **検索** ボックスに問題を入力し、**入力** を押します。 

> [!NOTE]
> すべてのユーザーに対して有効な既存の修正プログラムを検索する機能を使用しない場合は、**SearchExistingFixes** の職務をシステム ユーザー ロールから削除し、この機能を追加するロールにのみ追加できます。 検索結果は、環境に関連する Microsoft 問題検索データに基づきます。 既にインストールした修正は、検索結果には含まれません。 特定の結果を表示するには、リンクをクリックして詳細を表示します。 

割り当てられた職務に基づいて、**ダウンロード表示** または **要求表示** が表示されます。 

- **ダウンロード表示** - 既定では、この表示はシステム管理者のみが使用できます。 このビューから、直接修正プログラムをダウンロードできます。 

    > [!NOTE]
    > 職務 **DownloadHotfix** は、修正プログラムを要求するのではなく、LCS から直接ダウンロードする機能を制御します。 既定では、システム管理者のみそのアクセス権があります。 この職務をシステム管理者以外のユーザーに割り当てる場合は、職務を選択したロールに追加します。 
    
- **要求表示** - 既定では、システム管理者ではないすべてのユーザーがこのビューを使用できます。 このビューから、修正プログラムのダウンロードを要求できます。 修正プログラムをダウンロードする要求を送信した後は、LCS プロジェクトに関連付けられている Azure DevOps プロジェクトに作業項目が作成されます。 顧客の IT 管理者は、LCS の **サポート** タイルをクリックし、**修正プログラムの要求** タブをクリックして、要求したすべての修正プログラムを表示できます。

### <a name="search-for-project-work-items-in-azure-devops"></a>Azure DevOps で、プロジェクトの作業項目を検索

Azure DevOps 管理者は、**#SearchableInFinanceAndOperations** を作業項目にタグ付けすることによって、プロジェクトの作業項目を組織のユーザーに発行することができます。 タグ付けされた作業項目は、クライアント サポート検索ボックスからユーザーに対して検索可能になります。 検索結果には、Microsoft が公開した更新プログラムや修正プログラムに加えて、タグ付きの Azure DevOps 作業項目が含まれます。 次のグラフィックは、公開用のタグ付きの Azure DevOps 作業項目を示しています。

[![vstsTag.](./media/VSTS-Tagging.png)](./media/VSTS-Tagging.png)

サポート検索ボックスを使用して公開済みの Azure DevOps 作業項目を検索するとき、検索結果は、新しいブラウザー タブに **表示** モードで、作業項目のタイプ、タイトル、状態、および説明が表示されます。  適切なアクセス許可を持つユーザーが、Azure DevOps の作業項目を編集できます。 次のグラフィックは、公開された Azure DevOps 作業項目の検索結果を示しています。

[![ViewVSTS.](./media/ViewVSTSItem.png)](./media/ViewVSTSItem.png)

> [!NOTE]
> 発行済みの Azure DevOps 作業項目は、組織のユーザーにのみ表示されます。  

### <a name="create-and-submit-a-new-issue"></a>新しい問題の作成および送信
検索結果から修正プログラムが見つからない場合は、**作成** をクリックし、新しい問題を作成できます。 これは以前のリリースで使用できる機能と同じで、以前の手順で説明しています。

## <a name="work-with-issues-in-lcs"></a>LCS での問題についての作業

### <a name="view-issues"></a>問題の表示
LCS **サポート** タイルでは、問題が LCS プロジェクトに関連付けられている Azure DevOps プロジェクトで作業項目として保存されます。 具体的には、問題は、Azure DevOps プロジェクトのタイプに応じて **問題** または **懸案事項** タイプの作業項目として **AxAndLcsGeneratedIssues** 領域に保存されます。 その地域にあるタイプの作業項目のすべてが、**サポート** タイルの問題リストに含まれます。 Azure DevOps で問題点が変更されると、サポート案件で変更内容が反映されます。 問題は、Azure DevOps プロジェクト内のユーザーに割り当てることができます。 ユーザーは、Azure DevOps で案件を取り扱うために、LCS にアクセスする必要はありません。

1.  [lcs.dynamics.com,](https://lcs.dynamics.com/en/) に移動しサインインします。
2.  払出を表示する環境に関連付けられている LCS プロジェクトを開きます。
3.  **サポート** タイルをクリックします。 作成された問題の一覧を表示します。

    [![LCS-CPS-list.](./media/lcs-cps-list-1024x243.png)](./media/lcs-cps-list.png)

### <a name="edit-issues"></a>項目を編集
1.  **問題** グリッドで、問題のタイトルをクリックします。
2.  必要に応じて、この記事の最初のセクションで設定した Azure DevOps プロジェクトへのアクセス権を持つアカウントを使用して、Azure DevOps へサインインし、**Azure DevOps プロジェクトを作成** します。 

    > [!NOTE]
    > Azure DevOps には、サインインが必要な場合に作業項目を編集するためのリンクが正しく機能しないという問題があります。 Azure DevOps にサインインした後に **自分自身に割り当て** クエリが表示された場合、LCS に戻って、問題グリッドで問題のタイトルをもう一度クリックします。

3.  Azure DevOps エディターが開きます。 問題点を編集し、変更を保存します。 変更は **サポート** タイルに反映されます。


### <a name="submit-an-issue-to-microsoft"></a>Microsoft に問題を送信

Microsoft サポートに問題を送信することができます。 Microsoft に問題点を送信すると、問題に関する情報と添付ファイルを Microsoft サポート インシデントに含めることができます。 

Microsoft に問題を送信するためには、LCS ユーザーに有効な Microsoft サポート プランが必要です。 Microsoft に問題を報告する上で問題が発生している場合は、管理者と連携して、LCS 資格情報が、Microsoft Partner Source Business Center との組織のサポート計画に追加されている、または関連付けられているかを確認します。

1.  **問題** グリッドで、Microsoft に送信する問題を選択して、**Microsoft に送信** をクリックします。
2.  アカウントが複数のサポート組織に関連付けられている場合、使用する組織を選択して Microsoft サポート インシデントを作成します。
3.  **問題検索** を使用して、問題がまだ解決されていないことを確認します。
4.  **問題検索** により問題が解決されない場合、ページの下部にある **作成インシデント** をクリックします。
5.  Microsoft サポート チームに診断データを共有します。 バージョン情報を提供することによって、問題をより迅速に解決できます。
6.  問題を説明し、連絡先情報を入力してから、**送信** をクリックします。

## <a name="support-settings"></a>サポート設定 

> [!NOTE]
> このセクションの情報は、オンプレミスの配置には適用されません。 

アプリケーションを Lifecycle Services から配置するとき、構成は必要ありません。それは、サポート ツールが、配置された財務と運用の供給元である同じ LCS プロジェクトに問題を自動的に保存するためです。 サポートされている LCS プロジェクトを確認するには、**システム管理** > **設定** > **システム パラメーター** に移動し、**ヘルプ** > **サポートの連絡先** をクリックします。 

## <a name="prevent-users-from-creating-issues-from-the-client"></a>ユーザーが、クライアントからの問題を作成できなようにする
既定では、システム ユーザー ロールに *SysLCSCPSIssueEntry* という権限が割り当てられています。 この権限は、[ヘルプ] メニューの **サポート チームに連絡** メニュー項目へのアクセスを制御します。 ユーザーがクライアントからの問題を作成して送信できないようにするには、システム ユーザー ロールからこの権限を削除します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
