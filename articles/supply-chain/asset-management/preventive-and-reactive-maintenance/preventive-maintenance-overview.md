---
title: 予防的メンテナンスの概要
description: このトピックでは、資産管理における予防的メンテナンスについて説明します。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8949f9b26917c4a93faa5aea74faa0b6735d770f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206015"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="1bc09-103">予防的メンテナンスの概要</span><span class="sxs-lookup"><span data-stu-id="1bc09-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1bc09-104">このトピックでは、資産管理における予防的メンテナンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1bc09-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="1bc09-105">予防的メンテナンスは、通常のサービス、調整、検査など、計画されたメンテナンス作業を含む訓練分野です。</span><span class="sxs-lookup"><span data-stu-id="1bc09-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="1bc09-106">**資産管理**で、メンテナンス計画を作成し、資産と機能の場所に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="1bc09-107">メンテナンス ラウンドを機能の場所に設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="1bc09-108">資産のメンテナンス計画は、資産が導入されている場所に関係なく有効です。</span><span class="sxs-lookup"><span data-stu-id="1bc09-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="1bc09-109">機能の場所にあるメンテナンス計画とメンテナンス ラウンドは、現在その場所に導入されている資産に対して有効です。</span><span class="sxs-lookup"><span data-stu-id="1bc09-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="1bc09-110">資産に対してメンテナンス計画を設定したり、機能の場所にメンテナンス ラウンドを設定する代わりに、同じ作業ルーティンのメンテナンス作業タイプに関連して実行する必要のある複数の資産が含まれるメンテナンス ラウンドを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="1bc09-111">(機能の場所で作成される代わりに) 資産から作成されたメンテナンス ラウンドの場合、1 つのメンテナンス ラウンドに対して、同じ機能の場所に導入されていない、複数の資産を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="1bc09-112">メンテナンス計画は、個別資産に対する予防的および再有効化のメンテナンスを行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="1bc09-113">メンテナンス ラウンドは、グループまたは一連の資産に対する予防的メンテナンスを行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="1bc09-114">メンテナンス計画およびメンテナンス ラウンドは、作業指示書の提案の生成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="1bc09-115">作業指示書の提案はメンテナンス スケジュールの明細行として保存されます。これはバンドルし、作業指示書に変換できます。</span><span class="sxs-lookup"><span data-stu-id="1bc09-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="1bc09-116">次の図は、メンテナンス計画とメンテナンス ラウンドからそれらのメンテナンス計画とメンテナンス ラウンドに基づいて資産の作業指示書を作成するワーク フローの概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="1bc09-116">The following illustration provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![図 1](media/01-preventive-maintenance.png)

