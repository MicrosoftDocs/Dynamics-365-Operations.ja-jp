---
title: サービス レベルと説明
description: このトピックでは、資産管理のサービス レベルと説明について説明します。
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bb56e5103bd9e18e88c164cd308e55d48e64823
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019382"
---
# <a name="service-level-and-description"></a>サービス レベルと説明

[!include [banner](../../includes/banner.md)]

 

ワーク オーダーを作成するときに、そのサービス レベルを定義し、そのサービス レベルに一般的な説明を追加することができます。 **ワーク オーダー サービス レベル** のページでワーク オーダー サービス レベルを作成し、**ワーク オーダーの説明** のページで説明を作成することができます。

## <a name="create-a-service-level"></a>サービス レベルの作成

1. **資産管理** \> **設定** \> **ワーク オーダー** \> **サービス レベル** を選択します。
2. **新規** を選択します。
3. **サービス レベル** フィールドに、サービス レベル (番号など) を入力します。
4. **名前** フィールドに、名前を入力します。

    **ワーク オーダー** クイック タブでは、開始予定日時と終了予定日時を定義できます。 このファスト タブのフィールドは、ワーク オーダーを開始および終了する期間を定義します。 これらは、手動で作成されたワーク オーダーや、メンテナンス要求に基づいて作成されたワーク オーダーに使用されます。 

5. **開始日** のフィールドに日数を入力して、ワーク オーダーを開始する期間を定義します。 日数は、ワーク オーダーの作成日から計算されます。 たとえば、作成時にワーク オーダーを開始する場合は、**0** を入力します。 ワーク オーダーが作成されてから 1 週間以内に開始する場合は、**7** を入力します。
6. 開始日に加えてワーク オーダーに開始時刻を設定するには、**開始時刻の設定** オプションを **はい** に設定します。 次に、**開始時刻** フィールドに開始時刻を入力します。 このオプションを **いいえ** に設定した場合は、現在の時刻が使用されます。
7. **終了日** のフィールドに日数を入力して、ワーク オーダーを終了する期間を定義します。 日数は、ワーク オーダーの開始日から計算されます。 たとえば、開始日から 1 週間以内にワーク オーダーを終了する場合は **7** と入力します。
8. 終了日に加えてワーク オーダーに終了時刻を設定するには、**終了時刻の設定** オプションを **はい** に設定します。 次に、**終了時刻** フィールドに終了時刻を入力します。 このオプションを **いいえ** に設定した場合は、現在の時刻が使用されます。
9. **保存** を選択します。

![作業指示書サービス レベル ページ](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>説明の作成

1. **資産管理** \> **設定** \> **ワーク オーダー** \> **説明** を選択します。
2. **新規** を選択します。
3. **説明** フィールドに説明を入力します。
4. **保存** を選択します。
