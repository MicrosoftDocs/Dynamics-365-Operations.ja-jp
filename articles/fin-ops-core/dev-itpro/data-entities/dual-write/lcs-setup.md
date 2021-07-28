---
title: Lifecycle Services からの二重書き込みの設定
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS). からデュアル書き込み接続を設定する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e604e1491bbafa041fa3f52ad0f8b454c63d47de
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359366"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services からの二重書き込みの設定

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、 Microsoft Dynamics Lifecycle Services (LCS)から二重書き込みを有効にする方法について説明します。

## <a name="prerequisites"></a>必要条件

Power Platform の統合を完了する必要があります。次のトピックを参照ください:

+ [Power Platform 統合: 環境のデプロイ中に有効にします](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform 統合 - 環境のデプロイ後に設定します](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>新しい Dataverse 環境で使用する二重書き込みの設定

以下の手順で、LCS  **環境の詳細** ページから二重書き込みを設定します:

1. **環境の詳細** ページで、**Power Platform の統合** セクションを展開します。

2. **二重書き込みアプリケーション** ボタンを選択します。

    ![Power Platform 統合。](media/powerplat_integration_step2.png)

3. 条件を確認して、**構成** を選択します。

4. 続行するには **OK** を選択してください。

5. 環境の詳細ページを定期的に更新することで、進捗状況を監視できます。 通常、所要時間は 30 分以下です。  

6. 設定が完了すると、プロセスが正常に完了した場合、または失敗した場合にメッセージが表示されます。 設定に失敗した場合は、関連するエラー メッセージが表示されます。 エラーがある場合は、修正をしないと次の手順に進めません。

7. **Power Platform 環境へのリンク** を選択して、Dataverse と現在の環境のデータベースとのリンクを作成します。 通常、所要時間は 5 分以下です。

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Power Platform 環境へのリンク。":::

8. リンクが完了すると、ハイパーリンクが表示されます。 このリンクを使用して、Finance and Operations 環境内の二重書き込み管理領域にログインします。 そこから、エンティティ マッピングを設定します。

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>既存の Dataverse 環境で使用する二重書き込みの設定

既存の Dataverse 環境に対して二重書き込みを設定するには、Microsoft の [サポート チケット](../../lifecycle-services/lcs-support.md) を作成する必要があります。 このチケットには次の情報が必要となります:

+ ご利用の Finance and Operations 環境の ID。
+ Lifecycle Services から環境名を入力します。
+ Dataverse 管理センターの組織 ID、または Power Platform 管理センターの Power Platform環境 ID。 チケットの中で、ID が Power Platform 統合で使用するインスタンスであることを要求してください。

> [!NOTE]
> LCS を使用して環境のリンクを解除することはできません。 環境のリンクを解除するには、Finance and Operations 環境の **データ統合** ワークスペースを開き、**リンク解除** を選択します。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
