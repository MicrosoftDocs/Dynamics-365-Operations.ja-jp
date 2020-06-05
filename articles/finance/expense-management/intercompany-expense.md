---
title: 会社間経費
description: 組織内の 1 つの法人で雇用されている作業者は、同じ組織の別の法人の作業を実行する場合があります。 この場合、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390887"
---
# <a name="intercompany-expenses"></a>会社間経費

[!include [banner](../includes/banner.md)]

組織内の 1 つの法人で雇用されている作業者は、同じ組織の別の法人の作業を実行する場合があります。 この場合、会社間経費機能を使用して、作業が実行された法人に作業者の経費を割り当てることができます。 作業者を雇用する法人は、貸出側の法人と呼ばれます。 従業員が経費を支払う法人は、借入側法人と呼ばれます。 

作業者が別の法人に対して実行される作業の経費を作成および送信する前に、貸出側法人で、**経費管理パラメーター** ページで **会社間経費明細行を許可** オプションを選択します。 

## <a name="tax-posting-for-intercompany-expenses"></a>会社間の経費の税金計上

[!include [banner](../includes/banner.md)]

経費精算書の借入先の法人に関連付けられている税グループを使用する場合は、総勘定元帳の売上税を設定する際にそれを構成する必要があります。 総勘定元帳パラメータ ( **会社間税転記を行う法人)** が**ソース**に設定され、**売上税課税ルール** が **いいえ** に設定されている場合は、借入法人の税の組み合わせが使用されます。 同じパラメータが **宛先**に設定されている場合は 、借入法人の税の組み合わせが使用されます。 米国の法人で、パラメータが **ソース** に設定されている場合は、新しい **元帳転記グループ** ページでも **売上税収入** フィールドを構成する必要があります。 会計エンジンでは、このフィールドの情報を税務関連の勘定項目に使用します。   
この動作は、プロジェクトの有無に関わらず、経費明細行では一貫しています。  
