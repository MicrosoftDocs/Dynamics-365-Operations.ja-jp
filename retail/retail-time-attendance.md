---
title: "小売タイムと出勤"
description: "このトピックでは、]、Microsoft Dynamics 365の時間と出席管理でサポートされているシナリオについて説明します。"
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: eac0b85a17df33c860333c5c19d4fb58f160930f
ms.lasthandoff: 03/31/2017


---

# <a name="retail-time-and-attendance"></a>小売タイムと出勤

このトピックでは、]、Microsoft Dynamics 365の時間と出席管理でサポートされているシナリオについて説明します。 

<a name="manage-worker-setup-and-scheduling"></a>ために設定およびスケジュールを管理します。
----------------------------------

### <a name="initial-configuration"></a>初期コンフィギュレーション

-   コンフィギュレーション ウィザードを実行します。
-   時間登録作業者としての作業者を登録します。

### <a name="plan-worker-schedules"></a>作業者のスケジュールを計画する

-   ワーク プランナーを使用したプロファイルを適用します。 詳細については、<https://technet.microsoft.com/en-us/library/aa551234.aspx>を参照してください。

コンフィギュレーション手順については、<https://technet.microsoft.com/en-us/library/aa496971.aspx>を参照してください。

### <a name="retail-specific-configuration"></a>小売固有のコンフィギュレーション

-   時間登録を有効にする作業者のタイム レコーダーの機能プロファイルを有効にします。 [** POS機能プロファイル** &gt; **機能** &gt; ** POSの時間登録** &gt; **イネーブル時間登録**。
-   販売時点管理 (POS) のアクセス許可グループをコンフィギュレーションして、[タイム レコーダー エントリの表示] のアクセス許可を有効にします。 このアクセス許可により、ユーザーが、その店舗 (およびアドレス帳を介してユーザーが関連付けられている他のすべての店舗から) の他の作業者のタイム レコーダー登録を表示できるようにします。 レジ担当者ロールではなくマネージャー ロールに対してこのアクセス許可を有効にする場合があります。 [** POSのアクセス許可グループ** &gt; **ビューのタイム レコーダー エントリ**。

## <a name="register-time"></a>時刻の登録
### <a name="cashier-and-non-cashier-time-registrations"></a>レジ担当者と非レジ担当者の時間登録

-   POS で:
    -   出勤操作:
        -   非ドロワー操作または新しいシフトにログオンします。
        -   タイム レコーダーの操作を選択します。
        -   必要な操作を選択します:
            -   出勤
            -   休憩
            -   昼休み
            -   退勤

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>現在の状態</th>
    <th>使用可能な操作</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>出勤</td>
    <td><ul>
    <li>休憩</li>
    <li>昼休み</li>
    <li>退勤</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>休憩</td>
    <td>出勤</td>
    </tr>
    <tr class="odd">
    <td>昼休み</td>
    <td>出勤</td>
    </tr>
    <tr class="even">
    <td>退勤</td>
    <td>出勤</td>
    </tr>
    </tbody>
    </table>

    [![] TimeClockStates (。/media/timeclockstates.png) ] (。/media/timeclockstates.png) 
-   確認メッセージを表示して、現在の活動時間が正しいことを確認します。
-   ログ帳:
    -   [**ログ帳**] をクリックして、タイム レコーダーの活動を表示します。
    -   タイム フィルターを使用して、異なる時間枠を選択します。
    -   複数の店舗の場所で作業する場合、時間を記録したすべての店舗からの時間登録が表示されます。 店舗フィルターを使用して、選択した店舗からの時間登録を表示できます。

<!-- -->

-   異なるタイム ゾーン:
    -   別の場所からの時間を表示する場合で (レジ担当者ログ帳に対して、またはマネージャーのシナリオの [**タイム レコーダー エントリの表示**] を使用して)、その場所が別のタイム ゾーンである場合、表示される時刻記録はローカル タイム ゾーンに変換されます。 たとえば、二つの店舗 (1およびネバダのアリゾナの他のマネージャです。 レジ担当者は9:00の開始時に出勤を登録します。 アリゾナ。 その時点で、ネバダの時刻は午前 8 時です。 したがって、ネバダの店舗にいて時間登録のレコードを見ている場合、時間登録は 8 A.M としてマークされます。

## <a name="view-worker-time-registrations"></a>表示するための時間登録
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>作業者の時間登録を表示して、店舗または活動のタイプごとにフィルター処理をする

POS で:

-   [**タイム レコーダー エントリの表示**] を選択します。
-   あなたが割り当てられている同じ店舗に割り当てられているすべての作業者のタイム レコーダーの登録活動が表示されます。
-   活動タイプを使用して、時間登録をフィルター処理するフィルターを保存できます。

## <a name="process-and-manage-time-registrations"></a>プロセス時間登録を管理します
Dynamics 365 for Operations - Retailのユーザーは計算する作業の現在の続きましたり給与に、および移動時間登録を承認します。

### <a name="primary-operations"></a>基本工程

-   計算
-   承認
-   給与に送信

### <a name="other-common-operations"></a>他の共通の操作

-   一括退勤
-   休暇の登録

時刻と出勤の登録の処理方法の詳細については、<https://technet.microsoft.com/en-us/library/aa573180.aspx> を参照してください。


