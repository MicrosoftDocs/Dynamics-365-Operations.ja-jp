---
title: "派生帳簿"
description: "この記事は、派生帳簿機能の概要を示します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: 9319fe95a25b38ca12cbc8633763b042e4086aea
ms.lasthandoff: 03/31/2017


---

# <a name="derived-books"></a>派生帳簿

[!include[banner](../includes/banner.md)]


この記事は、派生帳簿機能の概要を示します。

派生帳簿の目的は、定期的に計画されている固定資産帳簿トランザクションの転記を簡素化することです。  1 つの帳簿を基本帳簿として選択します。 通常、これは会計上の減価償却に使用される帳簿です。 この価値モデルに、同じ期間にトランザクションを転記するように設定された他の帳簿を基本帳簿として関連付けます。 派生帳簿としてよく設定されるのが減価償却簿です。 

派生帳簿に転記するように設定するトランザクションとして最も一般的なものは、取得、取得原価調整、および処分です。 

## <a name="example"></a>例

帳簿 B および C は、取得トランザクション タイプの帳簿 A に対して、派生帳簿として設定されます。 帳簿 A で、価額 1,500.00 の資産 123 に対して取得トランザクションを入力します。 

トランザクションの転記時に、取得トランザクションが生成され、帳簿 B の資産 123 および帳簿 C の資産 123 に 1,500.00 として転記されます。 基本帳簿のトランザクションを固定資産仕訳帳で転記対象として作成した場合は、派生減価償却帳簿のトランザクションも表示および変更できます。 基本帳簿のトランザクションを別の仕訳帳で作成した場合は、派生価値モデルのトランザクションは表示されません。 ただし、基本帳簿のトランザクションを転記するときに適切な勘定および転記階層に転記されます。

> [!NOTE]                                                                                                                               
> 基本帳簿とは異なる間隔でトランザクションを転記するように設定された帳簿は、派生帳簿ではなく別の帳簿として、固定資産に関連付ける必要があります。  

詳細については、「[Posting with derived books](post-derived-value-models.md)」を参照してください。




