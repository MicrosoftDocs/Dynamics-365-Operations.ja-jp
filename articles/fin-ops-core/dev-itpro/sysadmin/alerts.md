---
title: 警告の設定
description: ここでは、バッチ ジョブの警告を設定する方法について説明します。
author: hasaid
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: c338e0d03bf848a19b17160c970b3f4f48bf86f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745109"
---
# <a name="set-up-alerts"></a>警告の設定

[!include [banner](../includes/banner.md)]

Finance and Operations の重大なイベントの通知システムは、警告によって形成されます。 警告を使用することで、作業日に追跡したいイベントに関する情報を常に受け取ることができます。 警告ルールの組み合わせを設定できます。そうすることでバッチ ジョブの終了時にエラーが発生した場合、またはキャンセルされた場合に警告を表示させることができます。 警告を電子メールで送信するか、アクション センターに通知として表示するかどうかを選択することができます。 警告はバッチ ジョブおよびユーザーごとに設定が可能です。

## <a name="set-up-alerts-for-batch-enhanced-forms"></a>バッチ ジョブの警告の設定

この手順では、バッチ化されたフォームに表示される警告を設定します。

1. **システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。
2. 一覧から バッチ ジョブ を選択し、次に アクション ウィンドウ で **警告** を選択します。
3. **バッチ ジョブの警告** ダイアログ ボックスでは、警告の内容を設定し、 **OK** します。

    ![警告の設定](./media/Batch-alert-configure.png) 

4. 警告の通知については [アクション センター] を確認してください。

    ![警告の通知](./media/Batch-alert-notification.png)

## <a name="set-up-alerts-for-batch-legacy-forms"></a>旧方式によるバッチ ジョブ 警告の設定

この手順では、従来のバッチ化されたフォームに表示される警告を設定します。

1. **システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。
2. 一覧から バッチ ジョブ を選択し、次に アクション ウィンドウ 内の **バッチジョブ** タブ で **警告** を選択します。

    ![旧方式の警告](./media/Batch-alert-legacy.png) 

3. **バッチ ジョブの警告** ダイアログ ボックスでは、警告の内容を設定し、 **OK** します。

> [!NOTE] 
> 電子メールで通知を受信するには、 **バッチ ジョブの警告** ダイアログ ボックスで、 **電子メール** のオプションを **はい** に設定します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]