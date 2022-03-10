---
title: 派生帳簿を転記する
description: この記事は、派生帳簿を使用する方法について説明します。
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.custom: 3421
ms.assetid: f5187c21-eec5-4148-b178-b8a5feff7f23
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef0c7b2ad93f4a9c4ff24052c749f7891f9e915d
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7675422"
---
# <a name="post-with-derived-books"></a>派生帳簿を転記する

[!include [banner](../includes/banner.md)]

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

2.  [VM 1] で、[派生帳簿] タブをクリックします。[帳簿] フィールドで [VM 2] を、[トランザクション タイプ] フィールドで [取得] を選択します。

これにより、特定の固定資産に帳簿を関連付けることができるようになります。 

帳簿 VM1 を使用して固定資産の取得を転記すると、VM 1 だけでなく派生帳簿 VM 2 にもその取得が転記されます。 両方の固定資産帳簿のステータスが [未処理] に更新されます。

> [!NOTE]                                                                                                         
> 派生帳簿を使用しない場合は、帳簿 VM 1 および帳簿 VM 2 の両方に対して固定資産の取得を転記する必要があります。

詳細については、[派生帳簿](derived-books.md) を参照してください。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
