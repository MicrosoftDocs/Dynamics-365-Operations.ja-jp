---
title: 作業指示書のメンテナンス ダウンタイム
description: この記事では、作業指示書で選択した資産において、メンテナンス ダウンタイム登録を作成する方法について説明します。
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4a310152685f733093cc7e50404c23b6f24c40cc
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016655"
---
# <a name="maintenance-downtime-for-work-orders"></a>作業指示書のメンテナンス ダウンタイム

[!include [banner](../../includes/banner.md)]


作業指示書で選択した資産に対して、メンテナンス ダウンタイム登録を作成できます。 この能力は、生産領域の 1 つ以上のマシンにメンテナンス ダウンタイムを登録する場合に便利です。 まず、使用するメンテナンス ダウンタイムの理由コードを作成します (例えば **故障** や **計画停止** など)。 このステップは、**メンテナンス ダウンタイムの理由コード** ページで実行されます。 次に、**メンテナンス ダウンタイム** ページでメンテナンス ダウンタイムの登録を作成し、関連するメンテナンス ダウンタイムの理由コードを追加します。

## <a name="create-maintenance-downtime-reason-codes"></a>メンテナンス ダウンタイムの理由コードの作成

1. **資産管理** > **設定** > **作業指示書** > **メンテナンス ダウンタイムの理由コード** を選択します。

2. **新規** を選択します。

3. **メンテナンス ダウンタイムの理由コード** フィールドに、メンテナンス ダウンタイムの理由コードの ID を入力します。

4. **名前** フィールドに、名前を入力します。

5. 理由コードを資産の主要業績評価指標 (KPI) の計算に含める必要がある場合は、**KPI include** チェック ボックスをオンにします。 一般に、想定されるパフォーマンスには影響しないため、計画済生産停止は KPI 計算には含めません。

6. **保存** を選択します。

次の図では、**メンテナンス ダウンタイムの理由コード** ページの例を示します。

![図 1。](media/15-work-orders.png)

使用するメンテナンス ダウンタイムの理由コードを作成したら、作業指示書および資産に対してメンテナンス ダウンタイムの登録を作成できます。


## <a name="create-maintenance-downtime-registrations"></a>メンテナンス ダウンタイムの登録の作成

1. **資産管理** > **作業指示書** > **すべての作業指示書** または **有効な作業指示書** をクリックします。

2. 作業指示書を選択してから、**作業指示書** タブ (**資産** グループ内) で、**メンテナンス ダウンタイム** を選択します。

3. **新規** を選択します。

4. **開始** および **終了** フィールドで、メンテナンス ダウンタイムの登録に使用する日付と時間の間隔を定義します。

>[!NOTE]
>**終了** フィールドを終了すると、期間 (時) が **期間** フィールドに自動的に挿入されます。

5. **メンテナンス ダウンタイムの理由コード** フィールドで理由コードを選択します。

6. ステップ 3 から 5 を繰り返して登録を追加します。

7. **保存** を選択します。

下の図は、メンテナンス ダウンタイム登録の例を示します。

![図 2。](media/16-work-orders.png)

メンテナンス ダウンタイムの登録の計算に使用されるカレンダーは、資産とパラメーターの設定での選択によって異なります。 次の図に示すように、**リソース** フィールド (**固定資産** クイック タブ、**すべての資産** ページ) の資産に対してリソースが選択されている場合は、関連付けられているリソース グループに対して設定されているカレンダーが使用されます。

![図 3。](media/17-work-orders.png)

資産に対してリソースが選択されていない場合、次の図に示すように、**資産管理パラメーター** ページで選択された標準カレンダーが使用されます。

![図 4。](media/18-work-orders.png)

すべてのメンテナンス ダウンタイムの登録の概要を表示するには、**資産管理** > **照会** > **メンテナンス ダウンタイム** をクリックします。

>[!NOTE]
>**資産管理** モジュールで使用されるすべてのカレンダーは、**組織管理** > **設定** > **カレンダー** > **カレンダー** で設定されます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]