---
title: "MPOS 画面レイアウトへのカスタム コントロールの追加"
description: "このトピックでは、最新POS (MPOS) の画面レイアウトに新しいカスタム コントロールを追加する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 65801
ms.assetid: 99079d81-fde2-4432-8cee-82bbcc3bd57e
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3622485c59f62c06024aa533d3eac3a00d370f09
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="add-a-custom-control-to-an-mpos-screen-layout"></a><span data-ttu-id="5bc19-103">MPOS 画面レイアウトへのカスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="5bc19-103">Add a custom control to an MPOS screen layout</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bc19-104">このトピックでは、最新POS (MPOS) の画面レイアウトに新しいカスタム コントロールを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-104">This topic explains how to add a new custom control to a Modern POS (MPOS) screen layout.</span></span>

<a name="scenario"></a><span data-ttu-id="5bc19-105">シナリオ</span><span class="sxs-lookup"><span data-stu-id="5bc19-105">Scenario</span></span>
--------

<span data-ttu-id="5bc19-106">販売に関する詳細な情報をレジ担当者およびマネージャに提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bc19-106">You want to provide the cashier and manager more information about sales.</span></span> <span data-ttu-id="5bc19-107">たとえば、トランザクションで購入された合計数および無効明細行の数などの、トランザクション ぺージに情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-107">For example, you want to add information to the transaction page, such as the total quantity that was purchased and the number of voided lines in the transaction.</span></span> <span data-ttu-id="5bc19-108">カスタム コントロールを使用してこの情報を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-108">You can use a custom control to add this information.</span></span>

## <a name="add-the-custom-control"></a><span data-ttu-id="5bc19-109">カスタム コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="5bc19-109">Add the custom control</span></span>
1.  <span data-ttu-id="5bc19-110">管理者として Microsoft Visual Studio を起動します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-110">Start Microsoft Visual Studio as an administrator.</span></span>
2.  <span data-ttu-id="5bc19-111">Modern POS(MPOS) ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-111">Open the Modern POS (MPOS) solution.</span></span> <span data-ttu-id="5bc19-112">ソリューションのフォルダーの場所は、ソリューション トポロジによって異なります。</span><span class="sxs-lookup"><span data-stu-id="5bc19-112">The location of the folder for the solution depends on your solution topology.</span></span>
3.  <span data-ttu-id="5bc19-113">POS.App プロジェクトの Views\\Controls フォルダーで、新しい HTML ページを追加し、**CustomControl.html** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-113">In the POS.App project, in the Views\\Controls folder, add a new HTML page, and name it **CustomControl.html**.</span></span>
4.  <span data-ttu-id="5bc19-114">POS.App プロジェクトの Views\\Controls フォルダーで、新しい TypeScript ファイルを追加し、**CustomControl.ts** と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-114">In the POS.App project, in the Views\\Controls folder, add new TypeScript file, and name it **CustomControl.ts**.</span></span>
5.  <span data-ttu-id="5bc19-115">CustomControl.html ファイルを開いて、既存のコードを次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-115">Open the CustomControl.html file, and replace the existing code with the following code.</span></span> <span data-ttu-id="5bc19-116">このコードは 2 つの新しいプロパティを追加し、**CustomControlOptions** クラスにバインドします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-116">This code adds two new properties and binds them to the **CustomControlOptions** class.</span></span>

        <!DOCTYPE html>
            <html>
                <head>
                    <meta charset="utf-8" />
                    <title>CustomControl</title>
                </head>
                <body>
                    <div data-bind="customControlInternal: 'CustomControlOptions'">
                        <div class="panel marginBottom1 marginTop05 primaryPanelBackgroundColor highContrastBorderThin height01">
                            <div class="row padTop1 padBottom0">
                                <div class="secondaryFontColor"><h4>Total quantities:</h4></div>
                                <div class="textRight"><h4 data-bind="text: _quantities" class="wrapText"></h4></div>
                            </div>
                            <div class="row padTop1 padBottom0">
                                <div class="secondaryFontColor"><h4>Voided lines:</h4></div>
                                <div class="textRight"><h4 data-bind="text: _voidedLines" class="wrapText"></h4></div>
                            </div>
                        </div>
                    </div>
                </body>
            </html>

6.  <span data-ttu-id="5bc19-117">CustomControl.ts ファイルを開いて、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-117">Open the CustomControl.ts file, and add the following code.</span></span> <span data-ttu-id="5bc19-118">2 つのメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="5bc19-118">There are two methods.</span></span> <span data-ttu-id="5bc19-119">1 つの方法は合計数量を取得し、もう 1 つは無効にされた数量を取得します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-119">One method retrieves the total quantities, and the other retrieves the voided quantities.</span></span> <span data-ttu-id="5bc19-120">値は、HTML ページのユーザー インターフェイスにバインドされているプライベート変数に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-120">The values are assigned to private variables that are bound to the user interface on the HTML page.</span></span>

        ///<reference path='K:\RainMainStab\7.0.1265.3014\retail\Services\RetailSDK\Code\POS\SharedApp\Views\Controls\UserControl.ts'/>
        module Commerce.Controls {
            "use strict";
            /**
            * Options passed to the custom control.
            * To pass more variables, change here and at the caller CartView.html (options: { data: ... })
            */
            export interface ICustomControlOptions {
                data: Proxy.Entities.Cart;
            }
            /*** User control for rendering custom control. */
            export class CustomControl extends UserControl {
                // Observable that is binded to the control's UI
                // See ExtraControl.html (data-bind="text: _quantities")
                private _quantities: Observable<number>;
                private _voidedLines: Observable<number>;
                /*** Initializes a new instance of the ExtraControlOptions class.  This is called every time the cart is changed.  */
                constructor(options: ICustomControlOptions) {
                super();
                options = options || { data: undefined };
                // Calculate the total quantities at lines and set to the observable.
                this._quantities = ko.observable(this.getTotalQuantity(options.data));
                this._voidedLines = ko.observable(this.getVoidedQuantity(options.data));
            }
            private getTotalQuantity(cart: Proxy.Entities.Cart): number {
                var totalQuantity: number = 0;
                if (ObjectExtensions.isNullOrUndefined(cart) || !ArrayExtensions.hasElements(cart.CartLines)) {
                    return totalQuantity;
                }
                cart.CartLines.forEach((cartLine: Proxy.Entities.CartLine) => {
                    if (!cartLine.IsVoided) {
                        totalQuantity = totalQuantity + cartLine.Quantity;
                } });
                return totalQuantity;
            }
            private getVoidedQuantity(cart: Proxy.Entities.Cart): number {
                var voidedQuantity: number = 0;
                if (ObjectExtensions.isNullOrUndefined(cart) || !ArrayExtensions.hasElements(cart.CartLines)) {
                    return voidedQuantity;
                }
                cart.CartLines.forEach((cartLine: Proxy.Entities.CartLine) => {
                    if (cartLine.IsVoided) {
                        voidedQuantity = voidedQuantity + 1;
                }});
                return voidedQuantity;
            }  }
        }

7.  <span data-ttu-id="5bc19-121">プロジェクトをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-121">Compile the project.</span></span>
8.  <span data-ttu-id="5bc19-122">MPOS を配置する前に、画面レイアウト デザイナーに新しいカスタム コントロールを追加し相対 URL を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5bc19-122">Before you deploy MPOS, you must add the new custom control in the screen layout designer and set the relative URL.</span></span> <span data-ttu-id="5bc19-123">クライアントにサインインし、**小売り** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **POS** &gt; **画面レイアウト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-123">Sign in to the client, and go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
9.  <span data-ttu-id="5bc19-124">**F2MP16:9M** 画面レイアウトを選択した後、アクション ウィンドウで **デザイナー** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-124">Select the **F2MP16:9M** screen layout, and then, on the Action Pane, click the **Designer** button.</span></span>
10. <span data-ttu-id="5bc19-125">デザイナー ツールをインストールするように求められたら、**開く** をクリックし、インストール手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5bc19-125">If you're prompted to install the designer tool, click **Open**, and follow the installation instructions.</span></span>
11. <span data-ttu-id="5bc19-126">インストールが完了すると、Microsoft Azure Active Directory (Azure AD) の資格情報が要求されます。</span><span class="sxs-lookup"><span data-stu-id="5bc19-126">After the installation is completed, you're prompted for your Microsoft Azure Active Directory (Azure AD) credentials.</span></span> <span data-ttu-id="5bc19-127">デザイナーを開始するために提供します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-127">Provide them to start the designer.</span></span>
12. <span data-ttu-id="5bc19-128">デザイナーで、トランザクション ページにカスタム コントロールをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-128">In the designer, drag the custom control to the transaction page.</span></span>
13. <span data-ttu-id="5bc19-129">トランザクション ページでカスタム コントロールを右クリックし、**カスタマイズ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-129">Right-click the custom control on the transaction page, and then click **Customize**.</span></span>
14. <span data-ttu-id="5bc19-130">相対 URIを **Views/Controls/CustomControl.html** に設定し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-130">Set the relative URI to **Views/Controls/CustomControl.html**, and then click **OK**.</span></span>
15. <span data-ttu-id="5bc19-131">デザイナーで、**閉じる**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-131">In the designer, click the **Close** button.</span></span>
16. <span data-ttu-id="5bc19-132">変更の保存を求められたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-132">When you're prompted to save your changes, click **Yes**.</span></span>
17. <span data-ttu-id="5bc19-133">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-133">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
18. <span data-ttu-id="5bc19-134">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-134">Select the **Registers** (**1090**) job, and then click **Run now**.</span></span>
19. <span data-ttu-id="5bc19-135">ジョブの実行が終了した後は、Visual Studio から**配置**ボタンをクリックして MPOS を配置します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-135">After the job has finished running, deploy MPOS from Visual Studio by clicking the **Deploy** button.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="5bc19-136">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="5bc19-136">Validate the customization</span></span>
1.  <span data-ttu-id="5bc19-137">オペレーター ID に **000160**、パスワードに **123** を使用して MPOS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-137">Sign in to MPOS by using **000160** as the operator ID and **123** as the password.</span></span>
2.  <span data-ttu-id="5bc19-138">ようこそ画面で、**現在のトランザクション**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5bc19-138">On the welcome screen, click the **Current transaction** button.</span></span>
3.  <span data-ttu-id="5bc19-139">トランザクションに任意の品目を追加し、合計数量がカスタム コントロールに正しく表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-139">Add any item to the transaction, and verify that the total quantity is shown correctly in the custom control.</span></span>
4.  <span data-ttu-id="5bc19-140">トランザクション内で任意の明細行を無効化し、無効にされた行の数がカスタム コントロールに正しく表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5bc19-140">Void any line in the transaction, and verify that the voided line count is shown correctly in the custom control.</span></span>





