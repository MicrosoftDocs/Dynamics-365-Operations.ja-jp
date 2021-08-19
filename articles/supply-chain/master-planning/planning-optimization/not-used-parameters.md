---
title: 計画最適化で使用されないパラメーター
description: このトピックでは、計画最適化で現在考慮されないパラメーターを一覧表示します。
author: crytt
ms.date: 6/29/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1992523ae10f30196ebe55d7c7fe6a2549a3a12853da261bd4a129523b8e4ea2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714286"
---
# <a name="parameters-not-used-by-planning-optimization"></a>計画最適化で使用されないパラメーター

[!include [banner](../../includes/banner.md)]

このトピックでは、計画最適化で現在考慮されないパラメーターを一覧表示します。 たとえば、関連する機能がまだサポートされていないため、計画サービスがパラメーターをスキップする場合があります。 また、機能が変更され、パラメーターが廃止された場合があります。

以下のセクションでは、特定のページで計画最適化により使用されないパラメーターを一覧表示します。 また、各パラメーターが使用されない理由も説明します。

## <a name="master-planning-parameters-page"></a>マスター プラン パラメーター ページ

計画最適化で、**マスター プラン パラメーター** ページの次のパラメーターやオプションは使用されません。

- **一般** タブ:

    - **現在の予測計画** – *予測* のサポートは保留中です。
    - **現在の静的マスター プラン** – *静的計画を動的計画へコピー* のサポートは保留中です。
    - **現在の動的マスター プラン** – *静的計画を動的計画へコピー* のサポートは保留中です。
    - **完全な、更新された静的マスター プランを動的マスター プランへコピー** – *静的計画を動的計画へコピー* のサポートは保留中です。
    - **計算済遅延の開始時刻** – *計算済遅延* のサポートは保留中です。
    - **動的マイナス在庫日数を使用** – 計画最適化では常に *動的マイナス在庫日数* アプローチが使用されます。
    - **今日の日付カレンダー** – *スケジューリング* のサポートは保留中です。
    - **キャッシュの使用** – Microsoft Azure サブスクリプションのコンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **ヘルパー タスク バンドル内のタスク数** – Azure サブスクリプション コンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **前処理: 直納品目で自動的にフィルター処理する** – Azure サブスクリプション コンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **後処理: 直納品目で自動的にフィルター処理する** – Azure サブスクリプション コンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **バンドル確定時の注文数** – Azure サブスクリプション コンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **スレッド数** – Azure サブスクリプション コンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **計画プロセス タイムアウト (分)** – Azure サブスクリプション コンフィギュレーションは、パフォーマンス ポイントを処理します。
    - **スケジューリングの開始時刻** – *スケジューリング* のサポートは保留中です。

- **計画オーダー** タブ:

    - **受入時刻** – *スケジューリング* のサポートは保留中です。
    - **生産** – *スケジューリング* のサポートは保留中です。
    - **プロジェクト** セクションのフィールド – *スケジューリング* のサポートは保留中です。

- **標準更新** タブ:

    - **マーキングの更新** – *確定* のサポートは保留中です。
    - **エラーが発生した場合は確定を中止** – *確定* のサポートは保留中です。
    - **仕入先ごとにグループ化** – *確定* のサポートは保留中です。
    - **購入担当者グループごとにグループ化** – *確定* のサポートは保留中です。
    - **購買契約ごとにグループ化** – *確定* のサポートは保留中です。
    - **期間ごとにグループ化** – *確定* のサポートは保留中です。
    - **購買契約の検索** – *確定* のサポートは保留中です。
    - **計画の優先順位ごとにグループ化** – *確定* のサポートは保留中です。
    - **期間ごとにグループ化** – *確定* のサポートは保留中です。

## <a name="coverage-groups-page"></a>補充グループ ページ

計画最適化で、**補充グループ** ページの次のパラメーターやオプションは使用されません。

- **全般** クイック タブ:

    - **プラス在庫日数** – *プラス在庫日数* のサポートは保留中です。
    - **手持在庫の消費** – *手持在庫の消費* のサポートは保留中です。
    - **特定の BOM またはフォーミュラ バージョンの使用** – *連産品/副産物を含むフォーミュラ バージョン* のサポートは保留中です。
    - **指定された工順バージョンの使用** – *特定の BOM またはルート要件が定義されている需要* のサポートは保留中です。

- **アクション** クイック タブ:

    - **アクション メッセージ** – *アクション* のサポートは保留中です。
    - **アクション タイム フェンス** – *アクション* のサポートは保留中です。
    - **延期日数** – *アクション* のサポートは保留中です。
    - **要求日前受入許容日数** – *アクション* のサポートは保留中です。
    - **基準日** – *アクション* のサポートは保留中です。
    - **繰り上げ** – *アクション* のサポートは保留中です。
    - **延期** – *アクション* のサポートは保留中です。
    - **減少** – *アクション* のサポートは保留中です。
    - **増加** – *アクション* のサポートは保留中です。
    - **派生アクション** – *アクション* のサポートは保留中です。

- **その他** クイック タブ:

    - **凍結タイム フェンス (日)** – 計画最適化では、*凍結タイム フェンス* のサポートは計画されていません。
    - **BOM 展開タイム フェンス (日)** – *スケジューリング* のサポートは保留中です。
    - **能力スケジューリング タイム フェンス (日)** – *スケジューリング* のサポートは保留中です。
    - **承認済要求タイム フェンス (日)** – *要求* のサポートは保留中です。
    - **予測計画タイム フェンス** – *予測* のサポートは保留中です。

- **遅延** クイック タブ:

    - **計算済遅延** – *計算済遅延* のサポートは保留中です。
    - **遅延の計算タイム フェンス (日)** – *計算済遅延* のサポートは保留中です。

## <a name="item-coverage-page"></a>品目補充ページ

計画最適化で、**品目補充** ページの次のパラメーターやオプションは使用されません。

- **一般** タブ:

    - **計画オーダータイプ** – 計画最適化では *かんばん* オプションはサポートされていません。*かんばん* のサポートは保留中です。
    - **凍結タイム フェンス (日)** – 計画最適化では、*凍結タイム フェンス* のサポートは計画されていません。
    - **BOM 展開タイム フェンス (日)** – *スケジューリング* のサポートは保留中です。
    - **能力スケジューリング タイム フェンス (日)** – *スケジューリング* のサポートは保留中です。
    - **承認済要求タイム フェンス (日)** – *要求* のサポートは保留中です。
    - **最小限実行** – 計画最適化では、*今日の日付*、*初回払出*、および *補充タイム フェンス* オプションはサポートされていません。 常に、*本日の日付 + 調達時間* オプションが使用されます。
    - **最小期間** – *最小在庫レベル* のサポートは保留中です。
    - **計画式** – *連産品/副産物を含むフォーミュラ バージョン* のサポートは保留中です。
    - **既定の優先順位** – *連産品/副産物を含むフォーミュラ バージョン* のサポートは保留中です。
    - **現在の優先順位** – *連産品/副産物を含むフォーミュラ バージョン* のサポートは保留中です。
    - **変更日付** – *連産品/副産物を含むフォーミュラ バージョン* のサポートは保留中です。
    - **手持在庫の消費** – *手持在庫の消費* のサポートは保留中です。

## <a name="master-plans-page"></a>マスター プラン ページ

計画最適化で、**マスター プラン** ページの次のパラメーターやオプションは使用されません。

- **全般** クイック タブ:

    - **手持在庫を含む** – *手持在庫の消費* のサポートは保留中です。
    - **手持の上書き** – *手持在庫の消費* のサポートは保留中です。
    - **手持在庫の消費** – *手持在庫の消費* のサポートは保留中です。
    - **在庫トランザクションを含める** – *手持在庫の消費* のサポートは保留中です。
    - **販売見積を含める** – *販売見積* のサポートは保留中です。
    - **見積依頼を含める** – *見積依頼* のサポートは保留中です。
    - **有効期限日付の使用** – *有効期限* のサポートは保留中です。
    - **連続計画を含める** – *連続スケジューリング* のサポートは保留中です。
    - **スケジューリング方法** – *スケジューリング* のサポートは保留中です。
    - **作業タイプ指定** – *スケジューリング* のサポートは保留中です。
    - **バックワード スケジューリング能力タイム フェンス** – *スケジューリング* のサポートは保留中です。
    - **有限能力** – *スケジューリング* のサポートは保留中です。
    - **有限能力タイム フェンス** – *スケジューリング* のサポートは保留中です。
    - **ボトルネック リソースに対する有限能力** – *スケジューリング* のサポートは保留中です。
    - **ボトルネック リソースに対する能力タイム フェンス** – *スケジューリング* のサポートは保留中です。
    - **計画オーダー** – 計画最適化では、固定番号順序が使用されます。
    - **セッション** – 計画最適化では、固定番号順序が使用されます。
    - **連続計画** – 計画最適化では、固定番号順序が使用されます。

- **タイム フェンス (日)** クイック タブ:

    - **凍結** – 計画最適化では、*凍結タイム フェンス* のサポートは計画されていません。
    - **展開** – *スケジューリング* のサポートは保留中です。
    - **予測計画タイム フェンス** – 追加の *予測* のサポートは保留中です。
    - **能力** – *スケジューリング* のサポートは保留中です。
    - **連続計画** – *連続スケジューリング* のサポートは保留中です。
    - **アクション メッセージ** – *アクション* のサポートは保留中です。
    - **計算済遅延** – 追加の *計算済遅延* のサポートは保留中です。
    - **優先順位** – *生産* のサポートは保留中です。

- **計算済遅延** クイック タブ:

    - **計画オーダーがマスター プランの実行日前に作成されていないことを確認する** – *計算済遅延* のサポートは保留中です。
    - **計算済遅延を要求日に追加** (**計画発注書** セクション) – *計算済遅延* のサポートは保留中です。
    - **計算済遅延を要求日に追加** (**計画製造オーダー** セクション) – *計算済遅延* のサポートは保留中です。
    - **計算済遅延を要求日に追加** (**計画移動** セクション) – *計算済遅延* のサポートは保留中です。
    - **計算済遅延を要求日に追加** (**計画かんばん** セクション) – *計算済遅延* のサポートは保留中です。

- **優先順位** クイック タブ:

    - **マスター プラン後の計画オーダーの順序付け** – *優先順位* のサポートは保留中です。
    - **バケット タイプ** – *優先順位* のサポートは保留中です。
    - **期間タイプ** – *優先順位* のサポートは保留中です。
    - **キャンペーン サイクルのバケットの数** – *優先順位* のサポートは保留中です。

## <a name="released-product-details-page"></a>リリース済製品の詳細ページ

計画最適化で、**リリース済製品の詳細** ページの次のパラメーター オプションは使用されません。

- **エンジニア** クイック タブ:

    - **生産タイプ** – 計画最適化では、*計画品目* オプションはサポートされていません。*計画品目* のサポートは保留中です。

## <a name="default-order-settings-page"></a>既定の注文設定ページ

計画最適化で、**既定の注文設定** ページの次のパラメーター オプションは使用されません。

- **在庫** クイック タブ:

    - **配送日管理** – 計画最適化では、*CTP* オプションはサポートされていません。*CTP* のサポートは保留中です。

## <a name="working-time-calendars-page"></a>作業時間カレンダー ページ

計画最適化で、**作業時間カレンダー** ページの次のパラメーターは使用されません。

- **基準カレンダー** – *基準カレンダー* のサポートは保留中です。

## <a name="batch-disposition-master-page"></a>バッチ廃棄マスター ページ

計画最適化で、**バッチ廃棄マスター** ページの次のパラメーターは使用されません。

- **設定** クイック タブ:

    - **利益あり** – *バッチ廃棄コード* のサポートは保留中です。