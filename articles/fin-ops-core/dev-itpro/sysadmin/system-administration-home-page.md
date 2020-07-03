---
title: システム管理ホーム ページ
description: このトピックは、システム管理者が利用できるリソースを一覧表示します。
author: sericks007
manager: AnnBe
ms.date: 10/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
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
ms.openlocfilehash: bc6102dae0fd2c88bc8f7b3228a51ccfabd66bbb
ms.sourcegitcommit: 497e07d7e42541f9e707495ab334cf2185b70e4e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454920"
---
# <a name="system-administration-home-page"></a>システム管理ホーム ページ

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations のシステム管理者向けコンテンツについて説明します。 このコンテンツは、組織が円滑かつ効果的に機能するようにシステムを構成するのに役立ちます。

## <a name="one-version"></a>1 つのバージョン
2018 年 7 月、一貫性があり、予測可能でシームレスな方法で最新の状態に保つのに役立つ Dynamics 365 の更新の提供方法の変更を発表しました。 次のトピックは、最新の状態を維持するために使用できる Finance and Operations サービスの更新プログラム、プロセス、ツールを明確にすることを目的としています。

- [1 つのバージョンのサービス更新の概要](../lifecycle-services/oneversion-overview.md)
- [1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-ops/get-started/one-version.md)
- [サービス更新の可用性](../../fin-ops/get-started/public-preview-releases.md)
- [クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md)
- [Lifecycle Services (LCS) によるサービスの更新の構成](../lifecycle-services/configure-service-updates.md)
- [Lifecycle Services (LCS) によるサービスの更新の一時停止](../lifecycle-services/pause-service-updates.md)
- [Lifecycle Services (LCS) でサービス更新プログラムに関する通知を受け取る](../lifecycle-services/notifications-service-updates.md)

## <a name="implementation-management-with-lifecycle-services"></a>Lifecycle Services を使用した実装管理
Microsoft Dynamics Lifecycle Services (LCS) は、Finance and Operations 実装のライフサイクルの管理に役立つ環境と定期的に更新される一連のサービスを提供するコラボレーション ポータルです。

実装のライフサイクルは、複数回、反復展開しながら、販売前から分析、設計と開発、テスト、配置、運用までのさまざまな段階に及んでいます。 管理されたクラウドまたはオンプレミスなど、プロジェクトおよび選択された配置モデルの範囲と複雑さに基づいて、数か月から数年にわたって継続できます。 

実装の管理には、顧客およびパートナー組織、特にマイクロソフトのクラウド ホスト型配置モデルのさまざまなステークホルダーが関係します。 この実装は、LCS 上で提供されるツールと、[Microsoft FastTrac](../../fin-ops/get-started/fasttrack-dynamics-365-overview.md) 内で定義されたプロセスとパートナーの実装方法を通じてサポートされます。 

- [Lifecycle Services のリソース](../lifecycle-services/lcs.md)
- [Lifecycle Services (LCS) ユーザー ガイド](../lifecycle-services/lcs-user-guide.md)

## <a name="deployment"></a>配置
クラウドまたはオンプレミスを配置できます。 クラウド展開では、Microsoft が完全に管理するエンタープライズ リソース プランニング (ERP) サービスが提供されます。 オンプレミス配置は、顧客のデータ センターにローカルに配置されます。

- [ソフトウェアのライフサイクル ポリシーおよびクラウド リリース](../migration-upgrade/versions-update-policy.md)
- [クラウド配置の概要](../deployment/cloud-deployment-overview.md)
- [クラウド配置のシステム要件](../../fin-ops/get-started/system-requirements.md)
- [オンプレミス配置のホーム ページ](../deployment/on-premises-deployment-landing-page.md)
- [オンプレミス配置のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md)

## <a name="upgrade"></a>アップグレード
アップグレードには、新しい製品バージョンへの移行、コードの移行およびアップグレード、更新プログラムへの移行、または修正プログラムの配置が含まれます。

アップグレードの各タイプのプロセスは似ていますが、開始する前に特定のタスクのトピックを確認するだけで十分です。

- [アップグレード、更新プログラム、および修正プログラムのリソース](../migration-upgrade/upgrade-home-page.md)

## <a name="database-management"></a>データベース管理
データベースを新しい環境に移動し、データベースを特定の時点に復元する方法ついての情報は、「[データベース移動操作ホーム ページ](../database/dbmovement-operations.md)」を参照してください。

## <a name="security"></a>セキュリティ
Finance and Operations アプリは、ロール ベースのセキュリティを使用します。 アクセスは、セキュリティ ロールにのみ付与され、個々のユーザーには付与されません。 ユーザーはロールに割り当てられます。 セキュリティ ロールに割り当てられているユーザーは、そのロールに関連付けられている一連の権限にアクセスできます。 任意のロールに割り当てられていないユーザーには権限がありません。

ロールベースのセキュリティは、業務の構造に合わせられます。 ユーザーが割り当てられるセキュリティ ロールは、組織内のユーザーの責任とビジネス プロセスへのユーザーの関与によって異なります。 管理者は、ユーザーが使用する必要があるプログラム要素へのアクセスではなく、ロールのユーザーが実行する職務権限へのアクセスを許可します。

自動ロール割り当てのルールを設定できるため、ユーザーの職責が変更されるたびに管理者が関与する必要はありません。 セキュリティ ロールとルールが設定された後、業務管理者は、業務データに基づいて、日常的なユーザーのアクセスを制御できます。

- [ロールベース セキュリティ](role-based-security.md)
- [セキュリティ アーキテクチャ](security-architecture.md)
- [Finance and Operations アプリにおける暗号化処理](encryption.md)

## <a name="batch-processing"></a>バッチ処理
多くのタスクをバッチ ジョブの一部として実行できます。 たとえば、バッチ ジョブには、レポートの印刷、管理の実行、電子ドキュメントの送信などのタスクを含めることができます。 バッチ ジョブを使用すると、通常の就業時間内におけるコンピュータまたはサーバーの処理速度の低下を回避できます。

- [バッチ処理の概要](batch-processing-overview.md)
- [バッチ処理とバッチ サーバー](batch-server-overview.md)

## <a name="optimization-advisor"></a>最適化アドバイザー
- [最適化アドバイザーの概要](optimization-advisor-overview.md)
- [最適化アドバイザー (ビデオ)](https://www.youtube.com/watch?v=MRsAzgFCUSQ&t=4s)
- [最適化アドバイザーのルールの作成](create-rules-optimization-advisor.md)

## <a name="office-integration"></a>Office 統合
Microsoft Office との統合により、Microsoft Office スイートを活用する、生産性の高い、コラボレーション、および統合ユーザー エクスペリエンスが提供されます。 この機能は、組織がより効率的かつ効果的になるのに役立ちます。

- [Office 統合の概要](../office-integration/office-integration.md)
- [Office 統合のチュートリアル](../office-integration/office-integration-tutorial.md)
- [Excel でエンティティ データを開き、Excel アドインを使用して更新する](../office-integration/use-excel-add-in.md)
- [[Excel で開く] エクスペリエンスの作成](../office-integration/office-integration-edit-excel.md)
- [[Excel で明細行を開く] メニューへのテンプレートの追加](../user-interface/add-templates-open-lines-excel-menu.md)
- [Microsoft Office で開くメニューのカスタマイズ](../office-integration/customize-open-office-menu.md)
- [電子メールのコンフィギュレーションと送信](../../fin-ops/organization-administration/configure-email.md)
- [Office 統合のトラブルシューティング](../office-integration/office-integration-troubleshooting.md)

## <a name="mobile"></a>携帯電話
Finance and Operations モバイル アプリにより、組織はビジネス プロセスをモバイル デバイスで使用できるようになります。 組織用のモバイル ワークスペースを有効にすると、ユーザーはアプリにサイン インしてすぐにモバイル デバイスからビジネス プロセスへ実行を開始できます。

- [モバイル アプリのホーム ページ](../mobile-apps/Mobile-app-home-page.md)
- [利用可能なモバイル ワークスペース](../mobile-apps/mobile-workspaces-released.md)

## <a name="general-administration"></a>一般管理
- [デモ データの概要](../../fin-ops/get-started/demo-data.md)
- [会社間データ共有](../sysadmin/cross-company-data-sharing.md)
- [組織の法律条項およびプライバシーに関する声明へのリンクの追加](legal-terms-privacy-statement.md)
- [ライセンス コードとコンフィギュレーション キーのレポート](license-codes-configuration-keys-report.md)
- [メンテナンス モード](maintenance-mode.md)
- [コンフィギュレーション済みのシステム アカウント](pre-configured-system-accounts.md)
- [企業間 (B2B) ユーザーを Azure Active Directory にエクスポートする](implement-b2b.md)
- [セッション アイドル タイムアウトの設定](session-idle-timeout.md)
- [AOS 起動時に Odata メタデータ キャッシュを作成する](odata-warmup.md)
- [データベース ログの構成と管理](configure-manage-database-log.md)
