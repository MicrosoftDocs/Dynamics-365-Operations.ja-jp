---
title: 製品を Supply Chain Management から Sales の製品に直接同期する
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に製品を同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 06/10/2019
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
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817824"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a>製品を Supply Chain Management から Sales の製品に直接同期する

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> 見込顧客を現金化するソリューションを使用する前に、[Microsoft Dataverse for Apps へデータを統合](https://docs.microsoft.com/powerapps/administrator/data-integrator) をよく理解しておく必要があります。

このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Sales に製品を直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

## <a name="data-flow-in-prospect-to-cash"></a>見込み客の現金化へのデータフロー

見込み客の現金化ソリューションは、Supply Chain Management と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。 データ統合機能で利用可能な見込み顧客を現金化するテンプレートにより、Supply Chain Management と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書のデータの流れが可能になります。 次の図は、Supply Chain Management と Sales の間でデータを同期させる方法を示しています。

[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

利用可能なテンプレートにアクセスするには、[Power Apps 管理者センター](https://admin.powerapps.com/dataintegration)を開きます。 **プロジェクト** を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。

Supply Chain Management から Sales への製品同期には、以下のテンプレートと基本的なタスクが使用されます。

- **データ統合における テンプレートの名前:** 製品 (Supply Chain Management から Sales)- 直接
- **データ統合プロジェクトのタスク名:** 製品

製品の同期が発生する前に、同期タスクは必要ありません。

## <a name="entity-set"></a>エンティティ セット

| サプライ チェーン マネジメント    | 販売注文    |
|----------------------------|----------|
| 販売可能なリリース済製品 | 製品 |

## <a name="entity-flow"></a>エンティティのフロー

製品は Supply Chain Management で管理され、Sales に同期されます。 Supply Chain Management の **販売可能なリリース済製品** のデータ エンティティは、*販売可能* な製品のみをエクスポートします。 販売可能製品には、販売注文で使用する必要のある情報があります。 **リリースされた製品** ページで **検証** 機能を使用して製品を検証する場合も、同じルールが適用されます。

[製品番号] がキーとして使用されます。 これは、製品バリアントが [製品バリアント] ごとの個別の [Product ID] で Sales に同期されることを意味します。

## <a name="prospect-to-cash-solution-for-sales"></a>売上の見込顧客を現金化するソリューション

Sales では、新しい **外部管理** フィールドが製品に追加され、特定の製品が外部で維持されていることを示します。 デフォルトでは、値は Sales へのインポート時に **はい** に設定されます。 使用可能な値は次のとおりです。

- **はい** – 製品は Supply Chain Management に由来し、Sales では編集できません。
- **いいえ** – 製品は Sales に直接入力します。
- **(空白)** – 見込顧客を現金化するソリューションを有効にする前に、製品が Sales に存在します。

**外部管理** フィールドは、外部管理された製品を持つ見積および受注のみが Supply Chain Management に同期されることを保証するのに役立ちます。

外部管理の製品が、同じ通貨で最初に有効な価格リストに自動的に追加されます。 価格リストは、名前がアルファベット順で構成されています。 Supply Chain Management の製品販売価格は価格リストの価格として使用されています。 したがって、Supply Chain Management の製品販売通貨ごとに、Sales の価格リストが必要です。 リリースされた販売可能商品の通貨は、製品が輸出される法人の会計通貨に設定されます。

> [!NOTE]
> - 製品の同期は、一致する通貨を含む価格リストなしでは成功しません。
> - データ統合プロジェクトの pricelevelid.name [既定の価格リスト (名前)] をマッピングすることにより、統合に使用される価格リストを制御できます。 入力値は、全小文字である必要があります。 たとえば、'標準' という名前の販売での価格リストの既定値は、次のようになります。出力先フィールド: pricelevelid.name [既定の価格リスト (名前)]、およびタイプのマッピング: [ { "transformType": "既定", "defaultValue": "標準" } ]。

## <a name="preconditions-and-mapping-setup"></a>前提条件とマッピングの設定

- 一番最初の同期を実行する前に、Supply Chain Management の既存製品に対して特徴的製品テーブルを全て入力する必要があります。 このジョブが完了するまで、既存の製品は同期されません。

    1. Supply Chain Management の場合は、検索を使用し、**特徴的製品テーブルの設定** を検索します。
    2. **特徴的製品テーブル** を選択し、ジョブを実行します。 このジョブには、1回のみ実行する必要があります。

- **SalesUnitSymbol** から **DefaultUnit (Name)** へのマッピングに、Supply Chain Management と Sales の間における販売量測定単位 (UOM) に必要な値マップが存在することを確認してください。
- **単位グループ** (**defaultuomscheduleid.name**) の値マップを更新し、Sales の **単位グループ** に一致させます。

    デフォルトのテンプレート値は、**既定単位** です。

- Supply Chain Management からのすべての製品の販売 UOM が Sales に存在することを確認します。
- 価格リストが、Supply Chain Management の製品販売通貨ごとに Sales に存在することを確認します。
- Sales で製品を作成すると、**ドラフト** または **有効** のステータスになります。 動作は、Sales の **設定** > **管理** > **システムの設定** > **販売** で制御されます。

    作成時にステータスが **ドラフト** である製品は、見積書または販売注文に追加する前に有効化する必要があります。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。 

> [!NOTE]
> マッピングは、Sales から Supply Chain Management にどのフィールド情報を同期するかを表示します。

![データ インテグレーターのテンプレートのマッピング](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>関連トピック

[見込顧客を現金化](prospect-to-cash.md)

[Supply Chain Management の顧客への Sales の勘定の直接同期](accounts-template-mapping-direct.md)

[Supply Chain Management の連絡先または顧客への Sales の連絡先の直接同期](contacts-template-mapping-direct.md)

[販売注文の Sales と Supply Chain Management の間の直接同期](sales-order-template-mapping-direct-two-ways.md)

[売上請求書のヘッダーおよび明細行の Supply Chain Management から Sales への直接同期](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]