---
title: サービス注文の在庫品目要求
description: この記事では、サービス注文の在庫品目要求について説明します。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjSalesItemReq
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 376cda6bbe1800611e6f24c347b9035469a30a14
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015175"
---
# <a name="service-order-item-requirements"></a>サービス注文の在庫品目要求

[!include [banner](../includes/banner.md)]

顧客に提供するサービスを追跡および管理するサービス注文を作成できます。 サービス注文に特定の品目を引き当てる必要がある場合、その在庫品目要求を作成できます。 品目要求を在庫からすぐ消費したり、その品目の製造オーダーを開始できます。

品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。

サービス注文に関する要求はプロジェクトを通じて処理します。 サービス注文に対して在庫品目要求を作成するには、サービス注文をプロジェクトに関連付ける必要があります。

サービス注文に対して作成された在庫品目要求は、個々のサービス注文の **プロジェクト** から、または **販売注文** フォームを使用して表示できます。

## <a name="view-an-item-requirement-from-a-service-order"></a>サービス注文からの在庫品目要求の表示

1. **サービス管理** \> **サービス注文** \> **サービス注文** に移動します。
1. **発送** を選択し、**在庫品目要求** を選択して **在庫品目要求** フォームを開きます。
1. **プロジェクト** タブを選択し、**サービス注文** フィールドを確認して、在庫品目要求のサービス注文を表示します。

## <a name="delete-service-orders-with-item-requirements"></a>在庫品目要求を含むサービス注文の削除

サービス注文に対して在庫品目要求が作成されている場合は、サービス注文を削除できません。 サービス注文を削除する前に、在庫品目要求を削除する必要があります。

1. **サービス管理** \> **サービス注文** \> **サービス注文** に移動します。
1. **発送** を選択し、**在庫品目要求** を選択して **在庫品目要求** フォームを開きます。 このフォームに、サービス注文に対して作成されている在庫品目要求が一覧表示されます。
1. 削除する在庫品目要求を選択し、**削除** を選択します。

- または -

1. **プロジェクト管理および会計** \> **プロジェクト** \> **すべてのプロジェクト** の順に移動します。
1. 在庫品目要求が作成されているサービス注文を含むプロジェクトを開きます。
1. **プロジェクト** フォームの右ペインで、**在庫品目要求** を選択します。 **在庫品目要求** フォームは、選択したプロジェクトに関連付けられている在庫品目要求を一覧表示します。
1. 削除する在庫品目要求を選択し、**削除** を選択します。

## <a name="see-also"></a>参照

[在庫品目要求 (フォーム)](https://technet.microsoft.com/library/aa552021\(v=ax.60\))



[!INCLUDE[footer-include](../../includes/footer-banner.md)]