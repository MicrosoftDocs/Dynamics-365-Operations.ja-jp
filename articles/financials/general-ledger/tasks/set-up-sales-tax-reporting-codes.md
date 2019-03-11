---
title: 消費税レポート コードを設定します
description: 売上税レポート コードは、売上税レポートのフィールド番号です。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4543cf7eaa0b1ef8e32d3fdafa2c354cd3739256
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "335672"
---
# <a name="set-up-sales-tax-reporting-codes"></a>消費税レポート コードを設定します

[!include [task guide banner](../../includes/task-guide-banner.md)]

売上税レポート コードは、売上税レポートのフィールド番号です。 これらは国固有のレポートのレイアウトやコード別売上税支払レポートで使用され、決済期間の売上税金額をレポート コードごとに集計して印刷します。 作成した売上税レポート コードは、[売上税コード] ページの [レポートの設定] クイック タブで参照できます。 

このレコードでは、USMF デモ会社を使用します。



1. [税] > [設定] > [売上税] > [売上税レポート コード] の順に移動します。
2. [新規] をクリックします。
3. レポート コードが所属するレポート レイアウトを選択します。
    * このレイアウトは、売上税コードに使用できるレポート コードをフィルター処理するために使用されます。 各売上税コードは、レポートのレイアウトを使用する売上税所轄官庁に属する決済期間に属します。  
4. 売上税レポートのフィールドを参照する番号を入力します。
5. [レポート テキスト] フィールドに、レポートに表示する説明を入力します。
6. [簡単な説明] フィールドに、社内用の説明を入力します。
7. [保存] をクリックします。

