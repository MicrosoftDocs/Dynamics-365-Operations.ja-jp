---
title: "モバイル アプリのホーム ページ"
description: "このトピックでは、Microsoft Dynamics 365 for Unified Operations モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。"
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f4736a7041c746350fa073bd58929c840f7689bf
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="mobile-app-home-page"></a>モバイル アプリのホーム ページ

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Unified Operations モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。

> [!NOTE]
> 以前のモバイル アプリの名前は、*Microsoft Dynamics 365 for Finance and Operations* でした。

<a name="overview"></a>概要
--------

モバイル アプリにより、組織が業務プロセスをモバイル デバイスで使用可能になります。 IT 管理者が組織用のモバイル ワークスペースを有効にすると、ユーザーはアプリにログインしてすぐにモバイル デバイスから業務プロセスの実行を開始できます。 モバイル アプリには、生産性を高めるのに役立つ次の機能が含まれています。

- ネットワーク接続が断続的な場合やモバイル デバイスが完全にオフラインの場合でも、ユーザーは業務データを表示、編集、および処理できます。 デバイスがネットワーク接続を再確立する際に、オフライン データ操作は Dynamics 365 for Finance and Operations と自動的に同期されます。
- IT 管理者または開発者は、組織に合わせたモバイル ワークスペースを構築し公開することができます。 アプリは既存のコード資産を使用します。 したがって、検証手順、ビジネス ロジック、またセキュリティ コンフィギュレーションも再実装の必要はありません。
- IT 管理者または開発者は、Web クライアントに含まれているポイント アンド クリック ワークスペース デザイナーを使用してモバイル ワークスペースを簡単に設計できます。
- IT 管理者または開発者は、ビジネス ロジック拡張フレームワークを使用してワークスペースのオフライン機能を必要に応じて最適化できます。 デバイスがオフラインの間もデータは引き続き処理されるため、デバイスが常時ネットワーク接続していなくても、モバイル シナリオは豊富で流動的なままです。

## <a name="elements-of-the-mobile-app"></a>モバイル アプリの要素
モバイル アプリのナビゲーションは、ダッシュボード、ワークスペース、ページ、およびアクションという 4 つの基本概念で構成されています。 

[![モバイル アプリのナビゲーション概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. アプリを起動すると、**ダッシュボード** に移動します。
2. ダッシュボードでは、公開された **ワークスペース** の一覧が表示されます。
3. 各ワークスペースでは、そのワークスペースで使用可能な **ページ** の一覧が表示されます。
4. ページ上では、いくつかの操作を行うことができます。 次にいくつか例を挙げます。

    - 詳細データの表示。
    - エンティティの詳細または明細行などの関連データの他のページに移動します。
    - そのページに有効な **アクション** の一覧を参照してください。 アクションで、データ作成もしくは既存データの編集ができます。

## <a name="implementation-process"></a>実装プロセス
次の図では、Microsoft に提供されるモバイル ワークスペースとカスタム モバイル ワークスペースの両方を実装するためのプロセスを表示します。 

![モバイル アプリの実装プロセス](./media/Mobile-implementation-process-5.png)

次の表には、Microsoft によって提供されるモバイル ワークスペースとカスタム モバイル ワークスペースの両方を実装する際に役立つリソースへのリンクが含まれています。 最初の列の番号は、前述の図の番号付きの手順に対応します。

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
<td>組織内の Finance and Operations を実装します。</td>
<td><ul><li>まだ Microsoft Dynamics 365 のバージョンを配置していない場合は、<a href="../deployment/deploy-demo-environment.md">デモ環境を配置</a> を参照してください。</li><li>使用可能なモバイル ワークスペースの一覧は、<a href="mobile-workspaces-released.md">最近リリースされたモバイル ワークスペース</a> を参照してください。</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>システム管理者</td>
<td><strong>Microsoft Dynamics 365 for Operations バージョン 1611 を使用している場合:</strong> Microsoft が提供するモバイル ワークスペースを有効にする KB をダウンロードしインストールします。</td>
<td>詳細については、次のトピックを参照してください。
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">コスト管理モバイル ワークスペース</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">手持在庫モバイル ワークスペース</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">販売注文モバイル ワークスペース</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">仕入先コラボレーションのモバイル ワークスペース</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">プロジェクト時間入力モバイル ワークスペース</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">経費管理モバイル ワークスペース</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>システム管理者</td>
<td>Microsoft が提供するモバイル ワークスペースを公開します。</td>
<td><a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>開発者もしくは独立系ソフトウェア ベンダー (ISV)</td>
<td>モバイル プラットフォームを使用して、カスタム モバイル ワークスペースを作成します。</td>
<td><a href="platform/mobile-platform-home-page.md">モバイル プラットフォーム</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>カスタム モバイル ワークスペースを含む配置可能パッケージを作成し、Microsoft Dynamics Lifecycle Services (LCS) にそのパッケージをアップロードします。</td>
<td><a href="../deployment/create-apply-deployable-package.md">配置可能パッケージを作成</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>システム管理者</td>
<td>独立系ソフトウェア ベンダー (ISV) が提供するカスタム ワークスペースの含まれた配置可能パッケージを適用します。</td>
<td><a href="../deployment/apply-deployable-package-system.md">配置可能パッケージの適用</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>システム管理者</td>
<td>ISV が提供するカスタム モバイル ワークスペースを公開します。</td>
<td><a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>ユーザー</td>
<td>モバイル アプリのダウンロードとインストール。</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android フォン用</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">iPhone 用</a></li></ul>
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>ユーザー</td>
<td>ログインして、モバイル アプリを使用します。 アプリには、システム管理者によって公開されたモバイル ワークスペースが含まれています。</td>
<td>Microsoft が提供したモバイル ワークスペースの一覧は、<a href="mobile-workspaces-released.md">最近リリースされたモバイル ワークスペース</a> を参照してください。
</td>
</tr>
</tbody>
</table>

