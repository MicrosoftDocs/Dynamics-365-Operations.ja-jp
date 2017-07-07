---
title: "経費管理モバイル ワークスペース"
description: "このトピックでは、Microsoft Dynamics 365 for Finance および Operations モバイル アプリに使用可能な経費管理モバイル ワークスペースについて説明します。 このワークスペースにより、ユーザーは領収書を取得し、アップロードできるため、経費精算書に後から添付することができます。 また、モバイル ワークスペース ユーザーにより、添付したを使用して経費明細行を迅速に作成することもできます。"
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 0e52d1c5dde7f79c4a8ac5ac2d9c3b25bba9c2cd
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017


---

# <a name="expense-management-mobile-workspace"></a>経費管理モバイル ワークスペース

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Finance および Operations モバイル アプリに使用可能な経費管理モバイル ワークスペースについて説明します。 このワークスペースにより、ユーザーは領収書を取得し、アップロードできるため、経費精算書に後から添付することができます。 また、モバイル ワークスペース ユーザーにより、添付したを使用して経費明細行を迅速に作成することもできます。

<a name="overview-of-the-expense-management-mobile-workspace"></a>経費管理モバイル ワークスペースの概要
---------------------------------------------------

多くの組織は、従業員が払い戻しのために提出する出張関連または事業関連の経費報告書に領収書のコピーを添付することを要求しています。 **経費管理** モバイル ワークスペースにより、領収書のコピーを添付して、任意のモバイル デバイスで新しい経費の明細行をすばやく作成できます。 また、ユーザーは、領収書の写真を撮り、その後で経費精算書に添付することもできます。 具体的には、**経費管理** モバイル ワークスペースによって、ユーザーは次が実行できるようになります。

-   領収書の写真を撮り、Microsoft Dynamics 365 for Finance および Operations にアップロードします。 その後にユーザーはその写真を経費精算書に添付できます。
-   キャプチャした領収書としてファイルをアップロードします。 その後にユーザーはそのファイルを経費精算書に添付できます。
-   新しい経費明細行を作成するには、添付されている領収書を使用します。 ユーザーはその後に、経費精算書に明細行品目を追加し、承認と払い戻しのために送信します。

このトピックの残りのセクションでは **経費管理** モバイル ワークスペースの実装および使用方法について説明します。

## <a name="prerequisites"></a>前提条件
**経費管理** モバイル ワークスペースを実装する前に、システム管理者が次の前提条件を満たしていることを確認してください。

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
<td>Finance および Operations をまだ組織に配置していない場合、システム管理者は <a href="/dynamics365/unified-operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Finance および Operations デモ環境の配置</a> を確認する必要があります。</td>
</tr>
<tr class="even">
<td>KB 4019015 を実装する必要があります。</td>
<td>システム管理者</td>
<td>KB 4019015 (X++ アップデートまたはメタデータ修正プログラム) には、サプライチェーン管理用の 4 つのモバイルワーク スペースが含まれています。 KB 4019015 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li>Microsoft Dynamics Lifecycle Services (LCS) から KB 4019015 をダウンロードします。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>アプリケーション スイート</strong> と <strong>ExpenseMobile</strong> モデルを含む <a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li>Finance および Operations システムに<a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用</a>します。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>経費管理</strong> モバイル ワークスペースを Finance および Operations モバイル アプリに公開しておく必要があります。</td>
<td>システム管理者</td>
<td><ol>
<li>Finance および Operations をブラウザで起動します。</li>
<li><strong>システム パラメーター</strong>ページで、<strong>モバイル ワークスペースの管理</strong>を選択します。</li>
<li><strong>経費管理</strong> ワークスペースを選択します。</li>
<li><strong>モバイル ワークスペースの公開</strong>をクリックします。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-finance-and-operations-mobile-app"></a>Finance および Operations モバイル アプリをダウンロードしてインストールします。
モバイル アプリ ストアで、Finance および Operations アプリをダウンロードおよびインストールします。

-   Android 用: [Google Play ストアの Finance および Operations](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   iPhone 用: [iTunes アプリ ストアの Finance および Operations](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-finance-and-operations-mobile-app"></a>Finance および Operations モバイルアプリへのログインをします。
1.  モバイル デバイスでアプリを起動します。
2.  Finance および Operations の URL を入力します。
3.  サインインする会社を入力します。 たとえば、「**USMF**」と入力します。
4.  最初にサインインしたときに、Finance および Operations アカウントのユーザー名とパスワードが要求されます。 資格情報を入力します。
5.  サインインすると、会社の使用できるワークスペースが表示されます。 システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新することができます。 

[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>経費管理のモバイル ワークスペースを使用して、領収書を取得します。
1.  モバイル デバイスで、**経費管理** ワークスペースを選択します。
2.  **領収書の取得** を選択します。
3.  **写真を撮る** または **画像の選択** を選択します。
4.  **写真を撮る** を選択した場合は、次の手順に従います。
    1.  モバイル デバイスのカメラが用意され、領収書の写真を撮ることができるようになります。 写真が撮り終わったら、**OK** をクリックして写真を確定します。
    2.  オプション: 写真の名前とメモを入力します。

     **または**、**画像の選択** を選択した場合は、次の手順に従います。
    1.  リストで画像を選択します。
    2.  オプション: 画像の名前とメモを入力します。

5.  **完了** を選択します。

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>経費管理のモバイル ワークスペースを使用して、経費を簡単に入力できます。
1.  モバイル デバイスで、**経費管理** ワークスペースを選択します。
2.  **経費簡単入力** を選択します。
3.  経費のカテゴリを選択します。 オフラインで使用する場合のために、アプリにロードされた経費カテゴリのリストが表示されます。 既定では、最大 50 品目がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [Finance および Operations モバイル プラットフォーム](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform) を確認する必要があります。 カテゴリがリストにない場合、**検索** を選択して、Finance および Operations をオンライン サーチします。 経費カテゴリで検索するか、経費タイプでの検索に切り替えます。
4.  経費のトランザクションの日付を入力します。
5.  オプション: 経費の商社を入力します。
6.  経費金額を入力します。
7.  経費の通貨を選択します。 オフラインで使用する場合のために、アプリにロードされた通貨コードが一覧表示されます。 既定では、最大 400 種類の通貨がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [Finance および Operations モバイル プラットフォーム](/dynamics365/unified-operations/dev-itpro/mobile-apps/mobile-platform) を確認する必要があります。 お使いの通貨がリストにない場合、**検索** を選択して、Finance および Operations をオンライン サーチします。 通貨で検索するか、名前での検索に切り替えます。
8.  **写真を撮る** または **画像の選択** を選択します。
9.  **写真を撮る** を選択した場合は、モバイル デバイスのカメラが用意され、領収書の写真を撮ることができます。 写真が撮り終わったら、**OK** をクリックして写真を確定します。  または、**画像の選択** を選択した場合は、一覧から画像を選択します。
10. **完了** を選択します。






