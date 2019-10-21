---
title: 販売時点管理 (POS) トランザクション グリッドへのカスタム列の追加
description: このトピックでは、画面レイアウト デザイナーを使用して POS トランザクション ページに新しいカスタム列を追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/09/2018
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
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: d701629db166dae3f07825e69c96e28e0c6c8eaa
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025537"
---
# <a name="add-custom-columns-to-a-point-of-sale-pos-transaction-grid"></a><span data-ttu-id="f2298-103">販売時点管理 (POS) トランザクション グリッドへのカスタム列の追加</span><span class="sxs-lookup"><span data-stu-id="f2298-103">Add custom columns to a point of sale (POS) transaction grid</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2298-104">このトピックでは、画面レイアウト デザイナーを使用して POS トランザクション ページに新しいカスタム列を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2298-104">This topic explains how to add a new custom column to a POS transaction page using the screen layout designer.</span></span> <span data-ttu-id="f2298-105">カスタム列フィーチャーを使用して、トランザクション ページにさらに情報を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f2298-105">You can add more information to a transaction page by using the custom column feature.</span></span> <span data-ttu-id="f2298-106">カスタム列は、画面レイアウト デザイナーを使用して、トランザクションのページ入庫グリッドに追加できます。</span><span class="sxs-lookup"><span data-stu-id="f2298-106">A custom column can be added to the transaction page receipt grid by using the screen layout designer.</span></span> <span data-ttu-id="f2298-107">デザイナーを使用して、列の幅および配置を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="f2298-107">You can adjust the width and position of the columns by using the designer.</span></span> <span data-ttu-id="f2298-108">拡張シナリオのレイアウトには、10 個のカスタム列があります。</span><span class="sxs-lookup"><span data-stu-id="f2298-108">There are 10 custom columns in the layout for extensions scenarios.</span></span> <span data-ttu-id="f2298-109">10 のすべてを 1 つのレイアウトで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f2298-109">You can use all 10 in one layout.</span></span> <span data-ttu-id="f2298-110">カスタム列は既にデザイナーのメタデータに追加されています。</span><span class="sxs-lookup"><span data-stu-id="f2298-110">The custom columns are already added to the designer metadata.</span></span> <span data-ttu-id="f2298-111">レイアウトに列を追加した後、トランザクション ページで列が表示できるように配送ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="f2298-111">After adding the column to the layout, you run the distribution job so that the column shows up on the transaction page.</span></span>

> [!NOTE]
> <span data-ttu-id="f2298-112">このトピックでは Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリ更新プログラム 4 修正プログラムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="f2298-112">This topic applies to Dynamics 365 for Finance and Operations, and to Microsoft Dynamics 365 Retail with platform update 8 and Retail App update 4 hotfix.</span></span>

## <a name="add-a-custom-column-to-the-page"></a><span data-ttu-id="f2298-113">ページへのカスタム列の追加</span><span class="sxs-lookup"><span data-stu-id="f2298-113">Add a custom column to the page</span></span>
1. <span data-ttu-id="f2298-114">Dynamics 365 Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="f2298-114">Sign in to Dynamics 365 Retail.</span></span>
2. <span data-ttu-id="f2298-115">**Retail** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト**と移動します。</span><span class="sxs-lookup"><span data-stu-id="f2298-115">Navigate to **Retail** > **Channel setup** > **POS setup** > **POS** > **Screen layouts**.</span></span> <span data-ttu-id="f2298-116">または、検索ばーで **画面レイアウト** を検索します。</span><span class="sxs-lookup"><span data-stu-id="f2298-116">Or, search for **Screen layout** in the search bar.</span></span>
3. <span data-ttu-id="f2298-117">**F3MGR** 画面レイアウト ID を選択した後、アクション バーで **デザイナー** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2298-117">Select the **F3MGR** screen layout ID and click the **Designer** button in the action bar.</span></span>
4. <span data-ttu-id="f2298-118">デザイナーを起動する Azure Active Directory (AAD) の資格情報をインストールおよび入力するよう求められる場合、指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="f2298-118">Follow the instructions if prompted to install and enter the Azure Active Directory (AAD) credentials to launch the designer.</span></span>
5. <span data-ttu-id="f2298-119">レイアウト サイズから **1440 x 960: フル レイアウト** を選択し、**レイアウト デザイナー** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2298-119">Select **1440x960 – Full layout** from the layout sizes and click the **Layout designer** button.</span></span>
6. <span data-ttu-id="f2298-120">プロンプトが表示されたら、**開く**をクリックし、指示に従ってデザイナー ツールをインストールする手順に従いします。</span><span class="sxs-lookup"><span data-stu-id="f2298-120">If prompted, click **Open** and follow the instruction to install the designer tool.</span></span>
7. <span data-ttu-id="f2298-121">インストール後、AAD 資格情報を入力してデザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="f2298-121">After installing, enter your AAD credentials to launch the designer.</span></span>
8. <span data-ttu-id="f2298-122">デザイナーで、トランザクション グリッド (受領書グリッド) を右クリックし、**カスタマイズ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2298-122">In the designer, right-click the transaction grid (receipt grid) and select **Customize**.</span></span>
9. <span data-ttu-id="f2298-123">**カスタマイズ – 入庫**ウィンドウで、ピボット パネルのドロップダウン メニューの**明細行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f2298-123">In the **Customization – Receipt** window, select the **lines** in the pivot panel drop-down menu.</span></span>
   > [!NOTE]
   > <span data-ttu-id="f2298-124">同様に、**支払および配送**タブにカスタム列を追加できます。</span><span class="sxs-lookup"><span data-stu-id="f2298-124">Similarly, you can add a custom column to the **Payment and Delivery** tab.</span></span>
10. <span data-ttu-id="f2298-125">**使用可能な列**ウィンドウで、**カスタム列 1** を選択してから、**> (矢印)** ボタンをクリックして**選択済**列に列を移動します。</span><span class="sxs-lookup"><span data-stu-id="f2298-125">In the **Available columns** window, select **Custom column 1**, and then click the **> (arrow)** button to move the column to the **Selected** columns.</span></span>
11. <span data-ttu-id="f2298-126">**OK** をクリックして保存し、ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f2298-126">Click **OK** to save and close the window.</span></span>
12. <span data-ttu-id="f2298-127">**画面レイアウト** デザイナーを使用してトランザクション グリッドの列幅を調整します。</span><span class="sxs-lookup"><span data-stu-id="f2298-127">Adjust the column width in the transaction grid using the **Screen layout** designer.</span></span> <span data-ttu-id="f2298-128">列が表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f2298-128">Make sure the column is visible.</span></span>
13. <span data-ttu-id="f2298-129">デザイナーを閉じるには、デザイナーの **X** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2298-129">Click the **X** button in the designer to close the designer.</span></span>
14. <span data-ttu-id="f2298-130">**変更の保存** を求められるときは、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2298-130">When prompted to **Save changes**, click **Yes**.</span></span> <span data-ttu-id="f2298-131">**いいえ**をクリックすると、変更は保存されません。</span><span class="sxs-lookup"><span data-stu-id="f2298-131">If you click **No** the changes will not be saved.</span></span>
15. <span data-ttu-id="f2298-132">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f2298-132">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
16. <span data-ttu-id="f2298-133">**1090 レジスター** ジョブを選択し、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2298-133">Select the **Registers (1090)** job and click **Run now**.</span></span>

## <a name="add-business-logic-to-a-custom-column"></a><span data-ttu-id="f2298-134">カスタム列へのビジネス ロジックの追加</span><span class="sxs-lookup"><span data-stu-id="f2298-134">Add business logic to a custom column</span></span>

1. <span data-ttu-id="f2298-135">管理者モードで Visual Studio 2015 を開きます。</span><span class="sxs-lookup"><span data-stu-id="f2298-135">Open Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="f2298-136">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="f2298-136">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="f2298-137">**POS.Extensions** プロジェクトで、**CustomColumnExtensions** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2298-137">Under the **POS.Extensions** project create a new folder named **CustomColumnExtensions**.</span></span>
4. <span data-ttu-id="f2298-138">**CustomColumnExtensions** の下で **Cart** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2298-138">Under **CustomColumnExtensions**, create a new folder named **Cart**.</span></span>
5. <span data-ttu-id="f2298-139">**Cart** の下で **LinesGrid** という名前の新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2298-139">Under **Cart**, create a new folder named **LinesGrid**.</span></span>
6. <span data-ttu-id="f2298-140">**LinesGrid** フォルダーに、新しい Typescript ファイルを追加し、**CustomColumn1Configuration.ts** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f2298-140">In the **LinesGrid** folder, add a new Typescript file and name it **CustomColumn1Configuration.ts**.</span></span>
7. <span data-ttu-id="f2298-141">次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="f2298-141">Add the following **import** statements to import the relevant entities and context.</span></span>

    ```Typescript
    import {

        ICustomLinesGridColumnContext,
        CustomLinesGridColumnBase

    } from "PosApi/Extend/Views/CartView";

    import { CustomGridColumnAlignment } from "PosApi/Extend/Views/CustomGridColumns";
    import { ProxyEntities } from "PosApi/Entities";
    ```
8. <span data-ttu-id="f2298-142">**LinesCustomGridColumn1** という名前の新しいクラスを作成し、**CustomLinesGridColumnBase** から拡張します。</span><span class="sxs-lookup"><span data-stu-id="f2298-142">Create a new class named **LinesCustomGridColumn1** and extend it from **CustomLinesGridColumnBase**.</span></span>

    ```Typescript
    export default class LinesCustomGridColumn1 extends CustomLinesGridColumnBase {}
    ```
9. <span data-ttu-id="f2298-143">クラス内で、選択した支払/入金明細行をキャプチャするプライベート変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="f2298-143">Inside the class declare a private variable to capture the selected tender lines.</span></span>

    ```Typescript
    private _selectedTenderLines: ProxyEntities.TenderLine[ ];
    ```
10. <span data-ttu-id="f2298-144">クラスのコンストラクター メソッドを作成して、コンテキストを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f2298-144">Create a class constructor method to initialize the context.</span></span>

    ```Typescript
    constructor(context: ICustomLinesGridColumnContext) {
        super(context);
    }
    ```
11. <span data-ttu-id="f2298-145">次の列のタイトルと配置のメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="f2298-145">Add the following methods for the columns title and alignment.</span></span>

    ```Typescript
    public title(): string {
        return "Line number";
    } 

    public alignment(): CustomGridColumnAlignment {
        return CustomGridColumnAlignment.Right;
    }
    ```
12. <span data-ttu-id="f2298-146">行番号を返す列計算値メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="f2298-146">Add the column compute value method, which returns the line number.</span></span>
    ```Typescript
    public computeValue(cartLine: ProxyEntities.CartLine): string {
        return cartLine.LineNumber.toString();
    }
    ```
    <span data-ttu-id="f2298-147">クラス全体のコードは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f2298-147">The code for the entire class is:</span></span>
    ```Typescript
    import {
        ICustomLinesGridColumnContext,
        CustomLinesGridColumnBase
    } from "PosApi/Extend/Views/CartView";
    import { CustomGridColumnAlignment } from "PosApi/Extend/Views/CustomGridColumns";
    import { ProxyEntities } from "PosApi/Entities";

    export default class LinesCustomGridColumn1 extends CustomLinesGridColumnBase {
        constructor(context: ICustomLinesGridColumnContext) {
            super(context);
        }

        public title(): string {
            return "Line number";
        }

        public computeValue(cartLine: ProxyEntities.CartLine): string {
            return cartLine.LineNumber.toString();
        }

        public alignment(): CustomGridColumnAlignment {
            return CustomGridColumnAlignment.Right;
        }
    }
    ```
13. <span data-ttu-id="f2298-148">新しい .json ファイルを **CustomColumnExtensions** フォルダーの下に作成し、**manifest.json** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="f2298-148">Create a new .json file under the **CustomColumnExtensions** folder and name it **manifest.json**.</span></span>
14. <span data-ttu-id="f2298-149">**manifest.json** ファイルで、生成されたコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="f2298-149">In the **manifest.json** file, replace the generated code with the following code.</span></span>

    ```Typescript
    {
        "$schema": "../manifestSchema.json",
            "name": "Pos_Extensibility_Samples",
                "publisher": "Microsoft",
                    "version": "7.2.0",
                        "minimumPosVersion": "7.2.0.0",
                            "components": {
            "extend": {
                "views": {
                    "CartView": {
                        "linesGrid": {
                            "customColumn1": { "modulePath": "Cart/LinesGrid/CustomColumn1Configuration" }
                        }
                    }
                }
            }
        }
    }
    
    > [!NOTE]
    > If you are adding a custom column to payment or delivery grid, you need to update the manifest with the following code.
    "paymentsGrid": {
        "customColumn1": { "modulePath": "Cart/PaymentsGrid/CustomColumn1Configuration" }
     },
     "deliveryGrid": {
         "customColumn1": { "modulePath": "Cart/DeliveryGrid/CustomColumn1Configuration" }
     }

    
    ```
    
    
15. <span data-ttu-id="f2298-150">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**CustomColumnExtensions** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="f2298-150">Open the **extensions.json** file under the **POS.Extensions** project and update it with the **CustomColumnExtensions** sample, so that POS during runtime will include this extension.</span></span>

    ```Typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions2"
            },
            {
                "baseUrl": "CustomColumnExtensions"
            }
        ]
    }
    ```
16. <span data-ttu-id="f2298-151">**tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="f2298-151">Open the **tsconfig.json** file and comment out the extension package folders from the exclude list.</span></span> <span data-ttu-id="f2298-152">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="f2298-152">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="f2298-153">既定では、リストにすべての除外された拡張子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f2298-153">By default, the list contains all the excluded extensions.</span></span> <span data-ttu-id="f2298-154">POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子リストから拡張子をコメントする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2298-154">If you want to include any extension part of the POS, then you need add the extension folder name and comment the extension from the extension list as shown.</span></span>

    ```Typescript
    "exclude": [
        "AuditEventExtensionSample",
        "B2BSample",
        "CustomerSearchWithAttributesSample",
        "FiscalRegisterSample",
        "PaymentSample",
        "PromotionsSample",
        "SalesTransactionSignatureSample",
        //"SampleExtensions2",
        "SampleExtensions",
        "StoreHoursSample",
        "SuspendTransactionReceiptSample"
        //"CustomColumnExtensions"
    ],
    ```
17. <span data-ttu-id="f2298-155">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="f2298-155">Compile and rebuild the project.</span></span>

> [!NOTE]
>  <span data-ttu-id="f2298-156">カスタム列のサンプルは [Retail SDK](./retail-sdk/retail-sdk-overview.md) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f2298-156">You can find the sample for the custom column in the [Retail SDK](./retail-sdk/retail-sdk-overview.md).</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="f2298-157">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="f2298-157">Validate the customization</span></span>

1. <span data-ttu-id="f2298-158">オペレーター ID に **000160**、パスワードに **123** を使用して MPOS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="f2298-158">Sign in to MPOS using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="f2298-159">**ようこそ**画面の **現在のトランザクション** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2298-159">Click the **Current transaction** button on the **Welcome** screen.</span></span>
3. <span data-ttu-id="f2298-160">トランザクションに品目 **(0005)** を追加します。</span><span class="sxs-lookup"><span data-stu-id="f2298-160">Add item **(0005)** to the transaction.</span></span>
4. <span data-ttu-id="f2298-161">カスタム列に行番号が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f2298-161">The custom column should display the line number.</span></span>



