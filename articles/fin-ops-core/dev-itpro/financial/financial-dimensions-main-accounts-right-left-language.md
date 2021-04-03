---
title: 右から左へ読み書きする言語の財務分析コードと主勘定
description: このトピックでは、右から左へ読み書きする言語を使用する際に考慮する必要がある決定について説明し、財務分析コードと主勘定を設定する必要があります。
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 496869bd3e7a372a5ec791df66fb7a8c43ccad13
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561003"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="b084e-103">右から左へ読み書きする言語での財務分析コードと主勘定</span><span class="sxs-lookup"><span data-stu-id="b084e-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b084e-104">このトピックでは、右から左へ読み書きする言語を使用する際に考慮する必要がある実装の決定について説明し、財務分析コードと主勘定を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b084e-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="b084e-105">財務分析コードと主勘定は、実装のための計画フェーズの主要部分です。</span><span class="sxs-lookup"><span data-stu-id="b084e-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="b084e-106">財務分析コードと主勘定がシステムに作成されると、**勘定構造のコンフィギュレーション**、**詳細なルール構造**、**アプリケーション統合用の財務分析コードのコンフィギュレーション** ページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="b084e-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="b084e-107">これらのページで定義された順序は、データ入力および消費のためにシステムで使用されます。</span><span class="sxs-lookup"><span data-stu-id="b084e-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="b084e-108">システムの一部の場所では、財務分析コードと主勘定は、別のフィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b084e-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="b084e-109">ただし、仕訳帳などの他の場所では、財務分析コードと主勘定は単一の文字列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="b084e-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="b084e-110">右から左のシステムの財務分析コードと主勘定を設定するためのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="b084e-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="b084e-111">勘定科目表の区切り記号を選択するときは、二重区切り記号オプションのうち 1 つを選択します: 二重ハイフン (`--`)、二重縦線 (`||`)、または 2 つのピリオド (`..`)、もしくは二重アンダースコア (`\\`)。</span><span class="sxs-lookup"><span data-stu-id="b084e-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="b084e-112">財務分析コードと主勘定の値を作成するときに、番号と右から左へ読み書きする言語文字のみを使用します。</span><span class="sxs-lookup"><span data-stu-id="b084e-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="b084e-113">財務分析コードと主勘定の値で選択した勘定科目表の区切り記号を使用することは避けてください。</span><span class="sxs-lookup"><span data-stu-id="b084e-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="b084e-114">これらのベスト プラクティスに従うことにより、システム全体のユーザー定義順序の一貫した表示を保証します。</span><span class="sxs-lookup"><span data-stu-id="b084e-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]