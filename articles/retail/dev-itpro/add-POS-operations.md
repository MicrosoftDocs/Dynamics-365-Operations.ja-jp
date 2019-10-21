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
ms.openlocfilehash: 26ca7fd7440aa6c7bda85f60ccb613e081fe3583
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250357"
---
# <a name="add-pos-operations-to-pos-layouts-by-using-button-grid-designer"></a><span data-ttu-id="4cfae-103">ボタン グリッドのデザイナーを使用して、POS 操作を POS レイアウトに追加</span><span class="sxs-lookup"><span data-stu-id="4cfae-103">Add POS operations to POS layouts by using Button grid designer</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4cfae-104">このトピックでは、新しい販売時点管理 (POS) 工程を作成し、ボタン グリッド デザイナーを使用して POS レイアウトに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-104">This topic explains how to create a new point of sale (POS) operation and add it to the POS layout by using Button grid designer.</span></span> <span data-ttu-id="4cfae-105">このトピックは、プラットフォーム更新プログラム 8 とアプリケーション更新プログラム 4 修正プログラムがインストールされている次のアプリケーションに適用されます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-105">This topic applies to the following applications where Platform update 8 and the Application update 4 hotfix are installed:</span></span>

- <span data-ttu-id="4cfae-106">財務</span><span class="sxs-lookup"><span data-stu-id="4cfae-106">Finance</span></span>
- <span data-ttu-id="4cfae-107">Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="4cfae-107">Dynamics 365 Retail</span></span>

<span data-ttu-id="4cfae-108">ユーザーがボタンをクリックしたときに POS でビジネス ロジックを実行したい場合は、POS 操作を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cfae-108">If you want your business logic to be run in the POS when users click a button, you should create POS operations.</span></span> <span data-ttu-id="4cfae-109">POS 操作では複数の活動およびワークフローを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-109">POS operations can run multiple activities or workflows.</span></span> <span data-ttu-id="4cfae-110">たとえば、新しいビューを開いたり、ユーザーの入力を求めたり、ビジネス ロジックを実行したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-110">For example, they can open a new view, ask for user input, or run business logic.</span></span> <span data-ttu-id="4cfae-111">すべての標準およびカスタム POS 操作では、プレ トリガーおよびポスト トリガーをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-111">All standard and custom POS operations support pre-triggers and post-triggers.</span></span>

> [!NOTE]
> <span data-ttu-id="4cfae-112">ロジックを別のワークフローの一部として実行する必要のある場合、もしくはボタンのクリックが不要な場合は、POS 要求/応答アプリケーション プログラミング インターフェイス (API) を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-112">If logic should be run as part of another workflow, or if no button click is required, create POS request/response application programming interfaces (APIs).</span></span> <span data-ttu-id="4cfae-113">POS 操作はこれらのシナリオで必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="4cfae-113">POS operations aren't required in these scenarios.</span></span>

<span data-ttu-id="4cfae-114">毎回の操作では、次の要素を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cfae-114">Every operation should implement the following elements:</span></span>

- <span data-ttu-id="4cfae-115">**操作要求** – 操作要求は、**ExtensionOperationRequestBase** クラスから拡張されています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-115">**Operation request** – The operation request is extended from the **ExtensionOperationRequestBase** class.</span></span> <span data-ttu-id="4cfae-116">操作を実行するために必要なすべての入力が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-116">It contains all the input that is required in order to run the operation.</span></span>
- <span data-ttu-id="4cfae-117">**操作要求** – 操作要求は**応答**クラスから拡張されています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-117">**Operation response** – The operation response is extended from the **Response** class.</span></span> <span data-ttu-id="4cfae-118">工程の実行に基づく応答全体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-118">It contains the whole response, based on execution of the operation.</span></span>
- <span data-ttu-id="4cfae-119">**操作ファクトリ** – 操作ファクトリは、操作のためのボタンのクリックを操作ハンドラーとリンクします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-119">**Operation factory** – The operation factory links the button click for the operation with the operation handler.</span></span>
- <span data-ttu-id="4cfae-120">**操作ハンドラー** – 操作ハンドラーは、**ExtensionOperationRequestHandlerBase** クラスから拡張されています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-120">**Operation handler** – The operation handler is extended from the **ExtensionOperationRequestHandlerBase** class.</span></span> <span data-ttu-id="4cfae-121">工程のコア ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-121">It contains core logic for the operation.</span></span> <span data-ttu-id="4cfae-122">すべてのビジネス ロジックはハンドラーに記述され、操作実行後、工程応答に戻される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cfae-122">All the business logic should be written in the handler, and it should return the operation response after the operation is run.</span></span>

## <a name="create-a-pos-operation"></a><span data-ttu-id="4cfae-123">POS 操作の作成</span><span class="sxs-lookup"><span data-stu-id="4cfae-123">Create a POS operation</span></span>

<span data-ttu-id="4cfae-124">このセクションでは、簡略化された営業終了 (EOD) 処理を行うサンプル工程を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-124">This section explains how to create a sample operation that does simplified end-of-day (EOD) processing.</span></span> <span data-ttu-id="4cfae-125">この操作は、シーケンス内の標準の支払/入金の削除、金庫保管、支払/入金申告、およびシフトのクローズ操作を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-125">This operation calls the standard Tender removal, Safe drop, Tender declaration, and Close shift operations in a sequence.</span></span> <span data-ttu-id="4cfae-126">したがって、この 1 回の操作は、複数の手順を組み合わせたものです。</span><span class="sxs-lookup"><span data-stu-id="4cfae-126">Therefore, this one operation combines multiples steps.</span></span> <span data-ttu-id="4cfae-127">定義する条件に基づいて実行されます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-127">It is run based on the conditions that you define.</span></span>

> [!NOTE]
> <span data-ttu-id="4cfae-128">新しい工程を作成して独自のカスタム ロジックを実行したり、カートにアイテムを追加したり、ライン割引を適用したりするなど、既存の POS オペレーションを呼び出すことも、現在のカートを取得する、拡張プロパティを設定するなどの既存の API を呼び出すこともできます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-128">You can create a new operation and run your own custom logic, you can call existing POS operations, such as Add item to cart and Apply line discount, or you can call existing APIs, such as Get current cart and Set extension properties.</span></span>

1. <span data-ttu-id="4cfae-129">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-129">Start Microsoft Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="4cfae-130">**...\RetailSDK\POSOpen** から、**ModernPOS** ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-130">From **...\RetailSDK\POSOpen**, open the **ModernPOS** solution.</span></span>
3. <span data-ttu-id="4cfae-131">**POS.Extensions** プロジェクトで、**EODSample** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-131">Under the **POS.Extensions** project, create a folder that is named **EODSample**.</span></span>
4. <span data-ttu-id="4cfae-132">**EODSample** フォルダーで、**Operations** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-132">Under the **EODSample** folder, create a folder that is named **Operations**.</span></span>

### <a name="create-the-operation-request-class"></a><span data-ttu-id="4cfae-133">operation request クラスの作成</span><span class="sxs-lookup"><span data-stu-id="4cfae-133">Create the operation request class</span></span>

1. <span data-ttu-id="4cfae-134">**工程** フォルダで、**EndOfDayOperationRequest.ts** という typescript (.ts) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-134">In the **Operations** folder, create a typescript (.ts) file that is named **EndOfDayOperationRequest.ts**.</span></span>
2. <span data-ttu-id="4cfae-135">**EndOfDayOperationRequest.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-135">Open the **EndOfDayOperationRequest.ts** file, and add the following **import** statements to import the relevant entities and context.</span></span>

    ```typescript
    import { ExtensionOperationRequestBase } from "PosApi/Create/Operations";
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    ```

3. <span data-ttu-id="4cfae-136">**EndOfDayOperationRequest** という名のクラスを追加し、**ExtensionOperationRequestBase** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-136">Add a class that is named **EndOfDayOperationRequest**, and extend it from the **ExtensionOperationRequestBase** class.</span></span>
    <span data-ttu-id="4cfae-137">この例では、**super** メソッドでの工程 ID が **5001** に初期化されます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-137">In this example, the operation ID in the **super** method is initialized to **5001**.</span></span> <span data-ttu-id="4cfae-138">ただし、4001 からすべての操作 ID を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-138">However, you can use any operation ID starting from 4001.</span></span> <span data-ttu-id="4cfae-139">操作 ID 0 ～ 4000 が内部の Retail POS 操作に対して引当が済んでおり、2 つの操作が同じ操作 ID を持つ必要がありません。</span><span class="sxs-lookup"><span data-stu-id="4cfae-139">Operation IDs 0 through 4000 are reserved for internal Retail POS operations, and no two operations should have the same operation ID.</span></span> <span data-ttu-id="4cfae-140">さらに、顧客パラメーター フィールドは工程 ID が 4001 またはそれ以上である場合にのみ、ボタン グリッド デザイナー プロパティに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-140">Additionally, the custom parameters field appears in Button grid designer properties only if the operation ID is 4001 or higher.</span></span> <span data-ttu-id="4cfae-141">(カスタム パラメーターフィールドを使用して、小売用バックオフィスから POS 操作にパラメータを渡すことができます。)</span><span class="sxs-lookup"><span data-stu-id="4cfae-141">(You can use custom parameters field to pass parameters to the POS operation from Retail headquarters).</span></span>

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
    
### <a name="create-the-operation-response-class"></a><span data-ttu-id="4cfae-142">operation response クラスの作成</span><span class="sxs-lookup"><span data-stu-id="4cfae-142">Create the operation response class</span></span>

1. <span data-ttu-id="4cfae-143">**工程** フォルダーで、**EndOfDayOperationResponse.ts** という typescript (.ts) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-143">In the **Operations** folder, create a typescript (.ts) file that is named **EndOfDayOperationResponse.ts**.</span></span>
2. <span data-ttu-id="4cfae-144">**EndOfDayOperationResponse.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-144">Open the **EndOfDayOperationResponse.ts** file, and add the following **import** statement to import the relevant entities and context.</span></span>

    ```typescript
    import { Response } from "PosApi/Create/RequestHandlers";
    ```

3. <span data-ttu-id="4cfae-145">**EndOfDayOperationResponse** という名のクラスを追加し、**応答**クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-145">Add a class that is named **EndOfDayOperationResponse**, and extend it from the **Response** class.</span></span>

    ```typescript
    /**
     * (Sample) Operation response of executing end of day operations.
     */
    export default class EndOfDayOperationResponse extends Response { }
    ```

### <a name="create-the-operation-handler-class"></a><span data-ttu-id="4cfae-146">operation handler クラスの作成</span><span class="sxs-lookup"><span data-stu-id="4cfae-146">Create the operation handler class</span></span>

1. <span data-ttu-id="4cfae-147">**工程** フォルダーで、**EndOfDayOperationRequestHandler.ts** という typescript (.ts) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-147">In the **Operations** folder, create a typescript (.ts) file that is named **EndOfDayOperationRequestHandler.ts**.</span></span>
2. <span data-ttu-id="4cfae-148">**EndOfDayOperationRequestHandler.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-148">Open the **EndOfDayOperationRequestHandler.ts** file, and add the following **import** statements to import the relevant entities and context.</span></span>

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

3. <span data-ttu-id="4cfae-149">**EndOfDayOperationRequestHandler** という名のクラスを追加し、**ExtensionOperationRequestHandlerBase** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-149">Add a class that is named **EndOfDayOperationRequestHandler**, and extend it from the **ExtensionOperationRequestHandlerBase** class.</span></span>

    <span data-ttu-id="4cfae-150">各ハンドラーは、2 つのメソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4cfae-150">Each handler should implement two methods:</span></span>

   - <span data-ttu-id="4cfae-151">supportedRequestType</span><span class="sxs-lookup"><span data-stu-id="4cfae-151">supportedRequestType</span></span>
   - <span data-ttu-id="4cfae-152">executeAsync</span><span class="sxs-lookup"><span data-stu-id="4cfae-152">executeAsync</span></span>
   
    ```typescript
    export default class EndOfDayOperationRequestHandler<TResponse extends EndOfDayOperationResponse> extends ExtensionOperationRequestHandlerBase<TResponse> {}
    ```

4. <span data-ttu-id="4cfae-153">サポートされている要求タイプをクラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-153">Add the supported request type in the class.</span></span>

    ```typescript
    /**
     * Gets the supported request type.
     * @return {RequestType<TResponse>} The supported request type.
     */
    public supportedRequestType(): ExtensionOperationRequestType<TResponse> {
        return EndOfDayOperationRequest;
    }
    ```

5. <span data-ttu-id="4cfae-154">**executeAsync** メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-154">Implement the **executeAsync** method.</span></span>

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

    <span data-ttu-id="4cfae-155">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4cfae-155">The overall code should look like this.</span></span>

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

### <a name="create-the-operation-factory-class"></a><span data-ttu-id="4cfae-156">operation factory クラスの作成</span><span class="sxs-lookup"><span data-stu-id="4cfae-156">Create the operation factory class</span></span>

1. <span data-ttu-id="4cfae-157">**工程** フォルダで、**EndOfDayOperationRequestFactory.ts** という typescript (.ts) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-157">In the **Operations** folder, create a typescript (.ts) file that is named **EndOfDayOperationRequestFactory.ts**.</span></span>
2. <span data-ttu-id="4cfae-158">**EndOfDayOperationRequestFactory.ts** ファイルを開き、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-158">Open the **EndOfDayOperationRequestFactory.ts** file, and add the following **import** statements to import the relevant entities and context.</span></span>

    ```typescript
    import EndOfDayOperationResponse from "./EndOfDayOperationResponse";
    import EndOfDayOperationRequest from "./EndOfDayOperationRequest";
    import { ExtensionOperationRequestFactoryFunctionType, IOperationContext } from "PosApi/Create/Operations";
    import { ClientEntities } from "PosApi/Entities";
    ```

3. <span data-ttu-id="4cfae-159">操作ハンドラーおよび操作ボタンをリンクする機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-159">Add a function to link the operation handler and the operation button.</span></span>

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

    <span data-ttu-id="4cfae-160">全体的なコードは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="4cfae-160">The overall code should look like this.</span></span>

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

4. <span data-ttu-id="4cfae-161">**manifest.json** ファイルを開き、次のコードに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-161">Open the **manifest.json** file, and paste in the following code.</span></span>

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

5. <span data-ttu-id="4cfae-162">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**EODSample** で更新し、実行時に POS に拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-162">Open the **extensions.json** file under the **POS.Extensions** project, and update it with **EODSample**, so that the POS will include the extension at runtime.</span></span>

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

6. <span data-ttu-id="4cfae-163">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストでコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-163">Open the **tsconfig.json** file, and comment out the extension package folders in the exclude list.</span></span> <span data-ttu-id="4cfae-164">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-164">The POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="4cfae-165">既定では、リストに除外された拡張リスト全体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-165">By default, the list contains the whole excluded extensions list.</span></span> <span data-ttu-id="4cfae-166">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、拡張リストの拡張をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-166">To include an extension as part of the POS, you must add the name of the extension folder and comment out the extension in the extension list, as shown here.</span></span>

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

7. <span data-ttu-id="4cfae-167">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-167">Compile and rebuild the project.</span></span>

## <a name="add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters"></a><span data-ttu-id="4cfae-168">小売用バックオフィス内の POS レイアウトにカスタム操作ボタンを追加します</span><span class="sxs-lookup"><span data-stu-id="4cfae-168">Add a custom operation button to the POS layout in Retail headquarters</span></span>

1. <span data-ttu-id="4cfae-169">Retail で**小売りとコマース &gt; チャンネル設定 &gt; POS 設定 &gt; POS &gt; 工程**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-169">In Retail go to **Retail and commerce &gt; Channel setup &gt; POS setup &gt; POS &gt; Operations**.</span></span>
2. <span data-ttu-id="4cfae-170">**EOD** という工程を作成して、**5001** の工程 ID をもつようにします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-170">Create an operation that is named **EOD** and that has an operation ID of **5001**.</span></span>
3. <span data-ttu-id="4cfae-171">**小売とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS &gt; ボタン グリッド**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-171">Go to **Retail and commerce &gt; Channel setup &gt; POS setup &gt; POS &gt; Button grids**.</span></span>
4. <span data-ttu-id="4cfae-172">**'F2W2'** コードのフィルターです。</span><span class="sxs-lookup"><span data-stu-id="4cfae-172">Filter for **'F2W2'**.</span></span>
5. <span data-ttu-id="4cfae-173">**デザイナー**ボタンを選択し、次の手順にしたがってデザイナーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-173">Select the **Designer** button, and then follow the instructions to install the designer.</span></span> <span data-ttu-id="4cfae-174">資格情報を求めるメッセージが表示されたら、Retail のユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-174">If you're prompted for credentials, enter the Retail user name and password.</span></span>
6. <span data-ttu-id="4cfae-175">デザイナ領域で右クリックし、**新しい行の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-175">Right-click in the designer area, and then select **Add new row**.</span></span>
7. <span data-ttu-id="4cfae-176">新しいボタンを右クリックし、**ボタン プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-176">Right-click the new button, and then select **Button properties**.</span></span>
8. <span data-ttu-id="4cfae-177">**EOD** に **アクション**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-177">Set the **Action** property to **EOD**.</span></span> <span data-ttu-id="4cfae-178">**OK** を選択し、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4cfae-178">Then select **OK**, and close the designer.</span></span>
9. <span data-ttu-id="4cfae-179">**小売りとコマース** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-179">Go to **Retail and commerce** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
10. <span data-ttu-id="4cfae-180">**1090** を選択してから、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-180">Select **1090**, and then select **Run now**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4cfae-181">上記の手順では、デモ データを使用していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="4cfae-181">The preceding steps assume that you're using demo data.</span></span> <span data-ttu-id="4cfae-182">デモ データを使用していない場合は、カスタム構成に従ってボタンを作成して追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-182">If you aren't using demo data, create and add the button according to your custom configurations.</span></span>

## <a name="validate-your-extension"></a><span data-ttu-id="4cfae-183">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="4cfae-183">Validate your extension</span></span>

1. <span data-ttu-id="4cfae-184">F5 キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="4cfae-184">Press F5, and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="4cfae-185">トランザクション画面で、新しい **EOD** 操作ボタンを選択し、手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4cfae-185">On the transaction screen, select the new **EOD** operation button, and follow the steps.</span></span>
