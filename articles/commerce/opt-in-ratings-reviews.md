---
title: 評価とレビューを使用するためのオプト イン
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプト イン方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697983"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>評価とレビューを使用するためのオプト イン

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプト イン方法について説明します。

## <a name="overview"></a>概要

評価およびレビューのソリューションは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Commerce で利用可能にできる オムニチャネル ソリューションです。 LCS は、小売業者が環境を準備から使用停止まで管理するために使用する管理ポータルです。

評価を使用し、E コマース Web サイトのソリューションをレビューする場合は、最初にオプト インをクリックする必要があります。

## <a name="opt-in-to-use-ratings-and-reviews"></a>評価とレビューを使用するためのオプト イン

サイトで評価およびレビューを使用しオプト インするには、次の手順に従います。

1. [新しい E コマース サイトの配置](deploy-ecommerce-site.md) の手順に従ってください。
1. まだ LCS を開いている間に、**小売配置の設定 \> その他の設定** の順に移動します。
1. **評価およびレビュー サービスの有効化**オプションを、**はい**に設定します。
1. **評価およびレビュー モデレーター (セキュリティ グループ オブジェクト ID) の AAD セキュリティ グループ** フィールドで、評価およびレビュー モデレーターを含む Microsoft Azure Active Directory (Azure AD) セキュリティ グループの ID を入力します。

    ![評価とレビューを使用するためのオプト イン](media/LCS_RnR_Preference.png)

1. E コマース初期化プロセスを完了します。

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューの管理](manage-reviews.md)

[評価とレビューのコンフィギュレーション](configure-ratings-reviews.md)

[Dynamics 365 Retail の商品評価の同期](sync-product-ratings.md)
