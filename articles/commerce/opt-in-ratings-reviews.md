---
title: 評価とレビューを使用するためのオプト イン
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプトイン方法について説明します。
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9e3f2a17e182c0e3efc8b90380eff74f350c3278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804652"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>評価とレビューを使用するためのオプト イン

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce サイトで評価およびレビューを使用するためのオプトイン方法について説明します。

## <a name="overview"></a>概要

評価およびレビューのソリューションは、Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Commerce で利用可能にできるオムニチャネル ソリューションです。 LCS は、小売業者が環境を準備から使用停止まで管理するために使用する管理ポータルです。

Commerce Web サイトで評価とレビューのソリューションを使用する場合は、Dynamics 365 Commerce で E コマース サイトを展開する際に、評価とレビューをオプトインする必要があります。

## <a name="opt-in-to-use-ratings-and-reviews"></a>評価とレビューを使用するためのオプト イン

サイトで評価およびレビューを使用しオプト インするには、次の手順に従います。

1. [新しい E コマース サイトの配置](deploy-ecommerce-site.md) の手順に従ってください。
1. まだ LCS を開いている間に、**小売配置の設定 \> その他の設定** の順に移動します。
1. **評価およびレビュー サービスの有効化** オプションを、**はい** に設定します。
1. **評価およびレビュー モデレーター (セキュリティ グループ オブジェクト ID) の AAD セキュリティ グループ** フィールドで、評価およびレビュー モデレーターを含む Microsoft Azure Active Directory (Azure AD) セキュリティ グループの ID を入力します。

    ![評価とレビューを使用するためのオプト イン](media/LCS_RnR_Preference.png)

1. E コマース初期化プロセスを完了します。

> [!NOTE] 
> 既存の Dynamics 365 Commerce の顧客であり、評価とレビューをオプトインせずに E コマース サイトを既に展開していて、Dynamics 365 Commerce パッケージから評価とレビューを使用する場合は、サービス要求を送信してください。 サービス要求を送信する方法については、[サービス要求送信プロセス](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json)を参照してください。 

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューの管理](manage-reviews.md)

[評価とレビューのコンフィギュレーション](configure-ratings-reviews.md)

[Dynamics 365 Commerce の商品評価の同期](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]