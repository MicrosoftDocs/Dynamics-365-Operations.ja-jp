---
title: "Dynamics 365 for Operations モバイル アプリのホームページ"
description: "このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。"
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Dynamics 365 for Operations モバイル アプリのホームページ

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Dynamics 365 for Operations モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。

<a name="overview"></a>概要
--------

Microsoft Dynamics 365 for Operations モバイル アプリにより、組織は業務プロセスをモバイル デバイスで使用できるようになります。 IT 管理者が組織用のモバイル ワークスペース機能を有効にすると、ユーザーはアプリにログインしてすぐにモバイル デバイスから業務プロセスの実行を開始できます。 Dynamics 365 for Operations モバイル アプリには、生産性を高めるのに役立つ次の機能が含まれています。

-   ネットワーク接続が断続的な場合やモバイル デバイスが完全にオフラインの場合でも、ユーザーは業務データを表示、編集、および処理できます。 デバイスがネットワーク接続を再確立する際に、オフライン データ操作は Dynamics 365 for Operations と自動的に同期されます。
-   IT 管理者または開発者は、組織に合わせたモバイル ワークスペースを構築し公開することができます。 アプリは既存のコード資産を使用します。 したがって、検証手順、ビジネス ロジック、またセキュリティ コンフィギュレーションも再実装の必要はありません。
-   IT 管理者または開発者は、Dynamics 365 for Operations の Web クライアントに含まれているポイント アンド クリック ワークスペース デザイナーを使用してモバイル ワークスペースを簡単に設計します。
-   IT 管理者または開発者は、ビジネス ロジック拡張フレームワークを使用してワークスペースのオフライン機能を必要に応じて最適化できます。 デバイスがオフラインの間もデータは引き続き処理されるため、デバイスが常時ネットワーク接続していなくても、モバイル シナリオは豊富で流動的なままです。

## <a name="elements-of-the-mobile-app"></a>モバイル アプリの要素
モバイル アプリのナビゲーションは、ダッシュボード、ワークスペース、ページ、およびアクションという 4 つの簡単な概念で構成されています。 

[![モバイル アプリのナビゲーション概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   アプリを起動すると、**ダッシュボード** に移動します。
-   ダッシュボードでは、Dynamics 365 for Operations 環境で公開されている **ワークスペース** の一覧が表示されます。
-   各ワークスペースでは、そのワークスペースで使用可能な **ページ** の一覧が表示されます。
-   ページ上では、Dynamics 365 for Operations の 1 ページ以上のページから収集されるデータが表示されます。
-   ページからは、エンティティの詳細または明細行などの関連データの他のページに移動することができます。
-   ページ上では、そのページで使用可能な **アクション** のリストも表示されます。
-   アクションで、データ作成もしくは既存データの編集ができます。

## <a name="implementation-process"></a>実装プロセス
次の図は、組織で Dynamics 365 for Operations モバイル アプリを実装するためのプロセスを示しています。 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

次の表には、組織で Microsoft Dynamics 365 for Operations モバイル アプリを実装するのに役立つリソースへのリンクが含まれています。 最初の列の番号は、前述の図の番号付きの手順に対応します。

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>ステップ</th>
<th>役割</th>
<th>アクション</th>
<th>アクションを完了するのに役立つリソース</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>システム管理者</td>
<td>組織の Dynamics 365 for Operations を実装します。</td>
<td>Dynamics 365 for Operations をまだ組織に配置していない場合は、<a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations デモ環境の配置</a> を参照してください。</td>
</tr>
<tr class="even">
<td>2</td>
<td>システム管理者</td>
<td>Microsoft が提供するモバイル ワークスペースを有効にする KB をダウンロードしインストールします。</td>
<td>組織が使用するモバイル ワークスペースに関するトピックの &quot;前提条件&quot; セクションを参照してください。
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">コスト管理モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">手持ち在庫モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">販売注文モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">仕入先コラボレーションのモバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">プロジェクト時間入力モバイル ワークスペース</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>システム管理者</td>
<td>Microsoft が提供するモバイル ワークスペースを公開します。</td>
<td>組織が使用するモバイル ワークスペースに関するトピックの &quot;前提条件&quot; セクションを参照してください。
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">コスト管理モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">手持ち在庫モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">販売注文モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">仕入先コラボレーションのモバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">プロジェクト時間入力モバイル ワークスペース</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>開発者もしくは独立系ソフトウェア ベンダー (ISV)</td>
<td>Dynamics 365 for Operations モバイル フレームワークを使用して、カスタム モバイル ワークスペースを作成します。</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operations モバイル フレームワーク</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Dynamics 365 for Operations ワークスペース X++ APIs</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>カスタム モバイル ワークスペースを含む配置可能パッケージを作成し、Microsoft Dynamics Lifecycle Services (LCS) にそのパッケージをアップロードします。</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを生成</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>システム管理者</td>
<td>ISV が提供するカスタム ワークスペースの含まれた配置可能パッケージを適用します。</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Microsoft Dynamics 365 for Operations システムでの配置可能パッケージの適用</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>システム管理者</td>
<td>ISV が提供するカスタム モバイル ワークスペースを公開します。</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの公開</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>ユーザー</td>
<td>Dynamics 365 for Operations モバイル アプリをダウンロードしてインストールします。</td>
<td><ul>
<li>Android 用 : <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Google Play ストアの Dynamics 365 for Operations</a></li>
<li>iPhone 用 : <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">iTunes アプリ ストアの Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>ユーザー</td>
<td>サインインして Dynamics 365 for Operations モバイル アプリを使用します。 アプリには公開されたモバイル ワークスペースが含まれています。</td>
<td>Microsoft は以下のモバイル ワークスペースを提供しています。
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">コスト管理モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">手持ち在庫モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">販売注文モバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">仕入先コラボレーションのモバイル ワークスペース</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">プロジェクト時間入力モバイル ワークスペース</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>参照
--------

[Dynamics 365 for Operations モバイル アプリ用に最近リリースされたモバイル ワークスペース](mobile-workspaces-released.md)





