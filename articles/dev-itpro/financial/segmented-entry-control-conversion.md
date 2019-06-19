---
title: セグメント化されたエントリ コントロールの移行
description: このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25611
ms.assetid: 82e953d0-878e-4a3f-a91b-7375017a2810
ms.search.region: Global
ms.author: ghenriks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f17adf415ec407d6058e0bf16d204114540cdb6a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555582"
---
# <a name="migrate-segmented-entry-controls"></a>セグメント化されたエントリ コントロールの移行

[!include [banner](../includes/banner.md)]

このチュートリアルでは、簡単なシナリオ (SMAServiceOrderTable フォームの場合) と複雑なシナリオ (LedgerJournalTransDaily フォームの場合) の 2 つのセグメント化エントリ管理の移行シナリオについて説明します。

<a name="simple-migration-scenario--smaserviceordertable-form"></a>簡易移行シナリオ - SMAServiceOrderTable フォーム
-----------------------------------------------------

1.  アプリケーション エクスプローラーで **SMAServiceOrderTable** フォームを検索します。
2.  現在のプロジェクトにフォームを追加します。
3.  フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。
4.  フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、**ファイル** タブの下にある検索バーで「SegmentedEntry」を検索して、セグメント化されたエントリ コントロール (SEC) を見つけます。
5.  SEC を選択し、次の情報を確認します。
    -   コントロールの横にある括弧で指定されたコントロールのタイプは、**SegmentedEntryControl** です。
    -   **コントローラー クラス** プロパティは **DimensionDynamicAccountController** に設定されます。 このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。 コントローラーのタイプによって、コントロールのビヘイビアーが決まります。

6.  コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) \[セグメント化されたエントリ コントロール\]" のすべての事例を検索します。
7.  検索結果で最初の結果を無視すると、コントローラー変数申告を示します。 制御変数への参照をすべて削除したら、最後に、この作業項目を修正する必要があります。
8.  次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。

### <a name="ledgerdimension-data-field"></a>LedgerDimension データ フィールド

(**フォーム**&gt;**データ ソース** &gt;**SMAServiceOrderLine**&gt; **フィールド** &gt;**LedgerDimension**&gt; **方法**)

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        ExpenseCost_LedgerDimension.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="expensecostledgerdimension-control"></a>ExpenseCost\_LedgerDimension コントロール

(**フォーム**タブの下にある検索バーで「ExpenseCost\_LedgerDimension」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        ExpenseCost_LedgerDimension.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は行わないため、削除できます。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimDynamicAccountController.loadSegments();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **loadSegments()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        switch (smaServiceOrderLine.OffsetAccountTypeExpense)
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
            case LedgerJournalACType::Project:
                ProjTable::lookupProjId(this, smaServiceOrderLine);
                break;
            case LedgerJournalACType::Vend:
                VendTable::lookupVendor(this);
                break;
            default:
                super();
                break;
            }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドをそのままにします。 "仕事" を削除します。 カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 次に例を示します。

    public boolean checkUseCustomLookup(int _accountTypeEnumValue, int _secondaryAccountTypeEnumValue)
    {
        boolean ret;
        switch(_accountTypeEnumValue)
        {
            case LedgerJournalACType::Bank:
            case LedgerJournalACType::Cust:
            case LedgerJournalACType::FixedAssets:
            case LedgerJournalACType::Project:
            case LedgerJournalACType::Vend:
                ret = true;
                break;
            default:
                ret = false;
        }
        return ret;
     }

また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimDynamicAccountController.segmentValueChanged(_e);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **segmentValueChanged()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimDynamicAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="controller-variable-declarations"></a>コントローラー変数申告

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

最後に、コントローラー変数申告のため、最初の TODO に戻ります。

    /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
    /* 'dimDynamicAccountController' controller object is used with 'ExpenseCost_LedgerDimension' segmented entry controls.*/
    DimensionDynamicAccountController dimDynamicAccountController;

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

**dimDynamicAccountController** 変数は、フォームで使用されなくなりました。 したがって、削除できるようになりました。

## <a name="complex-migration-scenario--ledgerjournaltransdaily-form"></a>複雑な移行シナリオ – LedgerJournalTransDaily フォーム
1.  アプリケーション エクスプローラーで **LedgerJournalTransDaily** フォームを検索します。
2.  現在のプロジェクトにフォームを追加します。
3.  フォーム デザイン ビューとコード エディタ ビューで、フォームを開きます。
4.  フォーム デザイン ビューで、手動でコントロール ツリーを移動するか、**ファイル** タブの下にある検索バーで「SegmentedEntry」を検索して、SEC を見つけます。
5.  SEC を選択し、次の情報を確認します。
    -   コントロールの横にある括弧で指定されたコントロールのタイプは、**SegmentedEntryControl** です。
    -   **コントローラー クラス** プロパティは **DimensionDynamicAccountController** に設定されます。 このプロパティは、SEC のこのインスタンスが使用するコントローラーのタイプを示します。 コントローラーのタイプによって、コントロールのビヘイビアーが決まります。

6.  コード エディタ ビューに切り替え、フォーム ソース コードで "TODO: (コード アップグレード) \[セグメント化されたエントリ コントロール\]" のすべての事例を検索します。
7.  検索結果で、最初の 3 件の結果はコントローラー変数申告用です。 "仕事" を添付しているコメントを参照して、どの SEC インスタンスがどのコントローラー インスタンスを使用しているか示すマッピングを記録します。 このマッピングは、コントローラーでのメソッド呼び出しをコントロールでのメソッド呼び出しに置き換えるときに必要です。 コントローラーからコントロールへのマッピングがどのようなものかを次に示します。
    1.  dimAccountController
        1.  LedgerJournalTrans\_AccountNum
        2.  LedgerJournalTrans\_AccountNum1
        3.  Group4\_AccountNum

    2.  dimOffsetAccountController
        1.  GridOffsetAccount
        2.  LedgerJournalTrans\_OffsetAccount1
        3.  Group4\_OffsetAccount

    3.  dimPaymentFeeAccountController
        1.  CustPaymJournalFee\_CustAccount

    コントローラー変数へのすべての参照を削除した後、最後に、これらの 3 つの TODO コメントを修正します。
8.  次のサブセクションでの説明にあるように、残りの各 TODO コメントが実行されます。

### <a name="ledgerdimension-data-field"></a>LedgerDimension データ フィールド

(**フォーム**&gt;**データ ソース** &gt;**LedgerJournalTrans**&gt; **フィールド** &gt;**LedgerDimension**&gt;  **方法**)

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    // </GEEPL>
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="offsetledgerdimension-data-field"></a>OffsetLedgerDimension データ フィールド

(**フォーム**&gt;**データ ソース** &gt;**LedgerJournalTrans**&gt; **フィールド** &gt;**OffsetLedgerDimension**&gt; **方法**)

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

**OffsetLedgerDimension** フィールドの **jumpRef()** メソッド。

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="ledgerjournaltransaccountnum-control"></a>LedgerJournalTrans\_AccountNum コントロール

(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_AccountNum」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.loadSegments();
        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  **initLedger()** メソッドを更新します。

        void initLedger()
        {
            TransDate   dateFrom   = dateNull();
            TransDate   dateTo     = systemDateGet();
            if (element.args().dataset() == tableNum(LedgerJournalTable))
            {
                ledgerJournalTable = element.args().record();
                journalNum         = ledgerJournalTable.JournalNum;
                LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
                LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
                Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        . . .

2.  **LedgerJournalTrans** データ ソースの **active()** メソッドでコードを更新します。 **注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。 それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。

        . . .
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        if (ledgerJournalTrans.AccountType == LedgerJournalACType::Ledger)
        {
            currentMainAccountId = LedgerJournalTrans_AccountNum.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentMainAccountId = 0;
        }
        return ret;

3.  **LedgerJournalTrans** データ ソースの **CurrencyCode** フィールドの **modified()** メソッドに、次のコードを追加します。

        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);

4.  **LedgerJournalTrans** データ ソースの **Company** フィールドの **modified()** メソッドに、次のコードを追加します。

        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());

5.  **LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。

        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

6.  **loadSegments()** メソッドを削除します。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        // Polish sale disposal may require to filter asset that are not
        // marked for sale. lookupAccountNum method needs the ledgerJournalTrans_Asset.TransType
        // value to filter appropriately the assets. Thus, ledgerJournalTrans_Asset is
        // passed to accountNumLookup metho jumpRef d.
        // <GEEPL>
        if (!ledgerJournalEngine.accountNumLookup(ledgerJournalTrans_AccountNum,
            ledgerJournalTrans,
            ledgerJournalTrans.OffsetAccountType,
            ledgerJournalTrans.parmOffsetAccount(),
            ledgerJournalTrans_Asset))
        {
            super();
        }
        // </GEEPL>
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドをそのままにします。 "仕事" を削除します。 カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        // <GIN>
        if (TaxWithholdParameters_IN::checkTaxParameters()
            && ledgerJournalTrans.TaxWithholdCode_IN != '')
        {
            if (Box::okCancel("@GLS222698",
                DialogButton::Cancel) == DialogButton::Cancel)
            {
                return;
            }
        }
        // </GIN>
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// Event handler for the segment changed event.
        /// </summary>
        /// <param name = "_segment">The segment that has been changed.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);

            // <GIN>
            if (TaxWithholdParameters_IN::checkTaxParameters()
                && ledgerJournalTrans.TaxWithholdCode_IN != '')
            {
                if (Box::okCancel("@GLS222698",
                    DialogButton::Cancel) == DialogButton::Cancel)
                {
                    return;
                }
            }

            // </GIN>
            if (_segment.parmName() == mainAccountDimAttrName)
            {
                previousMainAccountId = currentMainAccountId;
            }
            currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(LedgerJournalTrans_AccountNum, currentMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスに従うことによって新しいメソッドを追加できます。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="gridoffsetaccount-control"></a>GridOffsetAccount コントロール

(**フォーム**タブの下にある「GridOffsetAccount」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    void gotFocus()
    {
        super();
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            gridOffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!gridOffsetAccount.allowEdit())
        {
            gridOffsetAccount.allowEdit(true);
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  ledgerJournalTable バッファを更新するコードの後に、**initLedger()** メソッドへ次のコードを追加します。

        . . .
        if (element.args().dataset() == tableNum(LedgerJournalTable))
        {
            ledgerJournalTable = element.args().record();
            journalNum         = ledgerJournalTable.JournalNum;
            LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
            LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
            Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
            if (ledgerJournalTable.FixedOffsetAccount)
            {               
                gridOffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
            }
            else if (!gridOffsetAccount.allowEdit())
            {
                gridOffsetAccount.allowEdit(true);
            }
        . . .

2.  **gotFocus()** メソッドを削除します。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.loadSegments();
        currentOffsetMainAccountId = dimOffsetAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  **initLedger()** メソッドを更新します。 **注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。 それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。

        void initLedger()
        {
            TransDate   dateFrom   = dateNull();
            TransDate   dateTo     = systemDateGet();
            if (element.args().dataset() == tableNum(LedgerJournalTable))
            {
                ledgerJournalTable = element.args().record();
                journalNum         = ledgerJournalTable.JournalNum;
                GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
                LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
                Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
                if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
                {
                    currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
                }
                else
                {
                    currentOffsetMainAccountId = 0;
                }

                // Lock the main account segment if "Fixed offset account" is selected in Journal Names
                if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
                {
                    GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
                }
        . . .

2.  **LedgerJournalTrans** データ ソースの **active()** メソッドでコードを更新します。 **注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。 それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。

        . . .
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue( DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        { 
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
        return ret;

3.  **LedgerJournalTrans** データ ソースの **CurrencyCode** フィールドの **modified()** メソッドに、次のコードを追加します。

        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);

4.  **LedgerJournalTrans** データ ソースの **OffsetCompany** フィールドの **modified()** メソッドに、次のコードを追加します。

        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());

5.  **LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。

        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

6.  **LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドに、次のコードを追加します。 **注記:** **getValue()** メソッドは、勘定タイプが**元帳**に設定されている場合にのみ呼び出す必要があります。 それ以外の場合、このメソッドを呼び出すと、無効な関数呼び出しが発生します。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue( DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

7.  **loadSegments()** メソッドを削除します。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = dimOffsetAccountController.parmControl().currentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger &&
            dimOffsetAccountController.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) ||
            !ledgerJournalEngine.offsetAccountNumLookUp(gridOffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。 この場合、メソッドは **GridOffsetAccount** コントロールでオーバーライドされるため、**dimOffsetAccountController** が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。 したがって、コードは次のようになります。

    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = GridOffsetAccount.getCurrentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger && GridOffsetAccount.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) || !ledgerJournalEngine.offsetAccountNumLookUp(gridOffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// Event handler for the segment changed event.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(
            GridOffsetAccount, currentOffsetMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスに従うことによって新しいメソッドを追加できます。

#### <a name="step-6"></a>ステップ 6

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="ledgerjournaltransaccountnum1"></a>LedgerJournalTrans\_AccountNum1

(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_AccountNum1」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.loadSegments();
        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドを移行する手順は、**LedgerJournalTrans\_AccountNum.loadSegments()** メソッドを移行する手順と同じです。 したがって、追加の手順は必要はありません。 このメソッドを削除します。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.accountNumLookup(ledgerJournalTrans_AccountNum1, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドをそのままにします。 "仕事" を削除します。 カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 また、カスタム ルックアップで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);
        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// The event handler when a segment is modified.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(
            LedgerJournalTrans_AccountNum1, currentMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスに従うことによって新しいメソッドを追加できます。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();
        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="ledgerjournaltransoffsetaccount1"></a>LedgerJournalTrans\_OffsetAccount1

(**フォーム**タブの下にある検索バーで、「LedgerJournalTrans\_OffsetAccount1」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.loadSegments();
        currentOffsetMainAccountId = dimOffsetAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

**GridOffsetAccount.loadSegments()** メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。 ただし、次の変更を加える必要があります。

1.  **LedgerJournalTrans** データ ソースの**有効な**メソッドにコード行を追加します。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(
            DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

2.  **LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドで同じ変更を行います。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

3.  **initLedger()** メソッドで同じ変更を行います。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue( DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

4.  **loadSegments()** メソッドを削除します。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = dimOffsetAccountController.parmControl().currentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger &&
            dimOffsetAccountController.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) ||
            !ledgerJournalEngine.offsetAccountNumLookUp(ledgerJournalTrans_OffsetAccount1, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドを保持しますが、コントローラーをコントロール インスタンスに置き換えます。 この場合、メソッドは **LedgerJournalTrans\_OffsetAccount1** コントロールでオーバーライドされるため、**dimOffsetAccountController** が (コントローラー変数宣言の "仕事" に示されたマッピングに基づいて) 3 つの異なる SEC インスタンスに使用される場合でも、コントローラーをたった 1 つの SEC インスタンスに置き換える必要があります。 したがって、コードは次のようになります。

    public void lookup()
    {
        // Find the current segment index value
        int currentSegmentIndex = LedgerJournalTrans_OffsetAccount1.getCurrentSegmentIndex();
        if ((ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger && LedgerJournalTrans_OffsetAccount1.getDimensionAttributeByControlIndex(currentSegmentIndex) != DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount)) || !ledgerJournalEngine.offsetAccountNumLookUp(ledgerJournalTrans_OffsetAccount1, ledgerJournalTrans))
        {
            super();
        }
    }

カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// The event handler when a segment is modified.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(
            LedgerJournalTrans_OffsetAccount1, currentOffsetMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスに従うことによって新しいメソッドを追加できます。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="custpaymjournalfeecustaccount"></a>CustPaymJournalFee\_CustAccount

(**フォーム**タブの下にある検索バーで、「CustPaymJournalFee\_CustAccount」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        CustPaymJournalFee_CustAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        CustPaymJournalFee_CustAccount.parmJournalName(ledgerJournalTable.JournalName);
        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);
        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimPaymentFeeAccountController.loadSegments();
        currentPaymentFeeMainAccountId = dimPaymentFeeAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  **initLedger()** メソッドを更新します。

        ledgerJournalTable = element.args().record();
        journalNum = ledgerJournalTable.JournalNum;
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName); Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName); CustPaymJournalFee_CustAccount.parmJournalName(ledgerJournalTable.JournalName);
        . . .

2.  **CustVendPaymJournalFee** データ ソースの **active()** メソッドに、次のコードを追加します。 **注記:** このメソッドは存在しないため、上書きする必要があります。

        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);

3.  **CustVendPaymJournalFee** データ ソースの **FeeCurrency** フィールドの **modified()** メソッドに、次のコードを追加します。 **注記:** このメソッドは存在しないため、上書きする必要があります。

        CustPaymJournalFee_CustAccount.parmCurrency(custVendPaymJournalFee.FeeCurrency);

4.  **LedgerJournalTrans** データ ソースの **active()** メソッドに、次のコードを追加します。

        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

5.  **LedgerJournalTrans** データ ソースの **TransDate** フィールドの **modified()** メソッドに、次のコードを追加します。

        CustPaymJournalFee_CustAccount.parmControlDate(ledgerJournalTrans.TransDate);

6.  **loadSegments()** メソッドを削除します。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (custVendPaymJournalFee.Module == ModuleCustVend::Cust)
        {
            if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Cust)
            {
                CustTable::lookupCustomer(this, ledgerJournalTrans.Company);
            }
            else if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Ledger)
            {
                super();
            }
        }
        else if (custVendPaymJournalFee.Module == ModuleCustVend::Vend)
        {
            if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Vend)
            {
                VendTable::lookupVendor(this, ledgerJournalTrans.Company);
            }
            else if (custVendPaymJournalFee.LedgerJournalACType == LedgerJournalACType::Ledger)
            {
                super();
            }
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドをそのままにします。 "仕事" を削除します。 カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 次に例を示します。

    public boolean checkUseCustomLookup(int _accountTypeEnumValue, int _secondaryAccountTypeEnumValue)
    {
        boolean ret;
        switch(_accountTypeEnumValue)
        {
            case LedgerJournalACType::Bank:
            case LedgerJournalACType::Cust:
            case LedgerJournalACType::FixedAssets:
            case LedgerJournalACType::Project:
            case LedgerJournalACType::Vend:
                ret = true;
                break;
            default:
                ret = false;
        }
        return ret;
    }

また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimPaymentFeeAccountController.segmentValueChanged(_e);
        currentPaymentFeeMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimPaymentFeeAccountController, currentPaymentFeeMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// The event handler when a segment is modified.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentPaymentFeeMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(
            CustPaymJournalFee_CustAccount, currentPaymentFeeMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスの指示に従うことによって新しいメソッドを追加することができます。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimPaymentFeeAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="group4accountnum"></a>Group4\_AccountNum

(**フォーム**タブの下にある検索バーで「Group4\_AccountNum」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        LedgerJournalTrans_AccountNum.jumpRef();
        LedgerJournalTrans_AccountNum1.jumpRef();
        Group4_AccountNum.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        LedgerJournalTrans_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_AccountNum.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_AccountNum.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum1.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        Group4_AccountNum.parmDataAreaId(ledgerJournalTrans.Company ? ledgerJournalTrans.Company : curext());
        LedgerJournalTrans_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_AccountNum1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_AccountNum.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.loadSegments();
        currentMainAccountId = dimAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドを移行する手順は、**LedgerJournalTrans\_AccountNum.loadSegments()** メソッドを移行する手順と同じです。 したがって、追加の手順は必要はありません。 このメソッドを削除します。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.accountNumLookup(group4_AccountNum, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドをそのままにします。 "仕事" を削除します。 カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimAccountController.segmentValueChanged(_e);
        currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(dimAccountController, currentMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// The event handler for the segment change event.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            if (_segment.parmName() == mainAccountDimAttrName)
            {
                previousMainAccountId = currentMainAccountId;
            }
            currentMainAccountId = ledgerJournalEngine.onPrimaryAccountSegmentChanged(Group4_AccountNum, currentMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onPrimaryAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスに従うことによって新しいメソッドを追加できます。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

### <a name="group4offsetaccount"></a>Group4\_OffsetAccount

(**フォーム**タブの下にある検索バーで「Group4\_OffsetAccount」を検索してください。)

#### <a name="step-1"></a>ステップ１

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    void gotFocus()
    {
        super();
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            group4_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!group4_OffsetAccount.allowEdit())
        {
            group4_OffsetAccount.allowEdit(true);
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  ledgerJournalTable バッファを更新するコードの後に、**initLedger()** メソッドのコードを更新します。

        . . .
        if (ledgerJournalTable.FixedOffsetAccount)
        {
            gridOffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger); group4_OffsetAccount.allowEdit(ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger);
        }
        else if (!gridOffsetAccount.allowEdit())
        {
            gridOffsetAccount.allowEdit(true);
            group4_OffsetAccount.allowEdit(true);
        }
        . . .

2.  **gotFocus()** メソッドを削除します。

#### <a name="step-2"></a>ステップ２

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public void jumpRef()
    {
        GridOffsetAccount.jumpRef();
        LedgerJournalTrans_OffsetAccount1.jumpRef();
        Group4_OffsetAccount.jumpRef();
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **jumpRef()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

#### <a name="step-3"></a>ステップ 3

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void loadSegments()
    {
        super();
        GridOffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        LedgerJournalTrans_OffsetAccount1.parmJournalName(ledgerJournalTable.JournalName);
        Group4_OffsetAccount.parmJournalName(ledgerJournalTable.JournalName);
        GridOffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        LedgerJournalTrans_OffsetAccount1.parmCurrency(ledgerJournalTrans.CurrencyCode);
        Group4_OffsetAccount.parmCurrency(ledgerJournalTrans.CurrencyCode);
        GridOffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        LedgerJournalTrans_OffsetAccount1.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        Group4_OffsetAccount.parmDataAreaId(ledgerJournalTrans.getOffsetCompany());
        GridOffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);
        LedgerJournalTrans_OffsetAccount1.parmControlDate(ledgerJournalTrans.TransDate);
        Group4_OffsetAccount.parmControlDate(ledgerJournalTrans.TransDate);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.loadSegments();
        currentOffsetMainAccountId = dimOffsetAccountController.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

**GridOffsetAccount.loadSegments()** メソッドの移行手順は、すでにこのメソッドに必要な変更のほとんどを行いました。 ただし、次の変更を加える必要があります。

1.  **LedgerJournalTrans** データ ソースの **active** メソッドでコードを更新します。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }

        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

2.  **LedgerJournalTrans** データ ソースの **OffsetAccountType** フィールドの **modified()** メソッドで同じ変更を行います。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }
        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

3.  **initLedger()** メソッドで同じ変更を行います。

        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            currentOffsetMainAccountId = GridOffsetAccount.getValue(DimensionAttribute::getWellKnownDimensionAttribute(DimensionAttributeType::MainAccount));
        }
        else
        {
            currentOffsetMainAccountId = 0;
        }
        // Lock the main account segment if "Fixed offset account" is selected in Journal Names
        if (ledgerJournalTrans.OffsetAccountType == LedgerJournalACType::Ledger)
        {
            GridOffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            LedgerJournalTrans_OffsetAccount1.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
            Group4_OffsetAccount.parmLockMainAccountSegment(ledgerJournalTable.FixedOffsetAccount);
        }

4.  **loadSegments()** メソッドを削除します。

#### <a name="step-4"></a>ステップ 4

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] Fix controller usage, if any, in this method based on the migration guidance */
    public void lookup()
    {
        if (!ledgerJournalEngine.offsetAccountNumLookUp(group4_OffsetAccount, ledgerJournalTrans))
        {
            super();
        }
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドは、コントロールのカスタム ルックアップを実装します。 したがって、メソッドをそのままにします。 "仕事" を削除します。 カスタムのルックアップをフック アップするには、SEC の **checkUseCustomLookup** メソッドをオーバーライドする必要があります。 また、カスタム ルックアップ フォームで **closeSelectRecord** メソッドが上書きされたことを確認してください。 例については、**CustTableLookup** フォームを参照してください。

#### <a name="step-5"></a>ステップ 5

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] For custom implementation, code in this method needs to be moved elsewhere based on the migration guidance */
    public void segmentValueChanged(SegmentValueChangedEventArgs _e)
    {
        super(_e);

        /* TODO: (Code Upgrade) [Segmented entry control] Replace this based on the migration guidance */
        // dimOffsetAccountController.segmentValueChanged(_e);
        currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(dimOffsetAccountController, currentOffsetMainAccountId, ledgerJournalTrans);
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

1.  コントロールの **onSegmentChanged()** メソッドをオーバーライドし、次のコードを追加します。

        /// <summary>
        /// The event handler for the segment change event.
        /// </summary>
        /// <param name = "_segment">The segment that was modified.</param>
        public void onSegmentChanged(DimensionControlSegment _segment)
        {
            super(_segment);
            currentOffsetMainAccountId = ledgerJournalEngine.onOffsetAccountSegmentChanged(
            Group4_OffsetAccount, currentOffsetMainAccountId, ledgerJournalTrans);
        }

2.  **segmentValueChanged()** メソッドを削除します。 **注記:** **onOffsetAccountSegmentChanged()** メソッドでは、コントローラー オブジェクトが必要ですが、このコードは SEC のインスタンスを渡すので、**onSegmentChanged()** メソッドの前のコードはコンパイルされません。 コントロール インスタンスでメソッドを呼び出すには、メソッドのシグネチャとその実装を適宜変更する必要があります。 このメソッドは、50 以上の呼び出し元が使用されます。 したがって、これらの呼び出しをすべて更新する必要があります。 または、このガイダンスに従うことによって新しいメソッドを追加できます。

#### <a name="step-6"></a>ステップ 6

##### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

    /* TODO: (Code Upgrade) [Segmented entry control] This method can be removed if there is no custom implementation */
    public boolean validate()
    {
        boolean isValid;
        isValid = super();

        /* TODO: (Code Upgrade) [Segmented entry control] This statement can be removed if there is no custom logic */
        // isValid = dimOffsetAccountController.validate() && isValid;
        return isValid;
    }

##### <a name="dynamics-ax-for-operations"></a>Dynamics AX for Operations

このメソッドはコントロールの **validate()** メソッドのみを呼び出し追加の処理は実行しないため、削除できます。

<a name="additional-resources"></a>その他のリソース
--------

[セグメント化されたエントリ コントロールのダイアログのサポート](segmented-entry-control-dialog-support.md)

[セグメント化されたエントリ コントロールのメタデータ詳細](segmented-entry-control-metadata-specification.md)

[セグメント化されたエントリ コントロールの Parm メソッド詳細](segmented-entry-control-parm-method-specification.md)

[セグメント化されたエントリ コントロール - 移行のガイダンス](segmented-entry-control-migration-guidance.md)



