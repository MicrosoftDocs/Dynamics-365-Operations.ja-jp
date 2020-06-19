---
title: 二重書き込みでの在庫状況
description: このトピックでは、二重書き込みでの在庫状況の確認について説明します。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426985"
---
# <a name="inventory-availability"></a>在庫状況

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

在庫状況を使用すると、Dynamics 365 のモデル駆動型アプリの **見積**、**注文**、または **請求書** の各フォームに製品を追加する前に、在庫を確認できます。 たとえば、在庫の確認と履行日の決定は、[見込顧客から現金](dual-write-prospect-to-cash.md) プロセスの重要なタスクです。 十分な在庫がない場合は、予想在庫の入庫および払出に基づいて出荷日を見積もることができます。 また、製品の納期回答可能在庫 (ATP) 情報を確認して、事前に定義されたタイム フェンスで ATP 数量を検索することもできます。

## <a name="on-hand-inventory"></a>手持在庫 

Dynamics 365 Sales の **見積**、**注文**、または **請求書** フォームのヘッダーに、新しいボタン **手持在庫** が追加されました。 このボタンをクリックすると、ダイアログ ボックスが表示され、手持在庫を確認する会社と製品を指定できます。 Dynamics 365 Supply Chain Management から在庫情報を返し、[手持在庫](../../../../supply-chain/inventory/tasks/check-availability-stock.md) と同じ情報を表示します。 情報には、次の数量が含まれます:

- **手持数量**
- **予約済み手持数量**
- **使用可能な手持数量**
- **注文済数量**
- **注文中数量**
- **引当済の注文済数量**
- **利用可能な合計数量**

## <a name="atp-information"></a>ATP 情報

Dynamics 365 Sales の **見積**、**注文**、または **請求書** フォームの明細行品目に、新しいボタン **ATP 情報** が追加されました。 このボタンをクリックすると、ダイアログ ボックスが表示され、会社、製品、在庫サイト、在庫倉庫、注文数量を指定できます。 Supply Chain Management から **ATP 情報** を返し、[注文納期日](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) で説明されている設定を表示します。 この情報には、**ATP 数量**、**入庫数量**、**払出数量**、**手持数量** が含まれます。
