---
title: POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加
description: この記事では、顧客の追加/編集画面などの既存の POS ビューを拡張する方法について説明します。
author: mugunthanm
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-22
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9e582e0ce1fd06cb47f39bb29c8d5fbefda55014
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850290"
---
# <a name="extend-pos-views-to-add-custom-columns-and-app-bar-buttons"></a>POS ビューの拡張によるカスタム列およびアプリ バー ボタンの追加

[!include [banner](../../includes/banner.md)]

この記事では、既存の販売時点管理 (POS) ビューを拡張する方法について説明します。 **トランザクション** 画面および **ようこそ** 画面を拡張するには、画面レイアウト デザイナーを使用します。 **顧客の追加/編集** 画面など、他のすべての POS ビューを拡張するには、Retail ソフトウェア開発キット (SDK) を使用します。 この記事では、Retail SDK による既存の POS ビューの拡張について説明します。



POS ビューでは、次の拡張ポイントとパターンがサポートされます。

- **カスタム アプリケーション バーのボタン** - 選択したページのアプリケーション バーにカスタム ボタンを追加します。
- **カスタム列セット** - 選択したページのグリッド列をカスタム列に置き換えます。
- **カスタム コントロール** - 選択したページに、新しいコントロールを追加します。
- **カスタム フィルター** – 選択したページにカスタム フィルターを追加します。

## <a name="pos-views-that-currently-support-extensions"></a>現在拡張機能をサポートする POS ビュー

次のテーブルに、現在拡張機能をサポートしている POS ビューを示します。 また、各 POS ビューがサポートする拡張ポイントのタイプも示します。

> [!NOTE]
> 今後のリリースと修正プログラムで、他のビューの拡張ポイントをさらにサポートします。


| POS ビュー (リリース)              | カスタム コントロールがサポートされています | カスタム列がサポートされています | カスタムのアプリ バーのボタンがサポートされています |
|---------------------------------|-------------------------------|------------------------------|--------------------------------------|
| カート ビュー (画面レイアウトに基づく) | 有                           | 有                          | 無                                   |
| CustomerAddEditView             | 有                           | 無                           | 有                                  |
| CustomerDetailsView             | 有                           | 無                           | 有                                  |
| SearchView                      | 無                            | 有                          | 有                                  |
| InventoryLookupView             | 無                            | 有                          | 有                                  |
| ShowJournalView                 | 無                            | 有                          | 有                                  |
| SimpleProductDetailsView        | はい                           | いいえ                           | はい                                  |
| AddressAddEditView              | はい                           | いいえ                           | はい                                  |
| PaymentView                     | いいえ                            | いいえ                           | はい                                  |
| PriceCheckView                  | はい                           | いいえ                           | はい                                   |
| PriceCheckViewPhone             | いいえ                            | いいえ                           | はい                                   |
| SearchOrdersView                | いいえ                            | はい                          | いいえ                                   |
| SearchPickingAndReceivingView   | 無                            | 有                          | 有                                   |
| CustomerOrderHistoryView        | 無                            | 有                          | 無                                   |
| SearchStockCountView            | なし                            | あり                          | なし                                   |
| StockCountDetailsView           | なし                            | あり                          | あり                                   |
| ResumeCartView                  | なし                            | あり                          | あり                                    |
| InventoryLookupMatrixView       | なし                            | なし                           | はい                                   |
| SuspendTransactionView          | 無                            | あり                          | なし                               |   
| ManageShiftView                 | なし                            | なし                           | あり                               |  
| ReportDetailsView               | なし                            | なし                           | あり                               |
| TransferOrderDetailsView        | なし                            | なし                           | あり                               |
| FulfillmentLineView             | いいえ                            | はい                          | はい                               |
| ReturnTransactionView           | いいえ                            | はい                          | はい                               |
| PickingAndReceivingDetailsView  | いいえ                            | はい                          | はい                    |
| PickingAndReceivingDetailsView (高度な倉庫)  | 無                            | 有                          | 有           |
| SalesInvoiceDetailsView (10.0.11) | 無                            | 無                          | 有           |
| SalesInvoicesView (10.0.11) | 無                            | 有                          | 無           |
| InventoryDocumentShippingAndReceivingView (10.0.13) | なし                            | はい (10.0.23)                          | あり           |
| InventoryDocumentListView  | なし                            | はい (10.0.15)                          | はい (10.0.13)          |
| ManageShiftsView  | なし                            | はい (10.0.21)                          | なし          |



> [!NOTE]
> 上記に表示される表は、リリースされた最新バージョンおよび修正プログラムに基づいて更新されています。 旧バージョンでは、これらの拡張ポイントの一部は使用できません。
>
> 仕訳帳の表示 (行グリッド) と 返品トランザクション ビューでは、行サブ フィールドを使用してカスタム列をサポートしています。 これらのサブ フィールドは、情報コード メッセージ、シリアル番号、割引の値などのように、列ではなく行として表示されます。

## <a name="custom-filter-extension"></a>カスタム フィルターの拡張機能

次の表の POS ビューでは、カスタム フィルター拡張機能がサポートされています。 **注文検索ビュー** は拡張機能を使用してユーザー インターフェイス (UI) に検索用の既定パラメーターを設定することもサポートしています。 たとえば、店舗検索において既定のパラメーターを追加する場合は、拡張機能を使用して UI にそのパラメーターを表示することができます。 

| POS ビュー                                   | カスタム フィルターはサポートされていますか?  | 既定のフィルター パラメーター?    | リリース |
|--------------------------------------------|-------------------------------|-----------------------------|--------------------------------|
| ShowJournalView                            | 有効                           | 無効                          |                                |
| SearchOrdersView                           | 有効                           | 有効                         |                                |
| FulfillmentLineView                        | 有効                           | 無効                          |                                |
| InventoryDocumentListView                  | 有効                           | 無効                          | 10.0.23                        |
| InventoryDocumentShippingAndReceivingView  | 有効                           | 無効                          | 10.0.25                        |
| InventoryAdjustmentDocumentListView        | 有効                           | 無効                          | 10.0.25                        |
| InventoryAdjustmentDocumentWorkingView     | 有効                           | 無効                          | 10.0.25                        |
| InventoryDocumentStockCountingListView     | 有効                           | 無効                          | 10.0.25                        |
| InventoryDocumentStockCountingWorkingView  | 有効                           | 無効                          | 10.0.25                        |

カスタム フィルターの拡張機能のサンプル コードは、Retail SDK (...\RetailSDK\Code\POS\Extensions\SampleExtensions\ViewExtensions\SearchOrders\SampleOrderSearchTextFilter.ts) で使用可能です。

## <a name="add-a-custom-column-and-an-app-bar-button"></a>カスタム列とアプリ バー ボタンの追加

1. Microsoft Visual Studio 2015 を管理者として起動します。
2. **ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。
3. **POS.Extensions** プロジェクトで、**SearchExtension** というフォルダーを作成します。
4. **SearchExtension** フォルダーで、**ViewExtensions** というフォルダーを作成します。
5. **ViewExtensions** フォルダーで、**Search** というフォルダーを作成します。
6. **Search** フォルダーで、**CustomCustomerSearchColumns.ts** という Typescript ファイルを作成します。
7. **CustomCustomerSearchColumns.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { ICustomerSearchColumn } from "PosApi/Extend/Views/SearchView";
    import { ICustomColumnsContext } from "PosApi/Extend/Views/CustomListColumns";
    import { ProxyEntities } from "PosApi/Entities";
    ```

8. ファイルに既存の列とカスタム列を追加します。

    ```typescript
    export default (context: ICustomColumnsContext): ICustomerSearchColumn[] => {
        return [
            {
                title: context.resources.getString("string_2"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.AccountNumber; },
                ratio: 15,
                collapseOrder: 5,
                minWidth: 120
             }, {
                title: context.resources.getString("string_3"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.FullName; },
                ratio: 20,
                collapseOrder: 4,
                minWidth: 200
            }, {
                title: context.resources.getString("string_4"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.FullAddress; },
                ratio: 25,
                collapseOrder: 1,
                minWidth: 200
            }, {
                title: context.resources.getString("string_5"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.Email; },
                ratio: 20,
                collapseOrder: 2,
                minWidth: 200
            }, {
                title: context.resources.getString("string_7"),
                computeValue: (row: ProxyEntities.GlobalCustomer): string => { return row.Phone; },
                ratio: 20,
                collapseOrder: 3,
                minWidth: 120
            }
        ];
    };
    ```

9. ここで、列の名前のローカライズのためのリソース ファイルを追加します。 **SearchExtension** フォルダーで、**Resources** というフォルダーを作成します。
10. **Resources** フォルダーで、**Strings** というフォルダーを作成します。
11. **Strings** フォルダーで、**en-US** というフォルダーを作成します。
12. **en-us** フォルダーで、**resources.resjson** というファイルを作成します。
13. **resources.resjson** ファイルに次のコードを追加します。

    ```typescript
    {
        //======================== Sample View extensions strings. ========================
        "string_0" : "Quick compare products",
        "_string_0.comment" : "Product search page app bar command label.",
        "string_1" : "View customer summary",
        "_string_1.comment" : "Customer search page app bar command label.",
        //======================== Column names. ========================
        "string_2" : "ACCOUNT NUMBER_CUSTOMIZED",
        "_string_2.comment" : "Customer search column name.",
        "string_3" : "NAME",
        "_string_3.comment" : "Customer search column name.",
        "string_4" : "ADDRESS",
        "_string_4.comment" : "Customer search column name.",
        "string_5" : "CONTACT EMAIL",
        "_string_5.comment" : "Customer search column name.",
        "string_7" : "PHONE NUMBER",
        "_string_7.comment" : "Customer search column name."
    }
    ```

14. **SearchExtension** フォルダーで、**DialogSample** というフォルダーを作成します。
15. **DialogSample** フォルダーで、**MessageDialog.ts** という TypeScript ファイルを作成します。
16. **MessageDialog.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { ShowMessageDialogClientRequest, ShowMessageDialogClientResponse, IMessageDialogOptions } from "PosApi/Consume/Dialogs";
    import { IExtensionContext } from "PosApi/Framework/ExtensionContext";
    import { ClientEntities } from "PosApi/Entities";
    ```

17. **MessageDialog** という名前のクラスを作成します。

    ```typescript
    export default class MessageDialog {}
    ```

18. **MessageDialog** クラスで、次の **show** メソッドを追加します。

    ```typescript
    public static show(context: IExtensionContext, message: string): Promise<void> {
        let promise: Promise<void> = new Promise<void>((resolve: () => void, reject: (reason?: any) => void) => 
        {
            let messageDialogOptions: IMessageDialogOptions = {
                title: "Extension Message Dialog",
                message: message,
                showCloseX: true, // this property will return "Close" as result when "X" is clicked to close dialog.
                button1: {
                    id: "Button1Close",
                    label: "OK",
                    result: "OKResult"
                },
                button2: {
                    id: "Button2Cancel",
                    label: "Cancel",
                    result: "CancelResult"
                }
            };
            let dialogRequest: ShowMessageDialogClientRequest<ShowMessageDialogClientResponse> =
                new ShowMessageDialogClientRequest<ShowMessageDialogClientResponse>(messageDialogOptions);
                context.runtime.executeAsync(dialogRequest).then((
                    result: ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>) => {
                if (!result.canceled) {
                    context.logger.logInformational("MessageDialog result: " + result.data.result.dialogResult);
                    resolve();
                }
            }).catch((reason: any) => {
            context.logger.logError(JSON.stringify(reason));
            reject(reason);
            });
        });
        return promise;
    }
    ```

19. ここで、選択した顧客に関する詳細を含むダイアログ ボックスを開くために、検索ビューにカスタムのアプリ バー ボタンを追加します。 **ViewExtensions** フォルダーで、**ViewCustomerSummaryCommand.ts** という Typescript ファイルを作成します。
20. **ViewCustomerSummaryCommand.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions, ObjectExtensions } from "PosApi/TypeExtensions";
    import { IExtensionCommandContext } from "PosApi/Extend/Views/AppBarCommands";
    import * as SearchView from "PosApi/Extend/Views/SearchView";
    import MessageDialog from "../../Controls/DialogSample/MessageDialog";
    ```

21. **ViewCustomerSummaryCommand** という名前のクラスを作成し、**CustomerSearchExtensionCommandBase** からクラスを拡張します。

    ```typescript
    export default class ViewCustomerSummaryCommand extends SearchView.CustomerSearchExtensionCommandBase {}
    ```

22. **ViewCustomerSummaryCommand** クラスで、選択した顧客を検索するときに、結果をキャプチャするプライベート変数を宣言します。

    ```typescript
    private _customerSearchResults: ProxyEntities.GlobalCustomer[];
    ```

23. クラス **コンストラクター** メソッドを追加して、検索ハンドラーを初期化してクリアします。

    ```typescript
    constructor(context: IExtensionCommandContext<SearchView.ICustomerSearchToExtensionCommandMessageTypeMap>) {
        super(context);
        this.id = "viewCustomerSummaryCommand";
        this.label = context.resources.getString("string_1");
        this.extraClass = "iconLightningBolt";
        this._customerSearchResults = [];
        this.searchResultsSelectedHandler = (data: SearchView.CustomerSearchSearchResultSelectedData): void => {
            this._customerSearchResults = data.customers;
            this.canExecute = true;
        };
        this.searchResultSelectionClearedHandler = (): void => {
            this._customerSearchResults = [];
            this.canExecute = false;
        };
    }
    ```

24. **init** メソッドを追加して、**表示** プロパティを初期化します。

    ```typescript
    protected init(state: SearchView.ICustomerSearchExtensionCommandState): void {
        this.isVisible = true;
    }
    ```

25. アプリ ボタン クリック ハンドラーを処理する **実行** メソッドを追加します。 **execute** メソッドは、ハンドラーから選択した顧客のデータを読み取り、単純なダイアログ ボックスに表示します。

    ```typescript
    protected execute(): void {
        let customer: ProxyEntities.GlobalCustomer = ArrayExtensions.firstOrUndefined(this._customerSearchResults);
        if (!ObjectExtensions.isNullOrUndefined(customer)) {
            let message: string = "Customer Account: " + (customer.AccountNumber || "") + " | ";
            message += "Name: " + customer.FullName + " | ";
            message += "Phone Number: " + customer.Phone + " | ";
            message += "Email Address: " + customer.Email;
            MessageDialog.show(this.context, message);
        } 
    }
    ```

    コード サンプルの全体は次のようになります。

    ```typescript
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions, ObjectExtensions } from "PosApi/TypeExtensions";
    import { IExtensionCommandContext } from "PosApi/Extend/Views/AppBarCommands";
    import * as SearchView from "PosApi/Extend/Views/SearchView";
    import MessageDialog from "../../DialogSample/MessageDialog";
    export default class ViewCustomerSummaryCommand extends SearchView.CustomerSearchExtensionCommandBase {
        private _customerSearchResults: ProxyEntities.GlobalCustomer[];

        /**
        * Creates a new instance of the ViewCustomerSummaryCommand class.
        * @param {IExtensionCommandContext<CustomerDetailsView.ICustomerSearchToExtensionCommandMessageTypeMap>} context The command context.
        * @remarks The command context contains APIs through which a command can communicate with POS.
        */
        constructor(context: IExtensionCommandContext<SearchView.ICustomerSearchToExtensionCommandMessageTypeMap>) {
            super(context);
            this.id = "viewCustomerSummaryCommand";
            this.label = context.resources.getString("string_1");
            this.extraClass = "iconLightningBolt";
            this._customerSearchResults = [];

            this.searchResultsSelectedHandler = (data: SearchView.CustomerSearchSearchResultSelectedData): void => {
                this._customerSearchResults = data.customers;
                this.canExecute = true;
            };

            this.searchResultSelectionClearedHandler = (): void => {
                this._customerSearchResults = [];
                this.canExecute = false;
            };
        }

        /**
        * Initializes the command.
        * @param {CustomerDetailsView.ICustomerDetailsExtensionCommandState} state The state used to initialize the command.
        */
        protected init(state: SearchView.ICustomerSearchExtensionCommandState): void {
            this.isVisible = true;
        }

        /**
        * Executes the command.
        */
        protected execute(): void {
            let customer: ProxyEntities.GlobalCustomer = ArrayExtensions.firstOrUndefined(this._customerSearchResults);
            if (!ObjectExtensions.isNullOrUndefined(customer)) {
                let message: string = "Customer Account: " + (customer.AccountNumber || "") + " | ";
                message += "Name: " + customer.FullName + " | ";
                message += "Phone Number: " + customer.Phone + " | ";
                message += "Email Address: " + customer.Email;
                MessageDialog.show(this.context, message);
            }
        }
    }
    ```

26. **SearchExtension** フォルダーで、**manifest.json** という JSON ファイルを作成します。
27. **manifest.json** ファイルに次のコードを追加します。

    ```typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Microsoft",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
            "resources": {
                "supportedUICultures": [ "en-US" ],
                "fallbackUICulture": "en-US",
                "culturesDirectoryPath": "Resources/Strings ",
                "stringResourcesFileName": "resources.resjson",
                "cultureInfoOverridesFilePath": "Resources/cultureInfoOverrides.json"
            },
            "extend": {
                "views": {
                    "SearchView": {
                        "customerAppBarCommands": [ { "modulePath": "ViewExtensions/Search/ViewCustomerSummaryCommand" } ],
                        "customerListConfiguration": { "modulePath": "ViewExtensions/Search/CustomCustomerSearchColumns" }
                    }
                }
            }
        }
    }
    ```

28. **POS.Extensions** プロジェクトで **extensions.json** ファイルを開き、**SearchExtension** サンプルで更新して、POS が実行時にこの拡張機能に含まれるようにします。

    ```typescript
    {
        "extensionPackages": [
        {
            "baseUrl": "SampleExtensions2"
        },
        {
            "baseUrl": "SearchExtension"
        }
        ]
    }
    ```

29. **tsconfig.json** ファイルで、除外リストに拡張パッケージ フォルダーをコメントアウトします。 POS は、このファイルを使用して、拡張機能を追加または除外します。 既定では、リストに除外された拡張リスト全体が含まれています。 拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、除外リストの拡張子をコメントアウトします。

    ```typescript
    "exclude": [
    "SampleExtensions"
    //"SampleExtensions2",
    //"SearchExtension"
    ],
    ```

30. プロジェクトをコンパイル、およびリビルドします。

## <a name="validate-the-customization"></a>カスタマイズの検証

カスタマイズを検証するには、これらの手順に従います。

1. オペレーター ID に **000160**、パスワードに **123** を使用して Modern POS にサインインします。
2. 上部の検索バーを使って顧客 **2001** を検索します。

    追加したカスタム列が表示されました。

3. 顧客を選択し、新しいアプリケーション バーのボタンを選択します。 選択した顧客に関する詳細を含むダイアログ ボックスが表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
