---
title: "元帳配賦ルール"
description: "この記事は、元帳配賦ルールに関する情報を提供します。 これらの配賦ルールのさまざまなコンポーネントと使用できる配賦方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: cf723381ed2f9696512d17af7e882582cbfcb49e
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="ledger-allocation-rules"></a>元帳配賦ルール

[!include[banner](../includes/banner.md)]


この記事は、元帳配賦ルールに関する情報を提供します。 これらの配賦ルールのさまざまなコンポーネントと使用できる配賦方法を説明します。

元帳配賦ルールを使用すると、自動的に配賦仕訳帳と勘定項目の計算と生成を行い、元帳残高や固定金額を配賦できます。 配賦方法には、変動的または固定があります。 次の配賦方法が、元帳配賦ルールに使用できます。

-   **基準** – これは変動方式で、配賦方法がフィルター条件に基づいて実際の元帳残高に依存する場合に使用します。 たとえば、広告費を、全部門の合計売上に対する各部門の売上の割合に基づいて配賦することができます。
-   **固定割合**と**加重固定値** – これらの方式では、配賦率や配賦比重のルールを直接定義できます。 たとえば、部門 A が広告費の 70 パーセントを受け取り、部門 B が 30 パーセントを受け取るように広告費を割り当てることができます。
-   **均等** – この方式は、個々に定義した配賦先に均等に金額を配分します。 たとえば、配賦先として部門 A と部門 B が定義されている場合、部門 A と部門 B の双方が 50 パーセントずつの広告費を受け取るように割り当てることができます。

配賦ルールの配賦方法が [基準] である場合は、元帳配賦基準ルールも別途定義する必要があります。 「配賦要求の処理」プロセスでは、ユーザーが元帳配賦ルールを処理し、配賦仕訳帳入力の結果をプレビューしてから、計算された配賦を転記または削除できます。

## <a name="components-of-ledger-allocation-rules"></a>元帳配賦ルールのコンポーネント
各配賦ルールには、一般、入力元、出力先、および相殺の 4 つのコンポーネントがあります。 配賦方法として [基準] を使用する場合、追加のコンポーネントである元帳配賦基準ルールが必要になります。 各コンポーネントは、配賦の処理に要求される重要な情報を提供します。

-   **一般** – このコンポーネントでは、ユーザーが配賦方法、会社間ルール設定、ルールが有効かどうかなどのオプションを指定します。
-   **ソース** – このコンポーネントでは、ユーザーが配賦の入力元データを指定します。 配賦は、元帳残高 (**データ ソース** = **元帳**) または固定金額 (**データ ソース** = **固定値**) に基づきます。 **データ ソース**が**元帳**に設定されている場合、ソースのフィルタ条件は、元帳配賦ルールに対して定義する必要があります (たとえば、広告費)。
-   **出力先** – このコンポーネントでは、配賦計算の結果を配賦先明細行に配分し計上する方法を定義します。 たとえば、各部門には、配賦先明細行が 1 つあります。
-   **相殺** – このコンポーネントでは、主勘定および分析コードが配賦先入力の収支を合わせるための相殺仕訳に決定される方法を定義します。 ユーザー定義のオプションは通常、ソースに基づく勘定および分析コードの代わりに使用されます。 **データ ソース**に**固定値**が設定されている場合、**ソース**は選択肢として使用できません。
-   **元帳配賦基準ルール** – これらのルールは、独自のソース基準を使用して、元帳残高を配賦に使用するかを決定します (たとえば、部門ごとの収益)。 各配賦基準ルールは、複数の配賦ルールで使用できます。




