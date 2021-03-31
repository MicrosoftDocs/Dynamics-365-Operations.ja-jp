---
title: 発注書の承認モバイル ワークスペース
description: このトピックでは、発注書を表示したり、アクションを通じて対応したりできる発注書の承認モバイル ワークスペースに関する情報を提供します。 たとえば、発注書を承認または拒否できます。
author: RichardLuan
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 37c0fc273091af260089229ad9ee66b52dce3831
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215988"
---
# <a name="purchase-order-approval-mobile-workspace"></a>発注書の承認モバイル ワークスペース

[!include [banner](../includes/banner.md)]

このトピックでは、**発注書の承認** モバイル ワークスペースに関する情報を提供します。 このワークスペースでは、発注書を表示したり、アクションを通じて対応したりできます。 たとえば、発注書を承認または拒否できます。
 
## <a name="overview"></a>概要 
承認が必要な発注書は、承認ワークフローを経由します。 ワークフローには、1 人以上の人員のアクションが必要なさまざま手順を含めることができます。 たとえば、ある人物がタスクの完了または発注書の承認を行う必要があるとします。 

**発注書の承認** モバイル ワークスペースで、モバイル デバイスから簡単に発注書の確認および対応ができます。 また、このワークスペースを使用して、Web クライアントからできるものと同じワークフロー アクションを実行することもできます。

## <a name="prerequisites"></a>必要条件
組織に配置されている Supply Chain Management のバージョンによって、前提条件は異なります。

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Management を使用する場合の前提条件 
Supply Chain Management を組織に配置している場合、システム管理者は **発注書承認** モバイル ワークスペースを公開する必要があります。 手順については、「[モバイル ワークスペースの公開](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム 更新プログラム 3 以降を使用する場合の前提条件
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
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Microsoft Dynamics Lifecycle Services (LCS)</a> からメタデータ修正プログラムをダウンロードします。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="../../dev-itpro/deployment/create-apply-deployable-package.md">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">配置可能パッケージを適用します</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td><strong>発注書の承認</strong>モバイル ワークスペースを公開します。</td>
<td>システム管理者</td>
<td>「<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>モバイル アプリのダウンロードとインストール
Finance and Operations モバイル アプリのダウンロードとインストール。

- [Android フォン用](https://go.microsoft.com/fwlink/?linkid=850662)
- [iPhone 用](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>モバイル アプリにログインします。

1. モバイル デバイスでアプリを起動します。
2. Microsoft Dynamics 365 URL を入力します。
3. 初めてサインインすると、ユーザー名とパスワードを要求されます。 資格情報を入力します。
4. サインインすると、使用可能な会社のワークスペースが表示されます。 なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。

![使用可能なワークスペースの一覧の発注書の承認ワークスペース](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>自分に割り当てられている注文の表示
1. モバイル デバイスで、**発注書の承認** ワークスペースを選択します。
2. **自分に割り当てられた注文** を選択して、発注書の承認ワークフローでアクションを求められたすべての発注書を表示します。
3. 注文を選択します。 **注文の詳細** ページで、注文のヘッダー情報と明細行が表示されます。 ワークフロー タスクからガイドラインについて検索することもできます。
4. **勘定配布** を選択して、**ヘッダーの勘定配布** ページを開きます。
5. **注文の詳細** ページに戻り、明細行を選択します。 注文明細行の詳細から、明細行固有の勘定配布を検索することもできます。

## <a name="complete-an-action-on-the-purchase-order"></a>発注書の操作を完了します。
自分に割り当てられている発注書を表示し、ワークフローの指示を読んでから、アクションを実行することをお勧めします。

1. モバイル デバイスで、**発注書の承認** ワークスペースを選択します。
2. **自分に割り当てられた注文** を選択して、発注書の承認ワークフローでアクションを求められたすべての発注書を表示します。
3. 注文を選択し、詳細ページを表示します。
4. **アクション** を選択して、使用可能なアクションを表示します。 使用可能なアクションは、自分に割り当てられたタスクに依存します。

    | タスクのアクション    | 承認アクション  |
    |----------------|------------------|
    | 完了       | 承認          |
    | 却下         | 否認           |
    | 変更依頼 | 変更依頼   |
    | 委任       | 委任         |

5. 該当するアクションを選択します。
6. **タスクの完了** ページで、コメントを入力します。 **委任** アクションを選択した場合、タスクを委任するユーザーを選択する必要があります。
7. **完了** を選択します。 ワークスペースを更新すると、発注書がリストに表示されなくなります。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]