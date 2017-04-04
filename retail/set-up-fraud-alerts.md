---
title: "詐欺警告の設定"
description: "このトピックでは、注文が処理されるとき、詐欺の可能性ある情報を顧客サービス担当者に警告するルールを設定する方法について説明します。 自動または手動で疑わしい注文を保留にするために使用する、特殊なコードを定義できます。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabb7ee23e90feca818bebfa29c7048987193e4c
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fraud-alerts"></a>詐欺警告の設定

このトピックでは、注文が処理されるとき、詐欺の可能性ある情報を顧客サービス担当者に警告するルールを設定する方法について説明します。 自動または手動で疑わしい注文を保留にするために使用する、特殊なコードを定義できます。 

詐欺チェックルールを設定および使用する前に、コール センター パラメーターで、詐欺チェック機能が有効で、基本的な詐欺チェック値が定義されている必要があります。 詐欺警告には、次の 2 つのタイプがあります。

-   **静的ルール** ブラックリストに載せられた電話番号など、特定の値を使用します。
-   **動的ルール** 変数と要件を含めることができます。

動的ルールを作成する前に、だれにルールを適用するか、またいつルールを適用するかを定義する変数と条件を作成する必要があります。 たとえば、顧客 1202 が 1,000.00 以上の注文をしたとき、顧客支払が確認できるまで販売注文を保留するルールを作成します。 この場合、変数は顧客 1202 と注文合計 1,000.00 です。 条件は、顧客 1202 が 1,000.00 以上の注文をしたとき、顧客支払が確定されるまで、販売注文が保留されることを指定します。


