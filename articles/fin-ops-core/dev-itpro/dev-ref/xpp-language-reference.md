---
title: X++ 言語リファレンス
description: このトピックでは、X++ のプログラミング ガイドを提供します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 72181
ms.assetid: fe5d3cdd-8b3d-4967-98a2-dadada18a421
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eba91c78f1f2fb0b1d2a42d9b6fd575c54d8e119
ms.sourcegitcommit: c3bc5dd007d9f063631232497bd4cda9214e2e5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872431"
---
# <a name="x-language-reference"></a>X++ 言語リファレンス

[!include [banner](../includes/banner.md)]

X++ は、エンタープライズ リソース プランニング (ERP) プログラミングおよびデータベース アプリケーションで使用する、オブジェクト指向、アプリケーション対応、およびデータ対応のプログラミング言語です。 次の表で強調表示された幅広いシステム プログラミング領域のシステム クラスを提供します。

| X++ 言語属性 | 説明 |
|-----|-----|
| **クラス**                 | システム クラスに加えて、さまざまなタイプの業務プロセスを管理するためのアプリケーション クラスもあります。 クラスのリフレクションがサポートされます。            |
| **テーブル**                  | X++ のプログラマーは、リレーショナル テーブルにアクセスできます。 X++ には標準 SQL の大部分のキーワードと一致するキーワードが含まれます。 テーブルのリフレクションがサポートされます。 |
| **ユーザー インターフェイス**          | フォームやレポートなどのユーザー インターフェイス項目の操作。|
| **推奨チェック**    | X++ コードはコンパイル中に構文エラーがチェックされます。 コンパイル プロセスでは、ベスト プラクティス チェックも実行されます。 ベスト プラクティスの違反によりコンパイラのメッセージを生成できます。|
| **ガベージ コレクション**      | X++ ランタイム実行エンジンには、メモリ領域を再利用できるように、参照されなくなったオブジェクトを破棄する自動メカニズムがあります。 |
| **相互運用性**        | X++ および C\# (または他の .NET Framework 言語) で書かれたクラス間の相互運用性がサポートされます。                                                       |
| **ファイルの操作**       | ファイル入力および出力はサポートされており、XML 構築および解析を含みます。 |
| **取立**             | 動的配列はサポートされ、X++ にはいくつかのコレクション オブジェクトが含まれています。|

X++ 言語プログラミング ガイドは、以下のセクションに分かれています。 
+ [X++ 属性クラス](xpp-attribute-classes.md) 
+ [X++ クラスおよびメソッド](xpp-classes-methods.md) 
+ [X++ データの選択と操作](xpp-data-query.md) 
+ [X++ マクロ](xpp-macros.md) 
+ [X++ 演算子](xpp-operators.md) 
+ [X++ ステートメントおよびループ](xpp-statements-loops.md)
+ [X++ の変数とデータ型](xpp-variables-data-types.md)

## <a name="additional-resources"></a>その他のリソース
+ [X++ 構文](xpp-syntax.md)
+ [X++ と C# の比較](xpp-cs-comparison.md)


