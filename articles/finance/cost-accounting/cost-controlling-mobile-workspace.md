---
title: コスト管理モバイル ワークスペース
description: このトピックでは、原価管理モバイル ワークスペースについての情報を提供します。 このワークスペースにより、コスト センターの管理者は時間や場所に関わらず、コスト センターのパフォーマンスに関する情報を表示できます。
author: AndersGirke
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cd86fdf640e59885e5e8aea841dc1c1c9604825b0f18d3b741c5a2777f8e9ff8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728796"
---
# <a name="cost-controlling-mobile-workspace"></a>コスト管理モバイル ワークスペース

[!include [banner](../includes/banner.md)]

このトピックでは、**原価管理** モバイル ワークスペースについての情報を提供します。 このワークスペースにより、コスト センターの管理者は時間や場所に関わらず、コスト センターのパフォーマンスに関する情報を表示できます。

このモバイル ワークスペースは、Finance and Operations モバイル アプリで使用するためのものです。

## <a name="overview"></a>概要
**原価管理** モバイル ワークスペースは、予算原価に対する実際原価を比較して、原価部門の現在のパフォーマンスのインスタント ビューを提供します。 個々のコスト要素のステータスにドリル ダウンすることができます。

たとえば、従業員は国際会議への招待を受けますが、組織はすべての旅費を負担する必要があります。 従業員は、会議に出席できるかどうか管理者に尋ねます。 管理者は、モバイル端末で **コスト管理** モバイル ワークスペースを開き、従業員が会議に参加する予算があるかどうかを確認します。

### <a name="data-security"></a>データ セキュリティ
**原価管理** モバイル ワークスペースのデータは、ユーザー資格情報で保護されます。 原価部門管理者は、自身の原価部門のデータだけを表示することができます。 アクセス レベルのセキュリティは、**原価会計** モジュール内で管理されます。

原価経理担当は、**原価会計** モジュールで **原価管理** モバイル ワークスペースのコンフィギュレーションを定義します。 ワークスペースをモバイル アプリに公開すると、このアプリで使用できるようになります。 これで組織内のすべての原価部門管理者が同じ形式でデータを表示できるようになります。

### <a name="actions-views-and-links"></a>操作、ビュー、リンク
**原価管理** モバイル ワークスペースでは、次のアクション、ビュー、およびリンクが提供されます。

-   **アクション:**

    -   レイアウトを選択するには、**構成の選択** を使用します。
    -   データをフィルター処理する原価部門を選択するには、**原価オブジェクトの選択** を使用します。
    
        > [!NOTE]
        > 一覧に表示されるコスト センターは、**原価会計** モジュールで許可されるアクセスによって異なります。

-   **ビュー:** 選択されたアクションと **原価会計** モジュールの設定に基づいて、カードに関する以下の情報を表示することができます。

    -   実績対予算 (現在の期間)
    -   実績対修正予算 (現在の期間)
    -   実際対予算 (前の期間)
    -   実際対修正予算 (前の期間)
    -   実際対予算 (年度累計)
    -   実際対修正予算 (年度累計)

    すべてのカードに表示される金額は、実績、予算、差異、差異の割合 (%) です。

-   **リンク:**

    -   現在の期間の詳細
    -   前の期間の詳細
    -   年度累計の詳細

    リンクを選択すると、カードが原価要素ごとに表示されます。 すべてのカードに表示される金額は、実績、予算、予算差異、予算差異 (%)、修正予算、修正予算差異、修正予算差異 (%) です。
    
    [![原価要素のカード。](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>必要条件
組織に配置されている Microsoft Dynamics 365 のバージョンに基づいて、前提条件は異なります。

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Microsoft Dynamics 365 Finance を使用する場合の前提条件
Finance を組織に配置している場合、システム管理者は **原価管理** モバイル ワークスペースを公開する必要があります。 手順については、「[モバイル ワークスペースの公開](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md)」を参照してください。

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用する場合の前提条件
バージョン 1611 およびプラットフォーム更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。

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

<td>KB 4013633 は、<strong>原価管理</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。 KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services (LCS)</a> からメタデータ修正プログラムをダウンロードします。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></li>
<li><strong>SCMMobile</strong> モデルを含む<a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用します</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>原価管理</strong> モバイル ワークスペースを公開します。</td>
<td>システム管理者</td>
<td>「<a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの公開</a>」を参照してください。</td>
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

[![プルして更新。](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>原価管理モバイル ワークスペースを使用して、原価部門のパフォーマンスを表示します。

1.  モバイル デバイスで、**原価管理** ワークスペースを選択します。
2.  **原価オブジェクト管理** を選択します。
3.  **操作** を選択します。
4.  **コンフィギュレーションの選択** を選択して、原価管理レイアウトを選択します。
5.  **完了** を選択します。
6.  **操作** を選択します。
7.  **原価オブジェクトの選択** を選択して、アクセスが許可された原価部門を選択します。
8.  **完了** を選択します。
9.  原価部門の全体パフォーマンスを表示します。
10. **現在の期間の詳細を** リンクを選択します。
11. 個々の原価要素のパフォーマンスを表示します。
12. 特定の原価要素も検索できます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]