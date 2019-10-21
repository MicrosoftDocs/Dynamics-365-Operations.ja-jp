---
title: オンプレミス配置に実装されない機能
description: このトピックでは、オンプレミス展開で実装されていない機能を一覧表示します。
author: sericks007
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21881
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 8810a0279647ccabd45205c7847879ba1ad3b739
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250294"
---
# <a name="features-not-implemented-in-on-premises-deployments"></a>オンプレミス配置に実装されない機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 Finance + Operations (オンプレミス) の配置で実装されていない機能を一覧表示します。 このトピックは次の 2 つのセクションに分かれています。

- 最初のセクションにはまだ実装されていない機能がリストされています。 これらの機能は推奨されていません。
- 2 番目のセクションには、オンプレミスの展開で使用する予定のない機能が一覧表示されています。 これらの機能を実装する計画はありません。

## <a name="features-not-yet-implemented"></a>まだ実装されていない機能

次の機能は、オンプレミスの配置ではまだ実装されていません。 これらの機能は推奨されていませんでした。 これらの機能が、設置展開にとって重要な場合は、[アイデア](https://experience.dynamics.com/ideas/) サイトからフィードバックを提供し、お知らせください。

| 機能                                                          | 説明 |
|------------------------------------------------------------------|-------------|
| タスク レコーダー                                                    | Lifecycle Services (LCS) のタスク レコーダー ライブラリはサポートされていません。 タスクの記録は、ローカル ファイル システムから読み込むか保存できます。 |
| **サポート** ウィンドウ                                                 | **サポート** ウィンドウ (**ヘルプとサポート** \> **サポート**) はまだ使用できません。 |
| PowerBI.com 統合                                          | PowerBI.com 統合は、まだオンプレミス展開では使用できません。 たとえば、タイルをピン留めする、またはワークスペースに PowerBI.com 定期売買からレポートする機能は使用できません。 |
| 定期統合 API                                       | 継続的に統合が行われるAPIフレームワークでは、定期的なデータジョブの運用をサポートしていません。 オンプレミス環境ではデータ管理APIフレームワークのみに対応しています。 |
| Microsoft Office 統合                                             | SharePoint オンプレミス サポートは、まだ使用できません。 SharePoint オンラインもまだサポートされていません (認証の問題のため)。<br><br>Skype for Business オンプレミスはサポートされていません。  |
| 電子申告 (ER) と LCS の統合                   | LCS との ER 統合はサポートされません。 ER 構成は LCS から直接ダウンロードすることができません。                                   |
| SharePoint との ER 統合            | SharePoint との統合はサポートされていません。 SharePoint サーバーを、ER を使用して生成された電子ドキュメントの出力先として構成することはできません。                           |
| ビジネス ドキュメントの管理            | ビジネス ドキュメント管理機能を使用して、ビジネス ドキュメントの生成に使用するテンプレートの編集をすることはできません。 ER フレームワークのみを使用することができます。 Microsoft Office の統合は、オンプレミス展開には未対応のためです。                           |
| OData を使用して Power BI レポートを作成する                              | Power BI デスクトップまたは Excel PowerQuery ツールを使い、OData での Power BI レポートの作成はサポートされていません。                                                                                  |
|購買要求: 外部カタログからのパンチアウト |外部カタログから購買要求にショッピング カートをチェックアウトすることはできません。 |
|Trace Parser および PerfTimer |これらのツールは動作していないか、このリリースで機能が制限されています。 これらの機能は、将来のリリースで実装される予定です。 |
|SSRS スケール アウト  |現在の SQL Server Reporting Services (SSRS) はスケール アウトをサポートしていません。この機能は将来のリリースの際に追加されます。 |
|テレメトリ  |現在、テレメトリはクラウドへ転送されません。 今後の更新プログラムで、テレメトリ データをクラウドに転送できるようになります。 |
|データ タスクの自動化  |[データ タスクの自動化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-task-automation)は現在実装されていません。 |

## <a name="features-available-in-81"></a>8.1 で使用可能な機能

| 機能 | 説明 |
|---------|-------------|
| Retail  | オンプレミス展開で現在利用可能な小売機能の一覧を表示するには、[オンプレミス展開で利用可能な小売機能](../../../retail/retail-onprem.md)を参照してください。 |

## <a name="features-not-intended-for-use-in-on-premises-deployments"></a>オンプレミス配置での使用を目的としない機能

次の機能は、オンプレミスの配置での使用を目的としていません。 オンプレミスの展開でこれらの機能を実装する計画はありません。

| 機能                    | 説明 |
|----------------------------|-------------|
| SSRS レポート ビューアー コントロール | SQL Server Reporting Services (SSRS) では、オンプレミス Web クライアントと互換性のあるレポート ビューアー コントロールをサポートしていません。<p>レポートは、オンプレミス サービスによって PDF ドキュメントとしてレンダリングされます。 拡張機能を使用して、アプリケーション レポートに埋め込みドリルスルー リンクを有効にします。</p> |
| ドキュメント回覧エージェント     | このコンポーネントは、オンプレミスの展開には必要ありません。 オンプレミス配置は、ドメインで認証されたサーバーでホストされます。 これにより、ネットワーク プリンター デバイスに安全かつ直接アクセスできます。 |
