---
title: 返品品目の分納の受取
description: 分納は、返品注文の出荷ではなく返品注文明細行に対して定義されます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2b7bfad1e0d80675848353d4118960d44f2dc01
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "363916"
---
# <a name="receive-partial-deliveries-of-returned-items"></a>返品品目の分納の受取    

[!include [banner](../includes/banner.md)]


分納は、返品注文の出荷ではなく返品注文明細行に対して定義されます。

つまり、返品注文内の 1 つの返品注文明細行に示された全数量が入荷し、他の明細行の全数量が入荷しない場合は、分納ではありません。 これに対して、たとえば、1 つの返品注文明細行にある品目を 10 単位返品するよう指定されているのに 4 単位だけ入荷した場合は、分納です。

返品荷物の数量が返品注文明細行の全数量より少ない場合、残りの返品数量が入荷するまでそのまま待機することも、部分的な数量を登録および転記することもできます。

## <a name="register-and-post-a-partial-quantity"></a>部分的な数量の登録と転記

1.  着荷の返品注文を選択した後に、**着荷の概要 - 倉庫: %1、ドック: %2、仕訳帳名: %3** フォームで、**着荷開始**をクリックして着荷仕訳帳を作成し、**仕訳帳** \> **入庫の着荷の表示**をクリックして**在庫場所仕訳帳**フォームを開きます。

2.  操作する仕訳帳明細行を選択し、**明細行**をクリックして**仕訳帳明細行、場所**フォームを開きます。

3.  一部の数量だけが着荷した品目番号の明細行を選択し、**機能** \> **分割**の順にクリックして**分割**フォームを開きます。

4.  **分割数量**フィールドに、入荷済の品目の合計数量を入力し、**OK**をクリックします。

5.  **仕訳帳明細行、場所**フォームで、着荷した品目の数量を示す明細行を選択し、**転記**をクリックします。 品目が着荷したら、追加数量を示す明細行を転記できます。




