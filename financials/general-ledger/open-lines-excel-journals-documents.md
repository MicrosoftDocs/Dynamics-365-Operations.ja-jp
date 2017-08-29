---
title: "Excel から仕訳帳明細行とドキュメントを発行する"
description: "このトピックでは、Microsoft Excel の一般仕訳帳のドキュメント明細行入力および発行方法について説明します。 ここには、入力するトランザクションのタイプに応じて、使用できるさまざまなテンプレートに関する情報が含まれています。"
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 1fed8d162a37736883365fa765a059e5beff06be
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Excel から仕訳帳明細行とドキュメントを発行する

[!include[banner](../includes/banner.md)]


このトピックでは、Microsoft Excel の一般仕訳帳のドキュメント明細行入力および発行方法について説明します。 ここには、入力するトランザクションのタイプに応じて、使用できるさまざまなテンプレートに関する情報が含まれています。

ユーザーは、Microsoft Excel から財務仕訳帳の明細行を入力および発行することができます。 ユーザーが仕訳帳を作成した後、[**Excel で明細行を開く**] ボタンは使用できるテンプレートを表示します。 テンプレートは特定のシナリオをサポートするように設計されていますが、勘定タイプのすべての組み合わせが仕訳帳でサポートされるわけではありません。 次の表は、利用可能なテンプレートとそれらがサポートする勘定タイプを示しています。
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**テンプレート**]             | [**サポートされる勘定タイプ**]                                                                                             | [**テンプレートへのアクセス方法**]                                                          |
| 仕訳元帳明細行     | 勘定: 元帳、顧客、仕入先、銀行の相手勘定: 元帳、顧客、仕入先、銀行間でサポートされています。       | 一般仕訳帳                                                                         |
| 仕入帳         | 勘定: 仕入先の相手勘定: 会社間元帳ではサポートされていません。                                                    | AP 仕入帳                                                                     |
| 請求仕訳帳          | 勘定: 仕入先の相手勘定: 会社間元帳でサポートされています。                                                      | AP 請求仕訳帳                                                                      |
| 仕入先請求書           |                                                                                                                         | 仕入先請求書                                                                          |
| 顧客請求書仕訳帳 | 勘定: 顧客の相手勘定: 会社間元帳でサポートされています。                                                     | 一般仕訳帳                                                                         |
| 自由書式の請求書        |                                                                                                                         | [**自由書式の請求書**] ページで、[**Excel で開く**] (Microsoft Office のアイコン) をクリックします。 |
| 固定資産仕訳帳     | 元帳、銀行、顧客、または仕入先への資産。 会社間ではサポートされていません。                                               | 固定資産仕訳帳                                                                     |
| 仕入先支払仕訳帳   | 勘定: 仕入先の相手勘定: 銀行間でサポートされています。                                                 | 仕入先支払仕訳帳                                                                  |
| 顧客支払仕訳帳 | 勘定: 顧客の相手勘定: 銀行間でサポートされています。                                               | 顧客支払仕訳帳                                                                |
| プロジェクト経費仕訳帳  | 勘定: プロジェクト元帳、顧客、仕入先、仕入先の相手勘定: プロジェクト、元帳、顧客、仕入先会社間でサポートされています。 | 一般仕訳帳への経費 (プロジェクト管理および会計で)                       |

行が公開されると、それらの行が財務仕訳帳に設定されているルールに準拠していることが確認されます。 行が公開されると、ユーザーは Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition から伝票を編集または投稿することができます。 

テンプレートに財務分析コードを追加するには、追加の変更が必要です。 詳細については、「[Microsoft Excel テンプレートに分析コードを追加する](/dynamics365/unified-operations/dev-itpro/financial/add-dimensions-excel-templates)」を参照してください。 エンティティに分析コードを追加した後は、Excel デザイナーで使用でき、テンプレートに追加することができます。






