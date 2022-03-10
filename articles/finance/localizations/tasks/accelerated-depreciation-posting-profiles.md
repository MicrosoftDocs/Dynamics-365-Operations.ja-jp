---
title: 増加償却パラメーターおよび転記プロファイルのコンフィギュレーション
description: 日本では、加速償却は [レート係数]、[レートしきい値] および [計算方法] に基づいて計算されます。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, AssetPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032047878797752e10fd40090294292f5d51655279e4f66f69495c3691417e72
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714423"
---
# <a name="configure-accelerated-depreciation-parameters-and-posting-profiles"></a>増加償却パラメーターおよび転記プロファイルのコンフィギュレーション

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]