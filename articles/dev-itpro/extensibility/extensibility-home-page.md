---
title: "拡張機能のホーム ページ"
description: "このトピックでは、拡張性に関するトピックへのリンクを提供します。"
author: FrankDahl
manager: AnnBe
ms.date: 04/10/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e69dcb250385b375a356ce800f00229035bcaaf5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="extensibility-home-page"></a>拡張機能のホーム ページ

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations は、パートナー、付加価値再販業者によって、さらに一部の顧客によって、大幅にカスタマイズされます。 これは、アプリケーション コードのオーバーレイによって長くサポートされてきた製品の強みです。 柔軟なサービスと頻繁な更新によるクラウドへの移行には、更新によるカスタム ソリューションへの影響を受けにくくする、侵入性の低いカスタマイズが必要です。 この新しいモデルは *拡張性* と呼ばれ、オーバーレイによるカスタマイズに取って代わります。 

拡張性は、Microsoft Dynamics 365 for Retail と Microsoft Dynamics 365 for Finance and Operations での唯一のカスタマイズ フレームワークです。 オーバーレイはサポートされません。

## <a name="introduction"></a>概要

この概要のトピックには、カスタマイズがオーバーレイから純粋な拡張ベース モデルにいつ移行したかに関する情報を含む、すべてのカスタマイズに関する一般情報を示します。 このトピックでは、よく寄せられる質問および回答と共に、Microsoft への拡張性の要求を記録する方法についても説明します。

+ [アプリケーション機能拡張計画](extensibility-roadmap.md)
+ [拡張性の要求](extensibility-requests.md) 
+ [拡張性についてよく寄せられる質問](app-sealing-faq.md) 

## <a name="whats-new"></a>新機能
このセクションでは、2017 年 7 月以降に行われた拡張性に関連する更新プログラムを一覧表示します。

+ [Dynamics 365 for Finance and Operations, Enterprise Edition (2017 年 7 月) の拡張性の変更](changes-july-2017.md)
+ [Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 の拡張性の変更](extensibility-changes-73.md)
+ [Dynamics 365 for Finance and Operations リリース 8.0 の拡張性の変更](Changes-80.md)

## <a name="getting-started"></a>はじめに

「はじめに」では、拡張機能の構築と、オーバーレイ コードに基づいた現在のソリューションの拡張機能ベースソリューションへの移行に取り組みます。 このセクションには、簡単なカスタマイズについて説明した実践ラボが含まれています。

+ [オーバーレイから拡張機能への移行](migrate-overlayer-extension.md)
+ [拡張機能を使用したモデル要素のカスタマイズ (チュートリアル)](customize-model-elements-extensions.md)
+ [カスタマイズ: オーバーレイと拡張機能](customization-overlayering-extensions.md)
<!--+ [Customize by overlayering metadata source code (Office Mix)](https://mix.office.com/watch/1ol6ov90jrd4w)-->

## <a name="extensibility-fundamentals"></a>拡張性の基本

拡張性の基本では、拡張機能の作成方法に関する原則や手法について説明します。 以下のトピックの指針では、名前付けのガイドラインも含め、拡張機能を使用してカスタマイズに取り組む方法について説明します。 また、これらのトピックでは、拡張機能やコマンド チェーンなどの Foundation フレームワークについても説明します。

+ [侵入的なカスタマイズ](intrusive-customizations.md)
+ [クラスの拡張機能](class-extensions.md)
+ [クラスの拡張機能: メソッドのラッピングとコマンド チェーン](method-wrapping-coc.md)
+ [名前付けのガイドライン](naming-guidelines-extensions.md)
+ [オーバレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する](refactoring-over-layering.md)
  
## <a name="how-do-i"></a>操作方法

ここでは、特定のオブジェクト タイプまたはコードのカスタマイズに関する「操作方法」 について説明します。 このトピックのほとんどは、簡潔で要点を押さえています。 ここには多くのトピックがあるので、特定のトピックの検索が実際に役立つことがあります。

### <a name="data-types"></a>データ型
+ [列挙値の追加](add-enum-value.md)
+ [拡張データ型の変更](modify-edt.md) 

### <a name="classes"></a>クラス
+ [ファクトリ メソッドのサブクラスの登録](register-subclass-factory-methods.md)
+ [EventHandlerResult を使用した応答](respond-event-handler-result.md)
+ [RunBase クラスの拡張](extend-runbase-class.md)
+ [デリゲートを使用したアプリケーション起動のカスタマイズ](startup-customizations.md)

### <a name="tables"></a>テーブル
+ [テーブルの既存のフィールドの変更](modify-existing-field.md)
+ [既存のテーブルへの新しいフィールドの追加](add-field-extension.md)
+ [既存のテーブルへのインデックスの追加](add-index.md)
+ [既存のテーブルへのリレーションの追加](add-relation.md)
+ [既存のテーブルのプロパティの変更](modify-properties.md)
+ [テーブルへのメソッドの追加](add-method-table.md)
+ [テーブル レコードの有効期間中の業務処理の実行](subscribe-table-events.md)

### <a name="forms"></a>フォーム
+ [フォームへの新しいデータ ソースの追加](add-datasource.md)
+ [フォームのキャプションの変更](change-caption-form.md)
+ [フォーム コントロールのプロパティの変更](modify-control-properties.md)

### <a name="reports"></a>レポート
+ [電子申告機能の一覧の拡張](../analytics/general-electronic-reporting-formulas-list-extension.md)
+ [アプリ スイート レポートのカスタマイズ](../analytics/customize-app-suite-reports-with-extensions.md)

### <a name="labels"></a>ラベル
+ [ラベルの変更](change-label.md)

## <a name="blog-posts"></a>ブログの投稿

カスタマイズに関する情報は、さまざまなトピックが話し合われるさまざまなブログでも共有されます。 このセクションには、これらのブログの一部への参照が含まれています。

+ [Dynamics 365 for Finance and Operations の機能の拡張](https://blogs.msdn.microsoft.com/mfp/2017/01/31/extending-dynamics-365-for-operations/)
+ [クラスの状態の機能拡張](https://blogs.msdn.microsoft.com/mfp/2017/01/31/extending-class-state/)
+ [拡張メソッド](https://blogs.msdn.microsoft.com/mfp/2015/12/15/x-in-ax7-extension-methods/)
+ [拡張可能な基本列挙型](http://kashperuk.blogspot.dk/2016/09/development-tutorial-extensible-base.html)
+ [静的イベント サブスクリプション](https://blogs.msdn.microsoft.com/mfp/2015/12/10/x-in-ax7-static-event-subscription/)
+ [デリゲートを通じての応答](https://blogs.msdn.microsoft.com/mfp/2017/01/31/responding-through-delegates/)
+ [onValidatingWrite へのサブスクライブ](https://blogs.msdn.microsoft.com/mfp/2017/01/31/subscribing-to-onvalidatingwrite/)
+ [在庫分析コードの機能拡張](https://blogs.msdn.microsoft.com/mfp/2017/08/10/extensible-inventory-dimensions/)
+ [Dynamics 365 for Finance and Operations での拡張機能の考え方の活用](https://blogs.msdn.microsoft.com/axinthefield/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations/)

