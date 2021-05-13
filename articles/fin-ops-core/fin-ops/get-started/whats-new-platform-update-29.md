---
title: Finance and Operations アプリのプラットフォーム更新プログラム 29 (2019 年 10 月) の新機能および変更された機能
description: このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラム 29 の機能について説明します。
author: tonyafehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: Platform update 29
ms.openlocfilehash: 40d6178a57a0b1b82503631d232309b0e8bf9ac5
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937522"
---
# <a name="whats-new-or-changed-in-platform-update-29-for-finance-and-operations-apps-october-2019"></a>Finance and Operations アプリのプラットフォーム更新プログラム 29 (2019 年 10 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Finance and Operations アプリのプラットフォーム更新プログラム 29 の新機能または変更された機能について説明します。 このバージョンのビルド番号は 7.0.5372 です。 一般提供開始日は 10 月ですが、新機能は 8 月の初期リリースで使用できます。 プラットフォーム更新プログラム 29 の詳細については [追加リソース](whats-new-platform-update-28.md#additional-resources) を参照してください。


## <a name="feature-management"></a>機能管理
機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。 プラットフォーム更新プログラム29には、次のような追加機能が追加されています:
- 有効になっていないすべての機能を有効にします。
- 更新後にすべての機能を自動的に有効にします。
- 既存のコンフィギュレーション キーが有効になっているなど、条件に基づいて機能を有効にすることはできません。
- 新しい機能を手動で検索して、機能の一覧に追加する **更新の確認** というボタンを追加します。

詳細については [機能管理の概要](feature-management/feature-management-overview.md) を参照してください。

## <a name="data-management-job-history-clean-up"></a>データ管理ジョブ履歴のクリーンアップ
実行履歴の定期的なクリーンアップをスケジュールするには、データ管理の [ジョブ履歴クリーンアップ機能](../../dev-itpro/data-entities/data-import-export-job.md#job-history-clean-up) を使用する必要があります。 この機能は、現在は推奨されていない既存のステージング テーブルのクリーンアップ機能を置き換えます。

## <a name="business-events-catalog-security"></a>ビジネス イベント カタログのセキュリティ
[ロールベース セキュリティ](../../dev-itpro/business-events/home-page.md#role-based-security-for-business-events) は、ビジネス イベント カタログの個々のビジネス イベントに適用できるようになりました。 このセキュリティを有効にしてコンフィギュレーションすると、ユーザーは、ロールがアクセス権を持つビジネス イベントのみを表示したり、購読したりすることができます。 このセキュリティは、 Microsoft Flow などの統合シナリオにも適用されます。

## <a name="attachment-recovery"></a>添付ファイルの回復
レコード 添付ファイルのごみ箱を提供する添付ファイルの回復機能が追加されました。 削除後の設定された期間、ユーザーおよび管理者は、新しく削除された添付ファイルフォームを使用して、削除された添付ファイルを回復できます。 詳細については、以下 [ドキュメント管理のコンフィギュレーション](../organization-administration/configure-document-management.md) を参照してください。

## <a name="session-idle-timeout"></a>セッション アイドル タイムアウト
セッション アイドル タイムアウトは、セッションがタイムアウトして閉じるまでにユーザーが非アクティブになれる時間の長さを表します。 プラットフォーム更新プログラム 29では、ユーザーインターフェイスに Web ブラウザー セッション タイムアウト設定が公開され、既定値が 60 分ではなく 30 分に最適化されています。 最大60分まで値を変更および設定できますが、システムに余分な負荷が発生する可能性があります。 詳細については、 [セッション アイドル タイムアウトの設定](../../dev-itpro/sysadmin/session-idle-timeout.md) を参照してください。

## <a name="visual-refresh-of-the-web-client-to-align-with-the-fluent-design-language"></a>Fluent Design言語に合わせたWeb クライアントのビジュアル更新
Dynamics 365アプリ全体の取り組みの一環として、Web クライアントのビジュアル更新に向けて段階的に取り組んでおり、コントロールとページを Microsoft Fluent Design言語とより密接に連携させています。 プラットフォーム 更新プログラム 29 には、変更の初期セットが含まれています。 詳細については、リリース計画の [Fluent Design言語に合わせたWeb クライアントのビジュアル更新](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/visual-refresh-web-client-align-fluent-design-language) トピックを参照してください。

この変更の一部として、ダッシュボードのワークスペース タイルに新しいビジュアル スタイルが追加されました。 視覚的に配置されるワークスペース タイルの画像の作成に関する更新されたガイダンスについては、[ワークスペース タイル用のアイコンの作成](../../dev-itpro/user-interface/create-icons-workspace-tiles.md)を参照してください。

##  <a name="saved-views-preview"></a>保存されたビュー (プレビュー)
保存されたビュープがプレビューで使用できるようになりました。 この機能は、個人用設定サブシステムの大幅な拡張機能であり、ユーザーは、ページごとに複数の名前を付けた個人用設定セットを持つことができます。 リストページでは、これらのビューにフィルターを含めることもできます。 ビューはセキュリティ ロールに対して公開できるので、個人用設定の管理もビューを使用することで大幅に簡単になります。 開発者環境でこの機能を有効にする方法の詳細については、 [保存されたビュー](saved-views.md) を参照してください。 また、 [保存されたビューを十分に活用するフォームの作成](../../dev-itpro/user-interface/understanding-saved-views.md) トピックも参照してください。 このプレビュー機能は、一般に使用可能になるまで進化し変更し続けることに注意してください。 

## <a name="new-grid-control-preview"></a>新しいグリッド コントロール (プレビュー) 
[新しいグリッド コントロール](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/user-productivity-new-grid) がプレビューで使用できるようになりました。 この新しいグリッドは既存のグリッド コントロールに代わるものであり、より高速なレンダリング、よりスムーズなスクロール、グリッド内でのより簡単なナビゲーション、ドラッグ アンド ドロップによる列の並べ替えなどの機能を備えています。 新しいグリッドでは、フッターの表形式グリッドの数値列の下部に総計を表示することもできます。これは、列ヘッダーの右クリック コンテキスト メニューを使用して有効にできます。 有効にすると、すべての表形式とリストのグリッドが自動的に新しいグリッドを使用するように切り替わります。ただし、非反応拡張コントロールを含むグリッドがページにある場合は、既存のグリッドコントロールがそのページで使用されます。 このプレビュー機能は、一般に使用可能になるまで進化し変更し続けることに注意してください。

新しいグリッドコントロールを試すには、開発者環境のURLに &debug=reactGridを追加します。 フライティングによって、他の環境で機能が動作しなくなることに注意してください。  

## <a name="workflow-work-item-notifications-in-the-action-center"></a>アクション センターのワークフロー作業項目通知 
ユーザー は、 **設定** > **ユーザー オプション** > **ワークフロー** > **通知** > **アクションセンターに通知を送信** に移動して、アクション センターで通知を受信することを選択できます。 有効にすると、ユーザーに割り当てられた新しい作業項目ごとに通知を受け取ります。

## <a name="workflows-can-now-support-reset"></a>ワークフローがリセットをサポートできるようになりました。
ワークフローは、必要に応じて **WorkflowIRecallUnrecoverable** インターフェイスを実装することによって、ワークフロー履歴フォームからのリセットをサポートできるようになりました。 仕入先請求書ワークフローでは、このインターフェイスを使用して、修復できない仕入先請求書ワークフローを取り消して、キャンセル済の状態にすることができます。

## <a name="workflow-deletion-will-confirm-business-event-subscription-deletions"></a>ワークフローの削除によって、ビジネス イベント サブスクリプションの削除が確認されます。
ワークフローに関連付けられたビジネス イベント サブスクリプションが見つかると、ユーザーがワークフローの削除による影響を十分に認識できるように、関連するすべてのビジネス イベント サブスクリプションの一覧が確認ダイアログボックスに表示されます。

## <a name="improved-payloads-for-workflow-business-events"></a>ワークフロー ビジネス イベントのためのペイロードの改善
標準ワークフロー コンテキストが、所有者、作成者、前回のメモを含むすべてのワークフロー ビジネス イベントのペイロードに追加されました。

## <a name="flow-templates-for-workflow-work-item"></a>ワークフロー作業項目のフロー テンプレート
フローテンプレートは、作業項目の完了を容易にするフローを作成する際に便利な開始点を提供するために作成されました。 詳細については [ワークフロー ビジネス イベント](../../dev-itpro/business-events/business-events-workflow.md) を参照してください。

## <a name="extensibility-enhancements"></a>拡張性の強化
プラットフォーム更新プログラム 29では、次の拡張機能が追加されました。

- WorkflowApprovalプロパティ、WorkflowTaskプロパティの拡張、およびWorkflowOutcomesのWorkflowTaskへの追加を有効にします (Ref# 198831)。
- テーブル フィールド グループからのフォームのフィールドに対してイベント トリガーを有効にします (Ref# 247364)。
- クラス宣言で FormObservable 属性の使用を有効にします (Ref# 198797) 。
- 拡張子の既定の名前にモデル名を追加して競合を減らします (Ref# 300468)。
- フォーム データソースおよびセキュリティ権限で、拡張テーブル フィールドの使用を有効にします (Ref# 315634)。
- 標準フォーム コントロールのカスタム権限では、拡張フォームに設定されたアクセス許可プロパティ値を考慮する必要があります (Ref# 313650)。
- 拡張機能によって追加されたテーブル表示メソッドをルックアップ メソッドとして使用できるようにします (Ref# 243486)。
- 拡張機能を使用して、フォーム データソースに表示メソッドを追加できるようにします (Ref# 256004) 。

## <a name="codelens-for-method-references-in-the-x-editor"></a>X++ エディターのメソッド照会用 CodeLens
X++ ソース コード エディターには、現在、Visual Studio の CodeLens 機能を利用しています。 X++ メソッドへの参照の数は、メソッド宣言線のすぐ上の CodeLens に表示されます。 参照カウントをクリックすると、そのメソッドに関するすべての参照を見つけることができます。 

## <a name="additional-resources"></a>追加リソース

### <a name="platform-update-29-bug-fixes"></a>プラットフォーム アップデート 29 のバグ修正プログラム
プラットフォーム更新 29 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?kb=4515866&bugId=348252&dbType=3&qc=75eda4912fe476283a638fbb74fe1619ee8d1ac63a506b1197697c1c4693d1fc)を参照してください。

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 リリースのウェーブ 2 プラン
当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?

[Dynamics 365: 2019 リリース ウェーブ 2 プラン](/dynamics365-release-plan/2019wave2/) をご確認ください。 あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。

### <a name="removed-and-deprecated-features"></a>削除済みおよび非推奨の機能
[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md)トピックでは、削除または廃止された機能について説明します。

- *削除された* 機能は製品では使用できません。
- *削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。

製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。

コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。 通常、これらはコンパイラに加える必要がある機能の更新です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
