---
title: 製品の統合エクスペリエンス
description: このトピックでは、財務と運用アプリと Dataverse 間の製品データの統合について説明します。
author: t-benebo
ms.date: 12/12/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1b3dc1d16fc34992df0c9478b8b4d163c310b67b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062601"
---
# <a name="unified-product-experience"></a>製品の統合エクスペリエンス

[!include [banner](../../includes/banner.md)]



ビジネス エコシステムが Finance、Supply Chain Management、Sales などの Dynamics 365 アプリケーションで構成されている場合、企業では通常、製品データを調達するためにこれらのアプリケーションが使用されます。 これは、アプリケーションが、高度な価格決定の概念と正確な手持在庫のデータを補完する堅牢な製品インフラストラクチャを提供することが理由です。 製品データを調達するために外部の製品ライフサイクル管理 (PLM) システムを使用する企業では、財務と運用アプリから他の Dynamics 365 アプリに製品をチャネル化できます。 製品の統合エクスペリエンスによって Dataverse に統合された製品データ モデルがもたらされるため、Power Platform ユーザーを含むすべてのアプリケーション ユーザーが、財務と運用アプリからの豊富な製品データを利用することができます。

Sales の製品データ モデルを次に示します。

![CE の製品データ モデル。](media/dual-write-product-4.jpg)

財務と運用アプリの製品データ モデルを次に示します。

![Finance and Operations の製品データ モデル。](media/dual-write-products-5.jpg)

次に示すように、この 2 つの製品データ モデルは、Dataverse に統合されています。

![Dynamics 365 アプリの製品データ モデル。](media/dual-write-products-6.jpg)

製品のデュアル書き込みテーブル マップは、データを一方向にのみ、財務と運用アプリから Dataverse にほぼリアルタイムでフローするように設計されています。 ただし、製品のインフラストラクチャは開かれており、必要に応じて双方向で使用できるようになっています。 ユーザーは自己責任でカスタマイズできますが、Microsoft では、この方法を推奨していません。

## <a name="templates"></a>テンプレート

製品情報には、製品分析コードや追跡、保管分析コードなど、製品とその定義に関連するすべての情報が含まれます。 次のテーブルが示すように、製品と関連する情報を同期するためにテーブル マップのコレクションが作成されます。

財務と運用アプリ | その他の Dynamics 365 アプリ | Description
-----------------------|--------------------------------|---
[すべての製品](mapping-reference.md#138) | msdyn_globalproducts | すべての製品テーブルには、財務と運用アプリで使用可能なすべての製品 (リリース済製品と非リリース製品の両方) が含まれます。
[特徴的製品をリリースした CDS](mapping-reference.md#213) | 品目 | **製品** テーブルには、製品を定義する列が含まれます。 これには、個々の製品 (製品サブタイプの製品) と製品バリアントが含まれます。 次の表に、このマッピングを示します。
[カラー](mapping-reference.md#170) | msdyn\_productcolors
[構成](mapping-reference.md#171) | msdyn\_productconfigurations
[既定の注文設定](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[製品カテゴリ](mapping-reference.md#166) | msdyn_productcategories | 各製品カテゴリとその構造と特性に関する情報は、製品カテゴリ テーブルに含まれています。
[製品カテゴリの割り当て](mapping-reference.md#167) | msdyn_productcategoryassignments | 製品をカテゴリに割り当てるには、製品カテゴリの割り当てテーブルを使用できます。
[製品カテゴリ階層](mapping-reference.md#168) | msdyn_productcategoryhierarchies | 製品階層を使用して、製品を分類またはグループ化します。 カテゴリ階層は、製品カテゴリの階層テーブルを使用して Dataverse で利用可能です。
[製品カテゴリ階層ロール](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | 製品階層は、D365 Finance and Operations のさまざまなロールに対して使用できます。 これらは製品カテゴリのロール エンティティが使用される、各ロールで使用するカテゴリを指定します。
[製品の既定の注文設定 V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[製品分析コード グループ](mapping-reference.md#173) | msdyn\_productdimensiongroups | 製品を定義する製品分析コードが定義されている製品分析コード グループ。
[製品マスターの色](mapping-reference.md#187) | msdyn_sharedproductcolors | **共有製品の色** テーブルは、特定の製品マスターに対して設定できる色を示します。 この概念は、データの整合性を保つために Dataverse に移行されます。
[製品マスターのコンフィギュレーション](mapping-reference.md#188) | msdyn_sharedproductconfigurations | **共有製品の構成** テーブルは、特定の製品マスターに対して設定できる構成を示します。 この概念は、データの整合性を保つために Dataverse に移行されます。
[製品マスターのサイズ](mapping-reference.md#190) | msdyn_sharedproductsizes | **共有製品のサイズ** テーブルは、特定の製品マスターに対して設定できるサイズを示します。 この概念は、データの整合性を保つために Dataverse に移行されます。
[製品マスターのスタイル](mapping-reference.md#191) | msdyn_sharedproductstyles | **共有製品のスタイル** テーブルは、特定の製品マスターに対して設定できるスタイルを示します。 この概念は、データの整合性を保つために Dataverse に移行されます。
[バーコードを識別した製品番号](mapping-reference.md#164) | msdyn\_productbarcodes | 製品のバーコードは、製品を一意に識別するために使用されます。
[製品固有の単位換算](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[リリース済製品 V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | **msdyn\_sharedproductdetails** テーブルには、製品を定義する財務と運用アプリの列が含まれます。これには、製品の財務情報と管理情報が含まれています。
[サイズ](mapping-reference.md#174) | msdyn\_productsizes
[保管分析コード グループ](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | 製品保管分析コード グループは、倉庫における製品の配置を定義するために使用される方法を表します。
[スタイル](mapping-reference.md#178) | msdyn\_productsytles
[追跡用分析コード グループ](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | 製品追跡用分析コード グループは、在庫の製品を追跡するために使用される方法を表します。
[単位](mapping-reference.md#219) | uoms
[単位換算](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>製品の統合

このモデルでは、製品が、Dataverse にある **製品** と **msdyn\_sharedproductdetails** という 2 つのテーブルの組み合わせによって表されます。 最初のテーブルには、製品の定義 (製品の固有 ID、製品名、説明) が含まれており、2 番目のテーブルには、製品レベルで保存された列が含まれています。 この 2 つのテーブルの組み合わせを使用して、最小在庫管理単位 (SKU) の概念に従って製品を定義します。 リリースされた各製品の情報は、記載されているテーブル (製品および共有製品の詳細) で提供されます。 すべての製品 (リリース済であるかどうかにかかわらず) を追跡する場合は、**グローバル製品** テーブルが使用されます。

製品は SKU として表されるため、特徴的製品、製品マスター、および製品バリアントの概念は、次に示すとおり、Dataverse に取り込むことができます。

- **製品サブタイプの製品** は、自身で定義されている製品です。 分析コードを定義する必要はありません。 例として、特定の書籍が挙げられます。 これらの製品については、**製品** テーブルに 1 つの行が作成され、**msdyn\_sharedproductdetails** テーブルに 1 つの行が作成されます。 製品ファミリ行は作成されません。
- **製品マスター** は、業務プロセスの動作を決定する定義とルールを保持する汎用製品として使用されます。 これらの定義に基づいて、製品バリアントと呼ばれる特徴的製品を生成することができます。 たとえば、T シャツは製品マスターであり、色とサイズを分析コードとして持つことができます。 この分析コードの組み合わせが異なるバリアント (S サイズの青い T シャツまたは M サイズの緑の T シャツなど) をリリースすることができます。 統合では、バリアントごとに 1 つの行が製品テーブルに作成されます。 この行には、さまざまな分析コードなど、バリアント固有の情報が含まれています。 製品の一般情報は、**msdyn\_sharedproductdetails** テーブルに格納されています。 (この汎用情報は製品マスターに保持されます。) 製品マスター情報は、リリースされた製品マスターが作成されるとすぐに (ただし、バリアントがリリースされる前に)  Dataverse に同期されます。
- **特徴的製品** は、製品サブタイプのすべての製品とすべての製品バリアントを参照します。

![製品のデータ モデル。](media/dual-write-product.png)

デュアル書き込み機能が有効になっている場合、Finance and Operations からの製品はその他の Dynamics 365 アプリに **下書き** 状態で同期されます。 同期の内容は、Customer Engagement アプリで使用されているのと同じ通貨の最初の価格リストに追加され、価格リスト名でアルファベット順の並べ替えを使用して追加されます。 これは、同期の内容が、製品が財務と運用アプリでリリースされている法人テーブルの通貨と一致する Dynamics 365 アプリの最初の価格表に追加されるという意味です。 指定した通貨の価格リストがない場合は、価格リストが自動的に作成され、製品が割り当てられます。

既定の価格リストを単位に関連付ける二重書き込みプラグインの現在の実装は、 アプリに関連付けられている通貨を検索し、価格リスト名でアルファベット順の並べ替えを使用して、財務と運用アプリの最初の価格リストを見つけます。 特定の通貨に複数の価格リストがある場合に、その通貨の既定の価格リストを設定するには、価格リストの名前を同じ通貨の他の価格リストよりもアルファベット順で早い名前に更新する必要があります。 指定した通貨の価格リストがない場合は、新しい通貨が作成されます。

既定では、財務と運用アプリの製品は、**下書き** 状態で他の Dynamics 365 アプリに同期されます。 製品を **有効** 状態と同期して、販売注文の見積書で直接使用できるようにするには、例として、次の設定を選択する必要があります。**システム > 管理 > システム管理 > システム設定 > 販売** タブで、**有効な状態で製品を作成 = はい** を選択します。

製品が同期されている場合は、Salse では必須フィールドなので、財務と運用アプリの **販売単位** フィールドに値を入力する必要があります。

Dynamics 365 Sales からの製品ファミリーの作成は、製品の二重書き込み同期ではサポートされていません。

製品の同期は、財務と運用アプリから Dataverse に対して実行されることに注意してください。 つまり、製品テーブル列の値は Dataverse で変更できますが、同期がトリガーされるときに (財務と運用アプリで製品列が変更されるとき)、Dataverse の値が上書きされます。

財務と運用アプリ | Customer Engagement アプリ |
---|---
[特徴的製品をリリースした CDS](mapping-reference.md#213) | 品目 |
[リリース済製品 V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[すべての製品](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>製品分析コード

製品分析コードは、製品バリアントを識別する特性です。 また、4 つの製品分析コード (色、サイズ、スタイル、コンフィギュレーション) が Dataverse にマップされて、製品バリアントを定義します。 次の図は、製品分析コードの色のデータ モデルを示しています。 サイズ、スタイル、およびコンフィギュレーションに同じモデルが適用されます。

![製品ディメンションのデータ モデル。](media/dual-write-product-two.png)

財務と運用アプリ | Customer Engagement アプリ |
---|---
[カラー](mapping-reference.md#170) | msdyn\_productcolors
[サイズ](mapping-reference.md#174) | msdyn\_productsizes
[スタイル](mapping-reference.md#178) | msdyn\_productsytles
[構成](mapping-reference.md#171) | msdyn\_productconfigurations

1 つの製品に異なる製品分析コードが含まれている場合 (たとえば、製品マスターのサイズや色が製品分析コードと同じである場合)、個々の特徴的製品 (つまり、各製品バリアント) は、それらの製品分析コードの組み合わせとして定義されます。 たとえば、製品番号 B0001 は、XS サイズの黒い T シャツで、製品番号 B0002 は S サイズの黒い T シャツです。 この場合、製品分析コードの既存の組み合わせが定義されています。 たとえば、前の例の T シャツは、XS サイズの黒、S サイズの黒、M サイズの黒、L サイズの黒にすることができますが、XL サイズの黒にすることはできません。 つまり、製品マスターが実行できる製品分析コードは指定されており、これらの値に基づいてバリアントをリリースできます。

製品マスターで実行できる製品分析コードを追跡するために、各製品分析コードに対して次のテーブルが Dataverse に作成され、マッピングされます。 詳細については、「[製品情報の概要](../../../../supply-chain/pim/product-information.md)」を参照してください。

財務と運用アプリ | Customer Engagement アプリ |
---|---
[製品マスターの色](mapping-reference.md#187) | msdyn_sharedproductcolors |
[製品マスターのコンフィギュレーション](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[製品マスターのサイズ](mapping-reference.md#190) | msdyn_sharedproductsizes |
[製品マスターのスタイル](mapping-reference.md#191) | msdyn_sharedproductstyles |
[バーコードを識別した製品番号](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>既定の注文設定と製品固有の既定の注文設定

既定の注文設定は、品目が供給または保管されるサイトおよび倉庫、取引または在庫管理のために使用される最小、最大、複数、標準数量、リード タイム、停止フラグ、注文納期メソッドを定義します。 この情報は、既定の注文設定と製品固有の既定の注文設定エンティティを使用して Dataverse で利用できます。 機能の詳細については、[既定の注文設定トピック](../../../../supply-chain/production-control/default-order-settings.md) を参照してください。

財務と運用アプリ | Customer Engagement アプリ |
---|---
[既定の注文設定](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[製品の既定の注文設定 V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>測定単位と測定単位の換算

次の図のデータ モデルで示すように、測定単位と対応する変換は Dataverse で利用できます。

![測定単位のデータ モデル。](media/dual-write-product-three.png)

測定単位の概念は、財務と運用アプリとその他の Dynamics 365 アプリの間で統合されています。 財務と運用アプリの各単位クラスでは、単位グループは、単位クラスに属している単位を含む Dynamics 365 アプリで作成されます。 また、既定の基本単位は、すべての単位グループに対して作成されます。

財務と運用アプリ | Customer Engagement アプリ |
---|---
[製品固有の単位換算](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[単位](mapping-reference.md#219) | uoms
[単位換算](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Finance and Operations と Dataverse の間で一致する単位データの初期同期

### <a name="initial-synchronization-of-units"></a>単位の初期同期

デュアル書き込みが有効になっている場合、財務と運用アプリの単位は、他の Dynamics 365 アプリに同期されます。 Dataverse の財務と運用アプリから同期された単位グループには、"外部で管理されている" ことを示すフラグが設定されています。

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finance and Operations および他の Dynamics 365 アプリの単位と単位クラス/グループのデータの照合

まず、単位の統合キーが msdyn_symbol であることに注意する必要があります。 したがって、この値は、Dataverse または他の Dynamics 365 アプリで一意である必要があります。 他の Dynamics 365 アプリでは、単位の一意性を定義する "単位グループID" と "名前" のペアであるため、財務と運用アプリと Dataverse の間で単位データを一致させるためのさまざまなシナリオを検討する必要があります。

財務と運用アプリやその他の Dynamics 365 アプリで一致/重複する単位の場合:

+ **単位は、財務と運用アプリ内の関連付けられている単位クラスに対応する他の Dynamics 365 アプリの単位グループに属します**。 この場合、他の Dynamics 365 アプリの msdyn_symbol 列には、財務と運用アプリの単位記号を入力する必要があります。 したがって、データが照合されると、その単位グループは、他の Dynamics 365 アプリでは "外部管理" として設定されます。
+ **単位は、財務と運用アプリの関連付けられた単位クラスに対応していない他の Dynamics 365 アプリの単位グループに属しています (他の Dynamics 365 アプリにある単位クラスの財務と運用アプリに既存の単位クラスはありません)。** この場合、msdyn_symbol にはランダムな文字列を入力する必要があります。 この値は、他の Dynamics 365 アプリで一意である必要があります。

Finance and Operations の単位および単位クラスで、他の Dynamics 365 アプリに存在しない場合:

財務と運用アプリの単位グループをデュアル書き込みの一部とし、それに対応する単位を他の Dynamics 365 アプリと Dataverse に作成して同期し、この単位グループを "外部管理" として設定します。 追加のブートストラップ作業は不要です。

他の Dynamics 365 アプリの単位で、財務と運用アプリに存在しない場合:

すべての単位で msdyn_symbol の列を入力する必要があります。 単位は、対応する単位クラス (存在する場合) の財務と運用アプリでいつでも作成できます。 単位クラスが存在しない場合は、まず、他の Dynamics 365 アプリ単位グループに一致する単位クラスを作成する必要があります (ただし、列挙型を拡張する場合は、拡張機能を使用する場合を除き、財務と運用アプリで単位クラスを作成することはできません)。 これにより、単位を作成できます。 財務と運用アプリの単位記号は、その単位に対して他の Dynamics 365 アプリで以前に指定された msdyn_symbol である必要があります。

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>製品ポリシー: 分析コード、追跡、保管グループ

製品ポリシーは、在庫内で製品とその特性を定義するために使用される一連のポリシーです。 製品分析コード グループ、製品追跡分析コード グループ、および保管分析コード グループが製品ポリシーとして指定されている場合があります。

財務と運用アプリ | Customer Engagement アプリ |
---|---
[製品分析コード グループ](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[保管分析コード グループ](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[追跡用分析コード グループ](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>製品階層

財務と運用アプリ | Customer Engagement アプリ |
---|---
[製品カテゴリの割り当て](mapping-reference.md#167) | msdyn_productcategoryassignments |
[製品カテゴリ階層](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[製品カテゴリ階層ロール](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>製品の統合キー

Dynamics 365 for Finance and Operations と Dataverse の製品との間で製品を一意に識別するために、統合キーが使用されます。
製品では、**(productnumber)** は Dataverse の製品を識別する固有のキーです。 これは、次の連結によって構成されます **(会社、msdyn_productnumber)**。 **会社** は Finance and Operations の法人エンティティを示し、**msdyn_productnumber** は Finance and Operations の特定の製品の製品番号を示します。

その他の Dynamics 365 アプリのユーザーについては、この製品は **msdyn_productnumber** という UI で識別されます (列のラベルが **製品番号** であることに注意してください)。 製品フォームでは、会社と msydn_productnumber の両方が表示されます。 ただし、製品の固有キーである (productnumber) 列は表示されません。

Dataverse でアプリを作成した場合は、**製品番号** (固有の製品 ID) を統合キーとして使用することに注意する必要があります。 **msdyn_productnumber** は一意ではないので使用しないでください。

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>製品の初期同期と、Dataverse から Finance and Operations へのデータの移行

### <a name="initial-synchronization-of-products"></a>製品の初期同期

デュアル書き込みが有効になっている場合、財務と運用アプリからの製品は Dataverse と Customer Engagement アプリに同期されます。 デュアル書き込みの前に Dataverse およびその他の Dynamics 365 アプリで作成された製品は、財務と運用アプリの製品データに更新および照合されません。

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Finance and Operations および他の Dynamics 365 アプリの製品データの照合

Finance and Operations、Dataverse および他の Dynamics 365 アプリで同じ製品が保持 (重複/一致) されている場合、デュアル書き込みを有効にすると、Finance and Operations の製品が同期され、同じ製品の重複したレコードが Dataverse に表示されます。
以前の状況を回避するために、他の Dynamics 365 アプリが Finance and Operations と重複/一致する製品を所有している場合、二重書き込みを有効にする管理者は、製品の同期が行われる前に **会社** (例: "USMF") および **msdyn_productnumber** (例: "1234:Black:S") の列をブートストラップする必要があります。 つまり、Dataverse の製品のこの 2 つの列には、製品をその製品番号と照合する必要がある Finance and Operations アプリの各会社を入力する必要があります。

次に、同期が有効になって実行されると、Finance and Operations の製品が Dataverse および他の Dynamics 365 アプリの一致する製品と同期されます。 これは、特徴的製品と製品バリアントの両方に適用できます。

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Dynamics 365 アプリから Finance and Operations への製品データの移行

他の Dynamics 365 アプリに Finance and Operations に存在しない製品がある場合、管理者はまず **EcoResReleasedProductCreationV2Entity** を使用して、その製品を Finance and Operations にインポートできます。 次に、上記の説明に従って、Finance and Operations および他の Dynamics 365 アプリの製品データを照合します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
