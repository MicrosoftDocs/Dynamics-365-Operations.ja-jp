---
title: データ エンティティの動作プロパティ
description: この記事では、そのエンティティのデータ ソースであるテーブルまたはビューのプロパティ値をオーバーライドさせるデータ エンティティのプロパティについて説明します。
author: peakerbl
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65160e8064a92a3d5f27b10caa3a1d07ef4b98cd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897161"
---
# <a name="behavioral-properties-on-data-entities"></a>データ エンティティの動作プロパティ

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

すべてのデータ エンティティには、そのエンティティのデータソースであるテーブルまたはビューの同じプロパティ値をオーバーライドできるようにするプロパティがあります。 選択内容は、エンティティの動作に影響します。 次の表では、最初の列に、この記事で説明したプロパティが一覧表示されています。 一番上の行には、エンティティ デザイナーでプロパティが見つかったレベルが表示されます。 レベルは、精度の細かい順に一覧表示されます。データ ソース レベルはエンティティ レベルよりも細かく、フィールド レベルほどは細かくはありません。

|  &nbsp;           | エンティティ レベル | データ ソース レベル | フィールド レベル |
|-------------------|--------------|-------------------|-------------|
| ReadOnly          | 適用      | 適用           | .           |
| AllowEdit         | .            | .                 | 適用     |
| AllowEditOnCreate | .            | .                 | 適用     |
| 必須         | .            | .                 | 適用     |

## <a name="entity-level"></a>エンティティ レベル
データ エンティティのデザイナーで、ルート ノードの名前をクリックすると、**プロパティ** ウィンドウに **読み取り専用** プロパティがあります。 次のテーブルは、このプロパティの **Yes** と **No** 値の間の動作上の相違点を示しています。

<table>
<thead>
<tr>
<th>グループ化</th>
<th>プロパティ名</th>
<th>表示名</th>
<th>値</th>
<th>既定</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr>
<td>動作</td>
<td>IsReadOnly</td>
<td>読み取り専用です。</td>
<td>いいえ、はい</td>
<td>無</td>
<td><ul>
<li><strong>いいえ:</strong> エンティティのデザイナー内の個別のデータ ソース ノードが <strong>IsReadOnly</strong> = <strong>はい</strong>に設定されて<em>いない限り</em>、データ変更操作 (CUD) <em>は</em>許可されます。</li>
<li><strong>はい:</strong> エンティティのデザイナ内の個々のデータソースノードの <strong>IsReadOnly</strong> 設定に関係なく、読み取り操作のみが許可されます。</li>
</ul></td>
</tr>
</tbody>
</table>

主にエクスポートに使用されるエンティティに対して、**IsReadOnly** を **はい** に設定します。

## <a name="data-source-level"></a>データ ソース レベル
データ エンティティに 3 つのデータ ソースがある場合は、その中から 2 つではなく、1 つのデータ ソースのデータを変更するために、エンティティを使用するためのプロセスを許可する場合があります。 読み取り専用データ ソースは参照目的で使用することができます。 エンティティ デザイナーを使用すると、この非常に制度の高い制御を達成することができます。 エンティティの **メタデータ**&gt;**データ ソース** ノードで、エンティティ ノードを選択すると、その 1 つのデータソースの **IsReadOnly** プロパティの値を設定できます。 次のテーブルでは、データ ソース レベルの **IsReadOnly** 設定とエンティティ レベルの相互作用について説明します。

<table>
<thead>
<tr>
<th>グループ化</th>
<th>プロパティ名</th>
<th>表示名</th>
<th>値</th>
<th>既定</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr>
<td>動作</td>
<td>IsReadOnly</td>
<td>読み取り専用です。</td>
<td>いいえ、はい</td>
<td>無</td>
<td><ul>
<li><strong>いいえ:</strong> エンティティ レベルで <strong>IsReadOnly</strong> が<strong>はい</strong>に設定されて<em>いない限り</em>、データ変更操作 (CUD) <em>は</em>データ ソースで許可されます。</li>
<li><strong>はい:</strong> エンティティの <strong>IsReadOnly</strong> 設定に関係なく、操作のみが許可されます</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="field-level"></a>フィールド レベル
フィールド レベルにおいて、**AllowEdit** と **AllowEditOnCreate** プロパティは **IsReadOnly** プロパティの代わりに利用可能です。 2 つの **許可** プロパティには、3 番目の利用可能な値として **自動** が含まれています。 **自動** 値は、基になっているテーブルのフィールドにある値を継承します。

> [!NOTE]
> **自動** の値は、計算フィールドや仮想フィールドなどのマップされていないフィールドでは使用できません。

<table>
<thead>
<tr>
<th>グループ化</th>
<th>プロパティ名</th>
<th>表示名</th>
<th>先頭値</th>
<th>既定</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr>
<td>動作</td>
<td>AllowEditOnCreate</td>
<td>作成時の編集を許可</td>
<td>自動、いいえ、はい</td>
<td>自動</td>
<td><ul>
<li><strong>自動:</strong> 基になるテーブル フィールドから、プロパティを継承します。
<blockquote>[!NOTE] <strong>自動</strong>の値は、計算フィールドや仮想フィールドなどのマップされていないフィールドでは使用できません。</blockquote>
</li>
<li><strong>いいえ:</strong> ユーザーは、このフィールドのデータを新しいレコードで変更することはできません。</li>
<li><strong>はい:</strong> ユーザーは、このフィールドのデータを新しいレコードに対して変更することができます。</li>
</ul>
この動作は、すべてのコンシューマー (X++、OData など) に適用されます。
<blockquote>[!IMPORTANT] <strong>いいえ</strong>および<strong>はい</strong>の値は、基になるテーブル内のフィールドの設定を上書き<em>しません</em>。</blockquote></td>
</tr>
<tr>
<td>動作</td>
<td>AllowEdit</td>
<td>編集を許可</td>
<td>自動、いいえ、はい</td>
<td>自動</td>
<td>動作は、<strong>AllowEditOnCreate</strong> の動作と同じですが、作成されている新しいレコードではなく、<em>既存の</em>レコードへの更新に適用されます。 この動作は、すべてのコンシューマー (X++、OData など) に適用されます。</td>
</tr>
<tr>
<td>動作</td>
<td>必須</td>
<td>必須</td>
<td>自動、いいえ、はい</td>
<td>自動</td>
<td><strong>自動:</strong> 基になるテーブル フィールドから、プロパティを継承します。 この動作は、すべてのコンシューマー (X++、OData など) に適用されます。
<blockquote>[!IMPORTANT] <strong>いいえ</strong>および<strong>はい</strong>の値は、基になるテーブル内のフィールドの設定を上書き<em>しません</em>。</blockquote></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
