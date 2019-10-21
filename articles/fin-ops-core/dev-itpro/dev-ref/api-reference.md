---
title: API、クラス、テーブルのリファレンス
description: このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。
author: RobinARH
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 63853
ms.assetid: 46e5e47b-2c80-44fd-a7a3-e41884da2f55
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bebe030c4c3281271b663b8497993d3261e932f8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191616"
---
# <a name="api-class-and-table-resources"></a>API、クラス、テーブルのリファレンス

[!include [banner](../includes/banner.md)]

このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。

## <a name="application-classes-and-tables"></a>アプリケーション クラスおよびテーブル

### <a name="application-class-and-table-documentation-is-in-visual-studio"></a>アプリケーション クラスおよびテーブル ドキュメントは Visual Studio にあります

Microsoft Visual Studio 内のアプリケーション クラス用ドキュメントは、アプリケーション エクスプローラーのアプリケーション プログラミング インターフェイス (API) を検索してからコードを表示することにより見つけることができます。 API に関する追加のメタデータは **プロパティ** ウィンドウ内で見つけることができます。 また、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) 内のすべてのテーブルの一覧をダウンロードすることができます。

### <a name="programming-with-application-tables-and-classes"></a>アプリケーション テーブルおよびクラスを使用したプログラミング

アプリケーション テーブルはアプリケーション クラスと類似していますが、クラスとの違いは次のとおりです。

-   テーブルは維持されます。
-   テーブル フィールドは、常にパブリックになります。
-   テーブルは、ほとんどの場合、実際のオブジェクトに対応します。
-   後で他のテーブルで拡張する場合は、テーブルの定義を消去する必要になる場合があります。

### <a name="design-pattern-of-private-new-in-application-classes"></a>アプリケーション クラスの新規プライベート設計パターン

すべてのアプリケーション クラスはアプリケーション エクスプ ローラー &gt; クラスの下にあります。 クラスに AOT の新しいノードがなくても、すべてのアプリケーション クラスに `new` という名のコンストラクター メソッドがあります。 クラスに明示的な新しいノードがない場合、`new` メソッドがパブリックになります。 アプリケーション クラスで場合によって使用される設計パターンは、明示的な `new` コンストラクター メソッドを `private` として宣言します。 その後、`public static` メソッドを追加して `new` メソッドを呼び出します。 必要に応じて、静的メソッドは、さまざまな条件に基づき `new` メソッドの呼び出しを制限または制御できます。

## <a name="system-classes-and-tables"></a>システム クラスおよびテーブル
### <a name="system-api-class-and-table-documentation-is-on-the-microsoft-docs-site"></a>システム API、クラス、およびテーブル ドキュメントが Microsoft ドキュメント サイトにあります

Microsoft docs サイトで使用可能なアプリケーション エクスプローラーの**システム ドキュメント**の下に、表示されているクラスおよび機能のドキュメント。

## <a name="x-compile-time-functions"></a>X++ コンパイル時関数
[X++ コンパイル時関数](xpp-compile-time-functions.md)

## <a name="x-run-time-functions"></a>X++ ランタイム関数
[X++ ランタイム関数](xpp-string-run-time-functions.md):

-   [X++ コンテナー ランタイム関数](xpp-container-run-time-functions.md)
-   [X++ ビジネス ランタイム関数](xpp-business-run-time-functions.md)
-   [X++ 変換ランタイム関数](xpp-conversion-run-time-functions.md)
-   [X++ 日付ランタイム関数](xpp-date-run-time-functions.md)
-   [X++ 数学ランタイム関数](xpp-math-run-time-functions.md)
-   [X++ リフレクション ランタイム関数](xpp-reflection-run-time-functions.md)
-   [X++ セッション ランタイム関数](xpp-session-run-time-functions.md)
-   [X++ 文字列ランタイム関数](xpp-string-run-time-functions.md)

## <a name="system-tables"></a>システム テーブル
[システム テーブル](system-tables.md)

## <a name="system-classes"></a>システム クラス
-   [A クラス](a-classes.md)
-   [B クラス](b-classes.md)
-   [C クラス](c-classes.md)
-   [D クラス](d-classes.md)
-   [E クラス](e-classes.md)
-   [F クラス: FormBuildAnimateControl への FieldBinding](fieldbinding-classes.md)
-   [F クラス: FormBuildFastTabSummarySeparator への FormBuildButtonControl](FormBuildButtonControl-classes.md)
-   [F クラス: FormBuildRealControl への FormBuildFilterPaneControl](FormBuildFilterPaneControl-classes.md)
-   [F クラス: FormButtonSeparatorControl への FormBuildReferenceControl](FormBuildReferenceControl-classes.md)
-   [F クラス: FormControlEventArgs への FormChangeTracker](FormChangeTracker-classes.md)
-   [F クラス: FormFastTabHeaderControl への FormDataObject](FormDataObject-classes.md)
-   [F クラス: FormGridControl への FormFastTabSummarySeparator](FormFastTabSummarySeparator-classes.md)
-   [F クラス: FormIntControl への FormGroupControl](FormGroupControl-classes.md)
-   [F クラス: FormNotifyEventArgs への FormListBoxControl](FormListBoxControl-classes.md)
-   [F クラス: FormRealControl への FormObject](FormObject-classes.md)
-   [F クラス: FormStringControl への FormReferenceControl](FormReferenceControl-classes.md)
-   [F クラス: FormWindowControl への FormTabControl](FormTabControl-classes.md)
-   [G クラス](g-classes.md)
-   [H クラス](h-classes.md)
-   [I クラス](i-classes.md)
-   [J クラス](j-classes.md)
-   [K クラス](k-classes.md)
-   [L クラス](l-classes.md)
-   [M クラス](m-classes.md)
-   [N クラス](n-classes.md)
-   [O クラス](o-classes.md)
-   [P クラス](p-classes.md)
-   [Q クラス](q-classes.md)
-   [R クラス](r-classes.md)
-   [S クラス](s-classes.md)
-   [T クラス](t-classes.md)
-   [U クラス](u-classes.md)
-   [V クラス](v-classes.md)
-   [W クラス](w-classes.md)
-   [X クラス](x-classes.md)






