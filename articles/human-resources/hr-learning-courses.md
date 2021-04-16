---
title: トレーニング コースの設定
description: 人事管理の管理者とマネージャーは、作業者に提供されるトレーニングに関する情報を管理するためにコース機能を使用できます。
author: andreabichsel
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 0718987583d02a76acc2420e5a371c418757e384
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793540"
---
# <a name="set-up-training-courses"></a>トレーニング コースの設定

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

人事管理の管理者とマネージャーは、作業者に提供されるトレーニングに関する情報を管理するためにコース機能を使用できます。

 <a name="set-up-prerequisites"></a> 前提条件の設定
---------------------

次の情報は、必須でコースを作成する前に設定する必要があります。
-   **コースのタイプ**

次の情報は、コースに対して指定できるオプションの情報です。 コースのこの情報を入力することがわかっている場合は、コースのレコードを作成する前にこの情報を設定する必要があります。
-   **教室グループ**
-   **コース グループ**
-   **コースの開催場所**
-   **教室**
-   **講師**

## <a name="course-types"></a>コースのタイプ
コース構造または内容によってコースを分類するために、コース タイプを使用できます。 **コース タイプ** ページでコースのタイプを作成できます。 コースのレコードを作成するときにコース タイプを選択する必要があります。

## <a name="course-setup-type"></a>コース設定のタイプ
次の表に、コースの 3 種類の設定タイプの一覧を示します。 設定タイプによって、コースの構造が決まります。

<table>
<thead>
<tr class="header">
<th>設定タイプ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>標準</strong></td>
<td>毎日の議題がないコースのこのタイプを選択します。 これは、新しいコースを作成するときの既定の設定のタイプです。</td>
</tr>
<tr class="even">
<td><strong>議題</strong></td>
<td>複数の日数かけて実施するコースの日々の詳細を計画する場合は、このタイプを選択します。</td>
</tr>
<tr class="odd">
<td><strong>議題 + セッション</strong></td>
<td>より複雑なコースに対してこのタイプを選択します。 たとえば、追跡およびセッションにコースの議題を分割できます。
<ul>
<li><strong>トラック</strong> – トラックは、コースの特定のサブジェクト領域です。</li>
<li><strong>セッション</strong> - セッションはトラックに分割され、トラックに関連する特定プロセスまたは技術を識別できます。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>コースのタスク
コースごとに、次のタスクを実行できます。
- 参加者の登録
- 登録期限の指定
- 参加者の最小数と最大数の定義
- コースの開催場所と教室の割り当て
- コース参加者へのホテルの推奨
- コースの説明の作成 (作成後は従業員セルフ サービスで通知することが可能)

  >**注記** 登録者がいない場合のみコースを削除できます。 

## <a name="course-statuses"></a>コースのステータス
次の表に、可能なコースのステータスとコースに特定のステータスがある場合に実行するアクションを示します。

<table>
<thead>
<tr class="header">
<th>ステータス</th>
<th>アクション</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>作成済</strong></td>
<td><ul>
<li>コース情報を入力および修正します。</li>
<li>作業者がコースに登録できるように <strong>オープン</strong> にコースのステータスを変更します。</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>開始</strong></td>
<td><ul>
<li>コースの参加者を登録します。</li>
<li>コースの参加者をコースから削除します。</li>
<li>コースの参加者を確認します。</li>
<li>コースのステータスを <strong> クローズ</strong> または <strong>キャンセル</strong> に変更します。</li>
<li>ステータスが <strong>確認済み</strong> の参加者用のアンケートを計画します。</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>クローズ済</strong></td>
<td>コースを再度開くことができます。</td>
</tr>
<tr class="even">
<td><strong>キャンセル済</strong></td>
<td>コースを再度開くことができます。</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>コース参加者
コース参加者は、トレーニング コースまたはイベントに参加する作業者です。 オープン コースの参加者のみを登録できます。 コースに登録できる参加者の最小数と最大数は、**コース** ページの **全般** クイック タブで定義されます。

<a name="workflow"></a>ワークフロー
--------

**従業員セルフ サービス** ページからコースに登録する従業員は、承認のワークフローを経て登録することができます。 **コース** ページの **一般** クイック タブで、コースにワークフローを割り当てることができます。







[!INCLUDE[footer-include](../includes/footer-banner.md)]