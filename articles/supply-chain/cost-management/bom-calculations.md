---
title: BOM の計算
description: 原価ロールアップおよび販売価格計算は部品表 (BOM) 計算と呼ばれ、計算ページから開始します。 この記事では、BOM 計算に関する情報を示します。
author: JennySong-SH
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: c19c15f807a809a68043a75ca935fa92217fcd5f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902805"
---
# <a name="bom-calculations"></a>BOM の計算

[!include [banner](../includes/banner.md)]

原価ロールアップおよび販売価格計算は部品表 (BOM) 計算と呼ばれ、計算ページから開始します。 この記事では、BOM 計算に関する情報を示します。

原価ロールアップおよび販売価格計算は部品表 (BOM) 計算と呼ばれ、**計算ページ** から開始します。 **計算** ページから、次のタスクを実行します。

-   製品の原価を計算し、原価バージョン内で関連する品目原価レコードを生成する。
-   製品の販売価格を計算し、原価バージョン内で関連する品目販売価格レコードを生成する。

**計算** ページの使用方法は、どのように BOM 計算を開始するによってわずかに異なります。 **計算** ページの使用方法は、BOM 計算で使用する原価バージョン (標準原価または予定原価) や、その原価バージョンで定義されているポリシーによっても異なります。 **注記:** **計算** ページのバリエーションは、販売注文、販売見積、またはサービス注文明細行のコンテキストで使用されます。 これらの計算は、注文固有 BOM 計算と呼ばれます。 注文固有 BOM 計算では、原価バージョン内に品目の原価レコードが生成されません。 代わりに、**BOM 計算の詳細** ページに表示される計算レコードが生成されます。 この計算レコードには、算出原価および算出販売価格が含まれます。 **計算** ページは単一の製品または原価バージョンに対して開始できます。

-   単一の製品品目の原価を計算するには、**品目価格** ページから BOM 計算を開始します。 **計算** ページは、品目の ID を継承します。 原価バージョン、BOM バージョン、工順バージョン、計算量、計算日、およびサイトを指定する必要があります。
    -   既定では、BOM バージョンおよび工順バージョンは、品目、サイト、日付、および計算量の有効なバージョンに設定されます。 ただし、承認されたバージョンでの既定値を上書きすることができます。
    -   既定では、計算量は、品目の標準注文数量に設定されます。 しかし、ユーザーは既定値を上書きすることができます。
    -   計算日またはサイトは原価バージョンに基づいて指定されます。原価バージョンで指定されていない場合は、これらの値をユーザーが指定できます。 計算日として現在より先の日付を指定すると、保留原価レコードが使用されます。 BOM 計算では、計算日かそれより前の最も近い開始日を持つ保留原価レコードが使用されます。
-   すべての製品または選択した品目の原価を計算する場合、または使用場所に基づいて品目を更新する場合は、**原価バージョン設定** ページまたは **原価バージョンの保守** ページから BOM 計算を開始します。 **計算** ページは、原価バージョンを継承します。
    -   製造部品に下位 BOM または下位工程が指定されていない限り、BOM 計算では、製品 (および関連サイト、日付、数量) の有効な BOM バージョンと工程バージョンが使用されます。
    -   計算では、製造品目の標準注文数量が使用されます。 標準注文数量に基づいて、構成部品の数量が計算され、適切な BOM バージョンと工程バージョンが決定され (BOM と工程が数量の影響を受ける場合)、固定費が償却されます。 ただし、製造部品に **生産** または **仕入先** の BOM 明細行タイプがある場合、または BOM 計算で受注生産展開モードを使用する場合は、この仮定は適用されません。指定した計算数量が適用されます。
    -   計算日またはサイトは原価バージョンに基づいて指定されます。原価バージョンで指定されていない場合は、これらの値をユーザーが指定できます。

他のバリエーションの BOM 計算では、原価タイプおよび原価計算バージョンの制限を反映します。

-   標準原価での BOM 計算は、原価バージョン ポリシーによって制限される必要があります。この制限により、標準原価原則の使用が保証されます。 標準原価の原則は、購買品目の標準原価、単一レベル展開モード、および単位原価への雑費の包含の使用に関する制限の実施を要求します。
-   予定原価での BOM 計算では、標準原価の原則に従う必要がありません。 これらの BOM 計算では、さまざまな展開モード、購買品目の原価データの代替ソース、および原価バージョン内の制限の任意実施を使用できます。

### <a name="bom-calculations-that-use-standard-costs"></a>標準原価での BOM 計算

(標準原価の) 原価バージョン内のポリシーは、5 つの BOM 計算ポリシーの実施を必須指定できます。 原価バージョン内の **記録制限** オプションは、これらのポリシーの 1 つを必須指定します。ここで、雑費は単位原価に含まれている必要があります。 購買品目の雑費は手動で入力できますが、製品品目の雑費は固定費の計算済償却を反映します。 原価バージョン内の **計算制限** オプションは、他の 4 つの BOM 計算ポリシーを必須指定します。

-   購買品目の原価貢献度のソースは、標準原価に基づいている必要があります。 言い換えると、BOM 計算では、指定された原価バージョン内、または標準原価を含む予備内の品目原価レコードを使用する必要があります。
-   標準原価の正確で一貫した計算を保証するために、展開モードは単一レベルにする必要があります。
-   品目の販売価格の計算で一貫した結果を得るために、利益設定を必須にする必要があります。 原価バージョンで販売価格の内容が許可されている場合にのみ、利益設定が使用され、品目販売価格レコードが生成されます。
-   予備原則は必須にする必要があります。それは **なし**、**有効** (有効な原価レコード用)、または **原価バージョン** (特定の原価バージョン用) に設定することができます。

### <a name="bom-calculations-that-use-planned-costs"></a>予定原価での BOM 計算

(予定原価の) 原価バージョン内のポリシーは、5 つの BOM 計算ポリシーの実施をオプションとして必須指定できます。 また、ポリシーは既定値の指定のみもできます。 原価バージョン内の **記録制限** オプションは、雑費に関する BOM 計算ポリシーを必須にするか、既定値として使用するかを決定します。 必要であれば、オプションとして雑費を単価に含めることもできます。 原価バージョン内の **計算制限** オプションは、他の 4 つの BOM 計算ポリシーを必須にするか、既定値として使用するかを決定します。

-   原価バージョン内の品目原価レコードを、購買品目の原価貢献度のソースとすることができます。 また、品目に割り当てられている BOM 計算グループでソースを定義することもできます。 たとえば、BOM 計算グループは、原価貢献度データのソースとして購買価格売買契約を定義できます。
-   展開モードは、単一レベル、複数レベル、または受注生産にするか、BOM 明細行品目に基づくことができます。 BOM 明細タイプの展開モードは、製造オーダー見積の原価計算ロジックを複製します。
-   利益設定は、必須または既定値にできます。 原価バージョンで販売価格の内容が許可されている場合にのみ、利益設定が使用され、品目販売価格レコードが生成されます。
-   予備原則は、必須または既定値にできます。 予備原則は、**なし**、**有効** (有効な原価レコード用)、または **原価バージョン** (特定の原価バージョン用) に設定することができます。

BOM 計算では、警告メッセージおよびその他の種類のメッセージが生成されます。 いくつかの BOM 計算ポリシーでは、メッセージの種類が決定されます。 警告条件は、品目に割り当てられている BOM 計算グループで定義されます。 ただし、これらの警告条件は、BOM 計算の開始時に上書きできます。 予備原則を使用している場合、通常は予備情報を情報メッセージとして表示すると便利です。 また、不足している原価レコードのある品目の算出原価を更新しようとしている場合は、情報メッセージで更新されなかった品目を識別すると便利です。

## <a name="bom-calculations-that-use-the-fallback-principle"></a>予備原則を使用した BOM 計算
次の状況は、2 種類の予備原則の使用例を示しています。

-   **2 バージョン方式による標準原価の更新** – 原価計算バージョンには、新しい品目やコストの変更を表す保留中のコスト レコードなどの、標準コストの漸進的な変化を含めることができます。 この場合、予備原則により、他の原価計算バージョン内の有効な標準コストの使用を識別できます。
-   **予定コストによるコスト変更の影響のシミュレーション** - 予定コストの原価計算バージョンには、シミュレーションのために漸進的な変化を含めることができます。 この原価計算バージョンには、シミュレーションによる品目コストの変更、コスト カテゴリ、および間接原価の計算式を表す、保留中コスト レコードが含まれます。 この場合、予備原則により、他の原価計算バージョン内の有効な標準コストの使用を識別できます。

## <a name="bom-calculation-of-a-suggested-sales-price"></a>推奨販売価格の BOM 計算
原価プラス利幅手法を使用すると、品目の計算された販売価格に、BOM 計算に対して指定されている利益設定率のセットと、コンポーネント品目、工順操作、および該当する製造間接費に関連する原価が反映されます。 利幅には、原価グループに割り当てられている利益設定率と品目に割り当てられている原価グループ、工順操作の原価カテゴリ、および製造間接費の間接原価計算式が反映されます。 利益設定の割合のセットには **標準**、**利益 1**、**利益 2**、および **利益 3** というラベルが付いています。 利益 1 セットでは、たとえば、購入原料に割り当てられた原価グループに利益設定率 50% が、工順操作の原価カテゴリに割り当てられた原価グループに利益設定率 80% が定義されます。 BOM 計算のコンテキストにより、計算された販売価格の結果の処理方法が決まります。

-   **品目および指定されている原価バージョンに対する BOM 計算** - BOM 計算は、原価バージョン内の保留中販売価格レコードを生成します。 この販売価格レコードは、計算の詳細を表示するための開始点を提供します (**品目原価の計算** ページなど)。 販売価格レコードは、主に参照情報として機能し、販売注文の販売価格の基礎としては使用されません。
-   **注文固有の BOM 計算** - **BOM 計算** ページのバリエーションが販売注文、販売見積、またはサービス注文明細行のコンテキストで使用されます。 注文固有 BOM 計算では、原価バージョン内にレコードが生成されません。 代わりに、**BOM 計算の結果** ページに表示される計算レコードが生成されます。 この計算レコードは、計算の詳細を表示するための開始点を提供します (**品目原価の計算** ページなど)。 選択された計算レコードに関する情報は、計算元の明細行品目に転送できます。 たとえば、計算された販売価格は、販売注文明細行品目に転送できます。

## <a name="order-specific-bom-calculations"></a>注文ごとの BOM 計算
注文ごとの BOM 計算は、製造が完了した品目の BOM 計算の変動を表します。 注文ごとの BOM 計算は、販売注文、販売見積、またはサービス注文明細行の品目に関連して行われます。 注文固有 BOM 計算は、**BOM 計算の結果** ページに表示される計算レコードを生成します。 計算レコードには、重量、有効な原価レコードに基づいて計算された原価、および販売価格の計算結果が含まれます。 注文固有 BOM 計算を実行するたびに **BOM 計算の結果** ページに生成される計算レコードは、計算番号で一意に識別されます。 オプションで、計算レコードの結果を元の明細行品目に転送することができます。 注文ごとの BOM 計算は、製造が完了した品目の BOM 計算とは、2 つの点で異なります。

-   注文固有 BOM 計算では、原価バージョン内に品目の原価レコードが生成されません。 そのため、BOM 計算ポリシーは品目原価レコードの作成や原価レコードの上書きには適用されません。
-   注文ごとの BOM 計算では、常にコンポーネント、原価カテゴリ、間接原価の計算式が使用されます。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]