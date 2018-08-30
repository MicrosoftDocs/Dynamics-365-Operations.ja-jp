---
title: "オンプレミス配置で実装されていない機能"
description: "このトピックでは、オンプレミス展開で実装されていない機能を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21881
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: d060ec6f75be25605f5c57d256cd4cff49cf3d1b
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="features-that-arent-implemented-in-on-premises-deployments"></a>オンプレミス配置で実装されていない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations のオンプレミス展開で実装されていない機能を一覧表示します。 このトピックは次の 2 つのセクションに分かれています。
- 最初のセクションにはまだ実装されていない機能がリストされています。 これらの機能は推奨されていません。
- 2 番目のセクションには、オンプレミスの展開で使用する予定のない機能が一覧表示されています。 これらの機能を実装する計画はありません。

## <a name="features-not-yet-implemented"></a>まだ実装されていない機能
次の機能は、オンプレミスの配置ではまだ実装されていません。 これらの機能は推奨されていませんでした。 これらの機能が、設置展開にとって重要な場合は、[アイデア](https://experience.dynamics.com/ideas/) サイトからフィードバックを提供し、お知らせください。

| **機能**                                                      | **説明**                                                                                                                                                                          |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| タスク レコーダー                                                    | Lifecycle Services (LCS) のタスク レコーダー ライブラリはサポートされていません。 タスクの記録は、ローカル ファイル システムから読み込むか保存できます。                                                                  |
| **サポート** ウィンドウ                                                         | **サポート** ウィンドウ (**ヘルプとサポート** > **サポート**) はまだ使用できません。                                                                                                                                                   |
| PowerBI.com 統合                                          | PowerBI.com 統合は、まだオンプレミス展開では使用できません。 たとえば、タイルをピン留めする、またはワークスペースに PowerBI.com 定期売買からレポートする機能は使用できません。 |
| Microsoft Office 統合                                             | SharePoint オンプレミス サポートは、まだ使用できません。 SharePoint オンラインもまだサポートされていません (認証の問題のため)。<br><br>Skype for Business オンプレミス サポートは、まだ使用できません。 Skype for Business オンラインがサポートされます。  |
| データ統合 | データ管理でのパッケージ API 経由のデータのインポートおよびエクスポート機能は、Finance and Operations のすべてのバージョン (プラットフォーム更新プログラム 12 を含むバージョン 7.2、ビルド 7.0.4709.41184を除く) で、まだ使用できません。 | 
| 電子申告 (ER) と LCS の統合                   | LCS との ER 統合はサポートされません。 ER 構成は、LCS から Finance and Operations へ直接ダウンロードことはできません。                                   |
| ER と SharePoint の統合            | SharePoint との統合はサポートされていません。 SharePoint サーバーを、ER を使用して生成された電子ドキュメントの出力先として構成することはできません。                           |
| OData を使用して Power BI レポートを作成する                              | Power BI desktop または Excel PowerQuery ツールを使用して OData で Power BI レポートを作成することはサポートされていません。                                                                                  |
|Retail| オンプレミス展開で現在利用可能な小売機能の一覧を表示するには、[[オンプレミス展開で利用可能な小売機能](../../retail/retail-onprem.md)] を参照してください。 Retail 機能の可用性に関する詳細については、[Dynamics 365 for Retail オンプレミス – 変動配置オプションの有効化](https://community.dynamics.com/enterprise/b/365forretail/archive/2017/12/15/dynamics-365-for-retail-on-premises-enabling-flexible-deployment-options) を参照してください。
|購買要求: 外部カタログからのパンチアウト |外部カタログから購買要求にショッピング カートをチェックアウトすることはできません。 |
|Trace Parser および PerfTimer |これらのツールは動作していないか、このリリースで機能が制限されています。 これらの機能は、将来のリリースで実装される予定です。 |
|SSRS スケール アウト  |現在の SQL Server Reporting Services (SSRS) はスケール アウトをサポートしていません。この機能は将来のリリースの際に追加されます。 |
|テレメトリ  |現在、テレメトリはクラウドへ転送されません。 今後の更新プログラムで、テレメトリ データをクラウドに転送できるようになります。 |

## <a name="features-not-intended-for-use-in-on-premises-deployments"></a>オンプレミス配置での使用を目的としない機能
次の機能は、オンプレミスの配置での使用を目的としていません。 オンプレミスの展開でこれらの機能を実装する計画はありません。

| **機能**                                                      | **説明**                                                                                                                                                                          |
|----------------------------------|-------------------------------------------------|
| SSRS レポート ビューアー コントロール       |SQL Server Reporting Services (SSRS) では、オンプレミス Web クライアントと互換性のあるレポート ビューアー コントロールをサポートしていません。<br><br>レポートは、オンプレミス サービスによって PDF ドキュメントとしてレンダリングされます。 拡張機能を使用して、アプリケーション レポートに埋め込みドリルスルー リンクを有効にします。|
| ドキュメント回覧エージェント           |このコンポーネントは、オンプレミスの展開には必要ありません。  オンプレミス配置は、ドメインで認証されたサーバーでホストされます。 これにより、ネットワーク プリンター デバイスに安全かつ直接アクセスできます。



