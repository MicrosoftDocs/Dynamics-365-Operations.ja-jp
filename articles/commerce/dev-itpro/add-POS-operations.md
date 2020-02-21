---
title: ボタン グリッドのデザイナーを使用して、POS 操作を POS レイアウトに追加
description: このトピックでは、新しい POS 工程を作成し、ボタン グリッド デザイナーを使用して POS レイアウトに追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-31
ms.dyn365.ops.version: Application update 4
ms.openlocfilehash: 572077b39fa8549526f36a7de94fbae4387216a9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004607"
---
# <a name="add-pos-operations-to-pos-layouts-by-using-button-grid-designer"></a>ボタン グリッドのデザイナーを使用して、POS 操作を POS レイアウトに追加

[!include[banner](../includes/banner.md)]

このトピックでは、新しい販売時点管理 (POS) 工程を作成し、ボタン グリッド デザイナーを使用して POS レイアウトに追加する方法について説明します。 このトピックは、プラットフォーム更新プログラム 8 とアプリケーション更新プログラム 4 修正プログラムがインストールされている次のアプリケーションに適用されます。

- 財務
- Dynamics 365 Commerce

ユーザーがボタンをクリックしたときに POS でビジネス ロジックを実行したい場合は、POS 操作を作成する必要があります。 POS 操作では複数の活動およびワークフローを実行できます。 たとえば、新しいビューを開いたり、ユーザーの入力を求めたり、ビジネス ロジックを実行したりすることができます。 すべての標準およびカスタム POS 操作では、プレ トリガーおよびポスト トリガーをサポートします。

> [!NOTE]
> ロジックを別のワークフローの一部として実行する必要のある場合、もしくはボタンのクリックが不要な場合は、POS 要求/応答アプリケーション プログラミング インターフェイス (API) を作成します。 POS 操作はこれらのシナリオで必須ではありません。

毎回の操作では、次の要素を実装する必要があります。

- **操作要求** – 操作要求は、**ExtensionOperationRequestBase** クラスから拡張されています。 操作を実行するために必要なすべての入力が含まれています。
- **操作要求** – 操作要求は**応答**クラスから拡張されています。 工程の実行に基づく応答全体が含まれています。
- **操作ファクトリ** – 操作ファクトリは、操作のためのボタンのクリックを操作ハンドラーとリンクします。
- **操作ハンドラー** – 操作ハンドラーは、**ExtensionOperationRequestHandlerBase** クラスから拡張されています。 工程のコア ロジックが含まれています。 すべてのビジネス ロジックはハンドラーに記述され、操作実行後、工程応答に戻される必要があります。

## <a name="create-a-pos-operation"></a>POS 操作の作成

このセクションでは、簡略化された営業終了 (EOD) 処理を行うサンプル工程を作成する方法について説明します。 この操作は、シーケンス内の標準の支払/入金の削除、金庫保管、支払/入金申告、およびシフトのクローズ操作を呼び出します。 したがって、この 1 回の操作は、複数の手順を組み合わせたものです。 定義する条件に基づいて実行されます。

> [!NOTE]
> 新しい工程を作成して独自のカスタム ロジックを実行したり、カートにアイテムを追加したり、ライン割引を適用したりするなど、既存の POS オペレーションを呼び出すことも、現在のカートを取得する、拡張プロパティを設定するなどの既存の API を呼び出すこともできます。

1. Microsoft Visual Studio 2015 を管理者モードで起動します。
2. **...\RetailSDK\POSOpen** から、**ModernPOS** ソリューションを開きます。
3. **POS.Extensions** プロジェクトで、**EODSample** というフォルダーを作成します。
4. **EODSample** フォルダーで、**Operations** というフォルダーを作成します。

### <a name="create-the-operation-request-class"></a>operation request クラスの作成

1. **工程** フォルダで、**EndOfDayOperationRequest.ts** という typescript (.ts) ファイルを作成します。
2. **EndOfDayOperationRequest.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { ExtensionOperationRequestBase } from "PosApi/Create/Operations";
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    ```

3. **EndOfDayOperationRequest** という名のクラスを追加し、**ExtensionOperationRequestBase** クラスから拡張します。
    この例では、**super** メソッドでの工程 ID が **5001** に初期化されます。 ただし、4001 からすべての操作 ID を使用できます。 操作 ID 0 ～ 4000 が内部の POS 操作に対して引当が済んでおり、2 つの操作が同じ操作 ID を持つ必要がありません。 さらに、顧客パラメーター フィールドは工程 ID が 4001 またはそれ以上である場合にのみ、ボタン グリッド デザイナー プロパティに表示されます。 (カスタム パラメーターフィールドを使用して、小売用バックオフィスから POS 操作にパラメータを渡すことができます。)

    ```typescript
    /**
     * (Sample) Operation request for executing end of day operations.
     */
    export default class EndOfDayOperationRequest<TResponse extends EndOfDayOperationResponse> extends ExtensionOperationRequestBase<TResponse> {
        constructor(correlationId: string) {
            super(5001, correlationId);
        }
    }
    ```
    
### <a name="create-the-operation-response-class"></a>operation response クラスの作成

1. **工程** フォルダーで、**EndOfDayOperationResponse.ts** という typescript (.ts) ファイルを作成します。
2. **EndOfDayOperationResponse.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { Response } from "PosApi/Create/RequestHandlers";
    ```

3. **EndOfDayOperationResponse** という名のクラスを追加し、**応答**クラスから拡張します。

    ```typescript
    /**
     * (Sample) Operation response of executing end of day operations.
     */
    export default class EndOfDayOperationResponse extends Response { }
    ```

### <a name="create-the-operation-handler-class"></a>operation handler クラスの作成

1. **工程** フォルダーで、**EndOfDayOperationRequestHandler.ts** という typescript (.ts) ファイルを作成します。
2. **EndOfDayOperationRequestHandler.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { ExtensionOperationRequestType, ExtensionOperationRequestHandlerBase } from "PosApi/Create/Operations";
    import { CloseShiftOperationRequest, CloseShiftOperationResponse } from "PosApi/Consume/Shifts";
    import { SafeDropOperationRequest, SafeDropOperationResponse } from "PosApi/Consume/StoreOperations";
    import { TenderDeclarationOperationRequest, TenderDeclarationOperationResponse } from "PosApi/Consume/StoreOperations";
    import { TenderRemovalOperationRequest, TenderRemovalOperationResponse } from "PosApi/Consume/StoreOperations";
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    import EndOfDayOperationRequest from "./EndOfDayOperationRequest";
    import { ClientEntities } from "PosApi/Entities";|
    ```

3. **EndOfDayOperationRequestHandler** という名のクラスを追加し、**ExtensionOperationRequestHandlerBase** クラスから拡張します。

    各ハンドラーは、2 つのメソッドを実装する必要があります。

   - supportedRequestType
   - executeAsync
   
    ```typescript
    export default class EndOfDayOperationRequestHandler<TResponse extends EndOfDayOperationResponse> extends ExtensionOperationRequestHandlerBase<TResponse> {}
    ```

4. サポートされている要求タイプをクラスに追加します。

    ```typescript
    /**
     * Gets the supported request type.
     * @return {RequestType<TResponse>} The supported request type.
     */
    public supportedRequestType(): ExtensionOperationRequestType<TResponse> {
        return EndOfDayOperationRequest;
    }
    ```

5. **executeAsync** メソッドを実装します。

    ```typescript
    /**
     * Executes the request handler asynchronously.
     * @param {EndOfDayOperationRequest<TResponse>} request The request.
     * @return {Promise<ICancelableDataResult<TResponse>>} The cancelable async result containing the response.
     */
    public executeAsync(printRequest: EndOfDayOperationRequest<TResponse>): Promise<ClientEntities.ICancelableDataResult<TResponse>> {
        this.context.logger.logInformational("Log message from PrintOperationRequestHandler executeAsync().", this.context.logger.getNewCorrelationId());
        // Tender Removal
        let tenderRemovalRequest: TenderRemovalOperationRequest<TenderRemovalOperationResponse> =
        new TenderRemovalOperationRequest(this.context.logger.getNewCorrelationId());
        return this.context.runtime.executeAsync(tenderRemovalRequest).then((result: ClientEntities.ICancelableDataResult<TenderRemovalOperationResponse>)
        : Promise<Commerce.Client.Entities.ICancelableDataResult<SafeDropOperationResponse>> => {
            // Safe Drop
            if (!result.canceled) {
                let safeDropRequest: SafeDropOperationRequest<SafeDropOperationResponse> =
                new SafeDropOperationRequest(this.context.logger.getNewCorrelationId());
                return this.context.runtime.executeAsync(safeDropRequest);
            } else {
                return Promise.resolve({
                    canceled: true,
                    data: null
                });
            }
        }).then((result: Commerce.Client.Entities.ICancelableDataResult<SafeDropOperationResponse>)
        : Promise<ClientEntities.ICancelableDataResult<TenderDeclarationOperationResponse>> => {
            // Tender Declaration
            if (!result.canceled) {
                let tenderDeclarationRequest: TenderDeclarationOperationRequest<TenderDeclarationOperationResponse> =
                new TenderDeclarationOperationRequest(this.context.logger.getNewCorrelationId());
                return this.context.runtime.executeAsync(tenderDeclarationRequest);
            } else {
                return Promise.resolve({
                    canceled: true,
                    data: null
                });
            }
        }).then((result: ClientEntities.ICancelableDataResult<TenderDeclarationOperationResponse>)
        : Promise<ClientEntities.ICancelableDataResult<CloseShiftOperationResponse>> => {
            // Close Shift
            if (!result.canceled) {
                return new Promise(
                    (resolve: (value?: ClientEntities.ICancelableDataResult<CloseShiftOperationResponse>) => void, reject: (reason?: any) => void) => {
                        // A delay of ten seconds is added here as a work-around for issues with printing a second receipt to the windows driver
                        // printer before the first dialog is closed. A ten second delay gives the user a chance to close the first dialog before
                        // the issue occurs.
                        setTimeout(() => { resolve(null); }, 10000);
                    }).then(() => {
                        let closeShiftOperationRequest: CloseShiftOperationRequest<CloseShiftOperationResponse> =
                        new CloseShiftOperationRequest(this.context.logger.getNewCorrelationId());
                        return this.context.runtime.executeAsync(closeShiftOperationRequest);
                    });
            } else {
                return Promise.resolve({
                    canceled: true,
                    data: null
                });
            }
        }).then((result: ClientEntities.ICancelableDataResult<CloseShiftOperationResponse>)
        : ClientEntities.ICancelableDataResult<EndOfDayOperationResponse> => {
                return <ClientEntities.ICancelableDataResult<EndOfDayOperationResponse>>{
                    canceled: result.canceled,
                    data: result.canceled ? null : new EndOfDayOperationResponse()
                };
            });
        }
    }
    ```

    全体的なコードは、次のようになります。

    ```typescript
    /**
     * SAMPLE CODE NOTICE
     *
     * THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
     * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
     * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
     * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
     */
    import { ExtensionOperationRequestType, ExtensionOperationRequestHandlerBase } from "PosApi/Create/Operations";
    import { CloseShiftOperationRequest, CloseShiftOperationResponse } from "PosApi/Consume/Shifts";
    import { SafeDropOperationRequest, SafeDropOperationResponse } from "PosApi/Consume/StoreOperations";
    import { TenderDeclarationOperationRequest, TenderDeclarationOperationResponse } from "PosApi/Consume/StoreOperations";
    import { TenderRemovalOperationRequest, TenderRemovalOperationResponse } from "PosApi/Consume/StoreOperations";
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    import EndOfDayOperationRequest from "./EndOfDayOperationRequest";
    import { ClientEntities } from "PosApi/Entities";
    /**
     * (Sample) Request handler for the EndOfDayOperationRequest class.
     */
    export default class EndOfDayOperationRequestHandler<TResponse extends EndOfDayOperationResponse> extends ExtensionOperationRequestHandlerBase<TResponse> {
        /**
         * Gets the supported request type.
         * @return {RequestType<TResponse>} The supported request type.
         */
        public supportedRequestType(): ExtensionOperationRequestType<TResponse> {
            return EndOfDayOperationRequest;
        }
        /**
         * Executes the request handler asynchronously.
         * @param {EndOfDayOperationRequest<TResponse>} request The request.
         * @return {Promise<ICancelableDataResult<TResponse>>} The cancelable async result containing the response.
         */
        public executeAsync(printRequest: EndOfDayOperationRequest<TResponse>): Promise<ClientEntities.ICancelableDataResult<TResponse>> {
            this.context.logger.logInformational("Log message from PrintOperationRequestHandler executeAsync().", this.context.logger.getNewCorrelationId());
            // Tender Removal
            let tenderRemovalRequest: TenderRemovalOperationRequest<TenderRemovalOperationResponse> =
            new TenderRemovalOperationRequest(this.context.logger.getNewCorrelationId());
            return this.context.runtime.executeAsync(tenderRemovalRequest).then((result: ClientEntities.ICancelableDataResult<TenderRemovalOperationResponse>)
            : Promise<Commerce.Client.Entities.ICancelableDataResult<SafeDropOperationResponse>> => {
                // Safe Drop
                if (!result.canceled) {
                    let safeDropRequest: SafeDropOperationRequest<SafeDropOperationResponse> =
                    new SafeDropOperationRequest(this.context.logger.getNewCorrelationId());
                    return this.context.runtime.executeAsync(safeDropRequest);
                } else {
                    return Promise.resolve({
                        canceled: true,
                        data: null
                    });
                }
            }).then((result: Commerce.Client.Entities.ICancelableDataResult<SafeDropOperationResponse>)
            : Promise<ClientEntities.ICancelableDataResult<TenderDeclarationOperationResponse>> => {
                // Tender Declaration
                if (!result.canceled) {
                    let tenderDeclarationRequest: TenderDeclarationOperationRequest<TenderDeclarationOperationResponse> =
                    new TenderDeclarationOperationRequest(this.context.logger.getNewCorrelationId());
                    return this.context.runtime.executeAsync(tenderDeclarationRequest);
                } else {
                    return Promise.resolve({
                        canceled: true,
                        data: null
                    });
                }
            }).then((result: ClientEntities.ICancelableDataResult<TenderDeclarationOperationResponse>)
            : Promise<ClientEntities.ICancelableDataResult<CloseShiftOperationResponse>> => {
                // Close Shift
                if (!result.canceled) {
                    return new Promise(
                        (resolve: (value?: ClientEntities.ICancelableDataResult<CloseShiftOperationResponse>) => void, reject: (reason?: any) => void) => {
                            // A delay of ten seconds is added here as a work-around for issues with printing a second receipt to the windows driver
                            // printer before the first dialog is closed. A ten second delay gives the user a chance to close the first dialog before
                            // the issue occurs.
                            setTimeout(() => { resolve(null); }, 10000);
                    }).then(() => {
                        let closeShiftOperationRequest: CloseShiftOperationRequest<CloseShiftOperationResponse> =
                        new CloseShiftOperationRequest(this.context.logger.getNewCorrelationId());
                        return this.context.runtime.executeAsync(closeShiftOperationRequest);
                    });
                } else {
                    return Promise.resolve({
                        canceled: true,
                        data: null
                    });
                }
            }).then((result: ClientEntities.ICancelableDataResult<CloseShiftOperationResponse>)
            : ClientEntities.ICancelableDataResult<EndOfDayOperationResponse> => {
                return <ClientEntities.ICancelableDataResult<EndOfDayOperationResponse>>{
                    canceled: result.canceled,
                    data: result.canceled ? null : new EndOfDayOperationResponse()
                };
            });
        }
    }
    ```

### <a name="create-the-operation-factory-class"></a>operation factory クラスの作成

1. **工程** フォルダで、**EndOfDayOperationRequestFactory.ts** という typescript (.ts) ファイルを作成します。
2. **EndOfDayOperationRequestFactory.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    import EndOfDayOperationRequest from "./EndOfDayOperationRequest";
    import { ExtensionOperationRequestFactoryFunctionType, IOperationContext } from "PosApi/Create/Operations";
    import { ClientEntities } from "PosApi/Entities";
    ```

3. 操作ハンドラーおよび操作ボタンをリンクする機能を追加します。

    ```typescript
    let getOperationRequest: ExtensionOperationRequestFactoryFunctionType<EndOfDayOperationResponse> =
    /**
     * Gets an instance of EndOfDayOperationRequest.
     * @param {number} operationId The operation Id.
     * @param {string[]} actionParameters The action parameters.
     * @param {string} correlationId A telemetry correlation ID, used to group events logged from this request together with the calling context.
     * @return {EndOfDayOperationRequest<TResponse>} Instance of EndOfDayOperationRequest.
     */
    function (
        context: IOperationContext,
        operationId: number,
        actionParameters: string [],
        correlationId: string
    ): Promise<ClientEntities.ICancelableDataResult<EndOfDayOperationRequest<EndOfDayOperationResponse>>> {
        let operationRequest: EndOfDayOperationRequest<EndOfDayOperationResponse> = new EndOfDayOperationRequest<EndOfDayOperationResponse>(correlationId);
        return Promise.resolve(<ClientEntities.ICancelableDataResult<EndOfDayOperationRequest<EndOfDayOperationResponse>>>{
            canceled: false,
            data: operationRequest
        });
    };
    export default getOperationRequest;
    ```

    全体的なコードは、次のようになります。

    ```typescript
    /**
     * SAMPLE CODE NOTICE
     *
     * THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
     * OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
     * THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
     * NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
     */
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    import EndOfDayOperationRequest from "./EndOfDayOperationRequest";
    import { ExtensionOperationRequestFactoryFunctionType, IOperationContext } from "PosApi/Create/Operations";
    import { ClientEntities } from "PosApi/Entities";
    let getOperationRequest: ExtensionOperationRequestFactoryFunctionType<EndOfDayOperationResponse> =
    /**
     * Gets an instance of EndOfDayOperationRequest.
     * @param {number} operationId The operation Id.
     * @param {string[]} actionParameters The action parameters.
     * @param {string} correlationId A telemetry correlation ID, used to group events logged from this request together with the calling context.
     * @return {EndOfDayOperationRequest<TResponse>} Instance of EndOfDayOperationRequest.
     */
    function (
        context: IOperationContext,
        operationId: number,
        actionParameters: string[],
        correlationId: string
    ): Promise<ClientEntities.ICancelableDataResult<EndOfDayOperationRequest<EndOfDayOperationResponse>>> {
        let operationRequest: EndOfDayOperationRequest<EndOfDayOperationResponse> = new EndOfDayOperationRequest<EndOfDayOperationResponse>(correlationId);
        return Promise.resolve(<ClientEntities.ICancelableDataResult<EndOfDayOperationRequest<EndOfDayOperationResponse>>>{
            canceled: false,
            data: operationRequest
        });
    };
    export default getOperationRequest;
    ```

4. **manifest.json** ファイルを開き、次のコードに貼り付けます。

    ```typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_EODSample",
        "publisher": "Microsoft",
        "version": "7.3.0",
        "minimumPosVersion": "7.3.0.0",
        "components": {
            "create": {
                "operations": [
                    {
                        "operationId": "5001",
                        "operationRequestFactoryPath": "Operations/ EndOfDayOperationRequestFactory",
                        "operationRequestHandlerPath": "Operations/ EndOfDayOperationRequestHandler"
                    }
                ]
            }
        }
    }
    ```

5. **extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**EODSample** で更新し、実行時に POS に拡張機能が含まれるようにします。

    ```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions"
            },
            {
            "baseUrl": "EODSample"
            }
        ]
    }
    ```

6. **tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストでコメント アウトします。 POS では、このファイルを使用して、拡張機能を追加または除外します。 既定では、リストに除外された拡張リスト全体が含まれています。 拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、拡張リストの拡張をコメントアウトします。

    ```typescript
    "extends": "../tsconfigs/tsmodulesconfig",
    "exclude": [
        "AuditEventExtensionSample",
        "B2BSample",
        "CustomerSearchWithAttributesSample",
        "FiscalRegisterSample",
        //"EODSample",
        "PromotionsSample",
        "SalesTransactionSignatureSample",
        "SampleExtensions2",
        //"SampleExtensions",
        "StoreHoursSample",
        "SuspendTransactionReceiptSample"
    ],
     ```

7. プロジェクトをコンパイル、およびリビルドします。

## <a name="add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters"></a>小売用バックオフィス内の POS レイアウトにカスタム操作ボタンを追加します

1. Retail で**小売りとコマース &gt; チャンネル設定 &gt; POS 設定 &gt; POS &gt; 工程**の順に移動します。
2. **EOD** という工程を作成して、**5001** の工程 ID をもつようにします。
3. **小売とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS &gt; ボタン グリッド**の順に移動します。
4. **'F2W2'** コードのフィルターです。
5. **デザイナー**ボタンを選択し、次の手順にしたがってデザイナーをインストールします。 資格情報を求めるメッセージが表示されたら、Retail のユーザー名とパスワードを入力します。
6. デザイナ領域で右クリックし、**新しい行の追加**を選択します。
7. 新しいボタンを右クリックし、**ボタン プロパティ** を選択します。
8. **EOD** に **アクション**プロパティを設定します。 **OK** を選択し、デザイナーを閉じます。
9. **小売りとコマース** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。
10. **1090** を選択してから、**今すぐ実行**を選択します。

    > [!NOTE]
    > 上記の手順では、デモ データを使用していることを前提としています。 デモ データを使用していない場合は、カスタム構成に従ってボタンを作成して追加します。

## <a name="validate-your-extension"></a>拡張機能の検証

1. F5 キーを押し、POS を展開してカスタマイズをテストします。
2. トランザクション画面で、新しい **EOD** 操作ボタンを選択し、手順を実行します。
