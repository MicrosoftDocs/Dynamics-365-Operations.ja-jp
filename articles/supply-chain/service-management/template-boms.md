---
title: テンプレート BOM
description: テンプレート BOM (部品表) は、定期的にサービスされるサービス対象のコンポーネントの標準化された一覧を提供します。
author: ShylaThompson
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b514aeed48180bb1b14be8b3d95d55d44d2ca8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824331"
---
# <a name="template-boms"></a>テンプレート BOM    

[!include [banner](../includes/banner.md)]


テンプレート BOM (部品表) は、定期的なサービス対象のコンポーネントの一覧を標準化された形式で表示します。 テンプレート BOM に記載されるコンポーネントは、サービス対象の個々のサブコンポーネントを表します。 サービス対象にテンプレート BOM を適用して、サービス対象について交換されたサブコンポーネントのレコードを保持することができます。

サービス合意またはサービス注文にテンプレート BOM を適用するには、サービス対象の関係に関連付けます。


> [!NOTE]
> <P>1 つのサービス対象に適用できるテンプレートは 1 つだけです。</P>

## <a name="create-a-template-bom"></a>テンプレート BOM の作成

次の表は、テンプレート BOM を作成するために使用できるさまざまな方法について説明しています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>方法</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>生産</p></td>
<td><p>テンプレート BOM は製造オーダーに基づきます。 このオプションは、実稼働環境で使用している場合のみ適用できます。 メリットは、品目を構成するコンポーネントの最新の詳細なリストを維持できることです。</p></td>
</tr>
<tr class="even">
<td><p>品目 BOM</p></td>
<td><p>テンプレート BOM は、品目 BOM に基づきます。 品目 BOM は、生産 BOM とは異なり、品目を構成するコンポーネントの静的な一覧です。</p></td>
</tr>
<tr class="odd">
<td><p>既存のテンプレート</p></td>
<td><p>このテンプレートは、既存のテンプレート BOM に基づきます。</p></td>
</tr>
<tr class="even">
<td><p>手持在庫</p></td>
<td><p>サービス対象について頻繁に交換される予備部品がわかっている場合は、手動でテンプレート BOM を作成できます。 この方法を使用すると、テンプレートに含まれるコンポーネントが作業場所の実際の要件を反映していることの確認が容易になります。</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>サービス合意またはサービス注文へのテンプレート BOM の適用

テンプレート BOM を、サービス合意、サービス注文、またはその両方に適用できます。 一般にサービス合意には、顧客との長期的な関係があります。 サービス BOM に記録される交換の履歴は、サービス合意にとって有用なデータです。

サービス対象へのサービスの実行履歴を記録するサービス注文にテンプレート BOM を適用することもできます。

## <a name="copy-the-history-of-a-service-bom"></a>サービス BOM の履歴のコピー

サービス BOM 明細行の履歴は、複数のサービス合意間でコピーできます。 サービス合意間でサービスの履歴をコピーすることによって、品目の交換の記録を維持できます。

**例**

顧客の車に対して 3 年間のサービス合意を結びました。 この期間中に、顧客は会社が提供する上質のサービスに慣れてきます。 したがって、契約が切れた後、顧客は新しい合意の設定を望みます。 この時点で、会社に有利な合意を交渉できます。 交換されたコンポーネントに関する記録が将来役立つかもしれないので、サービス BOM の履歴を新しい合意にコピーします。

## <a name="modify-the-template-bom"></a>テンプレート BOM の変更

サービス対象に関連付けられていないテンプレート BOM の明細行は変更または削除できます。 テンプレート BOM をサービス対象に関連付けた後に、初めて BOM のローカル バージョンを変更できます。 テンプレート BOM のローカル バージョンの設定をコピーする場合は、ローカル バージョンに基づいて新しいテンプレート BOM を作成できます。 詳細については、[サービス BOM の変更](modify-service-bom.md) を参照してください。

BOM 内の品目を交換する場合は、BOM デザイナで BOM 明細行の交換を登録できます。 必要に応じて、交換オブジェクトのサービス注文明細行を作成できます。 サービス注文明細行を作成すると、交換品目の請求書を作成できます。 交換のためのサービス注文明細行を作成しない場合、サービス対象の履歴を追跡するために交換登録が維持されます。

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>BOM 明細行の情報の表示方法の変更

すべてのテンプレート BOM とサービス BOM の BOM 明細行の情報の表示方法を変更できます。 すべてのテンプレート BOM とサービス BOM に変更が適用されます。 これには、サービス対象に関連付けられている明細行も含まれます。

## <a name="set-up-number-sequences-for-template-boms"></a>テンプレート BOM 用の番号順序の設定

テンプレート BOM を使用するには、2 つの番号順序を設定する必要があります。 テンプレート BOM に 1 つの番号順序を、BOM 履歴行番号にもう 1 つの番号順序を設定します。


> [!NOTE]
> <P>番号順序が使用され、ID を必要とするレコードに割り当てます。 テンプレート BOM または BOM 履歴行番号に番号順序を割り当てるには、その前に、番号順序コードを設定する必要があります。</P>


## <a name="set-up-number-sequences"></a>番号順序の設定

1.  **Number sequences** リスト ページで、テンプレート BOM と BOM 履歴行番号の番号順序を作成します。 

2.  **サービス管理** \> **設定** \> **サービス管理パラメーター** の順にクリックします。

3.  **番号順序** をクリックし、**番号順序** フォームで作成した番号順序の参照に対する番号順序コードを選択します。

4.  フォームを閉じて、変更を保存します。


> [!NOTE]
> <P>BOM 履歴行番号はシステムによって使用され、BOM 履歴トランザクションをサービス合意またはサービス注文に関連付けます。 この番号は、ユーザー インターフェイスには表示されません。</P>



## <a name="see-also"></a>参照

[テンプレート BOM の作成](create-template-bom.md)

[対象関係でのテンプレート BOM の管理](manage-template-boms-on-object-relations.md)

[サービス BOM の変更](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]