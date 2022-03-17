---
title: 新規顧客の作成時にようこそメールが送信されない
description: このトピックでは、Microsoft Dynamics 365 Commerce で新規顧客が作成された時に、ようこそメール通知が送信されない場合に役立つトラブルシューティングのガイドラインを提供します。
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349961"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>新規顧客の作成時にようこそメールが送信されない

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で新規顧客が作成された時に、ようこそメール通知が送信されない場合に役立つトラブルシューティングのガイドラインを提供します。

## <a name="description"></a>Description

Commerce 本部で新規顧客が作成された時に、**顧客が作成した** メール通知のタイプに電子メール通知が構成されていたとしても、ようこそメールが顧客に送信されません。

## <a name="resolution"></a>解決策

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>顧客が作成したメール通知のタイプに対して正しいメール ID の値を設定する

本部で **顧客が作成した** 電子メール通知タイプに対して正しい **メール ID** の値を設定するには、次の手順に従います。

1. **Retail と Commerce \> 本部の設定 \> Commerce メール通知プロファイル** の順に移動します。
1. 左ナビゲーション ウィンドウで、メール通知プロファイルを選択します。
1. **Retail イベント通知の設定** で、**顧客が作成した** メール通知タイプについて **電子メール ID** フィールドを **NewCust** に設定します。

## <a name="additional-resources"></a>追加リソース

[電子メール通知プロファイルの設定](../email-notification-profiles.md)
