---
title: PageSubmitArgs タイプ
description: ページの OnSubmit イベントに指定された引数。
author: jasongre
ms.date: 05/26/2022
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.openlocfilehash: 6ce0b8fd28863226fe295511c28a929b5bb8b7e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273943"
---
# <a name="pagesubmitargs-type"></a>PageSubmitArgs タイプ

[!include [banner](../../../../includes/banner.md)]
[!include [mobile app deprecated](../../../../includes/mobile-app-deprecation-banner.md)]

ページの OnSubmit イベントに指定された引数。

### <a name="hierarchy"></a>階層

PageSubmitArgs <br>

## <a name="index"></a>指数

### <a name="properties"></a>プロパティ

* [dataValues](view-model-ipage-ipagesubmitargs.md#datavalues)
* [送信者](view-model-ipage-ipagesubmitargs.md#sender)

### <a name="methods"></a>メソッド

* [addMessage](view-model-ipage-ipagesubmitargs.md#addmessage)
* [キャンセル](view-model-ipage-ipagesubmitargs.md#cancel)
* [getMessages](view-model-ipage-ipagesubmitargs.md#getmessages)
* [isCancelled](view-model-ipage-ipagesubmitargs.md#iscancelled)
* [待機](view-model-ipage-ipagesubmitargs.md#wait)

## <a name="properties"></a>プロパティ

### <a name="datavalues"></a>dataValues

dataValues: any

送信アクションの伝送データを取得します。


### <a name="sender"></a>sender

sender: [Page](view-model-ipage-ipage.md)

送信アクションの送信者ページ インスタンスを取得します。


## <a name="methods"></a>メソッド

### <a name="addmessage"></a>addMessage


addMessage(message: string, type: any): any

表示される検証/エラー メッセージを追加します。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| メッセージ|string||
| タイプ|any||

#### <a name="returns-any"></a>any を返します

### <a name="cancel"></a>キャンセル


cancel(): any

アクションの送信を禁止します。

#### <a name="returns-any"></a>any を返します

### <a name="getmessages"></a>getMessages


getMessages(): string [ ]

以前に追加されたすべてのメッセージを取得します

#### <a name="returns-string--"></a>string [ ] を返します



### <a name="iscancelled"></a>isCancelled


isCancelled(): boolean

送信アクションがキャンセルされているかどうかを確認します。

#### <a name="returns-boolean"></a>ブール値を返します



### <a name="wait"></a>wait


wait(promise: Promise &lt;any&gt;): any

送信を続行する前に、指定された約束を待ちます。
待機を介して添付されたすべての約束は、送信アクションが実行される前に解決される必要があります。


#### <a name="parameters"></a>パラメーター

| 氏名 | 種類 | 説明 |
| ---- | ---- | ----------- |
| promise|&lt;任意&gt;の約束||

#### <a name="returns-any"></a>any を返します



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
