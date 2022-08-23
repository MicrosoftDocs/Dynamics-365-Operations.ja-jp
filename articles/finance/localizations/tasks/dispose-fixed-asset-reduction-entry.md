---
title: 圧縮記帳のある固定資産の処分
description: このタスクでは、圧縮記帳のある固定資産の日本での処理方法について説明します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
ms.openlocfilehash: e5398563b83b60d629ad18f88a85e085b1d59de7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267642"
---
# <a name="dispose-of-a-fixed-asset-with-reduction-entry"></a>圧縮記帳のある固定資産の処分

[!include [banner](../../includes/banner.md)]

このタスクでは、圧縮記帳のある固定資産の日本での処理方法について説明します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



このタスクは、デモ データ会社 JPMF を使用して完了しました。

1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [明細行] をクリックします。
5. [提案] をクリックします。
6. [処分 - 仕損] をクリックします。
7. 処分トランザクションの日付の入力
8. [フィルター] をクリックします。
9. [基準] フィールドに値を入力します。
10. [OK] をクリックします。
11. [OK] をクリックします。
12. 固定資産の処分の経費が転記される主勘定を入力します。
    * 仕訳帳に処分の経費を後で入力することもできます。     固定資産の主勘定と減価償却累計額の主勘定およびそのほかの関連固定資産勘定は、固定資産の転記プロファイル コンフィギュレーションに従って自動的に設定されます。  
    * 圧縮記帳ドキュメントは、固定資産ドキュメントとは別に処分されます。  
    * 元の助成金額および累計償却額は、固定資産の転記プロファイルのコンフィギュレーションに従って自動的に設定されます。  
13. [転記] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
