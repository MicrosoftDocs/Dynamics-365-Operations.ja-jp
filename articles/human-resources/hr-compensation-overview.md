---
title: 報酬プラン
description: 報酬と給付金マネージャーは、報酬管理を使用して、組織の従業員の固定報酬プランおよび変動報酬プランを管理し、処理できます。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1b2494ac717bc8c0171be49cc39e6aefff4425ab
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009727"
---
# <a name="compensation-plans"></a>報酬プラン

報酬と給付金マネージャーは、報酬管理を使用して、組織の従業員の固定報酬プランおよび変動報酬プランを管理し、処理できます。

### <a name="introduction"></a>はじめに

基準賃金と報奨を管理するには、報酬管理を使用します。 従業員の固定基準賃金および昇給は固定報酬プランで管理されます。 インセンティブ支払 (賞与の支払、業績報奨、ストック オプション、付与など) の支払および一時報奨は変動報酬プランで管理します。 

従業員は、両方のタイプの 1 つまたは複数のプランに登録することができます。 従業員は、報酬プランの登録対象となるには、次の要件を満たす必要があります。
-   従業員は、有効な職位割り当てが必要です。
-   従業員は、報酬プランの適格性ルールで定義された基準を満たす必要があります。

## <a name="compensation-setup"></a>報酬の設定
次の表に、会社の報酬プランの設定で不可欠な報酬プロセスのコンポーネント一覧を示します。

<table>
<thead>
<tr class="header">
<th>コンポーネント</th>
<th>詳細</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>固定報酬アクション</td>
<td>固定報酬アクションには 2 つの目的があります。
<ul>
<li>アクションで、従業員の報酬が変更されたときに記録する必要のある情報の種類を指定できます。 たとえば、昇給や降給などの変更と理由を記録するよう要求できます。</li>
<li>アクションによって、固定報酬プランが処理されるときの計算を適用することを確認できます。  たとえば、株主資本タイプのアクションでは、従業員のレベルの最小基準点と従業員への支払を比較し、従業員が最低限以上の給料を受け取っていることを確認します。</li>
</ul></td>
</tr>
<tr class="even">
<td>レベル</td>
<td>レベルは、ジョブと、ジョブ参照に関連付けられた職位に関連付けられます。 3 種類の報酬プラン (等級、バンド、ステップ) について、それぞれ異なるレベルを作成できます。</td>
</tr>
<tr class="odd">
<td>給与レンジ到達割合マトリックス</td>
<td>給与レンジ到達割合マトリックスでは、従業員を標準職務給に移行させることができます。 給与レンジ到達割合を使用して、各従業員の業績や会社全体の業績に関係のない、社内の支払レートの株式資本を管理することもできます。 たとえば、給与レンジの低い従業員は、給与レンジの高い従業員よりも高い昇給率が割り当てられます。 これにより、体系的に資本の差額を相殺できます。 給与レンジ到達割合は、"固定支払レート - 範囲の最低額 / 範囲の最高額 - 範囲の最低額" として計算されます。</td>
</tr>
<tr class="even">
<td>基準点設定</td>
<td>基準点設定には、マトリックスの範囲を構成する基準点のセットが含まれます。 それぞれの範囲は、支払レートに関連付けることができます。 たとえば、等級プランには、よく平均、最小および最大の基準点があります。</td>
</tr>
<tr class="odd">
<td>報酬マトリックス</td>
<td>報酬マトリックスは、報酬構造の作成に使用する基準点およびレベルのセットです。</td>
</tr>
<tr class="even">
<td>報酬構造</td>
<td>報酬構造は、各レベルの基準点に関連付けられている支払レートを持つ報酬マトリックスです。</td>
</tr>
<tr class="odd">
<td>適格性ルール</td>
<td>適格性ルールは、特定のジョブ、ジョブ機能、ジョブ タイプ、部門、労働組合、または特定の報酬プランの対象になる報酬場所で従業員を識別するために使用されます。 プランに従業員を登録するために、変動報酬プランと固定報酬プランの両方に対して適格性ルールを作成する必要があります。 報酬プランの適格性ルールを指定したら、そのプランの対象になるジョブに適用するレベルを定義できます。</td>
</tr>
<tr class="even">
<td>支払頻度</td>
<td>支払頻度は、報酬に指定される期間の定義に使用されます。  たとえば、支払頻度は、報酬額が年間給与または時給レートで指定されているかを把握することに役立ちます。 支払頻度は、換算率の設定にも使用され、支払頻度を月、週、隔週、および時間から年に変換できます。</td>
</tr>
<tr class="odd">
<td>報酬地域</td>
<td>報酬場所は、作業場所に基づいて従業員の報酬を指定するために使用されます。</td>
</tr>
<tr class="even">
<td>標準職務給</td>
<td>標準職務給は、ある報酬レベルにおける、すべての従業員に対して最適だと考える支払レートを定義します。 通常、段階的なプラン構造の場合、範囲の中間点が標準職務給になります。 バンド構造では、標準職務給はほとんど使用されません。 [固定報酬プラン] フォームで、固定報酬プランの標準職務給を指定できます。</td>
</tr>
<tr class="odd">
<td>ジョブ機能</td>
<td>職務権限は、特定の職務に対する報酬プランの分類やフィルタ処理に使用されます。</td>
</tr>
<tr class="even">
<td>ジョブ タイプ</td>
<td>ジョブ タイプは、特定の職務に対する報酬プランの分類やフィルタ処理に使用されます。</td>
</tr>
<tr class="odd">
<td>変動報酬タイプ</td>
<td>株式付与や賞金ボーナスなどの変動報酬タイプは、変動報酬プランで設定されます。</td>
</tr>
<tr class="even">
<td>報酬グリッド</td>
<td>報酬グリッドには、報酬構造が含まれます。  報酬グリッドは、1 つ以上の報酬プランで使用できます。</td>
</tr>
<tr class="odd">
<td>業績計画</td>
<td>業績計画を使用して業績を配賦マトリックスに関連付けると、業績計画を能力給戦略で使用できるようになります。</td>
</tr>
<tr class="even">
<td>業績評価</td>
<td>業績評価は、業績計画で昇給や業績報奨の金額を決定するために使用されます。</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>プロセス イベント
プロセス イベントでは、1 つ以上の固定報酬プランまたは変動報酬プランに登録されるすべての従業員の、特定の期間の報酬情報を計算します。 計算した報酬結果をテストしたり更新したり場合に、プロセス イベントを繰り返し実行できます。

<a name="compensation-events"></a>報酬イベント
-------------------

プロセス イベントを実行するたびに、報酬イベントが作成されます。  報酬イベントには、そのプロセス イベントに含まれる各従業員の報酬プロセスの結果が含まれます。  計算が正しい場合、プロセス イベントによって影響を受ける従業員の報酬レコードを更新するために、報酬イベントを読み込むことができます。

## <a name="recommendations"></a>推奨事項
プロセス イベントを実行した後、プロセス イベントの計算された規定に基づいて従業員の昇給または報奨の金額の調整を認定できます。 従業員の認定を行うには、報酬プランの設定時またはプロセス イベントの設定時に認定を有効にする必要があります。


