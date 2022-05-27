---
title: タスク管理
description: このトピックでは、Microsoft Dynamics 365 Human Resources で使用できるタスク管理機能について説明します。
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e1eb75f807d84f088cf3dd139eb094aa76618
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087220"
---
# <a name="task-management"></a>タスク管理

[!INCLUDE [PEAP](../includes/peap-1.md)]

タスク管理を使用すると、従業員の雇用 (変更)、終了 (オフボード)、および移動 (移行) 従業員に対して実行する必要があるタスクを作成できます。 タスク管理ではチェックリストの概念を使用します。 チェックリストは、オンボードとオフボード、または移行に関連するタスクの一覧です。 タスク管理では、チェックリストを使用してタスクをグループ化し、それらを個人またはグループに割り当てる必要があります。 オンボードとオフボード、および移行の変更を行う際のチェックリスト機能が似ています。

## <a name="checklist-overview"></a>チェックリストの概要

チェックリストはタスクのグループです。 チェックリストを使用すると、タスクを柔軟にグループ化し、再利用できます (追加の従業員を採用する場合など)。 チェックリストは必要な数でも作成できます。また、同じタスクを複数のチェックリストに割り当てすることもできます。

### <a name="examples"></a>例

次の例では、オンボード プロセスでチェックリストを使用する方法を示します。 ただし、オンボードとオフボード、および移行の変更を行うチェックリスト機能が類似している点から、この情報はオフボード プロセスと移行プロセスにも適用されます。

人事管理 (HR) の担当者は、オンボード プロセスの一部として、採用された従業員や最近採用された従業員のその後の問題の進捗を追跡するタスクを作成できます。 従業員の職位や地理的な場所によって、オンボード プロセスは異なる場合があります。これらの手順は、異なる採用状況に対応するために複数の役割を持つチェックリストを作成できます。

**例 1**

米国で雇用されているすべての従業員は、税の源泉徴収フォームへの記入などの作業を行う必要があります。 ただし、社用車の割り当てなどの作業は、経営幹部レベルのスタッフだけが適用できる場合があります。 この場合は、**米国を拠点とする従業員** と **経営幹部専用** の 2 つのチェックリストを作成できます。 次に、米国で中間レベルのマネージャを採用すると、**米国を拠点とする従業員** のチェックリストが選択されます。 ただし、米国で経営幹部を採用する場合は、必要なすべてのオンボード タスクの完了を確認するために両方のチェックリストが選択されます。

**例 2**

会社には、季節従業員と通常の常勤従業員の両方がいます。 一部のタスク (新しい従業員の到着時刻の確認など) は両方のタイプの従業員に適用しますが、通常の常勤従業員にのみ適用される追加のタスクがあります。 この場合、2 つのチェックリストを作成できます。 どちらのチェックリストにも、季節従業員と通常の常勤従業員の両方に適用するタスクが含まれますが、通常の常勤従業員に固有のタスクは 1 つのチェックリストにのみ含まれています。

## <a name="task-management-workspace"></a>タスク管理ワークスペース

**タスク管理** ワークスペースには、オンボード、オフボード、移行の各プロセス内の個人に割り当てられているすべてのタスクが一覧表示されます。 プロセスのタスクを表示するには、左上隅の適切なタブ (**オンボード**、**オフボード**、または **移行**) を選択します。 既定では、**タスク管理** ワークスペースには HR の担当者だけがアクセスできます。

**オンボード** タブには、新入社員を示す **もうすぐ開始** リストと、最近採用された従業員を示す **最近の採用** リストが表示されます。 どちらのリストでも、選択できる従業員は 1 人です。 従業員を選択すると、その従業員のオンボードに関連付けらたすべてのタスクがページの右側に表示されます。 **オンボード** タブには、新入社員または最近採用された従業員全員のすべてのタスクが表示される、**すべてのタスク** リストも表示されます。 最後に、タスクのリストと、現在のユーザーに割り当てられているタスクの一覧が含まれます。

**オフボード** タブには、会社を終了する従業員の一覧と、既に会社を終了している従業員の一覧が表示されます。 どちらのリストでも、選択できる従業員は 1 人です。 従業員を選択すると、その従業員のオフボードに関連付けらたすべてのタスクがページの右側に表示されます。 **オフボード** タブには、既存の従業員または退職した従業員全員のすべてのタスクが表示される、**すべてのタスク** リストも表示されます。 最後に、タスクのリストと、現在のユーザーに割り当てられているタスクの一覧が含まれます。

**移行** タブには、職位を変更する従業員、または最近職位を変更した従業員のすべてのタスクが表示される **すべてのタスク** リストが表示されます。 また、期日の過ぎたタスクのリストと、現在のユーザーに割り当てられているタスクの一覧が含まれます。

3 つのタブすべてで、HR アシスタントとマネージャーは次の活動を完了できます。

- 従業員にチェックリストを適用します。
- タスクの状態を更新します。
- タスクを再割り当てします。
- タスクの期日を更新します。

> [!NOTE]
> 既定では、**オンボード** タブには、過去 7 日間に雇用された従業員が表示されます。 この設定を変更するには、**人事管理パラメーター** ページの **全般** タブにある、**最近の採用** フィールドに概算時間を入力します。 **最近の採用** リストの情報は、特定の日数、月数、または年数で表示できます。 たとえば、過去 14 日間に採用された従業員のリストを表示するには、**期間** フィールドを **14** に、**単位** フィールドを **日数** に設定します。
>
> **人事管理パラメータ** ページでは、**オフボード** タブに表示される従業員の終了および終了の一覧の日付範囲 を更新 することもできます。
>
> これらの設定は、**担当者管理** ワークスペースにも適用されます。

## <a name="setting-up-tasks"></a>タスクの設定

タスクを個別に作成した後、複数のチェックリストで再利用できます。 タスクを作成するには、**オンボード設定** ページの **タスク** タブで、**新規** を選択します。

または、チェックリストに直接タスクを追加することもできます。 タスクをチェックリストに追加するには、**オンボード** ページの **チェックリスト** タブで、タスクを追加する新しいチェックリストを作成するか、タスクを既存のチェックリストに追加します。

> [!NOTE]
> タスクをチェックリストに直接追加した場合は、他のチェックリストで再利用することはできません。

次の表に、いずれかの方法でタスクを作成するときに使用できるフィールドを示します。

| フィールド           | Description |
|-----------------|-------------|
| タスク            | タスクの名前を入力します。 |
| Description     | タスクの説明を入力します。 |
| オプション        | タスクがオプションで、情報提供のみを行うかどうかを指定します。 |
| タスク リンク       | 外部 Web ページの URL またはユーザーがタスクを完了する必要があるアプリケーションの特定のページを入力します。 詳細については、[タスク リンク](#task-links) セクションを参照してください。 |
| 割り当てタイプ | タスクは、特定の作業者、職位、または職位のグループ、影響を受ける従業員のマネージャ (オンとオフボード、または移行のプロセスに参加する従業員)、または影響を受ける従業員に割り当てることができます。 割り当てタイプを選択します。 詳細については、[割り当てタイプ](#assignment-types) セクションをご覧ください。 |
| 割り当て先     | タスクを割り当てる特定の作業者、職位、または職位のグループを選択します。 |
| 連絡担当者  | タスクに関する質問がある場合の連絡担当者を指定します。 |
| 期限オフセット | タスクの開始予定日、終了日、または移行日の前または後の日数を指定します。 詳細については、[タスクの期日と期日オフセットフィールド](#task-due-dates-and-the-due-date-offset-field) を参照してください。 |
| 指示    | タスクを完了するための指示を入力します。 詳細については、[指示](#instructions) セクションを参照してください。 |

### <a name="task-links"></a>タスク リンク

タスク リンクは、外部 Web ページまたは Dynamics 365 アプリのページへのリンクを提供します。 タスクに割り当てられたユーザーが、特定の Web ページまたは Dynamics 365 アプリの特定のページに移動してタスクを完了する必要がある場合は、タスク リンクを指定できます。 タスク リンクを作成するときに、次のいずれかのオプションを選択できます。

- **メニュー項目** - このオプションを選択すると、Dynamics 365 アプリケーションのすべてのページの一覧が表示されます。 一覧でページを選択します。
- **URL** - このオプションを選択した場合は、タスクに割り当てられたユーザーの Web ページの URL を入力します。 指定したページは、Dynamics 365 アプリの一部ではないページです。
- **作業者の詳細** - このオプションを選択した場合は、次のいずれかのオプションを選択します。

    - **従業員セルフサービス アクション** - このオプションは、**従業員セルフサービス** で使用できるページの一覧を表示します。 関連付けされた従業員に割り当てられたタスクを **従業員セルフサービス** で完了する必要がある場合に使用します。 たとえば、従業員が自分の個人情報を入力するには、**従業員セルフサービス アクション** を選択し、**個人の詳細 &gt; 個人情報** を選択します。
    - **作業者管理アクション** - このオプションは、作業者のレコードに関連するページの一覧を表示しますが、その従業員はその説明にアクセスできないページの一覧を表示します。 たとえば、タスクの所有者に対して、報酬情報など、他の従業員に固有の情報を入力するには、**作業者管理アクション** を選択し、**報酬&gt;固定報酬** を選択します。

### <a name="assignment-types"></a>割り当てタイプ

従業員を雇用、終了、または移動した場合は、1 つ以上のチェックリストを選択できます。 チェックリストが選択され、採用、終了、または転送のプロセスが完了すると、タスクが作成され、進捗状況を追跡するためのタスクがユーザーに割り当てられます。

作成されたタスクは、特定のユーザーに割り当てられます。 タスクが割り当てられるユーザーは、そのタスクに対して選択されている割り当てタイプによって異なります。 **割り当て基準** フィールドでは、次の値を使用できます:

- **作業者** - 特定の作業者にタスクを割り当てます。 この値を選択した後、**割り当て先** フィールドで作業者を選択します。
- **職位** - 特定の職位にタスクを割り当てます。 この値を選択した後、**割り当て先** フィールドで職位を選択します。

    たとえば、IT エンジニアは、常に新しい従業員用のラップトップを準備する責任を負います。 この場合、このラップトップの構成タスクを作成するときは、割り当てタイプとして **職位** を選択し、職位として **IT エンジニア** を選択します。 次に、従業員を雇用し、チェックリストを割り当てると、採用アクションが入力された時点でITエンジニアの職位にいます。どの作業者にでもラップトップの構成タスクが割り当てられます。

- **グループ** - 職位のグループ (割り当てグループ) にタスクを割り当てます。 この値を選択した後、**割り当て先** フィールドでグループを選択します。 詳細については、[割り当てグループの設定 (オプション)](#setting-up-assignment-groups-optional) を参照してください。
- **管理者** - 雇用、終了、または異動した従業員のマネージャにタスクを割り当します。

    > [!IMPORTANT]
    > チェックリストが適用されている場合、現在、雇用された従業員、終了済、または異動した従業員に職位が割り当てられていない場合、マネージャは決定できません。 この場合、タスクはチェックリストの所有者に割り当てられます。 詳細については、[チェックリストの設定](#setting-up-checklists) セクションを参照してください。

- **従業員** - 雇用、終了、または異動する従業員を割り当てます。

### <a name="task-due-dates-and-the-due-date-offset-field"></a>タスク期日と期日オフセット フィールド

タスク期日は、雇用の開始日、終了日、または移行日に基づいて指定されます。 一部のタスクは従業員の開始日より前に完了する必要があります。他のタスクはそれ以降に完了できます。 タスク定義する場合は、**期日オフセット** フィールドを選定して、開始日、終了日、または切り替え日に関連する期日を指定します。 たとえば、IT エンジニアは、新しい従業員の開始日の 2 日前にラップトップを準備する必要があります。 この場合は、ラップトップ構成タスクを作成するときに、**期日オフセット** フィールドを **-2** に設定します。 その後、従業員の開始日が 5 月 5 日の場合、タスクの期限は 5 月 3 日になります。

> [!NOTE]
> 期日は、タスクが作成された後にも調整できます。

期日は、チェックリストに関連付けられているカレンダーに基づいて計算されます。 詳細については、[チェックリストの設定](#setting-up-checklists) セクションを参照してください。

### <a name="instructions"></a>指示

複雑なタスクには、複数のステップが必要な場合や、タスクを実行する人が追加情報を提供する必要のある場合があります。 **手順** フィールドに、タスクを完了するように割り当てられた担当者をサポートするための指示や追加情報を入力できます。

## <a name="setting-up-checklists"></a>チェックリストの設定

チェックリストはタスクのグループです。 チェックリストは必要な数でも作成できます。また、同じタスクを複数のチェックリストに割り当てすることもできます。 チェックリストを作成する場合は、所有者とカレンダーを指定します。

タスクの **割り当てタイプ** フィールドが **職位**、**マネージャー** または **グループ** に設定されている一方で、特定のユーザーを割り当てタイプから派生できる場合、タスクはチェックリストの所有者に割り当てられます。 チェックリストの所有者にタスクが割り当てられる状況の例を次に示します。

- 採用されたまたは雇用終了した従業員には職位は割り当てられません。 その従業員には職位の割り当てがないので、かれらの管理者は決定できません。
- **割り当てタイプ** フィールドは **職位** に設定されますが、タスクの作成時に職位に従業員が割り当てられていない場合。 たとえば、**ラップトップの設定** タスクは、職位番号 000876 (**技術サポートのスペシャリスト**) に割り当てられます。 従業員を採用した時点で、職位 000876 には従業員は割り当てられていません。 このため、チェックリストの所有者に対してタスクが作成されます。
- **割り当てタイプ** フィールドは **グループ** に設定されますが、タスクの作成時にそのグループには従業員が割り当てられていません。

チェックリストに指定されているカレンダーは、チェックリストに含まれるタスクの期日の計算に使用されます。 作業日および非作業日は、カレンダーの設定で定義されます。 作業日はタスクの期日が計算される際に含まれるので、非作業日は除外されます。 非作業日には、週末と休日が含まれます。 

カレンダーが設定された後、チェックリスト テンプレートに関連付けることができます。 同様の方法で、チェックリスト内のすべてのタスクの期日が計算されます。 複数のカレンダーを設定できますが、各チェックリストに関連付けできるのは 1 つのカレンダーのみです。

## <a name="setting-up-assignment-groups-optional"></a>割り当てグループの設定 (オプション)

ある個人グループがあるタスクの担当である場合があります。 たとえば、IT 作業者のグループが、新規採用用のラップトップを準備する責任がある場合があります。

割り当てグループを設定sるには、次の手順に従います。

1. **グループ割り当て** ページで、**新規** を選択します。
1. グループに名前 (**IT ラップトップ** など) と説明を入力します。
1. **保存** を選択します。
1. **メンバー** クイック タブで、**追加** を選択します。
1. **職位** フィールドで、タスクを担当するすべての職位を選択します。

割り当てグループを作成したら、タスクの作成時に割り当てグループを選択できます。 タスクの特定のグループを選択するには、**割り当てタイプ** で **グループ** を選択する必要があります。 作成したグループを **割り当て先** フィールドでの選択に使用できます。

> [!IMPORTANT]
> タスクがグループに割り当てられている場合、そのグループの 1 人のユーザーがタスクを完了すると、そのタスクは **完了** とマークされます。 タスクは、雇用、終了、または移行の時点で作成されます。 グループに含まれる職位に割り当てられているユーザーに対して作成されます。

## <a name="setting-up-task-groups-optional"></a>タスク グループの設定 (オプション)

オンボード、オフボード、または移行プロセスには、多くのタスクが含まれます。 必要なすべてのタスクをチェックリストに割り当てやすくするために、オプションの作業グループを作成して関連タスクを分類できます。 たとえば、HR、IT、給与の各部門は、新しい従業員を採用するために固有のタスクを完了する必要があります。 このため、次のタスクグループを作成できます: **HR**、**IT**、**給与**。 その後、タスクを作成するときに、それらの作業グループの 1 つをタスク グループに関連付けできます。

チェックリストにタスクを追加する場合は、目的のタスクが割り当てられている作業グループによってタスクの一覧をフィルタ処理できます。 たとえば、チェックリスト テンプレートを作成するときに、**IT** 作業グループに割り当てられている IT タスクのみを表示するために一覧をフィルタ処理することができます。 したがって、関連する IT タスクのみを選択できます。

## <a name="using-checklists"></a>チェックリストの使用

作業者が雇用、終了、または移動した場合は、1 つ以上のチェックリストを選択できます。 作業期日および作業者の割り当ては、採用、終了、または移行のプロセスの完了後に作成されます。 たとえば、**雇用** または **雇用して詳細を追加** ボタンを選択すると、タスクは割り当てタイプに基づいて個人に作成されます。

従業員の開始日からの期日相殺を加算または減算することで、各タスクに期日が割り当てられます。 詳細については、[タスクの期日と期日オフセットフィールド](#task-due-dates-and-the-due-date-offset-field) を参照してください。

人員アクションを使用している場合は、**完了** ボタンが選択された場合、またはアクションが承認されるとタスクが作成されます。

**タスク管理** ワークスペースで、簡易なリスト ページまたは詳細ページで従業員を選択し、チェックリストの適用を選択することで、従業員に **チェックリストを適用** できます。 **目標期日** フィールドの値は、タスクの期日の計算に使用されます。 通常、目標期日は従業員の雇用、終了、または移行日と一致する必要があります。

従業員にチェックリストを適用するには、**作業員** ページを開き、メニューで **チェックリスト** を選択します。

## <a name="completing-tasks"></a>完了済みのタスク

**従業員セルフサービス** ページで、従業員に割り当てられているすべてのタスクを表示できます。 割り当てられた各タスクの場合、**タスク**、**説明**、**指示**、**連絡担当者** の値が表示されます。 また、各タスクについて、従業員は Dynamics 365 アプリケーションで関連付けられている外部 Web ページまたは関連付けられたページを開くできます。

タスクは、**進行中**、**キャンセル済**、または **完了** としてマークすることができます。 タスクがグループに割り当てられていた場合、そのグループの 1 人のユーザーがタスクを完了すると、そのタスクは **完了** とマークされます。

タスクを再割り当てすることもできます。