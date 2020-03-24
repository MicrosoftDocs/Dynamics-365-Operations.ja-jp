---
title: 削除済みまたは非推奨のプラットフォーム機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095777"
---
# <a name="removed-or-deprecated-platform-features"></a>削除済みまたは非推奨のプラットフォーム機能

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="platform-update-32"></a>プラットフォーム update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります
|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 変更要求が意図しないユーザーに送信される可能性があったため、これはセキュリティ上の問題でした。 また、これはワークフローの作成者が誰であるかをユーザーが決定し、手動で選択するよう促すものであったため、操作性の問題でもありました。  |
| **別の機能で置き換えられているか?**   | いいえ |
| **影響を受ける製品領域**         | ワークフロー |
| **配置オプション**              | すべて |
| **ステータス**                         | Platform update 32 の要求変更ダイアログ ボックスからユーザー選択ドロップダウン リストが削除されました。 変更要求は、作成者に対して意図したとおりに自動的に送信されます。 この機能の詳細については、[ワークフロー承認プロセスでのアクション](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change)を参照してください。 |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>埋め込み型のドリルスルー リンクは、クラウドでホストされるサービスによって表示されるページ番号付きドキュメントではサポートされなくなりました 
|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | サービスによって表示されるドキュメントに埋め込まれたナビゲーション URL には、機密業務データが含まれる場合があります。 顧客データをさらに保護するセキュリティ上の事前措置として、ドキュメントでの埋め込み型のドリルスルー リンクのサポートを削除しています。 また、ユーザーは、この変更の結果として対話的にドキュメントを作成する際にパフォーマンスを向上させることもできます。  |
| **別の機能で置き換えられているか?**   | 無 |
| **影響を受ける製品領域**         | レポート |
| **配置オプション**              | すべて |
| **ステータス**                         | この機能は、サービスからアクティブに削除されています。<br><br>最新のクライアントには、アプリケーションのナビゲーションを支援する自動生成リンクを含むさまざまなオプションが用意されています。 サービスによって表示されるページ番号付きドキュメントは、受信者向けに電子メールで送信、アーカイブ、印刷される外部通信に推奨されます。 ドキュメントを直接ブラウザーでプレビューするエクスペリエンスが改善され、ローカル プリンターに直接アクセスできるようになりました。 詳細については、[埋め込みビュアーを使用してPDFドキュメントのプレビューをする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents) を参照してください。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表
以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../migration-upgrade/deprecated-features.md)を参照してください。

