---
title: サービス注文ステージ
description: サービス注文のステージを定義し、作業者に割り当てると、サービス組織内のさまざまな従業員が実行するタスクでのサービス注文の流れを管理します。
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817512"
---
# <a name="service-order-stages"></a>サービス注文ステージ   

[!include [banner](../includes/banner.md)]


サービス注文のステージを設定して、完了する必要があるタスク、完了する順番、それらの実行を担当する作業者を定義できます。 サービス注文のステージを定義し、作業者に割り当てると、サービス組織内のさまざまな従業員が実行するタスクでのサービス注文の流れを管理できます。 ステージ シーケンスには、初期ステージを含める必要があります。

また、各ステージで許可されるアクションを定義できます。 たとえば、最後のステージを除くすべてのステージの **転記** チェック ボックスをオフにすると、サービス注文がステージの全シーケンスを完了するまで、サービス注文を転記できないようにすることができます。

## <a name="branching-in-service-order-stages"></a>サービス注文ステージの分岐

サービス ステージを設定すると、次のサービス ステージ用にそこで選択できる複数の選択肢または分岐を作成できます。 作成したすべての分岐は、初期ステージが完了したときに選択できます。 たとえば、初期ステージとして **計画** を設定します。 **処理中** と **キャンセル** という 2 種類のステージを作成し、それらの親として **計画** を選択します。 販売注文に **計画** のステージを割り当てます。 販売注文の計画ステージが完了すると、販売注文の作業準備が完了したら **プロセス** ステージ、販売注文がキャンセルされたら **キャンセル** ステージを選択できます。

## <a name="see-also"></a>参照

[サービス注文ステージを設定します](set-up-service-order-stages.md)

[サービス注文ステージの変更](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]