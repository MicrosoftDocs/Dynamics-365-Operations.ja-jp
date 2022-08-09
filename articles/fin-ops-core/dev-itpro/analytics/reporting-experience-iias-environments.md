---
title: IaaS 環境における既定のレポート エクスペリエンス
description: この記事では、財務と運用アプリの改ページ対応レポートに関する情報を提供します。
author: RichdiMSFT
ms.date: 05/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom:
- "27661"
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: fb2042bdd1ecf59e8c77f7df28986a89c2373437
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9205578"
---
# <a name="document-reporting-service-in-dynamics-365-applications"></a>Dynamics 365 アプリケーションのドキュメント レポート サービス

[!include [banner](../includes/banner.md)]

## <a name="reporting-scenarios-in-erp"></a>ERP におけるレポートのシナリオ

財務と運用アプリにバンドルされたドキュメント レポート サービスは、エンタープライズ リソース プランニング (ERP) における次の 2 つの基本的なユーザー機能、または一般的なシナリオを促進するユーザー ツールを提供します: **ドキュメント生成** および **ビジネス インテリジェンス (BI) と分析**。 これらの一般的なシナリオは、業務データにアクセスするために最も頻繁に使用される 2 つの方法を表します。

- **ドキュメントの生成** 印刷や電子メールの一括配信を主要な目的とする、構造化されたドキュメントを作成します。
- **BI と分析** 集計に基づいた、参照データへのリンクが埋め込まれている対話形式の視覚化を行います,。 ユーザーは、これらの視覚情報を活用して、大量のデータのパターンと傾向を特定します。

Document Reporting Service は、ビジネス文書を一括生成するにあたっての最適なツールですが、分析ビューを適応させたり、ビジネス環境の頻繁な変化に対応するために、パワーユーザーが必要とする拡張性のオプションが不足しています。 また、[Microsoft Power BI サービス](/power-bi/fundamentals/power-bi-overview) は、あらゆる規模のビジネスに強力な分析を提供する業界のリーダーとして認知されています。 財務と運用アプリと Power BI サービスの統合オプションは、顧客のビジネス データのシームレスな探索に対応しています。

> [!NOTE]
> バージョン 10.0.12 のプラットフォーム更新プログラムがリリースされると、Dynamics 365 serviceでは、ページ分割されたレポートでの BI および分析の相互作用に使用されるレポート ビューア コントロールのサポートを中止します。 代わりに、ドキュメント報告サービスが表示するレポートには、埋め込み PDF ビューアーが使用されます。 埋め込み PDF ビューアーの詳細については、[埋め込みビューアを使用した PDF ドキュメントのプレビュー](preview-pdf-documents.md) を参照してください。

### <a name="comparison-of-report-scenarios"></a>レポート シナリオの比較

ドキュメント生成のシナリオでは、自動または手動のシンプルなビ業務活動が、1 から数百のドキュメントの生成をトリガーする場合があります。 これらドキュメントは、商業的なブランディングを含むグラフィックで装飾されている場合が多いです。 ドキュメントは、事前に定義された配信ルーティング指示を使用して、社内外の受信者に配信されます。

次の表では、2つのレポート作成経験の基本を比較しています。

| 項目                     | ドキュメントの生成 | BI と分析 |
|--------------------------|---------|------------------|
| **表示の形式**       | PDF と Office ドキュメント | HTML |
| **データ量**          | 1 から 数百規模の行 | 数万以上の行 |
| **インタラクティブな機能** | 印刷、テキスト検索、共有 | [ドリルスルー、ドリルダウン、ネストされた領域](/sql/reporting-services/report-design/drillthrough-drilldown-subreports-and-nested-data-regions) |
| **データ ソース**          | トランザクションのデータベース | データ ウェアハウス |
| **レポート作成者**        | 開発者 | パワー ユーザー |
| **レイアウト**               | 構造化された定義済みのレイアウト | 適応性のある柔軟なレイアウト |
| **推奨するツール**  | [ドキュメント レポート サービス](document-reporting-services.md)/[構成可能な Office ドキュメント](general-electronic-reporting.md) | [Power BI.com](power-bi-integration.md)/[analytical workspaces](embed-power-bi-workspaces.md) |

## <a name="enhancements-in-paginated-reporting"></a>改ページの調整がされるレポートの機能拡張

PDF を使用して、財務と運用アプリにバンドルされているドキュメント レポート サービスでレンダリングされたドキュメントを操作することには、いくつかの利点があります:

- **レポートが画面に迅速に表示されます。** レポートを画面に表示することで、パフォーマンスを向上させることができます。 このパフォーマンスの向上により、プログレス バーの数が減少し、レポートの速度が向上します。
- **サービスの信頼性が向上します。** 最新のドキュメント レポート サービスのアーキテクチャにより、クラウド規模の能力がご利用の環境に提供されます。 このサービスには、リソース使用率を最大化する自動スケーリング機能が含まれています。
- **印刷出力の忠実性が高くなります。** ドキュメントは、プリンタの出力との整合性を保つため、文書は PDF 形式で表示されます。
- **ローカルのデバイスを使用してドキュメントを印刷することができます。** ブラウザーからプリンターに直接ドキュメントを送信する際に、ユーザーの ID を管理できます。 [コントロール] ツールバーに組み込まれたユーザー オプションを使用して、ドキュメントの印刷時に印刷ジョブのセキュリティ保護に役立てることができます。

埋め込み型の PDF ビューアを環境でプレビューする方法については、、[埋め込みビューアを使用した PDF ドキュメントのプレビュー](preview-pdf-documents.md) を参照してください。

### <a name="turn-off-bi-and-analytics-in-one-box-environments"></a>単一ボックス環境で BI と Analytics をオフにする

バージョン 10.0.11 のプラットフォーム更新プログラムでは、BI 機能と分析機能をオフにした状態で、ローカル ドキュメント レポートサービスに RDL をレンダリングさせることによって、既存のソリューションをプレビューできます。 この表示モードは、**RDL サンドボックス** と呼ばれます。 この機能は、Windows PowerShell コマンドを使用してオン、またはオフにすることができます。

次の手順に従って、ローカルの単一ボックス環境で RDL サンドボックスを有効にします。

1. バージョン 10.0.11 またはそれ以降を使用している単一ボックス環境にログインします。
2. Windows PowerShell を開き、C:\AOSService\PackagesLocalDirectory\Plugins\AxReportVmRoleStartupTask\. に移動します。
3. **UpdateRDLSandboxRule.ps1** コマンドを実行します。 パラメータのリストを以下に示します。

    - **ConfigPath** : SQL Server Reporting SERVICES (SSRS) が既定の場所に配置されていない場合は、構成の場所を指定します。
    - **RemoveRules** : ルールを削除するには、このパラメーターを設定します。
    - **ForceUpdate** : ルールを強制的に再作成するには、このパラメーターを設定します。
    - **LogDir** : ログの書き込みをする場所を指定します。 既定の場所は、**UpdateRDLSandboxRule.ps1** コマンドの場所となります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
