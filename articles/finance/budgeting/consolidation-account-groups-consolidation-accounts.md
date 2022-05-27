---
title: 連結勘定グループおよび追加連結勘定
description: このトピックでは、連結勘定グループと追加連結勘定について、およびそれら使用方法について説明します。
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: kfend
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5ca7a50fcac53f1636da15b2d7977174b087ac25
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711696"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>連結勘定グループおよび追加の連結勘定

[!include [banner](../includes/banner.md)]

このトピックでは、連結勘定グループと追加連結勘定について、およびそれら使用方法について説明します。

## <a name="consolidation-account-groups"></a>連結勘定グループ

連結勘定グループで、データを連結するのに使用する勘定のグループを作成することができます。 通常、連結勘定グループは政府が定めた勘定科目を表します。 連結勘定グループは、本社が定義したグループに勘定をマッピングすることも可能です。 **連結** モジュールの **設定** 領域で連結勘定グループを検索できます。 新しいグループを追加するときに、勘定グループと名称の固有 ID を入力します。

## <a name="additional-consolidation-accounts"></a>追加連結勘定
連結統合で、既存の勘定科目表から連結勘定グループに勘定を割り当てることができます。 その後、連結勘定の値と名前を指定できます。 

**連結** モジュールの **設定** 領域で追加の連結勘定を検索できます。 新しい連結勘定を作成するときに、次の情報を指定する必要があります。

-   **主勘定** – このフィールドは、このページで選択した勘定科目表に基づいているすべての主勘定を示すルックアップです。 アカウントを選択すると、名前が **主勘定名** フィールドに自動的に入力されます。
-   **連結勘定グループ** – このフィールドを使用して、勘定を割り当てるグループを指定します。 2 つの異なる方法で連結する場合、4 つすべての連結勘定グループに同じ勘定を追加する必要があります。
-   **連結勘定** – 連結勘定の値を入力します。 この値は、勘定科目表の勘定である必要はありません。 必要とするどの値でも可能です。
-   **連結勘定名** – 照会およびレポートに表示させる勘定の名前を入力します。
-   **SAT レベル** – このフィールドは、メキシコの税務当局に取引明細書をレポートするのに使用されます。 

連結勘定グループおよび追加の連結勘定の作成を終了すると、[オンラインで連結] プロセスでこのグループを選択できます。


詳細については、[連結グループおよび追加の連結勘定の作成](../general-ledger/tasks/create-consolidation-groups.md)を参照してください。 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
