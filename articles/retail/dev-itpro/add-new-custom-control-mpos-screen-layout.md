---
title: "Retail Modern POS (MPOS) 画面レイアウトへのカスタム コントロールの追加"
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 57dc1e2c085da5eac5d25030bd34ff0037e29ee1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="add-custom-controls-to-retail-modern-pos-mpos-screen-layouts"></a>Retail Modern POS (MPOS) 画面レイアウトへのカスタム コントロールの追加

[!include [banner](../includes/banner.md)]

このトピックでは、最新POS (MPOS) の画面レイアウトに新しいカスタム コントロールを追加する方法について説明します。

<a name="scenario"></a>シナリオ
--------

販売に関する詳細な情報をレジ担当者およびマネージャに提供する必要があります。 たとえば、トランザクションで購入された合計数および無効明細行の数などの、トランザクション ぺージに情報を追加します。 カスタム コントロールを使用してこの情報を追加することができます。

## <a name="add-the-custom-control"></a>カスタム コントロールの追加
1.  管理者として Microsoft Visual Studio を起動します。
2.  Modern POS(MPOS) ソリューションを開きます。 ソリューションのフォルダーの場所は、ソリューション トポロジによって異なります。
3.  POS.App プロジェクトの Views\\Controls フォルダーで、新しい HTML ページを追加し、**CustomControl.html** と名前を付けます。
4.  POS.App プロジェクトの Views\\Controls フォルダーで、新しい TypeScript ファイルを追加し、**CustomControl.ts** と名前を付けます。
5.  CustomControl.html ファイルを開いて、既存のコードを次のコードに置き換えます。 このコードは 2 つの新しいプロパティを追加し、**CustomControlOptions** クラスにバインドします。

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

6.  CustomControl.ts ファイルを開いて、次のコードを追加します。 2 つのメソッドがあります。 1 つの方法は合計数量を取得し、もう 1 つは無効にされた数量を取得します。 値は、HTML ページのユーザー インターフェイスにバインドされているプライベート変数に割り当てられます。

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

7.  プロジェクトをコンパイルします。
8.  MPOS を配置する前に、画面レイアウト デザイナーに新しいカスタム コントロールを追加し相対 URL を設定する必要があります。 クライアントにサインインし、**小売り** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **POS** &gt; **画面レイアウト** の順に移動します。
9.  **F2MP16:9M** 画面レイアウトを選択した後、アクション ウィンドウで **デザイナー** ボタンをクリックします。
10. デザイナー ツールをインストールするように求められたら、**開く** をクリックし、インストール手順に従います。
11. インストールが完了すると、Microsoft Azure Active Directory (Azure AD) の資格情報が要求されます。 デザイナーを開始するために提供します。
12. デザイナーで、トランザクション ページにカスタム コントロールをドラッグします。
13. トランザクション ページでカスタム コントロールを右クリックし、**カスタマイズ** をクリックします。
14. 相対 URIを **Views/Controls/CustomControl.html** に設定し、**OK** をクリックします。
15. デザイナーで、**閉じる**ボタンをクリックします。
16. 変更の保存を求められたら、**はい** をクリックします。
17. **小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。
18. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行** をクリックします。
19. ジョブの実行が終了した後は、Visual Studio から**配置**ボタンをクリックして MPOS を配置します。

## <a name="validate-the-customization"></a>カスタマイズの検証
1.  オペレーター ID に **000160**、パスワードに **123** を使用して MPOS にサインインします。
2.  ようこそ画面で、**現在のトランザクション**ボタンをクリックします。
3.  トランザクションに任意の品目を追加し、合計数量がカスタム コントロールに正しく表示されることを確認します。
4.  トランザクション内で任意の明細行を無効化し、無効にされた行の数がカスタム コントロールに正しく表示されることを確認します。





