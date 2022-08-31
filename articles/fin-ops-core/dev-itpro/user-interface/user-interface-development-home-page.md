---
title: ユーザー インターフェイス開発のホーム ページ
description: この記事には、ユーザー インターフェイス要素の開発に関するトピックへのリンクが含まれています。
author: jasongre
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: intro-internal
ms.assetid: aea345a3-2302-4b72-9887-f23f72b911f1
ms.openlocfilehash: 61e3b27ac1bdfc467fa9a8274153d9085f9a0d2d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280784"
---
# <a name="user-interface-development-home-page"></a>ユーザー インターフェイス開発のホーム ページ

[!include [banner](../includes/banner.md)]

この記事には、ユーザー インターフェイス要素の開発に関するトピックへのリンクが含まれています。

Finance and Operation アプリケーションのユーザー インターフェイスは、 Microsoft Dynamics AX 2012 のインターフェイスと大きく異なります。 Dynamics AX 2012 のクライアントは、ActiveX、WinForm、または WPF コントロールを使用する拡張機能を備えた Microsoft Win32 アプリケーションです。 X++ アプリケーション ロジックが、フォーム メソッドおよびテーブル メソッドに対してクライアントで実行され、何らかのロジックがサーバー上で発生します。 コントロールについては、X++ ロジック アプリケーション プログラミング インターフェイス (API) および現物 Win32 コントロールの両方が、クライアントで密に接続されます。 クライアントは、すべての主要なブラウザーで動作する HTML Web クライアントです。 これらのブラウザーには、Microsoft Edge、Internet Explorer 11、Chrome、および Safari が含まれます ([システム要件](../../fin-ops/get-started/system-requirements.md) を参照)。 Web クライアントへの移行により、クライアントのフォームとコントロールに以下の変更が加えられました。

-   フォームとコントロールの物理的な表現は、現在は、ブラウザー内の HTML、JavaScript、および CSS です。
-   フォーム コントロールは、論理的および物理的な部分に分割されます。 X++ 論理 API および関連する状態は、サーバーで実行されます。
-   論理的部分と物理的部分は、それぞれの側から変更を伝えるサービス コールによって同期されています。 たとえば、クライアントのユーザー アクションは、すぐに送信されるまたは後で送信されるようにキューに入れられるかのいずれかであるサーバーへのサービス コールを作成します。
-   サーバー層は、フォームが開いている間にフォーム状態をメモリーに保持します。

フォーム メタモデルは、コントロールとアプリケーション ロジックを定義するために引き続き使用されます。 この方法は、ほとんどすべての既存の Form、Form DataSource、および Form Control のメタモデルと X++ のオーバーライドメソッドをサポートしています。 ただし、新しいプラットフォームでの互換性またはパフォーマンス上の理由から、一部のコントロール タイプ、プロパティ、およびオーバーライド メソッドは削除されました。 たとえば、ActiveX および ManagedHost コントロールは、HTML プラットフォームと互換性がないため、カスタム コントロールを追加するためには使用できなくなります。 代わりに、新しい拡張可能コントロール フレームワークが追加され、さらにコントロールを追加できます。

## <a name="tutorials"></a>チュートリアル
-   [レンタル料金のタイプ フォームの構築](build-rental-charge-type-form.md)
-   [顧客フォームの構築](build-customer-form.md)

## <a name="forms"></a>フォーム
-   [ナビゲーション概念](page-navigation.md)
-   [Web クライアントのページ レイアウト](page-layout.md)
-   [Dynamics Symbol フォント](symbol-font.md)
-   [カスタム パターンを使用するテスト フォーム](testing-forms-custom-patterns.md)

## <a name="controls"></a>コントロール
-   [アクション コントロール](action-controls.md)
-   [入力コントロールとグリッド列のサイズ](sizing-input-controls-grid-columns.md)
-   [ツリー コントロールでのチェック ボックスのサポート](check-box-tree-controls.md)
-   [フィルター処理のオプション](filtering.md)
-   [[新しいウィンドウで開く] アイコンを使用してページを並べて表示する](../../fin-ops/get-started/display-pages-side-by-side.md)
-   [コードの移行 - コンテキスト メニュー コード](../migration-upgrade/code-migration-context-menus.md)
-   [コードの移行 - マウス ダブルクリック ロジック](../migration-upgrade/code-migration-double-click.md)
-   [ルックアップのコンテキスト データ入力](contextual-data-entry-lookups.md)
-   [HierarchyViewer コントロール](hierarchy-viewer-control.md)
-   [ルックアップ コントロール](lookups-controls.md)
-   [ファイルのアップロード コントロール](file-upload-control.md)
-   [システム定義ボタン](system-defined-buttons.md)
-   [ページまたはグリッドの画像](images-form-grid.md)
-   [入力、テーブル、およびグリッド コントロール用のフォントと背景](specify-color-font-background-controls.md)
-   [右から左へ読み書きする言語のサポートと双方向のテキスト](bidirectional-support.md)
-   [ワークスペース タイル用のアイコンの作成](create-icons-workspace-tiles.md)
-   [拡張可能なコントロールのためのキーボード ショートカット](keyboard-shortcuts-controls.md)
-   [拡張可能なコントロール – パブリック JavaScript API](public-javascript-apis.md)

## <a name="messaging"></a>メッセージング
-   [スライダーとメッセージ ボックス](slider-messagebox.md)
-   [メッセージング API: メッセージ センター、メッセージ バー、およびメッセージ詳細](messaging-api-center-bar-details.md)
-   [ユーザーにメッセージを送信する](messaging-user.md)

## <a name="form-pattern-guidelines"></a>フォーム パターンのガイドライン
-   [フォーム パターンの選択](select-form-pattern.md)
-   [フォームのスタイルとパターン](form-styles-patterns.md)
-   [フォーム パターン アドイン](form-pattern-add-ins.md)

| フォーム パターン     | フォーム パターンのサポート       | サブ パターン      |
|---|---|---|
| [詳細マスター](details-master-form-pattern.md)<br>[詳細トランザクション](details-transaction-form-pattern.md)<br>[フォーム パート セクション リスト](section-list-form-pattern.md)<br>[リスト ページ](list-page-form-pattern.md)<br>[簡易詳細](simple-details-form-pattern.md)<br>[簡易リスト](simple-list-form-pattern.md)<br>[簡易リストと詳細](simple-list-details-form-pattern.md)<br>[目次](table-of-contents-form-pattern.md)<br>[タスク シングル](task-single-form-pattern.md)<br>[タスク ダブル](task-double-form-pattern.md)<br>[ウィザード](wizard-form-pattern.md)<br>[ワークスペース](workspace-form-pattern.md)<br>[フォームの全般的なガイドライン](general-form-guidelines.md) | [高度な選択](advanced-selection-form-pattern.md)<br>[ダイアログ](dialog-form-pattern.md)<br>[ドロップ ダイアログ](drop-dialog-form-pattern.md)<br>[ルックアップ](lookup-form-pattern.md)<br>[情報ボックス](factbox-form-patterns.md) | [カスタム フィルター グループ](custom-filter-group-subpattern.md)<br>[分析コード エントリ コントロール](../financial/dimension-entry-control-subpattern.md)<br>[分析コード式ビルダー](../financial/dimension-expression-builder-subpattern.md)<br>[フィールドおよびフィールド グループ](fields-field-groups-subpattern.md)<br>[フィルターおよびツールバー](filters-toolbar-subpattern.md)<br>[テキスト入力](fill-text-subpattern.md)<br>[水平フィールドおよびボタン グループ](horizontal-fields-buttons-group-subpattern.md)<br>[画像のプレビュー](image-preview-subpattern.md)<br>[リスト パネル](list-panel-subpattern.md)<br>[入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md)<br>[セクション グラフ](section-chart-form-pattern.md)<br>[セクション Power BI](section-powerbi-subpattern.md)<br>[セクション関連リンク](section-related-links-subpattern.md)<br>[セクション積み上げグラフ](section-stacked-chart-subpattern.md)<br>[セクション タブ付きリスト](section-tabbed-list-subpattern.md)<br>[セクション タイル](section-tiles-subpattern.md) [表形式フィールド](tabular-fields-subpattern.md)<br>[ツールバーおよびリスト](toolbar-list-subpattern.md)<br>[ツールバーおよびフィールド](toolbar-fields-subpattern.md)<br>[ワークスペース フィルター グループ](workspace-filter-group-subpattern.md) |

## <a name="control-extensibility"></a>コントロールの拡張機能
-   [拡張可能コントロールの構築](build-extensible-control.md)
-   [拡張可能なコントロールのプログラミング リファレンス](extensible-control-programming-reference.md)
-   [コントロールの拡張機能](control-extensibility.md)
-   [ローカライズ可能なラベルの作成](create-localizable-labels-client.md)
-   [拡張可能なコントロール レイアウトのガイドライン](extensible-controls-layout.md)
-   [コントロールに対してタスク レコーダーが生成するテキストの制御](task-recorder-control-text.md)








[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
