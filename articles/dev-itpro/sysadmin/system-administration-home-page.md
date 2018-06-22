---
title: "システム管理ホーム ページ"
description: "このトピックは、システム管理者が利用できるリソースを一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 11/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemAdministrationWorkspaceForm
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: 13531
ms.assetid: 2bb96ac4-0cef-4f66-a953-bd82c117247b
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 02afb36ed6b8e1a65ab1b0c6b6abe58237be3ef7
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="system-administration-home-page"></a>システム管理ホーム ページ

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations のシステム管理者向けコンテンツについて説明します。 このコンテンツは、組織が円滑かつ効果的に機能するようにシステムを構成するのに役立ちます。

## <a name="implementation-management-with-lifecycle-services"></a>Lifecycle Services を使用した実装管理
Microsoft Dynamics Lifecycle Services (LCS) は、Finance and Operations 実装のライフサイクルの管理に役立つ環境と定期的に更新される一連のサービスを提供するコラボレーション ポータルです。

Finance and Operations 実装のライフサイクルは、複数回、反復展開しながら、販売前から分析、設計と開発、テスト、配置、運用までのさまざまな段階に及んでいます。 管理されたクラウドまたはオンプレミスなど、プロジェクトおよび選択された配置モデルの範囲と複雑さに基づいて、数か月から数年にわたって継続できます。 

実装の管理には、顧客およびパートナー組織、特にマイクロソフトのクラウド ホスト型配置モデルのさまざまなステークホルダーが関係します。 この実装は、LCS 上で提供されるツールと、[FastTrack for Dynamics program](../../fin-and-ops/get-started/fasttrack-dynamics-365-overview.md) 内で定義されたプロセスとパートナーの実装方法を通じてサポートされます。 

- [Lifecycle Services for Finance and Operations](../lifecycle-services/lcs.md)
- [Dynamics Lifecycle Services ユーザー ガイド](../lifecycle-services/lcs-user-guide.md)

## <a name="deployment"></a>配置
Finance and Operations をクラウドまたはオンプレミスに展開することができます。 クラウド展開では、Microsoft が完全に管理するエンタープライズ リソース プランニング (ERP) サービスが提供されます。 オンプレミス配置は、顧客のデータ センターにローカルに配置されます。

- [オンライン サービスおよびオンプレミス ソフトウェアのライフサイクル ポリシー](../migration-upgrade/versions-update-policy.md)
- [Dynamics 365 for Finance and Operations クラウド配置の概要](../deployment/cloud-deployment-overview.md)
- [クラウド配置のシステム要件](../../fin-and-ops/get-started/system-requirements.md)
- [オンプレミス配置のランディング ページ](../deployment/on-premises-deployment-landing-page.md)
- [オンプレミス配置のシステム要件](../../fin-and-ops/get-started/system-requirements-on-prem.md)

## <a name="upgrade"></a>アップグレード
アップグレードには、新しい製品バージョンへの移行、コードの移行およびアップグレード、更新プログラムへの移行、または修正プログラムの配置が含まれます。

アップグレードの各タイプのプロセスは似ていますが、開始する前に特定のタスクのトピックを確認するだけで十分です。

- [ホーム ページのアップグレード](../migration-upgrade/upgrade-home-page.md)

## <a name="database-management"></a>データベース管理
次の内容は、データベースを新しい環境に移動し、データベースを特定の時点に復元するのに役立ちます。

- [Finance and Operations データベースを Azure SQL データベースから SQL Server 環境にコピーする](../database/copy-database-from-azure-sql-to-sql-server.md)
- [Finance and Operations データベースを SQL Server から Azure SQL データベース運用環境にコピーする](../database/copy-database-from-sql-server-to-azure-sql.md)
- [非実稼働環境でのデータベースの復元](../database/request-point-in-time-restore.md)
- [後で復元する Finance and Operations のデータベースのコピーを作成する](../database/copy-operations-database.md)

## <a name="security"></a>セキュリティ
Finance and Operations は、ロール ベースのセキュリティを使用します。 アクセスは、セキュリティ ロールにのみ付与され、個々のユーザーには付与されません。 ユーザーはロールに割り当てられます。 セキュリティ ロールに割り当てられているユーザーは、そのロールに関連付けられている一連の権限にアクセスできます。 任意のロールに割り当てられていないユーザーには権限がありません。

ロールベースのセキュリティは、業務の構造に合わせられます。 ユーザーが割り当てられるセキュリティ ロールは、組織内のユーザーの責任とビジネス プロセスへのユーザーの関与によって異なります。 管理者は、ユーザーが使用する必要があるプログラム要素へのアクセスではなく、ロールのユーザーが実行する職務権限へのアクセスを許可します。

自動ロール割り当てのルールを設定できるため、ユーザーの職責が変更されるたびに管理者が関与する必要はありません。 セキュリティ ロールとルールが設定された後、業務管理者は、業務データに基づいて、日常的なユーザーのアクセスを制御できます。

- [ロールベース セキュリティ](role-based-security.md)
- [セキュリティ アークテクチャ](security-architecture.md)

## <a name="batch-processing"></a>バッチ処理
Finance and Operations では、多くのタスクをバッチ ジョブの一部として実行できます。 たとえば、バッチ ジョブには、レポートの印刷、管理の実行、電子ドキュメントの送信などのタスクを含めることができます。 バッチ ジョブを使用すると、通常の就業時間内におけるコンピュータまたはサーバーの処理速度の低下を回避できます。

- [バッチ処理の概要](batch-processing-overview.md)
- [バッチ サーバーの概要](batch-server-overview.md)

## <a name="optimization-advisor"></a>最適化アドバイザー
- [最適化アドバイザーの概要](optimization-advisor-overview.md)
- [最適化アドバイザー (ビデオ)](https://www.youtube.com/watch?v=MRsAzgFCUSQ&t=4s)
- [最適化アドバイザーのルールの作成](create-rules-optimization-advisor.md)

## <a name="office-integration"></a>Office 統合
Microsoft Office との統合により、Microsoft Office スイートを活用する、生産性の高い、コラボレーション、および統合ユーザー エクスペリエンスが提供されます。 この機能は、組織がより効率的かつ効果的になるのに役立ちます。

- [Office 統合](../office-integration/office-integration.md)
- [Office 統合のチュートリアル](../office-integration/office-integration-tutorial.md)
- [Excel アドインの使用](../office-integration/use-excel-add-in.md)
- [[Excel で開く] エクスペリエンスの作成](../office-integration/office-integration-edit-excel.md)
- [[Excel で明細行を開く] メニューへのテンプレートの追加](../user-interface/add-templates-open-lines-excel-menu.md)
- [[Microsoft Office で開く] メニューのカスタマイズ](../office-integration/customize-open-office-menu.md)
- [電子メールのコンフィギュレーションと送信](../../fin-and-ops/organization-administration/configure-email.md)
- [Office 統合のトラブルシューティング (タスク ガイド)](../office-integration/office-integration-troubleshooting.md)

## <a name="mobile"></a>携帯電話
Microsoft Dynamics 365 for Unified Operations モバイル アプリにより、組織は業務プロセスをモバイル デバイスで使用できるようになります。 組織用のモバイル ワークスペースを有効にすると、ユーザーはアプリにサイン インしてすぐにモバイル デバイスからビジネス プロセスへ実行を開始できます。

- [モバイル アプリのホーム ページ](../mobile-apps/Mobile-app-home-page.md)
- [モバイル ワークスペース](../mobile-apps/mobile-workspaces-released.md)

## <a name="general-administration"></a>一般管理
- [デモ データの概要](../../fin-and-ops/get-started/demo-data.md)
- [会社間データ共有](../sysadmin/cross-company-data-sharing.md)
- [組織の法律条項およびプライバシーに関する声明へのリンクの追加](legal-terms-privacy-statement.md)
- [ライセンス コードとコンフィギュレーション キーのレポート](license-codes-configuration-keys-report.md)
- [メンテナンス モード](maintenance-mode.md)
- [コンフィギュレーション済みのシステム アカウント](pre-configured-system-accounts.md)
- [B2B ユーザーの Azure AD へのエクスポート](implement-b2b.md)

