---
title: 倉庫の設定のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management で倉庫を設定する際に発生する可能性がある一般的な問題の修正方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f2e111930431e908e5aaa2f08d04adbb2d952f0f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208114"
---
# <a name="troubleshoot-warehouse-setup"></a><span data-ttu-id="66362-103">倉庫の設定のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="66362-103">Troubleshoot warehouse setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66362-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management で倉庫を設定する際に発生する可能性がある一般的な問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="66362-104">This topic describes how to fix common issues that you might encounter while you set up warehouses in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-use-any-role-except-administrator-to-access-the-mobile-device-app-emulator"></a><span data-ttu-id="66362-105">管理者以外の役割を使用して、モバイル デバイスのアプリ エミュレーターにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="66362-105">I can't use any role except administrator to access the mobile device app emulator.</span></span>

### <a name="issue-description"></a><span data-ttu-id="66362-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="66362-106">Issue description</span></span>

<span data-ttu-id="66362-107">管理者の役割以外の役割を使用して、モバイル デバイスのアプリ エミュレーターにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="66362-107">You can't any use role except the administrator tole to access the mobile device app emulator.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="66362-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="66362-108">Issue resolution</span></span>

<span data-ttu-id="66362-109">モバイル デバイスのアプリ エミュレーターは、管理者アカウントでのみ機能するように設定されています。</span><span class="sxs-lookup"><span data-stu-id="66362-109">The mobile device app emulator is set to work only with the administrator account.</span></span> <span data-ttu-id="66362-110">すべてのテストとライブ プロセスの目的では、倉庫アプリ自体を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="66362-110">For all testing and live process purposes, we recommend that you use the warehouse app itself.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]