---
title: 指標金利の設定
description: この記事では、指標金利を設定する方法について説明します。 指標金利は、組織がリース支払額を一連の指標金利に関連付ける場合に必要です。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e700c6c0c66b855a3e329302ac27681f4d0144a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883390"
---
# <a name="set-up-index-rates"></a>指標金利の設定

[!include [banner](../includes/banner.md)]

リース支払が指標に依存している場合は、システムで指標金利タイプを追加および管理できます。 **指標金利タイプ** ページからのリース支払を再評価する場合、指標金利の再評価プロセスでは、再評価日から見て最新の指標金利が使用されます。

指標金利タイプと指標金利を追加するには、次の手順に従います。

1. **資産リース \> 設定 \> 指標金利タイプ** の順に移動します。
2. **新規** を選択します。
3. 適切なフィールドで、レート タイプと指標金利の名前を入力します。
4. 新しい指標金利の値を追加するには、指標金利タイプを選択し、**追加** をクリックします。
5. レートの有効開始日を選択し、レート値を選択します。

**指標金利値の差** または **指標金利値** を指標金利の方法として選択する必要があります。

- 開始日時点の指標金利と最新の指標金利の差に基づいて、新しいリース支払を計算する **指標金利値の差** の方法を選択します。 指標金利は、**指標金利 (%)** フィールドで定義されます。
- **指標金利値** の方法を選択して、**指標金利 (%)** フィールドに指定されている割合を使用してリース支払を計算します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
