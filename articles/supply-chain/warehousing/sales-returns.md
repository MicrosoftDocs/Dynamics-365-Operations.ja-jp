---
title: 販売返品
description: この記事では、返品注文のプロセスについての情報について説明します。 これは顧客の返品に関する情報、および返品による原価計算と手持在庫数量への影響に関する情報が含まれます。
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReturnTableListPage, ReturnTable, ReturnTableListPagePreviewPane, ReturnTableReferences, SalesReturnExpiredOrdersPart, SalesReturnFindOrderFormPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.assetid: 98a4b517-e606-4036-b55f-1ab248898bdf
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e8045ec39b9caf9bf0dc2b2d331419efb54e6d6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860409"
---
# <a name="sales-returns"></a>販売返品

[!include [banner](../includes/banner.md)]

この記事では、返品注文のプロセスについての情報について説明します。 これは顧客の返品に関する情報、および返品による原価計算と手持在庫数量への影響に関する情報が含まれます。

顧客はさまざまな理由で品目を返品できます。 たとえば、品目に欠陥があるかもしれず、または品目が顧客の期待に応えない場合もあります。 返品プロセスは、顧客が品目の返品要求を発行するとき開始します。 顧客の要求を受領後、返品注文が作成されます。

## <a name="return-order-process"></a>返品注文のプロセス
次の図は、返品注文プロセスの概要を表示します。  

[![返品注文のプロセス。](./media/salesreturns01.jpg)](./media/salesreturns01.jpg)  

返品注文プロセスの 2 つのタイプがあります: 現物返品および貸方のみ。

-   **現物返品** – 返品注文は商品の現物返品を承認します。
-   **貸方のみ** – 返品注文は顧客の貸方を承認しますが、顧客が商品を現物返品することを要求はしません。

### <a name="physical-return-order-process"></a>現物返品注文のプロセス

1.  **返品注文を作成します。** 顧客が、欠陥のあるまたは不要になったどんな製品でも返品するのを認証する正式書類を提供します。 返品注文は、会社が返品商品を受け入れるまたは顧客に与信を提供することを要求しません。 返品が受理されると、欠陥品目が返却される前に交換品目を送付するよう承認できます。
2.  **検査のため倉庫に入庫します。** 返品注文ドキュメントに対する初期検査および検証を完了します。 返品注文は、追加検査および品質テスト用に返品品目の検疫もサポートします。
3.  **廃棄するかを決定します。** 検査プロセスを終了し、返品商品をどうすべきか決定します。 この手順の一部として、顧客の貸方に記入するか、製品の返品を拒否するか、または製品の返品を受け入れ製品を処分し顧客に代替品を送付するかどうかを決定します。
4.  **梱包明細を生成します。** 梱包明細を生成し、手順 3 で作成した廃棄に関する決定を確定します。 物流プロセスを終了します。
5.  **請求書を生成します。** 返品注文を完了します。

### <a name="credit-only-process"></a>貸方のみプロセス

1.  **返品注文を作成します。** 顧客が、欠陥のあるまたは不要になった製品を返品せずに貸方を受け取るのを認証する正式書類を提供します。 **貸方のみ** 廃棄コードは、現物返品なしで顧客に貸方を記入する決定を認証します。
2.  **請求書を生成します。** 訂正票を生成し、返品注文を終了します。

## <a name="return-material-authorization"></a>返品確認 
返品確認 (RMA) プロセスは販売注文の機能に基づきます。 RMA は販売注文として作成される返品注文として登録され、交換注文と呼ばれる別の販売注文に関連付けられるかもしれません。 販売注文は両方とも発生元の RMA 番号にリンクしています。

-   **返品注文** – RMA を登録するには、返品注文を作成します。それは割り当てられているタイプ、**返品注文。** がある販売注文です。 RMA 情報を変更すると、販売注文が自動的に更新されます。 販売注文の状態が **未処理** になるまでは、販売注文の一覧は表示されません。 返品品目の着荷と入庫を扱ったり、貸方のみの処分アクション (**廃棄コードおよび処分アクション** セクションを参照してください) を承認するのに RMA を使用します。 他のすべてのフォローアップ プロセスは、販売注文で処理する必要があります。
-   **交換注文** – 交換注文を顧客に出荷する必要のある場合は、RMA が 2 つ目の関連する販売注文を含めることができます。 迅速な出荷をサポートするため、手動で RMA の交換注文を作成できます。 または、着荷、検査後に交換注文を自動的に作成でき、交換を表示する廃棄コードを伴う RMA 明細行品目での入庫が完了します。 交換注文には、販売注文と関連付けられる同じ機能があります。 たとえば、交換品目としてカスタム製品をコンフィギュレーションしたり、返品品目を修理するため製造オーダーを作成したり、仕入先からの交換品を送付するため直納の発注書を作成、またはそのほかの目的をサポートするのに交換注文を使用できます。

## <a name="create-a-return-order"></a>返品注文の作成
返品注文プロセスは、顧客がユーザー組織に、欠陥または不要な製品を返品する、または貸方に記入するよう連絡してきたときに開始されます。 組織が返品を受理した後、返品が返品注文によって記載されます。 この返品注文は返品される製品の内部プロセスの焦点となります。 次の図は、返品注文を作成するための手順を示します。  

[![返品注文を作成する手順。](./media/salesreturn02.png)](./media/salesreturn02.png)

### <a name="create-a-return-order-header"></a>返品注文ヘッダーの作成

返品注文を作成すると、次の表の情報が含まれる必要があります。

| フィールド              | 説明                                              | コメント                                                                                                                                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 顧客口座   | 顧客テーブルへの参照                       | 既存の顧客 ID を指定する必要があります。                                                                                                                                                                                                                                                                                                  |
| 配送先住所   | 品目が返却される住所                 | 既定では、組織の住所が使用されます。 特定の倉庫がヘッダーで選択されている場合、配送先住所は倉庫の配送先住所に変更されます。 **返品注文の詳細** ページで住所を変更できます。                                                                                                  |
| サイト/倉庫     | 返品製品を受け取るサイトまたは倉庫 | 返品注文の配送先住所は、サイトまたは倉庫の配送先住所に基づいて決定されます。                                                                                                                                                                                                                                 |
| RMA 番号         | 返品注文に割り当てられている ID              | RMA 番号は、返品注文プロセス全体の代替キーとして使用されます。 割り当てられた RMA 番号は、**売掛金勘定パラメータ** ページで設定される RMA 番号順序に基づきます。                                                                                                                              |
| 期日           | 品目が返品できる最終日付               | 現在の日付プラス有効期間として既定値が計算されます。 たとえば、返品注文が作成された日付から 90 日間のみ返品が有効な場合、返品注文が 5 月 1 日に作成されるとフィールド値は **7 月 30日** となります。 有効期間は **売掛金勘定パラメータ** ページで設定されます。 |
| 返品理由コード | 製品の返品に対する顧客の理由          | 理由コードは、ユーザー定義の理由コードの一覧で選択されます。 このフィールドはいつでも更新できます。                                                                                                                                                                                                                                    |
### <a name="create-return-order-lines"></a>返品注文明細行の作成

返品ヘッダーの完了後、次の方法の 1 つを使用して返品明細行を作成できます。

-   手動で各返品明細行の品目の詳細、数量または他の情報を入力します。
-   **販売注文の検索** 機能を使用して返品明細行を作成します。 返品注文を作成するときに、この機能を使用することをお勧めします。 **販売注文の検索** 機能は返品明細行から請求済の販売注文明細行への参照を設定し、品目番号、数量、価格、割引、および販売明細行からの原価値などの明細行の詳細を取得します。 参照ヘルプは、製品が会社に返品された場合でも、販売された時と同じ単位原価で評価されることを保証します。 参照は、返品注文が請求書で販売された数量を超える数量に対して作成されていないことも確認します。

>[!NOTE] 
>販売注文への参照がある返品明細行は、販売の訂正、または取消として処理されます。 詳細については、この記事の後半の「元帳への転記」セクションを参照してください。

### <a name="charges"></a>諸費用

手数料、および雑費は以下の 1 つ以上の方法で返品注文に追加することができます。

-   返品注文ヘッダー、返品注文明細行、または両方に手動で雑費を追加できます。
-   雑費は、返品理由コードの機能として返品注文ヘッダーに自動的に追加できます。
-   雑費は、明細行の廃棄コードに基づいて返品注文明細行に自動的に追加できます。

雑費は、返品理由コードまたは廃棄コードが明細行に割り当てられた後に自動的に追加されます。 理由コードが後に変更された場合は、既存の雑費エントリは削除されません。ただし新しい雑費エントリは新しい理由コードに基づいて追加される可能性があります。 返品注文明細行に雑費を追加すると、割合が負の値でないかぎり、明細行の割合として雑費が計算されるか、または明細行や注文明細行が負である場合に注文値が負になります。 負の値がある雑費は、顧客への貸方を表します。

### <a name="return-reason-codes"></a>返品理由コード

返品の理由コードを適用して、分析するための返品パターンを容易にすることができます。 理由コードは顧客がなぜ品目を返品するかに関する情報を提供します。 いくつかの組織には多くの理由コードがあります。 これらの組織は、正確な概要を取得したり、または累計レポートのため理由コード グループに理由コードをグループ化するかもしれません。

### <a name="disposition-codes-and-disposition-actions"></a>廃棄コードおよび処分アクション

返品注文プロセスの重要なステップは、着荷登録として返品注文明細行に廃棄コードを割り当てることです。 廃棄コードにより、次の情報を決定します。

-   **財務的影響** – 顧客は返品品目に対して貸方に記入されるべきですか、またはどんな雑費も返品注文明細行に追加されるべきですか。
-   **返品品目の廃棄** – 品目は在庫に追加される、処分される、または顧客に返品されるべきですか。
-   **返品品目の物流** – 交換品目は顧客に発行されるべきですか。

返品商品がどのように処分されるかを決定するのに加え、廃棄コードは、返品明細行に適用されるべき雑費をもたらすこともできます。 統計分析用に返品をグループ化するのにも使用できます。 廃棄コードは、返品注文の設定の一部として定義されます。 ただし、各廃棄コードは組み込みの処分アクションの 1 つを参照する必要があります。 次の表に、組み込みの処分アクションとそのアクションの一覧を示します。 **重要:** 品目が返品される必要がない場合でも、顧客は貸方に記入されるべきで、**貸方のみ** 廃棄コードを返品明細行に割り当てます。

<table>
<thead>
<tr class="header">
<th>廃棄コード</th>
<th>財務影響</th>
<th>物流への影響</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>貸方のみ</td>
<td><ul>
<li>顧客には、販売価格から手数料または雑費を差し引いた金額が貸方記入されます。</li>
<li>品目を処分した際の損失が元帳に転記されます。</li>
</ul></td>
<td>品目は返品しないでください。 この廃棄アクションは、次の場合に使用されます。
<ul>
<li>関係者間に十分な信頼があります。</li>
<li>欠陥品目を返品する費用は禁止されています。</li>
<li>品目を在庫に戻すことは&#39;できません。 その他の条件ゆえに、現物返品は必要では&#39;ありません。</li>
</ul></td>
</tr>
<tr class="even">
<td>クレジット</td>
<td><ul>
<li>顧客には、販売価格から手数料または雑費を差し引いた金額が貸方記入されます。</li>
<li>返品品目の原価により在庫金額が増加されます。</li>
</ul></td>
<td>品目が返品されると、在庫に追加されます。</td>
</tr>
<tr class="odd">
<td>置換と貸方転記</td>
<td><ul>
<li>顧客には、販売価格から手数料または雑費を差し引いた金額が貸方記入されます。</li>
<li>返品品目の原価により在庫金額が増加されます。</li>
<li>交換用の別の販売注文が作成され、別個に処理されます。</li>
</ul></td>
<td>品目が返品されると、在庫に追加されます。</td>
</tr>
<tr class="even">
<td>置換と仕損</td>
<td><ul>
<li>顧客には、販売価格から手数料または雑費を差し引いた金額が貸方記入されます。</li>
<li>品目を処分した際の損失が元帳に転記されます。</li>
<li>交換用の別の販売注文が作成され、別個に処理されます。</li>
</ul></td>
<td>品目が返品および処分されます。</td>
</tr>
<tr class="odd">
<td>顧客に戻る</td>
<td>手数料または雑費以外は何もありません。</td>
<td>品目は返品されますが、検査後に顧客に送り返されます。 この処分アクションは、品目が意図的に破損されたり、または保証が無効になった場合に使用されるかもしれません。</td>
</tr>
<tr class="even">
<td>仕損</td>
<td><ul>
<li>顧客には、販売価格から手数料または雑費を差し引いた金額が貸方記入されます。</li>
<li>品目を処分した際の損失が元帳に転記されます。</li>
</ul></td>
<td>品目が返品または処分されます。</td>
</tr>
</tbody>
</table>

## <a name="arrival-at-the-warehouse-for-inspection"></a>検査のため倉庫に着荷
梱包明細の転記によって、在庫で物理的に返品品目を受け取れるようになる以前に、品目は着荷登録およびオプション検査を経る必要があります。 次の図は、着荷プロセスの概要を表示します。 次のセクションでは、図で表示される各ステップについて説明します。  

[![着荷プロセス。](./media/salesreturn03.png)](./media/salesreturn03.png)  

プロセスには、この記事では対象にならない他の複数の変動があります。 次に変動の例を示します。

-   着荷仕訳帳を作成するために **着荷の概要** の一覧を使用しないでください。 代わりに、手動で着荷仕訳帳を作成します。 返品注文では、**販売注文** を参照できます。
-   倉庫管理を使用して、パレット配送を生成します。 返品明細行は、パレット配送時に **着荷済** の状態になります。
-   **登録** 機能を使用して、返品注文明細行からの返品品目の着荷を直接に登録します。

着荷プロセス中に、返品は、倉庫への着荷の一般的なプロセスに統合されます。 着荷プロセスは、別の検査を経るべき返品品目の検査指示の作成もサポートします。

### <a name="identify-products-in-the-arrival-overview-list"></a>着荷の概要一覧の製品を識別します

**着荷の概要** ページは、すべての計画された入庫の到着を一覧表示します。

>[!NOTE] 
>返品注文の着荷は、ほかのタイプの着荷トランザクションとは別に処理する必要があります。 **着荷の概要** ページ (たとえば、RMA 添付ドキュメントを使用して) で着信パッケージを識別したのち、アクション ウィンドウで **着荷開始** をクリックして着荷に適合する着荷仕訳帳を作成および初期化します。

### <a name="edit-the-arrival-journal"></a>着荷仕訳帳を編集します

**検査管理** オプションを **はい** に設定して、返品明細行の検査指示を作成できます。 明細行が点検用の検査に送信され場合、廃棄コードを指定することはできません。 
 
**検査管理** オプションを **はい** に設定すると、**仕訳帳明細行** ページの **検査管理** オプションが着荷仕訳帳明細行に対してマークされ、変更することはできません。 明細行が検査に送られる場合、適切な検査倉庫を指定する必要があります。 

着荷明細行が検査に送られない場合、倉庫の着荷係が着荷仕訳帳明細行の廃棄コードを直接指定し、着荷仕訳帳を転記する必要があります。 同じ廃棄コードが返品明細行の全数量に割り当てられるべきでない、または明細行の全数量を受け取っていない場合、明細行を分割する必要があります。 着荷仕訳帳明細行を分割すると、返品明細行 (**SalesLine**) も分割し、新しいロット ID を作成します。 着荷仕訳帳明細行の数量を小さくすることにより明細行を分割できます。 仕訳帳を転記すると、残余数量が **予定** の状態になっている新しい返品明細行が作成されます。 **機能** &gt; **分割** をクリックすることで、明細行を分割することもできます。

### <a name="process-the-quarantine-order"></a>検査指示のプロセス

返品された製品が検査倉庫での検査に送信される場合、検査指示でどの追加の処理も完了となります。 1 つの検査指示が、検査に送られる各着荷明細行に対して作成されます。 廃棄コードが検査プロセスの結果を示します。 

着荷仕訳帳を分割できるのと同じように、検査指示を分割できます。 検査指示を分割する場合、返品明細行の対応する分割が引き起こされます。 廃棄コードを入力したのち、**終了** 機能または **完了レポート** 機能のいずれかを使用することにより、検査指示を完了します。 **完了レポート** を選択すると、指定された倉庫で新しい着荷が作成されます。 **着荷の概要** ページを使用して、この着荷を処理できます。 

着荷が検査指示から生成される場合、検査中に割り当てられた廃棄コードを変更することはできません。 **終了** 機能を使用して検査指示を完了すると、ロットが自動的に登録されます。 場合によっては、品目は検査から出荷および入荷部門に送り返されるかもしれません。 たとえば、検査担当者は在庫内のどこに品目が保管されているかわからないかもしれません。 この場合、正しく登録するよう、および検査によって指定された廃棄コードを正しく実行するよう、対応する梱包明細を更新する必要があります。 

返品明細行の登録時に、顧客に受領確認を送信できます。 **受信確認の返信** レポートは、返品注文ドキュメントと似ています。 **受信確認の返信** レポートは仕訳されておらず、そうでなくてもシステムに登録されていないため、返品注文プロセスの必須のステップではありません。

## <a name="replace-a-product"></a>製品の置き換え
製品交換を管理するための 2 つの方法があります。

-   **事前交換** – 顧客から返品製品を受け取る前に、製品を置き換えます。
-   **廃棄コードによる交換** – 自動的に新しい交換注文明細行を作成します。

### <a name="up-front-replacement"></a>事前交換

事前交換では、品目が返品される前に、交換品目を顧客に出荷することができます。 この方法は、たとえば、品目が機械部品で、代わりになる予備部品が利用可能でない限り取り外せない場合、または顧客にすぐにでも交換製品を必要とする場合に役に立ちます。 事前交換注文は、独立した販売注文です。 ヘッダー情報は顧客から初期化され、明細行情報は返品注文から初期化されます。 返品注文の交換注文を個別に編集し、処理し、または削除できます。 交換注文を削除すると、交換注文として注文が作成されたというメッセージが表示されます。 次の図は、事前交換のプロセスを示します。  

![事前交換プロセス。](./media/SalesReturn04.png)

返品注文には、交換注文への出典が含まれます。 欠陥品目の返品前に事前交換注文が返品注文に対して作成されている場合は、欠陥品目が返品された後に交換の廃棄コードを選択することはできません。

### <a name="replacement-by-disposition-code"></a>廃棄コードによる交換

顧客に交換品目を出荷し、返品注文の **置換と仕損** または **置換と貸方転記** 処分アクションを使用する場合、次の図に表示されるプロセスを使用します。  

![廃棄コード使用時の交換プロセス。](./media/SalesReturn05.png)

交換品目は、独立した販売注文、交換販売注文を使用して配送されます。 この販売注文は、返品注文の梱包明細が生成されると作成されます。 注文ヘッダーは、返品注文ヘッダーで参照される顧客からの情報を使用します。 明細行情報は **交換品目** ページで入力された情報から収集されます。 「交換」の語で始まる処分アクションのある明細行に対して **交換品目** ページが入力されている必要があります。 ただし、交換品目の数量または ID は検証されておらず、または限定されていません。 この動作は、顧客が異なるコンフィギュレーションまたはサイズの同じ品目が欲しい、および顧客が全く別の品目が欲しい場合に可能になります。 既定では、同一品目は **交換品目** ページで入力されます。 ただし、機能が設定されて提供された異なる品目を選択できます。 

>[!NOTE] 
>作成した後、交換販売注文を編集、または削除できます。

## <a name="generate-a-packing-slip"></a>梱包明細の生成
返品品目を在庫に入庫する前に、品目が属する注文の梱包明細を更新する必要があります。 請求書更新プロセスが財務トランザクションの更新であるのと同様に、梱包明細更新プロセスは在庫レコードの現物更新になります。 つまり、このプロセスは在庫の変更をコミットします。 返品の場合、処分アクションに割り当てられる手順は、梱包明細の更新中に実行されます。 梱包明細の生成時には、次のイベントが発生します。

-   倉庫では、現物入庫を実行するのに標準プロセスが使用されます。 元帳転記は、在庫モデル グループ (**現物在庫の転記**) および売掛金勘定パラメータ (**梱包明細を元帳に転記**) が適切に設定されると生成されます。　
-   「処分」の語を含む処分アクションにマークされた品目は処分され、在庫損失が元帳に転記されます。
-   **顧客に戻る** 処分アクションでマークされた品目は受領され、顧客に配送されます。 これらの品目には、在庫での正味効果はありません。
-   交換販売注文が作成されました。 この販売注文は **交換品目** ページの情報に基づきます。

**登録済** の返品のステータスがある明細行にのみ、および返品明細行での全数量に対してのみ梱包明細を生成できます。 返品注文の複数の明細行に **登録済** ステータスがある場合、**梱包明細の転記** ページからほかの明細行を削除することにより、明細行のサブセットの梱包明細を生成できます。 

部分返品は、返品注文の出荷に対してではなく返品注文明細行に対して定義されます。 したがって、返品注文内の 1 つの返品注文明細行に示された全数量が入荷し、他の明細行の全数量が入荷しない場合は、分納ではありません。 これに対して、たとえば、1 つの返品注文明細行に品目を 10 単位返品するよう指定されているのに 4 単位だけ入荷した場合は、その出荷は分納です。 すべての予定返品品目が着荷していない場合、出荷は無視して、残りの返品数量が着荷するのを待機できます。 または、部分的な数量を登録および転記できます。 梱包明細の転記プロセスの一環として、顧客の出荷ドキュメントに記載されている梱包明細参照番号を注文明細行に関連付けることができます。 このアソシエーションはオプションであり、また参照専用です。 これによってトランザクションの更新は行われません。 

一般に、梱包明細プロセスをスキップし、請求に直接移動することができます。 この場合、梱包明細の生成時に実行した手順は、請求の際に完了します。

## <a name="generate-an-invoice"></a>請求書の生成
**返品注文** ページは、返品注文の特別な物流の側面を処理するのに必要な情報及びアクションを含みますが, **販売注文** ページを使用して請求プロセスを完了する必要があります。 組織は、返品注文と販売注文の請求を同時に行うことができ、必要に応じて同じ担当者が請求プロセスを完了できます。 **販売注文** ページから返品注文を表示するには、販売注文数のリンクをクリックして関連する販売注文を開きます。 **すべての販売注文** ページで返品注文を検索することもできます。 返品注文は **返品注文** の注文タイプのある販売注文です。

### <a name="credit-correction"></a>貸方訂正

請求プロセスの一部として、雑費が正しいことを確認します。 元帳転記が訂正 (Storno) となるよう、請求書または訂正票を転記する際に **請求の転記** ページの **その他** タブで **貸方訂正** オプションを使用することを考慮してください。

> [!NOTE]
> 既定では、**売掛金勘定パラメーター** ページで **修正用訂正票** オプションが有効になっている場合、**貸方訂正** オプションは有効化されます。 ただし、Storno で返品を転記しないことをお勧めします。

## <a name="create-intercompany-return-orders"></a>会社間返品注文の作成 
返品注文は組織内の 2 つの会社間で完了されます。 サポートされているシナリオは次のとおりです。

-   会社間関係に関与する 2 つの会社間の簡単な会社間返品
-   顧客の返品注文が販売会社で作成されるときに確立される会社間グループ
-   仕入先の返品注文が仕入元会社で作成されるときに確立される会社間グループ
-   外部顧客と、会社間関係に関与する 2 つの会社間の直納の出荷返品

### <a name="setup"></a>段取り

次の図は 2 つの会社が会社間関係に関与し、会社間取引を活用するのに必要な最小限の設定です。  

![最小限の設定。](./media/SalesReturn06.png)

次のシナリオでは、CompBuy は仕入元会社で、CompSell は販売会社です。 通常、販売会社が仕入元会社に、または直納の出荷シナリオでは、直接最終顧客に商品を出荷します。 CompBuy で、仕入先 IC\_CompSell は、会社 CompSell に関連付けられる会社間エンドポイントとして定義されます。 同時に CompBuy で、顧客 IC\_CompSell は、会社 CompBuy に関連付けられる会社間エンドポイントとして定義されます。 適切なアクション ポリシーの詳細および値のマッピングは、両方の会社で定義される必要があります。 直納の出荷シナリオでは、会社間販売注文でもある会社間返品注文は販売会社で作成されます。 会社間返品注文の RMA 番号は、CompSell の RMA 整理番号から選択できます。または CompBuy の元の返品注文に割り当てられた RMA 番号からコピーすることができます。 CompBuy の **PurchaseRequisition** アクション ポリシーの RMA 番号設定がこれらのアクションを決定します。 RMA 番号が同期しているなら、2 つの会社が同じ整理番号を使用する場合の数の衝突リスクを軽減するよう計画する必要があります。

### <a name="simple-intercompany-returns"></a>簡易な会社間返品

次の図に示すように、このシナリオには、同じ組織内の 2 つの会社が含まれます。  

![簡易な会社間返品。](./media/SalesReturn07.png)

注文チェーンは、仕入先の返品注文が仕入元会社で作成されるか、または顧客の返品注文が販売会社で作成されるときに確立されます。 対応する注文がほかの会社で作成され、仕入先の返品注文のヘッダーおよび明細行情報が顧客の返品注文の設定を反映するようにします。 設定された返品注文は、既存の顧客請求書への参照 (**販売注文の検索**) を含める、または除外することができます。 2 つの注文の梱包明細と請求は、個別に処理されます。 たとえば、顧客の返品注文の梱包明細を生成する前に、仕入先の返品注文の梱包明細を生成する必要はありません。

### <a name="direct-delivery-shipment-returns-among-three-parties"></a>3 つの関係者間の直納の出荷返品

このシナリオは、**直納** タイプの前回の販売が完了した場合、および顧客と連携する会社で顧客に対する請求が存在する場合に確立されます。 次の図では、会社 CompBuy は顧客 Extern に対して、過去に販売し請求した製品があります。 製品は、会社間注文チェーンを介して会社 CompSell から顧客に直接出荷されました。  

![3 つの関係者間の直納の出荷返品。](./media/SalesReturn08.png)

顧客 Extern が製品を返品する場合は、返品注文 (RMA02) が、会社 CompBuy で顧客に対して作成されます。 会社間グループを確立するには、返品注文が直納用にマークされる必要があります。 **販売注文の検索** 機能を使用して顧客請求書を返品するよう選択する場合、次のドキュメントで構成される会社間注文チェーンが確立されます。

-   **元の返品注文:** RMA02 (会社 CompBuy)
-   **発注書:** PO02 (会社 CompBuy)
-   **会社間返品注文:** RMA\_00032 (会社 CompSell)

直納の会社間グループが作成されたのち、返品のすべての物理的な処理およびプロセスは、会社間返品注文のコンテキスト、会社 CompSell の RMA\_00032 で実行する必要があります。 製品は、会社 CompBuy には入庫されません。 廃棄コードが会社間返品注文に割り当てられると、元の注文の適切な請求を許可するよう元の返品注文と同期されます。

## <a name="post-to-the-ledger"></a>元帳への転記
返品注文の請求時に生成される元帳転記は、いくつかの重要な設定とパラメータによって影響を受けます。

-   **返品原価価格** – **標準原価** 以外の在庫モデル用に、**返品原価価格** パラメータは、在庫として受け入れられたかまたは処分された品目の原価を決定します。 在庫の正確な評価を計算するため、**返品原価価格** パラメータを正確に設定することが重要です。 **販売注文の検索** 機能を使用して顧客請求書への参照がある返品注文明細行を作成すると、**返品原価価格** 値が販売された品目の原価価格と等しくなります。 それ以外の場合、原価価格の値は品目設定から取得されるか、または手動で入力されます。
-   **貸方訂正/Storno** – **請求の転記** ページで **貸方訂正** パラメータは、転記がプラス (DR/CR) 入力または訂正としてマイナス入力と記録すべきかどうかを決定します。

次の例では、返品原価価格は **Inv. Cost price** として表されます。

### <a name="example-1-the-return-order-doesnt-reference-a-customer-invoice"></a>例 1: 返品注文は顧客請求書を参照しません

返品注文は顧客請求書を参照しません。 返品品目が貸方に転記されます。 返品注文請求書または訂正票が生成されるとき、**貸方訂正** パラメータは選択されません。  

![返品注文は顧客請求書を参照しません。](./media/SalesReturn09.png)  

> [!NOTE]
> 品目マスターの価格が **返品原価価格** パラメーターの既定値として使用されます。 既定の価格は、在庫払出時に原価価格と異なります。 したがって、3 つの損失が発生するという影響が生じます。 さらに、返品注文には、販売注文で顧客に適用された割引は含まれません。 したがって、過大な貸方が発生します。

### <a name="example-2-credit-correction-is-selected-for-the-return-order"></a>例 2: 貸方訂正が返品注文に対して選択されます

例 2 は例 1 と同じですが、返品注文請求書が生成されると **貸方訂正** パラメータが選択されます。  

![貸方訂正が選択されている返品注文。](./media/SalesReturn10.png)  

>[!NOTE] 
>元帳転記がマイナス修正として入力されます。

### <a name="example-3-the-return-order-line-is-created-by-using-the-find-sales-order-function"></a>例 3: 返品注文明細行は販売注文の検索機能を使用して作成されます

この例では、返品注文明細行は **販売注文の検索** 機能を使用して作成されます。 **貸方訂正** パラメータは、請求書の作成時に選択されません。  

![販売注文の検索を使用して作成される返品注文明細行。](./media/SalesReturn11.png)  

> [!NOTE]
> **割引** および **返品原価価格** が正確に設定されます。 したがって、顧客請求書の的確な取消が発生します。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]