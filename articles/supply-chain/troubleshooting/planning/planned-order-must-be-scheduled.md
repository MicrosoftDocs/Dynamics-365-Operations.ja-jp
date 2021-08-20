---
title: 計画製造オーダーは、確定する前にスケジュールする必要があります
description: 計画オーダーを確定しようとする場合、オーダーは確定する前にスケジュールする必要があるというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a89f5f98895be5b934dbdc1194fa58b9af34f9cbc7f5e2092f6f47791dd52400
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777746"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>計画製造オーダーは、確定する前にスケジュールする必要があります

エラーコード: SYS309802

## <a name="symptoms"></a>現象

計画オーダーを確定しようとする際に、次のエラー メッセージが表示されます:

> 計画製造オーダーは、スケジュールが済んでからでないと、確定できません。

## <a name="cause"></a>原因

スケジュールされた開始日と終了日を空白にすることはできません。

## <a name="resolution"></a>解決策

計画オーダーの開始日と終了日を指定するには、次の手順を実行します。

1. **マスター プラン \> マスタープラン \> 計画オーダー** の順に移動します。
1. 関連する計画オーダーを開きます。
1. **一般** クイック タブの、**スケジュール済** セクションで、**開始日** および **終了日** フィールドに日付を指定します。
