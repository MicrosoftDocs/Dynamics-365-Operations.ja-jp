---
title: 住所をサービス注文に追加する
description: この記事では、サービス注文に顧客の住所を追加する方法について説明します。
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015728"
---
# <a name="add-an-address-to-a-service-order"></a>住所をサービス注文に追加する

[!include [banner](../includes/banner.md)]

この記事では、サービス注文に顧客の住所を追加する方法について説明します。 サービス注文を作成する際、住所情報は、そのサービス注文が関連付けられているプロジェクトから転送されます。 ただし、顧客、仕入先、サイト、倉庫、サービス注文およびプロジェクトの Microsoft Dynamics AX に既に入力した住所から別の場所を選択することができます。

また、新しい住所を作成することもできます。 既定では、新しい住所はプロジェクトに転送されます。 ただし、新しい住所がサービスのこのインスタンスにのみ関連するよう指定できます。 その場合、新しい住所はプロジェクトに転送されません。

## <a name="create-a-customer-address-for-a-service-order"></a>サービス注文に対する顧客の住所の作成

サービス注文に住所を追加するには、次の手順に従います。

1. **サービス管理** \> **サービス注文** \> **サービス注文** に移動します。

1. 住所を作成するサービス注文を開きます。

1. **ヘッダー** タブを開きます。

1. **住所** クイック タブを展開し、クイック タブ ツール バーから **住所の追加** を選択します。

1. **新しい住所** ダイアログに、住所の一意の名前を入力し、残りのフィールドに入力します。 

    > [!WARNING]
    > 既存の住所と同じ名前を入力した場合、残りのフィールドに入力した情報が、既存の住所の情報に上書きされます。

1. 自分のサービス注文に新しい住所をコピーするには **OK** を選択します。

## <a name="specify-an-alternative-address-on-a-service-order"></a>サービス注文に対する代替住所の指定

サービス注文に別の住所を追加するには、次の手順に従います。

1. **サービス管理** \> **サービス注文** \> **サービス注文** に移動します。

1. 別の住所を入力するサービス注文を開きます。

1. **ヘッダー** タブを開きます。

1. **住所** クイック タブを展開し、クイック タブ ツール バーから **その他の住所** を選択します。

1. **住所の選択** ダイアログ ボックスの上のドロップダウン リストから **サービス注文** を選択します。

1. 住所を選択して **OK** を選択し、自分のサービス注文にコピーします。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]