---
title: "発注書の承認モバイル ワークスペース"
description: "このトピックでは、発注書を表示したり、アクションを通じて対応したりできる発注書の承認モバイル ワークスペースに関する情報を提供します。 たとえば、発注書を承認または拒否できます。"
author: mkirknel
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: a2ab719b971c325be184d1d950f6c03815e4cea2
ms.contentlocale: ja-jp
ms.lasthandoff: 06/20/2017

---

# <a name="purchase-order-approval-mobile-workspace"></a>発注書の承認モバイル ワークスペース

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

このトピックでは、**発注書の承認**モバイル ワークスペースに関する情報を提供します。 このワークスペースでは、発注書を表示したり、アクションを通じて対応したりできます。 たとえば、発注書を承認または拒否できます。
 
## <a name="overview"></a>概要 
承認が必要な発注書は、承認ワークフローを経由します。 ワークフローには、1 人以上の人員のアクションが必要なさまざま手順を含めることができます。 たとえば、ある人物がタスクの完了または発注書の承認を行う必要があるとします。 

**発注書の承認**モバイル ワークスペースで、モバイル デバイスから簡単に発注書の確認および対応ができます。 また、このワークスペースを使用して、Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition の Web クライアントからできるものと同じワークフロー アクションを実行することもできます。

## <a name="prerequisites"></a>前提条件
組織に配置されている Finance and Operations のバージョンによって、前提条件は異なります。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 2017 年 7 月の更新プログラムを使用している場合の前提条件 
Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 2017 年 ７ 月の更新プログラムを組織に配置している場合、システム管理者は **発注書の承認** モバイル ワークスペースを公開する必要があります。 手順については、「[モバイル ワークスペースの公開](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace)」を参照してください。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用している場合の前提条件
Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。 

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
<td>KB 4017918 を実装します。</td>
<td>システム管理者</td>
<td>KB 4017918 は、<strong>発注書の承認</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。 KB 4017918 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用します</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td><strong>発注書の承認</strong>モバイル ワークスペースを公開します。</td>
<td>システム管理者</td>
<td>「<a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの公開</a>」を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>モバイル アプリのダウンロードとインストール
Microsoft Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。

- [Android フォン用](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone 用](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>モバイル アプリにログインします。

1. モバイル デバイスでアプリを起動します。
2. Microsoft Dynamics 365 の URL を入力します。
3. 初めてサインインすると、ユーザー名とパスワードを要求されます。 資格情報を入力します。
4. サインインすると、使用可能な会社のワークスペースが表示されます。 なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。

![使用可能なワークスペースの一覧の発注書の承認ワークスペース](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>自分に割り当てられている注文の表示
1. モバイル デバイスで、**発注書の承認**ワークスペースを選択します。
2. [**自分に割り当てられた注文**] を選択して、発注書の承認ワークフローでアクションを求められたすべての発注書を表示します。
3. 注文を選択します。 **注文の詳細**ページで、注文のヘッダー情報と明細行が表示されます。 ワークフロー タスクからガイドラインについて検索することもできます。
4. [**勘定配布**] を選択して、**ヘッダーの勘定配布**ページを開きます。
5. **注文の詳細**ページに戻り、明細行を選択します。 注文明細行の詳細から、明細行固有の勘定配布を検索することもできます。

## <a name="complete-an-action-on-the-purchase-order"></a>発注書の操作を完了します。
自分に割り当てられている発注書を表示し、ワークフローの指示を読んでから、アクションを実行することをお勧めします。

1. モバイル デバイスで、**発注書の承認**ワークスペースを選択します。
2. [**自分に割り当てられた注文**] を選択して、発注書の承認ワークフローでアクションを求められたすべての発注書を表示します。
3. 注文を選択し、詳細ページを表示します。
4. [**アクション**] を選択して、使用可能なアクションを表示します。 使用可能なアクションは、自分に割り当てられたタスクに依存します。

    | タスクのアクション    | 承認アクション  |
    |----------------|------------------|
    | 完了       | 承認          |
    | 却下         | 否認           |
    | 変更依頼 | 変更依頼   |
    | 委任       | 委任         |

5. 該当するアクションを選択します。
6. **タスクの完了**ページで、コメントを入力します。 **委任**アクションを選択した場合、タスクを委任するユーザーを選択する必要があります。
7. **完了** を選択します。 ワークスペースを更新すると、発注書がリストに表示されなくなります。 

