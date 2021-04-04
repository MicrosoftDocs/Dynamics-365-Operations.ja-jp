---
title: NF-e カスタム証明書の検証
description: このトピックでは、NF-e カスタム証明書の有効化と使用について説明します。
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240582"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e カスタム証明書の検証

[!include [banner](../includes/banner.md)]

NF-e のカスタム証明書の検証機能を有効にすると、カスタム検証によって Web サービスとの接続が許可されます。 この接続は、NF-e を送信し、SEFAZ から認証を受信するために必要です。

認証 V5 の **サーバー認証目的** プロパティは、ブラジルのルート証明機関によって発行されます。 このプロパティは既定でオフになっているため、手動で有効にする必要があります。 状況によっては、証明書の自動更新によって、このプロパティが有効でなくなる場合があります。 こうした状況では、TLS 接続が影響を受け、信頼されなくなります。 ミナス ジェライス州 (MG) およびパラナ州 (PR) の実稼働環境で NF-e を発行する機能も影響を受けます。

この更新により、証明書検証の代替ソリューションを使用できるようになります。つまり、セキュリティで保護された通信を確立することができます。




[!INCLUDE[footer-include](../../includes/footer-banner.md)]