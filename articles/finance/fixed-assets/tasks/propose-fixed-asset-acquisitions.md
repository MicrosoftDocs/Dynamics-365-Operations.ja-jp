---
title: 固定資産の取得の提案
description: このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 99202763ae32d02f94f1590783727d4f2cf7a7bbe45963d0e175bfc449b134d9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742932"
---
# <a name="propose-fixed-asset-acquisitions"></a>固定資産の取得の提案

[!include [banner](../../includes/banner.md)]

このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。 これは USMF の法人に対して経理担当ロールとデモ データを使用します。 固定資産提案仕訳帳を使用して固定資産を取得するには、最初に固定資産レコードを作成し、次に、取得価格を資産帳簿に定義する必要があります。

## <a name="create-an-asset-acquisition-proposal"></a>資産取得提案を作成する

資産取得提案を作成するには、次の手順を実行します。 

1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳** に移動します。
2. **新規** を選択します。
3. **名前** フィールドで値を入力または選択します。
4. アクション ウィンドウで、**明細行** を選択します。
5. **提案** を選択します。
6. **取得提案** を選択します。
7. **フィルター** を選択します。 **リセット** を選択すると、前の値がクリアされます。
8. **固定資産番号** の行を選択します。
9. **基準** フィールドで、値を入力または選択します。 この提案と一緒に取得したい固定資産の残余基準を設定します。  
10. **OK** を 2 回選択して、ウィンドウを終了します。
- 作成されたトランザクション明細行を確認します。  
- 帳簿で設定された取得日付と取得価格が付いている固定資産のみが取得提案に含まれます。  
11. ページで、**帳簿** タブを選択します。
12. **投稿** を選択します。

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a>取得提案に既定の財務分析コードを含める

取得トランザクションは、Excel アドインを使用して作成できます。このトランザクションは、**固定資産 > 仕訳帳エントリ > 固定資産仕訳帳** にアクセスして作成できます。 新しい仕訳帳を作成し、ページの **明細行** セクションに移動して Excel アイコンを選択し、固定資産仕訳帳明細行を選択します。 仕訳帳明細行を表す Excel テンプレートが作成され、開きます。 テンプレートに追加する仕訳帳明細行のデータを追加し、その情報を再度システムに公開します。 

選択した資産帳と、Excel テンプレートに入力された対応する固定資産に対して既定の分析コードが設定されている場合、Excel からシステムに仕訳帳を発行するときに、既定の財務分析コードが資産帳マスター データから呼び出されます。 Excel アドインから固定資産仕訳帳を発行する際に、資産帳に自動的に財務分析コードを含めるには、既定の分析コードを事前に設定する必要があります。  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
