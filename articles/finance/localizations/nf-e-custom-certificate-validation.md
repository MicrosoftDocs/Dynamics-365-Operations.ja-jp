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
ms.openlocfilehash: f13e8b8229bbd9e174e5bde7858a468048ba309b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990089"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="e48b9-103">NF-e カスタム証明書の検証</span><span class="sxs-lookup"><span data-stu-id="e48b9-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e48b9-104">NF-e のカスタム証明書の検証機能を有効にすると、カスタム検証によって Web サービスとの接続が許可されます。</span><span class="sxs-lookup"><span data-stu-id="e48b9-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="e48b9-105">この接続は、NF-e を送信し、SEFAZ から認証を受信するために必要です。</span><span class="sxs-lookup"><span data-stu-id="e48b9-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="e48b9-106">認証 V5 の **サーバー認証目的** プロパティは、ブラジルのルート証明機関によって発行されます。</span><span class="sxs-lookup"><span data-stu-id="e48b9-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="e48b9-107">このプロパティは既定でオフになっているため、手動で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e48b9-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="e48b9-108">状況によっては、証明書の自動更新によって、このプロパティが有効でなくなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e48b9-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="e48b9-109">こうした状況では、TLS 接続が影響を受け、信頼されなくなります。</span><span class="sxs-lookup"><span data-stu-id="e48b9-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="e48b9-110">ミナス ジェライス州 (MG) およびパラナ州 (PR) の実稼働環境で NF-e を発行する機能も影響を受けます。</span><span class="sxs-lookup"><span data-stu-id="e48b9-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="e48b9-111">この更新により、証明書検証の代替ソリューションを使用できるようになります。つまり、セキュリティで保護された通信を確立することができます。</span><span class="sxs-lookup"><span data-stu-id="e48b9-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


