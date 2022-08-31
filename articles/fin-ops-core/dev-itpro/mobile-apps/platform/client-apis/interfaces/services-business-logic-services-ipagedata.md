---
title: PageData タイプ
description: ページに読み込まれたデータを表します。
author: jasongre
ms.date: 05/24/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: f8ae24e5c8d066e4ba42eae7b8820436dff6354a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282533"
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
