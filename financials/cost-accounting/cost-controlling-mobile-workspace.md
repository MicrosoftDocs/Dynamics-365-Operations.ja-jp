---
title: "コスト管理モバイル ワークスペース"
description: "このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリに使用可能な、原価管理モバイル ワークスペースについて説明します。 このワークスペースにより、コスト センターの管理者は時間や場所に関わらず、コスト センターのパフォーマンスに関する情報を表示できます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>コスト管理モバイル ワークスペース

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリに使用可能な、原価管理モバイル ワークスペースについて説明します。 このワークスペースにより、コスト センターの管理者は時間や場所に関わらず、コスト センターのパフォーマンスに関する情報を表示できます。 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>原価管理モバイル ワークスペースの概要
-------------------------------------------------

**原価管理** モバイル ワークスペースは、予算原価に対する実際原価を比較して、原価部門の現在のパフォーマンスのインスタント ビューを提供します。 個々の原価要素のステータスにドリル ダウンすることができます。 たとえば、従業員は国際会議への招待を受けますが、組織はすべての旅費を負担する必要があります。 その従業員は、会議に出席できるかどうか管理者に尋ねます。 管理者は、すぐに携帯電話で **原価管理** モバイル ワークスペースを開き、会議に出席する予算があるかどうかを確認します。

### <a name="data-security"></a>データ セキュリティ

**原価管理** モバイル ワークスペースのデータは、ユーザー資格情報で保護されます。 原価部門管理者は、自身の原価部門のデータだけを表示することができます。 アクセス レベルのセキュリティは、**原価会計** モジュール内で管理されます。 原価経理担当は、**原価会計** モジュールで **原価管理** モバイル ワークスペースのコンフィギュレーションを定義します。 ワークスペースを Microsoft Dynamics 365 for Operations モバイル アプリに公開すると、このアプリで使用できるようになります。 これで組織内のすべての原価部門管理者が同じ形式でデータを表示できるようになります。

### <a name="actions-views-and-links"></a>操作、ビュー、リンク

Dynamics 365 for Operations アプリ用の **原価管理** モバイル ワークスペースでは、次の操作、ビュー、リンクを使用できます。

-   **アクション:**
    -   レイアウトを選択するには、**構成の選択** を使用します。
    -   データをフィルター処理する原価部門を選択するには、**原価オブジェクトの選択** を使用します。 **注:** 一覧に表示される原価部門は、**原価会計** モジュールで許可されるアクセスによって異なります。
-   **ビュー:** 選択されたアクションと **原価計算** モジュールの設定に基づいて、カードに関する以下の情報を表示することができます。
    -   実際対予算 (現在の期間)
    -   実際対修正予算 (現在の期間)
    -   実際対予算 (前の期間)
    -   実際対修正予算 (前の期間)
    -   実際対予算 (年度累計)
    -   実際対修正予算 (年度累計)

    すべてのカードに表示される金額は、実績、予算、差異、差異の割合 (％) です。
-   **リンク:**
    -   現在の期間の詳細
    -   前の期間の詳細
    -   年度累計の詳細

    リンクを選択すると、カードが原価要素ごとに表示されます。 すべてのカードに表示される金額は、実績、予算、予算差異、予算差異 %、修正予算、修正予算差異、修正予算差異 % です。 
    
    [![原価要素のカード](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>前提条件
**原価管理** モバイル ワークスペースを使用する前に、システム管理者が次の前提条件を満たしていることを確認してください。

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
<td>Dynamics 365 for Operations をまだ組織に配置していない場合、システム管理者は <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operations デモ環境の配置</a> を確認する必要があります。</td>
</tr>
<tr class="even">
<td>KB 4013633 を実装する必要があります。</td>
<td>システム管理者</td>
<td>KB 4013633 (X++ アップデートまたはメタデータ修正プログラム) には、サプライチェーン管理用の 4 つのモバイルワーク スペースが含まれています。 KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li>Microsoft Dynamics Lifecycle Services (LCS) から KB 4013633 をダウンロードします。</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li>Dynamics 365 for Operations システムに<a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">配置可能パッケージを適用</a>します。</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>原価管理</strong>モバイル ワークスペースを Dynamics 365 for Operations モバイル アプリに公開しておく必要があります。</td>
<td>システム管理者</td>
<td><ol>
<li>ブラウザーで、Dynamics 365 for Operations を開始します。</li>
<li><strong>システム パラメーター</strong>ページで、<strong>モバイル ワークスペースの管理</strong>を選択します。</li>
<li><strong>原価オブジェクトの概要</strong>ワークスペースを選択します。</li>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>原価管理モバイル ワークスペースを使用して、原価部門のパフォーマンスを表示します。
1.  モバイル デバイスで、[**原価管理**] ワークスペースを選択します。
2.  [**原価オブジェクト管理**] を選択します。
3.  **操作** を選択します。
4.  **コンフィギュレーションの選択** を選択して、原価管理レイアウトを選択します。
5.  **完了** を選択します。
6.  **操作** を選択します。
7.  [**原価オブジェクトの選択**] を選択して、アクセスが許可された原価部門を選択します。
8.  **完了** を選択します。
9.  原価部門の全体パフォーマンスを表示します。
10. **現在の期間の詳細を** リンクを選択します。
11. 個々の原価要素のパフォーマンスを表示します。
12. 特定の原価要素も検索できます。





