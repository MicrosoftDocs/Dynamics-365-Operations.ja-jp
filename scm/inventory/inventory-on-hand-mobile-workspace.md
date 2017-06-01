---
title: "手持ち在庫モバイル ワークスペース"
description: "このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリに使用可能な手持ち在庫モバイル ワークスペースについて説明します。 このワークスペースは、予約済みの在庫や利用可能な在庫に関する情報を、いつでも、どこでも取得するのに役立ちます。"
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
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>手持ち在庫モバイル ワークスペース

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリに使用可能な手持ち在庫モバイル ワークスペースについて説明します。 このワークスペースは、予約済みの在庫や利用可能な在庫に関する情報を、いつでも、どこでも取得するのに役立ちます。

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>手持ち在庫モバイル ワークスペースの概要
--------------------------------------------------

通常、企業は毎日複数の出荷と在庫の複数の領収書を持っています。 これらの動きは、常に手持ちの在庫ステータスを変更します。 **手持ち在庫** モバイル ワークスペースにより、社内の手持ちの在庫状態を把握し、選択したモバイル デバイス上で在庫データに関する最新の情報を取得できます。 倉庫、購買、営業、製造または管理のいずれで作業していようがそれ以外の役割を担っていようが関係なく、いつでもどこでも手持ちの在庫データにアクセスすることができます。 

モバイル ワークスペースは、複数の設備の手持ち状態のインスタント ビューを提供します。 複数の設備での手持ち在庫、現在の原料の予約、および予約されていない手持ち在庫を表示できます。 また、品目番号を入力して手持ち在庫を照会したり、手持ち製品やバリアントのフィルター検索を行うこともできます。 

具体的には、モバイル ワークスペースは次の機能を提供します。

-   製品番号または製品名で検索し、手持ちの在庫状況を表示して、製品を見つけることができます。

-   選択された製品に対して、次の情報を表示できます。
    -   サイトごとの手持ち在庫
    -   倉庫ごとの手持ち在庫
    -   場所ごとの手持ち在庫
    -   バッチごとの手持ち在庫 (バッチ管理されている製品の場合)
    -   在庫状態ごとの手持ち在庫
    
-   製品の手持ち在庫は、次の方法で表示されます:
    -   現物在庫による (このビューは、合計金額を表します)。
    -   現物引当済による (このビューは、引当済金額を表します)。
    -   引当可能現物数による (このビューは予約がない使用可能な残りの金額を表します)。

## <a name="prerequisites"></a>前提条件
**手持ち在庫** モバイル ワークスペースを使用するには、システム管理者が次の前提条件を満たしていることを確認してください。

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
<td><strong>手持ち在庫</strong> モバイル ワークスペースを Dynamics 365 for Operations モバイル アプリに公開しておく必要があります。</td>
<td>システム管理者</td>
<td><ol>
<li>ブラウザーで、Dynamics 365 for Operations を開始します。</li>
<li><strong>システム パラメーター</strong>ページで、<strong>モバイル ワークスペースの管理</strong>を選択します。</li>
<li><strong>手持ち在庫</strong> ワークスペースを選択します。</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>手持ち在庫モバイル ワークスペースを使用して、製品の手持ち在庫を表示します。
1.  モバイル デバイスで、[**手持ち在庫**] ワークスペースを選択します。
2.  [**品目の手持ち在庫の確認**] を選択します。 オフラインで使用する場合のために、アプリにロードされた製品のリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [Dynamics 365 for Operations モバイル プラットフォーム](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) を確認する必要があります。
3.  品目がリストにない場合、[**検索を続ける**] を選択して、Dynamics 365 for Operations をオンライン サーチします。 製品番号で検索するか、または製品名での検索に切り替えます。
4.  製品を選択します。 品目に画像が含まれる場合、画像が表示されます。
5.  手持ち在庫の状態を表示するために次のオプションの 1 つを選択します。
    -   サイトごとに手持ち在庫を表示する
    -   倉庫ごとに手持ち在庫を表示する
    -   場所ごとに手持ち在庫を表示する
    -   バッチ (バッチで制御された製品に対して) ごとに手持ち在庫を表示する
    -   在庫の状態ごとに手持ち在庫を表示する

    製品の手持ち在庫は、次の方法で表示されます:
    -   現物在庫による (このビューは、合計金額を表します)。
    -   現物引当済による (このビューは、引当済金額を表します)。
    -   物理的に利用可能ごと (この表示は予約なしの利用可能な金額を表します。)






