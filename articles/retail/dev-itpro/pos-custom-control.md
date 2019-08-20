---
title: POS ビューへのカスタム コントロールの追加
description: このトピックでは、カスタム コントロールを追加することで、Dynamics 365 for Retail の POS ビューに表示される情報を改善する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-15
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: 4cf1f94009886f648ab550b6537872f6ef5e78bf
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833754"
---
# <a name="add-custom-controls-to-pos-views"></a><span data-ttu-id="af73a-103">POS ビューへのカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="af73a-103">Add custom controls to POS views</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af73a-104">Microsoft Dynamics 365 for Retail POS のビューに表示される情報を改善するために、カスタム コントロールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="af73a-104">To enhance the information that appears in the views in Microsoft Dynamics 365 for Retail POS, you can add custom controls.</span></span> <span data-ttu-id="af73a-105">カスタム コントロールを使用すると、既存の POS のビューにカスタム情報を追加できます。</span><span class="sxs-lookup"><span data-stu-id="af73a-105">A custom control lets you add your own custom information to the existing POS views.</span></span> <span data-ttu-id="af73a-106">カスタム コントロールは、POS 拡張フレームワークを使用して実装できます。</span><span class="sxs-lookup"><span data-stu-id="af73a-106">Custom controls can be implemented by using the POS extension framework.</span></span>

<span data-ttu-id="af73a-107">カート ビューでは、POS 画面レイアウト デザイナーを使用してカスタム コントロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="af73a-107">In Cart view, you can add custom controls by using the POS screen layout designer.</span></span> <span data-ttu-id="af73a-108">この場合、カスタム コントロールを任意の場所までドラッグして、コントロールの高さと幅を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="af73a-108">In this case, you can drag a custom control to a location of your choice, and you can also set the height and width of the control.</span></span> <span data-ttu-id="af73a-109">次に、拡張機能プロジェクトに拡張機能ロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="af73a-109">You then write the extension logic in the extension project.</span></span>

<span data-ttu-id="af73a-110">たとえば、次の図では、3 つのカスタム コントロールは画面レイアウト デザイナーを使用して追加されました。</span><span class="sxs-lookup"><span data-stu-id="af73a-110">For example, in the following illustration, three custom controls were added by using the screen layout designer.</span></span>

![買い物カゴでの POS 画面レイアウト デザイナー](media/pos-custom-control-1.png)

<span data-ttu-id="af73a-112">現在、カート ビューのみでスクリーン レイアウ トデザイナーを使用してカスタム コントロールを追加できます。</span><span class="sxs-lookup"><span data-stu-id="af73a-112">Currently, only Cart view lets you use the screen layout designer to add custom controls.</span></span> <span data-ttu-id="af73a-113">その他のすべての画面については、拡張機能プロジェクトでレイアウトを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="af73a-113">For all other screens, you should do the layout in the extension project.</span></span> <span data-ttu-id="af73a-114">画面レイアウト デザイナーを使用するメリットの 1 つは、画面の任意の場所にカスタム コントロールをドラッグできることです。</span><span class="sxs-lookup"><span data-stu-id="af73a-114">One advantage of using the screen layout designer is that you can drag the custom control wherever you want on the screen.</span></span> <span data-ttu-id="af73a-115">他の画面では、位置は固定されていますが、高さと幅を指定することで位置を変更できます。</span><span class="sxs-lookup"><span data-stu-id="af73a-115">On other screens, the position is fixed, but you can modify the position by specifying the height and width.</span></span>

## <a name="custom-control-matrix"></a><span data-ttu-id="af73a-116">カスタム コントロール マトリックス</span><span class="sxs-lookup"><span data-stu-id="af73a-116">Custom control matrix</span></span>

<span data-ttu-id="af73a-117">次のテーブルは、POS のカスタム コントロールをサポートするビューを示しています。</span><span class="sxs-lookup"><span data-stu-id="af73a-117">The following table shows the views that support custom controls in POS.</span></span>

| <span data-ttu-id="af73a-118">POS ビュー</span><span class="sxs-lookup"><span data-stu-id="af73a-118">POS view</span></span>                   | <span data-ttu-id="af73a-119">カスタム コントロールのサポート</span><span class="sxs-lookup"><span data-stu-id="af73a-119">Supports custom controls</span></span> | <span data-ttu-id="af73a-120">画面レイアウト デザイナーのサポート</span><span class="sxs-lookup"><span data-stu-id="af73a-120">Supports screen layout designer</span></span> |
|----------------------------|--------------------------|---------------------------------|
| <span data-ttu-id="af73a-121">カート ビュー/トランザクション ページ</span><span class="sxs-lookup"><span data-stu-id="af73a-121">Cart view/Transaction page</span></span> | <span data-ttu-id="af73a-122">有</span><span class="sxs-lookup"><span data-stu-id="af73a-122">Yes</span></span>                      | <span data-ttu-id="af73a-123">有</span><span class="sxs-lookup"><span data-stu-id="af73a-123">Yes</span></span>                             |
| <span data-ttu-id="af73a-124">顧客の詳細表示</span><span class="sxs-lookup"><span data-stu-id="af73a-124">Customer details view</span></span>      | <span data-ttu-id="af73a-125">有</span><span class="sxs-lookup"><span data-stu-id="af73a-125">Yes</span></span>                      | <span data-ttu-id="af73a-126">無</span><span class="sxs-lookup"><span data-stu-id="af73a-126">No</span></span>                              |
| <span data-ttu-id="af73a-127">製品詳細表示</span><span class="sxs-lookup"><span data-stu-id="af73a-127">Product details view</span></span>       | <span data-ttu-id="af73a-128">有</span><span class="sxs-lookup"><span data-stu-id="af73a-128">Yes</span></span>                      | <span data-ttu-id="af73a-129">無</span><span class="sxs-lookup"><span data-stu-id="af73a-129">No</span></span>                              |
| <span data-ttu-id="af73a-130">顧客の追加/編集表示</span><span class="sxs-lookup"><span data-stu-id="af73a-130">Customer Add/Edit view</span></span>     | <span data-ttu-id="af73a-131">はい (仕掛品)</span><span class="sxs-lookup"><span data-stu-id="af73a-131">Yes (work in progress)</span></span>   | <span data-ttu-id="af73a-132">無</span><span class="sxs-lookup"><span data-stu-id="af73a-132">No</span></span>                              |
| <span data-ttu-id="af73a-133">アドレスの追加/編集表示</span><span class="sxs-lookup"><span data-stu-id="af73a-133">Address Add/Edit view</span></span>      | <span data-ttu-id="af73a-134">はい (仕掛品)</span><span class="sxs-lookup"><span data-stu-id="af73a-134">Yes (work in progress)</span></span>   | <span data-ttu-id="af73a-135">無</span><span class="sxs-lookup"><span data-stu-id="af73a-135">No</span></span>                              |

> [!NOTE]
> <span data-ttu-id="af73a-136">カスタム コントロールは、次の製品バージョンでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="af73a-136">Custom controls are supported only in the following product versions:</span></span>
> - <span data-ttu-id="af73a-137">**画面レイアウト デザイナーに基づかないビュー:** Microsoft Dynamics 365 for Finance and Operations アプリケーション更新プログラム 3 と Microsoft Dynamics 365 for Retail アプリケーション更新プログラム 3</span><span class="sxs-lookup"><span data-stu-id="af73a-137">**For views that aren't based on the screen layout designer:** Microsoft Dynamics 365 for Finance and Operations App update 3 and Microsoft Dynamics 365 for Retail App update 3</span></span>
> - <span data-ttu-id="af73a-138">**画面レイアウト デザイナーに基づくビュー:** Microsoft Dynamics 365 for Finance and Operations アプリケーション更新プログラム 4 と Microsoft Dynamics 365 for Retail アプリケーション更新プログラム 4</span><span class="sxs-lookup"><span data-stu-id="af73a-138">**For views that are based on the screen layout designer:** Microsoft Dynamics 365 for Finance and Operations App update 4 and Microsoft Dynamics 365 for Retail App update 4</span></span>

## <a name="create-a-custom-control"></a><span data-ttu-id="af73a-139">カスタム コントロールの作成</span><span class="sxs-lookup"><span data-stu-id="af73a-139">Create a custom control</span></span>

<span data-ttu-id="af73a-140">次の例は、既存の POS ビューの 1 つにカスタム コントロールを追加するために拡張機能を使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="af73a-140">The following example shows how you can use extension to add custom controls to one of the existing POS views.</span></span> <span data-ttu-id="af73a-141">この例では、製品の詳細ビューで表示される製品使用可能性についての情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="af73a-141">For this example, we want information about product availability to appear in the product details view.</span></span> <span data-ttu-id="af73a-142">この情報を表示するために、**場所**、**在庫**、**予約**、**注文**の 4 つの列を持つカスタム データ リストを追加します。</span><span class="sxs-lookup"><span data-stu-id="af73a-142">To show this information, we will add a custom data list that has four columns: **Location**, **Inventory**, **Reserved**, and **Ordered**.</span></span> <span data-ttu-id="af73a-143">同じ手順を使用して、POS ビューにその他のカスタム情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="af73a-143">You can use the same procedure to show other custom information in the POS views.</span></span>

1. <span data-ttu-id="af73a-144">開発者仮想マシン (VM) で、Microsoft Visual Studio 2015 を起動します。</span><span class="sxs-lookup"><span data-stu-id="af73a-144">On the developer virtual machine (VM), start Microsoft Visual Studio 2015.</span></span>
2. <span data-ttu-id="af73a-145">**ModernPos.sln** ファイルを RetailSDK\\POS から開きます。</span><span class="sxs-lookup"><span data-stu-id="af73a-145">Open the **ModernPos.sln** file from RetailSDK\\POS.</span></span>
3. <span data-ttu-id="af73a-146">**POS.Extensions** プロジェクトに新しいフォルダーを追加し、**SampleExtensions** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-146">In the **POS.Extensions** project, add a new folder, and name it **SampleExtensions**.</span></span>
4. <span data-ttu-id="af73a-147">新しい **SampleExtensions** フォルダーで、別のフォルダーを追加して **ViewExtensions** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-147">In the new **SampleExtensions** folder, add another folder, and name it **ViewExtensions**.</span></span>
5. <span data-ttu-id="af73a-148">**ViewExtensions** フォルダーで、別のフォルダーを追加して **SimpleProductDetails** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-148">In the **ViewExtensions** folder, add another folder, and name it **SimpleProductDetails**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="af73a-149">ビューを拡張する場合は、ナビゲーションとコードのメンテナンスを容易にするために、フォルダーの名前をビューと同じ名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="af73a-149">If you're extending a view, you should give the folder the same name as the view, to make navigation and code maintenance easier.</span></span>

6. <span data-ttu-id="af73a-150">**SimpleProductDetails** フォルダーで、新しい .html ファイルを追加し、**ProductAvailabilityPanel.html** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-150">In the **SimpleProductDetails** folder, add a new .html file, and name it **ProductAvailabilityPanel.html**.</span></span> <span data-ttu-id="af73a-151">また新しい .ts ファイルを追加し、**ProductAvailabilityPanel.ts** という名前をつけます。</span><span class="sxs-lookup"><span data-stu-id="af73a-151">Also add a new .ts file, and name it **ProductAvailabilityPanel.ts**.</span></span> <span data-ttu-id="af73a-152">.html ファイルで、カスタム コントロールに表示したい情報すべてを追加できます。</span><span class="sxs-lookup"><span data-stu-id="af73a-152">In the .html file, you can add whatever information you want the custom control to show.</span></span> <span data-ttu-id="af73a-153">.ts ファイルで、対応するロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="af73a-153">In the .ts file, you add the corresponding logic.</span></span>

    <span data-ttu-id="af73a-154">カスタム コントロールは、カスタム情報を含む単純な HTML ページです。</span><span class="sxs-lookup"><span data-stu-id="af73a-154">A custom control is a simple HTML page that has your custom information.</span></span>

7. <span data-ttu-id="af73a-155">**ProductAvailabilityPanel.html** ファイルを開いて、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-155">Open the **ProductAvailabilityPanel.html** file, and paste the following code into it.</span></span>

    ```
    <!DOCTYPE html>
    <html lang="en" xmlns="http://www.w3.org/1999/xhtml">
        <head>
            <meta charset="utf-8" />
            <title></title>
        </head>
        <body>
            <!-- Note: The element ID differs from the ID that is generated by the POS extensibility framework. This 'template' ID isn't used by the POS extensibility framework. -->
            <script id="Microsot\_Pos\_Extensibility\_Samples\_ProductAvailabilityPanel" type="text/html">
                <h2 class="marginTop8 marginBottom8" data-bind="text: title"></h2>
                <div class="width400 grow col">
                    <div id="Microsot\_Pos\_Extensibility\_Samples\_ProductAvailabilityPanel\_DataList" data-bind="msPosDataList: dataList"></div>
                </div>
            </script>
        </body>
    </html>
    ```

    <span data-ttu-id="af73a-156">ファイルで、POS データ リスト コントロールを追加して製品の可用性情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="af73a-156">In the file, you add the POS data list control to show the product availability information.</span></span> <span data-ttu-id="af73a-157">また、コントロールの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="af73a-157">You also specify the width of the control.</span></span>

    <span data-ttu-id="af73a-158">完全なコードは RetailSDK\\Code\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\SimpleProductDetails\\ProductAvailabilityPanel.html からコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="af73a-158">You can copy the full code from RetailSDK\\Code\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\SimpleProductDetails\\ProductAvailabilityPanel.html.</span></span>

8. <span data-ttu-id="af73a-159">**ProductAvailabilityPanel.ts** ファイルを開いて、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-159">Open the **ProductAvailabilityPanel.ts** file, and paste the following code into it.</span></span>

    ```
    /**
        SAMPLE CODE NOTICE
        THIS SAMPLE CODE IS MADE AVAILABLE AS IS. MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED,
        OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.
        THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.
        NO TECHNICAL SUPPORT IS PROVIDED. YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.
    **/

    import {
        SimpleProductDetailsCustomControlBase,
        ISimpleProductDetailsCustomControlState,
        ISimpleProductDetailsCustomControlContext
    } from "PosApi/Extend/Views/SimpleProductDetailsView";
    import { ProxyEntities } from "PosApi/Entities";
    import { ArrayExtensions } from "PosApi/TypeExtensions";
    import { DataList, SelectionMode } from "PosUISdk/Controls/DataList";
    ```

    <span data-ttu-id="af73a-160">カスタム ロジックを書くために、POS のアプリケーション プログラミング インターフェイス (API) からコントロールやその他のデータ オブジェクトのリストをインポートしました。</span><span class="sxs-lookup"><span data-stu-id="af73a-160">To write our custom logic, we imported the list of controls and other data objects from the POS application programming interface (API).</span></span>

<span data-ttu-id="af73a-161">次に、コンストラクターを追加して、製品の可用性情報でデータ リストを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af73a-161">Next, you must add the constructor and initialize the data list with the product availability information.</span></span> <span data-ttu-id="af73a-162">この方法で、ページに移動するときに、製品の可用性情報が読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="af73a-162">In this way, when you navigate to the page, the product availability information is loaded.</span></span>

> [!NOTE]
> <span data-ttu-id="af73a-163">ここではソース コードをコピーしませんでしたが、RetailSDK\\Code\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\SimpleProductDetails\\ProductAvailabilityPanel.ts から完全なコードをコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="af73a-163">We didn't copy the source code here, but you can copy the full code from RetailSDK\\Code\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\SimpleProductDetails\\ProductAvailabilityPanel.ts.</span></span>

1. <span data-ttu-id="af73a-164">**SampleExtensions** フォルダーで新しい .json ファイルを追加し、**manifest.json** と名前を付け、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-164">In your **SampleExtensions** folder, add a new .json file, name it **manifest.json**, and paste the following code into it.</span></span>

    ```
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Microsoft",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
            "resources": {
                "supportedUICultures": [ "en-US" ],
                "fallbackUICulture": "en-US",
                "culturesDirectoryPath": "Resources/Strings",
                "stringResourcesFileName": "resources.resjson",
                "cultureInfoOverridesFilePath": "Resources/cultureInfoOverrides.json"
            },
            "extend": {
                "views": {
                    "SimpleProductDetailsView": {
                        "controlsConfig": {
                            "customControls": [
                                {
                                    "controlName": "productAvailabilityPanel",
                                    "htmlPath": "ViewExtensions/SimpleProductDetails/ProductAvailabilityPanel.html",
                                    "modulePath": "ViewExtensions/SimpleProductDetails/ProductAvailabilityPanel"
                                }
                            ]
                        }
                    }
                }
            }
        }
    }
    ```

    <span data-ttu-id="af73a-165">ランタイム中に、マニフェストはカスタム制御が **SimpleProductDetailsView** に追加されたことを POS に通知します。</span><span class="sxs-lookup"><span data-stu-id="af73a-165">During runtime, the manifest informs the POS that a custom control has been added in **SimpleProductDetailsView**.</span></span> <span data-ttu-id="af73a-166">前のコード例では、コントロールを読み込むために POS が必要とするすべてのメタデータを含めました。</span><span class="sxs-lookup"><span data-stu-id="af73a-166">In the preceding code example, we included all the required metadata that the POS requires in order to load the control.</span></span>

    - <span data-ttu-id="af73a-167">**拡張** - 既存の POS 機能の拡張機能があることを POS に通知します。</span><span class="sxs-lookup"><span data-stu-id="af73a-167">**Extend** – Inform the POS that there is an extension for an existing POS feature.</span></span>
    - <span data-ttu-id="af73a-168">**ビュー** – 拡張された既存の POS ビューを指定します。</span><span class="sxs-lookup"><span data-stu-id="af73a-168">**Views** – Specify that an existing POS view is being extended.</span></span>
    - <span data-ttu-id="af73a-169">**名前を表示** – 拡張されているビューを指定します。</span><span class="sxs-lookup"><span data-stu-id="af73a-169">**View Name** – Specify the view that is being extended.</span></span>
    - <span data-ttu-id="af73a-170">**コンフィギュレーションのコントロール** - 追加するコントロールを指定します (例: **カスタム コントロール**)。</span><span class="sxs-lookup"><span data-stu-id="af73a-170">**Controls config** – Specify the control that you are adding, such as **Custom control**.</span></span>
    - <span data-ttu-id="af73a-171">**コントロール メタデータ** - 名前、.html ファイル パスのパス、および typescript モジュールのパス (つまり、.ts ファイル) を指定します。</span><span class="sxs-lookup"><span data-stu-id="af73a-171">**Control metadata** – Specify the name, the path of the .html file path, and the path of the typescript module (that is, the .ts file).</span></span>

3. <span data-ttu-id="af73a-172">**extensions.json** ファイルを開いて、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-172">Open the **extensions.json** file, and paste the following code into it.</span></span>

    ```
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions"
            }
        ]
    }
    ```

    <span data-ttu-id="af73a-173">extensions.json ファイルで、手持ちのさまざまな拡張機能を指定します。</span><span class="sxs-lookup"><span data-stu-id="af73a-173">In the extensions.json file, you specify the various extensions that you have.</span></span> <span data-ttu-id="af73a-174">この場合、新しい拡張フォルダーを追加しました。</span><span class="sxs-lookup"><span data-stu-id="af73a-174">In this case, we added a new extension folder.</span></span> <span data-ttu-id="af73a-175">したがって、そのフォルダーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af73a-175">Therefore, we must specify that folder.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="af73a-176">各拡張子フォルダーまたは指定したパッケージには、マニュフェストが必要です。</span><span class="sxs-lookup"><span data-stu-id="af73a-176">Each extension folder or package that you specify here should have a manifest.</span></span>

4. <span data-ttu-id="af73a-177">**tsconfig.json** ファイルを開いて、拡張子を含めます。</span><span class="sxs-lookup"><span data-stu-id="af73a-177">Open the **tsconfig.json** file, and include your extension.</span></span> <span data-ttu-id="af73a-178">次のコードをファイルに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="af73a-178">Paste the following code into the file.</span></span>

    ```
    "extends": "../tsconfigs/tsmodulesconfig",
    "exclude": [
        // "SampleExtensions"
    ],
    ```

## <a name="test-the-extension"></a><span data-ttu-id="af73a-179">拡張のテスト</span><span class="sxs-lookup"><span data-stu-id="af73a-179">Test the extension</span></span>

1. <span data-ttu-id="af73a-180">F5 キーを押し、POS を展開してカスタマイズをテストします。</span><span class="sxs-lookup"><span data-stu-id="af73a-180">Press F5, and deploy the POS to test your customization.</span></span>
2. <span data-ttu-id="af73a-181">POS が開始された後にサインインします。</span><span class="sxs-lookup"><span data-stu-id="af73a-181">After the POS is started, sign in.</span></span> <span data-ttu-id="af73a-182">次に、任意の製品を検索し、製品詳細ビューを開きます。</span><span class="sxs-lookup"><span data-stu-id="af73a-182">Then search for any product, and open to product details view.</span></span> <span data-ttu-id="af73a-183">追加したカスタム コントロールが表示されました。</span><span class="sxs-lookup"><span data-stu-id="af73a-183">You should now see the custom control that you added.</span></span> <span data-ttu-id="af73a-184">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="af73a-184">Here is an example.</span></span>

    ![製品の詳細ビューに表示された製品の可用性情報](media/pos-custom-control-2.png)

<span data-ttu-id="af73a-186">このサンプルの完全なコードは RetailSDK\\Code\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\SimpleProductDetails からコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="af73a-186">You can copy the full code for this sample from RetailSDK\\Code\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\SimpleProductDetails.</span></span>
