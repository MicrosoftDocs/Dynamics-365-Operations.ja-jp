---
title: 販売時点管理 (POS) Totals パネルへカスタム フィールドを追加
description: この記事では、画面レイアウト デザイナーを使用して、POS トランザクション画面の合計パネルに新しいカスタム フィールドを追加する方法について説明します。
author: josaw1
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 73e2f784d49ecd4cfd64b7e83f831d15644c4f52
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269212"
---
# <a name="add-custom-fields-to-the-point-of-sale-pos-totals-panel"></a>販売時点管理 (POS) Totals パネルへカスタム フィールドを追加

[!include[banner](../includes/banner.md)]

この記事では、画面レイアウト デザイナーを使用して、POS トランザクション画面の **合計** パネルに新しいカスタム フィールドを追加する方法について説明します。 この記事は、Microsoft Dynamics 365 Finance 7.3 およびそれ以降と、Microsoft Dynamics 365 Retail 7.3 およびそれ以降に適用されます。

**カスタム フィールド** ページの **合計** パネルに追加するカスタム フィールドが、デザイナーに表示されます。 次に、左右の列にあるカスタム フィールドを選択することができます。 カスタム フィールドのロジックは、販売時点管理 (POS) 拡張機能でコーディングされる必要があります。

## <a name="scenariobusiness-problem"></a>シナリオ/ビジネスの問題

<span id="_Toc446093285" class="anchor"></span>画面レイアウト デザイナーを使用して、POS トランザクション画面の **合計** パネルにカスタム フィールドを追加します。 また、POS 拡張のカスタム項目のビジネス ロジックをコード化します。

## <a name="overview-of-the-required-steps"></a>必要な手順の概要

まず、バックオフィスをコンフィギュレーションするには、これらの手順を完了する必要があります。

1. **言語テキスト** ページで、カスタム フィールドの言語テキストを追加します。
2. **カスタム フィールド** ページで、新しいカスタム フィールドを追加します。
3. 画面レイアウト デザイナーで、**合計** パネルに新しいカスタム フィールドを追加します。
4. **レジスター** (**1090**) ジョブを実行します。

POS の拡張機能プロジェクトでは、この手順を行う必要があります。

- ビジネス ロジックをカスタム フィールドへ追加します。

## <a name="configure-headquarters"></a>バックオフィスのコンフィギュレーション

1. コマースにサインインします。
2. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト** の順に移動します。
3. **POS** タブで、**追加** を選択して新しい POS 言語テキストを追加します。

    **合計** パネルに表示されるテキストはローカライズすることができます。 したがって、同じテキスト ID の異なる言語で複数のテキストを作成することができます。 次に例を示します。

    | 言語 ID | テキスト ID | テキスト   |
    |-------------|---------|--------|
    | ja       | 1       | サンプル |
    | en-UK       | 1       | デモ   |

4. アクション ウィンドウで、**保存** を選択して変更を保存します。
5. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> カスタム フィールド** の順に移動します。
6. アクション ウィンドウで、**新規** を選択して新しいカスタム フィールドを追加し、次の情報を指定します。 

    1. **名前** フィールドに、カスタム フィールドの名前を入力します。
    2. **タイプ** フィールドで、**合計エリア** を選択します。
    3. **キャプション テキスト ID** フィールドで、手順 3 で使用したテキスト ID を指定します。

    次に例を示します。

    | 氏名   | 種類        | キャプション テキスト ID |
    |--------|-------------|-----------------|
    | サンプル | 合計エリア | 1               |


7. アクション ウィンドウで、**保存** を選択して変更を保存します。
8. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS \> 画面レイアウト** の順に移動します。
9. **F3MGR** 画面レイアウト ID を選択した後、アクション ウィンドウで **デザイナー** を選択します。

    > [!NOTE]
    > 既存のレイアウトを選択するか、新しいレイアウトを作成することができます。 **F3MGR** 画面レイアウト ID は、デモ データを使用している場合にのみ使用できます。

10. **1440x960 – フル** レイアウト サイズを選択し、**レイアウト デザイナー** を選択します。
11. アプリケーションを開いて確認するよう求めるメッセージが表示されたら、**開く** を選択して、インストールの指示に従ってください。
12. デザイナーをインストールすると、Azure Active Directory (Azure AD) の資格情報を要求されます。 デザイナーを開始するための情報を入力します。
13. デザイナーで、左ウィンドウから画面レイアウトへ **合計パネル** コントロールをドラッグします。 レイアウトに既に **合計** パネルが含まれている場合、コントロールは左ウィンドウに淡色表示されます。
14. 画面レイアウトで、**合計パネル** を右クリックし、**カスタマイズ** を選択します。
15. **カスタマイズ - 合計パネル** ダイアログ ボックスで、**SAMPLE** カスタム フィールドが **利用可能なフィールド** リストに表示されます。 矢印ボタンを使用して左列または右列のいずれかに移動します。
16. カスタム フィールドを上下に移動するには、**アップ** および **ダウン** ボタンを使用します。
17. **OK** を選択して変更を保存し、**カスタマイズ - 合計パネル** ダイアログ ボックスを終了します。
18. 右上隅の **閉じる** ボタン (**X**) を選択して、デザイナーを閉じます。
19. 変更の保存を求められたら、**はい** を選択します。 **いいえ** を選択した場合、変更は保存されません。
20. **Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。
21. **レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。

## <a name="add-business-logic-to-the-custom-field"></a>ビジネス ロジックをカスタム フィールドへ追加

同様のサンプルコードは、\\RetailSDK\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\Cart\\TipsCustomField.ts の Retail ソフトウェア開発キット (SDK) で見つけることができます。

1. Microsoft Visual Studio 2015 を管理者モードで起動します。
2. **ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。
3. **POS.Extensions** プロジェクトで、**CustomFieldExtensions** というフォルダーを作成します。
4. **CustomFieldExtensions** フォルダーで、**Cart** というフォルダーを作成します。
5. **カート** フォルダーで、**SampleCustomField.ts** という .ts (typescript) ファイルを作成します。
6. **SampleCustomField.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { CartViewTotalsPanelCustomFieldBase } from "PosApi/Extend/Views/CartView";
    import { ProxyEntities } from "PosApi/Entities";
    ```

7. **SampleCustomField** という名前のクラスを作成し、**CartViewTotalsPanelCustomFieldBase** クラスから拡張します。 この方法で、基本クラスからの **computeValue** メソッドでは、カスタム フィールドの任意のカスタム ロジックが実行されます。

    ```typescript
    export default class SampleCustomField extends CartViewTotalsPanelCustomFieldBase {

    }
    ```

8. **SampleCustomField** クラス内で、カスタム フィールドのロジックを設定するため **computeValue** 抽象メソッドを実装します。

    ```typescript
    public computeValue(cart: ProxyEntities.Cart): string {

        // Let's show 10% of total amount in the custom field.

        if (isNaN(cart.TotalAmount) || cart.TotalAmount <= 0) {
            return "$0.00";
        }
        return "$" + (cart.TotalAmount * 0.1).toFixed(2).toString();
    }
    ```

    全体的なクラスは、次のようになります。

    ```typescript
    import { CartViewTotalsPanelCustomFieldBase } from "PosApi/Extend/Views/CartView";
    import { ProxyEntities } from "PosApi/Entities";

    export default class SampleCustomField extends CartViewTotalsPanelCustomFieldBase {
        public computeValue(cart: ProxyEntities.Cart): string {

            // Let's show 10% of total amount in the custom field.
            if (isNaN(cart.TotalAmount) || cart.TotalAmount <= 0) {
                return "$0.00";
            }
            return "$" + (cart.TotalAmount * 0.1).toFixed(2).toString();
        }
    }
    ```

9. **CustomFieldExtensions** フォルダーで、**manifest.json** という .json ファイルを作成します。
10. **manifest.json** ファイルに、以下のコードを貼り付けます。

    ```typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Contoso",
        "version": "7.3.0",
        "minimumPosVersion": "7.3.0.0",
        "components": {
            "extend": {
                "views": {
                    "CartView": {
                        "totalsPanel": {
                            "customFields": [
                                {
                                    "fieldName": "Sample",
                                    "modulePath": "Cart/SampleCustomField"
                                }
                            ]
                    } }
            }  }
    } }
    ```

    マニフェストでは、**customFields** セクションの **fieldName** 値が、バックオフィスで追加されたカスタム フィールドの名前、および "バックオフィスのコンフィギュレーション" 手順のステップ 6 のカスタム フィールドで指定した名前と一致している必要があることに注意してください。 **modulePath** は、実装ファイルの名前です。その実装ファイル名は、"ビジネス ロジックをカスタム フィールドへ追加" 手順のステップ 5 で作成したファイルの名前です。
    
    複数のカスタム フィールドを追加する場合は、複数の実装ファイルを追加し、custonFileds セクションの情報を更新する必要があります。

    たとえば、2 つのカスタム フィールド、**サンプル 1** と **サンプル 2** を追加する場合、同じ基本クラスの **CartViewTotalsPanelCustomFieldBase** から拡張された 2 つの実装ファイルが必要になります。

    この場合、マニフェストは次のようになります。

    ```typescript
    "customFields": [
        {
            "fieldName": "Sample1",
            "modulePath": "Cart/SampleCustomField1"
        },
        {
            "fieldName": "Sample2",
            "modulePath": "Cart/SampleCustomField2"
        }
    ]
    ```
    
    この例では、**SampleCustomField1** と **SampleCustomField2** は、ビジネス ロジックを実行する typescript ファイルの名前になります。

11. **extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**CustomFieldExtensions** サンプルで更新し、実行時に POS にこの拡張機能を読み込むようにします。

    ```typescript
    {
        "extensionPackages": [
            { 
                "baseUrl": "SampleExtensions2" 
            }, 
            {
                "baseUrl": "CustomFieldExtensions"
            }
        ]
    }
    ```

12. **tsconfig.json** ファイルを開き、拡張子フォルダ名 **CustomFieldExtensions** を追加し **除外** リストで拡張子フォルダをコメントアウトします。 POS では、このファイルを使用して、拡張機能を追加または除外します。 既定では、**除外** リストには除外されたすべての拡張リストが含まれています。 拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、**拡張** リストの拡張をコメントアウトします。

    ```typescript
    "exclude": [
        "SampleExtensions",
        //"SampleExtensions2",
        //"CustomFieldExtensions"
    ],
    ```

13. プロジェクトをコンパイル、およびリビルドします。
14. **ローカル コンピューター** ボタンをクリックすることで、Retail Modern POS (MPOS) のカスタマイズされたバージョンを配置します。 ソリューション プラットフォームが x86 であることを確認します。 または、配置可能パッケージの作成およびパッケージから MPOS のインストールが可能です。

    > [!NOTE]
    > この記事で MPOS を使用しても、MPOS またはクラウド POS のいずれかを使用できます。

## <a name="validate-the-customization"></a>カスタマイズの検証

1. オペレーター ID に **000160**、パスワードに **123** を使用して MPOS にサインインします。
2. ようこそ画面で、**現在のトランザクション** ボタンを選択します。
3. 品目をトランザクションに追加します。

カスタム フィールドが **合計** パネルに表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
