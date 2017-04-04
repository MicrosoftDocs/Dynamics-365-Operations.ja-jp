---
title: "派生減価を含む転記"
description: "この記事は、派生帳簿を使用する方法について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: ca077727910059878fb16a3f78c5b9133c6c741f
ms.lasthandoff: 03/31/2017


---

# <a name="post-with-derived-books"></a>派生減価を含む転記

この記事は、派生帳簿を使用する方法について説明します。

派生帳簿を含む帳簿のトランザクションを転記すると、派生帳簿トランザクションは仕訳帳、発注書、または自由書式の請求書に自動的に転記されます。 ただし、[固定資産] 仕訳で基本帳簿トランザクションを作成した場合は、派生トランザクションを転記する前にその金額を表示および変更できます。
-   売上税勘定、顧客勘定、仕入先勘定など一部の勘定は、基本帳簿の転記によって一度だけ更新されます。 派生帳簿トランザクションは、[固定資産転記プロファイル] ページの派生帳簿で定義されている勘定に転記されます。
-   [取得] は、派生帳簿のトランザクション タイプとして頻繁に使用されます。 帳簿および派生帳簿を固定資産の取得時から固定資産に適用する必要がある場合は、このタイプを使用します。
-   トランザクション タイプの他の値も適用できます。 たとえば、帳簿および派生帳簿の売却および処分の間隔が同一である場合は、すべての固定資産トランザクション タイプを派生帳簿の設定に使用できます。

> [!WARNING]
> 派生帳簿に転記する減価償却額は、基本帳簿に転記した金額と同じになります。 これらの帳簿間で減価償却方法が異なる場合は、派生プロセスを使用して減価償却トランザクションを生成しないでください。 |

## <a name="example"></a>例 
ここでは、派生帳簿機能を使用して取得トランザクションを設定する方法について説明します。

1.  [帳簿] ページの帳簿を作成します。
    -   会計用の帳簿: VM 1、現在の転記階層
    -   税務用の帳簿: VM 2、税の転記階層

2.  VM 1 で、[派生帳簿] タブをクリックします。 [帳簿] フィールドで VM 2 を選択し、[トランザクション タイプ] フィールドで [取得] を選択します。

これにより、特定の固定資産に帳簿を関連付けることができるようになります。 

取得が簿VM 1を使用して固定資産の取得を転記すると、取得、VM 1では、派生減価償却簿VM 2.でだけでなく、転記されます。 両方の固定資産帳簿のステータスが開くように更新されます。

> [!NOTE]                                                                                                         
> 派生帳簿を使用しない場合は、帳簿 VM 1 および帳簿 VM 2 の両方に対して固定資産の取得を転記する必要があります。

詳細については、" [ (取得books.md) 派生減価]


