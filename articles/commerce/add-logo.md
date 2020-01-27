---
title: ロゴの追加
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914625"
---
# <a name="add-a-logo"></a>ロゴの追加

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のサイトにロゴを追加する方法について説明します。

## <a name="overview"></a>概要

サイトの構築時には、まず最初に会社またはブランド ロゴをサイトのヘッダーに追加するのが一般的です。 Dynamics 365 Commerce オンライン スタート キットでは、このタスクを簡単にするためのモジュールが提供されます。

テンプレート、レイアウト、またはページに、ロゴを直接追加できます。 この方法により、特定のページまたはページ グループに表示されるロゴを簡単に変更できます。 ただし、このトピックでは、サイトのすべてのページで再利用できるヘッダー フラグメントにロゴを追加する最もよくあるシナリオについて説明します。

## <a name="prerequisites"></a>必要条件

サイトのすべてのページにロゴを追加する前に、これらのタスクを完了する必要があります。

1. **資産**ページからアクセスできるデジタル資産マネージャーにロゴをアップロードします。
1. ヘッダー フラグメントを作成します。 フラグメントの作成および使用方法の詳細については、[フラグメントの使用](work-with-fragments.md) を参照してください。
1. サイトのページがレイアウトやモジュール オプションとして使用するヘッダー フラグメントをテンプレートに含めます。 テンプレートの詳細については、[テンプレートの使用](work-with-templates.md) を参照してください。

## <a name="add-a-logo-to-a-header-fragment"></a>ヘッダー フラグメントへのロゴの追加

サイトのヘッダー フラグメントにロゴを追加するには、次の手順を実行します。

1. 左側のナビゲーション ウィンドウで**フラグメント**を選択し、作成したヘッダー フラグメントを選択します。
2. **チェック アウト**を選択します。
3. **ヘッダー** スロットおよび**ロゴ** スロットを展開します。
4. **ロゴ** スロットの省略ボタン (**...**) を選択し、**モジュールの追加**を選択します。
5. ロゴ モジュールを選択します。
6. 右側のプロパティ ウィンドウで、ロゴ モジュールをコンフィギュレーションしてロゴが表示されるようにします。
7. ヘッダー フラグメントを保存し、チェック イン後に公開します。

更新されたヘッダー フラグメントを公開すると、ヘッダー フラグメントを含むテンプレートを使用するすべてのサイト ページにロゴが表示されます。

## <a name="additional-resources"></a>追加リソース

[サイト テーマの選択](select-site-theme.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[ようこそメッセージの追加](add-welcome-message.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

