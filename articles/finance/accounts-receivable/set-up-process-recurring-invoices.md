---
title: 定期請求書の設定と処理
description: この記事は、定期的な請求書の設定および処理の方法を説明します。 定期的に同じ金額に対して請求書を発行する場合に、定期的な請求書を使用できます。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834dc64ce531fb614bc7836e0def16f27ecf5e18
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188641"
---
# <a name="set-up-and-process-recurring-invoices"></a>定期請求書の設定と処理

[!include [banner](../includes/banner.md)]

この記事は、定期的な請求書の設定および処理の方法を説明します。 定期的に同じ金額に対して請求書を発行する場合に、定期的な請求書を使用できます。

## <a name="create-a-recurring-free-text-invoice-template"></a>定期的な自由書式の請求書テンプレートの作成

同じサービスに関する請求を定期的に顧客に行うには、請求書を作成する場合でも、請求書の作成に再利用できる自由書式の請求書テンプレートを定義する必要があります。 このテンプレートには、次の情報が含まれます。

-   税グループ、支払条件、および支払方法などのヘッダー情報
-   サービスの説明、収益勘定、単価、請求金額などの明細行情報
-   出荷または処理の請求
-   コスト センター、事業単位などの財務分析コード情報を伴う勘定配布

実際には、請求書全体を作成し、テンプレートとして保存します。 **定期請求書** ページを使用してテンプレートを設定できます。

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>顧客への自由書式の請求書テンプレートの割り当て、および繰り返し詳細の入力
テンプレートの作成後、請求先の顧客にテンプレートを割り当てる必要があります。 また、請求をいつ、どのくらいの頻度で使用するか指定する必要があります。 **顧客** ページの **請求書** タブでテンプレートを割り当てることができます。 一覧にテンプレートを追加し、次の情報を更新します。

-   必要に応じた、定期請求の開始日と終了日
-   定期請求の頻度 (たとえば、毎日または月に一度)
-   最大請求金額 (この情報が必要な場合)

顧客はさまざまな頻度の複数のテンプレートを使用できます。

## <a name="generate-the-recurring-invoices"></a>定期請求書の生成
**定期請求書** ページには、定期的な請求書テンプレートを処理するタスクがあります。 請求書を生成する請求日およびテンプレートを指定します。 請求書が生成され、処理される請求書の各グループに固有の再実行 ID 番号が請求書に割り当てられます。

## <a name="post-recurring-free-text-invoices"></a>定期的な自由書式の請求書の転記

定期請求書が生成された後、請求書の再実行 ID が **定期請求書** ページの転記タスクに表示されます。 リンクをクリックすることにより、再実行 ID の請求書をすべて表示できます。 再実行 ID の請求書の確認中に、請求書を個別に削除できます。 顧客の再実行設定をそのテンプレートに対してリセットすると、あとで再生成できます。 再実行 ID の請求書は、1 つ、複数、またはすべてを転記できます。 ワークフローが有効な場合、請求書を転記する前に **送信** をクリックする必要があります。

## <a name="print-recurring-free-text-invoices"></a>定期的な自由書式の請求書の印刷

定期請求書が転記された後、自由書式の請求書のリスト ページから請求書を印刷できます。 選択した請求書を印刷でき、また印刷する請求書の範囲を選択できます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]