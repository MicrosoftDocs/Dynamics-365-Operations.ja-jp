---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e1efada0dd3f3d012ba3d96978a62eb05ac276c5
ms.sourcegitcommit: 3f2bcb8745e826efcf3d82194e1cb2a41e7e0bf2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770148"
---
# <a name="known-issues-with-self-service-deployment"></a>セルフサービス配置に関する既知の問題

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。

## <a name="lifecycle-services-lcs"></a>Lifecycle Services (LCS)

### <a name="features-not-intended-to-be-implemented"></a>実装が意図されていない機能
次の LCS 機能は、セルフ サービス配置では実装されません。

- **システム診断** - 現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。 
 - **サービス要求** - サービス要求は、セルフ サービス アクションに置き換えられます。 

### <a name="known-issues-in-this-release"></a>このリリースの既知の問題
既知の問題は、将来のリリースで解決されるバグです。 2 週間おきに LCS の新しいリリースがあります。

## <a name="finance-and-operations-apps"></a>Finance and Operations アプリ 

> [!NOTE]
> Dynamics 365 Commerce は、10.0.10 リリースを使用した最新の配置エクスペリエンスに実装されています。 詳細については、[セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。

### <a name="features-not-intended-to-be-implemented"></a>実装が意図されていない機能
次の機能は、セルフ サービス配置では実装されません。

- **カスタム フォント** - カスタム フォントはサポートされていません。 詳細については、[Dynamics 365 アプリケーションのドキュメント レポート サービス](../analytics/reporting-experience-iias-environments.md)を参照してください。
- **セルフサービスのユーザー インターフェイス (UI) コンポーネントに関連したカスタマイズ** - Finance and Operations アプリで標準の Financial Reporting または SQL Server Reporting Services (SSRS) を使用しないカスタマイズは、多くの場合、AOS が実行されているオペレーティング システムの UI コンポーネントに依存します。 依存関係の例としては、Windows フォント、Internet Explorer などの Web ブラウザー、またはカスタム PDF レンダリングなどがあります。 ホスト オペレーティング システムに、フォント インフラストラクチャ、Web ブラウザー、または一般的な UI コンポーネントのサポートが含まれることを保証するものではありません。 セルフサービス インフラストラクチャに移行すると、ホスト オペレーティング システムが変更されます。 このような依存関係があり他にご質問がある場合は、Microsoft サポートに問い合わせてください。

### <a name="features-no-longer-supported"></a>サポートされなくなった機能
次の機能は、セルフ サービス配置ではサポートされなくなりました。

#### <a name="ftp"></a>FTP
FTP に依存するカスタマイズは、セルフサービスの配置ではサポートされていません。 次の情報を考慮する必要があります。

- Application Object Server (AOS) からの送信要求すべてが静的 IP アドレス上にあることを保証するものではありません。 

- 2021 年 6 月まで、特定の AOS セッション中のすべての発信要求が同じ IP アドレスに設定されます。 これは、FTP などの一部のプロセスに影響を与える可能性があります。 Power Apps を使用してファイルを引き出し、Finance and Operations アプリに API 呼び出しを実行して、データ統合フレームワークを使用してファイルをインポートすることにより、FTP の使用を除去することをお勧めします。 詳細については、[データ エンティティ統合の概要](../data-entities/integration-overview.md) を参照してください。 特定の例には以下が含まれます。

  - ([Azure Logic App での SFTP ファイルの監視、作成、および管理で説明されているように](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp))、ネイティブの SFTP コネクタを使用します。そのために、オン プレミス サービスを呼び出すためにファイアウォールでいくつかのポートを開いておく必要があります。 Logic Apps の場合、IP のリストは、全体の[地域の許可リスト ](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound)および [Power Automate での制限と構成](https://docs.microsoft.com/power-automate/limits-and-config#logic-apps)よりもはるかに短いことを考慮してください。

  - [発信 IP アドレス](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) の説明に従って、オンプレミスのデータ ゲートウェイと組み合わせて、「ローカル ファイルシステム」コネクタを使用します。 詳細については、[Azure Logic Apps のオンプレミス データ ゲートウェイのインストール](https://docs.microsoft.com/azure/logic-apps/logic-apps-gateway-install) を参照してください。 このソリューションでは、非常に高いセキュリティ レベルを維持しながら、セルフサービス配置では非推奨の IP 許可リストの必要性を完全に排除します。

  - セルフサービス機能: セルフサービス機能への移行後に FTP シナリオが失敗した場合は、FTP サーバーのコンフィギュレーションを確認してください。 最も一般的なシナリオは、許可された [IP リスト](deploymentFAQ.md#for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment)をセルフサービス環境の範囲で更新する必要があることです。

> [!NOTE]
> 非推奨機能の詳細については、[削除済みまたは非推奨のプラットフォーム機能](../get-started/removed-deprecated-features-platform-updates.md)および[以前のリリースの削除済みまたは非推奨の機能](../migration-upgrade/deprecated-features.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
