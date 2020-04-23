---
title: 削除済みまたは非推奨のプラットフォーム機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。
author: sericks007
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: 0072ca507301fdb880f0595a06377ff01366ca20
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260532"
---
# <a name="removed-or-deprecated-platform-features"></a>削除済みまたは非推奨のプラットフォーム機能

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。

- *削除された*機能は製品では使用できません。
- *削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

> [!NOTE]
> Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.11 に対する Platform update

### <a name="field-groups-containing-invalid-field-references"></a>無効なフィールド参照を含むフィールド グループ

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | テーブル メタデータ定義のフィールド グループには、無効なフィールド参照を含めることができます。 これらのフィールド グループを展開すると、Financial Reporting と Microsoft SQL Server Reporting Services (SSRS) でランタイム エラーが発生する可能性があります。 Platform update 23 では、このメタデータの問題に対応するコンパイラの *警告* が導入されました。 Finance and Operations アプリのバージョン 10.0.11 に対する Platform update は、この問題をコンパイラ *エラー* として分類します。<p>この問題を解決するには、次の手順に従います。</p><ol><li>テーブルのフィールド グループの定義から無効なフィールド参照を削除します。</li><li>再コンパイル。</li><li>すべてのエラーが対処されていることを確認します。</li></ol> |
| **別の機能で置き換えられているか?**   | コンパイラ エラーは、コンパイラの警告を完全に置換します。  |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | すべて |
| **ステータス**                         | **非推奨:** コンパイラ警告は、Finance and Operations アプリのバージョン 10.0.11 に対する Platform update でコンパイラ エラーになりました。 |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>SHA1 ハッシュ アルゴリズムを使用して作成された ISV ライセンス

|   |  |
|------------|--------------------|
| **廃止 / 削除の理由** | 独立系ソフトウェア ベンダー (ISV) ライセンスを作成するためのプロセスが変更されました。 詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes) を参照してください。 |
| **別の機能で置き換えられているか?**   | はい。 Windows PowerShell を使用してライセンスを作成します。 |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | すべて |
| **ステータス**                         | <strong>非推奨:</strong> SHA1 ハッシュ アルゴリズムを使用して作成された ISV のライセンス。 このアルゴリズムは、MakeCert ユーティリティを使用して作成された証明書に依存しており、このユーティリティは推奨されていません。<p><strong>非推奨:</strong> セキュリティまたはハッシュ目的の SHA1 の使用。 SHA1 は、2021 年の初めに機能を停止する予定です。 したがって、今後は使用しないでください。<p><strong>削除済み:</strong> トランスポート層セキュリティ (TLS) 1.0 と TLS 1.1 着信要求または送信要求をサポートします。 |

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

