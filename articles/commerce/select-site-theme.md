---
title: サイト テーマの選択
description: この記事では、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。
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
ms.openlocfilehash: b038dc996c571d54dce3f2aec679f7af8af85074
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900389"
---
# <a name="select-a-site-theme"></a>サイト テーマの選択

[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。

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

[著作権に関する注意事項の追加](add-copyright-notice.md)

[サイトに言語を追加する](add-languages-to-site.md)

[サイト ページにスクリプト コードを追加してテレメトリをサポートする](add-telemetry.md)

[テーマの概要](e-commerce-extensibility/theming.md)

[新しいテーマの作成](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
