---
title: コースの概要
description: この記事は、人事管理の管理者とマネージャーが、作業者が利用できるコースに関する情報を管理するためのコース機能を使用できる方法について説明します。
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716338"
---
# <a name="courses-overview"></a>コースの概要

Microsoft Dynamics 365 Human Resources は、組織の学習ニーズに対するソリューションを提供します。 このソリューションには、*仮想* コースと *講師主導型* という 2 つの学習コース パスが用意されています。

*仮想学習* は、オンライン リソースによって強化された学習体験です。 *講師主導* によるトレーニングでは、講師が作業者または学習者のグループに対するトレーニング セッションを円滑に行います。

当社のトレーニング モジュールでは、人事管理のプロ、管理者、トレーニング マネージャー、マネージャーたちが、両方の学習コース パスを作成して、作業者に割り当てできます。

> [!NOTE]
> 仮想コースを使用するには、機能管理の **コースの拡張機能** 機能を有効にする必要があります。

## <a name="set-up-virtual-courses"></a>仮想コースの設定

仮想コースを構成するには、機能管理の **コースの拡張機能** 機能を有効にする必要があります。 **コース \> 新規** に移動し、**仮想** オプションを **はい** に設定します。 機能が有効な後、コースのリンクが必要です。 **コースの状態** フィールドは **オープン** に設定されます。 **従業員に自己登録を許可する** オプションは **はい** に 設定されますが、**いいえ** にも設定できます。

機能管理で **コースの拡張** 機能が有効になると、次の変更が行われます。

- コースの割り当てには期限を定義する必要があります。
- コース のリンクが必要です。
- **従業員セルフサービス** では、**コース** に従業員の概要が表示されます。 ユーザーは、期限が過ぎたコース、間近に期日が来て、割り当てられたコースを表示できます。
- 従業員は仮想コースを修了し、自己テストを行うことができます。

## <a name="set-up-instructor-led-courses"></a>講師主導型コースの設定

講師主導型コースは、使用する前に構成する必要があります。

次の情報は、オプションでコースに対して指定できます。 この情報がコースに対して入力される場合は、コース レコードを作成する前に設定する必要があります。

- コースのタイプ
- 教室グループ
- コース グループ
- コースの開催場所
- 教室
- 講師
- コースのタイプ

コース構造または内容によってコースを分類するために、*コース タイプ* を使用できます。  **コース タイプ**  ページでコースのタイプを作成できます。

コースに登録できる参加者の最小数と最大数は、 **コース**  ページの  **全般**  クイック タブで定義されます。

### <a name="course-setup-type"></a>コース設定のタイプ 

*設定タイプ* によって、コースの構造が決まります。 コースには 3 つの設定タイプがあります。

| 設定の種類 | Description |
|------|--------|
| 標準 | この設定タイプのコースには、毎日の議題は含めではありません。 これは、新しいコースを作成するときの既定の設定のタイプです。 |
| 議題 | 複数の日数かけて実施するコースの日々の詳細を計画する場合は、この設定タイプを選択します。 |
| 議題 + セッション | <p>より複雑な設定コースに対してこのタイプを選択します。 たとえば、*追跡* および *セッション* にコースの議題を分割できます。</p><ul><li>*トラック* は、コースの特定のサブジェクト領域です。</li><li>*セッション* はトラックに分割され、トラックに関連する特定プロセスまたは技術を識別できます。</li></ul> |

### <a name="course-tasks"></a>コースのタスク

コースごとに、次のタスクを完了します。

- 参加者の登録。
- 登録期限の指定。
- 参加者の最小数と最大数の定義。
- コースの開催場所と教室の割り当て。
- コース参加者へのホテルの推奨。
- コースの説明の作成 (作成後は  **従業員セルフ サービス** で通知)。

> [!NOTE]
> 登録者がいない場合のみコースを削除できます。

### <a name="course-statuses"></a>コースのステータス

次の表に、コースの状態と、それぞれのアクションの一覧を示します。

| Status | アクション |
|------|--------|
| 作成済み | <ul><li>コース情報を入力および修正します。</li><li>作業者がコースに登録できるように  **オープン** にコースのステータスを変更します。</li></ul> | 
| 未完了 | <ul><li>コースの参加者を登録します。</li><li>コースの参加者をコースから削除します。</li><li>コースの参加者を確認します。</li><li>コースの状態が、 **確認済み** のステータスの参加者に対して  **クローズ**  または  **キャンセル済み** に変更します。</li></ul>|
| 終了した | コースを再度開くことができます。 |
| キャンセル済み | コースを再度開くことができます。 |

### <a name="course-participants"></a>コース参加者

*コース参加者* は、トレーニング コースまたはイベントに参加する作業者です。 オープン コースの参加者のみを登録できます。

### <a name="workflow"></a>ワークフロー

 **従業員セルフ サービス**  ページからコースに登録する従業員は、承認のワークフローを経て登録することができます。  **コース**  ページの  **一般**  クイック タブで、コースにワークフローを割り当てることができます。