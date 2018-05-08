---
title: "バーコード スキャナー用かんばん転送ボードのサポート"
description: "かんばん転送ボードは、かんばん作業を選択、開始、完了、および空にするためのウィジェット バーコード スキャナーのスキャナー入力をサポートします。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a8393efd51032271d3023f1e0569425a16222cc3
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>バーコード スキャナー用かんばん転送ボードのサポート

[!include [banner](../includes/banner.md)]

かんばん転送ボードは、かんばん作業を選択、開始、完了、および空にするためのウィジェット バーコード スキャナーのスキャナー入力をサポートします。

<a name="registration-modes"></a>登録モード
------------------

**スキャナーの登録**クイック タブで登録モードを選択すると、登録モードを選択できます。これは、[かんばんカード番号] フィールドでかんばんカード番号をスキャンまたは手動入力するときのアクションを制御します。

| 登録モードの設定 | 説明                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| 開始日                 | かんばん転送ジョブを進行中として登録します。                                                 |
| 完了              | かんばん転送ジョブを完了として登録します。                                                   |
| 空                 | かんばんカードで参照される材料取り扱い単位を空として登録します。              |
| 選択                | かんばんカード番号を登録すると、自動的にかんばんリストに参照されるジョブが選択されます。 |

 
<a name="registration-mode-select"></a>[選択] の登録モード
------------------------

ジョブを選択するのにバーコードを使用する場合、かんばんボードの表示モードを変更します。 このモードでは、次の要件が適用されます:

-   スキャンしたかんばん作業のみを表示します。
-   選択したジョブの詳細は、**詳細**クイック タブに表示されます。
-   **メッセージ** クイック タブでは、選択したジョブに対してのみメッセージが表示されます。
-   [アクション ウィンドウ] で使用できる機能を使用してジョブのステータスを変更できます。 今回、かんばん転送ボードは 1 つのジョブのみを継続して表示します。
-   ジョブのリストの情報を手動で更新するには、アクション ペインの \[**更新**\] (Shift+F5) をクリックします。 情報を更新すると、ジョブのフィルターの完全な結果が再び表示されます。

## <a name="job-status-and-possible-actions"></a>ジョブ状態と実行可能なアクション
選択したジョブのステータスおよびイベントのかんばんにペギングされたジョブのステータスによって、このジョブをさらに処理するかどうかが決まります。 次の表に、これらのステータスやタスクに関する情報が表示されます。
-   ジョブに使用できるステータス、またはジョブによって参照される材料取り扱い単位のステータス。
-   ジョブに対して実行できる各タスク。

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>ジョブ タイプ</th>
<th>ジョブ ステータスまたは材料取り扱い単位ステータス</th>
<th>ピッキング リストの更新</th>
<th>開始日</th>
<th>登録の更新</th>
<th>完了</th>
<th>空</th>
<th>イベントのかんばんを作成</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>移動</td>
<td><ul>
<li>未定</li>
<li>ペギングにしたジョブがない、またはペギングにしたジョブが [完了]</li>
</ul></td>
<td>有</td>
<td>有</td>
<td>有</td>
<td>有</td>
<td>第        条</td>
<td>有</td>
</tr>
<tr class="even">
<td>移動</td>
<td><ul>
<li>未定</li>
<li>ペギングにされたジョブが [完了] ではない</li>
</ul></td>
<td>有</td>
<td>第        条</td>
<td>有</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
</tr>
<tr class="odd">
<td>移動</td>
<td>処理中</td>
<td>有</td>
<td>第        条</td>
<td>有</td>
<td>有</td>
<td>第        条</td>
<td>第        条</td>
</tr>
<tr class="even">
<td>移動</td>
<td>完了</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>有</td>
<td>第        条</td>
</tr>
<tr class="odd">
<td>転送または処理中</td>
<td>空</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
</tr>
<tr class="even">
<td>転送または処理中</td>
<td>かんばんカードがない</td>
<td>いいえ</td>
<td>いいえ</td>
<td>いいえ</td>
<td>いいえ</td>
<td>いいえ</td>
<td>いいえ</td>
</tr>
<tr class="odd">
<td>転送または処理中</td>
<td>かんばんカードはあるが、かんばんに割り当てられていない</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
</tr>
<tr class="even">
<td>処理</td>
<td><ul>
<li>未定</li>
<li>準備済</li>
<li>処理中</li>
</ul></td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
</tr>
<tr class="odd">
<td>処理</td>
<td>完了</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
<td>第        条</td>
</tr>
</tbody>
</table>






