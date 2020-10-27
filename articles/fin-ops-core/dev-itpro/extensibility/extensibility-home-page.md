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
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-14
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 36446a1ca5e8c4bf47e44cb8cbe1d457ad0b7088
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893092"
---
# <a name="extensibility-home-page"></a>拡張機能のホーム ページ

[!include [banner](../includes/banner.md)]

Dynamics 365 Finance、Supply Chain、およびコマースは、パートナー、付加価値再販業者 (VAR) や、さらには一部の顧客によって大幅にカスタマイズされます。 製品をカスタマイズする機能は、アプリケーション コードのオーバーレイによって長くサポートされてきた強みです。 クラウドへの移行を、柔軟なサービスの提供や頻繁な更新と合わせて行う場合、更新がカスタム ソリューションに及ぼす影響を小さくとどめるため、侵入性の低いカスタマイズが必要となります。 この新しいモデルは *拡張性* と呼ばれており、オーバーレイによるカスタマイズに取って代わる存在となりました。

拡張性は、Finance、Supply Chain、およびコマースにおける唯一のカスタマイズ フレームワークです。 オーバーレイはサポートされません。

## <a name="introduction"></a>はじめに

この概要のトピックでは、カスタマイズに関する一般情報を取り上げています。 カスタマイズからオーバーレイを経て純粋な拡張ベース モデルに至る場合などに関する情報が含まれます。 このトピックでは、Microsoft への拡張性の要求を記録する方法と、よく寄せられる質問 (FAQ) への回答についても解説します。

+ [アプリケーション機能拡張計画](extensibility-roadmap.md)
+ [拡張性の要求](extensibility-requests.md) 
+ [拡張性に関するよく寄せられる質問](app-sealing-faq.md) 

## <a name="whats-new"></a>新機能

2017 年 7 月以降に行われた拡張性関連の更新については [拡張性の新機能および変更された機能](extensibility-new.md) を参照してください。

## <a name="getting-started"></a>はじめに

このセクションのトピックは、拡張機能の構築を開始するのに役立ちます。 また、オーバーレイ コードに基づいた現在のソリューションを、拡張機能ベースのソリューションに移行する上でも参考になる内容です。 このセクションには、簡単なカスタマイズについて説明した実践ラボが含まれています。

+ [オーバーレイから拡張機能への移行](migrate-overlayer-extension.md)
+ [拡張機能によってモデル要素をカスタマイズする](customize-model-elements-extensions.md)
+ [拡張機能およびオーバーレイによるカスタマイズ](customization-overlayering-extensions.md)

## <a name="fundamentals-on-extensions"></a>拡張機能の基本

このセクションでは、拡張機能の作成に関する基本や原則、手法について説明します。 以下のトピックの指針では、拡張機能を使用してカスタマイズに取り組む方法について説明します。 この原則には、名前付けのガイドラインが含まれています。 また、これらのトピックでは、拡張機能やコマンド チェーンなど、基盤となるフレームワークについても説明します。

+ [侵入的なカスタマイズ](intrusive-customizations.md)
+ [X++ の拡張モデルのクラス](class-extensions.md)
+ [クラスの拡張機能 - メソッドのラッピングとコマンド チェーン](method-wrapping-coc.md)
+ [拡張機能の名前付けガイドライン](naming-guidelines-extensions.md)
+ [オーバーレイを拡張機能にリファクタリングするため、モデルの制限を緩和する](refactoring-over-layering.md)

## <a name="how-do-i-create-extensions"></a>拡張機能の作成方法

このセクションは "方法" を含みます トピックが含まれています。 このトピックのほとんどは、簡潔で要点を押さえた内容となっています。 ここには多くのトピックがあるため、特定のトピックを検索すると便利にご利用いただける場合があります。

### <a name="data-types"></a>データ型
+ [拡張機能を使用して列挙体に値を追加](add-enum-value.md)
+ [拡張機能を通じて拡張データ型 (EDT) を変更する](modify-edt.md) 

### <a name="classes"></a>クラス
+ [ファクトリ メソッドのサブクラスの登録](register-subclass-factory-methods.md)
+ [EventHandlerResult を使用して応答](respond-event-handler-result.md)
+ [RunBase クラスの拡張](extend-runbase-class.md)
+ [デリゲートを使用してアプリケーション起動をカスタマイズする](startup-customizations.md)

### <a name="tables"></a>テーブル
+ [拡張機能を使用したテーブル内の既存のフィールドの変更](modify-existing-field.md)
+ [拡張機能を使用してテーブルにフィールドを追加](add-field-extension.md)
+ [拡張機能を使用してテーブルにインデックスを追加](add-index.md)
+ [拡張機能を使用してテーブルに関係を追加](add-relation.md)
+ [拡張機能を使用して、テーブルのプロパティを変更する](modify-properties.md)
+ [拡張機能を使用してテーブルにメソッドを追加](add-method-table.md)
+ [テーブル レコードの有効期間中の業務処理の実行](subscribe-table-events.md)

### <a name="forms"></a>フォーム
+ [フォームへの新しいデータ ソースの追加](add-datasource.md)
+ [拡張機能によって、フォームのキャプションを変更します。](change-caption-form.md)
+ [拡張機能を使用して、フォーム コントロールのプロパティを変更する](modify-control-properties.md)

### <a name="others"></a>その他
+ [選択したデータ型の小数点以下の精度の拡張](decimal-point-precision.md)
+ [拡張機能を通じた新しい在庫分析コードの追加](inventory-dimensions.md)

### <a name="reports"></a>レポート
+ [電子申告 (ER) 機能の一覧の拡張](../analytics/general-electronic-reporting-formulas-list-extension.md)
+ [拡張機能を使用してアプリケーション スイート レポートをカスタマイズする](../analytics/customize-app-suite-reports-with-extensions.md)

### <a name="blog-posts"></a>ブログの投稿

カスタマイズに関する情報は、さまざまなトピックが取り上げられるブログでも共有されます。 このセクションには、そのようなブログの一部への参照が含まれています。

+ [Dynamics 365 for Finance and Operations の拡張](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extending-dynamics-365-for-operations)
+ [拡張メソッド](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/x-in-ax7-extension-methods/)
+ [拡張可能な基本列挙型](https://kashperuk.blogspot.dk/2016/09/development-tutorial-extensible-base.html)
+ [静的イベント サブスクリプション](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/x-in-ax7-static-event-subscription/)
+ [onValidatingWrite へのサブスクライブ](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/subscribing-to-onvalidatingwrite/)
+ [Dynamics 365 for Finance and Operations での拡張機能のご要望を採用します。](https://community.dynamics.com/ax/b/axinthefield/posts/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations-2-sysextension-framework)
+ [拡張可能な X++ - メソッドの署名](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extensible-x-method-signatures/)

## <a name="how-do-i-create-an-extensible-solution"></a>拡張可能なソリューションを作成するには

このセクションでは、コードのユーザーがソリューションを拡張できるように、拡張可能なソリューションを作成する方法や、ソリューションを拡張可能にする方法に関するベスト プラクティスについて説明します。

+ [拡張可能なコードの書き込み](writing-extensible-code.md)
+ [クラス](extensible-classes.md)
+ [メソッド](extensible-methods.md)
+ [フォーム](extensible-forms.md)
+ [拡張データ型](extensible-edts.md)
+ [拡張可能な列挙](extensible-enums.md)
+ [委任](extensible-code-delegates.md)
+ [テーブル](extensible-tables.md)
+ [メソッドを拡張可能にする属性](extensibility-attributes.md)

## <a name="breaking-changes"></a>変更の分割

ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。 

+ 消費者に重大な影響が及ぶのを防ぐ指針に関しては、[重大な変更](breaking-changes.md) をご覧ください。
+ [互換性チェック ツール](compatibility-checker-tool.md) を使用すると、指定されたベースライ ンリリースまたは更新に対して、メタデータの互換性に影響する変更を検出できます。
