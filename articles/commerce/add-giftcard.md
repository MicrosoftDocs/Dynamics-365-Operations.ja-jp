---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261577"
---
# <a name="gift-card-module"></a>ギフト カード モジュール

[!include [banner](includes/banner.md)]

このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

## <a name="overview"></a>概要

ギフト カードは一般的な支払形式であり、ギフト カード モジュールはチェックアウト モジュールで使用してギフト カードを受け入れることができます。 ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。 SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。

SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください

## <a name="module-properties"></a>モジュール プロパティ

- **追加フィールドの表示** - このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。 たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。 または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。

サポートされている値:
-   暗証番号 (PIN)
-   有効期限
-   PIN と 有効期限 
-   None

## <a name="site-settings-for-gift-card-modules"></a>ギフト カード モジュールのサイト設定

コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。 この設定は 3 つの値をサポートします:
- **Dynamics 365 ギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。 この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。
- **SVS と Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。 この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。
- **Dynamics 365、SVS、Givex のギフト カード** - この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。 この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。

## <a name="add-a-gift-card-module-to-a-page"></a>ギフト カード モジュールをページに追加する

ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[スタート キットの概要](starter-kit-overview.md)

[チェックアウト モジュール](add-checkout-module.md)

[外部ギフト カードのサポート](./dev-itpro/gift-card.md)
