---
title: 支払額タイプの追加
description: このトピックでは、資産リースで支払額タイプを設定する方法について説明します。
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 037afa458277a3a07bcb937c6ec4d961d0dd5ca9
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968324"
---
# <a name="add-payment-amount-types"></a>支払額タイプの追加

[!include [banner](../includes/banner.md)]

このトピックでは、資産リースで支払額タイプを設定する方法について説明します。 これにより、支払スケジュール明細行に総額を追加する代わりに、リース支払額を明細化できます。

支払額タイプを追加するには、次の手順に従います。

1. **資産リース \> 設定 \> 支払額タイプ** の順に移動します。
2. **新規** を選択します。
3. 新しい支払タイプと説明を入力します。

> [!NOTE]
> IFRS 16 インデックス再評価の場合は、支払金額タイプを 1 つ作成し、**IRIF 16 インデックス再評価に使用** としてマークする必要があります 。 この支払額タイプは、IFRS 16 帳に対してインデックス再評価プロセスを実行する場合に使用され、インデックスの再評価プロセスのために発生した変更が考慮されます。
>
> リースの **支払内訳** オプションが **はい** に設定されている場合、IFRS 16 のインデックス再評価が実行されますが 、IFRS 16 の支払タイプがない場合、プロセスは完了されません。

**IFRS 16 インデックス再評価で使用済** とマークできるレコードは1つのみです。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
