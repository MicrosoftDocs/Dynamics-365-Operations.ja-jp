---
title: テキスト ブロック モジュール
description: このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025600"
---
# <a name="text-block-module"></a>テキスト ブロック モジュール


[!include [banner](includes/banner.md)]

このトピックでは、テキスト ブロック モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

## <a name="overview"></a>概要

テキスト ブロック モジュールは、テキスト コンテンツを追加するために使用されるモジュールです。 このコンテンツは、情報提供またはプロモーションです。

テキスト ブロック モジュールは、コンテンツ管理システム (CMS) からのデータによって駆動し、任意のページに配置できます。 これらは、ページ コンテキストやその他の任意のモジュールに依存しないスタンドアロン モジュールです。

## <a name="examples-of-text-block-modules-in-e-commerce"></a>E コマースのテキスト ブロック モジュールの例

テキスト ブロック モジュールは、次の方法で使用できます。

* 製品の詳細ページで製品機能について紹介します。
* 任意のページで情報提供を目的とします。 たとえば、ロイヤルティ プログラムの利点を説明し、出荷ポリシーと返品ポリシーを説明し、よく寄せられる質問に回答し、または "弊社について" コンテンツを提供したりできます。
* 製品の詳細ページでカスタム メッセージを追加します。 (たとえば、"$50 以上のご注文で送料無料")。
* 製品の詳細ページ、カート ページ、チェックアウト ページ、およびその他のページで免責事項や連絡先の詳細を提供します (たとえば、"出荷および返品には店舗ポリシーが適用されます") 。

## <a name="text-block-module-properties"></a>テキスト ブロック モジュール プロパティ

| プロパティ名     | Value                                            | 説明 |
|-------------------|--------------------------------------------------|-------------|
| リッチ テキスト         | リッチ テキスト                                        | 段落のテキスト。 太字、下線付き、斜体など、基本的なリッチ テキスト機能がいくつかサポートされます。 |
| カスタム クラス名 | カスケード スタイル シート (CSS) クラス名        | 開発者がこのモジュールをフォーマットするために提供するカスタム CSS クラス名。 クラス名は、テーマ パックで定義する必要があります。 |
| フォント サイズ         | **小**、**中**、**大**、または**特大** | コンテンツのフォント サイズ。 |

## <a name="add-a-text-block-module-to-a-page"></a>テキスト ブロック モジュールをページに追加する

新しいページテキスト ブロック モジュールを追加して必要なプロパティを設定するには、次の手順を実行します。

1. **コンテンツ テンプレート**という名前のページ テンプレートを作成します。 
1. **本文**スロットで、**既定のページ** モジュールを追加します。
1. テンプレートの編集を終了し、公開します。
1. 作成したコンテンツ テンプレートを使用して、**コンテンツ ページ**という名前のページを作成します。
1. 新しいページの**メイン** スロットで、コンテナ― モジュールを追加します。
1. コンテナー モジュールのプロパティ ウィンドウで、**幅**プロパティを**全コンテナー**に設定します。
1. テキスト ブロック モジュールをコンテナー モジュールに追加します。 
1. テキスト ブロック モジュールのプロパティ ウィンドウで、**リッチ テキスト** フィールドにテキストを追加します。
1. ページの編集を終了し、公開します。

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[プロモーション バナー モジュール](add-alert.md)

[カルーセル モジュール](add-carousel.md)

[コンテンツ ブロック モジュール](add-hero-module.md)

[ビデオ プレーヤー モジュール](add-video-player.md)

