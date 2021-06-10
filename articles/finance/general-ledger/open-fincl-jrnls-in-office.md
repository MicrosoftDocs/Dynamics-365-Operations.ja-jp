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
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="29b42-103">Office で財務仕訳帳テンプレートを開く</span><span class="sxs-lookup"><span data-stu-id="29b42-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29b42-104">このトピックでは、Microsoft Excel テンプレートを使用してカスタム財務仕訳帳を作成するときに発生する可能性がある問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="29b42-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="29b42-105">現象</span><span class="sxs-lookup"><span data-stu-id="29b42-105">Symptom</span></span>

<span data-ttu-id="29b42-106">財務仕訳帳用のカスタム Excel テンプレートを作成しましたが、**Excel で明細行を開く** メニューに表示されません。</span><span class="sxs-lookup"><span data-stu-id="29b42-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="29b42-107">また、メニューに表示されるので選択すると、別のテンプレートが開きます。</span><span class="sxs-lookup"><span data-stu-id="29b42-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="29b42-108">解決策</span><span class="sxs-lookup"><span data-stu-id="29b42-108">Resolution</span></span>

<span data-ttu-id="29b42-109">既定の [Excel で開く] 機能では、現在のページのルート データ ソース (テーブル) を使用して、**Excel で開く** メニューのオプションとして表示される Office テンプレートまたはデータ エンティティを決定します。</span><span class="sxs-lookup"><span data-stu-id="29b42-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="29b42-110">財務仕訳帳は他の多くのタイプの仕訳帳のルート データ ソースと同じテーブル (LedgerJournalTable および LedgerJournalTrans) を使用するため、この動作は財務仕訳帳に適したエクスペリエンスではありません。</span><span class="sxs-lookup"><span data-stu-id="29b42-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="29b42-111">財務仕訳帳の [Excel で明細行を開く] 機能は、一般仕訳帳や支払仕訳帳などのコンテキストで現在作業している仕訳帳用に設計されたテンプレートを表示することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="29b42-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="29b42-112">たとえば、仕入先支払仕訳帳で使用することを目的としたテンプレートは、基本勘定を仕入先勘定として適用するように設計されます。</span><span class="sxs-lookup"><span data-stu-id="29b42-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="29b42-113">**Excel で明細行を開く** および **Excelで開く** メニューで使用できるようにテンプレートのレベルを上げる場合、簡単な開発者エクスペリエンスは、**LedgerIJournalExcelTemplate** インターフェイスを実装し **、DocuTemplateRegistrationBase** クラスを拡張することです。</span><span class="sxs-lookup"><span data-stu-id="29b42-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="29b42-114">この方法の例の多くはシステムに実装されています。</span><span class="sxs-lookup"><span data-stu-id="29b42-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="29b42-115">参照用に使用できる例の 1 つに、一般仕訳帳 (または日次仕訳帳) 用に作成された **LedgerDailyJournalExcelTemplate** インターフェイスがあります。</span><span class="sxs-lookup"><span data-stu-id="29b42-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="29b42-116">**LedgerIJournalExcelTemplate** インターフェイスがテンプレートに実装されている場合、**Excel で明細行を開く** メニューで仕訳帳の仕訳帳タイプに応じてテンプレートがフィルタ処理され、その仕訳帳で使用できるテンプレートのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="29b42-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="29b42-117">また、このインターフェイスで検証方法を指定して、勘定タイプの要件を満たしてない場合に仕訳帳用のテンプレートを開けないようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="29b42-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="29b42-118">たとえば、勘定タイプは **仕入先** または **元帳** タイプである必要があると指定できます。</span><span class="sxs-lookup"><span data-stu-id="29b42-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="29b42-119">この機能の詳細については、[[Excel で明細行を開く] メニューへのテンプレートの追加](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="29b42-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
