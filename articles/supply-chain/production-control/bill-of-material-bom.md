---
title: 部品表およびフォーミュラ
description: この記事では、製品および製品バリアントの定義の中心となる部品表 (BOM) およびフォーミュラについて説明します。
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace, ProdBOM, ProdJournalTransBOM, ProdBOMCurrent, PmfBOMDesignerEditCoBy, ProdJournalPickingListLineSummary, ProdBOMOverview, PmfCoReqPlanning, EcoResProductProdTypeFormulaNoActiveFormulaFormPart, EcoResItemsMissingActiveRouteVersionFormPart, EcoResItemsProdTypeBOMExpiringBOMFormPart, BOMDesignerBOMVersion, BOMExpandPurch, BOMChangeLine, BOMExpandSales, EcoResItemsProdTypeBOMExpiringRouteFormPart, EngChgEcmBomDesigner, EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmBOMCopyDialog, EngChgEcmBomDesignerEditBom, BOMDesignerFilterDialog, BOMDesignerFilterDialog, BOMPartOf, BOMSetupReportFinish, EcoResItemsMissingActiveBOMVersionFormPart, BOMIdLookup, EcoResProductProdTypeFormulaNoActiveRouteFormPart, BOMExpandPurchRFQ, EngChgCaseRouteTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 57a30aba3b0a37d939d0747b2dd305a92c82ae23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887286"
---
# <a name="bills-of-materials-and-formulas"></a>部品表およびフォーミュラ

[!include [banner](../includes/banner.md)]

この記事では、製品および製品バリアントの定義の中心となる部品表 (BOM) およびフォーミュラについて説明します。 BOM およびフォーミュラは、特定の製品に必要な材料または成分を指定します。 フォーミュラは、特定の生産コンテキストで入庫する連産品および副産物も指定します。 

## <a name="bills-of-materials"></a>部品表

部品表 (BOM) は、製品の製造に必要なコンポーネントを定義します。 コンポーネントは、原材料、半完成製品、または材料のいずれかです。 場合によっては、サービスを BOM 内で参照できます。 ただし、一般的に、BOM は、必要な *原材料リソース* について説明しています。  

製品の作成のために必要な工程とリソースを説明するルートまたは生産フローと BOM を組み合わせた場合、BOM は、製品の見積原価を計算するための基礎になります。  

BOM は次の情報によって説明される個別のエンティティです。

-   BOM
-   BOM 名
-   コンポーネントと材料を説明する BOM 明細行
-   BOM を使用できる製品と期間を定義する BOM バージョン

1 つの BOM は、固有 ID によって識別される単一レベルについて説明しています。 コンポーネントには、BOM バージョンによって参照される固有の BOM が存在する可能性があります。 BOM デザイナーの特定の製品のために、BOM の完全な階層を表示および編集できます。

### <a name="formulas-co-products-and-by-products"></a>フォーミュラ、連産品、および副産物

フォーミュラは、通常プロセス製造に使用される BOM のサブタイプです。 コンポーネント、材料、フォーミュラに加えて、連産品と副産物について説明します。 実際のバージョンでは、フォーミュラの連産品と副産物の定義には、フォーミュラ バージョンが必要です。 フォーミュラは、通常、フォーミュラ バージョンで定義されている 1 つの特定の完成品 (フォーミュラまたは計画品目) に定義されます。

### <a name="boms-in-the-product-lifecycle"></a>製品ライフ サイクルの BOM

製品ライフ サイクルで、さまざまなタイプの BOM が、さまざまな理由で作成される場合があります。

-   **スケッチ/ドラフトの BOM** – この BOM は、早期設計フェーズに必要な材料の見積のドラフトを提供します。また、原価のおおまかな見積と見積済製品属性に役立ちます。 通常、この BOM は、エンタープライズ リソース プランニング (ERP) では使用されません。
-   **エンジニアリング BOM** – このBOMは、通常、既存の製品のポートフォリオに基づく製品を作成するときに使用されます。 エンジニアリング BOM は、設計プロセスを簡素化し、複雑な製品をエンジニアリング モジュールにグループ化するために構造化されます。 簡単な製品の場合、実際の生産プロセスにエンジニアリング BOM が使用できる場合があります。 ただし、他の製品の場合、エンジニアリング BOM は実際の生産 BOM に変換する必要があります。 エンジニアリング BOM は、通常 BOM 階層のファントムにより表されます。 エンジニアリング BOM は製造工程の計画と実行に使用されますが、この方法は、特に多くの注文を作成する反復的な工程の場合には、非能率を発生する可能性があります。
-   **計画 BOM** – この BOM は、必要な材料の計画に使用されます。 コンポーネントと材料の需要は、完成品の需要に基づいて計算されます。 BOM の原価計算と同様に、計画 BOMは、期間内に使用される材料の特定の組み合わせを表す場合があります。
-   **生産 BOM** – これは、特定の生産に使用される実際の BOM です。 生産 BOM は、製品の生産で使用される実際のリソースを考慮する必要があります。 製造オーダー、バッチ オーダー、またはかんばんが作成されると、ファントムで表される BOM の複数のレベルは、1 つのレベルに折りたたまれ、注文の工程に配分されます。
-   **原価計算 BOM** – この BOM は、製品の見積原価の計算に使用されます。 たとえば、標準原価を使用する場合、または特定の製品の予定原価見積を計算する場合に、原価計算 BOM を使用できます。 原価計算 BOM は、使用すると想定されている材料とリソースの特定の組み合わせを参照できます。 したがって、ある期間の代表的な見積原価を作成し、時間経過に伴う差異を回避するために、原価計算 BOM を使用できます。

実装に実際に使用される BOM のタイプは、実装や取引シナリオと要件によって異なります。 簡単な実装では、計画 BOM、生産 BOM、原価計算 BOM は、1 つの BOM としてモデル化できます。 頻繁な技術変更、複数の代替工順がある環境では、大規模な一連の BOM タイプが要求される可能性があります。

### <a name="approval-of-boms-and-formulas"></a>BOM とフォーミュラの承認

各 BOM とフォーミュラは、個別に承認または未承認にすることができます。 通常、最初に関連する BOM バージョンが承認されると、BOM またはフォーミュラの承認が発生します。 ただし、一部の業務シナリオでは、これらの承認は、プロセスで異なるステップがあったり、異なるプロセス オーナーを含む場合があります。  

BOM が承認されない場合は、すべての関連する BOM バージョンも承認されないことに注意してください。

## <a name="bom-and-formula-versions"></a>BOM とフォーミュラのバージョン
生産できる製品バリアントに特定の BOM またはフォーミュラを関連付けるには、BOM バージョンまたはフォーミュラ バージョンを作成する必要があります。 BOM バージョンとフォーミュラ バージョンの有効性は、期間、数量、サイト、特定の製品分析コード、およびその他の基準によって制約することができます。 フォーミュラ バージョンには、歩留まり、連産品と副産物の定義などの追加の重要な属性があり、またフォーミュラの原価配分の指示があります。

### <a name="approval-of-bom-and-formula-versions"></a>BOM とフォーミュラ バージョンの承認

BOM バージョンは、計画プロセスまたは製造プロセスで使用する前に、承認される必要があります。 BOM バージョンが承認されると、関連する BOM もユーザーの選択と認証権限に応じて承認できます。 関連する BOM 自体が承認されている場合のみ、BOM バージョンを承認できることに注意してください。

### <a name="activation-of-the-default-bom-or-formula-version"></a>既定の BOM またはフォーミュラ バージョンの有効化

マスタ プランで使用する、または製造オーダーの作成に使用する既定の BOM バージョンまたはフォーミュラ バージョンとして、特定の BOM またはフォーミュラを設定するには、そのバージョンを有効化する必要があります。 バージョンが有効になると、指定された制約 (たとえば、期間、サイト、または数量) のバージョンの独自性が確認されます。 有効化しようとしているバージョンが、すでに有効なバージョンと競合している場合には、エラー メッセージを受信します。 競合するバージョンを無効にするか、バージョンの制約 (通常は期間) を変更して、あいまいな有効化を禁止する必要があります。

### <a name="product-change-with-case-management"></a>ケース管理を使用した製品変更

新しい、または変更された BOM および BOM バージョンの承認や有効化のための製品変更ケースは、BOM バージョンの制約の概要を簡単に表示する方法を提供します。 また、1 つの有効化日付の特定の変更に関連するすべての BOM やフォーミュラを、承認して有効化することができます。

### <a name="alternative-bom-versions"></a>代替 BOM バージョン

場合によっては、有効な BOM バージョンまたはフォーミュラ バージョンは、予測、販売、または親製品で使用できません。 この場合、代替 BOM またはフォーミュラに、承認済 BOM バージョンまたはフォーミュラ バージョンが存在するときには、要件 (予測明細行、販売明細行、または BOM 明細行) の一部として、特定の承認済 BOM を選択できます。  

計画オーダー、製造オーダー、またはかんばんが作成されると、プランナーまたは作業現場の監督は、特定の製品を計画または製造するために必要な計画製造日付で有効になる承認済 BOM バージョンを使用できます。 使用する BOM バージョンは、既定の BOM バージョンとして有効化する必要はありません。

## <a name="bom-and-formula-lines"></a>BOM 明細行とフォーミュラ明細行
BOM 明細行は、各材料、サービス、または成分に対して作成されます。 明細行は、指定された製品バリアントの予定消費を定義し、予定消費に関連付けられるさまざまな属性を定義します。  

BOM 明細行は、次の明細行タイプを使用できます。**品目**、**ファントム**、**ペギングされた供給**、**仕入先**。

### <a name="item"></a>品目

直接消費される、さらに展開する必要がないまたはペギングされた供給がない、材料やサービスに対しては、**品目** 明細行タイプを選択します。

### <a name="phantom"></a>ファントム

BOM 明細行に含まれる低レベルの BOM 品目を展開する場合は、**ファントム** 明細行タイプを選択します。 マスター スケジューリングの場合、予定原価の計算では、**ファントム** タイプの BOM 明細行を使用する製造オーダーの見積で、ファントム BOM をもつ製品バリアントを参照する親 BOM 明細行が、その製品バリアントに適用できる有効な BOM バージョンによって決定される BOM で BOM 明細行として表示されているコンポーネント品目と置き換えられます。 製品バリアントが適用できる有効な工順を持つ場合、その工順の工程は親の工順にマージされます。  

通常、ファントムは、エンジニアリング プロセスを簡略化するために使用されることに注意してください。 多くのレベルのファントム BOM を広い範囲で使用すると、特に非常に反復的な製造シナリオではパフォーマンスに影響を与えます。 パフォーマンスを改善するには、ファントムの階層が深くなることを避ける必要があります。 代わりに、事前に展開される生産 BOM および工順を使用します。

### <a name="pegged-supply"></a>ペギングされた供給

BOM 明細行が参照する製品バリアントのための、サブ生産、BOM 明細行のイベントかんばん、または直接発注書を作成する場合は、**ペギングされた供給** 明細行タイプを選択します。 製造オーダーを見積ると、サブ生産、イベントかんばん、または発注書が作成されます。 必要な品目数量が消費する製造オーダーに自動的に引き当てられます。

### <a name="vendor"></a>ベンダー

生産プロセスが下請業者を使用し、下請業者にサブ生産や発注書を自動的に作成したい場合は、**仕入先** 明細行タイプを選択します。  

**BOM の外注した工程に関する注記:** 下請業者が実行するサービスや作業は、在庫を追跡されるサービス品目として作成する必要があります。 BOM 明細行として親品目にサービス品目を関連付ける必要があります。 工順には、協力会社の運営ソースに割り当てられる工程を含める必要があります。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]