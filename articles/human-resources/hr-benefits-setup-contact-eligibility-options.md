---
title: 個人の連絡先適格性オプションのコンフィギュレーション
description: Microsoft Dynamics 365 Human Resources にて、個人の連絡先の適格性オプションをコンフィギュレーションします。 個人の連絡先は、受益者または扶養家族とすることができます。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009697"
---
# <a name="configure-personal-contact-eligibility-options"></a>個人の連絡先適格性オプションのコンフィギュレーション

[!include [banner](includes/preview-feature.md)]

この記事では、Microsoft Dynamics 365 Human Resources で給付金で使用する個人の連絡先のタイプをコンフィギュレーションする方法について説明します。 個人の連絡先は、受益者または扶養家族とすることができます。 

1. **給付金管理**ワーク スペースの**設定**で、**個人の連絡先適格性オプション**を選択します。

2. **新規** を選択します。

3. 次のフィールドの値を指定します。

   | フィールド | 説明 |
   | --- | --- |
   | **適格性オプション** | 適格性オプションを識別する固有の適格性オプション名またはコード。 |
   | **説明** | 適格性オプションの簡単な説明。 |
   | **連絡先適格性コード** | 個人の適格性オプションを最もよく表しているシステムコードです。 次から選択できます。 <ul><li>リレーションシップ</li><li>学生</li><li>規定年齢を超えた被扶養者</li><li>規定年齢を過ぎた無効な被扶養者</li></ul> |
   | **ステータス** | 適格性オプションの状態。 適格性オプション状態が無効に設定されている場合は、個人の連絡先に対して、その個人連絡先の適格性オプションを選択することはできません。 |
   | **リレーションシップ** | 個人の連絡先と従業員の関係を指定します。 このフィールドは、連絡先の適格性コードがリレーションシップに設定されている場合にのみ有効になります。 |
   | **年齢** | 給付金プランの受給資格を持つ個人連絡先の最大年齢。 このフィールドは、リレーションシップを選択した場合にのみ有効になります。 この年齢は、個人の連絡先の計算された年齢と比較されます。 計算された年齢: (補充日 – 個人連絡先の生年月日 / 365)。 この数値は、常に整数です。 |

4. **保存** を選択します。 
