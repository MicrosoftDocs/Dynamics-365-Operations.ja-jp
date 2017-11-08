---
title: "プロジェクト時間入力モバイル ワークスペース"
description: "このトピックでは、プロジェクト時間入力モバイル ワークスペースに関する情報を提供します。 このワークスペースにより、ユーザーはモバイル デバイスを使用して入力をし、プロジェクトに対して時間を節約できます。"
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 2acf5a982988fe00492523ed5ce77d6de4a9e146
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="project-time-entry-mobile-workspace"></a>プロジェクト時間入力モバイル ワークスペース

[!include[banner](../includes/banner.md)]

このトピックでは、[**プロジェクト時間入力**] モバイル ワークスペースに関する情報を提供します。 このワークスペースにより、ユーザーはモバイル デバイスを使用して入力をし、プロジェクトに対して時間を節約できます。

このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリで使用するためのものです。 

## <a name="overview"></a>概要
毎日の作業の一環として、プロジェクト リソースは多くの場合オンサイトか、または出張します。 **プロジェクト時間入力** モバイル ワークスペースでは、選択したモバイル デバイスで、プロジェクトに対する支払請求可能または非請求可能な時間を入力できます。 そのためプロジェクト リソースは、いつでも、どこでも時間のエントリを記録できます。 既に記録されている時間のエントリを表示することもできます。 

具体的には、[**プロジェクト時間の入力**] モバイル ワークスペースでは、ユーザーは、これらのタスクを実行できます。

-   選択された任意の日付について、特定のタスクに費やした時間数を入力します。
-   時間を入力するプロジェクトを特定するため、プロジェクト名または顧客で検索します。
-   費やした時間のカテゴリおよび活動を指定します。
-   プロジェクトに支払請求可能または非請求可能として時間を記録します。
-   必要に応じて外部または内部コメントを入力します。

## <a name="prerequisites"></a>前提条件
組織に配置されている Microsoft Dynamics 365 のバージョンに基づいて、前提条件は異なります。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 7 月) を使用している場合の前提条件 
Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 ７ 月) を組織に配置している場合、システム管理者は [**プロジェクト時間の入力**] モバイル ワークスペースを公開する必要があります。 手順については、「[モバイル ワークスペースの公開](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用している場合の前提条件
Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム 更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。 

<table>
<thead>
<tr class="header">
<th>前提条件</th>
<th>役割</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>KB 4018050 を実装します。</td>
<td>システム管理者</td>
<td>KB 4018050 は、<strong>プロジェクト時間入力</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。 KB 4018050 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>ApplicationSuite</strong> と <strong>ProjectMobile</strong> モデルを含む <a href="../../dev-itpro/deployment/create-apply-deployable-package.md">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">配置可能パッケージを適用します</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td>[<strong>プロジェクト時間の入力</strong>] モバイル ワークスペースを公開します。</td>
<td>システム管理者</td>
<td>「<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>モバイル アプリのダウンロードとインストール

Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。

-   [Android フォン用](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone 用](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>モバイル アプリにログインします。
1.  モバイル デバイスでアプリを起動します。
2.  Dynamics 365 の URL を入力します。
3.  初めてサインインすると、ユーザー名とパスワードを要求されます。 資格情報を入力します。
4.  サインインすると、使用可能な会社のワークスペースが表示されます。 なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。

[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>プロジェクト時間入力モバイル ワークスペースを使用して時間を入力します。
1.  モバイル デバイスで、**プロジェクト時間入力** ワークスペースを選択します。
2.  **時間入力** を選択します。 現在の週のカレンダーの日付が表示されます。
3.  選択された日付で、**アクション** &gt; **新しいエントリ** を選択します。
4.  記録する時間数を入力します。
5.  時間入力するプロジェクトを選択します。 オフラインで使用する場合のために、アプリに読み込まれたプロジェクトのリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を参照してください。
6.  プロジェクトが一覧にない場合は、[**検索**] を選択します。 名前で検索するか、プロジェクト名または顧客での検索に切り替えます。
7.  カテゴリを選択します。 オフラインで使用する場合のために、アプリに読み込まれたカテゴリのリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を参照してください。
8.  カテゴリが一覧にない場合は、[**検索**] を選択します。 カテゴリで検索するか、カテゴリ名での検索に切り替えます。
9.  活動を選択します。 一覧には、オフラインで使用するためにアプリケーションに読み込まれた活動が表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、[モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を参照してください。
10. 活動が一覧にない場合は、[**検索**] を選択します。 活動番号で検索するか、目的別の検索に切り替えます。

11. 明細行プロパティを選択します。
12. オプション: 外部または内部コメントを入力します。
13. **完了** を選択します。

