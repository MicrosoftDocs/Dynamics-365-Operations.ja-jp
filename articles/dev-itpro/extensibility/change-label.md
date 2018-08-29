---
title: "ラベル拡張ファイルを使用してラベルを変更します"
description: "このトピックでは、ラベル拡張ファイルを作成してラベルの文字列値を変更する方法、同じラベル ファイルに新しいラベルを追加する方法、または新しい言語を追加する方法について説明します。"
author: smithanataraj
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 5e6856476e532e7e50f656f0e64d013d0e5aa03c
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="change-labels-by-using-label-extension-files"></a><span data-ttu-id="e6a5d-103">ラベル拡張ファイルを使用してラベルを変更します</span><span class="sxs-lookup"><span data-stu-id="e6a5d-103">Change labels by using label extension files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6a5d-104">ラベルの文字列値を変更、同じラベル ファイルに新しいラベルを追加、または新しい言語を追加する、ラベル拡張ファイルを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-104">You can create label extension files to modify the string value of a label, add new labels to the same label file, or add new languages.</span></span> <span data-ttu-id="e6a5d-105">ラベル拡張ファイルの名前は、ラベル ファイルの名前に **\_extension** の接尾語を加えたものでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-105">The name of a label extension file must consist of the name of the label file plus the **\_extension** suffix.</span></span> 

<span data-ttu-id="e6a5d-106">次の例は、AccountsPayable ラベルファイルを拡張して、ウェールズ語を新しい言語として追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-106">The following example shows how to extend the AccountsPayable label file to add Welsh as a new language.</span></span>
 
1. <span data-ttu-id="e6a5d-107">新しいラベル拡張を追加する必要があるモデルに属するプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-107">Create a project that belongs to the model where you must add the new label extension.</span></span> <span data-ttu-id="e6a5d-108">この例では、プロジェクトは **ApplicationSuite** と名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-108">For this example, the project is named **ApplicationSuite**.</span></span>
1. <span data-ttu-id="e6a5d-109">プロジェクトに新しいラベル ファイルを追加し、**AccountsPayable_Extension** という名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-109">Add a new label file to the project, and name it **AccountsPayable_Extension**.</span></span> <span data-ttu-id="e6a5d-110">ラベル ファイルを追加した後、**ラベル ファイル** ウィザードが起動します。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-110">After you add the label file, the **Label file** wizard starts.</span></span>

    ![ラベル ファイル ウィザード: ラベル ファイル ID ページの指定](media/ExtendLabel01.png)

2. <span data-ttu-id="e6a5d-112">ウィザードの次のページで、拡張機能の一部となる言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-112">On the next page of the wizard, select the languages that should be part of the extension.</span></span> <span data-ttu-id="e6a5d-113">この例では、**英語 (米国)** (**EN-US**) が既に基本言語となっており、**ウェールズ語** (**cy**) を追加しました。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-113">In this example, **English (United States)** (**en-US**) was already the base language, and we added **Welsh** (**cy**).</span></span>

    ![ラベル ファイル ウィザード: 言語ページの選択](media/ExtendLabel02.png)

3. <span data-ttu-id="e6a5d-115">ウィザードの操作を完了します。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-115">Complete the wizard.</span></span> <span data-ttu-id="e6a5d-116">次の図に示すように、2 つのラベル拡張ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-116">Two label extension files are created, as shown in the following illustration.</span></span>

    ![ラベル拡張ファイル](media/ExtendLabel03.png)

4. <span data-ttu-id="e6a5d-118">この例の拡張ファイルでは、新しいラベルを作成したり、アプリケーション スイート モデルの **AccountsPayable** で定義されているラベルの値を変更したりできます。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-118">In the extension file in this example, you can create new labels or modify the value of labels that are defined in the **AccountsPayable** label file of the Application Suite model.</span></span> <span data-ttu-id="e6a5d-119">新しいラベルを定義するか、既に存在するラベルを再定義するには、標準のラベル エディタを使用します。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-119">Use the standard label editor to define new labels or redefine labels that already exist.</span></span>
5. <span data-ttu-id="e6a5d-120">任意の時点で、ラベル ファイルにその他の言語を追加できます。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-120">At any point, you can add more languages to a label file.</span></span> <span data-ttu-id="e6a5d-121">プロジェクトで名前が **\_extension** で終わるラベル ファイルを右クリックしてから、**新しい言語の追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-121">In your project, right-click a label file that has a name that ends in **\_extension**, and then select **Add new languages**.</span></span> <span data-ttu-id="e6a5d-122">その後、翻訳ファイルを追加するウィザードに従います。</span><span class="sxs-lookup"><span data-stu-id="e6a5d-122">Then follow the wizard to add the translation files.</span></span>

