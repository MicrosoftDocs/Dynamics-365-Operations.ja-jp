---
title: Office で財務仕訳帳テンプレートを開く
description: このトピックでは、Microsoft Excel テンプレートを使用してカスタム財務仕訳帳を作成するときに発生する可能性がある問題について説明します。
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089460"
---
# <a name="open-financial-journal-templates-in-office"></a>Office で財務仕訳帳テンプレートを開く

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Excel テンプレートを使用してカスタム財務仕訳帳を作成するときに発生する可能性がある問題について説明します。

## <a name="symptom"></a>現象

財務仕訳帳用のカスタム Excel テンプレートを作成しましたが、**Excel で明細行を開く** メニューに表示されません。 また、メニューに表示されるので選択すると、別のテンプレートが開きます。

## <a name="resolution"></a>解決策

既定の [Excel で開く] 機能では、現在のページのルート データ ソース (テーブル) を使用して、**Excel で開く** メニューのオプションとして表示される Office テンプレートまたはデータ エンティティを決定します。 財務仕訳帳は他の多くのタイプの仕訳帳のルート データ ソースと同じテーブル (LedgerJournalTable および LedgerJournalTrans) を使用するため、この動作は財務仕訳帳に適したエクスペリエンスではありません。

財務仕訳帳の [Excel で明細行を開く] 機能は、一般仕訳帳や支払仕訳帳などのコンテキストで現在作業している仕訳帳用に設計されたテンプレートを表示することを目的としています。 たとえば、仕入先支払仕訳帳で使用することを目的としたテンプレートは、基本勘定を仕入先勘定として適用するように設計されます。

**Excel で明細行を開く** および **Excelで開く** メニューで使用できるようにテンプレートのレベルを上げる場合、簡単な開発者エクスペリエンスは、**LedgerIJournalExcelTemplate** インターフェイスを実装し **、DocuTemplateRegistrationBase** クラスを拡張することです。 この方法の例の多くはシステムに実装されています。 参照用に使用できる例の 1 つに、一般仕訳帳 (または日次仕訳帳) 用に作成された **LedgerDailyJournalExcelTemplate** インターフェイスがあります。

**LedgerIJournalExcelTemplate** インターフェイスがテンプレートに実装されている場合、**Excel で明細行を開く** メニューで仕訳帳の仕訳帳タイプに応じてテンプレートがフィルタ処理され、その仕訳帳で使用できるテンプレートのみ表示されます。 また、このインターフェイスで検証方法を指定して、勘定タイプの要件を満たしてない場合に仕訳帳用のテンプレートを開けないようにすることもできます。 たとえば、勘定タイプは **仕入先** または **元帳** タイプである必要があると指定できます。

この機能の詳細については、[[Excel で明細行を開く] メニューへのテンプレートの追加](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md)を参照してください。
