---
title: API、クラス、テーブルのリファレンス
description: この記事では、Visual Studio および Microsoft Learn で API ドキュメントを見つける場所について説明します。
author: josaw1
ms.date: 07/23/2019
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac158e07353db85d9cc58cc5038a82321fa9174d
ms.sourcegitcommit: d3f7a56eaf788d223ece4cedac4a319eaf5f6112
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/19/2022
ms.locfileid: "9538545"
---
# <a name="api-class-and-table-resources"></a>API、クラス、テーブルのリファレンス

[!include [banner](../includes/banner.md)]

この記事では、Visual Studio および Microsoft Learn で API ドキュメントを見つける場所について説明します。

## <a name="application-classes-and-tables"></a>アプリケーション クラスおよびテーブル

### <a name="application-class-and-table-documentation-is-in-visual-studio"></a>アプリケーション クラスおよびテーブル ドキュメントは Visual Studio にあります

Microsoft Visual Studio のアプリケーション クラスについては、ドキュメントを参照してください。 アプリケーション エクスプローラーでクラス名を検索し、そのコードを表示します。 クラスに関する追加のメタデータは **プロパティ** ウィンドウ内にあります。 [技術参照レポート](/dynamics/s-e/global/axtechrefrep_61) 内のすべてのテーブルの一覧をダウンロードすることができます。 詳細については、[標準データ エンティティに関する情報の検索](../data-entities/data-entities-report.md) を参照してください。

### <a name="programming-with-application-tables-and-classes"></a>アプリケーション テーブルおよびクラスを使用したプログラミング

アプリケーション テーブルはアプリケーション クラスと類似していますが、クラスとの違いは次のとおりです。

- テーブルは維持されます。
- テーブル フィールドは、常にパブリックになります。
- テーブルは、ほとんどの場合、実際のオブジェクトに対応します。
- 後で他のテーブルで拡張する場合は、テーブルの定義を消去する必要になる場合があります。

### <a name="design-pattern-of-private-new-in-application-classes"></a>アプリケーション クラスの新規プライベート設計パターン

すべてのアプリケーション クラスはアプリケーション エクスプ ローラー &gt; クラスの下にあります。 クラスにアプリケーション エクスプローラーの **新規** ノードがなくても、すべてのアプリケーション クラスに `new` という名前のコンストラクター メソッドがあります。 クラスに明示的な **新規** ノードがない場合、暗黙的な **新規** メソッドがパブリックになります。 アプリケーション クラスで場合によって使用される設計パターンは、明示的な **新規** コンストラクター メソッドを **プライベート** として宣言します。 その後、**パブリック静的** メソッドを追加して **新規** メソッドを呼び出します。 静的メソッドは、必要に応じてさまざまな条件に基づき、**新規** メソッドの呼び出しを制限または制御できます。

## <a name="system-classes-and-tables"></a>システム クラスおよびテーブル

### <a name="system-api-class-and-table-documentation-in-microsoft-learn"></a>Microsoft Learn のシステム API、クラス、テーブル ドキュメント

[Microsoft Learn](/docs/) ドキュメントで使用可能なアプリケーション エクスプローラーの **システム ドキュメント** の下に、表示されているクラスおよび機能のドキュメント。

## <a name="x-compile-time-functions"></a>X++ コンパイル時関数

[X++ コンパイル時関数](xpp-compile-time-functions.md)

## <a name="x-run-time-functions"></a>X++ ランタイム関数

[X++ ランタイム関数](xpp-string-run-time-functions.md):

- [X++ コンテナー ランタイム関数](xpp-container-run-time-functions.md)
- [X++ ビジネス ランタイム関数](xpp-business-run-time-functions.md)
- [X++ 変換ランタイム関数](xpp-conversion-run-time-functions.md)
- [X++ 日付ランタイム関数](xpp-date-run-time-functions.md)
- [X++ 数学ランタイム関数](xpp-math-run-time-functions.md)
- [X++ リフレクション ランタイム関数](xpp-reflection-run-time-functions.md)
- [X++ セッション ランタイム関数](xpp-session-run-time-functions.md)
- [X++ 文字列ランタイム関数](xpp-string-run-time-functions.md)

## <a name="system-tables"></a>システム テーブル

[システム テーブル](system-tables.md)

## <a name="system-classes"></a>システム クラス

システム クラスのリファレンス ドキュメントは .NET API ブラウザーに含まれています。

[Finance and Operations アプリの API 参照](/dotnet/api/fin-ops-api-landing)

[Microsoft.Dynamics.Ax.Xpp 名前空間](/dotnet/api/microsoft.dynamics.ax.xpp)

[Dynamics.AX.Application 名前空間](/dotnet/api/dynamics.ax.application)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
