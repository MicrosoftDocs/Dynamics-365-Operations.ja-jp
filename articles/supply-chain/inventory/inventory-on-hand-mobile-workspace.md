---
title: 手持ち在庫モバイル ワークスペース
description: このトピックでは、手持在庫モバイル ワークスペースに関する情報を提供します。 このワークスペースは、予約済みの在庫や利用可能な在庫に関する情報を、いつでも、どこでも取得するのに役立ちます。
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 7d0440514369f8271004993d009ef7c3a36edb53
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008062"
---
# <a name="inventory-on-hand-mobile-workspace"></a>手持ち在庫モバイル ワークスペース

[!include [banner](../includes/banner.md)]

このトピックでは、**手持ち在庫** モバイル ワークスペースに関する情報を提供します。 このワークスペースは、予約済みの在庫や利用可能な在庫に関するモバイル情報を、いつでも、どこでも取得するのに役立ちます。

このモバイル ワークスペースは、Finance and Operations モバイル アプリで使用するためのものです。

## <a name="overview"></a>概要
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

## <a name="prerequisites"></a>必要条件
組織に配置されている Supply Chain Management のバージョンによって、前提条件は異なります。

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Supply Chain Management を使用する場合の前提条件
Supply Chain Management が組織に配置されている場合、システム管理者は **手持在庫** モバイル ワークスペースを公開する必要があります。 手順については、「[モバイル ワークスペースの公開](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>プラットフォーム 更新プログラム 3 以降を使用する場合の前提条件 
プラットフォーム更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。 

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

<td>KB 4013633 は、<strong>手持ち在庫</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。 KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Microsoft Dynamics Lifecycle Services (LCS)</a> からメタデータ修正プログラムをダウンロードします。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="../../dev-itpro/deployment/create-apply-deployable-package.md">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">配置可能パッケージを適用します</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>手持在庫</strong> モバイル ワークスペースを公開します。</td>
<td>システム管理者</td>
<td>「<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">モバイル ワークスペースの公開</a>」を参照してください。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>モバイル アプリのダウンロードとインストール

Finance and Operations モバイル アプリのダウンロードとインストール。

-   [Android フォン用](https://go.microsoft.com/fwlink/?linkid=850662)
-   [iPhone 用](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>モバイル アプリにログインします。

1.  モバイル デバイスでアプリを起動します。
2.  Dynamics 365 の URL を入力します。
3.  初めてサインインすると、ユーザー名とパスワードを要求されます。 資格情報を入力します。
4.  サインインすると、使用可能な会社のワークスペースが表示されます。 なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。

    [![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>手持ち在庫モバイル ワークスペースを使用して、製品の手持ち在庫を表示します。

1.  モバイル デバイスで、**手持ち在庫** ワークスペースを選択します。

2.  **品目の手持ち在庫の確認** を選択します。 オフラインで使用する場合のために、アプリにロードされた製品のリストが表示されます。 既定では、50 の品目がロードされますが、開発者はこの数値を変更できます。 詳細については、開発者は [モバイル プラットフォーム](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md) を確認する必要があります。
3.  品目が一覧にない場合は、**検索を続ける** を選択します。 製品番号で検索するか、または製品名での検索に切り替えます。

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]