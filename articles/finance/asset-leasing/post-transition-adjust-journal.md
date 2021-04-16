---
title: 資産リースの移行調整仕訳入力の転記
description: このトピックでは、リース ポートフォリオを新しいリース会計基準、Accounting Standards Codification Topic 842 (ASC 842) および International Financial Reporting Standard 16 (IFRS 16) に移行できる機能について説明します。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819773"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>資産リースの移行調整仕訳入力の転記

[!include [banner](../includes/banner.md)]

このトピックでは、リース ポートフォリオを次の新しいリース会計基準、米国 (US GAAP) および International Financial Reporting Standard 16 (IFRS 16) の標準規格である、Accounting Standards Codification Topic 842 (ASC 842)、に移行するために使用できる機能について説明します。

新しい基準への切り替えに関する帳簿の設定方法については、[リース帳簿の設定](set-up-lease-books.md) を参照してください。

切り替え調整仕訳入力を作成すると、仕訳入力が生成されます。 この入力には、その日付に新しい標準が追加されたときにリースを記録したときの貸借対照表への影響が反映されます。 該当する日付のキャリー額に対して適切な資産勘定が借方に転記され、負債勘定が貸方に転記されます。 この差額は、保留中の収益に借方または貸方記入されます。

新しい会計基準に準拠するように切り替え調整を転記するには、次のステップに従います。

1. **リースの概要** ページで、リースを選択して **帳簿** を選択します。
2. 帳簿で、**支払スケジュール** を選択します。
3. **支払スケジュール** ダイアログ ボックスで、**確認** を選択します。 ダイアログ ボックスを閉じます。
4. **切り替えの調整** を選択します。

    > [!NOTE]
    > **切り替え帳簿** フィールドが使用可能な帳簿に割り当てられているリース帳簿に対してのみ、切り替え調整を作成できます。 **リースの開始日** フィールドの値が切り替え日よりも後の場合、**切り替え調整** フィールドの値は更新されません。

5. 仕訳入力を表示するには、**資産リース仕訳** を選択します。
6. 新規仕訳を選択し、**転記** を選択します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]