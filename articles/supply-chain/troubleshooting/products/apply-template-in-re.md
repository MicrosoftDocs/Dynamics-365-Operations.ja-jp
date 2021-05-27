---
title: リリースされた製品にテンプレートを適用できない
description: リリースされた製品にテンプレートを適用できない。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026670"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="35aa8-103">リリースされた製品を作成するためにテンプレートを適用できない</span><span class="sxs-lookup"><span data-stu-id="35aa8-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="35aa8-104">KB 番号: 4612097</span><span class="sxs-lookup"><span data-stu-id="35aa8-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="35aa8-105">現象</span><span class="sxs-lookup"><span data-stu-id="35aa8-105">Symptoms</span></span>

<span data-ttu-id="35aa8-106">**新しいリリースされた製品** ダイアログ ボックスを使用して新しいリリース済製品を作成する場合は、テンプレートを選択できます。</span><span class="sxs-lookup"><span data-stu-id="35aa8-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="35aa8-107">このテンプレートは、新しいリリースされた製品の多くのフィールドに対する既定の設定を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35aa8-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="35aa8-108">ただし、テンプレートを選択した後は、フィールドの一部またはすべてが設定されていないフィールドです。</span><span class="sxs-lookup"><span data-stu-id="35aa8-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="35aa8-109">原因</span><span class="sxs-lookup"><span data-stu-id="35aa8-109">Cause</span></span>

<span data-ttu-id="35aa8-110">Microsoft Dynamics 365 Supply Chain Management の多くのページでは、それらのページに表示されるレコードの初期設定を確立するテンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="35aa8-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="35aa8-111">これらのテンプレートの 1 つを作成するには、アクション ペインの **オプション** タブで **レコード** 情報を選択します。</span><span class="sxs-lookup"><span data-stu-id="35aa8-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="35aa8-112">ただし、リリースされた製品は他のほとんどのタイプのレコードよりずっと複雑です。</span><span class="sxs-lookup"><span data-stu-id="35aa8-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="35aa8-113">**リリースされた製品** ページで **レコード情報** を選択してテンプレートを作成することもできますが、リリースされた製品を作成するときにそのテンプレートを選択することもできますが、このテンプレートは、新しいリリース済製品の予想されるフィールド値を提供しません。</span><span class="sxs-lookup"><span data-stu-id="35aa8-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="35aa8-114">そのため、リリースされた製品には "レコード情報" テンプレートを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="35aa8-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="35aa8-115">代わりに、専用の製品テンプレートを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35aa8-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="35aa8-116">解像度</span><span class="sxs-lookup"><span data-stu-id="35aa8-116">Resolution</span></span>

<span data-ttu-id="35aa8-117">製品テンプレートを作成するには、**オプション** タブの **レコード情報** ボタンではなく、アクション ペインの **製品** タブの **テンプレート** メニューを使用します。</span><span class="sxs-lookup"><span data-stu-id="35aa8-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="35aa8-118">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="35aa8-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="35aa8-119">アクション ペインの **製品** タブの **新規** グループで、**テンプレート** を選択し、必要に応じて **個人テンプレートの作成** または **共有テンプレートの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="35aa8-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
