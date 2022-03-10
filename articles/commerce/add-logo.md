---
title: ロゴの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 583462755838e51b4c988b8da057dbeeee773e0b
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964582"
---
# <a name="add-a-logo"></a>ロゴの追加

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。

サイトの構築時には、まず最初に会社またはブランド ロゴをサイトのヘッダーに追加するのが一般的です。 Dynamics 365 Commerce オンライン モジュール ライブラリでは、このタスクを簡単にするためのモジュールが提供されます。

テンプレート、レイアウト、またはページに、ロゴを直接追加できます。 この方法により、特定のページまたはページ グループに表示されるロゴを簡単に変更できます。 ただし、このトピックでは、サイトのすべてのページで再利用できるヘッダー フラグメントにロゴを追加する最もよくあるシナリオについて説明します。

## <a name="prerequisites"></a>必要条件

サイトのすべてのページにロゴを追加する前に、これらのタスクを完了する必要があります。

1. ロゴをメディア ライブラリにアップロードします。
1. ヘッダー フラグメントを作成します。 フラグメントの作成および使用方法の詳細については、[フラグメントの使用](work-with-fragments.md) を参照してください。
1. サイトのページがレイアウトやモジュール オプションとして使用するヘッダー フラグメントをテンプレートに含めます。 テンプレートの詳細については、[テンプレートの使用](work-with-templates.md) を参照してください。

## <a name="add-a-logo-to-a-header-fragment"></a>ヘッダー フラグメントへのロゴの追加

サイトのヘッダー フラグメントにロゴを追加するには、次の手順を実行します。

1. 左のナビゲーション ウィンドウで、**フラグメント** を選択します。
1. 作成したヘッダー フラグメントを選択し、**編集** を選択します。
1. ヘッダー モジュールを展開します。
1. ヘッダー モジュールのプロパティ ウィンドウで、ロゴの画像とリンクを提供します。 
1. ヘッダー フラグメントを保存し、編集を終了して、公開します。

更新されたヘッダー フラグメントを公開すると、ヘッダー フラグメントを含むテンプレートを使用するすべてのサイト ページにロゴが表示されます。

## <a name="additional-resources"></a>追加リソース

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
