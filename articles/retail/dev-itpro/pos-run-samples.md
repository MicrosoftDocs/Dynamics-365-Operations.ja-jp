---
title: "Retail POS サンプルの実行"
description: "このトピックでは、Retail POS サンプルを実行する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ace4878b53904bb581630ba135a95307521332ff
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="run-retail-pos-samples"></a><span data-ttu-id="73775-103">Retail POS サンプルの実行</span><span class="sxs-lookup"><span data-stu-id="73775-103">Run Retail POS samples</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73775-104">小売用拡張機能を示す Retail SDK にはいくつかのサンプルがあります。</span><span class="sxs-lookup"><span data-stu-id="73775-104">There are several samples in the Retail SDK that demonstrate retail extensions.</span></span> <span data-ttu-id="73775-105">このトピックでは、これらのサンプルを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="73775-105">This topic explains how to run these samples.</span></span> 

<span data-ttu-id="73775-106">このトピックは、プラットフォーム更新プログラム 8 および Retail アプリケーション更新プログラム 4 修正プログラムを備えた、Dynamics 365 for Finance and Operations、および Dynamics 365 for Retail に適用されます。</span><span class="sxs-lookup"><span data-stu-id="73775-106">This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</span></span>

## <a name="run-the-sampleextensions-in-pos"></a><span data-ttu-id="73775-107">POS で SampleExtensions を実行</span><span class="sxs-lookup"><span data-stu-id="73775-107">Run the SampleExtensions in POS</span></span>
1. <span data-ttu-id="73775-108">**Retail SDK\\POS** フォルダーから **ModernPos.Sln** あるいは **CloudPos.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="73775-108">Open **ModernPos.Sln** or **CloudPos.sln** from the **Retail SDK\\POS** folder.</span></span>
2. <span data-ttu-id="73775-109">ソリューションで **POS 拡張機能** プロジェクトを選択し、**ファイルをすべて表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="73775-109">Select the **POS.Extensions** project in the solution and click **Show All Files**.</span></span>
3. <span data-ttu-id="73775-110">**SampleExtensions** フォルダーを右クリックし、**プロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73775-110">Right-click the **SampleExtensions** folder and select **Include in Project**.</span></span>
4. <span data-ttu-id="73775-111">**SampleExtensions2** フォルダーを右クリックし、**プロジェクトに追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="73775-111">Right-click the **SampleExtensions2** folder and select **Include in Project**.</span></span>
5. <span data-ttu-id="73775-112">**extensions.json** ファイルを開いて、**SampleExtensions** および **SampleExtensions2** の拡張フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="73775-112">Open the **extensions.json** file and add the extension folder for **SampleExtensions** and **SampleExtensions2**.</span></span> <span data-ttu-id="73775-113">これは、実行時に POS にこの拡張が含まれることを意味します。</span><span class="sxs-lookup"><span data-stu-id="73775-113">This means that during runtime POS will include this extension.</span></span> <span data-ttu-id="73775-114">**baseUrl** 値は、相対パスおよび拡張子フォルダーの名前に完全に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="73775-114">The **baseUrl** value must exactly match the relative path and extension folder name.</span></span>

    ```Typescript
    {
        "extensionPackages": [
            {
                "baseUrl": " SampleExtensions"
            },
            {
                "baseUrl": " SampleExtensions2"
            }
        ] 
    }
    ```
    > [!Note]  
    > <span data-ttu-id="73775-115">extension.json ファイルには、2 つ以上の拡張機能フォルダーを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="73775-115">In the extension.json file you must include at least two extension folders.</span></span> <span data-ttu-id="73775-116">拡張子フォルダーを 1 つだけ追加する場合は、POS は拡張子を読み込みません。</span><span class="sxs-lookup"><span data-stu-id="73775-116">If you add only one extension folder, then POS will not load the extension.</span></span>
5. <span data-ttu-id="73775-117">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="73775-117">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="73775-118">POS は、拡張機能をコンパイルするかどうかを決定するために、このファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="73775-118">POS will use this file to determine whether to compile the extension.</span></span> <span data-ttu-id="73775-119">既定では、リストにサンプル拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="73775-119">By default, the list contains the sample extensions list.</span></span> <span data-ttu-id="73775-120">POS に拡張子をコンパイルする場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。</span><span class="sxs-lookup"><span data-stu-id="73775-120">If you want to compile any extension to the POS, then you need add the extension folder name and comment out the extension from the extension as shown below.</span></span> 

    ```Typescript
    {
        "extends": "../tsconfigs/tsmodulesconfig",
        "exclude": [
            "AuditEventExtensionSample"
            , "B2BSample"
            ,"CustomerSearchWithAttributesSample"
            ,"FiscalRegisterSample"
            ,"PaymentSample"
            ,"PromotionsSample"
            ,"SalesTransactionSignatureSample"
            // ,"SampleExtensions"
            // ,"SampleExtensions2"
            ,"StoreHoursSample"
            ,"SuspendTransactionReceiptSample"
        ],
        "compilerOptions": {
            // There is an unexpected behavior for TypeScript 2.2.2 in map and source roots generated in compiled JS and map files. 
            // The following may change in future TypeScript versions.
            // In case there is only one top level extensions folder with .ts files included, the following two root 
            // directories need to be changed to include the extensions folder.
            // For example, change both roots to "./SampleExtensions" if "SampleExtensions" folder is the only top level 
            // folder that has .ts files included in the project.
            // That is, either "SampleExtensions" folder is the only top level folder, or all other top level folders 
            // have .js files only, no .ts files.
            "mapRoot": "./", /* Cannot be specified in base file. Adds full path to ".map" in the js file to enable debug in VS. */
            "sourceRoot": "./" /* Cannot be specified in base file. Adds full path to ".ts" in the map file to enable debug in VS. */
        }
    }
    ```
    <span data-ttu-id="73775-121">他の拡張子を有効にする場合は、除外リストからそれらをコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="73775-121">If you want to enable other extensions, comment them out from the exclude list.</span></span> <span data-ttu-id="73775-122">たとえば、**B2BSample** を含める場合、コードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="73775-122">For example, if you want to include **B2BSample**, the code would be as follows.</span></span> 
    
    ```Typescript
    "exclude": [
        "AuditEventExtensionSample"
        // ,"B2BSample"
        ,"CustomerSearchWithAttributesSample"
        ,"FiscalRegisterSample"
        ,"PaymentSample"
        ,"PromotionsSample"
        ,"SalesTransactionSignatureSample"
        // ,"SampleExtensions"
        // ,"SampleExtensions2"
        ,"StoreHoursSample"
        ,"SuspendTransactionReceiptSample"
    ],
    ```
    > [!Note] 
    > <span data-ttu-id="73775-123">その他の拡張機能パッケージ フォルダーは、Visual Studioプロジェクトに含まれていない場合でも、追加する予定でない場合は除外リストに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="73775-123">Other extension package folders, even though not included in the Visual Studio project, should be kept in the exclude list if they are not meant to be included.</span></span>
6. <span data-ttu-id="73775-124">検証のために Modern POS を使用している場合、**ソリューション プラットフォーム** を **x86** に、**オプションの配置** を **ローカル コンピューター** または **シミュレーター** に設定します。</span><span class="sxs-lookup"><span data-stu-id="73775-124">Set **Solution platform** to **x86** and **Deploy option** to **Local Machine** or **Simulator** if you are using Modern POS for validation.</span></span>
7. <span data-ttu-id="73775-125">**すべて保存**をクリックし、**F5** キーを押して拡張機能を検証します。</span><span class="sxs-lookup"><span data-stu-id="73775-125">Click **Save all** and press the **F5** key to validate the extensions.</span></span>

    > [!Note] 
    > <span data-ttu-id="73775-126">クラウド POS では、Visual Studio できれいな解決策を使用して、ソリューションを再構築します。</span><span class="sxs-lookup"><span data-stu-id="73775-126">For cloud POS, use a clean solution in Visual Studio, and then rebuild the solution.</span></span>
8. <span data-ttu-id="73775-127">製品の検索画面に移動、または上部の検索バーを使用して製品を検索します。</span><span class="sxs-lookup"><span data-stu-id="73775-127">Go to the product search screen or use the top search bar to search for a product.</span></span> <span data-ttu-id="73775-128">グリッドおよび新しいアプリケーション バーのボタンのカスタム列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="73775-128">You should see custom columns in the grid and new app bar buttons.</span></span>

