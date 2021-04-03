---
title: ライフ イベントのプロセス
description: Microsoft Dynamics 365 Human Resources の従業員のライフサイクル中に、各従業員に対してさまざまなイベントの変化が発生する可能性があります。
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cfb0fc54e3904655cea0c795a46c540bd2a529a2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466257"
---
# <a name="process-life-events"></a>ライフ イベントのプロセス

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources の従業員のライフサイクル中に、各従業員に対してさまざまなイベントの変化が発生する可能性があります。 たとえば、結婚、雇用の変更、または被扶養/受益者の変更などです。 ライフ イベントを使用するには、給付金パラメータ フォームのライフ イベントを有効にし、ライフ イベント タイプを設定し、さらにプラン タイプのライフ イベント オプションを設定する必要があります。

ライフ イベントを処理するには、採用期間中に、少なくとも一度はオープン登録を実行しておく必要があります。 米国では、オープン登録を通常年に 1 回行います。 米国以外では、オープン登録は入社時に実行されます。 作業者は、処理するべきライフ イベントのために給付金プランを選択する必要はありませんが、オープン登録処理に含まれている必要があります。 

将来の日付で発生するライフ イベントをもつ作業者が存在する場合は、ライフ イベント処理を使用します。 このイベントは、処理されていないすべてのライフ イベント (将来のライフ イベント、またはいずれかの作業者に固有ではない追加されたライフ イベント – 1 つの例は、新しい給付金) を処理します。 リアル タイムのライフ イベントは表示されません。

たとえば、今日が 2 月 1 日で、2 月 14 日に作業者である Joe Smith が法人を変更する予定である場合、2 月 15 日にライフ イベント処理を実行すると、2 月 15 日までのすべてのイベントが処理されます。 

1. **給付金管理** ワークスペースにて、**処理** の下の **ライフ イベントの処理** を選択します。

2. **ライフ イベントの処理を実行** ダイアログ ボックスで、次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **登録期間** | ライフ イベントを処理する登録期間。 |
   | **法人エンティティ** | ライフ イベントを処理する法人。 |
   | **ライフ イベント日付** | システムによって登録期間中に、この日付までのすべてのイベントが処理されます。 |
   | **ワーカー** | ライフ イベントを処理する作業者。 このフィールドを空白のままにすると、ライフ イベントがすべての作業者に対して処理されます。 |

3. バックグラウンドで処理を実行する場合は、**バックグラウンドで実行** を選択し、次のタスクを実行します。

   1. 処理情報を入力します。

   2. 定期的なジョブを設定するには、**再実行** を選び、繰り返しの情報を入植し、**OK** を選択します。

   3. ジョブ警告を設定するには、**警告** を選び、入庫する警告を選択し、**OK** を選択します。

   4. **OK** を選択します。 設定したパラメータで処理が実行されます。

4. **OK** を選択します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]