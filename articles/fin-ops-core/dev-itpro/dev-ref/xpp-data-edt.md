---
title: X++ 拡張データ型
description: この記事では、X++ の拡張データ型について説明します。
author: RobinARH
ms.date: 06/17/2019
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7528d58cd8d8ab038291bd58ba90b28949242aa2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867207"
---
# <a name="x-extended-data-types"></a>X++ 拡張データ型

[!include [banner](../includes/banner.md)]

この記事では、X++ の拡張データ型について説明します。 

*拡張データ型* は **ブール**、**int**、**int64**、**実数**、**str**、および **日付** プリミティブ データ型、および **コンテナー** 複合型に基づくユーザー定義型です。 EDT はプリミティブ データ型または補助名および追加のプロパティを持つコンテナーです。 たとえば、文字列を基準にして、**名前** という新しい EDT を作成することができます。 新しい EDT は、開発環境の変数とフィールド宣言で使用することができます。 

また、EDT を他の EDT の基準にすることができます。 EDTs は、標準的なデータ型ですが、特定の名前および追加のプロパティがあります。 EDTs は、それらが基づいている標準データ型と同じ値とタイプ[換算](xpp-conversion-run-time-functions.md)を適用します。 EDT の利点を次に示します。

-   変数は意味のあるデータ型を持つため、コードは読みやすくなります。 たとえば、データ型は **str** の代わりに **名前** です。
-   EDT に設定するプロパティは、そのタイプのすべてのインスタンスで使用されます。 したがって、EDT は作業を減らし、一貫性を促進するのに役立ちます。 たとえば、勘定番号 (**AccountNum** データ型) には、システム全体で同じプロパティがあります。
-   EDT の階層を作成することができます。 EDT は、親から適切なプロパティを継承でき、その他のプロパティを変更することができます。 たとえば、**ItemCode** データ型が、**MarkupItemCode** および **PriceDiscItemCode** データ型の基準として使用されます。

## <a name="create-an-edt"></a>EDT の作成

この機能は、言語コンストラクトとして実装されていません。 EDT を作成するには、次の手順を実行します。

1.  ソリューション エクスプローラーで、プロジェクトを右クリックして **追加** をポイントしてから **新しい項目** をクリックします。
2.  **新しい項目の追加** ダイアログ ボックスで、**インストール済み** を選択してから左ウィンドウの **アーティファクト** を選択します。
3.  中央ウィンドウで、作成する EDT タイプを選択します。
4.  名前を入力し、次に **追加** をクリックします。

## <a name="edt-example"></a>EDT 例

```xpp
public void EdtMethod()
{
    // Example of declaring EDT variables where
    // a UserGroupID (integer) variable is declared and initialized to 1.
    UserGroupID groupID = 1;

    // An Amount (real) variable is declared.
    Amount currency;
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]