---
title: Cookie の同意モジュール
description: このトピックでは、Cookie の同意モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 504232285267fb3663093a84a371e0040233ce23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993528"
---
# <a name="cookie-consent-module"></a>Cookie の同意モジュール

[!include [banner](includes/banner.md)]

このトピックでは、Cookie の同意モジュールと、これを Microsoft Dynamics 365 Commerce のサイト ページに追加する方法について説明します。

## <a name="overview"></a>概要

Cookie の同意モジュールは、ブラウザのクッキーを追跡する機能やモジュールに対し、サイトの利用者に向けて明示的にクッキーの同意を促すものです。 サイトの利用者が新しいブラウザ セッションでサイトを初めて閲覧する際には、この同意が必要となります。 同意が得られて場合は、追跡されるため、サイトの利用者は再び同意を求められることはありません。 詳細については、[Cookie に関するコンプライアンス](cookie-compliance.md) を参照してください。

サイト利用者のクッキーの同意が得られない場合、クッキーの同意が必要となる機能やモジュールはページ上に表示されません。 たとえば、精算モジュール、ソーシャル共有モジュール、優先保管機能にはすべて、cookie の同意が必要となり、サイト利用者の同意が得られれない場合は表示されません。 

Cookie の同意モジュールは、ページの読み込み時に適用できるよう、ページのヘッダー フラグメントに構成可能です。 cookie 同意モジュールは、サイト上での cookie の使用についてサイト利用者に通知する明示的ななメッセージを含み、かつサイトのプライバシー ページへのリンクを提供する必要があります。

以下の図は、サイト ページのヘッダーに表示される、サイトの [プライバシーポリシー] ページへのリンクを含む cookie 同意メッセージの例を示しています。
![Cookie 同意モジュールの例](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Cookie 同意モジュールのプロパティ

| プロパティ名             | 先頭値                 | 説明 |
|---------------------------|-----------------------|-------------|
| リッチ テキスト                  | リッチ テキスト | サイトがブラウザの Cookie を使用していること、およびサイトが完全に機能するためには Cookie の使用に同意する必要があることをサイト利用者に通知するリッチテキストを指定します。 |
| リンク | URL | サイトで追跡されている cookie の種類を説明するサイトのプライバシー ページに、1つ以上のリンクを追加することができます。 |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>サイト ページへの cookie 同意モジュールを追加する

Cookie 同意モジュールを複数のサイト ページに効率的に追加するには、共有ページ ヘッダーのフラグメントに追加します。 ヘッダー フラグメントをすべてのサイトのページに追加すると、サイトの利用者がサイトのページに最初に移動した際に、cookie の同意を通知するメッセージが自動的に表示されます。

ヘッダーのフラグメントとモジュールの詳細については、[ヘッダー モジュール](author-header-module.md)を参照してください 。

## <a name="additional-resources"></a>追加リソース

[モジュール ライブラリの概要](starter-kit-overview.md)

[ヘッダー モジュール](author-header-module.md) 

[Cookie のコンプライアンス](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]