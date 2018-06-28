---
title: "セグメント化されたエントリ コントロール移行のガイダンス"
description: "このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。"
author: twheeloc
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25651
ms.assetid: eea675a0-d9d8-453d-9f5a-70c833a7a0d6
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 193117cac28dd66a4ca5d8cf981d99788c2bb410
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="segmented-entry-control-migration-guidance"></a>セグメント化されたエントリ コントロール移行のガイダンス

[!include [banner](../includes/banner.md)]

このトピックでは、セグメント化エントリ コントロールを Microsoft Dynamics AX 2012 のパターンから Microsoft Dynamics AX の新しいパターンに移行するプロセスについて説明します。

新しい設計の目標は、コントロールの実装をカプセル化し、コントロールをサポートするクラスとやり取りするフォームを必要としないことです。 したがって、Microsoft Dynamics AX で、<em>すべてのフォームは、**セグメント化されたエントリ</em>* コントロール インスタンス<em>のアプリケーション プログラミング インターフェイス (API) とのみ対話する必要があります。それらは、コントローラー クラス (**LedgerDimensionAccountController</em>* や <strong>DimensionDynamicAccountController</strong> など) と直接対話してはなりません。 コントローラー上で以前に操作または呼び出された任意のプロパティは、コントロール上で呼び出される必要があります。 <strong>メモ :</strong>

-   一部の API は、コントローラーとコントロールで命名方法が違います。 次のテーブルにこれらの API の一覧を示します。
    **コントローラー メソッド (旧)**
    **コントロール メソッド (新)** parmDate parmControlDate parmFilterLedgerPostingType parmPostingType parmDimensionAccountStorageUsage parmDimensionAccountStorageUsageType
-   **例**
    -   **以前:** controller.parmDate(systemDateGet())
    -   **以後:** LedgerAccount.parmControlDate(systemDateGet());

    この例では、**コントローラー** &gt; **LedgerDimensionAccountController** インスタンスと **LedgerAccount** &gt; 新しい**セグメント化エントリ** コントロールのインスタンス
-   コントロールやデータ フィールドでオーバーライドされたメソッドでは、コード アップグレード ルールが、コントローラーのメソッドの呼び出しを、特定のコントローラーを使用していた各コントロール インスタンスのメソッドの呼び出しに置き換えます。 **例**
    -   **以前:**

            Public void jumpRef()
            {
                ledgerDimensionDefaultAccountcontroller.jumpRef();
            }

    -   **以後:**

            Public void jumpRef()
            {
                segmentedEntryControl1.jumpRef();
                segmentedEntryControl2.jumpRef();
            }

    これらの変更は、他の場所に移動する必要があるコードをコピーして貼り付ける方が簡単になるように行われています (例: **loadSegments()** およびその他の類似メソッドの一部のインスタンス)。 メソッドを削除するかどうか決定するときは、この変更を無視することができます。 決定内容は、メソッドにカスタム ロジックにあるかどうかによって異なります。
-   コードのアップグレード スクリプトは、コントローラーがメソッド内でインスタンス化されるケースを処理しません。 このような場合は、手動で移行する必要があります。
-   Microsoft Dynamics AX 2012 の MRU 機能は、Dynamics AX で削除されました。置き換えの予定はありません。
-   **parmTaxCode** が削除されました。 交換はありません。

## <a name="properties"></a>プロパティ
**セグメント化エントリ**コントロールのカスタム プロパティは、**コントローラー**の下にあります。 次のスクリーン ショットは、例を示します。 [![111](./media/111.png)](./media/111.png) すべてのプロパティがすべての**コント ローラー**クラス タイプに適用されるわけではありません。 選択したコントローラー クラスに適用されないプロパティは無効になります。 次のテーブルは、それぞれのプロパティに関する詳細を示します。

**プロパティ**

**有効な値**

**用途**

勘定タイプ フィールド

データ ソースからのフィールド。

使用されるアカウントの種類を決定します。 通常、複数セグメントの勘定科目から、Cust、Vend、Bank、Project などの他のックアップ テーブルの単一セグメント値への仕訳入力に使用されます。

コントローラー クラス

6 つのコントローラー クラスのうちの 1 つです。 たとえば LedgerDimensionDefaultAccountController。

セグメント化されたエントリ コントロールの動作およびパターンを決定します。 このプロパティの詳細については以下で説明します。

財務勘定を含む

NoYes

財務勘定である主勘定が有効であるかどうかを決定します。

勘定合計を含む

NoYes

タイプが "合計" の主勘定が有効であるかどうかを判断します。

既定の勘定です。

TrueFalse

動的アカウントで、アカウントが既定または完全アカウントであるべきかどうかを決定します。

主勘定セグメントのロック

NoYes

主勘定セグメントがロックされているかどうかをコントロールします。 通常は仕訳帳や構成に基づく配分に使用されます。

転記タイプ

LedgerPostingType 列挙の値。

主勘定が検証され、そのアカウントで使用される転記タイプが許可されているかどうかを確認されます。

手動入力のブロック状態の検証

NoYes

分析コードの「手動入力のブロック」ステータスを優先するかどうかを決定します。

## <a name="controller-class-property"></a>コントローラー クラス プロパティ
次のテーブルは、それぞれのコントローラーに関する詳細を示します。

**コントローラー**

**詳細**

BudgetLedgerDimension

このコントローラーは、セグメント化された入力コントロールのデータ入力の予算に基づくサポートを提供します。 このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。

BudgetPlanningLedgerDimension

このコントローラーは、セグメント化された入力コントロールのデータ入力の予算計画に基づくサポートを提供します。 このコント ローラーを使用するときは、勘定構造をセグメント化エントリ コントロールに提供する必要があります。

DimensionDynamicAccount

このコントローラーは、セグメント化された入力コントロールの複数のアカウント タイプのサポートを提供します。

LedgerDimensionAccountAlias

このコントローラーは、セグメント化された入力コントロールのアカウント エイリアスのサポートを提供します。

LedgerDimensionAccount

このコントローラーは、セグメント化された入力コントロールの複数のセグメントのデータ入力のサポートを提供します。

LedgerDimensionDefaultAccount

このコントローラーは、セグメント化された入力コントロールの既定のアカウントのサポートを提供します。

## <a name="migration-steps"></a>移行ステップ
### <a name="step-1"></a>ステップ１

#### <a name="ax-2012"></a>AX 2012

**SegmentedEntry** は任意のコントロールの横にあるタイプとして表示され、**SegmentedEntryControl** と変更します。 [![SegmentMigrate01](./media/segmentmigrate01.png)](./media/segmentmigrate01.png)

#### <a name="dynamics-ax"></a>Dynamics AX

簡単な方法は古いコントロールの名前に「\_旧」を追加し、新しいコントロール (コントロールの元の名前がある必要があります) を付け加え、すべての設定を移行した後、古いコントロールを削除します。 **注記:** コントロールを参照するテストおよび他のコードが破損しないようにするには、新しいコントロールが古いコントロールと同じ名前であることを確認します。 新しいコントロールを追加するには、**Segmented Entry** コントロールを含む親コントロールを右クリックし、**New** &gt; **SegmentedEntryControl** を選択します。 [![SegmentMigrate02](./media/segmentmigrate02-623x1024.png)](./media/segmentmigrate02.png) 次のスクリーンショットは、新しいコントロールの外観を示しています。 [![SegmentMigrate03](./media/segmentmigrate03.png)](./media/segmentmigrate03.png)

### <a name="step-2"></a>ステップ２

#### <a name="ax-2012"></a>AX 2012

 **jumpRef()** コントロール/メソッドをオーバーライドします。

    public void jumpRef()
    {
        ledgerDimensionDefaultAccountController.jumpRef();
    }

#### <a name="dynamics-ax"></a>Dynamics AX

他の機能が含まれなくなった場合は **jumpRef()** メソッドを完全に削除します。 その他のカスタム **jumpRef** 機能がある場合は、それをそのままにします。 ただし、**jumpRef** がコントロールによって自動的に処理されます。

### <a name="step-3"></a>ステップ 3

#### <a name="ax-2012"></a>AX 2012

**loadAutoCompleteData()** コントロール メソッドをオーバーライドします。

    public void loadAutoCompleteData(LoadAutoCompleteDataEventArgs _e)
    {
        ledgerDimensionDefaultAccountController.loadAutoCompleteData(_e);
        super(_e);
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**loadAutoCompleteData()** メソッドを削除します。

### <a name="step-4"></a>ステップ 4

#### <a name="ax-2012"></a>AX 2012

**loadSegments()** コントロール メソッドをオーバーライドします。

    public void loadSegments()
    {
        super();
        ledgerDimensionDefaultAccountController.loadSegments();
        ledgerDimensionDefaultAccountController.parmControl(this);
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**loadSegments()** メソッドが、コントローラーの **loadSegments()** および **parmControl()** メソッドを呼ぶ以外に何もしない場合は、それを削除します。 ただし、**parmControl()** 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。 呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。

### <a name="step-5"></a>ステップ 5

#### <a name="ax-2012"></a>AX 2012

**loadSegments()** コントロール メソッドをオーバーライドします。

    public void loadSegments()
    {
        super();
        dimAccountController.parmControl(this);
        dimAccountController.parmJournalName(ledgerJournalTable.JournalName);
        dimAccountController.parmCurrency(ledgerJournalTrans.CurrencyCode);
        dimAccountController.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        dimAccountController.parmDate(ledgerJournalTrans.TransDate);
        dimAccountController.parmTaxCode(ledgerJournalTrans.TaxCode);

        dimAccountController.loadSegments();
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**loadSegments()** メソッドがコントローラーでのパラメーターを設定するために使用された場合、**パラメーター** メソッドへの呼び出しは、**パラメーター** メソッドのソースを変更することができるすべての場所に移動する必要があります。 ほとんどの場合、これらの場所は対応するデータ フィールドの **modified()** メソッドおよび/またはデータ ソースの **active()** メソッドです。 たとえば、**loadSegments()** の移行したコードの一部は、左側で上書きをし、次のようになります。

    dimAccountController.parmControl(this) -> No longer needed.

**parmControl()** 呼び出しに渡される SEC コントロール インスタンスをメモしておきます。 コントローラー上で呼び出されていたメソッドは、そのインスタンスで呼び出される必要があります。

    dimAccountController.parmJournalName(ledgerJournalTable.JournalName) ->
    LedgerJournalTable data source,
    JournalName field,
    public void modified()
    {
        .parmJournalName(ledgerJournalTable.JournalName);
    }

**LedgerJournalTable データ ソース**

    public void active()
    {
        .parmJournalName(ledgerJournalTable.JournalName);
    }

**注記:** **loadSegments()** メソッドからすべてのコードを削除したら、そのメソッドを削除できます。

### <a name="step-6"></a>ステップ 6

#### <a name="ax-2012"></a>AX 2012

**loadSegments()** コントロール メソッドをオーバーライドします。 場合によっては、**loadSegments()** メソッドは、テーブル バッファを使用してコントローラーでパラメーターを設定することがありますが、そのテーブル バッファはフォーム上のデータ ソースではありません。 たとえば、**LedgerJournalTransDaily** フォームでは、**loadSegments()** の元の実装は次のようになります。

    public void loadSegments()
    {
        super();

        dimAccountController.parmControl(this);
        dimAccountController.parmJournalName(ledgerJournalTable.JournalName);
        dimAccountController.parmCurrency(ledgerJournalTrans.CurrencyCode);
        dimAccountController.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        dimAccountController.parmDate(ledgerJournalTrans.TransDate);
        dimAccountController.parmTaxCode(ledgerJournalTrans.TaxCode);

        dimAccountController.loadSegments();

        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getMainAccountDimensionAttribute());
    }

**JournalName** プロパティは、ledgerJournalTable バッファから設定されますが、LedgerJournalTable テーブルはフォームのデータ ソースではないことに注意してください。

#### <a name="dynamics-ax"></a>Dynamics AX

このような場合、そのコードをデータ ソースの **active()** メソッド、またはデータ フィールドの **modified()** メソッドに移動できません。 代わりに、テーブル バッファが設定されている場所を特定する必要があります。 たとえば、**LedgerJournalTransDaily** フォームの元の実装では、ledgerJournalTable バッファはフォームの **initLedger()** メソッドで設定されました。 **parmJournalName()** に渡される値は、バッファが **initLedger()** メソッドで再割り当てされる場合のみ変更できることを明らかにする必要があります。 したがって、バッファを割り当てた後、コードを **initLedger()** メソッドに移動する必要があります。 また、一般的なガイドラインに従って、コントロールインスタンスに対して **parmJournalName()** メソッドが呼び出されます。

    void initLedger()
    {
        TransDate   dateFrom   = dateNull();
        TransDate   dateTo     = systemDateGet();

        if (element.args().dataset() == tableNum(LedgerJournalTable))
        {
            ledgerJournalTable = element.args().record();
            LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
            LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
            GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
            LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
            ...
        }
        ...
    }

### <a name="step-7"></a>ステップ 7

#### <a name="ax-2012"></a>AX 2012

**segmentValueChanged()** コントロール メソッドをオーバーライドします。

    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        ledgerDimensionDefaultAccountController.segmentValueChanged(_e);
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**segmentValueChanged()** を実装した場合に、コントローラー上で **super()** と **segmentValueChanged()** メソッドを呼び出す以外何も起こらない場合は、メソッドを削除することができます。

### <a name="step-8"></a>ステップ 8

#### <a name="ax-2012"></a>AX 2012

**segmentValueChanged()** コントロール メソッドをオーバーライドします。

    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**segmentValueChanged()** の実装に追加のロジックがある場合、次に示すように、メソッドを **onSegmentChanged()** メソッドに置き換える必要があります。

    public void onSegmentChanged(DimensionControlSegment _segment)
    {
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(this, currentOffsetMainAccountId, ledgerJournalTrans);
    }

**メモ :**

-   **onSegmentChanged()** メソッドを追加するには、次の手順を実行します。
    1.  メソッドを追加するには、**セグメント化されたエントリ**コントロールを展開します。
    2.  **メソッド** ノードをクリックし、**オーバーライド** &gt; **onSegmentChanged** を選択します。
-   新しいメソッドは、**super()** またはコントロールまたはコントローラーのいずれかの他のメソッドを呼び出す必要はありません。

### <a name="step-9"></a>ステップ 9

#### <a name="ax-2012"></a>AX 2012

**validate()** コントロール メソッドをオーバーライドします。

    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        isValid = ledgerDimensionDefaultAccountController.validate() && isValid;

        return isValid;
    }

#### <a name="dynamics-ax"></a>Dynamics AX

追加の検証がある場合以外は、**validate()** メソッドを削除します。 **super()** 呼び出しは、このコードが行っていたすべてのことを行います。 したがって、保持している新しいコードのみを残しておいてください。

### <a name="step-10"></a>ステップ 10

#### <a name="ax-2012"></a>AX 2012

**lookup()** コントロール メソッドをオーバーライドします。

    public void lookup()
    {
        switch (emplParameters_RU.BankCloseACType)
        {
        case LedgerJournalACType::Bank:
            BankAccountTable::lookupBankAccount(this);
            break;
        case LedgerJournalACType::Cust:
            CustTable::lookupCustomer(this);
            break;
        case LedgerJournalACType::FixedAssets:
            AssetTable::lookupAccountNum(this);
            break;
        case LedgerJournalACType::Ledger:
            super();
            break;
        case LedgerJournalACType::Project:
            ProjTable::lookupProjId(this, emplParameters_RU);
            break;
        case LedgerJournalACType::Vend:
            VendTable::lookupVendor(this);
            break;
        default:
            super();
            break;
        }
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**lookup()** メソッドをそのままにします。

### <a name="step-11"></a>ステップ 11

#### <a name="ax-2012"></a>AX 2012

 **lookupReference()** コントロール メソッドをオーバーライドします。

    public Common lookupReference()
    {
        Common ret;
        ret = super();
        return ret;
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**lookupReference()** メソッドが既定の実装を使用している場合、それを削除することができます。

### <a name="step-12"></a>ステップ 12

#### <a name="ax-2012"></a>AX 2012

**modified()** コントロール メソッドをオーバーライドします。

    public boolean modified()
    {
        boolean ret;

        ret = super();

        if (tmpCurrencyLedgerGainLossAccount.LedgerDimension)
        {
            tmpCurrencyLedgerGainLossAccount.AccountName =
            MainAccount::getLocalizedNameByMainAccountId(
            DimensionStorage::getMainAccountNumFromLedgerDimension(
            tmpCurrencyLedgerGainLossAccount.LedgerDimension), ledger.ChartOfAccounts);
        }
        else
        {
            tmpCurrencyLedgerGainLossAccount.AccountName = '';
        }

        return ret;
    }

#### <a name="dynamics-ax"></a>Dynamics AX

**modified()** メソッドをそのままにします。

### <a name="step-13"></a>ステップ 13

#### <a name="ax-2012"></a>AX 2012

**gotFocus()** コントロール メソッドをオーバーライドします。

    void gotFocus()
    {
        super();
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

#### <a name="dynamics-ax"></a>Dynamics AX

このアプローチは、**loadSegments()** メソッドのアプローチに似ています。 **parm** メソッドのソースが変更できるすべての場所にコードを移動する必要があります。 ほとんどの場合、これらの場所は対応するデータ フィールドの **modified()** メソッドおよび/またはデータ ソースの **active()** メソッドです。 たとえば、上記のコードでは、移行したコードはこのようになります。

    LedgerJournalTable data source,
    FixedOffsetAccount field
    public void modified()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

    LedgerJournalTrans data source,
    OffsetAccountType field
    public void modified()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
            else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

    LedgerJournalTrans data source:
    public void active()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

    LedgerJournalTable data source:
    public void active()
    {
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!ledgerJournalTrans_OffsetAccount.allowEdit())
        {
            ledgerJournalTrans_OffsetAccount.allowEdit(true);
        }
    }

**注記:** **gotFocus()** メソッドからすべてのコードを削除したら、そのメソッドを削除できます。

### <a name="step-14"></a>ステップ 14

#### <a name="ax-2012"></a>AX 2012

フォーム **init()** メソッド:

    ledgerDimensionDefaultAccountController = LedgerDimensionDefaultAccountController::construct(vendParameters_ds, fieldStr(VendParameters, ClearingLedgerDimension));

#### <a name="dynamics-ax"></a>Dynamics AX

コントロールで以下のプロパティを設定します。

-   **データ ソース**
-   **参照フィールド**
-   **コントローラー クラス**

[![SegmentMigrate04](./media/segmentmigrate04.png)](./media/segmentmigrate04.png) [![SegmentMigrate05](./media/segmentmigrate05.png)](./media/segmentmigrate05.png) **注記:** コントロールが動作するためにはコントローラー クラスが必要です。 したがって、**Controller Class** プロパティが設定されていないと、ランタイム エラーがスローされます。

### <a name="step-15"></a>ステップ 15

#### <a name="ax-2012"></a>AX 2012

    ledgerDimensionAccountController.setValues(ledgerJournalTrans.DefaultDimension, false);

#### <a name="dynamics-ax"></a>Dynamics AX

分析コードの指定子のマップを作成してから、**セグメント化されたエントリ**コントロールの **setDimensionSpecifiers** メソッドに送信する必要があります。

    Map defaultDimensionSpecifiers = LedgerDimensionDefaultingEngine::getDefaultDimensionSpecifiers(ledgerJournalTable.DefaultDimension);

    TmpLedgerJournalSplitLines_LedgerAccount.setDimensionSpecifiers(defaultDimensionSpecifiers, false);

**注記:** 分析コードの指定子のマップに何かを追加してからコントロールに送ることができます。 新しいマップをここで作成することもできます。 (同様のロジックに関しては、**LedgerJournalEngine** クラス内の **onSegmentChangedForPrimaryAccount** メソッドを参照してください。)

### <a name="step-16"></a>ステップ 16

#### <a name="ax-2012"></a>AX 2012

**parmControl()** メソッド呼び出し:(これらは通常、フォームの **init()** メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)

    ledgerDimensionDefaultAccountController.parmControl(clearingAccount);

#### <a name="dynamics-ax"></a>Dynamics AX

必要がなくなったため、このコード行を削除します。 ただし、最初にどのコントローラーがどのコントロールで使用されるかを記録します。 たとえば、この場合、ledgerDimensionDefaultAccountController が ClearingAccount SEC で使用されています。 マッピングは、コントロールでコントローラー オブジェクトのメソッド呼び出しを対応するメソッド呼び出しに置き換える場合、およびデザイン時にプロパティを設定する場合に必要です。

### <a name="step-17"></a>ステップ 17

#### <a name="ax-2012"></a>AX 2012

フォーム **init()** メソッド:

    ledgerDimensionDefaultAccountController.parmFilterLedgerPostingType(LedgerPostingType::VendSettlement);

#### <a name="dynamics-ax"></a>Dynamics AX

これは、コントロールの**転記タイプ**プロパティです。 **PostingType** プロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判別できます。 [![SegmentMigrate06](./media/segmentmigrate06.png)](./media/segmentmigrate06.png) これらのプロパティは、コントロール インスタンスで **parm** メソッドを介してコードで設定することもできます。 次に例を示します。

    ClearingAccount.parmPostingType(LedgerPostingType::VendSettlement);

### <a name="step-18"></a>ステップ 18

#### <a name="ax-2012"></a>AX 2012

元帳分析コードのデータ ソース フィールドで **resolveReference()** をオーバーライドします。 [![SegmentMigrate07](./media/segmentmigrate07.png)](./media/segmentmigrate07.png)

#### <a name="dynamics-ax"></a>Dynamics AX

不要になったので、このコードを削除してください。 コントロールこれを自動的に処理します。

### <a name="step-19"></a>ステップ 19

#### <a name="ax-2012"></a>AX 2012

フォームは、**parm** メソッドを通じてコントローラーのプロパティを設定します。

#### <a name="dynamics-ax"></a>Dynamics AX

一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。 このプロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判断できます。 また、**セグメント化エントリ** コントロールの場合、Microsoft Visual Studio の**プロパティ** ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する **parm** メソッドを使用して、コードで設定することもできます。

### <a name="step-20"></a>ステップ 20

#### <a name="ax-2012"></a>AX 2012

フォームは、コントロールの **currentSegmentIndex()** メソッドを使用します。

    dimOffetAssetController. getDimensionAttributeByControlIndex(currentSegmentIndex);

#### <a name="dynamics-ax"></a>Dynamics AX

一般に、コントローラー クラスに以前設定されていたプロパティをコントロールに直接設定する必要があります。 このプロパティを設定する必要があるコントロールは、**parmControl()** 呼び出しを見て派生したマッピングの詳細から判断できます。 また、**セグメント化エントリ** コントロールの場合、Visual Studio の**プロパティ** ダイアログ ボックスで使用できるプロパティは、コントロール インスタンスで対応する **parm** メソッドを使用して、コードで設定することもできます。

### <a name="step-21"></a>ステップ 21

#### <a name="ax-2012"></a>AX 2012

このフォームは、コントローラー オブジェクトのメソッドを呼び出します。 次に例を示します。

    dimOffetAssetController. getDimensionAttributeByControlIndex(currentSegmentIndex);

#### <a name="dynamics-ax"></a>Dynamics AX

コントローラー上のすべてのメソッド呼び出しはコントロール上のメソッド呼び出しに置き換える必要があります。 この例では、代わりにコントロールで **getDimensionAttributeByControlIndex()** メソッドを使用します。

    segmentedEntryControl. getDimensionAttributeByControlIndex();

### <a name="step-22"></a>ステップ 22

#### <a name="ax-2012"></a>AX 2012

**DimensionDynamicAccountController** で、勘定タイプはコンストラクターを通して指定されます。

    DimensionDynamicAccountController::construct(ledgerJournalTrans_ds, fieldStr(LedgerJournalTrans, LedgerDimension), fieldStr(LedgerJournalTrans, AccountType));

#### <a name="dynamics-ax"></a>Dynamics AX

この機能を実装するには、2 つのメソッドがあります。 これらのメソッドは相互に排他的なため、状況に応じてそれらのメソッドのうち 1 つのみを使用してください。

-   **セグメント化されたエントリー**コントロールについては、**プロパティ**ダイアログ ボックスで、**勘定タイプ フィールド**プロパティを勘定タイプを提供するデータ ソース フィールドに設定します。 これが推奨されるメソッドです。 **注記:** **super()** 呼び出しが、**勘定タイプ フィールド** プロパティにバインドされているフィールドの **modified()** メソッドから削除されている場合、このメソッドは機能しません。 **LedgerJournalTransDaily** などのいくつかの仕訳帳フォームで、この問題が確認されました。 このような場合、**super()** コールバックを **modified()** メソッドに追加するか、2 つ目のメソッドを使用します。
-   コントロールで **parmAccountTypeEnumValue()** メソッドを呼び出すことにより、勘定タイプを手動で設定します。 次に例を示します。

        LedgerJournalTrans_AccountNum.parmAccountTypeEnumValue(enum2int(ledgerJournalTrans.AccountType));

    **注記:** **parmAccountTypeEnumValue()** への呼び出しは、勘定タイプを提供するフィールドの、データソースの **active()** メソッド、および **modified()** メソッドの両方に入力する必要があります。

### <a name="step-23"></a>ステップ 23

#### <a name="ax-2012"></a>AX 2012

フォームには定義されている変数があります。

    LedgerDimensionDefaultAccountController ledgerDimensionDefaultAccountController;

#### <a name="dynamics-ax"></a>Dynamics AX

コントローラーが必要なくなったため、これを削除します。

### <a name="step-24"></a>ステップ 24

#### <a name="ax-2012"></a>AX 2012

**parmCurrentLedgerCOA()** メソッド呼び出し:(これらは通常、フォームの **init()** メソッドまたはコントロールで上書きされたメソッドのうちの 1 つに存在します。)

    ledgerDimensionDefaultAccountController.parmCurrentLedgerCOA(LedgerCOA::current());

#### <a name="dynamics-ax"></a>Dynamics AX

ほとんどの場合に必要がなくなったため、このコード行を削除します。 この線を削除する前に、**LedgerCOA** 値がその情報から派生するため、データ領域 ID がパラメーターとしてコントローラーに正しく渡されていることを確認してください。 データ領域 ID が渡されない場合は、**parmCurrentLedgerCOA(â€¦)** を **parmDataAreaId(â€¦)** で交換し、通常は **curext()** または会社のアカウント管理のために範囲を制御する別のテーブル フィールドである適切な **SelectableDataArea** 値を渡します。 フォームにデータ領域のコンテキストはありませんが、現在の **LedgerCOA** 値のみがある場合、既定のアカウント コント ローラーだけで動作する必要があります。 企業には無関係ですが、特定の勘定科目表 (COA) (**MainAccount** および **Allocations** など) にスコープされているフォームがいくつかあります。 そのような場合、**parmCurrentLedgerCOA** が、既定のアカウント コントローラー タイプ セットを持つ**セグメント化エントリ** コントロール インスタンスで呼び出される必要があります。

### <a name="step-25"></a>ステップ 25

#### <a name="ax-2012"></a>AX 2012

**parmIncludeFinancialAccounts(NoYes)** メソッド呼び出し:

    LedgerDimensionDefaultAccountController.parmIncludeFinancialAccounts(NoYes::Yes);

#### <a name="dynamics-ax"></a>Dynamics AX

このコード行は不要になり、**セグメント化されたエントリ**コントロールのプロパティを使用して直接設定する必要があります。 **注記:** フレームワークのバグのため、これを明示的に設定しないと、以前の動作では、構築中に暗黙的に**はい**が割り当てられていましたが、勘定分析コードの既定のアカウント コントローラーに**いいえ**が割り当てられます。 この操作は、プロパティとして手動で設定する必要があります。 または、**ダイアログ**クラスへの、**parm** メソッドがまだ明示的に呼び出されるはずです。

### <a name="step-26"></a>ステップ 26

#### <a name="ax-2012"></a>AX 2012

**セグメント化エントリ** コントロールのアカウントタイプを提供するデータフィールドの **変更済み** メソッドのコードは、コントロールが動的アカウントコントロールとして使用されている場合、このようになります。

    public void modified()
    {
        super();

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTable.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            controller.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

#### <a name="dynamics-ax"></a>Dynamics AX

このデータ フィールドの **modified** メソッドは、**参照** フィールドとして **セグメント化されたエントリ** コントロールにバインドされた勘定分析コード フィールドをクリアしなければならなくなりました。 たとえば、**セグメント化されたエントリ**コントロールの名前が **OffsetAccount** である場合、このコントロールの**参照**フィールド プロパティが **LedgerDimension** に設定され、上記のコード内の**変更**メソッドが次のように変更される必要があります。

    public void modified()
    {
        super();

        OffsetAccount.LedgerDimension = 0;

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTable.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

追加の明細行は、勘定タイプが変更されたときにコントロールをクリアするために必要です。

### <a name="step-27"></a>ステップ 27

#### <a name="ax-2012"></a>AX 2012

コントローラーで **parmAccountStructure()** メソッドを呼び出すことができます。

    fromBudgetPlanningLedgerDimensionController.parmAccountStructureId(accountStructureIdLocal);

#### <a name="dynamics-ax"></a>Dynamics AX

このメソッドは 2 つの異なるメソッドで置き換えられます。 また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。 したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。 たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。

    ToBudgetTransactionLine_LedgerDimension.parmDoValueActiveDatesValidation(false);

    ToBudgetTransactionLine_LedgerDimension.parmDoValueSuspendedValidation(false);

### <a name="step-28"></a>ステップ 28

#### <a name="ax-2012"></a>AX 2012

以下のコントローラーで **parmAccountStructure()** メソッドを呼び出すことができます。

    fromBudgetPlanningLedgerDimensionController.parmAccountStructureId(accountStructureIdLocal);

#### <a name="dynamics-ax"></a>Dynamics AX

**parmAccountStructureId()** メソッドは、コントロール上に存在しません。 代わりに、個別の **getAccountStructure()** および **setAccountStructure()** メソッドがあります。 したがって、**parmAccountStructureId()** 呼び出しは、**parm** メソッドがどのように使用されていたかに応じて、**get** メソッドまたは **set** メソッドで置き換えられる必要があります。 たとえば、上記のコードで **parm** メソッドはセッターとして呼び出されたので、呼び出しは**設定**メソッドへの呼び出しによって置換される必要があります。

    ToBudgetPlanningTransactionLine_LedgerDimension.setAccountStructureId(accountStructureIdLocal);

### <a name="step-29"></a>ステップ 29

#### <a name="ax-2012"></a>AX 2012

    parmSkipSuspendedAndActiveDateValidation:

#### <a name="dynamics-ax"></a>Dynamics AX

このメソッドは 2 つの異なるメソッドで置き換えられます。 また、新しいメソッドの目的は、古いメソッドの逆です: 古いメソッドは検証を無効にしましたが、新しいメソッドはそれを有効にします。 したがって、コードを移行するときは、新しいメソッドの Boolean パラメーターを逆にする必要があります。 たとえば、上記のコードでメソッドの呼び出しについては、新しいメソッドはこのようになります。

    ToBudgetTransactionLine_LedgerDimension.parmDoValueActiveDatesValidation(false);

    ToBudgetTransactionLine_LedgerDimension.parmDoValueSuspendedValidation(false);

### <a name="step-30"></a>ステップ 30

#### <a name="ax-2012"></a>AX 2012

通常は **loadSegments()** メソッド内でコントローラーの **loadFromId** メソッドを呼び出します。

    ledgerDimensionDefaultAccountControllerResourceIssueOffset.loadFromId(wrkCtrTable.ResourceIssueOffsetLedgerDimension);

#### <a name="dynamics-ax"></a>Dynamics AX

このメソッドは推奨されておらず、使用しないでください。 このメソッドに対するすべての呼び出しを削除する必要があります。

### <a name="migrating-a-segmented-entry-control-on-a-dialog"></a>ダイアログ上のセグメント化エントリ コントロールの移行

ダイアログ上の新しい**セグメント化されたエントリ** コントロールの取得パターンは Dynamics AX で変更されています。 コントローラー クラス API とのやり取りではなく、**SegmentedEntryControlBuild** クラスとやり取りしてダイアログと SEC をリンクする必要があります。 このセクションでは、異なるコントローラー タイプのダイアログで SEC を使用するためのコード パターンを示します。 **注記:** Dynamics AX ではヘルプ テキストが不要になるため、ダイアログ フィールドにヘルプ テキストを設定する必要はありません。

-   **動的アカウント:**
    -   **以前:**

            // Creating the dialog field for the SEC
            dialogDynamicAccountType = _dialog.addFieldValue(enumStr(LedgerJournalACTypeForPaymProposal), defaultOffsetAccountType, "@SYS115164", "@SYS115165");
            dialogDynamicAccount = _dialog.addFieldValue(extendedTypeStr(LedgerDimensionBase), defaultOffsetLedgerDimension, "@SYS115166", "@SYS115167");
            dimensionDynamicAccountController = DimensionDynamicAccountController::constructForDialog(dialogDynamicAccount, dialogDynamicAccountType, enumStr(LedgerJournalACTypeForPaymProposal));
                       dimensionDynamicAccountController.parmIsDefaultAccount(true);

            public void dialogPostRun(DialogRunBase _dialog)
            {
            …

            dialogDynamicAccountType.registerOverrideMethod('modified', 'accountType_Modified', this);

            ...
            }

            private boolean accountType_Modified(FormComboBoxControl _formComboBoxControl)
            {
             boolean valueWasModified;

             valueWasModified = _formComboBoxControl.modified();
             if (valueWasModified)
             {
             dialogDynamicAccount.value(0);
                        }

             return valueWasModified;
            }

    -   **以後:**

            // Creating the dialog field for the SEC
            protected Object dialog()
            {
            ...        

            // Create the account type dialog field
            dialogDynamicAccountType = _dialog.addFieldValue(enumStr(LedgerJournalACTypeForPaymProposal), defaultOffsetAccountType, "@SYS115164", "@SYS115165");
            // Create the SEC dialog field
            dialogDynamicAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(DimensionDynamicAccountControl), extendedTypeStr(LedgerDimensionBase), "@SYS115166", defaultOffsetLedgerDimension);

            // Provide account type information for the SEC field
            SegmentedEntryControlBuild::initDialogFieldAccountType(dialogDynamicAccount, enumStr(LedgerJournalACTypeForPaymProposal) , defaultOffsetAccountType);
            // Set additional parameters on the SEC dialog field
            SegmentedEntryControlBuild segmentedEntryControlBuild = dialogDynamicAccount.control(); 
            segmentedEntryControlBuild.parmIsDefaultAccount(true);

            …
            }

            // Override for modified method of the Account type checkbox to update the SEC when account type is changed
            public int accountType_selectionChange(FormComboBoxControl _formComboBoxControl)
            {
            SegmentedEntryControl secDDAC = dialogDynamicAccount.control();
            accountType = _formComboBoxControl.selection();

            // This is the backing variable used to pack the account specified via the SEC
            ledgerDimensionDynamicAccount = 0; 
            // Clear the SEC value
            secDDAC.clearReference();                     

            // Specify the new account type to the SEC; this is an additional step needed for the AX SEC
            secDDAC.parmAccountTypeEnumValue(enum2int(accountType));

            return true;
            }

            // Set default account type based on value read from SysLastValue
            public void dialogPostRun(DialogRunBase _dialog)
            {
            …
            // Default any previously saved account type info
            secDDAC = dialogDynamicAccount.control();
            secDDAC.parmAccountTypeEnumValue(enum2int(accountType));
            ….
            }

-   **勘定科目:**
    -   **以前:**

            dialogFeeLedgerDimension = dialog.addFieldValue(extendedtypestr(LedgerDimensionAccount),feeLedgerDimension,"@SYS119703", "@SYS85534");
            ledgerDimensionAccountController = LedgerDimensionAccountController::constructForDialog(dialogFeeLedgerDimension);

    -   **以後:**

            DialogField dialogLedgerAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionAccountControl), extendedTypeStr(LedgerDimensionAccount), "@SYS119703", feeLedgerDimension);

-   **既定の勘定:**
    -   **以前:**

            dialogInterCompanyLedgerDimension = dialog.addFieldValue(extendedTypeStr(LedgerDimensionDefaultAccount),interCompanyLedgerDimension, "@SYS21687", "@SYS85534");
            ledgerDimensionDefaultAccountController = LedgerDimensionDefaultAccountController::constructForDialog(dialogInterCompanyLedgerDimension);

    -   **以後:**

            DialogField dialogDefaultAccount = SegmentedEntryControlBuild::addToDialog(dialog, classstr(LedgerDimensionDefaultAccountControl), extendedTypeStr(LedgerDimensionDefaultAccount), "@SYS21687", interCompanyLedgerDimension);

-   **予算:**
    -   **以前:** 既存のプログラム ソース コード内でダイアログ シナリオの**予算計画**コントローラー (**BudgetLedgerDimensionController**) の取り込みは見つかりませんでした。
    -   **以後:**

            DialogField dialogBudget = SegmentedEntryControlBuild::addToDialog(dialog, classstr(BudgetLedgerDimensionControl), extendedTypeStr(LedgerDimensionBudget), 'Budget', ledgerDimensionBudget);

    **メモ :**
    -   新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では **予算**) を指定できます。
    -   コントロールのデフォルト値は、**ledgerDimensionBudget** 変数で指定します。
    -   **予算** コントローラーを用いて、使用する勘定構造を指定する必要があります。 **Dialog** クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。
-   **予算計画:**
    -   **以前:** 既存のプログラム ソース コード内でダイアログ シナリオの**予算計画**コントローラー (**BudgetPlanningLedgerDimensionController**) の取り込みは見つかりませんでした。
    -   **以後:**

            DialogField dialogBudgetPlanning = SegmentedEntryControlBuild::addToDialog(dialog, classstr(BudgetPlanningLedgerDimensionControl), extendedTypeStr(LedgerDimensionBudgetPlanning), 'Budget planning', ledgerDimensionBudgetPlanning);

    **メモ :**
    -   新しい API を使用すると、ダイアログ フィールドを設定しているときに、ラベル (前述の例では **予算計画**) を指定できます。
    -   コントロールのデフォルト値は、**ledgerDimensionBudgetPlanning** 変数で指定します。
    -   **予算計画** コントローラーを用いて、使用する勘定構造を指定する必要があります。 **Dialog** クラスは、ユーザーが勘定構造を選択し (SEC の外部で)、選択した勘定構造を SEC で設定する方法を実装する必要があります。


<a name="additional-resources"></a>その他のリソース
--------

[セグメント化されたエントリ コントロールのダイアログのサポート](segmented-entry-control-dialog-support.md)

[セグメント化されたエントリ コントロールのメタデータ詳細](segmented-entry-control-metadata-specification.md)

[セグメント化されたエントリ コントロールの Parm メソッド詳細](segmented-entry-control-parm-method-specification.md)

[セグメント化されたエントリ コントロールの移行](segmented-entry-control-conversion.md)





