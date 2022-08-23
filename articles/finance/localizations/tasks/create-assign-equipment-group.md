---
title: 設備グループの作成および割り当て
description: この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: AssetAcceleratedDepEquipmentGroup_JP, AssetTable
ms.openlocfilehash: a07af8ce97cec78e1dd3b9adf9de8cc3a3d92b1e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281197"
---
# <a name="create-and-assign-an-equipment-group"></a>設備グループの作成および割り当て

[!include [banner](../../includes/banner.md)]

この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。



設備のグループは、加速償却ドキュメントを作成する際の既定値を提供します。



この手順を完了するためには、[資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="create-equipment-group"></a>設備グループの作成
1. [固定資産] > [設定] > [設備グループ] に移動します。
2. [新規] をクリックします。
3. [固定資産設備グループ] フィールドに値を入力します。
4. [説明] フィールドで値を入力します。
5. [設備のタイプ] フィールドに値を入力します。
6. [場所] フィールドで、値を入力します。
    * これが加速償却ドキュメントを作成する際の既定値になります。  
7. [設備のタイプ区分] フィールドに値を入力します。
8. [業種の 1 日あたりの平均時間] フィールドに数値を入力します。
    * これが加速償却ドキュメントを作成する際の既定値になります。  
9. [年間の平均稼働日] フィールドに数値を入力します。
    * これが加速償却ドキュメントを作成する際の既定値になります。  
10. [保存] をクリックします。

## <a name="configure-default-equipment-group-on-fixed-assets"></a>固定資産の既定の設備グループのコンフィギュレーション
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 設備グループを割り当てる固定資産の選択
3. [編集] をクリックします。
4. [固定資産設備グループ] フィールドに値を入力します。
5. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
