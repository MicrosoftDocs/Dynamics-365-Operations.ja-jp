---
title: 注文属性の定義と設定をする
description: このトピックでは、コマース バックオフィス、POS、および CRT でオーダーの属性値を直接編集および設定する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-24
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: dae44f25429bfec12cdb06cd04a12af47e075851
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004662"
---
# <a name="define-and-set-order-attributes"></a>注文属性の定義および設定

[!include [banner](../../includes/banner.md)]

以前は、属性フレームワークは、オンライン注文でのみ属性をサポートしていました。 ただし、フレームワークが拡張されたため、現金売りトランザクション、顧客の注文、およびコール センター注文の属性がサポートされるようになりました。 この機能拡張により、バックオフィス、販売時点管理 (POS)、および Commerce runtime (CRT) でオーダーの属性値を直接編集および設定できます。 

バックオフィスには、属性の値を編集したり更新するためのページが含まれています。 たがって、コール センター注文の値は、バックオフィスで設定できます。 POS で使用できる属性値を設定するためのユーザー インターフェイス (UI) がありませんが、新しい UI を追加する POS を拡張することができます。 UI を必要とせず、ビジネス ロジックを追加するだけの場合、ビジネス ロジックを CRT に直接追加できます。 バックオフィス コンフィギュレーションを使用することにより、新しい属性を作成することができます。 データベースの変更は必要ありません。 以前は、バックオフィスとチャンネル データベースで新しいテーブルを作成するには、それらのテーブルを変更する必要がありました。

## <a name="why-and-when-you-should-order-attributes"></a>注文属性が必要な理由および場合

現金売りトランザクション、顧客注文、またはコールセンターの注文に新しいフィールドを追加し、POS またはバックオフィスで情報をキャプチャする場合は、注文属性を使用します。 以前は、現金売りトランザクション (トランザクション ヘッダーまたは行) または POS の顧客注文に新しいフィールドを追加するには、バックオフィスとチャネル データベースで新しい拡張テーブルを作成し、CRT および POS コードにインライン変更を加えて各種画面および操作を処理する必要がありました。 また、チャネル データベースとバックオフィス間でデータを同期するように Commerce Data Exchange を構成する必要がありました。 ただし、注文属性はコンフィギュレーションを通してこれらすべてのアクションを完了できます。 コードを記述またはカスタム拡張機能テーブルを作成する必要はありませんが、主要なビジネス ロジックおよび POS UI を作成する必要があります。

この最初のバージョンは **String** 属性タイプのみをサポートしますが、将来のバージョンは他の属性タイプをサポートします。 データをマスター テーブルから取得し、そのデータに X++ の複雑な検索ロジックとコア ビジネス ロジックが必要な場合は、拡張プロパティを使用する必要があります。

> [!NOTE]
> 顧客注文および現金店頭払いのトランザクションでのみ属性がサポートされます。他のトランザクション タイプはサポートされていません。

## <a name="define-attribute-types"></a>属性タイプを定義

最初に、属性タイプを定義し、それに有効な範囲を割り当てる必要があります。

1. **製品情報管理** > **設定** > **カテゴリと属性** > **属性タイプ**の順に移動します。
2. **属性タイプ**ページで、**新規**を選択し、新しい属性タイプを追加します。
3. 階層タイプ名を入力します。
4. **一般**クイック タブの、**タイプ**フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。
5. 属性タイプが**少数点**または**整数**の場合、測定単位を選択します。
6. 属性の型が**テキスト**である場合は、それを固定値の一覧を定義できます。 **固定リスト** チェック ボックスをオンにし、**値** クイック タブで、値の一覧を入力します。
7. 属性タイプに有効な値の範囲を定義するには、**値の範囲** チェック ボックスをオンにします。 次に、**範囲** クイックタブで、値の有効範囲を入力します。

## <a name="define-the-attributes"></a>属性の定義 

次に、属性を定義する必要があります。 定義する各属性に対して、これらの手順に従います。

1. **製品情報管理** > **設定** > **カテゴリと属性** > **属性**の順に移動します。
2. **属性**ページで、**新規**を選択し、新しい属性を追加します。
3. 属性の名前、フレンドリ名、および説明を入力します。 また、属性にユーザーを表示する必要があるヘルプ テキストを入力します。
4. **属性タイプ** フィールドで、属性に割り当てる属性タイプを選択します。
5. 属性タイプに応じて、**既定値** フィールドに、属性がチャネルに割り当てられたときに既定で表示される値または値の範囲を入力します。
6. **翻訳** を選択します。 その後、**テキストの翻訳** ページで、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。

## <a name="define-attribute-groups"></a>属性グループの定義

1. **製品情報管理** > **設定** > **カテゴリと属性** > **属性グループ**の順に移動します。
2. **属性グループ**ページで、**新規**を選択し、新しい属性グループを追加します。
3. 属性グループ名を入力します。 その後、**全般** クイックタブで、属性グループのフレンドリ名、説明、およびヘルプ テキストを入力します。
4. **属性**クイック タブで、**追加**を選択して、属性グループに属性を追加します。 **既定値**フィールドでは、選択した属性の既定値を入力できます。
5. **翻訳** を選択します。 その後、**テキストの翻訳** ページで、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。

## <a name="link-the-attribute-group-to-the-channel"></a>属性グループのチャネルへのリンク

1. **Retail とコマース** > **チャネル** > **店舗** > **すべての店舗**の順に移動します。
2. **チャネル** ページの属性をリンクする必要があるチャネルを選択します。
3. **設定**タブで、**属性グループ**の**販売注文属性**を選択します。
4. **販売注文属性グループ**ページで、**新規**を選択し、属性グループをチャネルにリンクします。
5. **名前**フィールドで属性グループを選択してチャネルにリンクします。
6. **属性の適用先**フィールドで、次のいずれかのオプションを選択します。

    - **ヘッダー** – 属性は、トランザクション ヘッダーにのみ適用されます。
    - **明細行** – 属性は、トランザクション明細行にのみ適用されます。
    - **既定** - 属性は、トランザクション ヘッダーとトランザクション明細行の両方に適用されます。

7. **保存** を選択します。

## <a name="run-the-distribution-jobs"></a>配送ジョブを実行

1. **Retail とコマース** > **Retail とコマース IT** > **配送スケジュール**の順に移動します。
2. **製品 (1040)** を選択し、アクション ペインで **今すぐ実行** を選択します。 メッセージが表示されたら、**はい** を選択します。 このステップは、新しい属性、属性タイプ、または属性グループを追加した場合にのみ必要です。
3. **チャネル コンフィギュレーション ジョブ (1070)** を選択し、アクション ペインで **今すぐ実行** を選択します。 メッセージが表示されたら、**はい** を選択します。

## <a name="show-order-attributes-in-the-pos-transaction-screen-using-the-attribute-control-this-feature-is-available-in-version-813-and-later"></a>属性コントロールを使用して POS トランザクション画面に注文属性を表示します (この機能はバージョン 8.1.3 以降で使用できます)。

### <a name="headquarters"></a>バックオフィス

1. **Retail とコマース > チャネル設定 > POS 設定 > POS > 画面レイアウト**の順に選択します。
2. 画面レイアウトページで、**新規** をクリックして新しい画面レイアウトを作成するか、既存の画面レイアウトを選択します。
3. スクリーン レイアウトの名前と ID を入力します。
4. **レイアウト サイズ**クイック タブで、**追加**ボタン選択して、POS の新しいレイアウト サイズを追加します。
5. **名前**フィールドで POS 画面の解像度を選択します。
6. **レイアウト サイズ**クイック タブで、**レイアウト デザイナー**ボタンをクリックします。
7. プロンプトが表示されたら、**はい**を選択して、**インストール/実行**ボタンを使用してデザイナー ホストをダウンロードおよびインストールします。
8. 入力を求めるメッセージが表示されたら、Microsoft Dynamics 365 のユーザー名とパスワードを入力して、デザイナーを起動します。
9. デザイナーが開始されたら、属性パネルを画面レイアウト デザイナー内の任意の場所にドラッグし、画面の幅に従ってサイズを調整します。
10. 完了したら、**OK** を選択して、変更を保存します。
11. 右上隅の **閉じる** ボタン (X) をクリックし、画面レイアウト デザイナーを閉じます。 メッセージが表示されたら、**はい** を選択して、変更を保存します。
12. **Retail とコマース > Retail とコマース IT > 配送スケジュール**の順に移動します。
13. レジスター ジョブ (1090) を選択し、アクション ペインで **今すぐ実行** を選択します。 メッセージが表示されたら、はい を選択します。

### <a name="pos"></a>POS

1. POS を起動し、任意の品目をトランザクションに追加します。 ヘッダーと明細行の両方のコンフィギュレーション済の属性と共に、トランザクション画面に属性パネルが表示されます。
2. 属性パネルで **編集** アイコンをクリックして、属性の値を更新します。
3. 属性パネルでヘッダーまたは明細行タブをクリックして、ヘッダーまたは明細行の属性パネルを表示します。 
4. 明細行の属性は、トランザクションで選択した明細行に基づいて自動的に更新されます。

## <a name="set-attribute-values-for-call-center-orders"></a>コール センターの注文の属性値を設定

チャンネルの注文属性を構成した後、**顧客サービス**または**すべての販売注文**、およびコール センターの新しい注文を作成します。

1. 顧客注文の作成後または作成中に、トランザクション ヘッダーの属性値を設定する場合は、アクション ウィンドウで、**コマース** タブに移動し、**小売属性**を選択します。
2. **販売注文属性値**ページで、属性値を設定することができます。 このページの属性のリストは、チャネル用にコンフィギュレーションした属性グループに基づいています。
3. 行レベルで属性値を設定するには、**販売注文** ページで **行** ビューを選択し、属性値を設定する行を選択します。 **販売注文明細行グループ**で、**Retail とコマース** > **属性**を選択します。
4. 値を設定するすべての販売明細行に対して手順 3 を繰り返します。

## <a name="view-the-attributes-values-for-cash-and-carry-transactions-in-headquarters"></a>バックオフィスでの現金売りトランザクションの属性値の表示

配送ジョブを実行し、バックオフィスに現金売りトランザクションを収集した後、トランザクションの属性値を表示できます。 POS は、注文の属性を表示するための UI を提供しません。 したがって、注文の属性値を表示するには、POS を拡張する必要があります。

1. **Retail とコマース** > **照会およびレポート** > **店舗のトランザクション**の順に移動します。
2. トランザクション ヘッダー属性を表示するには、アクション ウィンドウで**属性**を選択します。
3. トランザクション ヘッダー行の属性を表示するには、アクション ウィンドウで **トランザクション** > **販売トランザクション** を選択します。
4. **販売トランザクション** ページで、すべての明細行を選択し、アクション ウィンドウで、**属性**を選択して、明細行の属性を表示します。

> [!NOTE]
> あなたの属性グループの一部として構成され、チャンネルにリンクされている属性のみ、バックオフィス UI に表示されます。

## <a name="extend-attributes-to-add-business-logic-in-crt"></a>CRT でビジネス ロジックを追加するには、属性を拡張します。

Retail SDK に追加された新しいサンプルでは、CRT の注文属性のビジネス ロジックを追加します。 この例には、ビジネス ロジックのコードのみが含まれています。 属性に対する読み取りおよび書き込み処理は自動化されているため、属性を保存したり読み取ったりする方法は示しません。

このサンプルでは、次のシナリオを実装しています。カートを中断するときはいつでも、属性値を設定します。 カートを再開するとき、その値を消去します。 事前トリガーが **SuspendCartRequest** に追加され、ビジネス ロジックが記述されました。 CRT で任意のトリガーを拡張または任意の要求をオーバーライドして、シナリオに基づきロジックをセットすることができます。

完全なサンプル コードは Retail SDK\\SampleExtensions\\CommerceRuntime\\Extensions.TransactionAttributesSample の Retail SDK で見つけることができます。

- 新しい C# ポータブル クラス ライブラリ プロジェクトを作成し、次のコードを貼り付けます。

    ```C#
    public class CustomSuspendCartTrigger : IRequestTrigger
    {
        // summary
        // Gets the list of supported request types.
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new [ ] { typeof(SuspendCartRequest)};
            }
         }

        // Pre-trigger code.

        // summary
        // param name="request" The request param
        public void OnExecuting(Request request)
        {
            ThrowIf.Null(request, "request");
            Type requestedType = request.GetType();
            if (requestedType == typeof(SuspendCartRequest))
            {
                SuspendCartRequest suspendCartRequest = request as SuspendCartRequest;
                // Get the cart.
                var getCartServiceRequest = new GetCartServiceRequest(
                    new CartSearchCriteria(suspendCartRequest.CartId), QueryResultSettings.SingleRecord);
                Cart cart = request.RequestContext.Execute<GetCartServiceResponse>(getCartServiceRequest).Carts.Single();
                // Update the transaction header attribute for customer order.
                if (cart.CartType == CartType.CustomerOrder)
                {
                    bool cartUpdated = CustomCartHelper.CreateUpdateTransactionHeaderAttribute(
                        cart, reserveNow: false, updateAttribute: true);
                    if (cartUpdated)
                    {
                        // Save the cart after updating the header attribute.
                        var saveCartRequest = new SaveCartRequest(cart);
                        request.RequestContext.Execute<SaveCartResponse>(saveCartRequest);
                    } 
                } 
            } 
        }

        // Post-trigger code.

        // summary
        // param name="request" The request param
        // param name="response" The response param
        public void OnExecuted(Request request, Response response)
        {
        }
    ```

## <a name="extend-attributes-to-do-some-business-logic-in-the-pos"></a>POS でビジネス ロジックを行うには、属性を拡張します。

> [!NOTE]
> バージョン 8.1.2 以降でアプリケーションを実行している場合にのみ、次の変更が必要です。 8.1.3 以降は、新しい属性パネルを使用して、POS で属性の値を設定または更新できます。 このコントロールでは、POS で属性値を設定するために追加のコードを記述したり、UI を作成したりする必要がなくなりました。 属性値を設定または更新するための属性コントロール UI が追加されました。 詳細については、このドキュメントの**属性コントロールを使用して POS トランザクション画面で注文属性を表示する**セクションを参照してください。

Retail SDK に追加された新しいサンプルでは、POS の注文属性のビジネス ロジックを設定します。 この例には、ビジネス ロジックのコードのみが含まれています。 属性に対する読み取りおよび書き込み処理は自動化されているため、属性の値を保存したり読み取ったりする方法は示しません。 属性の値は、シナリオに基づき、CRT または POS のいずれかで設定することができます。 値が顧客の入力に基づいている場合、POS クライアントで設定します。 一部のビジネス ロジックが含まれている場合は、CRT で値を設定します。

このサンプルでは、次のシナリオを実装しています。企業間 (B2B) 注文を作成し、 顧客からのフィードバックに基づいて B2B 属性の値を設定する場合 (**Yes** または **No**)。 **PreEndTransactionTrigger** は値を設定するために POS で拡張されました。 必要に応じて任意の POS トリガーを拡張、または要求をオーバーライドすることができます。

完全なサンプル コードは Retail SDK\\POS\\Extensions\\B2BSample の Retail SDK で見つけることができます。

> [!NOTE]
> そのコードに属性と属性値を設定または追加した場合でも、構成された属性のみバックオフィス UI に表示されます。 属性が、チャンネルにリンクされている属性グループに属さない場合は、バックオフィス UI に反映されません。

1. Retail SDK から **ModernPOS.sln\\CloudPos.sln** を開きます。
2. Retail SDK で、**POS.Extension** プロジェクトに新しい拡張フォルダーを作成します。
3. 新しい拡張フォルダーに、新しい **manifest.json** ファイルを追加します。
4. 次のコードに貼り付けます。

    ```typescript
    {
        "$schema": "..manifestSchema.json",
        "name": "Pos_Extensibility_B2BSample",
        "publisher": "Microsoft",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
        "resources": {
        "supportedUICultures": [ "en-US" ],
        "fallbackUICulture": "en-US",
        "culturesDirectoryPath": "Resources/Strings",
        "stringResourcesFileName": "resources.resjson" 
    },
    "extend": {
        "triggers": [
        {
            "triggerType": "PreEndTransaction",
            "modulePath": "TriggerHandlers/PreEndTransactionTrigger"
        }  
        ]
    } } }
    ```
5.  新しい TypeScript ファイルを作成して **PreEndTransactionTrigger** を実装し、次のコードを追加します。

    ```typescript
    /**
     * Executes the trigger functionality.
     * @param {Triggers.IPreEndTransactionTriggerOptions} options The options provided to the trigger.
     */

    public execute(options: Triggers.IPreEndTransactionTriggerOptions): Promise<ClientEntities.ICancelable {
        console.log("Executing PreEndTransactionTrigger with options " + JSON.stringify(options) + ".");
        let currentCart: ProxyEntities.Cart;
        return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())
    then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):
        Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {
            currentCart = getCurrentCartClientResponse.data.result;
            // Gets the current customer.
            let result: Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>>;
            if (!ObjectExtensions.isNullOrUndefined(currentCart) && !ObjectExtensions.isNullOrUndefined(currentCart.CustomerId)) {
                let getCurrentCustomerClientRequest: GetCustomerClientRequest<GetCustomerClientResponse =
                    new GetCustomerClientRequest(currentCart.CustomerId);
                result = this.context.runtime.executeAsync<GetCustomerClientResponse>(getCurrentCustomerClientRequest);
            } else {
                result = Promise.resolve({ canceled: false, data: new GetCustomerClientResponse(null) });
            }
            return result;
        })
     .then((getCurrentCustomerClientResponse: ClientEntities.ICancelableDataResult<GetCustomerClientResponse>):
        Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>> => {
        let currentCustomer: ProxyEntities.Customer = getCurrentCustomerClientResponse.data.result;
        // If the cart is a customer order with a B2B customer, then we display a dialog to determine if the order should be B2B.
        let result: Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>>;
        if (!ObjectExtensions.isNullOrUndefined(currentCart)
            && currentCart.CustomerOrderModeValue === ProxyEntities.CustomerOrderMode.CustomerOrderCreateOrEdit
            && !ObjectExtensions.isNullOrUndefined(currentCustomer)
            && this.isCustomerB2B(currentCustomer)) {
            let yesButton: ClientEntities.Dialogs.IDialogResultButton = {
                id: PreEndTransactionTrigger.DIALOG_YES_BUTTON_ID,
                label: this.context.resources.getString("string_0"),  "Yes"
                result: PreEndTransactionTrigger.DIALOG_RESULT_YES
            };
            let noButton: ClientEntities.Dialogs.IDialogResultButton = {
                id: PreEndTransactionTrigger.DIALOG_NO_BUTTON_ID,
                label: this.context.resources.getString("string_1"),  "No"
                result: PreEndTransactionTrigger.DIALOG_RESULT_NO
            };
            let showMessageDialogClientRequestOptions: ClientEntities.Dialogs.IMessageDialogOptions = {
                title: this.context.resources.getString("string_2"),  "B2B Order"
                subTitle: StringExtensions.EMPTY,
                message: this.context.resources.getString("string_3"),  "Do you want to mark this order as a B2B order?"
                button1: yesButton,
                button2: noButton
            };
            let showMessageDialogClientRequest: ShowMessageDialogClientRequest<ShowMessageDialogClientResponse> =
                new ShowMessageDialogClientRequest(showMessageDialogClientRequestOptions);
            result = this.context.runtime.executeAsync<ShowMessageDialogClientResponse>(showMessageDialogClientRequest);
        } else {
            result = Promise.resolve({ canceled: false, data: new ShowMessageDialogClientResponse(null) });
        }
        return result;
    })
    .then((showMessageDialogClientResponse: ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse):
        Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>> => {
        // Save the B2B attribute value depending on the dialog result.
        let messageDialogResult: ClientEntities.Dialogs.IMessageDialogResult = showMessageDialogClientResponse.data.result;
        let result: Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>>;
        if (!ObjectExtensions.isNullOrUndefined(messageDialogResult)) {
            let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();
            attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;
            attributeValue.TextValue = messageDialogResult.dialogResult === PreEndTransactionTrigger.DIALOG_RESULT_YES?
            PreEndTransactionTrigger.B2B_ATTRIBUTE_VALUE_TRUE : PreEndTransactionTrigger.B2B_ATTRIBUTE_VALUE_FALSE;
            let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];
            let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =
            new SaveAttributesOnCartClientRequest(attributeValues);
            result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
        } else {
            result = Promise.resolve({ canceled: false, data: new SaveAttributesOnCartClientResponse(null) });
        }
        return result;
    });
    }
    /**
    * Returns whether or not the given customer is a B2B customer.
    * @param {ProxyEntities.Customer} customer The customer.
    * @returns {boolean} Whether or not the given customer is a B2B customer.
    */
    private isCustomerB2B(customer: ProxyEntities.Customer): boolean {
        let isB2B: boolean = false;
        if (!ObjectExtensions.isNullOrUndefined(customer.Attributes)) {
            for (let i: number = 0; i < customer.Attributes.length; i++) {
                let currentAttribute: ProxyEntities.CustomerAttribute = customer.Attributes[i];
                if (currentAttribute.Name === PreEndTransactionTrigger.B2B_CUSTOMER_ATTRIBUTE_NAME) {
                    if (!ObjectExtensions.isNullOrUndefined(currentAttribute.AttributeValue.BooleanValue)) {
                        isB2B = currentAttribute.AttributeValue.BooleanValue;
                    }
                    break;
                }
            }  
        }
        return isB2B;
    } } } }
    ```
