---
title: "モバイル バーコードのサポート"
description: "このトピックでは、Android 対応デバイスで倉庫モバイル スキャン アプリを処理する方法について説明します。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 05f00bfbe7ef1dfce58b242d4defa925649e1dae
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="mobile-bar-code-support"></a><span data-ttu-id="9f977-103">モバイル バー コードのサポート</span><span class="sxs-lookup"><span data-stu-id="9f977-103">Mobile bar code support</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9f977-104">Android はオープン ソース プロジェクトであるため、ウェアハウス バーコード スキャナ用のハードウェアを製造するすべてのメーカーは、Android オペレーティングシステムを実行するためのデバイスを構築できます。</span><span class="sxs-lookup"><span data-stu-id="9f977-104">Because Android is an open source project, any manufacturer of hardware for warehouse bar code scanners can build a device to run the Android operating system.</span></span> <span data-ttu-id="9f977-105">デバイスは、Android 実行環境用に作成されたアプリを実行できるのであれば、Android 互換のデバイスのみとなります。</span><span class="sxs-lookup"><span data-stu-id="9f977-105">A device is only Android-compatible if it can run apps that are written for the Android execution environment.</span></span>
<span data-ttu-id="9f977-106">ただし、ハードウェア ベンダーは、ハードウェア上で動作する Android バージョンのオーバーレイを変更して作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9f977-106">However, a hardware vendor can modify and create overlays for the Android version that runs on their hardware.</span></span> <span data-ttu-id="9f977-107">Microsoft は、Android 用モバイル バーコード スキャニングアプリが、メーカーのバーコード スキャニング ハードウェアおよびその上で動作する Android バージョンと互換性があることを確認する責任は負いません。</span><span class="sxs-lookup"><span data-stu-id="9f977-107">Microsoft cannot take any responsibility to ensure that a mobile bar code scanning app for Android is compatible with a manufacturer’s bar code scanning hardware and the Android version that runs on it.</span></span> 

<span data-ttu-id="9f977-108">Microsoft Dynamics 365 for Finance and Operations の倉庫保管アプリは、バーコードスキャン用の Android 搭載端末でテストされています。</span><span class="sxs-lookup"><span data-stu-id="9f977-108">The Warehousing app for Microsoft Dynamics 365 for Finance and Operations has been tested with a selection of Android powered devices for bar code scanning.</span></span> <span data-ttu-id="9f977-109">これらのテストでは、市場で利用可能なデバイスのサンプルのみカバーしています。</span><span class="sxs-lookup"><span data-stu-id="9f977-109">These tests only cover a sample of the devices that are available on the market.</span></span>

<span data-ttu-id="9f977-110">顧客は購入するハードウェアを決定する前に、選択したハードウェアで倉庫モバイル スキャンのアプリケーションをテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="9f977-110">As a customer, we recommend that you test the Warehouse mobile scanning app on selected hardware before you decide on the hardware that you want to buy.</span></span>


