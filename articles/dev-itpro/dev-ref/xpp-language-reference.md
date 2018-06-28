---
title: "X++ 言語リファレンス"
description: "このトピックでは、X++ のプログラミング ガイドを提供します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 72181
ms.assetid: fe5d3cdd-8b3d-4967-98a2-dadada18a421
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 3c913f8161ecf9734a60acd3c0c29ac93076ae82
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="x-language-reference"></a>X++ 言語リファレンス

[!include [banner](../includes/banner.md)]

X++ は、Microsoft Dynamics 365 for Finance and Operations がエンタープライズ リソース プランニング (ERP) プログラミングおよびデータベース アプリケーションで使用する、オブジェクト指向、アプリケーション対応、およびデータ対応のプログラミング言語です。 次の表で強調表示された幅広いシステム プログラミング領域のシステム クラスを提供します。

| **X++ 言語属性** | **説明** |
|-----|-----|
| **クラス**                 | システム クラスに加えて、Dynamics 365 for Finance and Operations はさまざまなタイプの業務プロセスを管理するためのアプリケーション クラスも提供します。 クラスのリフレクションがサポートされます。            |
| **テーブル**                  | X++ のプログラマーは Dynamics 365 for Finance and Operations のリレーショナル テーブルにアクセスすることができます。 X++ には標準 SQL の大部分のキーワードと一致するキーワードが含まれます。 テーブルのリフレクションがサポートされます。 |
| **ユーザー インターフェイス**          | フォームやレポートなどのユーザー インターフェイス項目の操作。|
| **推奨チェック**    | X++ コードはコンパイル中に構文エラーがチェックされます。 コンパイル プロセスでは、ベスト プラクティス チェックも実行されます。 ベスト プラクティスの違反によりコンパイラのメッセージを生成できます。|
| **ガベージ コレクション**      | X++ ランタイム実行エンジンには、メモリ領域を再利用できるように、参照されなくなったオブジェクトを破棄する自動メカニズムがあります。 |
| **相互運用性**        | Dynamics 365 for Finance and Operations は、X++ および C\# (または他の .NET Framework 言語) で書かれたクラス間の相互運用性をサポートします。                                                       |
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



