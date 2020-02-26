---
title: ようこそメッセージの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001257"
---
# <a name="add-a-welcome-message"></a>ようこそメッセージの追加


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。

## <a name="overview"></a>概要

E コマース Web サイトのようこそメッセージは、訪問者に実施中のセール、サイトの更新、または季節のコレクションが利用可能であることについて知らせることができます。 ようこそメッセージは、警告モジュールを使用して設定されます。

警告モジュールをヘッダー フラグメントの**エラー/情報メッセージ** スロットに追加する必要があります。 警告モジュールを使用すると、表示されるテキスト、テキストの色、および配置を指定できます。 また、サイトの訪問者がメッセージを閉じることができるかどうかを指定することもできます。

共有ヘッダー フラグメントに追加されたようこそメッセージは、共有ヘッダー フラグメントが使用されているテンプレートを使用するすべてのページに表示されます。

サイトにようこそメッセージを追加するには、次のステップを実行します。

1. Dynamics 365 Commerce で、サイトに移動します。
1. **フラグメント**を選択します。
1. メッセージを追加するヘッダー フラグメントを選択します。
1. アウトライン ツリーで、**エラー/情報メッセージ**を展開します。
1. 警告モジュールを選択します。

    警告モジュールがまだ存在しない場合は、**エラー/情報メッセージ**の隣にある省略記号ボタン (**...**) を選択し、**モジュールの追加**を選択します。 警告モジュールを選択し、**OK** を選択します。

1. 右側のプロパティ ウィンドウの**データ** タブで、**データ ソースの追加**を選択し、**コンテンツ**を選択します。
1. **入力テキスト** フィールドに、ようこそメッセージのテキストを入力します。
1. ヘッダー フラグメントを保存し、チェック イン後に公開します。

これで、選択したヘッダー フラグメントを使用するすべてのサイト ページの上部にようこそメッセージが表示されます。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

