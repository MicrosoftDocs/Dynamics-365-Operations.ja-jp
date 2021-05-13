---
title: API、クラス、テーブルのリファレンス
description: このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。
author: RobinARH
ms.date: 07/23/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 63853
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 149e524c550f810d514b548e9cb0ea65ba28d81f
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923255"
---
# <a name="api-class-and-table-resources"></a>API、クラス、テーブルのリファレンス

[!include [banner](../includes/banner.md)]

このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。

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

### <a name="system-api-class-and-table-documentation-is-on-the-microsoft-docs-site"></a>システム API、クラス、およびテーブル ドキュメントが Microsoft ドキュメント サイトにあります

Microsoft docs サイトで使用可能なアプリケーション エクスプローラーの **システム ドキュメント** の下に、表示されているクラスおよび機能のドキュメント。

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

[Microsoft.Dynamics.Ax.Xpp 名前空間](/dotnet/api/microsoft.dynamics.ax.xpp)

[Dynamics.AX.Application 名前空間](/dotnet/api/dynamics.ax.application)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]