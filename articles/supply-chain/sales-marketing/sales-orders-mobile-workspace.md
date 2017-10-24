---
title: "販売注文モバイル ワークスペース"
description: "このトピックでは、販売注文モバイル ワークスペースについての情報を提供します。 このワークスペースは、どこでも、いつでも販売注文について最新の状態に保つのに役立ちます。"
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: abc117ad935b27cdfb15e43e4c12c9d0a65f176e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="sales-orders-mobile-workspace"></a>販売注文モバイル ワークスペース

[!include[banner](../includes/banner.md)]

このトピックでは、**販売注文**モバイル ワークスペースについての情報を提供します。 このワークスペースは、どこでも、いつでも販売注文について最新の状態に保つのに役立ちます。 

このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリで使用するためのものです。

## <a name="overview"></a>概要
**販売注文**モバイル ワークスペースを使用して、各販売注文に関する詳細情報を表示できます。 この情報には、注文のステータス、顧客の連絡先情報および注文受付者の連絡先情報が含まれます。 **販売注文** モバイル ワークスペースは、販売注文のインスタント ビューを提供します。 すべての販売注文、顧客別の販売注文、または特定の販売注文に関する情報を表示できます。 

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
組織に配置されている Microsoft Dynamics 365 のバージョンに基づいて、前提条件は異なります。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 7 月) を使用している場合の前提条件 
Dynamics 365 for Finance and Operations, Enterprise edition (2017 年 ７ 月) を組織に配置している場合、システム管理者は [**販売注文**] モバイル ワークスペースを公開する必要があります。 手順については、「[モバイル ワークスペースの公開](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用している場合の前提条件
Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。 

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
<td>KB 4013633 を実装します。</td>
<td>システム管理者</td>

<td>KB 4013633 は、<strong>販売注文</strong>モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。 KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="../../dev-itpro/deployment/create-apply-deployable-package.md">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">配置可能パッケージを適用します</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>販売注文</strong>モバイル ワークスペースを公開します。</td>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>販売注文モバイル ワークスペースを使用して顧客の販売注文に関する情報を表示

1.  モバイル デバイスで、**販売注文** ワークスペースを選択します。
2.  **顧客の注文の表示**を選択します。
3.  顧客を見つけるため、アカウントまたは顧客名情報を使用します。
4.  顧客を選択します。
5.  **連絡先情報** または **販売注文**を選択します。 **販売注文** を選択すると、顧客の販売注文の一覧が表示されます。
6.  **販売注文**を選択します。 販売注文明細行、出荷に関する情報、顧客の連絡先情報、および注文受付者の連絡先情報を表示できるようになりました。

