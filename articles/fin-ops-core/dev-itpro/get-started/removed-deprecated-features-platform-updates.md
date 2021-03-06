---
title: 削除済みまたは非推奨のプラットフォーム機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。
author: sericks007
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 435f7f0090ca16a9e8cfee2d1ceb65bec8457d09
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111727"
---
# <a name="removed-or-deprecated-platform-features"></a>削除済みまたは非推奨のプラットフォーム機能

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラムから削除された、または削除される予定の機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

このリストは、これらの削除および削除予定に対して、自身の計画を検討するために役立ちます。 

Finance and Operations アプリ内のオブジェクトに関する詳細情報については、[技術参照レポート](/dynamics/s-e/global/axtechrefrep_61)を参照してください。 これら異なるバージョンのレポートを比較し、Finance and Operations アプリの各バージョンで変更または削除されたオブジェクトについて確認することができます。

## <a name="feature-deprecation-notice-effective-may-2021"></a>2021 年 5 月からの機能非推奨の通知

### <a name="globalization-portal-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) のグローバリゼーション ポータル

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | この機能は他の LCS ベースのサービスに引き継がれたため、LCS のグローバリゼーション ポータルは非推奨になりました。 |
| **別の機能で置き換えられているか?**   | はい、この機能は LCS [問題検索](../lifecycle-services/issue-search-lcs.md) と [Dynamics 規制警告送信サービス](../lcs-solutions/submit-localization-alerts.md) に置き換えられます。 |
| **影響を受ける製品領域**         | LCS のグローバリゼーション ポータル|
| **配置オプション**              | クラウド配置 |
| **状態**                         | 非推奨: 2022 年 5 月に削除予定。 |


## <a name="feature-removed-effective-january-28-2021"></a>機能が 2021 年 1 月 28 日に削除済み

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>SQL インデックスの最適化を処理するためのバッチ ジョブ

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 顧客によるインデックス管理の運用、監視、および管理の間接費を削減するために、この機能は削除されました。 |
| **別の機能で置き換えられているか?**   | 今後、インデックスのメンテナンスは Microsoft サービスによって実行されます。 これは、ユーザーのワークロードに影響を与えずに連続して発生します。 |
| **影響を受ける製品領域**         | Finance and Operations アプリ|
| **配置オプション**              | クラウドの配置: Microsoftによって管理される実稼働環境および Tier 2 から Tier 5 の環境に影響します。 |
| **状態**                         | この機能は削除されました。 |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.17 に対する Platform update


### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | Visual Studio の最新バージョンをサポートするためには、Visual Studio の X++ 拡張機能に変更を加える必要があります。 これらの変更は、Visual Studio 2015 と互換性がありません。 |
| **別の機能で置き換えられているか?**   | Visual Studio 2017 は、配置および必要なバージョンとして Visual Studio 2015 を置き換えます。 |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | All |
| **状態**                         | 非推奨: 更新時に、以前の X++ ツールは Visual Studio 2015 から削除され、更新されたツールは Visual Studio 2015 にはインストールされません。 ホストされているビルドには影響はありません。 仮想マシンを構築する場合は、[Azure Pipelines でのレガシ パイプラインの更新](../dev-tools/pipeline-msbuild-update.md) の説明に従って、ビルド パイプライン (ビルド定義) を手動で更新して、MSBuild 14.0 (Visual Studio 2015) から MSBuild 15.0 (Visual Studio 2017) に依存関係を変更する必要があります。 |

### <a name="user-avatar"></a>ユーザー アバター 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | ナビゲーション バーの右側に表示されるユーザーの権限は、既に廃止されている、Dynamics 365 ヘッダー コントロールの API を使用して取得されました。 |
| **別の機能で置き換えられているか?**   | ユーザーは、ナビゲーション バーのイニシャルを円の中に表示します。 これは、開発機械で現在使用されているビジュアルと同じです。 |
| **影響を受ける製品領域**         | Web クライアント |
| **配置オプション**              | All |
| **状態**                         | バージョン 10.0.17 から削除済み |

### <a name="enterprise-portal-ep-deprecation"></a>エンタープライズ ポータル (EP) の非推奨  

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | Dynamics AX 2012 エンタープライズ ポータル (EP) に関連付けられたメタデータ コンポーネントは、Finance and Operations アプリケーションでサポートされたことがないので廃止されました。 |
| **別の機能で置き換えられているか?**   | なし |
| **影響を受ける製品領域**         | Web クライアント |
| **配置オプション**              | All |
| **状態**                         | 非推奨: すべての EP コードは、2021 年 10 月リリース版で削除される予定です。 |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.15 に対する Platform update

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Dynamics 365 における Internet Explorer 11 のサポートの非推奨

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 2020 年 12 月より、すべての Dynamics 365 製品における Microsoft Internet Explorer 11 のサポートは非推奨になり、2021 年 8 月以降、Internet Explorer 11 はサポートされなくなります。<br><br>これは、Internet Explorer 11 のインターフェイスを通じて使用されるように設計された Dynamics 365 製品を使用しているユーザーに影響します。 2021 年 8 月以降、そのような Dynamics 365 製品では Internet Explorer 11 はサポートされません。 |
| **別の機能で置き換えられているか?**   | Microsoft Edge に移行することをお勧めします。|
| **影響を受ける製品領域**         | すべての Dynamics 365 製品 |
| **配置オプション**              | All|
| **状態**                         | 非推奨: 2021 年 8 月を過ぎると、Internet Explorer 11 はサポートされなくなります。|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>メタデータ修正プログラムを適用するための Visual Studio アドイン

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | メタデータ修正プログラムは、バージョン 8.1 で 2018 年 7 月に導入された [One Version](../../fin-ops/get-started/one-version.md) サービス更新プログラムではサポートされなくなりました。 |
| **別の機能で置き換えられているか?**   | サポートされているバージョンでは、個別のメタデータ修正プログラムは使用できません。 代わりに、累積的な品質更新が適用されます。 |
| **影響を受ける製品領域**         | Visual Studio アドイン |
| **配置オプション**              | 開発仮想マシン |
| **ステータス**                         | バージョン 10.0.15 では、アドインが Visual Studio ツールに含まれなくなりました。 |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.14 に対する Platform update

### <a name="online-users-page"></a>オンライン ユーザー ページ 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | これは、以前のクライアント/サーバー アーキテクチャ用に構築されたレガシーページです。 このページの情報は常に正確であるとは限らず、混乱や誤解を招く可能性があります。 |
| **別の機能で置き換えられているか?**   | 今後の更新プログラムで新しいページを提供する予定です。|
| **影響を受ける製品領域**         | システム管理 |
| **配置オプション**              | All |
| **ステータス**                         | 2021 年 10 月までに、このフォームは削除されます。   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.13 に対する Platform update


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS レポート プロパティで定義されたカスタム コード 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 一般に、カスタム コードは限られたメリットしかなく、同時に重要なリソースと、サポートのためのコンピューティングが必要になります。 カスタム コードは、レポート作成者が主にカスタム コード アセンブリからパブリック メソッドを呼び出すために使用します。 ただし、クラウドにホストされるサービスは、SSRS レポートのカスタム アセンブリへの参照はサポートしていません。 |
| **別の機能で置き換えられているか?**   | レポート作成者は、すべてのテキスト ボックス式での計算、変換、書式設定の処理に対して、パブリック .NET API を引き続き参照することを選択できます。 詳細については、[コードをレポート (SSRS) に追加する](/sql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15) をご覧ください。  |
| **影響を受ける製品領域**         | カスタム コードを含む RDL で定義されているアプリケーション レポート デザインのサブセット。 |
| **配置オプション**              | All |
| **ステータス**                         | バージョン 10.0.13 を使用した場合、コンパイラは、SSRS レポート定義でカスタム コードが検出された場合に警告を発行します。 この問題を修正するには、レポート デザイン定義を開き、すべてのカスタム コードの成果物を削除します。 この警告は、将来の更新でコンパイラ エラーに置換されます。   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>3 つの jQuery コンポーネント ライブラリのアップグレード 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | セキュリティ修正プログラムと通貨を維持するために、3 つの jQuery コンポーネントライブラリが更新されています。   
| **別の機能で置き換えられているか?**   | この問題は、jQuery (バージョン 2.1.4 からのバージョン 3.5.0)、jquery UI (バージョン 1.11.4 1.12.1 のバージョン 3.0.3)、jQuery qTip (バージョンから 2.2.1) に影響されます。 JQuery は移行ガイダンスをオンラインで提供しています。  |
| **影響を受ける製品領域**         | 拡張可能なコントロール、特に廃止または削除された Api を使用したカスタム JavaScript コード |
| **配置オプション**              | すべて |
| **ステータス**                         | バージョン 10.0.13/プラットフォーム アップデート 37を使用すると、必要に応じて "3 つの jQuery コンポーネント ライブラリをアップグレードする" 機能を有効にして、最新のライブラリに移動することができます。 影響を受ける API の移行時間を確保するために、2021 年 4 月のリリースでは、新しいライブラリへの移動が必須となります。   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>既存のグリッドコントロール/forceLegacyGrid () API

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 既存のグリッドコントロールは、新しいグリッドコントロールに置き換えられます。 |
| **別の機能で置き換えられているか?**   | [新しいグリッド コントロール](../..//fin-ops/get-started/grid-capabilities.md) |
| **影響を受ける製品領域**         | Web クライアント |
| **配置オプション**              | すべて |
| **ステータス**                         | バージョン 10.0.13 では、新しいグリッド コントロールが一般に使用可能であり、ユーザーは必要に応じてこの機能を有効にすることができます。 新しいグリッド コントロールは、2021 年 10 月リリースで必須になります。 この新しいグリッド コントロールが必須化される場合、**forceLegacyGrid()** API は尊重されません。 |

### <a name="personalization-without-saved-views"></a>保存されていないビューのないパーソナル化 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | パーソナル化サブシステムは、ビューの保存機能にオーバーホールされているので、パフォーマンスが向上し、追加機能を提供します。 |
| **別の機能で置き換えられているか?**   | 保存されているビュー |
| **影響を受ける製品領域**         | Web クライアント |
| **配置オプション**              | すべて |
| **ステータス**                         | バージョン 10.0.13/プラットフォーム更新プログラム 37では、ビューの保存機能は一般に使用可能であり、ユーザーは必要に応じてこの機能を有効にすることができます。 この保存されたビュー機能は、2021 年 10 月リリースで必須になります。 |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.12 に対する Platform update

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>無効なフィールド参照を含むグリッドまたはグループ コントロール フォームの拡張機能

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | グリッド コントロールまたはグループ コントロールのデータ グループ プロパティは、フィールド グループのすべてのフィールドを自動的に表示するために使用されます。 拡張機能によって追加されたグリッドまたはグループ コントロールには、そのフィールド グループで既に定義されていないフィールドが含まれているか、そのフィールド グループで定義されているフィールドが欠落している可能性があります。 これにより、ランタイムで動作が一貫しなくなる場合があります。 Finance and Operations アプリのバージョン 10.0.12 に対するプラットフォームのアップデートは、この問題をコンパイラ *警告* として分類できるようになりました。 この問題を解決するには、フォームの拡張機能を開いて保存します。
| **別の機能で置き換えられているか?**   | このコンパイラの警告は、将来の更新でコンパイラ エラーに置換されます。 |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | すべて |
| **ステータス**                         | Finance and Operations アプリのバージョン 10.0.12 のプラットフォーム更新でコンパイラの警告が出て、コンパイラのエラーになりました。 |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations アプリのバージョン 10.0.11 に対する Platform update

### <a name="explicit-safe-lists-for-self-service-environments"></a>セルフ サービス環境のための明示的なセーフ リスト

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | IP をセーフ リストに移動するプロセスが変更されました。 セルフサービスでは IP セーフ リストはもうサポートしていません。 |
| **別の機能で置き換えられているか?**   | 詳細については、[Azure Active Directory の条件付きアクセスの構成](/appcenter/general/configuring-aad-conditional-access) をご覧ください。|
| **影響を受ける製品領域**         | セキュリティ |
| **配置オプション**              | クラウド |
| **ステータス**                         | 非推奨: この機能は、セルフサービス配置に対して完全に廃止されました。 |

### <a name="visual-studio-2015"></a>Visual Studio2015

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | Visual Studio の最新バージョンをサポートするためには、Visual Studio の X++ 拡張機能に変更を加える必要があります。 これらの変更は、Visual Studio 2015 と互換性がありません。 |
| **別の機能で置き換えられているか?**   | Visual Studio 2017 は、配置および必要なバージョンとして Visual Studio 2015 を置き換えます。 |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | All |
| **ステータス**                         | バージョン 10.0.13 (プラットフォームの更新 37) またはそれ以降のバージョンで展開される仮想マシンには、Visual Studio 2017 が含まれます。 バージョン 10.0.16 (プラットフォームの更新 40) は、Visual Studio 2015 をサポートする最終リリースです 。 Visual Studio 2015 のみを含む仮想マシンは、バージョン 10.0.17 (プラットフォーム更新 41) に更新することはできません。 |

### <a name="field-groups-containing-invalid-field-references"></a>無効なフィールド参照を含むフィールド グループ

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | テーブル メタデータ定義のフィールド グループには、無効なフィールド参照を含めることができます。 これらのフィールド グループを展開すると、Financial Reporting と Microsoft SQL Server Reporting Services (SSRS) でランタイム エラーが発生する可能性があります。 Platform update 23 では、このメタデータの問題に対応するコンパイラの *警告* が導入されました。 Finance and Operations アプリのバージョン 10.0.11 に対する Platform update は、この問題をコンパイラ *エラー* として分類します。<p>この問題を解決するには、次の手順に従います。</p><ol><li>テーブルのフィールド グループの定義から無効なフィールド参照を削除します。</li><li>再コンパイル。</li><li>すべてのエラーが対処されていることを確認します。</li></ol> |
| **別の機能で置き換えられているか?**   | コンパイラ エラーは、コンパイラの警告を完全に置換します。  |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: コンパイラの警告は、Finance and Operations アプリのバージョン 10.0.11 に対するプラットフォーム更新でのコンパイラ エラーです。 |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>SHA1 ハッシュ アルゴリズムを使用して作成された ISV ライセンス

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 独立系ソフトウェア ベンダー (ISV) ライセンスを作成するためのプロセスが変更されました。 詳細については、[独立系ソフトウェア ベンダー (ISV) ライセンス](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes) を参照してください。 |
| **別の機能で置き換えられているか?**   | はい。 Windows PowerShell を使用してライセンスを作成します。 |
| **影響を受ける製品領域**         | Visual Studio 開発ツール |
| **配置オプション**              | すべて |
| **ステータス**                         | 非推奨: SHA1 ハッシュ アルゴリズムを使用して作成された ISV のライセンス。 このアルゴリズムは、MakeCert ユーティリティを使用して作成された証明書に依存しており、このユーティリティは推奨されていません。<br><br>非推奨: セキュリティまたはハッシュ目的の SHA1 の使用。 SHA1 は、2021 年の初めに機能を停止する予定です。 したがって、今後は使用しないでください。<br><br>削除済み: トランスポート層セキュリティ (TLS) 1.0 と TLS 1.1 着信要求または送信要求をサポートします。 |

## <a name="platform-update-32"></a>プラットフォーム update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>ワークフロー要求の変更ダイアログ ボックスにユーザー選択ドロップダウン リストは表示されなくなります

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | 変更要求が意図しないユーザーに送信される可能性があったため、これはセキュリティ上の問題でした。 また、これはワークフローの作成者が誰であるかをユーザーが決定し、手動で選択するよう促すものであったため、操作性の問題でもありました。  |
| **別の機能で置き換えられているか?**   | いいえ |
| **影響を受ける製品領域**         | ワークフロー |
| **配置オプション**              | すべて |
| **ステータス**                         | Platform update 32 の要求変更ダイアログ ボックスからユーザー選択ドロップダウン リストが削除されました。 変更要求は、作成者に対して意図したとおりに自動的に送信されます。 この機能の詳細については、[ワークフロー承認プロセスでのアクション](../../fin-ops/organization-administration/workflow-actions.md?toc=%2fdynamics365%2fcommerce%2ftoc.json#request-change)を参照してください。 |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>埋め込み型のドリルスルー リンクは、クラウドでホストされるサービスによって表示されるページ番号付きドキュメントではサポートされなくなりました 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **廃止 / 削除の理由** | サービスによって表示されるドキュメントに埋め込まれたナビゲーション URL には、機密業務データが含まれる場合があります。 顧客データをさらに保護するセキュリティ上の事前措置として、ドキュメントでの埋め込み型のドリルスルー リンクのサポートを削除しています。 また、ユーザーは、この変更の結果として対話的にドキュメントを作成する際にパフォーマンスを向上させることもできます。  |
| **別の機能で置き換えられているか?**   | 無 |
| **影響を受ける製品領域**         | レポート |
| **配置オプション**              | すべて |
| **ステータス**                         | この機能は、サービスからアクティブに削除されています。<br><br>最新のクライアントには、アプリケーションのナビゲーションを支援する自動生成リンクを含むさまざまなオプションが用意されています。 サービスによって表示されるページ番号付きドキュメントは、受信者向けに電子メールで送信、アーカイブ、印刷される外部通信に推奨されます。 ドキュメントを直接ブラウザーでプレビューするエクスペリエンスが改善され、ローカル プリンターに直接アクセスできるようになりました。 詳細については、[埋め込みビュアーを使用してPDFドキュメントのプレビューをする](../analytics/preview-pdf-documents.md) を参照してください。 |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>削除済みまたは非推奨の機能に関する以前の発表
以前のリリースで削除または非推奨になった機能の詳細については、[以前のリリースで削除または非推奨になった機能](../migration-upgrade/deprecated-features.md)を参照してください。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
