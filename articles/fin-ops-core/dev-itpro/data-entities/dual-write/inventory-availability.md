---
title: 二重書き込みでの在庫状況
description: このトピックでは、二重書き込みでの在庫状況の確認方法について説明します。
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4454615"
---
# <a name="inventory-availability-in-dual-write"></a>二重書き込みでの在庫状況

[!include [banner](../../includes/banner.md)]

在庫状況を使用すると、Microsoft Dynamics 365 Sales の **見積**、**注文**、または **請求書** ページに製品を追加する前に、在庫を確認できます。 たとえば、[見込顧客から現金](dual-write-prospect-to-cash.md) の一つの重要なタスクとして在庫の確認と履行日の決定をおこないます。

十分な在庫がない場合は、予想在庫の入庫および払出に基づいて出荷日を見積もることができます。 また、製品の納期回答可能在庫 (ATP) 情報を確認して、事前に定義されたタイム フェンスで ATP 数量を検索することもできます。

## <a name="on-hand-inventory"></a>手持在庫

Dynamics 365 Sales で、**見積**、**注文**、**請求書** の各ページのヘッダーに、新規の **手持在庫** ボタンが追加されました。 このボタンをクリックすると、ダイアログ ボックスが表示され、手持在庫を確認する会社と製品を指定できます。 このダイアログボックスには、[手持在庫](../../../../supply-chain/inventory/tasks/check-availability-stock.md) と同じ情報が表示されます。

このダイアログ ボックスでは、Dynamics 365 Supply Chain Management からの在庫情報が返されます。 この情報には、次の数量が含まれています。

- 手持在庫数量
- 予約済み手持数量
- 使用可能な手持数量
- 注文済数量
- 注文中数量
- 引当済の注文済数量
- 利用可能な合計数量

## <a name="atp-information"></a>ATP 情報

Sales では、**ATP情報** ボタンが **見積**、**注文**、**請求書** の各ページの品目に追加されました。 このボタンを選択すると、ダイアログ ボックスが表示され、会社、製品、在庫サイト、在庫倉庫、注文数量を指定できます。 このダイアログボックスの設定は、[注文-受注](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) に記述されている設定と同じです。

このダイアログ ボックスでは、Supply Chain Management からの ATP 情報が返されます。 この情報には、次の数量が含まれています。

- ATP 数量
- 受入数量
- 払出数量
- 手持在庫数量
