---
title: 販売注文の作成
description: この資料では、発注書を手動で作成する場合の手順、およびオプションを説明します。
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70050efb31040f2c7ebfc55681a7145e313d804d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674368"
---
# <a name="create-purchase-orders"></a>販売注文の作成

[!include [banner](../includes/banner.md)]

この資料では、発注書を手動で作成する場合の手順、およびオプションを説明します。

発注書 (PO) を作成するとき、発注全体に関する一般的な情報が発注書ヘッダーで指定され、1 つまたは複数の購買注文明細行が追加されます。 この資料では、いくつかの利用可能な最も頻繁に使用されるオプションについて説明します。  

別の発注ドキュメントまたは販売注文から明細行をコピーして、発注書を作成することもできます。 この例では、クレジットを示す請求書の符号を取り消すように、棚卸資産の符号を取り消すことができます。  

発注書を手動で作成できますが、通常は別のプロセスから生成されます。 注文は、要求書など他のドキュメントに基づいて自動的に作成できます。 また、計画された PO でマスタ プラン プロセスの一部として登録することもできます。 購買契約を使用すると、PO は **リリース注文** 操作で作成できます。 発注書を自動的に作成するためのより詳細なメソッドもあります。 例えば直納か、会社間発注チェーンを使用する際に注文を作成できます。

## <a name="creating-a-purchase-order-header"></a>発注書ヘッダーの作成
新しい発注書を作成するときは、発注書ヘッダーに最も一般的な情報を入力できる場所に、[ダイアログ ボックス] が表示されます。 **OK** をクリックしてダイアログ ボックスを閉じるときに発注書が作成され、ヘッダーで追加情報を指定できます。  

発注書を作成するときに考慮が必要な最初の詳細は、発注のタイプです。 **発注書** タイプは、最も頻繁に使用されます。 ただし、クレジットの請求書が必要な場合、**返品済注文** タイプを使用できます。  

**仕入先** フィールドで仕入先を指定する必要があります。 このフィールドにアカウントまたは仕入先の名前のいずれかで検索できます。 仕入先が複数の場所から出荷するものの、1 つの請求先を使用する場合、**請求先** フィールドで請求先を選択し、異なる仕入先アカウントを使用します。 繰り返し注文しない製品の発注書を作成する必要があるなら、**一時仕入先** オプションを使用できます。 このオプションでは **買掛金勘定** モジュールで、後にクリーンアップ処理を実行できるよう一時アカウントとしてマークされる新しい仕入先アカウントが自動的に作成されます。 仕入先アカウントを選択すると、発注書ヘッダーの多くのフィールドは、仕入先アカウントに関連付けられている情報から既定値を継承します。 例えば、既定の配送サイトと倉庫は、仕入先情報からコピーされます。 ただし、別の場所向けの購入の場合は、これらの既定値を上書きできます。  

仕入先から注文の参照番号が提供される場合、**仕入先参照** フィールドでこの情報を記録できます。 返品済み注文には、返送処理のための仕入先による承認を照会するため、**RMA** フィールドの値を指定する必要があります。  

購買契約書が注文に関連付けられているなら、**購買契約書** フィールドのこの情報を指定する必要があります。  

発注書ヘッダーには個々の明細行ではなく、注文全体に適用される諸費用に関する情報も含まれています。 自動請求が仕入先、または仕入先の請求グループに設定されている場合、請求金額がその注文に自動的に追加されます。 アクション ペインの **諸費用の管理** をクリックして、注文ヘッダーに請求金額を手動で追加することもできます。

## <a name="adding-purchase-order-lines"></a>購買注文明細行の追加
発注書は、物理的な製品やサービスに使用できます。 在庫モデル グループの設定は、特定の品目番号が製品またはサービスに適用されるかどうかを決定します。 通常、購入する品目は、品目番号によって指定されます。 ただし、注文が直接消費される製品やサービスの場合、アイテム調達カテゴリを使用して、品目を指定することもできます。  

購買注文明細行には、たくさんのフィールドが含まれていますが、これらのフィールドには既定値または注文ヘッダーから継承された値が含まれています。 製品またはサービスを選択すると、追加のフィールドが設定されます。 ほとんどの場合手動で設定されるフィールドには、品目番号、数量、および配送指定日のフィールドが含まれています。 単価と割引についての情報も非常に重要ですが、これらのフィールドの値は多くの場合、売買契約書や購買契約書により決定されます。  

製品を選択すると、品目番号を使用する代わりに製品名のすべてまたは一部を検索できます。 異なるサイズなど、製品にいくつかのバリエーションがある場合、**行の追加** 機能、または **バリアント番号** フィールドで利用可能なルックアップ機能を使用して、バリエーションの概要を表示できます。  

多くの場合、各購買注文明細行で選択されている品目のいくつかの分析コードを指定する必要があります。 指定の必要な分析コードは、製品マスター定義に割り当てられている分析コード グループによって決まります。 たとえば、多くの場合、製品が配送される場所を表示するためのサイトや倉庫を指定する必要があります。 バリエーションの数を指定するか、色、サイズ、構成、スタイルなど、製品分析コードの 1 つまたは複数の値を入力することにより、商品のバリエーションを識別します。 バッチ番号およびシリアル番号などの分析コードを追跡すると、各在庫のロットを一意に識別できます。 注文を作成した後、**登録** アクションを使用して、その注文の分析コード値をキャプチャできます。 たとえば、1 つの品目で、数量 5 個を注文したとします。 以降、この品目の内 3 つを黒、2 つを青で登録します。 この方法は、着荷の登録時に分析コード情報を取得する代替の 1 つになります。  

在庫製品の在庫トランザクションのステータスの詳細を確認できます。 たとえば、注文の割合を決定するために、手持在庫をチェックする可能性があります。 または、着荷の登録が発生したかどうかを確認するには、注文数量の在庫状態を確認したいと思うかもしれません。  

仕入先に製品を返品するために使用される購買注文明細行には、負の数量があります。 **予約** アクションを使用して、返品するロットの詳細を選択できます。  

場合によっては、異なる品目が部分的に別の日付で配送されるよう、注文数量を分割したいと思うかもしれません。 **配送スケジュール** アクションを使用して、これらの配送を設定できます。このアクションは **購買注文明細行** メニューにあり、**行** ビューから選択できます。  

自動請求が仕入先、または仕入先の請求グループに設定されており、また品目または品目請求グループに設定されている場合、請求金額がその購買注文明細行に自動的に追加されます。 ただし一般的には、請求金額は手動で注文明細行レベルに追加されます。 諸費用を追加するには、**行** ビューの中にある **財務** メニューの、**諸費用の管理** アクションを使用して、**諸費用の管理** ページを開きます。 注文明細行レベルで費用を直接追加することの利点は、在庫コストとして請求金額を割り当てることができるということです。 請求コードを製品コストの勘定に設定するには、**品目** 借方オプションを使用します。 これらのタイプの費用は注文確定前に、発注書ヘッダーから購買注文明細行に割り当てられる必要があります。 たとえば、各明細行の数量に基づき、費用を割り当てたいと思うかもしれません。 費用カテゴリは、諸費用を計上する方法にも影響します。 たとえば、固定費では固定金額を指定し、パーセント費用では注文明細行の正味金額の割合として計算されます。 発注書では荷重を割り当てることが可能で、その荷重には輸送費として予想される経費見積もりが含まれるかもしれません。 荷重から購買注文明細行に、この経費を割り当てることができます。

## <a name="purchase-order-actions"></a>発注書アクション
ヘッダーと明細行を発注書に追加したなら、注文確定が可能になる前に、多くの場合、追加手順を完了する必要があります。 たくさんのオプションが利用可能なため、関連するメニュー項目を検索するため、[[アクション検索]](../../fin-ops-core/fin-ops/get-started/action-search.md) の使用が助けとなるかもしれません。  

提供品をセットにするため、注文で製品をコンフィギュレートできます。 提供品とは他の製品と購入が必要、または購入できる製品です。 提供品は、付属製品として無料で追加される、または注文に追加するかどうかを決定できる場合があります。 追加された各注文明細行ごとに、提供品を確認できます。 ただし、アクションページから開ける **提供品** ページを使用して、すべての注文明細行に関連する提供品を確認して追加する方が、より便利と感じるかもしれません。  

割引は通常、明細行が作成された時に、それらの行に追加されます。 ただし、中には注文全体に適用される割引もあります。

-   **割引合計** アクションでは、すべての注文に適用される合計割引率が計算されます。 この割引を現金割引と混同しないでください。 現金割引は、請求書の支払が完了した時点で適用され、かつ特定の日付までに支払決済をするかどうかが重要です。
-   複数行割引が適用される場合、その計算、およびそれを注文に割り当てるため、**複数行割引** アクションを使用する必要があります。 複数行割引は、注文製品の組み合わせが、共同のしきい値を超えた場合に提供可能となる割引です。 このタイプの割引を使用しているのは少数の企業だけです。

**品目** 借方タイプを使用する費用コードの存在する請求費用は、注文確定が可能になる前に、明細行レベルに割り当てられる必要があります。 費用の合計金額を指定できるよう、諸費用を発注書ヘッダー レベルに割り当てると便利だと思われるかもしれません。 ただしこの例では、注文確定前に、費用を各明細行に割り当てる必要があります。 ヘッダー レベルから下の注文明細行まで割り当てられる諸費用から金額を分離するため、**諸費用の配賦** アクションを使用できます。 諸費用は注文済数量または注文明細行にわたって均等にそれぞれの行の正味金額に基づいて分割できます。 明細行に諸費用を割り当てた後、その費用は発注書ヘッダーから削除されます。  

購買注文書は処理される前に、注文に割り当てられる予算資金額を要求するようコンフィギュレートできます。 この例では、予算を割り当てるため、**予算チェック** アクションを使用できます。  

発注書の完了を延期する必要があるかもしれません。 例えば、製品やサービスに関する追加情報が必要とされる、または支出の承認を得る必要があるかもしれません。 注文を保留するにはいくつかの方法があります。 例えば、注文確定を待機できます。 または、変更管理ワークフローを使用している場合は、承認を得るための発注書送信を行いません。 特定の仕入先へのすべての注文をブロックする必要がある場合は、仕入先マスターで処理するため、その仕入先を **保留中** としてマークできます。 注文の処理を妨げる状況が発生する場合もあります。 例えば、与信限度額を超過した場合、または予算資金が利用できないため、処理の進行が妨げられるかもしれません。

## <a name="additional-resources"></a>追加リソース

[発注書の概要](purchase-order-overview.md)

[発注書の承認と確認](purchase-order-approval-confirmation.md)

[発注書に対する製品受領書](product-receipt-against-purchase-orders.md)

[仕入先請求書の概要](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]