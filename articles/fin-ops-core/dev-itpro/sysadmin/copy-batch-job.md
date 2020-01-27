---
title: バッチ ジョブのコピー
description: このトピックでは、バッチ ジョブとバッチ タスクのコピーに関する情報を提供します。
author: Peakerbl
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-08-15
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: df3fa0a253399a0dff6527ef21e0d4e2a7663cf2
ms.sourcegitcommit: 65f4b8a751670a7fe9ef4cb8b218213f792d57a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945405"
---
# <a name="copy-a-batch-job"></a>バッチ ジョブのコピー

[!include [banner](../includes/banner.md)]

別の法人の同じジョブを作成する場合、コピー バッチ ジョブ機能を使用して、定期的なアイテムを含む既存のバッチ ジョブとバッチ タスクをコピーできます。

説明、会社、スケジュールの開始日および時間、繰り返し、およびアカウントごとの実行を同時に設定することができます。 バッチ ジョブをコピーするときに、元のジョブから警告と依存関係もコピーされます。 

>[!NOTE] 
>この機能は、Platform update 20 以降で利用できます。

## <a name="copy-a-batch-job"></a>バッチ ジョブのコピー
バッチ ジョブをコピーする次の手順を実行します。

1.  **システム管理** > **照会** > **バッチ ジョブ** をクリックします。
2.  コピーするジョブを選択し、アクション ペインで **バッチ ジョブ** > **バッチ ジョブのコピー** をクリックします。

![バッチ関数のコピー](./media/copy-batch-function.png) 
 
4.  変更を入力または追加します。 **タスクの表示** を **はい** に設定した場合、**OK** をクリックすると、コピーしたジョブの **バッチ タスク** ページに直接移動します。

![バッチ フォームのコピー](./media/copy-batch-form.png) 

>[!IMPORTANT] 
>コピーされたバッチ ジョブは、**保留** 状態で作成されるため、有効にする必要があります。 **実行者** ユーザーを設定することもできます。設定すると、そのユーザーは、システム管理者でなくてもジョブを実行する権限が付与されます。

## <a name="enable-the-batch-job"></a>バッチ ジョブの有効化
バッチ ジョブを有効にする次の手順を実行します。

1.  **バッチ ジョブ** ページのアクション ウィンドウで、**バッチ ジョブ** > **ステータスを変更** をクリックします。
2.  **待機中** 状態を選択して **OK** をクリックします。
