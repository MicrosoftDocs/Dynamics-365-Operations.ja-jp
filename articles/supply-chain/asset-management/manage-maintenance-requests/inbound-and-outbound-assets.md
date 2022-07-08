---
title: 入庫および出庫資産
description: この記事では、資産管理で入庫および出庫資産を登録する方法について説明します。
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016539"
---
# <a name="inbound-and-outbound-assets"></a>入庫および出庫資産

[!include [banner](../../includes/banner.md)]

 

会社が他の場所または顧客から受け取った資産の修復作業またはメンテナンス作業をする場合、資産管理は、会社に向かう途中の入庫資産と返される出庫資産の両方を追跡できます。

> [!NOTE]
> 入庫および出庫のライフサイクル状態を使用して、入庫および出庫される資産を管理する場合は、これらのアクションをサポートするライフスタイル モデルを設定する必要があります。 詳細については、[メンテナンス要求](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview) を参照してください。

資産管理の設定によって、入庫資産と出庫資産を操作できるかどうかが決まります。

## <a name="register-assets-as-inbound"></a>資産を入庫として登録する

1. **資産管理** \> **メンテナンス要求** \> **有効なメンテナンス要求** を選択します。
2. メンテナンス要求を選択します。
3. **メンテナンス要求の状態の更新** を選択します。
4. **入庫** (または入庫資産用に作成した別のライフサイクル状態) を選択し、**OK** を選択します。

![資産を入庫として登録する。](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>入庫資産を入庫済として登録する

1. **資産管理** \> **入庫/出庫** \> **入庫資産** を選択します。
2. 資産またはメンテナンス要求を選択します。
3. **資産の受入** を選択します。
4. **受入済** フィールドで、日時を入力します。 その後、**OK** を選択します。 レコードは、**入庫資産** リスト ページから削除されます。

![入庫資産を入庫済として登録する。](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>資産を出庫として登録する

メンテナンス作業または修理作業が完了したら、資産を返却済として登録できます。

1. **資産管理** \> **メンテナンス要求** \> **有効なメンテナンス要求** を選択します。
2. メンテナンス要求を選択します。
3. **メンテナンス要求の状態の更新** を選択します。
4. **出庫** (または出庫資産用に作成した別のライフサイクル状態) を選択し、**OK** を選択します。

## <a name="register-outbound-assets-as-delivered"></a>出庫資産を配送済として登録する

1. **資産管理** \> **入庫/出庫** \> **出庫資産** を選択します。
2. 資産またはメンテナンス要求を選択します。
3. **資産を配送** を選択します。
4. **配送済** フィールドで、日時を入力します。 その後、**OK** を選択します。 レコードは、**出庫資産** リスト ページから削除されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]