---
title: PageData タイプ
description: ページに読み込まれたデータを表します。
author: tonyafehr
ms.date: 05/24/2022
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: tfehr
ms.openlocfilehash: 99a5824584fd0bdb7fe0994e072b649c5c7fee1c
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811591"
---
# <a name="pagedata-type"></a>PageData タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

ページに読み込まれたデータを表します。

### <a name="hierarchy"></a>階層

PageData <br>

## <a name="index"></a>指数

### <a name="methods"></a>メソッド

* [getControlValue](services-business-logic-services-ipagedata.md#getcontrolvalue)
* [setControlValue](services-business-logic-services-ipagedata.md#setcontrolvalue)

## <a name="methods"></a>メソッド

### <a name="getcontrolvalue"></a>getControlValue


getControlValue(controlName: string): any

ページでデータ セットから直接読み込まれるコントロールの値を取得します。
「値」は、あらゆる種類のコントロールで柔軟に定義されており、通常は、コントロールと共に表示または操作されるプライマリ単一フィールド値を示します。 一部の複雑なコントロール (ルックアップやリストなど) には、単純な値がない場合があるため、この API を通じてアクセスできません。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string|値を取得する対象のコントロールの名前|

#### <a name="returns-any"></a>any を返します

### <a name="setcontrolvalue"></a>setControlValue


setControlValue(controlName: string, value: any): any

ページでデータ セットに直接読み込まれるコントロールの値を設定します。
「値」は、あらゆる種類のコントロールで柔軟に定義されており、通常は、コントロールと共に表示または操作されるプライマリ単一フィールド値を示します。 一部の複雑なコントロール (ルックアップやリストなど) には、単純な値がない場合があるため、この API を通じてアクセスできません。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| controlName|string|値を設定する対象のコントロールの名前|
| 値|any|設定する値|

#### <a name="returns-any"></a>any を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
