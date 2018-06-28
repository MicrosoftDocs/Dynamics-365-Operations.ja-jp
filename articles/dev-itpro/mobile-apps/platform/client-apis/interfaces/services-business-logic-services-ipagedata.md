---
title: PageData
description: "ページに読み込まれたデータを表します。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: d38edf21342f6c19e12073daebb3355c598633bb
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="pagedata-type"></a>PageData タイプ

[!include [banner](../../../../includes/banner.md)]

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


