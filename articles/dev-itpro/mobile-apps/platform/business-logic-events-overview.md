---
title: ビジネス ロジック イベント
description: ビジネス ロジックで実行されるコードは、ページ、アクション、コントロールのメタデータにランタイム変更を加えることができます。
author: makhabaz
manager: AnnBe
ms.date: 08/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 0107a49e22b03492421b00296df2cafb4c29a8cd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537337"
---
# <a name="business-logic-events"></a><span data-ttu-id="8ffdf-103">ビジネス ロジック イベント</span><span class="sxs-lookup"><span data-stu-id="8ffdf-103">Business logic events</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ffdf-104">モバイル ワークスペースのビジネス ロジック イベントは、開発者が能力を高めるためにワークスペースの構成を指定する場所を提供し、業務シナリオ固有の動作を実装します。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-104">Mobile workspace business logic events provide places for developers to specify workspace configuration to enhace capability, and implement business-scenario-specific behaviors.</span></span> <span data-ttu-id="8ffdf-105">モバイル アプリのプロセスで、すべてのモバイル ビジネス ロジックを実行した場合、ビジネス ロジック実行フローは Operations モバイル アプリ フレームワークによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-105">All mobile business logic executes in the process of the mobile app, and busines logic execution flow is controlled by the Operations mobile app framework.</span></span> 

<span data-ttu-id="8ffdf-106">ビジネス ロジックで実行されるコードは、ページ、アクション、コントロールのメタデータにランタイム変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-106">Code that executes in business logic can make runtime modifications to the metadata of Pages, Actions and Controls.</span></span> <span data-ttu-id="8ffdf-107">これらの実行時の変更は、アプリにキャッシュされている静的メタデータをオーバーレイしますが、変更はキャッシュされた静的メタデータを直接変更するものではなく、サーバーに格納されている静的メタデータにも影響しません。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-107">These runtime modifications will overlayer the static metadata that is cached in the app, but the modifications do not directly change the cached static metadata, nor do they affect the static metadata that is stored on the server.</span></span> <span data-ttu-id="8ffdf-108">これらのランタイム変更は、アプリケーションが終了するまで続きます。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-108">These runtime modifications only persist until the app is closed.</span></span> 

<span data-ttu-id="8ffdf-109">アプリケーションのビジネス ロジックで実行されるコードは、アプリケーションに格納されているビジネス データにランタイム変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-109">Code that executes in the business logic of the app can make runtime modifications to business data that is stored in the app.</span></span> <span data-ttu-id="8ffdf-110">これらの変更 (正しいプラクティスに従って実行される場合) は、アプリ内の他のビジネス データとして通常のデータ処理フレームワークに参加します。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-110">These modifications (when performed according to correct practices) participate in the normal data processing framework as other business data in the app.</span></span> <span data-ttu-id="8ffdf-111">これは、オフライン優先機能とフレームワークによって提供される非同期保存動作に従うことを意味します。</span><span class="sxs-lookup"><span data-stu-id="8ffdf-111">That means adhering to the offline-first capabilities and asycnrhonous save behaviors provided by the framework.</span></span>

