---
title: 国/地域の選択モジュール
description: このトピックでは、国/地域の選択モジュールを取り上げ、Microsoft Dynamics 365 Commerce で構成する方法について説明します。
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2021-08-12
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 35d78cdcc356d35776940147e9b0afee0f0be2a2
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674726"
---
# <a name="countryregion-picker-module"></a>国/地域の選択モジュール

[!include [banner](includes/banner.md)]

このトピックでは、国/地域の選択モジュールを取り上げ、Microsoft Dynamics 365 Commerce で構成する方法について説明します。

国/地域の選択モジュールは、Dynamics 365 Commerce の[地域検出およびリダイレクト](geo-detection-redirection.md)機能を使用して、国または地域に関連付けられていない eコマース サイトの URL を要求する顧客に推奨 URL を表示します。

たとえば、カナダの顧客が、カナダに関連付けされていないサイト URL を要求したとします。 この場合、国/地域の選択モジュールには、カナダに関連付けられているサイトの URL を推奨するダイアログ ボックスが表示されます。 次の図は、国/地域の選択ダイアログ ボックスの例を示します。

![ホーム ページの国/地域の選択ダイアログ ボックスの例。](./media/Geo_country-region-module-insitu.png)

## <a name="countryregion-picker-module-properties"></a>国/地域の選択モジュール プロパティ

| プロパティ名              | 先頭値       | 説明 |
| -------------------------- | ----------- | ----------- |
| ヘッダー                    | テキスト        | ダイアログ ボックスの上部に表示されるヘッダー。 |
| サブヘッダー                 | テキスト        | ヘッダーの下に表示されるサブヘッダー。 |
| 国: 表示文字列    | テキスト        | URL オプションの表示名 (「カナダ」など)。 |
| 国: 表示サブ文字列 | テキスト        | URL オプションのオプション表示サブ文字列 (「英語」や「フランス語」など)。 |
| 国: 国の画像     | メディア アセット | URL オプションに関連付けられているオプションの画像 (カナダ国旗の画像など)。 |
| 国: 国の URL       | テキスト        | サイト ビルダーの **チャネル** ページ (**サイト設定 \> チャネル**) で国または地域に設定されているチャネルとロケールに対応する URL。 この URL は **チャネル** ページで構成されている URL と完全に一致している必要があります。 |
| アクション リンク                | アクション リンク | ダイアログ ボックスの下部に表示されるオプションのリンク。 たとえば、このリンクは、サイトがサポートしているすべての国と地域の一覧を表示する内部ページを指定できます。 |

## <a name="add-a-countryregion-picker-module-to-a-page"></a>ページに国/地域の選択モジュールを追加する

国/地域の選択モジュールは、ヘッダー モジュールに直接または共有フラグメントを介して追加できます。 ヘッダー モジュールの詳細については、[ヘッダー モジュール](author-header-module.md)を参照してください 。

## <a name="configure-the-countryregion-picker-module-in-commerce-site-builder"></a>Commerce サイト ビルダーで国/地域の選択モジュールを構成する

> [!NOTE]
> 顧客に推奨する URL は、国/地域の選択モジュールで国オブジェクトとして構成する必要があります。

表示して顧客に推奨する URL ごとに、Commerce サイト ビルダーで次の手順を実行します。

1. 国/地域の選択モジュール スロットを選択します。
1. プロパティ ウィンドウの **国リスト** から、**国を追加** を選択します。
1. 新しい **国** ボックスを選択します。
1. **表示文字列** のフィールドに、表示名 (**カナダ** など) を入力します。
1. オプション: **表示サブ文字列** フィールドに、表示サブ文字列 (たとえば、**フランス語**、または **fr-ca** など) を入力します。
1. オプション: メディア ライブラリから画像を選択します。
1. **国 URL** フィールドに、URL を入力します。 この URL は、**チャネル** ページに表示され、国または地域に関連付けられているロケールを含め、チャネルにマップされている URL と完全に一致する必要があります。
1. **OK** を選択します。
1. 国/地域の選択モジュールに表示する他の国の URL に対して、この手順を繰り返します。

## <a name="additional-resources"></a>追加リソース

[地域検出およびリダイレクトの設定](geo-detection-redirection.md)

[モジュール ライブラリの概要](starter-kit-overview.md)

[ヘッダー モジュール](author-header-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
