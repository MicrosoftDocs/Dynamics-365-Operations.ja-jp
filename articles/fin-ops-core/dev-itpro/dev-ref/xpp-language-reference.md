---
title: X++ 言語リファレンス
description: このトピックでは、X++ のプログラミング ガイドを提供します。
author: RobinARH
ms.date: 06/20/2017
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.custom: intro-internal
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07746cc3d879f9757bd6079a693ee618ad0a68f78f996563ece98e0099cc34d5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751477"
---
# <a name="x-language-reference"></a>X++ 言語リファレンス

[!include [banner](../includes/banner.md)]

X++ は、エンタープライズ リソース プランニング (ERP) プログラミングおよびデータベース アプリケーションで使用する、オブジェクト指向、アプリケーション対応、およびデータ対応のプログラミング言語です。 次の表で強調表示された幅広いシステム プログラミング領域のシステム クラスを提供します。

| X++ 言語機能 | 説明 |
|-----|-----|
| クラス              | システム クラスに加えて、さまざまなタイプの業務プロセスを管理するためのアプリケーション クラスもあります。 クラスのリフレクションがサポートされます。 |
| テーブル               | X++ のプログラマーは、リレーショナル テーブルにアクセスできます。 X++ には標準 SQL の大部分のキーワードと一致するキーワードが含まれます。 テーブルのリフレクションがサポートされます。 |
| ユーザー インターフェイス       | フォームやレポートなどのユーザー インターフェイス項目の操作。|
| 推奨チェック | X++ コードはコンパイル中に構文エラーがチェックされます。 コンパイル プロセスでは、ベスト プラクティス チェックも実行されます。 ベスト プラクティスの違反によりコンパイラのメッセージを生成できます。|
| ガベージ コレクション   | X++ ランタイム実行エンジンには、メモリ領域を再利用できるように、参照されなくなったオブジェクトを破棄する自動メカニズムがあります。 |
| 相互運用性     | X++ および C\# (または他の .NET Framework 言語) で書かれたクラス間の相互運用性がサポートされます。                                      |
| ファイルの操作    | ファイル入力および出力はサポートされており、XML 構築および解析を含みます。 |
| 取立          | 動的配列はサポートされ、X++ にはいくつかのコレクション オブジェクトが含まれています。|

X++ 言語プログラミング ガイドは、以下のセクションに分かれています。 

+ [変数とデータ型](xpp-variables-data-types.md)
+ [ステートメント、ループ、および例外処理](xpp-conditional.md)
+ [演算子](xpp-operators.md) 
+ [クラスおよびメソッド](xpp-classes-methods.md) 
+ [データの選択と操作](xpp-data/xpp-data-home-page.md)
+ [マクロ](xpp-macros.md) 
+ [属性クラス](xpp-attribute-classes.md) 

## <a name="additional-resources"></a>追加リソース
+ [X++ 構文](xpp-syntax.md)
+ [X++ と C# の比較](xpp-cs-comparison.md)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]