---
title: 設備グループの作成および割り当て
description: この手順では、設備のグループの作成方法と設備グループの固定資産へのコンフィギュレーション方法について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetAcceleratedDepEquipmentGroup_JP, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2753b3d8e5c7861b16aaea73f541e56a250eb998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821853"
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