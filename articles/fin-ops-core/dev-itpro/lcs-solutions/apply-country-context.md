---
title: 国/地域コンテキストの適用
description: この記事では、ローカライズおよび翻訳要件を満たすために国/地域コンテキストを適用する方法に関する情報を提供します。
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 21681
ms.assetid: d02eee15-bbeb-4e0f-a59f-0313da9334da
ms.openlocfilehash: 9f81816ae173fd36fedac63b135d0f37962261ea
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270751"
---
# <a name="apply-countryregion-context"></a>国/地域コンテキストの適用

[!include [banner](../includes/banner.md)]

ローカライズおよび翻訳向け LCS ソリューション要件の一部として、ローカライズ ISV ソリューション プロバイダーは国/地域コンテキストによって制御できるように、すべての国または地域固有の機能を実装する必要があります。 この記事では、これらの要件を満たすために、国/地域コンテキストを適用する方法について説明します。 この記事では、国コンテキスト プロパティを使用する方法と、どのようなアプリケーション オブジェクトがユーザー インターフェイス要素を制御するのかに関する情報を確認できます。

## <a name="countryregion-specific-functionality"></a>国/地域固有の機能

個々の地域の法律、規制、ビジネス要件への対応を容易にするために、国/地域に固有の機能を使用します。 地理は、国際標準化機構 (ISO) の国/地域コードで識別されている任意の国または地域です。 次のテーブルでは、国/地域固有の機能をコンフィギュレーションするために使用する主要な要素について説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>要素</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>制御されたエンティティ</td>
<td>制御されたエンティティは、その国/地域のコンテキストが制御エンティティの国/地域のコンテキストと一致するかどうかによって、非表示または表示される UI 要素です。 国/地域のコンテキストに基づくメニュー、メニュー項目、フォーム コントロールを非表示にするために、一部の要素で、コントロールされたエンティティに <strong>CountryRegionCodes</strong> プロパティが含まれます。 このプロパティを使用して、要素が表示される国または地域を指定します。 次のアプリケーション オブジェクト ツリー (AOT) 要素で <strong>CountryRegionCodes</strong> プロパティを検索します。
<ul>
<li>拡張データ型</li>
<li>メニューとメニュー項目</li>
<li>列挙と列挙値</li>
<li>テーブルとテーブル フィールド</li>
<li>データ エンティティとデータ エンティティ フィールド</li>
<li>表示と表示フィールド</li>
<li>マップおよびマップ フィールド</li>
<li>フォーム コントロール</li>
<li>タイル</li>
</ul></td>
</tr>
<tr class="even">
<td>制御関係者</td>
<td>制御関係者の役割は、国/地域固有の機能または UI 要素が有効かどうかを判断するために使用されます。 制御関係者は、組織モデルによって定義されます。 例には、法人、顧客、仕入先、銀行、または作業者が含まれます。 既定では、法人が管理関係者として使用されます。 制御の関係者の国/地域のコンテキストでは、コントロールのエンティティの国/地域コンテキストが一致すると、機能または UI 要素が有効になります。 制御関係者の国/地域コンテキストを設定します。 一致する国/地域のコンテキストを持つ制御されたエンティティが表示されます。</td>
</tr>
</tbody>
</table>

## <a name="using-the-countryregioncodes-property"></a>CountryRegionCodes プロパティの使用
制御されたエンティティで国/地域コンテキストを作成するには、**CountryRegionCodes** プロパティで ISO コード値の設定します。 ISO の国および地域コードの一覧は [ISO の Web サイト](https://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm) にあります。 **CountryRegionCodes** プロパティの値を管理関係者の国/地域コンテキストと比較します。 値が一致した場合は、要素が表示されます。 それ以外の場合、表示されません。

> [!TIP]
> **CountryRegionCodes** プロパティに複数の ISO 国および地域コードを追加するには、コンマ区切りのリストを使用します。

## <a name="using-the-legal-entity-as-the-controlling-party"></a>法人を管理関係者として使用
法人のプライマリ住所の **国/地域** 値により、制御側関係者の国/地域コンテキストが決定されます。 **国/地域** フィールドの既定値は、システムのロケールです。 次の図は、法人の基本住所を設定する方法を示しています。 [![LE\_Edit\_address。](./media/le_edit_address-1024x570.jpg)](./media/le_edit_address.jpg)

## <a name="setting-another-party-as-the-controlling-party"></a>別の当事者を管理側の関係者として設定
顧客、銀行、または仕入先などの、別の関係者を制御関係者として使用することができます。 たとえば、特定の国/地域の顧客に対して対象となる機能を有効化する、または特定の国/地域から仕入先の固有の検証を必要とすることができます。 管理者を設定するには、フォーム、コントロール、またはその他の要素の **CountryRegionContextField** プロパティを使用します。 このプロパティを使用すると、管理関係者であるエンティティを選択できます。 既定値は法人です。 次の図は、フィールドに **CountryRegionContextField** プロパティを設定する方法を示しています。 
[![DE\_CountryRegionContextField。](./media/de_countryregioncontextfield.jpg)](./media/de_countryregioncontextfield.jpg) 

この例では、顧客が制御エンティティになります。 顧客の住所が **CountryRegionCodes** フィールドの値と比較され、**GermanSpecifcSetting** フィールドが表示されているかどうかが判別されます。

## <a name="additional-resources"></a>その他のリソース

[ISO コード](https://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm)





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
