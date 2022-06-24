---
title: Supply Chain Management の価格決定エンジンとのオンデマンド同期
description: この記事では、Microsoft Dynamics 365 Sales から Microsoft Dynamics 365 Supply Chain Management の価格決定エンジンを使用する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 259bdd5f868945c3857b045fbd3cbd4fceb26951
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862222"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Supply Chain Management の価格決定エンジンとのオンデマンド同期

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Managementには、売買契約、価格リスト、顧客ロイヤルティ プログラム、プロモーション、および割引を処理する価格決定エンジンが含まれています。 価格決定エンジンでは、複雑なルールを使用して、特定の見積または注文に対して最適な価格を決定します。 二重書き込みを使用する場合は、Microsoft Dynamics 365 Sales の **見積書** と **注文** ページで、Supply Chain Management からの静的な価格または価格設定エンジンのいずれかを使用します。

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Sales の Supply Chain Management からの価格決定エンジンを使用する

1. Sales で、**販売\>注文** に移動します。
1. 新規注文を作成するには **新規** を選択するか、**自分の注文** リストから既存の注文を選択します。
1. 新しい注文明細行を追加します。
1. 新しい注文を作成する場合は、アクション ウィンドウで **価格注文** を選択します。 既存の注文を更新する場合は、アクション ウィンドウで **再計算** を選択します。
1. 以下の列は、自動入力されます。

    - 詳細金額
    - 割引率
    - 割引
    - 送料を差し引いた金額
    - 送料
    - 税合計
    - 合計金額

> [!NOTE]
> 見積を作成するときに同様のプロセスが適用されます。

## <a name="how-it-works"></a>この機能の動作

Salse で注文を作成すると、その注文は Sales に入力した値を使用して直ちに Supply Chain Management に同期されます。 Sales で **価格注文** または **価格見積** を選択すると、Supply Chain Management は、Supply Chain Management で定義された契約ルールに基づいて、各注文明細行の価格と注文合計が計算されます。 新しく計算された値は、Sales に同期されます。

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Supply Chain Management での契約評価オプションの設定

Supply Chain Management を構成して、Sales で作成された注文の価格を計算する際に契約の点数を無視するように設定できます。 このオプションを設定するには、次の手順に従います。

1. Supply Chain Management 環境にサインインします。
1. **売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。
1. **価格** タブの **取引契約評価** クイック タブで、必要に応じて **手動入力** ポリシーの行を追加または削除します。 このポリシーの有無によって、Supply Chain Management の価格決定エンジンによって、Sales に入力された販売価格が自動的に変更するかどうかが制御されます。

    - **契約評価** 設定に **手動入力** ポリシーが存在 *しない* 場合、Supply Chain Management は価格マスターになります。 ユーザーが Sales のアクション ウィンドウで **価格注文** または **価格見積** を選択すると、Supply Chain Management の価格決定エンジンが呼び出され、Supply Chain Management で計算される販売価格と等しい場合を除き、Sales に入力された販売価格が上書きされます。
    - **売買契約評価** 設定に **手動入力** ポリシーが存在 *しない* 場合、Sales は価格マスターになります。 Sales に入力された販売価格は、ユーザーが Sales のアクション ウィンドウで **価格注文** または **価格見積** を選択しても自動的に上書きされることはありません。
    - Sales の **単位ごとの価格** および/または **割引** の値が *0 (ゼロ)* の注文明細行および見積明細行は、特別なケースとして処理されます。 該当する契約価格がある場合は、**売買契約評価** 設定に関係なく、Supply Chain Management が *常に* これらのフィールドに適用されます。

    これらのケースの例については、次のシナリオを参照してください。

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>シナリオ例 1: 手動入力オプションなしの売買契約評価

このシナリオでは、Supply Chain Management の **売買契約評価** 設定は、**手動入力** ポリシーを含み *ません*。 Sales ユーザーは、Salse にゼロ以外の販売価格を持つ注文明細行を入力し、Supply Chain Management の品目に販売価格が定義されていません。

1. Sales では、ユーザーが 1 米国ドルの **単位ごとの価格** を持つ注文明細行を作成します。
1. この注文明細行は、1 米国ドルの販売価格を持つ Supply Chain Management と同期されます。
1. Sales で、ユーザーはアクション ウィンドウ で **価格注文** を選択します。
1. Supply Chain Management は、関連する価格と割引を検索した後、合計を計算します。 この品目は Supply Chain Management に販売価格を持たないので、この計算はその品目の販売価格が 0 米国ドルになるように更新されます。
1. その明細行の新しい販売価格は、Sales に同期されます。
1. その結果、Salse の注文明細行は 0 米国ドルの販売価格を持つようになります。

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>シナリオ例 2: 手動入力オプションを使った売買契約評価

このシナリオでは、Supply Chain Management の **売買契約評価** 設定は、**手動入力** ポリシーを含み *ません*。 Sales のユーザーは、Salse にゼロ以外の販売価格を持つ注文明細行を入力します。 Supply Chain Management には、注文品目に対して販売価格を 2 米国ドルと設定する売買契約が含まれています。

1. Sales では、ユーザーが 1 米ドルの **単位ごとの価格** を持つ品目の注文明細行を作成します。
1. この注文明細行は、1 米国ドルの販売価格を持つ Supply Chain Management と同期されます。
1. Sales で、ユーザーはアクション ウィンドウ で **価格注文** を選択します。
1. Supply Chain Management の **売買契約評価** 設定には **手動入力** ポリシーが含まれるため、該当する契約で別の販売価格が指定されている場合でも、販売価格の変更は行されません。
1. Sales および Supply Chain Management でも、販売価格は変わりません。

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>シナリオ例 3: Sales で販売価格がゼロの品目に対する売買契約評価

このシナリオでは、Supply Chain Management の **売買契約評価** 設定は、**手動入力** ポリシーを含み *ません*。 Sales のユーザーは、Salse で 0 (ゼロ) 以外の販売価格を持つ注文明細行を入力します。 Supply Chain Management には、注文品目に対して販売価格 2 米国ドルと設定する売買契約が含まれています。

1. Sales では、ユーザーは **出荷単位ごとの価格** の値が 0 米国ドルで 0 米国ドルの **明細行割引** の注文明細行を作成します。
1. この注文明細行は、0 米国ドルの販売価格を持つ Supply Chain Management と同期されます。
1. 販売価格が 0 (ゼロ) の注文明細行を受け取ったので、**手動** 入力オプションが有効な場合でも、Supply Chain Management はその価格決定エンジンが呼び出されます。 価格決定エンジンは、契約で決定された2 米国ドルの販売価格を返品し、Supply Chain Management の注文明細行を更新します。
1. 更新された販売価格の売上は、まだ Sales の注文明細行に同期されていません。
1. Sales で、ユーザーはアクション ウィンドウ で **価格注文** を選択します。
1. Supply Chain Management の注文明細行は 2 米国ドルの販売価格を維持し、それはここで Sales に同期されます。 したがって、Sales の販売明細行の **単位ごとの価格** は、0 米国ドルから 2 米国ドルに更新されます。
1. Salse では、ユーザーは  0.50 米国ドルの新しい **明細行割引** を入力します。 Sales では、明細行の **増額** が 1.50 米国ドルを計算するようになりました。
1. この注文明細行は、0 50 米国ドルの **明細行割引** 額で Supply Chain Management と同期されます。
1. Sales で、ユーザーはアクション ウィンドウ で **価格注文** を選択します。
1. Salse の注文、注文明細行の価格や割引は変更されません。

## <a name="limitations"></a>制限

Sales の列が入力されている場合は、次の制限事項が適用されます。

- Supply Chain Management での請求金額と請求金額配賦の設定は、Sales ではレプリケートされません。
- 価格決定では、Supply Chain Management の販売注文行ページの **小売チャネル** 列で指定された特別な小売価格は考慮しません。
- Supply Chain Management の **取引手当管理** セクションで定義されている割引は考慮されません。
- 価格では販売契約が考慮されます。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
