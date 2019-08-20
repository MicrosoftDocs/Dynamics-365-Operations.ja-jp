---
title: フォーム パターンをサポートしている Visual Studio アドイン
description: Visual Studio のツールには、パターンの使用をサポートするいくつかのアドインが含まれています。
author: jasongre
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 28891
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ffa9e3c8f91c417634bfcdbece7a6b33799b1e77
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851159"
---
# <a name="visual-studio-add-ins-that-support-form-patterns"></a><span data-ttu-id="ac88d-103">フォーム パターンをサポートしている Visual Studio アドイン</span><span class="sxs-lookup"><span data-stu-id="ac88d-103">Visual Studio add-ins that support form patterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac88d-104">Visual Studio のツールには、パターンの使用をサポートするいくつかのアドインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac88d-104">The tools for Visual Studio include a number of add-ins that support pattern usage.</span></span> 

## <a name="form-statistics-add-in"></a><span data-ttu-id="ac88d-105">フォーム統計アドイン</span><span class="sxs-lookup"><span data-stu-id="ac88d-105">Form statistics add-in</span></span>
<span data-ttu-id="ac88d-106">**フォーム統計情報** アドインは、フォームのパターン使用状況の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac88d-106">The **Form statistics** add-in provides a summary of the pattern usage for forms.</span></span> <span data-ttu-id="ac88d-107">**Dynamics 365** メニューから **フォームの統計情報** アドインにアクセスすると、すべてのフォームの統計情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="ac88d-107">When you access the **Form statistics** add-in from the **Dynamics 365** menu, it displays statistics for all forms.</span></span> <span data-ttu-id="ac88d-108">フォーム デザイナーで開いているフォームのショートカット メニューからアドインにアクセスしたとき、アドインにそのフォームのみの統計情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ac88d-108">When you access the add-in from the shortcut menu for a form that is open in the form designer, it displays statistics for that form only.</span></span> 

![フォーム統計レポート](media/form-statistics.png) 

## <a name="forms-pattern-report"></a><span data-ttu-id="ac88d-110">フォームのパターン レポート</span><span class="sxs-lookup"><span data-stu-id="ac88d-110">Forms Pattern report</span></span>
<span data-ttu-id="ac88d-111">**フォーム パターン**レポートは、フォームがトップレベル フォーム パターンを使用するかどうか、ユーザー定義のフォームかどうか、フォーム パターンを指定しないかどうかなど、すべてのフォームについてのパターン情報を示します。</span><span class="sxs-lookup"><span data-stu-id="ac88d-111">The **Form Patterns** report provides pattern information about every form, including whether the form uses a top-level form pattern, is a custom form, or is not specifying a form pattern.</span></span> <span data-ttu-id="ac88d-112">**フォーム パターン** レポートを生成するには、Microsoft Visual Studio を起動し、**DYNAMICS 365**  メニューをクリックし、**アドイン** を展開してから **フォーム パターン レポートを実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ac88d-112">To generate the **Form Patterns** report, start Microsoft Visual Studio, click the **DYNAMICS 365** menu, expand **Add-ins**, and then click **Run the form patterns report**.</span></span> <span data-ttu-id="ac88d-113">このプロセスは数秒かかります。</span><span class="sxs-lookup"><span data-stu-id="ac88d-113">The process will take several seconds.</span></span> <span data-ttu-id="ac88d-114">レポートが生成されると、ダイアログ ボックスにレポートの場所を提供します。</span><span class="sxs-lookup"><span data-stu-id="ac88d-114">After the report has been generated, a dialog box will provide the location of the report.</span></span><span data-ttu-id="ac88d-115">指定された場所を参照し、Microsoft Excel でファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="ac88d-115"> Browse to the specified location, and open the file in Microsoft Excel.</span></span><span data-ttu-id="ac88d-116">興味のあるモデルまでレポートをフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="ac88d-116"> You can then filter the report down to the models that interest you.</span></span>

<span data-ttu-id="ac88d-117">Visual Studio アドインの詳細については、[Visual Studio 用のツールおよびアドイン](../dev-tools/developer-tools-add-ins.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ac88d-117">For more information about Visual Studio add-ins, see [Tools add-ins for Visual Studio](../dev-tools/developer-tools-add-ins.md).</span></span>
