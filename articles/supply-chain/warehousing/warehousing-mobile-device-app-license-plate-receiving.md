---
title: Warehouse Mobile App 経由のライセンス プレート受け取り
description: このトピックでは、現物在庫を受け取るためにライセンス プレート入庫プロセスの使用をサポートするように Warehouse Mobile App を設定する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261350"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a>Warehouse Mobile App 経由のライセンス プレート受け取り

このトピックでは、現物在庫の受け取りにライセンス プレート入庫プロセスを使用できるように Warehouse Mobile App を設定する方法について説明します。

この機能を使用すると、事前出荷明細通知 (ASN) に関連する入庫在庫の受け取りを簡単に記録できます。 倉庫管理プロセスを使用して移動オーダーを出荷すると、システムは ASN を自動的に作成します。 発注書プロセスでは、ASN は手動で記録することも、入荷 ASN データ エンティティ プロセスを使用して自動的にインポートすることもできます。

ASN データは、*梱包構造* を使用して、積荷と出荷にリンクされ、パレット (親のライセンス プレート) にはケース (入れ子になったライセンス プレート) を含めることができます。

> [!NOTE]
> 入れ子になったライセンス プレートを持つ梱包構造を使用する場合、在庫トランザクションの数を減らすには、システムによって親ライセンス プレート上の現物手持在庫が記録されます。 梱包構造データに基づいて、親ライセンス プレートから入れ子になったライセンス プレートに現物手持在庫を移動するには、モバイル デバイスはで、*入れ子になったライセンス プレートに梱包* 作業作成プロセスに基づくメニュー項目を用意する必要があります。

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>入荷の概要ページを表示またはスキップする

*モバイル デバイスに入荷の概要ページを表示するかどうかを制御する* 機能を使用して、追加の詳細な倉庫アプリ フローを、ライセンス プレートの入庫プロセスの一部として利用できます。

この機能を使用するには、システム上で有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています:

- **モジュール:** *倉庫管理*
- **機能名:** *モバイル デバイスに入荷の概要ページを表示するかどうかを制御する*

この機能を有効にすると、ライセンス プレートの受け取り、またはライセンスプレートの受け取りとプット アウェイのモバイル デバイス メニュー項目で、**入荷の概要ページを表示** 設定が提供されます。 この設定には、次のオプションがあります:

- **詳細な概要の表示** – ライセンス プレートの受け取り中に、作業者は、完全な ASN 情報を示す追加のページが表示されます。
- **概要のスキップ** – 作業者は完全な ASN 情報を参照することはできません。 倉庫作業者は、入庫プロセス中に廃棄コードを設定したり、例外を追加したりすることもできなくなります。

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする

既に存在するライセンス プレート ID が ASN に含まれ、ライセンス プレート登録が行われている倉庫の場所以外の倉庫の場所に現物手持在庫データがある場合、ライセンス プレートの入庫プロセスは使用できません。

流通倉庫がライセンス プレートを追跡しない (したがって、ライセンス プレートごとの現物手持在庫も追跡しない) 移動オーダーのシナリオの場合、*移動オーダー出荷済ライセンス プレートが出荷先倉庫以外の別の倉庫で使用されないようにする* 機能を使用して、輸送中のライセンス プレートを物理的に手動で更新することを防止できます。

この機能を使用するには、システム上で有効にする必要があります。 管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。 **機能管理** ワークスペースで、この機能は次のようにリストされています:

- **モジュール:** *倉庫管理*
- **機能名:** *移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする*

この機能が使用可能になったときに機能を管理するには、次の手順を実行します。

1. **倉庫管理 \> 設定 \> 倉庫管理パラメーター**の順に移動します。
1. **一般** タブの **ライセンス プレート** クイックタブで、**流通倉庫ライセンス プレート ポリシー** フィールドを次のいずれかの値に設定します:

    - **追跡されていないライセンス プレート再利用の許可** – システムは、*移動オーダー出荷済ライセンス プレートを出荷先倉庫以外の倉庫で使用されないようにする* 機能が使用できない場合と同じように機能します。 この値は、初めて機能をアクティブにしたときの既定の設定です。
    - **追跡されていないライセンス プレートの再利用防止** – 移動オーダーを受領するまで、出荷したライセンス プレートに関連する手動更新のみが出荷先倉庫で許可されます。

## <a name="more-information"></a>詳細

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

モバイル デバイス メニュー項目の詳細については、[倉庫作業用のモバイル デバイスの設定](configure-mobile-devices-warehouse.md) を参照してください。
