---
title: 検査指示
description: このトピックは、在庫をブロックする検査指示の使用方法について説明します。
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "362582"
---
# <a name="quarantine-orders"></a>検査指示

[!include [banner](../includes/banner.md)]

このトピックは、在庫をブロックする検査指示の使用方法について説明します。

検査指示は、在庫をブロックするのに使用できます。 たとえば、 品質テストの理由で品目を検査する場合があります。 検査された在庫は、検査倉庫に転送されます。 **注記:** 高度な倉庫管理プロセス (倉庫管理で) を使用している場合、検査指示の処理は返品販売注文に対してのみ使用されます。

## <a name="quarantine-on-hand-inventory-items"></a>手持在庫品目の検査
品目を検査する場合、検査指示を手動で作成するか、受信処理時に検査指示を自動的に作成するようにシステムを設定するかのいずれかが可能です。 検査指示を自動的に作成するには、**品目モデル グループ** ページの **在庫ポリシー** タブの **検査管理** オプションを選択します。 また、入荷倉庫について、**検査倉庫** フィールドで既定の検査倉庫を指定する必要があります。 Microsoft Dynamics 365 for Finance and Operations では、現物手持在庫が発注書または製造オーダーで記録されると、検査品目は検査倉庫に自動的に移動されます。 この移動は、検査指示のステータスが**開始済**に変更されるため、実行されます。 検査指示を手動で作成する場合、品目は、関連する品目モデル グループで検査管理のために設定する必要はありません。 このプロセスでは、検査する手持在庫と、使用する検査倉庫を指定する必要があります。 プロセスの計画を支援するために、検査指示のステータスを使用できます。

## <a name="quarantine-order-statuses"></a>検査指示のステータス
検査指示には次のステータスがあります。

-   作成済み
-   開始済
-   完了レポート済
-   終了済

### <a name="created"></a>作成済み

検査指示のステータスが**作成済**になるのは、検査指示が手動で作成されているが、まだ品目が検査倉庫に配置されていない場合です。 2 つの在庫トランザクションが生成されます。 1 つ目のトランザクションは**注文中**、**引当済現物**、または**ピッキング済**のステータスがある払出トランザクションです。 2 つ目のトランザクションは、検査倉庫に**注文済**または**登録済**のステータスがある受入トランザクションです。 通常のプロセスで在庫への更新を引当、ピック、または登録できます。

### <a name="started"></a>開始済

検査指示のステータスが**開始済**になると、在庫は通常の倉庫から検査倉庫へ移動され、2 つの在庫トランザクションが生成されます。 1 つのトランザクションには**払出済**のステータスがあり、もう一方のトランザクションには**受取済**のステータスがあります。 同時に、戻りの転送を処理するための 2 つの在庫トランザクションが作成されます。 これらのトランザクションは日付がありません。 1 つのトランザクションには**引当済現物**のステータスがあり、もう一方のトランザクションには**注文済**のステータスがあります。

### <a name="reported-as-finished"></a>完了レポート済

**完了レポート**をクリックすると、開始された検査指示の完了を報告できます。 品目は検査からリリースされますが、まだ通常の倉庫に戻されてはいません。 通常の倉庫への返送は、完了レポート プロセス時に初期化される着荷仕訳帳によって処理できます。

### <a name="ended"></a>終了済

検査指示が終了すると、品目は検査倉庫から通常の倉庫に戻ります。 品目トランザクションのステータスは、検査倉庫で**売却済**に、そして通常の倉庫で**購買済**に設定されます。

## <a name="quarantine-order-scrap"></a>検査指示仕損
検査指示のプロセスの一環として、在庫の仕損ができます。 仕損を処理するときは、在庫のステータスは検査倉庫からの払出トランザクションによって**売却済**に設定されます。

<a name="additional-resources"></a>その他のリソース
--------

[在庫ブロック](inventory-blocking.md)
