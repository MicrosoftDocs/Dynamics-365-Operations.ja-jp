---
title: Visual Studio 用のツールおよびアドイン
description: このトピックでは、Microsoft Visual Studio に追加されたアドイン インフラストラクチャを説明し、開発者が開発ツールをより簡単に追加できるようにします。
author: RobinARH
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 27521
ms.assetid: a73c64e1-7e24-4845-b5da-35b1678ddb60
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26752d72c4c10a1c252b615d06d568b7bbd6fd52
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191692"
---
# <a name="tools-add-ins-for-visual-studio"></a><span data-ttu-id="53fda-103">Visual Studio 用のツールおよびアドイン</span><span class="sxs-lookup"><span data-stu-id="53fda-103">Tools add-ins for Visual Studio</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53fda-104">このトピックでは、Microsoft Visual Studio に追加されたアドイン インフラストラクチャを説明し、開発者が開発ツールをより簡単に追加できるようにします。</span><span class="sxs-lookup"><span data-stu-id="53fda-104">This topic reviews the Add-ins infrastructure that has been added to Microsoft Visual Studio, so that developers can more easily add tools for development.</span></span>

<span data-ttu-id="53fda-105">開発をサポートするため、数多くの優れたツールが Microsoft Visual Studio に追加されました。</span><span class="sxs-lookup"><span data-stu-id="53fda-105">A lot of great tools have been added to Microsoft Visual Studio to support development.</span></span> <span data-ttu-id="53fda-106">ただし、特定の要件を満たすため、追加のツールが常にあります。</span><span class="sxs-lookup"><span data-stu-id="53fda-106">However, there will always be additional tools to meet specific requirements.</span></span> <span data-ttu-id="53fda-107">これらの追加ツールを簡単に追加できるように、開発者向けに**アドイン** インフラストラクチャが提供されています。</span><span class="sxs-lookup"><span data-stu-id="53fda-107">To make it easier to add these additional tools, an **Add-ins** infrastructure has been provided for developers.</span></span> <span data-ttu-id="53fda-108">追加ツールが、次の 2 つの場所に用意されています。</span><span class="sxs-lookup"><span data-stu-id="53fda-108">The additional tools are available in two places:</span></span>

-   <span data-ttu-id="53fda-109">**Dynamics 365** メニューで **アドイン** サブメニューをポイントします。</span><span class="sxs-lookup"><span data-stu-id="53fda-109">The **Add-ins** submenu on the **Dynamics 365** menu</span></span>
-   <span data-ttu-id="53fda-110">要素デザイナーのショートカット メニューの **アドイン** サブメニュー</span><span class="sxs-lookup"><span data-stu-id="53fda-110">The **Add-ins** submenu on the shortcut menu in the element designer</span></span>

<span data-ttu-id="53fda-111">独自のアドインを簡単に作成できるようにするには、Visual Studioで新規プロジェクトを作成するときに **Dynamics 開発者ツール アドイン** プロジェクト タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="53fda-111">To make it easier to create your own add-ins, you can select the **Dynamics Developer Tools Add-in** project type when you create a new project in Visual Studio.</span></span> <span data-ttu-id="53fda-112">このプロジェクト タイプには、アドインを実装するために必要なインフラストラクチャがあります。</span><span class="sxs-lookup"><span data-stu-id="53fda-112">This project type has the infrastructure that is required to implement an add-in.</span></span>

<span data-ttu-id="53fda-113">アドインの詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53fda-113">For more information on add-ins, see:</span></span>
- [<span data-ttu-id="53fda-114">フォーム パターン アドイン</span><span class="sxs-lookup"><span data-stu-id="53fda-114">Form pattern add-ins</span></span>](../user-interface/form-pattern-add-ins.md)
