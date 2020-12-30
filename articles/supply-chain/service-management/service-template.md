---
title: サービス テンプレート
description: サービス合意をテンプレートとして定義し、後でテンプレート行を別のサービス合意やサービス注文にコピーできます。
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8a92d67afe5fd427d1bc272c59e459cb1547d22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431644"
---
# <a name="service-templates"></a><span data-ttu-id="0a693-103">サービス テンプレート</span><span class="sxs-lookup"><span data-stu-id="0a693-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a693-104">サービス合意をテンプレートとして定義し、後でテンプレート行を別のサービス合意やサービス注文にコピーできます。</span><span class="sxs-lookup"><span data-stu-id="0a693-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="0a693-105">例</span><span class="sxs-lookup"><span data-stu-id="0a693-105">Example</span></span>

<span data-ttu-id="0a693-106">サービスの提供先の顧客は、5 つの異なる場所で同一の業務用エレベータを使用しています。</span><span class="sxs-lookup"><span data-stu-id="0a693-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="0a693-107">この顧客向けの 5 つのサービス合意を、各サイトに 1 つずつ設定するとします。</span><span class="sxs-lookup"><span data-stu-id="0a693-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="0a693-108">設定作業の繰り返しを省き、サービス合意の設定情報が同一になるようにするために、サービス合意を 1 つ作成して、各エレベータのサービス作業のテンプレートとして指定します。</span><span class="sxs-lookup"><span data-stu-id="0a693-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="0a693-109">これにより、テンプレート行を 5 つの新しいサービス合意にコピーし、その行を使用してサービス合意を設定できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0a693-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="0a693-110">テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="0a693-110">Create a template</span></span>

<span data-ttu-id="0a693-111">サービス テンプレートを作成する際には、サービス合意を作成してから、必要な行をサービス合意に作成して、サービス合意をサービス テンプレート グループに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="0a693-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="0a693-112">サービス合意は、サービス注文が関連付けられていない場合にのみ、テンプレートとして定義できます。</span><span class="sxs-lookup"><span data-stu-id="0a693-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="0a693-113">また、テンプレートとして定義したサービス合意からサービス注文を生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="0a693-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="0a693-114">テンプレートの行のコピー</span><span class="sxs-lookup"><span data-stu-id="0a693-114">Copy template lines</span></span>

<span data-ttu-id="0a693-115">サービス テンプレート行は、別のサービス合意またはサービス注文にコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="0a693-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="0a693-116">テンプレート行をサービス注文またはサービス合意にコピーすると、各テンプレート グループを展開可能なツリー ビューにテンプレート グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a693-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="0a693-117">これにより、各テンプレートとテンプレート行を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="0a693-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="0a693-118">テンプレートの用途を表す名前でテンプレートをグループ化すると、コピーするサービス テンプレート行を簡単に特定できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0a693-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a693-119">関連トピック</span><span class="sxs-lookup"><span data-stu-id="0a693-119">Related topics</span></span>

[<span data-ttu-id="0a693-120">サービス テンプレート行のコピー</span><span class="sxs-lookup"><span data-stu-id="0a693-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
