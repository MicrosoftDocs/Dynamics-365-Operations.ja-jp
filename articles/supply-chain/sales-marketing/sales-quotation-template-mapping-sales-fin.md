---
title: 販売見積のヘッダーおよび明細行の Sales から Supply Chain Management への直接同期
description: このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に販売見積ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: a39b6b5fff88a02b71d81fd870e8c92ab055bc4d257e14c9b84cac0deac2c5c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771326"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>販売見積のヘッダーおよび明細行の Sales から Supply Chain Management への直接同期

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Sales から Dynamics 365 Supply Chain Management に販売見積ヘッダーおよび明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Microsoft Dataverse for Apps へデータを統合](/powerapps/administrator/data-integrator) をよく理解しておく必要があります。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー。](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>テンプレートおよびタスク

Sales から Supply Chain Management への販売見積ヘッダーと明細行の直接同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合における テンプレートの名前:** 販売見積 (Sales から Supply Chain Management)- 直接
- **データ統合プロジェクトのタスク名:**

    - QuoteHeader
    - QuoteLine

販売見積ヘッダーと明細行を同期させるには、次の同期タスクが必要です。

- 製品 (Supply Chain Management から Sales) - 直接
- 勘定 (Sales から Supply Chain Management) - ダイレクト (使用する場合)
- 顧客への連絡先 (Sales から Supply Chain Management) - ダイレクト (使用する場合)

## <a name="entity-set"></a>エンティティ セット

| 販売注文        | サプライ チェーン マネジメント     |
|--------------|----------------------------|
| 引用       | Dataverse 販売見積もりのヘッダー |
| QuoteDetails | Dataverse 販売見積明細行  |

## <a name="entity-flow"></a>エンティティのフロー

販売見積が Sales で作成され、Supply Chain Management に同期されます。

Sales からの販売見積は、次の条件が満たされた場合にのみに同期されます。

- 販売見積のすべての見積は、外部から管理されます。
- **有効化見積** をクリックした後、販売見積は有効です。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

**外部で管理された製品のみ** フィールドが **見積** エンティティに追加され、販売見積が完全に外部管理製品から構成されているかどうか一貫して追跡されます。 販売見積に外部で管理された製品のみがある場合、製品は Supply Chain Management で管理されます。 この動作は、Supply Chain Management で不明な製品を含む販売見積明細行を同期させないことを保証するのに役立ちます。

販売見積書のすべての見積製品は、販売見積書ヘッダーからの **外部で管理される製品のみ** 情報で更新されます。 この情報は、**QuoteDetails** エンティティの **外部で管理される製品のみの見積** フィールドに記載されています。

割引は、見積製品に追加することができ、Supply Chain Management と同期されます。 **割引**、**請求**、および **税** フィールドは、ヘッダーで Supply Chain Management の設定によって制御されます。 今現在、この設定では、統合マッピングはサポートされていません。 現在の設計では、**価格**、**割引**、**請求金額**、および **税** の各フィールドは、FSupply Chain Management によって維持され、処理されます。

Sales では、値が Supply Chain Management に同期されていないため、このソリューションでは次のフィールドを読み取り専用にします。

- 販売見積ヘッダーの読み取り専用フィールド: **割引率**、**割引**、**貨物量**
- 見積製品の読み取り専用フィールド: **税**

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

販売見積が同期される前に、以下の設定を更新することが重要です。

### <a name="setup-in-sales"></a>Sales での設定

- Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可が設定されていることを確認します。 デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。 チームがデータ統合からプロジェクトを実行するときにチームに管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。

    チームのアクセス許可を設定するには、**設定** &gt; **セキュリティ** &gt; **チーム** の順に進み、該当するチームを選択します。 **ロールの管理** を選択して、**システム管理者** などの必要なアクセス許可を持つロールを選択します。

- **設定** &gt; **管理** &gt; **システム設定** &gt; **Sales** へと順に進み、次の設定が使用されていることを確認してください。

    - **システム プライジング計算システムの使用** オプションが、**はい** に設定されている。
    - **割引の計算方法** フィールドが、**明細行品目** に設定されている。

### <a name="setup-in-the-data-integration-project"></a>データ統合プロジェクトでの設定

#### <a name="quoteheader"></a>QuoteHeader

- 必要なマッピングが **Shipto\_country** から **DeliveryAddressCountryRegionISOCode** に存在することを確認します。 値マップでは、値が空白の場合に使用される既定値を定義できます。 左側を空白のままにして、右側を希望する国または地域に設定します。 これにより、国または地域国内の注文を入力する必要はありません。

    テンプレートの値は、複数の国または地域がマップされている値マップで、空白値は **米国** の値と等しくなります。

#### <a name="quoteline"></a>QuoteLine

- Supply Chain Management の **SalesUnitSymbol** に必要な値マップが存在することを確認して下さい。
- Sales に必要な単位が定義されていることを確認します。

    値マップを持つテンプレート値が **oumid.name** から **SalesUnitSymbol** まで定義されています。

- オプション： 次のマッピングを追加して、顧客または製品からの既定の情報がない場合、販売見積明細行を Supply Chain Management にインポートすることができます。

    - **SiteId** – Supply Chain Management で見積書および販売注文を生成するにはサイトが必要です。 **SiteId** に対する既定のテンプレート値はありません。
    - **WarehouseId** – Supply Chain Management で見積書および販売注文を処理するには倉庫が必要です。 **WarehouseId** に対する既定のテンプレート値はありません。

## <a name="template-mapping-in-data-integrator"></a>データ インテグレーターでテンプレートのマッピング

> [!NOTE]
> - **割引**、**請求**、および **税** フィールドは、Supply Chain Management 内の複雑な設定によって制御されています。 今現在、この設定では、統合マッピングはサポートされていません。 現在の設計では、**価格**、**割引**、**請求金額**、および **税** の各フィールドは、Supply Chain Management によって処理されます。
> - **支払条件**、**運賃条件**、**配送条件**、**送付方法**、および **配送モード** フィールドは、既定のマッピングの一部ではありません。 これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。

### <a name="quoteheader"></a>QuoteHeader

![データ インテグレーターのテンプレート マッピング。](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![データ インテグレーターのテンプレート マッピング。](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>関連トピック

[見込顧客の現金化](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]