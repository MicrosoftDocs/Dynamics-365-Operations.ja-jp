---
title: 場所に基づく店舗検出の有効化
description: このトピックでは、Dynamics 365 Commerce サイトの場所に基づく店舗検出を有効にする方法について説明します。
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3f7e9a3acde508f405ce85f125db552c3ae3656b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000726"
---
# <a name="enable-location-based-store-detection"></a>場所に基づく店舗検出の有効化


[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Commerce サイトの場所に基づく店舗検出を有効にする方法について説明します。

## <a name="overview"></a>概要

コマースでの場所に基づく店舗検出により、場所に基づいて、関連するサイト コンテンツを顧客に提供することができます。 場所に基づく店舗検出が有効になっている場合、コマースのレンダリング サービスは、顧客の Web ブラウザー IP アドレスの国/地域の情報を使用して、使用可能で最適な地理的サイト構成に顧客を誘導します。

## <a name="privacy-notice"></a>プライバシー通知

場所に基づく店舗検出機能を有効にすると、顧客のブラウザーからの情報が Microsoft location 位置情報サービスに送信されます。 その後、この情報を使用して、その場所に関連するコンテンツを顧客に提供します。 顧客のブラウザーから送信される情報と、顧客に返される場所に基づく情報の両方が、プライバシー ポリシーと Cookie コンプライアンス ポリシーの対象となります。

## <a name="turn-on-location-based-store-detection"></a>場所に基づく店舗検出の有効化

コマースで場所に基づく店舗検出を有効にするには、次の手順に従います。

1. オーサリング ツールで、サイトに移動します。
1. 左のナビゲーション ウィンドウで、**サイト管理** を選択します。
1. **サイトの設定** を選択します。
1. **場所に基づく店舗検出を有効にする** のオプションを **オン** に設定します。

## <a name="additional-resources"></a>追加リソース

[ドメイン名のコンフィギュレーション](configure-your-domain-name.md)

[新しい eコマース テナントのデプロイ](deploy-ecommerce-site.md)

[E コマース サイトの作成](create-ecommerce-site.md)

[オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け](associate-site-online-store.md)

[robots.txt ファイルの管理](manage-robots-txt-files.md)

[URL リダイレクトの一括アップロード](upload-bulk-redirects.md)

[B2C テナントを Commerce に 設定](set-up-B2C-tenant.md)

[ユーザー ログイン用のカスタム ページの設定](custom-pages-user-logins.md)

[Commerce 環境での複数の B2C テナントのコンフィギュレーション](configure-multi-B2C-tenants.md)

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]