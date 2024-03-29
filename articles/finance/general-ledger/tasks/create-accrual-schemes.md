---
title: 発生主義スキーマの作成
description: この記事では、発生主義スキーマを作成する方法を説明します。
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8974eed40a60aeee5a32932ac070a870289ec20a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858428"
---
# <a name="create-accrual-schemes"></a>発生主義スキーマの作成

[!include [banner](../../includes/banner.md)]

この記事では、発生主義スキーマを作成する方法を説明します。 このタスクでは、USMF というデモ会社を使用します。

1. **ナビゲーション ウィンドウ > モジュール > 総勘定元帳 > 仕訳帳の設定 > 発生主義スキーマ** の順に移動します。
2. **新規** を選択します。
3. **発生主義スキーマ ID** フィールドに値を入力します。
4. **発生主義スキーマの説明** フィールドに値を入力します。
5. **借方** フィールドで、任意の値を指定します。 定義した主勘定は、仕訳帳伝票の明細行の借方主勘定と置き換えられ、元帳計上トランザクションに基づく繰延の取消にも使用されます。  
6. **貸方** フィールドで、任意の値を指定します。 定義した主勘定は、仕訳帳伝票の明細行の貸方主勘定と置き換えられ、元帳計上トランザクションに基づく繰延の取消にも使用されます。  
7. トランザクションの転記時に、どのように伝票を判別するかを **伝票** フィールドで選択します。
8. **説明** フィールドに、転記されるトランザクションを説明する値を入力します。
9. **期間の頻度** フィールドで、トランザクションの発生頻度を選択します。
10. **期間別の発生数** フィールドに数値を入力します。
11. **トランザクションの転記** フィールドで、トランザクションを転記する時期、**毎月** などを選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
