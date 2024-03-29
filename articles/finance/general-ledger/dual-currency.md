---
title: 二重通貨
description: この記事では、レポート通貨が Microsoft Dynamics 365 Finance の 2 番目の会計通貨として使用されている二重通貨に関する情報を提供します。
author: kweekley
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 19337b2651830d79543361d525bf24c4f794e825
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065749"
---
# <a name="dual-currency"></a>二重通貨

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance バージョン 8.1 (2018 年 10 月) で導入された機能は、レポート通貨の別目的での使用および 2 番目の会計通貨としての使用を有効にします。 この機能は、*二重通貨* と呼ばれます。 二重通貨の変更を、コンフィギュレーション キーまたはパラメーターを通じて無効にはできません。 レポート通貨が 2 つ目の会計通貨として使用され、転記論理でのレポート通貨の計算方法が変更されたためです。

さらに、複数のモジュールが、さまざまなプロセスでレポート通貨を追跡、レポート、および使用するよう強化されました。 影響を受けるモジュールは、次のとおりです。

- 一般会計 
- 財務諸表 
- 買掛金勘定
- 売掛金勘定 
- 現金および銀行管理 
- 固定資産 
- 連結

アップグレード後に、現金および銀行管理と固定資産の特定の手順を完了する必要があります。 したがって、この記事の関連するセクションを必ずお読みください。

## <a name="posting-process"></a>転記プロセス

総勘定元帳への勘定項目を生成するすべてのトランザクションに対して、転記ロジックが変更されました。 レポート通貨の以前の計算方法を以下に示します。

トランザクション通貨金額 \> 会計通貨金額 \> レポート通貨金額

たとえば、トランザクションはカナダ ドル (CAD) 通貨で入力されます。 CAD の金額は、米ドル (USD) である会計通貨に換算されます。 それから USD の金額は、ユーロ (EUR) であるレポート通貨に換算されます。 したがって、CAD と USD 間、および USD と EUR 間には為替レートが存在している必要があります。

新しい計算を次に示します。

トランザクション通貨金額 \> 会計通貨金額

トランザクション通貨金額 \> レポート通貨金額

この変更により、CAD と USD 間、および CAD と EUR 間に為替レートが存在している必要があります。

## <a name="reports-and-inquiries"></a>レポートおよび照会

さまざまなレポートや照会では、レポート通貨金額および会計通貨金額の両方が表示されます。 すべてのレポートおよび照会が更新されているわけではありません。 たとえば、トランザクション通貨でのみ金額を表示するレポートは変更されていません。

変更は、2 つのパターンのいずれかに従って実行されます。

- レポートまたは照会に、会計通貨とレポートの通貨の両方で金額を表示する十分な領域があった場合には、レポート通貨金額が追加されました。
- レポートまたは照会に、両方の通貨で金額を表示する十分な領域がなかった場合には、ユーザーがどの通貨で表示するかを選択できるようオプションが追加されました。

さまざまなレポートおよび照会で、レポート通貨が会計通貨と同じである場合、またはレポート通貨が法人の元帳で定義されていない場合、レポート通貨金額を非表示にするロジックも追加されました。

## <a name="financial-journals"></a>財務仕訳帳

一般仕訳帳および仕入先請求仕訳帳などの財務仕訳帳が、レポート通貨に関する追加情報が含まれるよう更新されています。 伝票および仕訳帳の合計はレポート通貨で表示されます。 さらに、レポート通貨の為替レートに関する情報は、仕訳帳明細行の **一般** タブで表示されるようになります。 したがって、トランザクションを入力するときに、レポート通貨の為替レートを上書きできます。

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>仕入先請求書、販売注文、および販売契約書
仕入先請求書、販売注文、および販売契約書が更新され、レポート通貨に固定為替レートが含まれるようになりました。 固定為替レートは、トランザクション通貨が異なる場合に、会計通貨とレポート通貨の両方に対して定義できます。 会計通貨とレポート通貨が同じである場合、固定為替レートは、会計通貨の固定レートをレポート通貨の固定レートとして使用することによって、同期されたままになります。 このコンフィギュレーションでは、レポート通貨の固定為替レートを変更できません。 会計通貨とレポート通貨が異なる場合には、トランザクションの入力中、固定為替レートを会計通貨とレポート通貨の両方に対して定義できます。 元帳にレポート通貨が定義されていない場合は **レポート通貨の固定為替** フィールドは有効にならず、レポート通貨金額は計算されません。

## <a name="module-changes"></a>モジュール変更

以下のモジュールでは、2 つ目の会計通貨としてレポート通貨を使用します。

- [一般会計](#general-ledger)
- [財務報告](#financial-reporting)
- [買掛金勘定](#accounts-payable-and-accounts-receivable)
- [売掛金勘定](#accounts-payable-and-accounts-receivable)
- [現金および銀行管理](#cash-and-bank-management)
- [固定資産](#fixed-assets)
- [連結](#consolidations)

### <a name="general-ledger"></a>一般会計

レポート通貨が元帳で定義されている場合、総勘定元帳は既に各勘定項目でレポート通貨金額を追跡していました。 ただし、それらの値はトランザクション通貨金額から換算されるようになります。

次の追加変更は、**総勘定元帳** モジュールで加えられました。

- 元帳では、レポート通貨に対する異なる為替レート タイプを定義できます。 組織が異なる為替レート タイプを使用しない場合、レポート通貨の為替レート タイプのフィールドを空白のままにしておきます。 または、会計通貨に使用される同じ為替レート タイプを選択できます。 フィールドを空白のままにすると、システムでは会計通貨の為替レート タイプが使用されます。
- 新しい仕訳帳であるレポート通貨の調整仕訳帳では、レポート通貨のみで勘定科目に転記されるための調整を有効にします。 この仕訳帳は、勘定科目のみへの転記を有効にします。 会社間はサポートされませんし、通貨は、仕訳帳が転記される法人のレポート通貨である必要があります。 仕訳帳が転記されると、トランザクション通貨および会計通貨金額が 0 (ゼロ) となり、レポート通貨金額はトランザクションで入力される金額で転記されます。 レポート通貨が **買掛金勘定**、**売掛金勘定**、および **固定資産** モジュールで使用される方法が変更されたため、この仕訳帳はアップグレード後に調整用に使用されます。 この仕訳帳の使用方法を示す例では、それらのモジュールのセクションを参照してください。
- 期間割り当てのプロセスは、トランザクション、会計、およびレポート通貨で金額を配賦できるように更新されました。 以前では、トランザクションおよび会計通貨で金額が配賦されてから、会計通貨金額がレポート通貨に変換されていました。 その動作により、残高がレポート通貨の勘定科目に残る可能性がありました。 これで、金額が計算され勘定項目で使用されても、換算は行われません。
- 外貨再評価のプロセスで、すでにレポート通貨の金額が再評価されました。 ただし、この記事で前述した [転記プロセス](#posting-process) セクションの手順に従って、レポート通貨金額はトランザクション通貨金額から計算されるようになります。
- 総勘定元帳の多くのレポートおよび照会には既にレポート通貨がありましたが、いくつかにはレポート通貨がありませんでした。 1 つの例は、**試算表** リスト ページです。 このリスト ページには、会計通貨とレポート通貨の両方の列が含まれるようになります。 会計通貨とレポート通貨が同じで、またはどのレポート通貨も元帳で定義されていない場合は、レポート通貨の列が非表示になっていることに注意してください。

### <a name="financial-reporting"></a>財務諸表

**財務報告** モジュールへの拡張により、2 つの方法でレポート通貨金額を財務諸表に含めることができます。 列の定義では、 元帳 (新しい機能) に転記されるレポート通貨金額に直接報告できます。 または、会計通貨からの金額をレポート通貨 (既存の機能) への変換を続行できます。

この変更は、列定義の **通貨の表示** 設定を通じて使用可能です。 **元帳のレポート通貨** を選択した場合、列の金額は変換されません。 代わりに、総勘定元帳から直接報告されます。 列が変換された金額を表示するようにするには、**XXXX に変換** オプションを選択します。この場所、*XXXX* は、列を表示する必要があるレポート通貨です。 この場合、既存の変換機能を使用して、会計通貨金額は選択した通貨に変換されます。

### <a name="accounts-payable-and-accounts-receivable"></a>買掛金勘定および売掛金勘定

**買掛金勘定** および **売掛金勘定** モジュールは、既にレポート通貨金額を追跡しています。 ただし、金額が表示されなかったり、またはさまざまなプロセスに使用されています。 次の変更が加えられました。

- レポート通貨金額は、顧客および仕入先の両方のトランザクションに対して表示されます。 レポート通貨金額は各トランザクションの未処理残高に対しても表示されます。
- エイジング プロセスは、組織が会計通貨またはレポート通貨のいずれかでエイジング バケットを表示できるように更新されました。
- さまざまな照会やレポートは、レポート通貨金額が表示されるように更新されました。 **顧客と元帳間の調整** および **仕入先と元帳間の調整** レポートなどがその例です。
- 外貨再評価のプロセスで、すでにレポート通貨の金額が再評価されました。 ただし、[転記プロセス](#posting-process) セクションの手順に従って、レポート通貨金額はトランザクション通貨金額から計算されるようになります。
- **アップグレードの考慮事項:** アップグレード前に、会計通貨を通じてドキュメント (請求書や支払など) のレポート通貨金額が計算されます。 例えば、組織のアップグレード前に請求書が転記され、請求書の支払はありません。 アップグレードの際、請求書の勘定項目は変更されません。 ただし、アップグレード後に、二重通貨の変更が有効になります。 したがって、請求書の支払が行われると、支払のレポート通貨金額はトランザクション通貨金額を通じて計算されるようになります。 レポート通貨金額が別々に計算されるようになったため、支払および請求書の決済時に、実現利益/損失金額のわずかな差が計算される可能性があります。 計算された差異が重要と見なされる場合、新しいレポート通貨の調整仕訳帳は、レポート通貨のみで実現利益/損失および勘定買掛金勘定/売掛金勘定の勘定科目の残高を調整するために使用できます。

### <a name="cash-and-bank-management"></a>現金および銀行管理

以前に、**現金および銀行管理** モジュールでは、各銀行口座に対して転記されたトランザクションのレポート通貨金額を追跡しませんでした。 アップグレード後は、任意の新しいトランザクションに対して、レポート通貨金額が自動的に追跡されます。 ただし、補助元帳で以前に転記されたトランザクションに、レポート通貨金額が追加される必要があります。

- **アップグレードの考慮事項:** 以前に銀行口座トランザクションは補助元帳のレポート通貨金額を追跡していなかったため、レポート通貨金額を銀行口座トランザクションに追加できるよう、ウィザードが追加されました。 このウィザードは今後、総勘定元帳には転記 **しません**。 代わりに、総勘定元帳からレポート通貨金額を受け取り、補助元帳テーブルでそれらを更新します。

    - ウィザードを開始するには、**現金および銀行管理** \> **設定** \> **銀行口座トランザクションのレポート通貨金額を追加する** の順に選択します。
    - ウィザードでは、0 (ゼロ) のレポート通貨金額のある現在の会社で、すべての銀行口座に対するトランザクションを表示します。 アップグレード前に転記されたトランザクションのみが含まれます。
    - 各銀行口座トランザクションについては、ウィザード総勘定元帳で対応する勘定項目を検索し、既定のレポート通貨金額を入力します。 金額は編集できますが、編集 **しない** ことをお勧めします。 それ以外の場合は、総勘定元帳への銀行口座残高を調整できない可能性があります。 レポート通貨金額が総勘定元帳に見つからない場合にのみ、金額を編集する必要があります。 その場合は、ウィザードではレポート通貨に対して 0 (ゼロ) の金額が表示されます。
    - ウィザードで **キャンセル** を選択する場合、銀行口座トランザクションおよびレポート通貨金額への任意の変更が、次回ウィザードを実行する時まで保存されます。 ただし、レポート通貨金額は銀行口座トランザクションで更新されません。 その更新は、ウィザードで **完了** を選択する場合にのみ実行されます。 ウィザードは、複数回実行できます。 したがって、間違えた場合、誤ったレポート通貨金額を修正できます。

- 現金および銀行管理のプロセスは変更されませんが、各種レポートや照会は、レポート通貨金額が表示されるように更新されました。 キャッシュ フロー予測レポートは、例外です。 レポート通貨金額を含めるようには更新されませんでした。

### <a name="fixed-assets"></a>固定資産

以前に、**固定資産** モジュールでは、各固定資産帳簿に対して転記されたトランザクションのレポート通貨金額を追跡しませんでした。 アップグレード後は、任意の新しいトランザクションに対して、レポート通貨金額が自動的に追跡されます。 ただし、補助元帳で以前に転記されたトランザクションに、レポート通貨金額が追加される必要があります。

さらに、減価償却プロセスに重要な変更が加えられました。 これらの変更により、アップグレード後にユーザー アクションが必要になります。 固定資産をまだ使用していない場合でも、次の変更についてよく読み理解しておくことが重要です。

- 減価償却プロセスがレポート通貨金額を決定する方法が変更されました。 次のシナリオでは、減価償却が以前にレポート通貨金額を決定した方法と、現在レポート通貨金額を決定する方法を比較します。



    **減価償却のシナリオ**

    資産が次の金額で取得および転記されます。 レポート通貨金額は総勘定元帳に転記されますが、固定資産の補助元帳テーブルには保存されないことに注意してください。

    | トランザクション タイプ | トランザクション金額 | 為替レート | 会計通貨金額 | 為替レート | レポート通貨金額 |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | 取得      | 1,000,000 DKK      | 2.0           | 500,000 USD                | 2.5           | 200,000 EUR               |

    **レポート通貨に対する前の減価償却**

    年度末には、減価償却の提案が実行され、次の金額を計算します。

    | トランザクション タイプ | トランザクション金額 | 為替レート | 会計通貨金額 | 為替レート | レポート通貨金額 |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | 減価償却     | 50,000 USD         | 1.0           | 50,000 USD                 | 2.6           | 19,230.77 EUR             |

    減価償却の提案が実行されると、減価償却方法を使用して会計通貨金額を計算します。 USD と EUR 間の現在の為替レートを使用して、レポート通貨への金額を変換します。 スポット レートが使用される場合、資産はレポート通貨で完全に減価償却できないため、この変換に問題が発生します。

    **レポート通貨に対する新しい減価償却**

    減価償却プロセスが変更されたため、レポート通貨金額も減価償却方法を使用して計算されるようになります。 減価償却が資産で実行された場合の結果を以下に示します。

    | トランザクション タイプ | トランザクション金額 | 為替レート | 会計通貨金額 | 為替レート                                                       | レポート通貨金額 |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | 減価償却     | 50,000 USD         | 1.0           | 50,000 USD                 | 2.5<blockquote>[!NOTE] この為替レートが表示されますが、レポート通貨への変換には使用されません。</blockquote> | 20,000 EUR                |

    減価償却の提案を実行する場合、減価償却方法を使用して、会計通貨金額およびレポート通貨金額の両方が計算されます。 金額は、総勘定元帳の勘定項目で使用されます。 レポート通貨金額を決定するために変換は行われません。

- **アップグレードの考慮事項:** 以前に固定資産帳簿トランザクションはレポート通貨を追跡していなかったため、レポート通貨金額を固定資産帳簿トランザクションに追加できるよう、ウィザードが追加されました。 このウィザードは今後、総勘定元帳には転記 **しません**。 減価償却の提案でレポート通貨金額を計算する方法が変更されたため、組織が任意の減価償却トランザクションを入力する前に、各会社に対してウィザードが実行および完了される **必要があり** ます。

    - ウィザードを開始するには、**固定資産** \> **設定** \> **レポート通貨金額を固定資産帳簿に追加する** の順に選択します。
    - ウィザードでは、0 (ゼロ) のレポート通貨金額のある現在の会社で、すべての固定資産帳簿に対するトランザクションを表示します。 アップグレード前に転記されたトランザクションのみが含まれます。
    - ウィザードでは、総勘定元帳からのレポート通貨金額を取得 **しません**。 前のシナリオで説明されたように、最初に総勘定元帳に転記されたレポート通貨金額は、間違ってスポット レートを使用します。 次の減価償却の計算が正しくない金額を使用するため、それらの金額は固定資産補助元帳には表示されません。 代わりに、ウィザードは最初の取得の日付で為替レートを検索します。 次にその為替レートを使用して、レポート通貨金額が補助元帳に転記されるよう推奨します。 例えば、前のシナリオに対して、ウィザードが何を表示する可能性があるかを示します。

        | 固定資産 | 予約      | トランザクション タイプ | 取引日付 | Currency | トランザクション通貨の金額 | 量  | 為替レート | レポート通貨金額 |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | 取得      | 2016 年 3 月 6 日         | DKK      | 1.000.000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | 減価償却     | 2016 年 3 月 6 日         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | 減価償却     | 2016 年 3 月 6 日         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | 減価償却     | 2016 年 3 月 6 日         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - 多くの顧客がワークブックで資産トランザクションの詳細を追跡しました。 これらの詳細には、為替レートおよび金額が含まれます。 ワークブックにこのデータがある場合、カスタム 為替レート タイプを作成し、およびワークブックからの為替レートで更新できます。 この為替レート タイプは、取得日付で既定の為替レートを入力し、レポート通貨金額を計算するために使用されます。 為替レートのタイプが選択されていない場合、ウィザードは元帳で定義された為替レート タイプを使用します。
    - 為替レートおよびレポート通貨金額は変更可能です。 為替レートが変更された場合は、新しいレートを使用してレポート通貨金額が再計算されます。
    - ウィザードで **キャンセル** を選択する場合、固定資産帳簿トランザクションおよび為替レートへの任意の変更、またはレポート通貨金額が次回ウィザードを実行する時まで保存されます。 ただし、レポート通貨金額は固定資産帳簿トランザクションで更新されません。 その更新は、ウィザードで **完了** を選択する場合にのみ実行されます。 ウィザードは、複数回実行できます。 したがって、間違えた場合、誤ったレポート通貨金額を修正できます。
    - レポート通貨金額が補助元帳で完全に更新される場合、**固定資産帳簿トランザクションにおけるすべてのレポート通貨金額を更新しましたか** オプションを **はい** に設定し、**完了** を選択する **必要があり** ます。 **固定資産帳簿トランザクションにおけるすべてのレポート通貨金額を更新しましたか** オプションを **はい** に設定するまで、減価償却計算を完了することはできません。 そのオプションを **はい** に設定した後、ウィザードは使用できなくなります。
    - 補助元帳の固定資産トランザクションがレポート通貨金額で更新されると、それらの金額は総勘定元帳に最初に転記された金額と一致しません。 ただし、レポート通貨の調整仕訳帳は、総勘定元帳での減価償却勘定科目の残高を更新するために使用されます。それにより最初に転記された金額と一致するようになります。
    - **データ管理** ワークスペースに追加された新しい **資産トランザクションのレポート通貨金額** エンティティにより、ウィザードからのデータをエクスポートできます。 次に減価償却トランザクションに対する固定資産の補助元帳での残高を決定するために、そのデータを使用できます。 その残高は、総勘定元帳でレポート通貨の調整の金額を決定するために使用されます。

- **アップグレードの考慮事項:** 新しい設定フィールドが固定資産に追加され、減価償却の計算で使用されます。 次の減価償却計算の前にこれらのフィールドを更新する必要が生じる場合があります。

    - 固定資産帳簿 (**固定資産** \> **帳簿**) の、**一般** クイック タブには、新しい **レポート通貨での取得価格** フィールドがあります。
    - 固定資産帳簿 (**固定資産** \> **帳簿**) の、**減価償却** クイック タブには、新しい **レポート通貨での予定仕損価格** フィールドがあります。
    - 固定資産パラメータ (**固定資産** \> **設定** \> **固定資産パラメータ**) の、**一般** クイック タブには、新しい **レポート通貨での減価償却の最低金額** フィールドがあります。
    - 帳簿 (**固定資産** \> **設定** \> **帳簿**) の、**一般** クイック タブには、2 つの新しいフィールド: **レポート通貨での減価償却の丸め** および **レポート通貨で正味簿価額を残す** があります。

- 減価償却の提案により会計通貨およびレポート通貨の両方で金額が計算されるため、レポート通貨での減価償却金額が表示されるよう、固定資産仕訳帳が更新されました。 減価償却トランザクションについては、トランザクション通貨は常に会計通貨です。 したがって、それらの金額は引き続き **借方** および **貸方** 列に表示されます。 2 つの新しい列、**レポート通貨での借方** および **レポート通貨での貸方** がグリッドに追加されました。

    - 新しいフィールドは、トランザクション タイプが次の 4 つの減価償却タイプのいずれかである場合にのみ使用可能です: **減価償却**、**減価償却調整**、**特別減価償却**、または **特別減価償却費**。
    - 固定資産仕訳帳で減価償却トランザクション タイプを入力すると、レポート通貨金額が新しい列に表示されます。 それらの値は変更可能です。
    - 元帳の会計通貨およびレポート通貨が同じである場合、金額が同期しています。**貸方** 金額を変更すると、**レポート通貨での貸方** 金額がそれに一致するよう自動で変更されます。
    - 固定資産仕訳帳で別のトランザクション タイプを入力すると、転記の前後どちらでも **レポート通貨での借方** および **レポート通貨での貸方** 金額は決して表示されません。 会計通貨およびレポート通貨金額は、総勘定元帳に転記された伝票で引き続き利用できます。
    
### <a name="consolidations"></a>連結
    
Dynamics 365 Finance バージョン 10.0.5 (2019 年 10 月) に導入された機能により、連結および二重通貨に対する柔軟性の向上を促す機能管理を通じて機能が有効になります。 この機能を有効にするには、**機能管理** ワークスペースに移動し、**総勘定元帳の連結で二重通貨機能を有効にする** を選択します。

総勘定元帳の連結では、ソース会社からの会計通貨金額またはレポート通貨金額のいずれかを連結するため新しいオプションが追加されました。 会計通貨またはレポート通貨が、連結会社の会計通貨またはレポート通貨と同じである場合、金額は変換されるのではなく直接コピーされます。

-  連結会社のトランザクション通貨として、ソース会社から会計通貨またはレポート通貨を使用するかどうかを選択できるようになります。

- ソース会社からの会計通貨またはレポート通貨は、双方の通貨が同じである場合は、連結会社の会計通貨金額またはレポート通貨金額に直接コピーされます。 連結会社の会計およびレポートの通貨金額は、いずれの通貨も同じでない場合は、為替レートを使用して計算されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

