---
title: 診断とトラブルシューティングの Commerce コンポーネント イベント
description: このトピックでは、Commerce 固有のコンポーネントからイベントを検索する場所について説明します。
author: aamirallaqaband
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.custom: 85493
ms.assetid: a22c9493-c000-4514-bb0d-b3cc674439d9
ms.search.region: Global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 9684f955c67100113425908bbb38972c6a672c13cc72ec2cf669c98a34922965
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758354"
---
# <a name="commerce-component-events-for-diagnostics-and-troubleshooting"></a>診断とトラブルシューティングの Commerce コンポーネント イベント

[!include [banner](../includes/banner.md)]

このトピックでは、Commerce 固有のコンポーネントからイベントを検索する場所について説明します。 診断とトラブルシューティングを有効にするには、Retail Modern POS などのセルフホスト型のコンポーネントを含むすべての Commerce コンポーネントと Commerce Scale Unit や e コマース モジュールなどのクラウド ホスト型コンポーネントは、それらのイベントにイベント ビューアー (または Retail Cloud F12 などのブラウザー開発ツール コンソール) にローカルでログします。 イベントは、Microsoft Dynamics Lifecycle Services (LCS) ログ検索エクスペリエンスにも記録されます。

## <a name="viewing-events-in-event-viewer"></a>イベント ビューアーでのイベントの表示

イベントがログされるコンピューターに対して物理的にアクセスできる場合、イベント ビューアーを使用して、Microsoft Windows を実行するコンピューター上にインストールされたコンポーネント用イベントを表示することができます。 イベント ビューアーの詳細については、TechNet の [イベント ビューアー](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)) を参照してください。 また、イベント ビューアーを使用して、ユーザーがアクセス権を持つコンピューターからリモートでイベントを表示することができます。 イベント ビューアーを使用して、リモートでイベントを表示する方法の詳細については、TechNet の [リモート コンピューターでイベント ログを使用](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766438(v=ws.11)) を参照してください。 イベント ビューアは通常、次の使用例でのトラブルシューティングに使用されます。

- 開発者トポロジまたはイベント ビューアーへのアクセスを提供するダウンロード可能な仮想ハードディスク (VHD) での開発。
- 会議室パイロットを実行していて、そのコンピューターのイベント ビューアにアクセスできるときのクライアント コンポーネント。

ただし、ほとんどの場合、特にコンピューターのイベント ビューアーへのアクセスがない場合、LCS でログ検索を使用できます。 E コマース モジュールに対しては、イベントは現在のところ、ブラウザ開発者ツール (F12キーなど) でのみ使用できます。 ログ検索については、このトピックの後半で説明します。 このセクションは、次のコンポーネントに適用されます。

- Commerce Scale Unit
- Retail Modern POS
- Retail ハードウェア ステーション

### <a name="find-commerce-specific-events-in-event-viewer"></a>イベント ビューアーで、コマース固有のイベントを検索する

コンピューターでイベント ビューアを起動するには、**開始** ボタンをクリックし、**イベント ビューア** をクリックします。

[![スタート ボタンのショートカット メニューのイベント ビューアー コマンド。](./media/launch-event-viewer.png)](./media/launch-event-viewer.png)

すべてのコマース固有イベント ログにはイベント ビューアーで次のパスを確認できます。アプリケーションおよびサービス ログ \\Microsoft\\Dynamics 以下のコマース固有のイベント ログを提供します。

- **Commerce-RetailServer** – このログには、Commerce Scale Unit コンポーネントによって記録されるイベントが含まれます。
- **Commerce-ModernPos** - このログには、Retail Modern POS によって記録されるイベントが含まれます。 これらのイベントには、TypeScript および C\# (CRT) レイヤーからのイベントが含まれます。
- **Commerce-LoggingProvider** – このログには、この記事の前半で一覧に含まれていない他のすべてのコマース コンポーネントによって記録されるイベントが含まれています。

### <a name="enable-debug-event-logs"></a>デバッグ イベント ログの有効化

現在、さまざまなコンポーネントによって記録されたイベントの一部がデバッグ イベント ログに送信されます。 これらのイベントは非常に高いレートで記録され、詳細なデバッグ シナリオでのみ有用な詳細イベントです。 イベント ビューアーでのデバッグ イベント ログを有効にするには、この手順を実行します。

- デバッグ ログを右クリックし、**ログの有効化** をクリックします。

![デバッグ ログのショートカット メニューでログ コマンドを有効にします。](./media/enable-debugging-log.png)

## <a name="viewing-events-by-using-the-f12-browser-developer-tools-console"></a>(F12) ブラウザー開発者ツール コンソールを使用してイベントを表示

Retail Cloud POS と e コマース モジュールはブラウザー ベースのコンポーネントなので、ブラウザー開発者ツール コンソールを使用してそのイベントを表示できます。 Microsoft ブラウザ開発者ツール コンソールの詳細については、[コンソールを使用してエラーとデバッグを表示する](/microsoft-edge/devtools-guide/console) を参照してください。 Retail Cloud POS または e コマース モジュールのブラウザー開発者ツールを使用するには、サポートされているバージョンのブラウザを使用する必要があります。

### <a name="view-events-in-the-browser-developer-tools-console"></a>ブラウザー開発者ツール コンソールでのイベントの表示

1. ブラウザーを起動し、Retail Cloud POS または e コマースの Web サイトに移動します。
2. F12 キーを押し、**コンソール** タブをクリックします。
3. Retail Cloud POS または e コマース Web サイトの操作を実行する際に、イベントはコンソールに記録されます。 イベント重要度でフィルター処理して、異なる重要度レベルのイベントを表示することができます。

[![ブラウザー開発者ツールのコンソール タブ。](./media/browser-console-1024x522.png)](./media/browser-console.png)

## <a name="correlating-events"></a>関連のイベント

このセクションでは、さまざまなコマース コンポーネントからイベントを関連付ける方法について説明します。

### <a name="data-flow-between-a-pos-client-and-commerce-scale-unit"></a>POS クライアントと Commerce Scale Unit 間のデータ フロー

以下の図は、販売時点管理 (POS) クライアントと Commerce Scale Unit 間のデータ フローを示しています。

#### <a name="pos-client-startup"></a>POS クライアントの起動

ユーザーが POS クライアントを起動すると、新しい AppSessionID が生成されます。 AppSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。 イベント ビューアおよびアプリ インサイトに記録したすべてのイベントはこの ID を持っています。

#### <a name="user-sign-in"></a>ユーザー サインイン

ユーザーが POS クライアントにサインインすると、新しい UserSessionID が生成されます。 UserSessionID は、POS クライアントで計測されるすべてのイベントのログを作成するために使用されます。 イベント ビューアーに記録されたすべてのユーザー イベントはこの ID を持ちます。 この ID は、ユーザーがログインしている間維持されます。 現在のユーザーがサインアウトして、新しいユーザーがログインすると、新しい UserSessionID が生成されます。

#### <a name="pos-client-calls-to-commerce-scale-unit"></a>POS クライアントによる Commerce Scale Unit への呼び出し

POS クライアントが Commerce Scale Unit を呼び出すときはいつでも、AppSessionID と UserSessionID がヘッダーとして送信されます。 次に、Commerce Scale Unit は、受信要求 (イベント ID 5000) のイベントを記録します。 このイベントには、2 つの ID と ActivityID が含まれます。 その後、ActivityID はすべての関連するイベントにも使用されます。 AppSessionID、UserSessionID、ActivityID は、Commerce Scale Unit がホストされているイベント ログで使用可能です。 LCS ログ検索でも利用できます。

#### <a name="request-activity-on-commerce-scale-unit"></a>Commerce Scale Unit での要求の活動

Commerce Scale Unit 要求の一部として記録されるすべてのイベントは、最初の受信要求イベント用に記録された初期イベントと同じ ActivityID を持ちます (イベント ID 5000)。 これらのイベントは、イベント ビューアーと LCS ログ検索の両方で利用できます。

[![POS クライアントと Commerce Scale Unit 間のデータ フロー。](./media/event-log-data-flow1-1018x1024.png)](./media/event-log-data-flow1.png)

### <a name="finding-retail-modern-pos-events-in-event-viewer"></a>イベント ビューアーでの Retail Modern POS イベントの検索

Retail Modern POS によってが記録されたすべてのイベントには、次のデータ点が含まれています。

- **AppSessionID** - アプリケーションが最初に起動されたときに生成される一意の ID。 これは記録されるすべてのイベントに含まれています。
- **UserSessionID** – ユーザーが Retail Modern POS にサインインするときに生成される固有の ID。 これはユーザーがサインインしている限り、記録されるすべてのイベントに含まれています。 新しいユーザーがサインインするとき、新しい UserSessionID が作成されます。

AppSessionID 値および UserSessionID 値は、Retail Modern POS がインストールされているマシン上のイベント ビューアーの **詳細** タブで見つけることができます。

[![イベント ビューアーの詳細タブ。](./media/correlation-1024x672.png)](./media/correlation.png)

### <a name="finding-incoming-commerce-scale-unit-request-events-in-event-viewer"></a>イベント ビューアーで、受信する Commerce Scale Unit 要求のイベントを検索

イベント ビューアで受信する Commerce Scale Unit 要求のデータを関連付けるには、最初に **Analytic** チャネルを有効にする必要があります。 分析チャネルを有効にするには、次の手順を実行します。

1. イベント ビューアーの左ウィンドウで、**Commerce RetailServer** を選択します。
2. **表示** &gt; **分析とデバッグ ログを有効にします** をクリックします。 分析チャネルの新しいノードは、**Commerce-RetailServer** ログ プロバイダーの下に表示されます。
3. **分析** ノードを右クリックし、**ログの有効化** をクリックします。

イベント ビューアーでは、受信しているすべての Commerce Scale Unit の要求がイベント 5000 として Commerce-RetailServer ソースの分析チャネルに記録されます。 これらのイベントには、前述した AppSessionID と UserSessionID もあります。 すべてのイベントには、同じ要求のログに記録されたイベントごとに、固有の ActivityID も用意されています。

## <a name="using-lcs-log-search"></a>LCS ログ検索の使用

LCS ログ検索で、1 つのポータルからすべてのコンポーネントのデータを表示できます。 イベントは、(Commerce Scale Unit などの) クラウドでホストされたコンポーネントと (Retail Modern POS および Retail Hardware Station などの) 店舗内コンポーネントの両方からアクセスすることができます。 すべてのクラウドホストおよびストア内コンポーネントからのイベント データは、索引付けされ検索可能になる LCS ログ検索に流れます。 データは通常、記録されてから 5 分以内に利用可能です。 POS クライアントおよび Retail Hardware Station では、すべてのイベントが永続ストレージにローカルでキュー格納され、キューがいっぱいになった後にバッチでアップロードされます。 この動作により、ネットワーク トラフィックを最適化できます。  また、インターネット接続がない場合でもイベントを保存することができます。 接続が回復した後、すべての保留中のイベントがアップロードされます。

LCS ログ検索は、HA 運用トポロジに使用できます。 次のコマースのコンポーネントに使用することができます。

- Retail Modern POS
- Retail Cloud POS
- Commerce Scale Unit (Retail Cloud Scale Unit で実行中)

LCS ログ検索に、次のコマース コンポーネントからのログは **含まれません**。

- コマース レイアウト デザイナー
- コマース受領書デザイナー
- Retail Modern POS のセルフ サービス インストーラー
- 小売ハードウェア ステーション用のセルフ サービス インストーラー
- Commerce Scale Unit (Retail Store Scale Unit で実行中)
- Retail ハードウェア ステーション

### <a name="access-lcs-log-search"></a>LCS ログ検索にアクセス

LCS ログ検索にアクセスするには、次の手順を実行します。

1. [Lifecycle Services](https://lcs.dynamics.com/) に移動します。
2. プロジェクトに関連付けられている資格情報を使用してログインします。
3. プロジェクト ページで、正しいプロジェクトを選択します。
4. **プロジェクトの詳細** ページで、正しい環境を選択します。
5. **環境の詳細** ページで、**環境の監視** をクリックします。
6. **環境の監視** ページで、**未加工ログの表示** をクリックします。
7. **ログ検索** ページで、次のいずれかのクエリを選択します。

    - **コマース クライアント イベント** クエリには、Retail Modern POS、Retail Cloud POS、および Commerce Scale Unit (Retail Cloud Scale Unit で実行中) からのイベントが含まれます
    - **すべてのログ** クエリには、Commerce Scale Unit、Commerce Data Exchange、および Commerce Data Exchange: リアルタイム サービスからのデータが含まれます

以下の条件でフィルター処理してクエリを調整することができます。

- 開始および終了日時 (協定世界時 \[UTC\])
- デバイス ID
- POS ユーザー
- POS アプリケーション セッション ID
- POS ユーザー セッション ID
- 重大度

![環境監視ページの検索結果。](./media/log-search-results.png)

### <a name="e-commerce-events"></a>E コマース イベント

次のイベントは、e コマース Web サイトによって記録され、トラブルシューティングに直接ブラウザーで、または分析、実験、またはその他の目的でパートナー拡張機能を使用してプログラムで処理できます。

### <a name="button-and-link-clicks"></a>ボタンとリンクのクリック

ボタンとリンクのクリックにより、E コマース Web サイト上の次のタイプの要素がテレメトリイベントとして記録されます。

- 表題
  - ナビゲーション階層
  - カート アイコン
  - サインイン
  - 検索アイコン
  - Wishlist アイコン
- コンテンツ ブロック アクション リンク (これは、マーケティング コンテンツ用のヒーロー、タイル、およびフィーチャー の内容を表します)
- ビデオ プレーヤー
- 製品カード
- フッター リンク
- 階層リンク
- 広告バナー
- カートに追加ボタン
- チェックアウト ボタン
- 注文する ボタン

**クリック** アクションのスキーマは次のとおりです。

```json
Click
IPayLoad = {
        contentCategory: Name of element clicked on,
        contentAction:  {
            pgname: Name of page,
            mname: name of module,
            etext: Text of element clicked on,
            recid: Product ID if a product was clicked on,
            etype: ‘click’,
        }
    };
```

### <a name="page-views"></a>ページ ビュー

ページ ビューの各操作について、ページ ビュー イベントがログに記録されます。

**PageView** アクションのスキーマは次のとおりです。

```json
PageView
IPageViewInfo = {
    title;
}
```

### <a name="cart-operations"></a>カートの操作

次の **カート** 関連のイベントがログに記録されます。

- カートに品目を追加する。
- カートの品目を更新する。
- カートから品目を削除する。
- 清算する。
- 製品ページ ビュー。

**カート** イベントのスキーマは次のとおりです。

```json
/***
 * Defines the telemetry properties to track for a Cart object
 * @property products       {IProductInfo[]}    - Array of product information
 * @property orderId        {string}            - ID for the order
 * @property cartId         {string}            - ID for the current cart object
 * @property cartVersion    {string}            - Version number for the current cart object
 */
export interface ICartInfo {
    products: IProductInfo[];
    orderId: string;
    cartId: string;
    cartVersion: string;
}
```

### <a name="purchase"></a>購買

注文が送信されると、購入イベントがログに記録されます。 **購買** イベントのスキーマは次のとおりです。

```json
/***
 * Defines the telemetry properties to track for a Purchase event
 * @property id            {string}         - Transaction ID
 * @property affiliation   {string}         - Origin of this transaction (e.g. Online Store)
 * @property revenue       {number}         - Revenue from this transaction
 * @property tax           {number}         - Tax amount
 * @property shippingCost  {number}         - Shipping cost
 * @property products      {IProductInfo[]} - List of products in this transaction
 */
export interface IProductTransaction {
    id: string;
    affiliation?: string;
    revenue?: number;
    tax?: number;
    shippingCost?: number;
    products?: IProductInfo[];
}
```

### <a name="product-details"></a>製品の詳細

製品の詳細は、**カート** および **購買** 操作に記録されます。 **製品** の詳細に関するスキーマは次のとおりです。

```json
/***
 * Defines the telemetry properties to track for a Product object
 * @property productChannelId       {string}   - Product channel ID
 * @property productChannelName     {string}   - Product channel name
 * @property productCategoryId      {string}   - Product category ID
 * @property productCategoryName    {string}   - Product category name
 * @property productId              {string}   - Product ID
 * @property productName            {string}   - Product name
 * @property productSku             {string}   - Product SKU
 * @property productPrice           {string}   - Product price
 * @property productQuantity        {string}   - Product quantity
 * @property productCurrency        {string}   - Product currency code
 */
export interface IProductInfo {
    productChannelId: string;
    productChannelName: string;
    productCategoryId: string;
    productCategoryName: string;
    productId: string;
    productName: string;
    productSku: string;
    productPrice: string;
    productQuantity: string;
    productCurrency: string;
}
```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]