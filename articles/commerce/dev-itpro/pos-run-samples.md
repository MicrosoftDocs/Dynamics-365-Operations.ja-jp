---
title: 販売時点管理 (POS) サンプルを実行
description: このトピックでは、POS サンプルを実行する方法について説明します。
author: mugunthanm
ms.date: 11/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-11-27
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: a5dfdf092b1dc0c859f10f69258422bd77d26423
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781132"
---
# <a name="run-the-point-of-sale-pos-samples"></a>販売時点管理 (POS) サンプルを実行

[!include [banner](../../includes/banner.md)]

拡張機能を示す Retail SDK にはいくつかのサンプルがあります。 このトピックでは、これらのサンプルを実行する方法について説明します。

## <a name="run-the-sampleextensions-in-pos"></a>POS で SampleExtensions を実行
1. **Retail SDK\\POS** フォルダーから **ModernPos.Sln** あるいは **CloudPos.sln** を開きます。
2. ソリューションで **POS 拡張機能** プロジェクトを選択し、**ファイルをすべて表示** をクリックします。
3. **SampleExtensions** フォルダーを右クリックし、**プロジェクトに追加** を選択します。
4. **SampleExtensions2** フォルダーを右クリックし、**プロジェクトに追加** を選択します。
5. **extensions.json** ファイルを開いて、**SampleExtensions** および **SampleExtensions2** の拡張フォルダーを追加します。 これは、実行時に POS にこの拡張が含まれることを意味します。 **baseUrl** 値は、相対パスおよび拡張子フォルダーの名前に完全に一致する必要があります。

    ```typescript
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions"
            },
            {
                "baseUrl": "SampleExtensions2"
            }
        ] 
    }
    ```
    > [!Note]  
    > extension.json ファイルには、2 つ以上の拡張機能フォルダーを含める必要があります。 拡張子フォルダーを 1 つだけ追加する場合は、POS は拡張子を読み込みません。
5. **tsconfig.json** ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。 POS は、拡張機能をコンパイルするかどうかを決定するために、このファイルを使用します。 既定では、リストにサンプル拡張リストが含まれています。 POS に拡張子をコンパイルする場合は、拡張子フォルダー名を追加し、以下のように拡張子から拡張子をコメント アウトする必要があります。 

    ```typescript
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
    他の拡張子を有効にする場合は、除外リストからそれらをコメント アウトします。 たとえば、**B2BSample** を含める場合、コードは次のようになります。 
    
    ```typescript
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
    > その他の拡張機能パッケージ フォルダーは、Visual Studio プロジェクトに含まれていない場合でも、追加する予定でない場合は除外リストに含める必要があります。
6. 検証のために Modern POS を使用している場合、**ソリューション プラットフォーム** を **x86** に、**オプションの配置** を **ローカル コンピューター** または **シミュレーター** に設定します。
7. **すべて保存** をクリックし、**F5** キーを押して拡張機能を検証します。

    > [!Note] 
    > クラウド POS では、Visual Studio でクリーン ソリューションを使用して、ソリューションを再構築します。
8. 製品の検索画面に移動、または上部の検索バーを使用して製品を検索します。 グリッドおよび新しいアプリケーション バーのボタンのカスタム列が表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]