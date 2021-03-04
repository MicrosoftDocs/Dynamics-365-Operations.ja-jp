---
title: サービス合意とプロジェクトの統合
description: サービス合意およびサービス合意項目を操作する場合、プロジェクト管理と会計の領域で設定するデータを使用します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 578e4b9fe5ef487e999fd0de28d7566bad21fd89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432182"
---
# <a name="integration-for-service-agreements-and-projects"></a>サービス合意とプロジェクトの統合 

[!include [banner](../includes/banner.md)]


サービス合意およびサービス合意項目を操作する場合、**プロジェクト管理と会計** の次の領域で設定するデータを使用します。

## <a name="project-prices"></a>プロジェクト価格

サービス合意トランザクションの原価および販売価格は、サービス合意に関連付けられたプロジェクトに適用される原価価格設定から算出されます。 原価価格および販売価格は、プロジェクト、従業員、およびカテゴリ別に設定できます。 

## <a name="project-validation"></a>プロジェクトの検証

サービス合意明細行で選択できるプロジェクト、従業員、およびカテゴリは、**プロジェクト管理と会計** の検証設定で制限できます。 検証設定を使用すると、従業員、プロジェクト、およびカテゴリを組み合わせてアクセスを制御できます。 

## <a name="project-line-properties"></a>プロジェクト明細行プロパティ

明細行プロパティは、サービス合意明細行に自動的に入力されます。

明細行プロパティは、**プロジェクト管理と会計** の **明細行プロパティ** フォームで作成されます。 サービス合意に入力される明細行プロパティは、サービス合意に対して選択したプロジェクトに関連付けられ、以降、サービス合意明細行に継承されます。 

## <a name="default-offset-accounts"></a>既定の相手勘定

経費トランザクションを入力すると、トランザクションに対して、既定の経費相手勘定が自動的に選択されます。 既定の経費勘定は、現在のサービス合意に関連付けられているプロジェクトに対して設定します。

## <a name="project-categories"></a>プロジェクト カテゴリ

サービス合意項目で使用できるカテゴリは、**プロジェクト管理と会計** の **プロジェクト カテゴリ** フォームで設定します。 

> [!NOTE]
> <P><STRONG>プロジェクト カテゴリ</STRONG>フォームの<STRONG>プロジェクト</STRONG>タブの<STRONG>仕訳帳で有効</STRONG>チェック ボックスがオンになっているカテゴリを選択できます。 ただし、<STRONG>プロジェクト管理および会計パラメーター</STRONG>フォームの<STRONG>仕訳帳</STRONG>タブで<STRONG>有効ではないカテゴリ</STRONG>チェック ボックスがオンになっている場合、すべてのカテゴリは選択可能です。</P>

## <a name="project-parameters"></a>プロジェクト パラメーター

**プロジェクト管理および会計パラメーター** フォームの **仕訳帳** タブで **退職済作業者** フィールドが選択されている場合、**サービス契約** および **サービス注文** フォームで無効な従業員と有効な従業員を選択できます。

また、**サービス注文** フォームの **プロジェクト** タブで、**開始時刻** および **終了時刻** フィールドを有効にして、サービス注文明細行に開始時刻と終了時刻を入力することもできます。

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a>サービス注文の開始時刻と終了時刻の機能の有効化

1.  **プロジェクト管理と会計** \> **設定** \> **プロジェクト管理および会計パラメーター** の順にクリックします。

2.  **仕訳帳** タブをクリックし、**開始時刻と終了時刻の表示** チェック ボックスをオンにします。

3.  **プロジェクト管理および会計** \> **設定** \> **仕訳帳** \> **仕訳帳名** の順にクリックします。

4.  サービス注文に関連付けられている仕訳帳名を選択します。

5.  **一般** タブをクリックし、**開始時刻と終了時刻の表示** チェック ボックスをオンにします。


> [!NOTE]
> <P><STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>仕訳帳</STRONG>タブの<STRONG>時間</STRONG>フィールドで、サービス注文の仕訳帳名を選択します。</P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]