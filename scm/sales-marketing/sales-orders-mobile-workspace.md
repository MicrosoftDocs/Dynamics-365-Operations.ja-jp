---
title: "販売注文モバイル ワークスペース"
description: "このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリに使用可能な、販売注文モバイル ワークスペースについて説明します。 このワークスペースは、どこでも、いつでも販売注文を最新の状態に保つのに役立ちます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>販売注文モバイル ワークスペース

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリに使用可能な、販売注文モバイル ワークスペースについて説明します。 このワークスペースは、どこでも、いつでも販売注文を最新の状態に保つのに役立ちます。 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>販売注文モバイル ワークスペースの概要
---------------------------------------------

**販売注文** モバイル ワークスペースは、Microsoft Dynamics 365 for Operations にアクセスして、各販売注文に関する詳細情報を表示することができます。 この情報には、注文のステータス、顧客の連絡先情報および注文受付者の連絡先情報が含まれます。 **販売注文** モバイル ワークスペースは、販売注文のインスタント ビューを提供します。 すべての販売注文、顧客別の販売注文、または特定の販売注文に関する情報を表示できます。 

モバイル ワークスペースは、より詳しい販売注文の分析に役立つ 2 つのビューを提供します。

### <a name="view-all-sales-orders"></a>すべての販売注文の表示

このビューは、すべての販売注文を一覧表示します。

-   表示する販売注文を選択するため、次のフィルターのいずれかを使用します。
    -   販売注文で検索
    -   顧客 ID で検索
    -   顧客名で検索
    -   ステータスで検索
    -   リリース状態で検索
    -   作成日時で検索
    
-   販売注文を選択したのち、特定の注文の詳細を表示できます。 具体的には、次の情報を表示できます。
    -   顧客の名前と住所情報
    -   指定出荷日や確定出荷日などの、販売注文に関するさまざまな日付
    -   注文受付者の連絡先情報
    -   顧客の連絡先情報
    -   注文明細行
    -   販売注文がいつどのように出荷されたかを示す出荷

### <a name="view-orders-for-a-customer"></a>顧客の注文の表示

顧客ごとの販売注文の一覧を表示します。

-   顧客の注文を表示するため、次のフィルターのいずれかを使用します。
    -   名前で検索
    -   ID で検索

-   顧客を選択したのち、次の情報を表示することができます。
    -   顧客名およびグループ
    -   顧客の連絡先情報
    -   顧客の販売注文およびそれらの販売注文に関する詳細。
        -   顧客の名前と住所情報
        -   さまざまな販売注文日
        -   注文受付者の連絡先情報
        -   顧客の連絡先情報
        -   注文明細行
        -   販売注文がいつどのように出荷されたかを示す出荷

## <a name="prerequisites"></a>前提条件
**販売注文** モバイル ワークスペースを使用する前に、システム管理者が次の前提条件を満たしていることを確認してください。

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
<td>Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を実装する必要があります。</td>
<td>システム管理者</td>
<td>Dynamics 365 for Operations をまだ組織に配置していない場合、システム管理者は <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Microsoft Dynamics 365 for Operations デモ環境の配置</a> を確認する必要があります。</td>
</tr>
<tr class="even">
<td>KB 4013633 を実装する必要があります。</td>
<td>システム管理者</td>
<td>KB 4013633 (X++ アップデートまたはメタデータ修正プログラム) には、サプライチェーン管理用の 4 つのモバイルワーク スペースが含まれています。 KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li>Microsoft Dynamics Lifecycle Services (LCS) から KB 4013633 をダウンロードします。</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li>Dynamics 365 for Operations システムに<a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用</a>します。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>販売注文</strong> モバイル ワークスペースを Dynamics 365 for Operations モバイル アプリに公開しておく必要があります。</td>
<td>システム管理者</td>
<td><ol>
<li>ブラウザーで、Dynamics 365 for Operations を開始します。</li>
<li><strong>システム パラメーター</strong>ページで、<strong>モバイル ワークスペースの管理</strong>を選択します。</li>
<li><strong>販売注文</strong> ワークスペースを選択します。</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>モバイル ワークスペースを使用して顧客の販売注文に関する情報を表示
1.  モバイル デバイスで、**販売注文** ワークスペースを選択します。
2.  **顧客の注文の表示**を選択します。
3.  顧客を見つけるため、アカウントまたは顧客名情報を使用します。
4.  顧客を選択します。
5.  **連絡先情報** または **販売注文**を選択します。 **販売注文** を選択すると、顧客の販売注文の一覧が表示されます。
6.  **販売注文**を選択します。 販売注文明細行、出荷に関する情報、顧客の連絡先情報、および注文受付者の連絡先情報を表示できるようになりました。





