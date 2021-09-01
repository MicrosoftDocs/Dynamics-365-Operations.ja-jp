---
title: 販売時点管理 (POS) トランザクション グリッドへのカスタム列の追加
description: このトピックでは、画面レイアウト デザイナーを使用して POS トランザクション ページに新しいカスタム列を追加する方法について説明します。
author: mugunthanm
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-01-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: 22f04623fabca9e4cbdaba015fc0a35e8127deb16d783b0f942780b4f13edd18
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713980"
---
# <a name="add-custom-columns-to-a-point-of-sale-pos-transaction-grid"></a>販売時点管理 (POS) トランザクション グリッドへのカスタム列の追加

[!include [banner](../../includes/banner.md)]

このトピックでは、画面レイアウト デザイナーを使用して POS トランザクション ページに新しいカスタム列を追加する方法について説明します。 カスタム列フィーチャーを使用して、トランザクション ページにさらに情報を追加することができます。 カスタム列は、画面レイアウト デザイナーを使用して、トランザクションのページ入庫グリッドに追加できます。 デザイナーを使用して、列の幅および配置を調整することができます。 拡張シナリオのレイアウトには、10 個のカスタム列があります。 10 のすべてを 1 つのレイアウトで使用することができます。 カスタム列は既にデザイナーのメタデータに追加されています。 レイアウトに列を追加した後、トランザクション ページで列が表示できるように配送ジョブを実行します。

> [!NOTE]
> このトピックでは Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 Retail プラットフォーム更新 8 と Retail アプリ更新プログラム 4 修正プログラムが適用されます。

## <a name="add-a-custom-column-to-the-page"></a>ページへのカスタム列の追加
1. Dynamics 365 Commerce へサインインします。
2. **Retail とコマース** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト** の順に移動します。 または、検索ばーで **画面レイアウト** を検索します。
3. **F3MGR** 画面レイアウト ID を選択した後、アクション バーで **デザイナー** ボタンをクリックします。
4. デザイナーを起動する Azure Active Directory (AAD) の資格情報をインストールおよび入力するよう求められる場合、指示に従ってください。
5. レイアウト サイズから **1440 x 960: フル レイアウト** を選択し、**レイアウト デザイナー** ボタンをクリックします。
6. プロンプトが表示されたら、**開く** をクリックし、指示に従ってデザイナー ツールをインストールする手順に従いします。
7. インストール後、AAD 資格情報を入力してデザイナーを起動します。
8. デザイナーで、トランザクション グリッド (受領書グリッド) を右クリックし、**カスタマイズ** を選択します。
9. **カスタマイズ – 入庫** ウィンドウで、ピボット パネルのドロップダウン メニューの **明細行** を選択します。

   > [!NOTE]
   > 同様に、**支払および配送** タブにカスタム列を追加できます。
   
10. **使用可能な列** ウィンドウで、**カスタム列 1** を選択してから、**> (矢印)** ボタンをクリックして **選択済** 列に列を移動します。
11. **OK** をクリックして保存し、ウィンドウを閉じます。
12. **画面レイアウト** デザイナーを使用してトランザクション グリッドの列幅を調整します。 列が表示されていることを確認します。
13. デザイナーを閉じるには、デザイナーの **X** ボタンをクリックします。
14. **変更の保存** を求められるときは、**はい** をクリックします。 **いいえ** をクリックすると、変更は保存されません。
15. **Retail とコマース** > **Retail とコマース IT** > **配送スケジュール** の順に移動します。
16. **1090 レジスター** ジョブを選択し、**今すぐ実行** をクリックします。

## <a name="add-business-logic-to-a-custom-column"></a>カスタム列へのビジネス ロジックの追加

1. 管理者モードで Visual Studio 2015 を開きます。
2. **ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。
3. **POS.Extensions** プロジェクトで、**CustomColumnExtensions** という名前の新しいフォルダーを作成します。
4. **CustomColumnExtensions** の下で **Cart** という名前の新しいフォルダーを作成します。
5. **Cart** の下で **LinesGrid** という名前の新しいフォルダーを作成します。
6. **LinesGrid** フォルダーに、新しい Typescript ファイルを追加し、**CustomColumn1Configuration.ts** と名前を付けます。
7. 次の **import** 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import {

        ICustomLinesGridColumnContext,
        CustomLinesGridColumnBase

    } from "PosApi/Extend/Views/CartView";

    import { CustomGridColumnAlignment } from "PosApi/Extend/Views/CustomGridColumns";
    import { ProxyEntities } from "PosApi/Entities";
    ```
8. **LinesCustomGridColumn1** という名前の新しいクラスを作成し、**CustomLinesGridColumnBase** から拡張します。

    ```typescript
    export default class LinesCustomGridColumn1 extends CustomLinesGridColumnBase {}
    ```
9. クラス内で、選択した支払/入金明細行をキャプチャするプライベート変数を宣言します。

    ```typescript
    private _selectedTenderLines: ProxyEntities.TenderLine[ ];
    ```
10. クラスのコンストラクター メソッドを作成して、コンテキストを初期化します。

    ```typescript
    constructor(context: ICustomLinesGridColumnContext) {
        super(context);
    }
    ```
11. 次の列のタイトルと配置のメソッドを追加します。

    ```typescript
    public title(): string {
        return "Line number";
    } 

    public alignment(): CustomGridColumnAlignment {
        return CustomGridColumnAlignment.Right;
    }
    ```
12. 行番号を返す列計算値メソッドを追加します。
    ```typescript
    public computeValue(cartLine: ProxyEntities.CartLine): string {
        return cartLine.LineNumber.toString();
    }
    ```

    クラス全体のコードは次のとおりです。

    ```typescript
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

13. 新しい .json ファイルを **CustomColumnExtensions** フォルダーの下に作成し、**manifest.json** という名前を付けます。
14. **manifest.json** ファイルで、生成されたコードを次のコードに置き換えます。

    ```typescript
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
    
    
15. **extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**CustomColumnExtensions** サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。

    ```typescript
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
16. **tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。 POS では、このファイルを使用して、拡張機能を追加または除外します。 既定では、リストにすべての除外された拡張子が含まれています。 POS の一部である拡張子を含める場合は、拡張子フォルダー名を追加し、以下のように拡張子リストから拡張子をコメントする必要があります。

    ```typescript
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
17. プロジェクトをコンパイル、およびリビルドします。

> [!NOTE]
>  カスタム列のサンプルは [Retail ソフトウェア開発キット (SDK) アーキテクチャ](./retail-sdk/retail-sdk-overview.md) で見つけることができます。

## <a name="validate-the-customization"></a>カスタマイズの検証

1. オペレーター ID に **000160**、パスワードに **123** を使用して MPOS にサインインします。
2. **ようこそ** 画面の **現在のトランザクション** ボタンをクリックします。
3. トランザクションに品目 **(0005)** を追加します。
4. カスタム列に行番号が表示されます。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]