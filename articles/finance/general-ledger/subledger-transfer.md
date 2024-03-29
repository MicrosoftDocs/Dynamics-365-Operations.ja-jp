---
title: 総勘定元帳への補助元帳の転送
description: この記事では、総勘定元帳の補助元帳の転送プロセスに関する機能について説明します。
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7ef93b81ce37128f7ff400eb4034ffea01756038
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779856"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>総勘定元帳への補助元帳の転送

[!include [banner](../includes/banner.md)]

この記事では、補助元帳仕訳のバッチの転送のルールに関連する機能について説明します。

バージョン 8.1 では、ルールの転送を許可するよう変更が加えられ、**同期** オプションは非推奨になりました。 詳細については、[財務と運用の削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20) を参照してください。

次のオプションは、補助元帳バッチの転送に使用できます:

- **非同期** – 総勘定元帳への補助元帳勘定項目の転送が直ちにスケジュールされます。 総勘定元帳伝票は、リソースがサーバー上で要求を処理できるようになるとすぐに記録されます。
- **スケジュール済バッチ** – 転送する必要がある補助元帳勘定仕訳が、総勘定元帳の処理キューに追加されます。 キュー内の仕訳は、受信した順序で処理されます。 リソースがサーバー上でバッチ ジョブを処理できる場合、各総勘定元帳伝票は予定時刻に勘定を更新します。

**非同期** オプションのパフォーマンスを向上させるための改良が加えられました。 この機能は、機能名 **総勘定元帳への補助元帳の転送パフォーマンスの最適化** で有効にできます。

補助元帳バッチの非同期転送の機能により、補助元帳から総勘定元帳へのデータの転送が向上します。 一連の小さなトランザクションをグループ化し、グループ内でトランザクションを転送することで、トランザクションの処理効率が向上します。 トランザクションをグループ化すると、バッチ サーバーのリソースが効率的に使用できます。

補助元帳バッチの非同期転送では、バッチ サーバー上で即時実行されるバッチ タスクが作成されるため、バッチ サーバーが設定され、オンラインであり、動作していることが必要です。 **総勘定元帳への補助元帳転送パフォーマンスの最適化** 機能を有効にする場合は、**プロセス自動化ポーリング システム ジョブ** という名前の **プロセスの自動化** システム バッチ ジョブも有効にする必要があります。 このプロセスの詳細については、[プロセスの自動化](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md)を参照してください。

バッチ レベルでの効率の変更では、システムのすべての法人に対して単一の定期バッチ ジョブが使用されます。 実行時に、まだ転送されていない必要なレコードを処理するための、新しいバッチ ジョブが作成されます。 追加の設定は、システム管理の **プロセスの自動化** ページから制御できます。 このページでは、バックグラウンド プロセスの変更、頻度の変更、およびスリープ期間の定義を実行できます。

プロセス自動化設定の詳細については、[プロセスの自動化](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md)を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

