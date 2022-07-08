---
title: NF-e カスタム証明書の検証
description: この記事では、NF-e カスタム証明書の有効化と使用について説明します。
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3d69aa9d6d0ce33fbed9ba1c7a7af441e14d0d07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875907"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e カスタム証明書の検証

[!include [banner](../includes/banner.md)]

ブラジルのルート証明機関によって発行された証明書からの **サーバー認証目的** プロパティは、既定で無効になっており、手動で有効にする必要があります。 状況によっては、証明書の自動更新によって、このプロパティが有効でなくなる場合があります。 こうした状況では、TLS 接続が影響を受け、信頼されなくなる可能性があります。 ミナス ジェライス州 (MG) およびパラナ州 (PR) の運用環境で ブラジルの電子会計ドキュメント モデル55 (NF-e) を発行する機能も影響を受けます。

**NF-e カスタム証明書の検証** の修正を有効にするには、 **機能管理** に移動します。 この機能により、V5 証明書検証および V10 証明書検証の代替ソリューションが可能になり、NF-e のセキュリティで保護された転送と SEFAZ からの認証の受取を要求する Web サービスとの信頼できる接続を許可します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
