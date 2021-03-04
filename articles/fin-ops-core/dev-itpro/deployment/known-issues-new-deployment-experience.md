---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: f9345aa54995608e496cf53b8bd21f20edbd9d36
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679284"
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
- **セルフサービスの UI コンポーネントに関連したカスタマイズ** - Finance and Operations アプリで標準の Financial Reporting または SQL Server Reporting Services (SSRS) を使用しないカスタマイズは、多くの場合、AOS が実行されているオペレーティング システムの UI コンポーネントに依存します。 依存関係の例としては、Windows フォント、Internet Explorer などの Web ブラウザー、またはカスタム PDF レンダリングなどがあります。 ホスト オペレーティング システムに、フォント インフラストラクチャ、Web ブラウザー、または一般的な UI コンポーネントのサポートが含まれることを保証するものではありません。 セルフサービス インフラストラクチャに移行すると、ホスト オペレーティング システムが変更されます。 このような依存関係があり他にご質問がある場合は、Microsoft サポートに問い合わせてください。

### <a name="features-no-longer-supported"></a>サポートされなくなった機能
次の機能は、セルフ サービス配置ではサポートされなくなりました。

#### <a name="ftp"></a>FTP
FTP に依存するカスタマイズは、セルフ サービス配置ではサポートされず、次のアクションを検討する必要があります。

- **再試行の追加** - これは、短期から中期のオプションと見なす必要があります。 現在のインフラストラクチャ デザインによって、コントロールとデータ呼び出しに一致する IP が許可されます。 このデザインは変更される場合があります。 
- **コントロールおよび同じ IP からのデータに対する FTP 要求を無効にする** - この場合は、状況に応じてセキュリティの影響を慎重に評価します。
- **FTP の使用を削除** - たとえば、Power Apps を使用してファイルを引き出し、Finance and Operations にアプリに API 呼び出しを実行して、データ統合フレームワークを使用してファイルをインポートします。 詳細については、[データ統合戦略の選択](../data-entities/integration-overview.md) を参照してください。
- **SFTP 使用** - 静的な発信 IP アドレスを使用することはお勧めしません。 詳細については、[Finance and Operations 静的 IP アドレス](https://community.dynamics.com/ax/b/axinthefield/posts/dynamics-365-for-finance-and-operations-static-ip-addresses) ブログの投稿を参照してください。

一般には、FTP の使用を解除することをお勧めします。 Dynamics 365 から SFTP への直接接続は使用しないでください。 代わりに、2 つの間の Logic App を使用します。 Logic App では、次の 2 つのオプションがあります。

- ([Azure Logic App での SFTP ファイルの監視、作成、および管理で説明されているように](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp))、ネイティブの SFTP コネクタを使用します。そのために、オン プレミス サービスを呼び出すためにファイアウォールでいくつかのポートを開いておく必要があります。 Logic Apps の場合、IP のリスト、全体の[地域の許可リスト ](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) および [Power Automate での制限と構成](https://docs.microsoft.com/power-automate/limits-and-config#logic-apps) よりもはるかに短いことを考慮してください。

- [発信 IP アドレス](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) の説明に従って、オンプレミスのデータ ゲートウェイと組み合わせて、「ローカル ファイルシステム」コネクタを使用します。 詳細については、[Azure Logic Apps のオンプレミス データ ゲートウェイのインストール](https://docs.microsoft.com/azure/logic-apps/logic-apps-gateway-install) を参照してください。 このソリューションでは、非常に高いレベルのセキュリティを維持しながら、セルフ サービス配置では非推奨の IP 許可リストは、完全に削除する必要があります。

> [!NOTE]
> 非推奨の機能の詳細については、[削除済みまたは非推奨のプラットフォーム機能](../get-started/removed-deprecated-features-platform-updates.md)、[以前のリリースからの削除済みおよび非推奨の機能](../migration-upgrade/deprecated-features.md)、[以前のリリースの削除済みおよび非推奨の機能](../get-started/removed-deprecated-features-platform-updates.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]