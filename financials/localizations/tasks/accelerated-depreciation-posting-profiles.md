--- 
title: "増加償却パラメーターおよび転記プロファイルのコンフィギュレーション (日本)"
description: "日本では、加速償却は [レート係数]、[レートしきい値] および [計算方法] に基づいて計算されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 82a16bdd917f6d03c06af9aa6c5c6f033242c896
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="configure-accelerated-depreciation-parameters-and-posting-profiles-japan"></a>増加償却パラメーターおよび転記プロファイルのコンフィギュレーション (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

日本では、加速償却は [レート係数]、[レートしきい値] および [計算方法] に基づいて計算されます。 これらのパラメーターは、加速償却ドキュメントで提供されています。 これらを固定資産パラメーターでコンフィギュレーションすることで、加速償却ドキュメントに対する既定値が提供されます。 



加速償却金額を転記するためには、最初に [加速償却] に対する [主勘定] と [相手勘定] を [固定資産転記プロファイル] でコンフィギュレーションする必要があります。



この手順では、加速償却パラメーターと転記プロファイルの設定について説明します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="configure-parameters-for-accelerated-depreciation"></a>加速償却パラメータのコンフィギュレーション
1. [固定資産] > [設定] > [固定資産パラメーター] の順に移動します。
2. [減価償却] セクションを展開または折りたたみます。
3. [レート係数] フィールドに数値を入力します。
    * これが各加速償却ドキュメントに対する既定値を提供します。  
4. [レートしきい値] フィールドに数値を入力します。
    * これが各加速償却ドキュメントに対する既定値を提供します。  
    * どの既定式を使用して毎日の平均過剰使用量時間を計算するかを指定します。  

## <a name="configure-a-posting-profile"></a>転記プロファイルのコンフィギュレーション
1. [固定資産] > [設定] > [固定資産転記プロファイル] の順に移動します。
2. [加速償却] セクションを展開または折りたたみます。
    * [加速償却] に使用する [主勘定] と [相手勘定] を指定します。  


