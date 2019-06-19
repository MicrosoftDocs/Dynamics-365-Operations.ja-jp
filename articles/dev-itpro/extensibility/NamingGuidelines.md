---
title: 拡張機能の名前付けのガイドライン
description: このトピックでは、拡張機能の名前付けガイドラインについて説明します。
author: LarsBlaaberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: acc8d70394c41cba51f8a7cebb75b8750ea72651
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550924"
---
# <a name="naming-guidelines-for-extensions"></a>拡張機能の名前付けのガイドライン

[!include [banner](../includes/banner.md)]

## <a name="naming-model-elements"></a>モデル要素に名前を付ける
モデル内の要素には、インストール時にすべてのモデルで一意の名前を付ける必要があります。 すべての潜在的なモデルの場合、実装時に共にインストールされるモデルは不明であり、すべての要素名にはソリューション固有の接頭辞が含まれる必要があります。 モデルに複数のソリューションが含まれている場合は、さまざまな接頭語によって、モデルでは、各ソリューションを識別できます。

接頭語の選択は、他の関係者からの他のモデルの要素に同じ接頭語が選択されるというリスクを最小限に抑えるように慎重に行う必要があります。
モデルに要素の名前を付けるときに接頭語を含めると、モデルが他のモデルと一緒に後でインストールされるときに名前の競合のリスクが大幅に引き下げられます。

他のモデル内の機能を拡張するとき、拡張される要素には接頭語がすでに含まれています。 接頭語を拡張要素に追加し、それぞれの後に複数の接頭語を続けずに、拡張要素に名前を付けるときに接頭語やその他の語句、省略形をインフィックスとして含める必要があります。

拡張機能の特定の名前付けに関する詳細を次に示します。

## <a name="naming-extensions"></a>拡張機能に名前を付ける

拡張要素、すなわちテーブル拡張子、ビュー拡張子、フォーム拡張子など、他のモデルの拡張子と競合のリスクを最小限にする一意の名前を付ける必要があります。現在と将来の両方で行なえます。 競合のリスクを最小限に抑えるために、名前には、拡張機能を他のモデル内の同じ要素の他の拡張機能と区別するための用語、省略形、または接中辞が含まれている必要があります。

- **必ず**拡張要素が存在するモデルの名前、または拡張子が関連付けられている接頭辞のいずれかを含めます。
WHS 接頭語を使用してその他すべての要素の名前を付ける HCMWorker テーブルの拡張クラスは、ウェアハウジング モジュールにより HCMWorker.WHSExtension という名前を付けることができます。 モジュール内の他の要素に名前を付けるために使用される接頭語は、接中辞として挿入されます。
ApplicationSuite の ContactPerson テーブルの拡張子は、ApplicationSuite モデルから ContactPerson テーブルへすべての拡張機能を含む拡張子である場合、ContactPerson.ApplicationSuiteExtension という名前を付けることができます。

- **必ず**末尾に Extension という用語を付けます。
InventLocation テーブルの拡張は、次のパターン InventLocation に従う必要があります。<Model>拡張

- 拡張子に <ElementBeingExtended>.Extension のような簡単な名前を**つけないで**ください。
競合のリスクが高すぎるため、InventLocation テーブルの拡張子は InventLocation.Extension という名前を付けることができません。


## <a name="naming-extension-classes"></a>拡張クラスの名前を付ける

強化を介して拡張可能なテーブル、クラス、または他の要素ロジックを拡張するために使用される拡張子クラスには、すべてのモデルのすべてのタイプで一意の名前を付ける必要が今後もあります。

拡張クラスに拡張されている型の名前を含めることは望ましいですが、同時に、その名前にその他の型とクラスを区別する用語、省略形または接頭語も含める必要があります。

- **必ず**拡張クラスの名前を強化された型の名前で開始し、_Extension という用語で終了します。
ContactPerson テーブルを増補する拡張クラスは、ContactPerson という名前で開始し、_Extension、および ContactPersonWHS_Extension などで終了する必要があります

- **必ず**拡張要素が存在するモデルの名前、または拡張子が関連付けられている接頭辞のいずれかを含めます。
WHS 接頭語を使用してその他すべての要素の名前を付ける ContactPerson テーブルを拡張する拡張クラスは、ウェアハウジング モジュールにより ContactPersonWHS_Extension という名前付けることができます。 モジュール内の他の要素に名前を付けるために使用される接頭語は、接中辞として挿入されます。
ApplicationSuite モデルの ContactPerson テーブル を増補する拡張クラスは、拡張クラス ApplicationSuite の ContactPerson テーブルへすべての拡張機能を含む拡張をしている場合、ContactPersonApplicationSuite 拡張子という名前にすることができます。

- 拡張子に <ElementBeingExtended>_Extension のような簡単な名前を**つけないでください**。
競合のリスクが高すぎるため、InventLocation テーブルを増補する拡張クラスは InventLocation_Extension という名前を付けることができません。

## <a name="naming-fields-field-groups-indexes-relations-and-other-metadata-nodes-in-extension-elements"></a>拡張要素のフィールド、フィールド グループ、インデックス、関係およびその他のメタデータ ノードに名前を付ける

拡張要素のフィールド、インデックス、関係、およびその他のメタデータ要素は、その他の拡張要素と同じように、拡張されている両方の要素間で一意である必要もあります。
したがって、これらのメタデータ ノードには、モデル間の競合のリスクを制限する用語、省略形または接頭辞も含める必要があります。

- **必ず**メタデータ ノードの名前の先頭に接頭語、用語、または省略形を含めます。
承認する作業者の外部キー フィールドは、テーブルの拡張機能の一部として追加され、WHS がホスティング モデル内の他の要素の専用接頭語の 1 つとして想定した場合 WHSApprovingWorker という名前を付けることができます。


## <a name="naming-members-in-extension-classes"></a>拡張クラス内のメンバーの名前を付ける
クラス レベルの変数、および拡張クラスのメソッドには、拡張される型全体で一意の名前と、同じタイプを拡張する他のすべての拡張クラスを指定する必要があります。

- **必ず**メンバー名の先頭に接頭辞、用語、または省略形を含めます。
WHS がモデル内の他の要素で使用される接頭語の 1 つである場合、承認する作業者クラス レベルの変数に WHSApprovingWorker という名前を付けることができます。
WHS がホスティング モデルの他の要素で使用される接頭語の 1 つである場合、approveWork メソッドは WHSApproveWork という名前を付けることができます。

