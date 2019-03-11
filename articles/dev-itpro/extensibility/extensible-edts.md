---
title: 拡張データ型
description: このトピックでは、拡張データ型 (EDT) について説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: 6f9b02081fdfdead8b9c26e43992fcbd4bc5b7d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369526"
---
# <a name="extended-data-types"></a>拡張データ型
[!include [banner](../includes/banner.md)]

拡張データ型 (EDT) には、拡張担当者が特定の動作を変更できる豊富な拡張モデルがあります。

拡張可能なソリューションを提供するには、EDT を操作する際に次のガイドラインに注意してください。

## <a name="labelhelp-text"></a>ラベル/ヘルプ テキスト
ラベルおよびヘルプ テキストのプロパティは、拡張によって変更できますが、値は 1 つだけ残すことができます。 複数のソリューションで同じ EDT のラベルが変更される場合、機能の観点でさまざまなラベルが相互に排他的です。 したがって、それらのラベルをすべて同じシステムにインストールすることはできません。

## <a name="string-size"></a>文字列サイズ
文字列サイズは、ルート EDT でのみ定義できます。 EDT とその拡張の間で定義されている最大値が使用されます。

派生 EDT の場合、EDT 間の IS-A 関係が壊れるため、文字列サイズを拡張によって変更することはできません。

文字列 EDT への割り当てでは、定義されている文字列のサイズを照合するために文字列が切り捨てられます。

## <a name="extends"></a>拡張
拡張によって**拡張**プロパティを変更することはできません。 リリース後にこのプロパティに対して行った変更はすべて、重大な変更を引き起こします。 したがって、リリース前に、プロパティが正しく設定されていることを確認する必要があります。

このプロパティを設定した場合、自分も拡張担当者も後での文字列サイズを変更することはできません。 

不要な依存関係を回避してください。 たとえば、名前や説明などの一般的な EDT を拡張しないでください。

## <a name="number-of-decimals"></a>小数点以下の桁数
拡張によって**拡張によって**プロパティを変更することはできません。

このプロパティを **True** に設定した場合、拡張担当者は小数点以下桁数を変更できます。 

このプロパティを **True** に設定した場合、以下の条件を満たすことを確認します。

+ 暗黙的またはハードコードされた四捨五入が発生しないように、すべての切り捨てロジックでは、EDT で指定されている小数点以下の桁数が受け入れられます。
+ この値は、四捨五入が正しく処理されないその他の互換性のない EDT には割り当てられません。
