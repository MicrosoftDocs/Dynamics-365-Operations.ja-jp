---
title: 実験の設定
description: この記事では、サードパーティ サービスで実験を設定する方法について説明します。
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946169"
---
# <a name="set-up-an-experiment"></a>実験の設定

[仮説を定義し、使用する成功メトリックスを決定](experimentation-identify.md) したら、サードパーティ サービスで実験を設定する必要があります。 次の図は、Dynamics 365 Commerce の電子商取引 web サイトでの実験の設定と実行に関連するすべての手順を示しています。 追加の手順については、個別の記事で説明します。

[![実験ユーザー体験 - 設定。](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>サードパーティ サービスで実験を設定する
この時点で、サードパーティ サービスを選択して実験を実行および監視し、実験コネクタを設定する必要があります。 これらの前提条件は、[Dynamics 365 Commerce での実験](experimentation-overview.md) で一覧表示されています。

サードパーティ サービスで実験を作成するために必要な手順に従います。 コネクタが適切に構成されている場合、サードパーティ サービスで設定した実験の完全なリストが、約 5 分以内にサイト ビルダーに表示されます。

## <a name="set-up-your-success-metrics"></a>成功メトリックスの設定
各実験には、バリエーションの影響を測定し、仮説を検証するためのメトリックスが必要です。 次の手順に従って、Dynamics 365 Commerce からの実際のテレメトリ イベントを使用して、サードパーティ サービスのメトリックスの計算を有効にします。

すぐに利用できるモジュールの成功メトリックスを設定するには、次の手順を実行します。

1. Commerce のサイト ビルダーで、左側のナビゲーション ウィンドウの **ページ** を選択して、メトリックスを収集するページを選択します。 
1. 追跡するページまたはモジュールの右側のプロパティ ウィンドウで、**追跡するイベント ID** セクションに移動します。
1. **表示** を選択します。 すべてのクリック イベント ID の一覧が表示されます。 追跡するイベントをコピーし、そのイベント キーをサードパーティ サービスの指定された場所に貼り付けます。 複数のイベントが必要な場合は、一度に 1 つのキーをコピーします。 
1. ページ ビューの場合は、サイト ビルダーのページ名の SHA-256 ハッシュ値に `.PageView` を追加して使用します。 たとえば、`Homepage.PageView` のイベント ID は `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9` です。
1. 必要に応じて、サードパーティ サービスで、メトリックスを追跡するためのその他の手順を実行します。

カスタム モジュールのクリックの場合は、次の手順に従ってクリック イベントをインストルメント化します:

1. 次の関数を使用して、モジュールの **TelemetryContent** オブジェクトを準備します。 この関数は、ページ名、モジュール名、SDK によって指定された既定のテレメトリ オブジェクトを入力として受け取ります。

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    以下は、例を示します: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. キャプチャする必要がある情報を含むペイロード データを作成します。 ボタンおよびその他のスタティック コントロールの場合は、"今すぐ購入" や "検索" などの **etext** を含めることができます。 また、製品カードをクリックなどのクリックを伴うコンポーネントの場合は、製品のレコード ID または製品 ID である **recid** を送信できます。

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    スタティック コントロールの例として、次に示すようにボタン テキスト文字列を渡します:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    製品のクリックの例として、次に示すように製品 recordId を渡します:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. **OnClick** 関数を呼び出して、イベントを登録します。

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    以下は、例を示します:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>前のステップ
[仮説を識別して実験のメトリックスを決定する](experimentation-identify.md) 


## <a name="next-step"></a>次のステップ
[実験を接続して編集する](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
