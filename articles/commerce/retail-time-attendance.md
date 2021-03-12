---
title: Retail での時間と出勤管理
description: このトピックでは、Dynamics 365 Commerce の時間と出勤管理でサポートされているシナリオについて説明します。
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e28df09ecb592ae7df360d1b2d0bf06339c1410d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989380"
---
# <a name="time-and-attendance-management-in-retail"></a>Retail での時間と出勤管理

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce の時間と出勤管理でサポートされているシナリオについて説明します。

## <a name="manage-worker-setup-and-scheduling"></a>作業者設定およびスケジュールの管理

### <a name="initial-configuration"></a>初期コンフィギュレーション

- コンフィギュレーション ウィザードを実行します。
- 時間登録作業者としての作業者を登録します。

### <a name="plan-worker-schedules"></a>作業者のスケジュールを計画する

- ワーク プランナーを使用したプロファイルを適用します。 詳細については、 [ワーク プランナーを使用したプロファイルの適用](https://technet.microsoft.com/library/aa551234.aspx)を参照してください。

コンフィギュレーションの手順については、[時刻と出勤の設定](https://technet.microsoft.com/library/aa496971.aspx)を参照してください。

### <a name="commerce-specific-configuration"></a>コマース固有のコンフィギュレーション

- 時間登録を有効にする作業者のタイム レコーダーの機能プロファイルを有効にします。 **POS機能プロファイル** &gt; **機能** &gt; **POS 時間登録** &gt; **時間登録の有効化** をクリックします。
- 販売時点管理 (POS) のアクセス許可グループをコンフィギュレーションして、[タイム レコーダー エントリの表示] のアクセス許可を有効にします。 このアクセス許可により、ユーザーが、その店舗 (およびアドレス帳を介してユーザーが関連付けられている他のすべての店舗から) の他の作業者のタイム レコーダー登録を表示できるようにします。 レジ担当者ロールではなくマネージャー ロールに対してこのアクセス許可を有効にする場合があります。 **POS アクセス許可グループ** &gt; **タイム レコーダー エントリの表示** をクリックします。

## <a name="register-time"></a>時刻の登録

### <a name="cashier-and-non-cashier-time-registrations"></a>レジ担当者と非レジ担当者の時間登録

- POS で:

    - 出勤操作:

        - 非ドロワー操作または新しいシフトにログオンします。
        - タイム レコーダーの操作を選択します。
        - 必要な操作を選択します:

            - 出勤
            - 休憩
            - 昼休み
            - 退勤

        <table>
        <thead>
        <tr>
        <th>現在の状態</th>
        <th>使用可能な操作</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td>出勤</td>
        <td>
        <ul>
        <li>休憩</li>
        <li>昼休み</li>
        <li>退勤</li>
        </ul>
        </td>
        </tr>
        <tr>
        <td>休憩</td>
        <td>出勤</td>
        </tr>
        <tr>
        <td>昼休み</td>
        <td>出勤</td>
        </tr>
        <tr>
        <td>退勤</td>
        <td>出勤</td>
        </tr>
        </tbody>
        </table>

        [![タイム レコーダーの状態](./media/timeclockstates.png)](./media/timeclockstates.png)

- 確認メッセージを表示して、現在の活動時間が正しいことを確認します。
- ログ帳:

    - **ログ帳** をクリックして、タイム レコーダーの活動を表示します。
    - タイム フィルターを使用して、異なる時間枠を選択します。
    - 複数の店舗の場所で作業する場合、時間を記録したすべての店舗からの時間登録が表示されます。 店舗フィルターを使用して、選択した店舗からの時間登録を表示できます。

- 異なるタイム ゾーン:

    - 別の場所からの時間を表示する場合で (レジ担当者ログ帳に対して、またはマネージャーのシナリオの **タイム レコーダー エントリの表示** を使用して)、その場所が別のタイム ゾーンである場合、表示される時刻記録はローカル タイム ゾーンに変換されます。 たとえば、アリゾナとネバダの 2 つの店舗のマネージャだと仮定します。 レジ担当者は午前 9 時に アリゾナで出勤を登録します。 その時点で、ネバダの時刻は午前 8 時です。 したがって、ネバダの店舗にいて時間登録のレコードを見ている場合、時間登録は 8 A.M としてマークされます。

## <a name="view-worker-time-registrations"></a>作業者の時間登録の表示

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>作業者の時間登録を表示して、店舗または活動のタイプごとにフィルター処理をする

POS で:

- **タイム レコーダー エントリの表示** を選択します。
- あなたが割り当てられている同じ店舗に割り当てられているすべての作業者のタイム レコーダーの登録活動が表示されます。
- 活動タイプを使用して、時間登録をフィルター処理するフィルターを保存できます。

## <a name="process-and-manage-time-registrations"></a>時間登録の処理と管理

コマース ユーザーは、計算、承認および給与への時間登録の転送のためのワークフローに従います。

### <a name="primary-operations"></a>基本工程

- 計算
- 承認
- 給与に送信

### <a name="other-common-operations"></a>他の共通の操作

- 一括退勤
- 休暇の登録

時刻と出勤の登録の処理方法については、[時刻と出勤の登録を処理](https://technet.microsoft.com/library/aa573180.aspx)を参照してください。
