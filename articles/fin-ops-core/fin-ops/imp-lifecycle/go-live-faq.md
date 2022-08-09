---
title: 実装プロジェクト FAQ の Go-live
description: この記事では、実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。
author: OlgaPetrovaFT
ms.date: 06/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: olpetrov
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 09cd16b8f46b0c01de13fe6d109e4a913b42976b
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108894"
---
# <a name="go-live-for-implementation-projects-faq"></a>実装プロジェクト FAQ の Go-live

[!include [banner](../includes/banner.md)]

この記事では、実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。

## <a name="when-can-i-configure-and-request-my-production-environment"></a>運用環境をいつ構成および要求できますか ?

通常、運用環境は、すべてのカスタマイズのコードが完了し、ユーザー受け入れテスト (UAT) が完了し、顧客がソリューションからサインオフし、稼働中にブロッキングの問題がなく、Microsoft で **Go-live 準備完了レビュー** が正常に完了した後に展開されます。 このプロセスを理解するには、[Go-Live の準備](prepare-go-live.md)を参照してください。 

運用環境は、業務運営の実行のためにのみ使用し、テストまたはトレーニング目的で使用しないでください。 切替を実行し、計画した場合は、運用の切替を無視することができます。 ソリューションをテストするには、テストに必要な要素とサービスを使用して設計されたサンドボックス環境を使用する必要があります。

## <a name="what-are-the-prerequisites-to-deploy-a-production-environment"></a>運用環境を配置するための前提条件

前提条件の一覧については、 [Go-Live の準備](prepare-go-live.md) を参照してください。

## <a name="what-is-a-go-live-readiness-review-and-why-is-it-required"></a>Go-live 準備完了レビューとは何ですか、またそれがなぜ必要ですか?

Go-live 準備完了レビューは、プロジェクトの準備完了を評価し、円滑で正常な稼働を支援することを目的にしています。 このプロセスを理解するには、[Go-Live の準備](prepare-go-live.md)を参照してください。 

このレビューは、運用環境を展開する前にすべての実装プロジェクトで必須です。

## <a name="i-want-to-request-my-production-environment-who-do-i-contact-for-a-go-live-readiness-review"></a>運用環境を要求します。 Go-live 準備完了レビューのために誰に連絡しますか?
[Go-live の準備](prepare-go-live.md) という記事のガイダンスに従って、Go-live 準備完了レビューを開始する方法について理解してください。  

## <a name="the-production-button-isnt-available-in-lcs-how-do-i-request-my-production-environment"></a>生産ボタンは、LCS では使用できません。 運用環境を要求するにはどうすればよいですか。

LCS の **生産** ボタンは、LCS 実装方法の **分析**、**デザイン & 開発**、および **テスト** フェーズが完了し、Microsoft で **Go-live 準備完了レビュー** が完了した後にのみ使用できます。 詳細については、「[Go-Live の準備](prepare-go-live.md)」を参照してください。

LCS で方法フェーズを完了する方法の詳細については、[財務と運用アプリの顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。

## <a name="my-sandbox-environment-is-currently-on-an-update-that-is-set-to-expire-in-two-months-can-i-request-a-production-environment-that-has-the-latest-update"></a>自分のサンドボックス環境は、現在有効期限が 2 か月に設定されている更新プログラムにあります。 最新の更新プログラムを含む運用環境を要求できますか。

稼働予定のバージョンである受入テスト環境で使用したのと同じバージョンの運用環境を配置することを強く推奨します。 予期しない動作や予期しない問題が発生し Go-live エクスペリエンスに悪影響を与えることがあるので、実際にテストしたバージョンとは異なるバージョンで稼働することは推奨 **されません**。 

必要に応じて本稼働後しばらくは品質アップデートを適用することができるように、サービス終了間近 **ではない** バージョンで稼働することを強くお勧めします。 ユーザー受け入れテスト (UAT) を行うバージョンを慎重に計画し、最新の状態に保つことは重要です。

詳細については、[ソフトウェアのライフサイクル ポリシーおよびクラウド リリース](../../dev-itpro/migration-upgrade/versions-update-policy.md) および [サービス更新の可用性](../../fin-ops/get-started/public-preview-releases.md) を参照してください。

## <a name="our-sandbox-environments-are-deployed-in-a-different-datacenter-from-where-we-want-our-production-environment-to-be-deployed-can-i-select-a-different-datacenter-for-my-production-environment"></a>運用環境は、サンド ボックス環境が配置されている同じデータ センターに配置する必要があります。 運用環境に対して別のデータセンターを選択できますか?

稼働予定のデータセンターである受入テスト環境で使用したのと同じデータセンターの運用環境を配置することを強く推奨します。 同じデータセンターを使用することで、待機時間を検証し、生産のような条件下ですべてのサービスをサポートすることができます。 予期しないパフォーマンスの問題や予期しない機能のギャップが発生し Go-live エクスペリエンスに悪影響を与えることがあるので、実際にテストしたバージョンとは異なるデータセンターで稼働することは推奨 **されません**。

正しいデータ センターを選択するのに役立つ情報の詳細については、「システム要件」記事の[ネットワーク要件](../get-started/system-requirements.md#network-requirements) セクションを参照してください。

## <a name="how-will-my-production-environment-be-sized"></a>運用環境はどのくらいの規模になりますか。

運用環境のサイズは、現在のユーザー ライセンス数と、運用環境を要求するときに有効なサブスクリプションの推定の情報に基づいて決まります。

> [!NOTE]
> 新しいサブスクリプション見積を送信する場合、運用環境のサイズは、ユーザー数、ユーザーのライセンスの種類、および予想されるピーク時のトランザクション量に応じて変更する必要があります。 新しい見積が処理された後、3日以内に、環境の次のサービス工程により、更新が自動的に適用されます。 または、サポート チケットを作成して、変更を適用する特定の時間を要求することもできます。

## <a name="i-submitted-the-request-for-a-production-environment-but-i-made-a-mistake-can-i-still-change-it"></a>運用環境の要求を送信しましたが、間違いが発生しました。 いまでも変更できますか。

いいえ。 要求を送信すると、すぐに運用環境の展開が開始されます。 展開が完了するまで待ち、サポート チケットをログに記録して運用環境を削除して、再配置する必要があります。

## <a name="how-long-does-it-take-to-deploy-my-production-environment"></a>運用環境を配置するにはどのくらい時間がかかりますか。

Microsoft の Go-live 準備完了レビューが完了すると、LCS の運用環境スロットが有効になり、プロジェクト チーム (顧客/パートナー) が環境の配置をトリガーできます。 配置プロセスには約 30 分かかります。

## <a name="what-level-of-access-do-i-have-in-my-production-environment-can-i-sign-in-to-the-vm"></a>自分の運用環境にて、どのレベルのアクセスが可能ですか。 VM にログインできますか。

一連番号 運用環境へのアクセスは制限されます。 仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。 また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。

## <a name="how-often-is-my-production-database-backed-up"></a>どのくらいの頻度で運用データベースがバックアップされますか。

データベースは自動バックアップによって保護されています。 完全なデータベース バックアップは毎週行われ、差異のデータベース バックアップは毎時間行われ、およびトランザクション ログのバックアップは 5 分ごとに行われます。 自動バックアップは 28 日間保持されます。

詳細については、[自動 SQL データベースのバックアップについて](/azure/sql-database/sql-database-automated-backups) を参照してください。

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>運用データベースのバックアップのコピーを要求できますか。

いいえ。 ただし、運用データベースはティア 2 以上の環境にコピーできます。 コピー操作が完了した後、サンドボックス環境をバックアップすることができます。 詳細については、[データベースの更新](../../dev-itpro/database/database-refresh.md) を参照してください。

## <a name="my-golden-configuration-database-is-in-a-tier-1-sandbox-environment-how-can-i-copy-and-restore-it-to-my-production-environment"></a>高品質の構成データベースは、第 1 層サンドボックス環境にあります。 運用環境にどのようにコピーおよび復元しますか。
データベースをコピーして復元するには、記事の[ゴールデンコンフィギュレーションプロモーション](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md) の指示に従います。 

> [!NOTE]
> 高品質の構成がデータ パッケージにある場合、運用環境に手動でデータ パッケージをインポートする必要があります。

## <a name="after-go-live-can-i-apply-new-code-changes-to-the-production-environment"></a>Go-Live の後、運用環境に新しいコード変更を適用することはできますか?

はい。 

詳細については、[クラウド環境への更新プログラムの適用](../../dev-itpro/deployment/apply-deployable-package-system.md)を参照してください。

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>運用環境がダウンした場合はどうすればよいでしょうか ?

稼働停止をレポートするには、記事の[稼働停止のレポート](../../dev-itpro/lifecycle-services/report-production-outage.md) で説明されているプロセスに従います。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

