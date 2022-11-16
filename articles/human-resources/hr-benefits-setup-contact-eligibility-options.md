---
title: 個人の連絡先の適格性オプションのコンフィギュレーション
description: この記事では、Microsoft Dynamics 365 Human Resources で、個人の連絡先の適格性オプションを構成する方法について説明します。
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 251a12b0da364744f1d8c84324099708a2f816a1
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749285"
---
# <a name="configure-personal-contact-eligibility-options"></a>個人の連絡先の適格性オプションのコンフィギュレーション


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Microsoft Dynamics 365 Human Resources で給付金で使用できる個人の連絡先のタイプをコンフィギュレーションする方法について説明します。 個人の連絡先は、プランの対象となる個人 (扶養家族)、または計画から益を得る個人 (受益者) です。 通常、扶養家族は配偶者または子です。 受益者は、配偶者、子、信頼関係にある人、または親とすることができます。

1. **給付金管理** ワーク スペースの **設定** で、**個人の連絡先適格性オプション** を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **適格性オプション** | 適格性オプションを識別する固有の適格性オプション名またはコード。 |
   | **説明** | 適格性オプションの簡単な説明。 |
   | **連絡先適格性コード** | 個人の適格性オプションを最もよく表しているシステムコードです。 次から選択できます。 <ul><li>リレーションシップ</li><li>学生</li><li>規定年齢を超えた被扶養者</li><li>規定年齢を過ぎた無効な被扶養者</li></ul> |
   | **ステータス** | 適格性オプションの状態。 適格性オプション状態が無効に設定されている場合は、個人の連絡先に対して、その個人連絡先の適格性オプションを選択することはできません。 |
   | **リレーションシップ** | 個人の連絡先と従業員の関係を指定します。 このフィールドは、連絡先の適格性コードがリレーションシップに設定されている場合にのみ有効になります。 |
   | **年齢** | 給付金プランの受給資格を持つ個人連絡先の最少年齢。 このフィールドは、リレーションシップを選択した場合にのみ有効になります。 この年齢は、個人の連絡先の計算された年齢と比較されます。 計算された年齢: (補充日 – 個人連絡先の生年月日 / 365)。 この数値は、常に整数です。 |

4. **保存** を選択します。 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
