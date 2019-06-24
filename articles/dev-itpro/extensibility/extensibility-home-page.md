---
title: 拡張機能のホーム ページ
description: このトピックでは、拡張性に関するトピックへのリンクを提供します。
author: FrankDahl
manager: AnnBe
ms.date: 05/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-14
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: e58f4291d6413117657a6aaa2e215c8d7386cb47
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595379"
---
# <a name="extensibility-home-page"></a>拡張機能のホーム ページ

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations は、パートナー、付加価値再販業者 (VAR) や、さらには一部の顧客によって大幅にカスタマイズされます。 製品をカスタマイズする機能は、アプリケーション コードのオーバーレイによって長くサポートされてきた強みです。 クラウドへの移行を、柔軟なサービスの提供や頻繁な更新と合わせて行う場合、更新がカスタム ソリューションに及ぼす影響を小さくとどめるため、侵入性の低いカスタマイズが必要となります。 この新しいモデルは *拡張性* と呼ばれており、オーバーレイによるカスタマイズに取って代わる存在となりました。

拡張性は、Finance and Operations と Microsoft Dynamics 365 for Retail における唯一のカスタマイズ フレームワークです。 オーバーレイはサポートされません。

## <a name="introduction"></a>はじめに

この概要のトピックでは、カスタマイズに関する一般情報を取り上げています。 カスタマイズからオーバーレイを経て純粋な拡張ベース モデルに至る場合などに関する情報が含まれます。 このトピックでは、Microsoft への拡張性の要求を記録する方法と、よく寄せられる質問 (FAQ) への回答についても解説します。

+ [アプリケーション機能拡張計画](extensibility-roadmap.md)
+ [拡張性の要求](extensibility-requests.md) 
+ [拡張性に関するよく寄せられる質問](app-sealing-faq.md) 

## <a name="whats-new"></a>新機能

2017 年 7 月以降に行われた拡張性関連の更新については [拡張性の新機能](extensibility-new.md) を参照してください。

## <a name="getting-started"></a>はじめに

このセクションのトピックは、拡張機能の構築を開始するのに役立ちます。 また、オーバーレイ コードに基づいた現在のソリューションを、拡張機能ベースのソリューションに移行する上でも参考になる内容です。 このセクションには、簡単なカスタマイズについて説明した実践ラボが含まれています。

+ [オーバーレイから拡張機能への移行](migrate-overlayer-extension.md)
+ [拡張機能を使用したモデル要素のカスタマイズ (チュートリアル)](customize-model-elements-extensions.md)
+ [カスタマイズ: オーバーレイと機能拡張](customization-overlayering-extensions.md)
<!--+ [Customize by overlayering metadata source code (Office Mix)](https://mix.office.com/watch/1ol6ov90jrd4w)-->

## <a name="fundamentals-on-extensions"></a>拡張機能の基本

このセクションでは、拡張機能の作成に関する基本や原則、手法について説明します。 以下のトピックの指針では、拡張機能を使用してカスタマイズに取り組む方法について説明します。 この原則には、名前付けのガイドラインが含まれています。 また、これらのトピックでは、拡張機能やコマンド チェーンなど、基盤となるフレームワークについても説明します。

+ [侵入的なカスタマイズ](intrusive-customizations.md)
+ [クラスの拡張機能](class-extensions.md)
+ [クラスの拡張機能: メソッドのラッピングとコマンド チェーン](method-wrapping-coc.md)
+ [名前付けのガイドライン](naming-guidelines-extensions.md)
+ [オーバレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する](refactoring-over-layering.md)

## <a name="how-do-i-create-extensions"></a>拡張機能の作成方法

このセクションは "方法" を含みます トピックが含まれています。 このトピックのほとんどは、簡潔で要点を押さえた内容となっています。 ここには多くのトピックがあるため、特定のトピックを検索すると便利にご利用いただける場合があります。

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

### <a name="others"></a>その他
+ [小数点以下の精度の拡張](decimal-point-precision.md)

### <a name="reports"></a>レポート
+ [電子申告機能の一覧の拡張](../analytics/general-electronic-reporting-formulas-list-extension.md)
+ [アプリ スイート レポートのカスタマイズ](../analytics/customize-app-suite-reports-with-extensions.md)

### <a name="blog-posts"></a>ブログの投稿

カスタマイズに関する情報は、さまざまなトピックが取り上げられるブログでも共有されます。 このセクションには、そのようなブログの一部への参照が含まれています。

+ [Dynamics 365 for Finance and Operations の拡張](https://blogs.msdn.microsoft.com/mfp/2017/01/31/extending-dynamics-365-for-operations/)
+ [クラスの状態の機能拡張](https://blogs.msdn.microsoft.com/mfp/2017/01/31/extending-class-state/)
+ [拡張メソッド](https://blogs.msdn.microsoft.com/mfp/2015/12/15/x-in-ax7-extension-methods/)
+ [拡張可能な基本列挙型](https://kashperuk.blogspot.dk/2016/09/development-tutorial-extensible-base.html)
+ [静的イベント サブスクリプション](https://blogs.msdn.microsoft.com/mfp/2015/12/10/x-in-ax7-static-event-subscription/)
+ [デリゲートを通じての応答](https://blogs.msdn.microsoft.com/mfp/2017/01/31/responding-through-delegates/)
+ [onValidatingWrite へのサブスクライブ](https://blogs.msdn.microsoft.com/mfp/2017/01/31/subscribing-to-onvalidatingwrite/)
+ [在庫分析コードの機能拡張](https://blogs.msdn.microsoft.com/mfp/2017/08/10/extensible-inventory-dimensions/)
+ [Dynamics 365 for Finance and Operations での拡張機能のご要望を採用します。](https://blogs.msdn.microsoft.com/axinthefield/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations/)
+ [拡張可能な X++ - メソッドの署名](https://blogs.msdn.microsoft.com/mfp/2017/08/31/extensible-x-method-signatures/)

## <a name="how-do-i-create-an-extensible-solution"></a>拡張可能なソリューションを作成するには

このセクションでは、コードのユーザーがソリューションを拡張できるように、拡張可能なソリューションを作成する方法や、ソリューションを拡張可能にする方法に関するベスト プラクティスについて説明します。

+ [拡張可能なコードの記述](writing-extensible-code.md)
+ [クラス](extensible-classes.md)
+ [メソッド](extensible-methods.md)
+ [フォーム](extensible-forms.md)
+ [拡張データ型](extensible-edts.md)
+ [拡張可能な列挙](extensible-enums.md)
+ [委任](extensible-code-delegates.md)
+ [テーブル](extensible-tables.md)
+ [メソッドの拡張属性](extensibility-attributes.md)

## <a name="breaking-changes"></a>重大な変更
ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。 消費者に重大な影響が及ぶのを防ぐ指針に関しては、[重大な変更](breaking-changes.md) をご覧ください。
