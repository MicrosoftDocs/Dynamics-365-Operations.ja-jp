---
title: 完了レポート仕訳帳が転記されるとエラーが発生する
description: 完了レポート仕訳帳を転記すると、注文済み注文数量を減らすことができないというエラー メッセージが表示されます。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750933"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>完了レポート仕訳帳が転記されるとエラーが発生する

KB 番号: 4612891

## <a name="symptoms"></a>現象

**完了レポート** 仕訳帳を転記すると、エラーが発生し 、次のエラー メッセージが表示されます。

> 注文済数量を削減できません。十分な数の注文済ステータスの未処理の在庫トランザクションがありません。 品目は購買、受取り、または登録済みです。

このエラーは、**完了レポート** 仕訳帳の最初の行で **エラー数量** フィールドが設定され、最後の行で **商品数量** フィールドが設定されている場合にのみ発生します。 最後の行で **エラー数量** フィールドが設定されている場合、エラーは発生しません。

## <a name="resolution"></a>解像度

このエラーを防ぐには、**生産管理パラメーター** ページを開き、**全般** タブで、**エラー数量を含む残数量の増加** オプションを *はい* に設定します 。
