---
title: 圧縮記帳のある固定資産の処分
description: このタスクでは、圧縮記帳のある固定資産の日本での処理方法について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f4967a222bf0056d1898db5f70cb6abd8ef7670
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183743"
---
# <a name="dispose-of-a-fixed-asset-with-reduction-entry"></a>圧縮記帳のある固定資産の処分

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

