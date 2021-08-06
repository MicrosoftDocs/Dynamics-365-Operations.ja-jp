---
title: 二重書き込みの見込顧客を現金化
description: このトピックでは、二重書き込みの見込顧客を現金化に関する情報を提供します。
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0fcbc5b0f571e9f2cf7f1ad7c1e976d022199b47
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542274"
---
# <a name="prospect-to-cash-in-dual-write"></a>二重書き込みの見込顧客を現金化

[!include [banner](../../includes/banner.md)]

ほとんどの企業にとって重要な目標は、見込顧客を顧客に変換し、その顧客との継続的な取引関係を維持することです。 Microsoft Dynamics 365 アプリでは、見込顧客を現金化のプロセスが見積または注文処理のワークフローで行われ、財務の調整と認識が行われます。 二重書き込みによる見込顧客を現金化の統合により、見積と、Dynamics 365 Sales または Dynamics 365 Supply Chain Management のいずれかの方法で発生した注文を取得し、両方のアプリで見積と注文を使用できるようにするワークフローが作成されます。

アプリ インターフェイスでは、処理のステータスおよび請求書情報にリアル タイムでアクセスできます。 したがって、見積と注文を再作成することなく、Supply Chain Management の製品在庫、在庫処理、およびフルフィルメントなどの機能をより簡単に管理することができます。

![見込顧客を現金化への二重書き込みデータフロー。](../dual-write/media/dual-write-prospect-to-cash[1].png)

顧客と連絡先の統合については、[統合された顧客マスター](customer-mapping.md) を参照してください。 成果物統合については、[統一された製品経験](product-mapping.md) を参照してください。

> [!NOTE]
> Dynamics 365 Sales では、見込顧客と顧客の両方が、**RelationshipType** 列が **見込顧客** または **顧客** である **アカウント** テーブル内のレコードを参照します。 ビジネス ロジックに、最初に見込み客として、次に顧客として **アカウント** レコードを作成して承認する **アカウント** 認定プロセスが含まれる場合、そのレコードは顧客 (`RelationshipType=Customer`) の場合にのみ Finance and Operations アプリに同期されます。 **アカウント** 行を見込顧客として同期する場合は、見込顧客データを統合するカスタム マップが必要です。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

販売見積を同期するためには、次の設定を更新する必要があります。

### <a name="setup-in-sales"></a>Sales での設定

Sales で、**設定 \> 管理 \> システム設定 \> 販売** の順にクリックし、次の設定が使用されていることを確認してください。

- **システム価格計算を使用** システム オプションが、**はい** に設定されています。
- **割引の計算方法** 列が、**明細行品目** に設定されている。

### <a name="sites-and-warehouses"></a>サイトと倉庫

Supply Chain Management では、見積明細行と注文明細行に対して **サイト** と **倉庫** 列が必要です。 サイトと倉庫を既定の注文設定で設定した場合、これらの列は、見積明細行または注文明細行に製品を追加したときに自動的に設定されます。 

### <a name="number-sequences-for-quotations-and-orders"></a>見積と注文の番号順序

Sales および Supply Chain Management で見積と注文が作成され同期されている場合、Supply Chain Management と販売の番号順序は接続されていません。 Sales で作成された販売注文が Supply Chain Management に同期されている場合は、Supply Chain Management の販売注文番号も同じになります。 販売注文番号が重複しないようにするには、2 つのアプリで別の番号順序システムを使用する必要があります。

たとえば、Supply Chain Management の番号順序は **1、2、3、4、5** となり、売上の番号順序は **100、99、98、...** となります。Sales で 100 の販売注文を作成する場合は、最終的に、Supply Chain Management に既に存在する注文番号が生成されます。 つまり、2 つの番号順序は、Supply Chain Management および Sales で販売注文が作成されるときに、最終的に重複します。 代わりに、Supply Chain Management で **F1、F2、F3、...** などの番号順序や Sales で **C1、C2、C3、...** などの番号順序を使用することができます。 これらの番号順序では重複する販売注文番号が作成されることはありません。

## <a name="sales-quotations"></a>販売見積

販売見積が Sales または Supply Chain Management で作成されます。 Sales で見積を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。 同様に、Supply Chain Management で見積を作成すると、その見積がリアル タイムで Sales に同期されます。 次のポイントに注意します。

+ 見積の製品に割引を追加できます。 この場合、割引は Supply Chain Management に同期されます。 **割引**、**諸費用**、**税** 列は、ヘッダーで Supply Chain Management の設定によって制御されます。 この設定では、統合マッピングはサポートされていません。 代わりに、**価格**、**割引**、**諸費用**、**税** の各列は、Supply Chain Management で管理および処理されます。
+ 販売見積ヘッダーの **割引 %**、**割引**、**送料** 列は、読み取り専用列です。
+ **運賃条件**、**配送条件**、**送付方法**、および **配送モード** 列は、既定のマッピングの一部ではありません。 これらの列をマップするには、テーブルが同期される組織内のデータに固有の値マッピングを設定する必要があります。

また、Field Service ソリューションも使用している場合は、**見積明細行の簡易作成** パラメータを再度有効にする必要があります。 このパラメータを再度有効にすると、簡易作成機能を使用して、見積明細行の作成を続行することができます。

1. Dynamics 365 Sales アプリケーションに移動します。
2. ナビゲーション バー上部の設定アイコンを選択します。
3. **詳細設定** を選択します。
4. **システムのカスタマイズ** オプションを選択します。
5. **見積明細行** のメニュー項目を選択します。
6. **データ サービス** セクションに移動し、**簡易作成を許可する** チェックボックスをオンにします。

## <a name="sales-orders"></a>販売注文

販売注文が Sales または Supply Chain Management のいずれかで作成されます。 Sales で販売注文を作成すると、その見積がリアル タイムで Supply Chain Management に同期されます。 同様に、Supply Chain Management で販売注文を作成すると、その見積もりがリアル タイムで Sales に同期されます。 次のポイントに注意します。

+ Dynamics 365 Sales でリスト外製品は、Dynamics 365 Supply Chain Management では製品カテゴリとして表示されます。
+ 割引計算と丸め:

    - Sales での割引計算モデルは、Supply Chain Management の割引計算モデルとは異なります。 Supply Chain Management では、販売注文明細行の最終的な割引金額は、割引額と割引率の組み合わせの結果です。 この最終割引額をライン上の数量で割ると、丸め処理が発生する可能性があります。 ただし、この丸め処理単位の割引額が Sales に同期されている場合は、この丸め処理は考慮されません。 Supply Chain Management の販売明細行からの全額割引が Sales に正しく同期されるようにするには、全額を明細行の数量で除算せずに同期させる必要があります。 したがって、Sales で割引の計算方法を **明細行品目** として定義する必要があります。
    - 販売注文行が Sales から Supply Chain Management に同期される場合、明細行全体の割引額が使用されます。 Supply Chain Management には、明細行の完全な割引金額を格納できる列がないため、金額は数量で除算されて、**行割引** 列に格納されます。 この区分中に発生する丸めは、販売明細行の **販売費用** 列に保管されます。

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>例: Sales から Supply Chain Management への同期

次の販売注文があります。

+ **Sales:** 数量 = 3、行あたりの割引 = 10.00 USD
+ **Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01

Supply Chain Management から Sales に同期すると、次の結果が得られます。

+ **Supply Chain Management:** 数量 = 3、明細行割引金額 = $3.33、売上諸掛 = -$0.01
+ **Sales:** 数量 = 3、行あたりの割引 = (3 × 3.33 USD) + 0.01 USD = 10.00 USD

## <a name="dual-write-solution-for-sales"></a>Sales のための二重書き込みソリューション

新しい列が **注文** テーブルに追加され、ページに表示されます。 これらの列のほとんどは、Sales の **統合** タブに表示されます。 状態列がどのようにマッピングされるかについての詳細は、[販売注文の状態列のマッピングを設定する](sales-status-map.md) を参照してください。

+ **販売注文** ページに **請求書作成** または **注文のキャンセル** ボタンは Sales に表示されません。
+ **販売注文状態** は **有効** のままにすると、Supply Chain Management からの変更が Sales の販売注文に流れるようにします。 この動作を管理するためには、既定の **ステイトコード \[ステータス\]** 値を **有効** に設定します。

## <a name="invoices"></a>請求書

売上請求書が Supply Chain Management で作成され、Sales に同期されます。 次のポイントに注意します。

+ **請求書番号** 列が **請求書** テーブルに追加され、ページに表示されます。
+ 請求書が Supply Chain Management で作成され、Sales に同期されるため、**販売注文** ページの **請求書の作成** ボタンは非表示になります。 請求書が Supply Chain Management から同期されるため、**請求書** ページは編集できません。
+ Supply Chain Management からの関連請求書が Sales に同期されると、**販売注文状態** 値は自動的に **請求済** に変更されます。 さらに、請求書の作成元である販売注文の所有者は、請求書の所有者として割り当てられます。 したがって、販売注文書の所有者は、請求書を表示することができます。
+ **運賃条件**、**配送条件**、および **配送モード** 列は既定のマッピングには含まれていません。 これらの列をマップするには、テーブルが同期される組織内のデータに固有の値マッピングを設定する必要があります。

## <a name="templates"></a>テンプレート

次の表に示されているように、見込顧客を現金化するには、データ操作中に連携して動作するコア テーブル マップのコレクションが含まれています。

| Finance and Operations アプリ | Customer Engagement アプリ | 説明 |
|-----------------------------|-----------------------------------|-------------|
[すべての製品](mapping-reference.md#138) | msdyn_globalproducts | |
[顧客 V3](mapping-reference.md#101) | 勘定 | |
[顧客 V3](mapping-reference.md#116) | 連絡先 | |
[連絡先 V2](mapping-reference.md#221) | msdyn_contactforparties | |
[CDS 販売注文ヘッダー](mapping-reference.md#217) | 販売注文 | |
[CDS 販売注文明細行](mapping-reference.md#216) | 販売注文詳細 | |
[CDS 販売見積ヘッダー](mapping-reference.md#215) | 見積 | |
[CDS 販売見積明細行](mapping-reference.md#214) | 見積詳細 | |
[リリース済製品 V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[売上請求書ヘッダー V2](mapping-reference.md#118) | 請求書 | Finance and Operations アプリの売上請求書ヘッダー V2 テーブルには、販売注文と自由形式の 請求書が含まれています。 Dataverse では、自由形式の請求書ドキュメントを除外するデュアル書き込み用のフィルターが適用されます。 |
[売上請求書明細行 V2](mapping-reference.md#117) | invoicedetails | |
[販売注文元コード](mapping-reference.md#186) | msdyn_salesorderorigins | |

価格リストの詳細については、[統一された製品経験](product-mapping.md) を参照してください。

## <a name="limitations"></a>制限

- 返品注文はサポートされていません。
- 訂正票はサポートされていません。
- 顧客や仕入先など、マスタ データに対して財務分析コードを設定する必要があります。 顧客が見積書または販売注文に追加されると、顧客レコード に関連付けられている財務分析コードが自動的に注文にフローします。 現在、デュアル書き込みにはマスター データの財務分析コード データは含まれていません。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
