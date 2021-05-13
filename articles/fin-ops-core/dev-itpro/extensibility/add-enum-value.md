---
title: 拡張機能を使用して列挙体に値を追加
description: このトピックでは、列挙型を拡張することによって列挙型に新しい値を追加する方法について説明します。
author: smithanataraj
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 01b05f47f5c8544cc516fdde2d6ed3584608ea3c
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866222"
---
# <a name="add-values-to-enums-through-extension"></a>拡張機能を使用して列挙体に値を追加

[!include [banner](../includes/banner.md)]

新しい値を列挙型に追加するには、列挙型を拡張する必要があります。 **拡張可能** (**IsExtensible = true**) としてマークされている列挙は拡張できます。 拡張機能の情報は、次の図に示すように、Microsoft Visual Studio の **プロパティ** ウィンドウで見つけることができます。

![拡張可能な列挙](media/AddEnum01.png)

拡張可能な列挙の列挙値が同期されると、拡張可能な列挙の値が non-deterministic であるのに対して、ベースライン列挙の整数値は deterministic です。 値は、同期時に生成されます。 したがって、列挙値の整数値に依存する X++ ロジックを持つことはできません。 次にいくつか例を挙げます。

+ `<`、`>`、`..` などの範囲比較
+ ビューおよびクエリのモデル化された範囲
+ コードから作成されたクエリの範囲 

通常、拡張された列挙型は、それが使用される場所で独自の実装を必要とします。 列挙のすべての使用を確認して、必要な場合に実装を取得します。 検索するいくつかの重要な場所を次に示します。

+ ブロックの切り替え:

    - Switch ブロックに、既定の case ブロックまたは例外が発生しない既定のケース ブロックがない場合、デリゲートが指定されている場合、デリゲートを購読することにより拡張の列挙値を処理します。 それ以外の場合、メソッドにポストイベント ハンドラーを追加します。 
    - 列挙型に例外をスローする既定のケース ブロックを持つスイッチが使用されている場合、Microsoft に問い合わせ、デリゲートを要求します。

+ 列挙型に、列挙型を処理する関連付けられたクラス階層がある場合は、列挙型固有の実装に対してサブクラスを作成し、必要に応じて基本クラスにコンストラクターを取り込みます。 詳細については、[ファクトリ メソッドのサブクラスを登録](register-subclass-factory-methods.md) を参照してください。
    
## <a name="extend-an-enum"></a>列挙型を拡張します。

列挙型を拡張するには 2 つの方法があります。

+ 新しい列挙拡張子を使用するモデル参照を持つプロジェクトを作成します。 拡張する列挙値を右クリックし、**拡張を作成** を選択します。

    ![拡張列挙を作成する (方法1)](media/AddEnum02.png)

+ 拡張する列挙値を右クリックし、**新しいプロジェクトで拡張を作成** を選択します。 拡張列挙を作成する必要のあるモデルを選択するように求められます。
        
    ![拡張列挙を作成する (方法2)](media/AddEnum03.png)
        
選択されたモデルで列挙型拡張が作成されます。 新しい列挙値をこの拡張に追加することができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]