---
title: ようこそメッセージの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6c4f1746dc0e5f3e6525f36979e33a4ebd0180fa1e52ec011a8c1cfa69565c3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725365"
---
# <a name="add-a-welcome-message"></a>ようこそメッセージの追加

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce Web サイトにようこそメッセージを追加する方法について説明します。

E コマース Web サイトのようこそメッセージは、訪問者に実施中のセール、サイトの更新、または季節のコレクションが利用可能であることについて知らせることができます。 ようこそメッセージは、警告モジュールを使用して設定されます。

警告モジュールをヘッダー フラグメントの **エラー/情報メッセージ** スロットに追加する必要があります。 警告モジュールを使用すると、表示されるテキスト、テキストの色、および配置を指定できます。 また、サイトの訪問者がメッセージを閉じることができるかどうかを指定することもできます。

共有ヘッダー フラグメントに追加されたようこそメッセージは、共有ヘッダー フラグメントが使用されているテンプレートを使用するすべてのページに表示されます。

サイトにようこそメッセージを追加するには、次のステップを実行します。

1. Commerce サイト ビルダーで、ご利用のサイトに移動します。
1. **フラグメント** を選択します。
1. メッセージを追加するヘッダー フラグメントを選択します。
1. アウトライン ツリーで、**エラー/情報メッセージ** を展開します。
1. 警告モジュールを選択し、**OK** を選択します。 警告モジュールがまだ存在しない場合は、まず **エラー/情報メッセージ** の隣にある省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。
1. 右側のプロパティ ウィンドウの **データ** タブで、**データ ソースの追加** を選択し、**コンテンツ** を選択します。
1. **入力テキスト** フィールドに、ようこそメッセージのテキストを入力します。
1. **保存** を選択し、 **編集の完了** を選択してヘッダー フラグメントにチェックインし、**発行** を選択して公開します。 

これで、選択したヘッダー フラグメントを使用するすべてのサイト ページの上部にようこそメッセージが表示されます。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
