---
title: 日本の消費税レポートの設定
description: このタスクでは、日本の消費税申告をサポートするシステムの設定について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerBadDebtAccounts_JP, OMLegalEntity, TaxTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32f8ffd4370c1f7c21830ee6f8f15521430261fd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174647"
---
# <a name="setup-japan-consumption-tax-report"></a>日本の消費税レポートの設定

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクでは、日本の消費税申告をサポートするシステムの設定について説明します。 このタスクでは、一般会計パラメータ、法人、売上税申告勘定および売上税コードを修正します。 

このタスクは デモ データ会社 JPMF を使用して作成されました。




## <a name="enable-the-consumption-tax-report"></a>消費税申告を有効にする
1. [税] > [設定] > [パラメーター] > [総勘定元帳パラメーター] の順に移動します。
2. [売上税] タブをクリックします。
3. [日本の税申告] セクションを展開します。
4. [消費税申告] フィールドで [はい] を選択します。

## <a name="tax-reporting-accounts"></a>税申告勘定
1. [税] > [設定] > [売上税] > [税申告勘定] の順に移動します。
2. [編集] をクリックします。
3. [貸倒損失] フィールドで、任意の値を指定します。
    * 例: 84720  
4. [償却債権取立益] フィールドで、任意の値を指定します。
    * 例: 84710  

## <a name="enter-japan-reporting-information-for-a-legal-entity"></a>法人の日本報告書情報を入力
1. [組織管理] > [組織] > [法人] の順に移動します。
2. [登録番号] セクションを展開します。
3. [編集] をクリックします。
4. [経理担当者] フィールドに値を入力します。
5. [代表者氏名または氏名] フィールドに値を入力します。

## <a name="enter-report-setup-information-for-a-sales-tax-code"></a>売上税コードのレポート設定情報を入力
1. [税] > [間接税] > [売上税] > [売上税コード] の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、 [売上税コード] フィールドを「JP」の値でフィルタリングします。
3. [レポートの設定] セクションを展開します。
4. [編集] をクリックします。
    * レポート コードが正しくコンフィギュレーションされたか確認します。   

