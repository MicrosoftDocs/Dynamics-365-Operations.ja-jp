---
title: 標準原価を使用する BOM 計算で使用される情報
description: 部品表 (BOM) 計算では、さまざまなデータ ソースのデータで、製造品目の標準原価を計算します。 データ ソースには、品目、部品表の工順、間接原価の計算式、および原価バージョンについての情報があります。
author: JennySong-SH
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aad47abd72876da67dc6cb2602893281a5b270eb
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676218"
---
# <a name="information-used-in-bom-calculations-with-standard-costs"></a>標準原価を使用する BOM 計算で使用される情報

[!include [banner](../includes/banner.md)]

部品表 (BOM) 計算では、さまざまなデータ ソースのデータで、製造品目の標準原価を計算します。 データ ソースには、品目、部品表の工順、間接原価の計算式、および原価バージョンについての情報があります。

標準原価 BOM 計算では、次の購買済品目情報が使用されます。
-   原価 : 購買済品目の原価は、標準原価用の原価バージョンの中でサイト固有の原価レコードとして管理します。 各原価レコードには有効日があり、BOM 計算日によって使用される原価レコードが決まります。 たとえば、計算日が未来である BOM 計算の場合は、ステータスが保留中であり、有効日が未来である原価レコードが使用されます。
-   原価グループ : 購買済品目に割り当てられた原価グループは、製造品目の算出原価における原価区分の基準を提供します。
-   品目の BOM 計算グループに埋め込まれている警告条件により、潜在的問題を BOM 計算で特定できます。 これは BOM では、購買品目のコストがゼロで、数量がゼロの場合か、有効期限切れのコスト レコードがある場合に該当します。 適用された警告状態は、BOM 計算を開始するときに上書きできます。

標準原価 BOM 計算では、次の製造品目情報が使用されます。
-   在庫用標準注文数量 : 品目の在庫用の標準注文数量は、BOM 計算において固定費を償却するための既定の会計ロットサイズとして機能します。 会計ロット サイズは、指定した場合は、注文数量の倍数も反映します。
-   品目の BOM 計算グループに埋め込まれている警告条件により、潜在的問題を BOM 計算で特定できます。 1 例として、製造品目に BOM や工順がない場合がそうです。 適用された警告状態は、BOM 計算を開始するときに上書きできます。

標準原価 BOM 計算では、次の部品表情報が使用されます。
-   BOM バージョン : 製造品目に割り当てられた BOM バージョンには、有効期間 (開始日と終了日) が設定され、さらに、承認と有効というステータスがあります。 部品表バージョンは、全社的なバージョンとサイト固有のバージョンのどちらも使用でき、オプションで数量の区切り点を反映できます。
-   BOM 明細行品目数量 : 通常、コンポーネントが必要とする数量は可変ですが、定数にすることができます。 コンポーネントの数量は、通常は 1 個の親品目の生産に対して表現されますが、小数点の精度問題を処理するために、100 個または 1000 個単位で表現できます。 コンポーネント数量は測定に基づいて計算することもできます。
-   BOM 明細行品目仕損 : コンポーネントには、予定された仕損数量 (可変または固定) を設定できます。
-   BOM 明細行品目有効日 : コンポーネントには、有効期間 (開始日と終了日) を設定できます。
-   BOM 明細行品目生産タイプ : 固定費を償却するための原価ロットサイズは、BOM 計算数量と受注生産展開モードを反映します。これは、BOM 計算では、製造コンポーネントは、標準注文数量ではなく、正確な数量が生産されることが前提になるためです。
-   製造コンポーネントの下位 BOM : 製造コンポーネントには、オプションで BOM バージョンを指定できます。指定された BOM バージョンは、BOM 計算の中で、品目の現在有効な BOM バージョンの代わりに使用されます。
-   製造コンポーネントの下位工順 : 製造コンポーネントには、オプションで工順バージョンを指定できます。指定された工順バージョンは、BOM 計算の中で、品目の現在有効な工順バージョンの代わりに使用されます。
-   工程番号と仕損率の影響 − 工程番号はコンポーネントを特定の工程にリンクし、工程には仕損率を割り当てることができます。 このリンクにより、コンポーネントの要求数量の複数の工程における仕損率と累積仕損率を BOM 計算で算出できます。
-   原価計算における BOM 明細行品目の無視 : BOM 計算でコンポーネントを無視できます。

標準原価 BOM 計算では、運営リソース情報を使用します。
-   時間原価 − 運営リソースに関連付けられた時間原価は、段取り時間と実行時間に割り当てられた原価カテゴリとして表します。 これらの原価カテゴリは、リソース グループと運営リソースに対して識別する必要があります。 原価カテゴリに関連付けられた時間原価は、サイト固有であっても、全社的であってもかまいません。
-   単位原価 − 一部の製造環境では出力単位ごとに運営リソース コストを割り当てます。これは、数量に対するさまざまなコスト カテゴリとして表します。 たとえば、数量関連原価は、労務の出来高レートを反映し、塗料の製造業者は出荷 1 ガロンごとの運用リソース コストを割り当てます。
-   工順工程における運営リソース情報の上書き − 原価カテゴリに関するリソース情報は工程に継承され、工程で上書きされることがあります。 BOM 計算では、工順工程で指定された原価カテゴリ情報が使用されます。
-   原価カテゴリの原価グループ : 原価カテゴリに割り当てられた原価グループは、製造品目の算出原価における原価区分の基準を提供します。 たとえば、複数の原価グループを使用して、機械と労務、または段取り時間と実行時間に関連付けられた算出原価を区分できます。

標準原価 BOM 計算では、次の工順情報が使用されます。
-   工程バージョン : 製造品目に割り当てられた工程バージョンには、有効期間 (開始日と終了日) が設定され、さらに、承認と有効というステータスがあります。 工程バージョンはサイト固有である必要があり、オプションで数量の区切り点を反映できます。
-   工程時間 : この時間は、実行時間または段取り時間に対して指定できます。 時間は、通常は 1 個の親品目の生産に対して表現されますが、小数点の精度問題を処理するために、100 個または 1000 個単位で表現できます。
-   二次リソースの工程時間 : 二次リソースには、一次リソースと同じ工程番号が設定され、同じ工程時間が割り当てられます。 たとえば、ある工程では、一次リソースとして機械を、二次リソースとして労務とツールを必要とします。
-   工順工程の仕損率 − BOM では、複数の工程における仕損率と累積仕損率を計算します。 これは、工程番号にリンクされている、工順工程の所用時間と、コンポーネントの必要量に適用します。
-   工程の原価カテゴリ − 原価カテゴリに関する運用リソース情報は、工程に継承され、工程で上書きされることがあります。 BOM 計算では、工程で指定された原価カテゴリ情報が使用されます。

標準原価 BOM 計算では、次の製造間接費情報が使用されます。
-   割増金 : 割増金計算式は、労務などの特定の原価グループに関係する値の割合 (100% など) を反映します。
-   レート : レート計算式は、労務などの特定の原価グループに関係する単位あたりの金額 (時間あたり USD 10.00 など) を反映します。
-   時間ベースの間接費と材料ベースの間接費 : 製造間接費は、工程または材料コンポーネントに関係させることができます。

標準原価 BOM 計算では、次の原価バージョン情報が使用されます。
-   原価タイプ : 原価バージョンには、標準原価を格納する必要があります。 標準原価を使用する BOM 計算には、さまざまな制約が適用されます。 たとえば、これらの制約は、単位原価に雑費を含める必要があることや、BOM 計算の展開モードは単一レベルでなければならないことを指定します。
-   要求された予備原則 : 原価バージョンでは、指定した原価バージョンや有効な原価レコードの使用などの予備原則を使用することを要求できます。 要求された予備原則は、通常は、原価を更新するための 2 バージョン アプローチにおける差分更新を表す原価バージョンに適用されます。
-   保留中の原価に対するブロック フラグ : ブロック フラグは、製造品目に対する保留中の原価の BOM 計算を禁止できます。
-   指定された開始日 : 指定された開始日は、原価バージョンが関係するすべての BOM 計算で既定の計算日として機能します。
-   指定されたサイト : 指定されたサイトは、BOM 計算を単一のサイトに制限します。
-   原価バージョンの内容には原価が含まれている必要がある : 内容には、原価が含まれている必要があります。 オプションで、製造品目の推奨販売価格を計算するための販売価格を含めることができます。

BOM 計算を開始するときに、さまざまな情報ソースを指定できます。 サイト、計算日、原価バージョンなどを指定できます。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]