---
title: サイト テーマの選択
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794070"
---
# <a name="select-a-site-theme"></a>サイト テーマの選択

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。

サイトのレイアウトおよびスタイル (たとえば、フォント、サイズ、および色) は、選択し、サイトに適用するテーマによって定義されます。 テーマは会社の開発者が作成し、配置します。 テーマの概要については、[テーマの概要](e-commerce-extensibility/theming.md) を参照してください。 テーマを作成し、配置する方法の詳細については、[新しいテーマの作成](e-commerce-extensibility/create-theme.md) を参照してください。

既定では、サイトを最初に作成した時に、**Fabrikam** という名前のテーマが使用されます。 この既定のテーマは、Commerce モジュール ライブラリの一部として提供されます。 サイトに追加のテーマを配置した後、サイトをコンフィギュレーションして、それらの 1 つを使用することができます。

## <a name="select-the-site-theme"></a>サイトのテーマの選択

サイトに適用するテーマを選択するには、次の手順に従います。

1. サイト作成環境で、サイトに移動します。
1. **サイトの管理**\>**拡張性** に移動します。
1. **テーマ** の下で、ドロップダウン メニューでテーマを選択します。
1. 選択したテーマをサイトに適用するには、**保存して公開** を選択します。

> [!NOTE]
> 選択したテーマは、**拡張性** のページで **保存して公開** を選択してすぐにサイトに公開されます。 適用する前にサイトでテーマをプレビューするには、開発またはサンドボックス環境を使用できます。

## <a name="additional-resources"></a>追加リソース

[ロゴの追加](add-logo.md)

[CSS 上書きファイルの作業](css-override-files.md)

[ファビコンの追加](add-favicon.md)

[ようこそメッセージの追加](add-welcome-message.md)

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

[テーマの概要](e-commerce-extensibility/theming.md)

[新しいテーマの作成](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
