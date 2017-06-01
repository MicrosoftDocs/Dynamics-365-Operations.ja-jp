---
title: "Dynamics 365 for Operations アプリ用のプロジェクト時間入力モバイル ワークスペース"
description: "このトピックでは、プロジェクト時間入力モバイル ワークスペースに関する情報を提供します。 このワークスペースにより、ユーザーはモバイル デバイスを使用して入力をし、プロジェクトに対して時間を節約できます。"
author: annbe
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9c592c301908898915164e9236850759b73543fe
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>プロジェクト時間入力モバイル ワークスペース

[!include[banner](../includes/banner.md)]



このトピックでは、Dynamics 365 for Operations モバイル アプリ用の、プロジェクト時間入力モバイル ワークスペースについて説明します。 このワークスペースにより、ユーザーはモバイル デバイスを使用して入力をし、プロジェクトに対して時間を節約できます。

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>プロジェクト時間入力モバイル ワークスペースの概要
---------------------------------------------------

毎日の作業の一環として、プロジェクト リソースは多くの場合オンサイトか、または出張します。 **プロジェクト時間入力** モバイル ワークスペースでは、選択したモバイル デバイスで、プロジェクトに対する支払請求可能または非請求可能な時間を入力できます。 そのためプロジェクト リソースは、いつでも、どこでも時間のエントリを記録できます。 既に記録されている時間のエントリを表示することもできます。 

具体的には、**プロジェクト時間入力** モバイル ワークスペースは次の機能を提供します。

-   選択された任意の日付について、特定のタスクに費やした時間数を入力します。
-   時間を入力するプロジェクトを特定するため、プロジェクト名または顧客で検索します。
-   費やした時間のカテゴリおよび活動を指定します。
-   プロジェクトに支払請求可能または非請求可能として時間を記録します。
-   必要に応じて外部または内部コメントを入力します。

**プロジェクト時間入力** モバイル ワークスペースを実装するには、このトピックの次のセクションを参照してください。

## <a name="prerequisites"></a>前提条件
**プロジェクト時間入力** モバイル ワークスペースを実装する前に、システム管理者が次の前提条件を満たしていることを確認してください。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>前提条件</th>
<th>役割</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を実装する必要があります。</td>
<td>システム管理者</td>
<td>Dynamics 365 for Operations をまだ組織に配置していない場合、システム管理者は <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations デモ環境の配置</a> を確認する必要があります。</td>
</tr>
<tr class="even">
<td>KB 4018050 を実装する必要があります。</td>
<td>システム管理者</td>
<td>KB 4018050 は、<strong>プロジェクト時間入力</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。 KB 4018050 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li>Microsoft Dynamics Lifecycle Services (LCS) から KB 4018050 をダウンロードします。</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>ApplicationSuite</strong> と <strong>ProjectMobile</strong> モデルを含む <a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li>Dynamics 365 for Operations システムに<a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用</a>します。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>プロジェクト時間入力</strong> モバイル ワークスペースを Dynamics 365 for Operations モバイル アプリに公開しておく必要があります。</td>
<td>システム管理者</td>
<td><ol>
<li>ブラウザーで、Dynamics 365 for Operations を開始します。</li>
<li><strong>システム パラメーター</strong> ページの、<strong>モバイル ワークスペースの管理</strong> タブで、<strong>プロジェクト時間入力</strong> ワークスペースを選択します。</li>
<li><strong>モバイル ワークスペースの公開</strong>をクリックします。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations モバイル アプリをダウンロードしてインストールする
モバイル アプリ ストアで、Microsoft Dynamics 365 for Operations アプリをダウンロードおよびインストールします。

-   Android 用: [Google Play ストアの Dynamics 365 for Operations](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone 用: [iTunes アプリ ストアの Dynamics 365 for Operations](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations モバイル アプリにサインインする
1.  モバイル デバイスでアプリを起動します。
2.  Dynamics 365 for Operations URL を入力します。
3.  サインインする会社を入力します。 たとえば、「**USMF**」と入力します。
4.  最初にサインインしたときに、Dynamics 365 for Operations アカウントのユーザー名とパスワードが要求されます。 資格情報を入力します。
5.  サインインすると、会社の使用できるワークスペースが表示されます。 システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新することができます。

[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>プロジェクト時間入力モバイル ワークスペースを使用して時間を入力します。
1.  モバイル デバイスで、**プロジェクト時間入力** ワークスペースを選択します。
2.  **時間入力** を選択します。 現在の週のカレンダーの日付が表示されます。
3.  選択された日付で、**アクション** &gt; **新しいエントリ** を選択します。
4.  記録する時間数を入力します。
5.  時間入力するプロジェクトを選択します。 オフラインで使用する場合のために、アプリにロードされたプロジェクトのリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [Dynamics 365 for Operations モバイル プラットフォーム](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) を確認する必要があります。
6.  プロジェクトがリストにない場合、**検索** を選択して、Dynamics 365 for Operations をオンライン サーチします。 名前で検索するか、プロジェクト名または顧客での検索に切り替えます。
7.  カテゴリを選択します。 オフラインで使用する場合のために、アプリにロードされたカテゴリのリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [Dynamics 365 for Operations モバイル プラットフォーム](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) を確認する必要があります。
8.  カテゴリがリストにない場合、**検索** を選択して、Dynamics 365 for Operations をオンライン サーチします。 カテゴリで検索するか、カテゴリ名での検索に切り替えます。
9.  活動を選択します。 オフラインで使用する場合のために、アプリにロードされた活動のリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [Dynamics 365 for Operations モバイル プラットフォーム](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) を確認する必要があります。
10. 活動がリストにない場合、**検索** を選択して、Dynamics 365 for Operations をオンライン サーチします。 活動番号で検索するか、目的別の検索に切り替えます。
11. 明細行プロパティを選択します。
12. オプション: 外部または内部コメントを入力します。
13. **完了** を選択します。






