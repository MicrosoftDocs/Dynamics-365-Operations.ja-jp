---
title: 請求書における TDS の計算
description: この記事では、請求書レベルで源泉徴収 (TDS) が計算されるトランザクションについての参考情報を提供します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: efc12e0839fe87e9db435f481ce1fd733c286d6c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855366"
---
# <a name="tds-calculation-on-invoices"></a>請求書における TDS の計算

[!include [banner](../includes/banner.md)]

この記事では、請求書レベルで源泉徴収 (TDS) が計算されるトランザクションについての参考情報を提供します。

| シリアル番号 | トランザクション タイプ                                 | トランザクション金額 | ページ名とパスの選択                                 | 勘定タイプと相手勘定タイプ                         |
| ------------- | ------------------------------------------------ | ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1.            | 仕入先からのの購買/費用の計上   | 借方または貸方  | 一般仕訳帳ページ ([総勘定元帳] > [仕訳帳エントリ] > [一般仕訳帳])、請求書承認仕訳帳ページ ([買掛金管理] > [請求書の承認])、請求仕訳帳ページ ([買掛金管理] > [請求書] > [請求仕訳帳]) | 仕入先 (Dr.)  仕入先 (Cr.)  源泉徴収税は、勘定科目が転記タイプが **購買** もしくは **現金** の場合にのみ、仕入先と元帳の組み合わせに対して計算されます。 |
| 2.            | 顧客からの仕入れ/経費計上 | 借方または貸方  | [一般仕訳帳] ページ ([総勘定元帳] > [仕訳帳エントリ] > [一般仕訳帳])、請求仕訳帳ページ ([買掛金管理] > [請求書] > [請求仕訳帳]) | 仕入先 (Dr.)、顧客 (Cr.)                                 |
| 3.            | 仕入先からの固定資産の購入              | 借方または貸方  | 一般仕訳帳ページ ([総勘定元帳] > [仕訳帳エントリ] > [一般仕訳帳])、請求書登録仕訳帳ページ ([買掛金管理] > [請求書の登録])、請求仕訳帳ページ ([買掛金管理] > [請求書] > [請求仕訳帳]) | 固定資産 (Dr.)、 仕入先 (Cr.)                             |
| 4.            | 顧客からの固定資産の購入            | 借方または貸方  | [一般仕訳帳] ページ ([総勘定元帳] > [仕訳帳エントリ] > [一般仕訳帳])、請求仕訳帳ページ ([買掛金管理] > [請求書] > [請求仕訳帳]) | 固定資産 (Dr.)、 顧客 (Cr.)                           |
| 5.            | 購買請求書 (TDS 買掛金)                  |                    | 買掛金勘定のページ ([買掛金勘定] > [発注書] > [すべての発注書]) |                                                              |
| 6.            | 売上請求書 (TDS 売掛金)                  |                    | [販売注文] ページ ([売掛金管理] > [注文] > [すべての販売注文])、自由形式の請求書ページ ([売掛金管理] > [請求書] > [すべての自由形式の請求書]) |                                                              |
