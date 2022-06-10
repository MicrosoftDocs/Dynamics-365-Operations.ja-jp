---
title: Lifecycle Services からの二重書き込みの設定
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS). からデュアル書き込み接続を設定する方法について説明します。
author: laneswenka
ms.date: 05/16/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 53e82fbf8cff834c9eb0d14a0597561158b85fa1
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783204"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Lifecycle Services からの二重書き込みの設定

[!include [banner](../../includes/banner.md)]



このトピックでは、 Microsoft Dynamics Lifecycle Services (LCS)から二重書き込みを有効にする方法について説明します。

## <a name="prerequisites"></a>必要条件

次のトピックで説明するように、顧客は Power Platform の統合を完了する必要があります。

- まだ Microsoft Power Platform を使用しておらず、プラットフォーム機能を追加して財務および運用の環境を拡張する場合は、[Power Platform 統合 - 環境の展開中に有効化する](../../power-platform/enable-power-platform-integration.md#enable-during-deploy) を参照してください。
- すでに Dataverse と Power Platform 環境が存在し、それらを財務および運用の環境に接続する場合は、[Power Platform 統合 - 環境の展開後に有効化する](../../power-platform/enable-power-platform-integration.md#enable-after-deploy) を参照してください。

## <a name="set-up-dual-write-for-new-or-existing-dataverse-environments"></a>新規または既存の Dataverse 環境で二重書き込みを設定する

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

## <a name="linking-mismatch"></a>リンクの不一致

LCS を Power Platform 統合に設定していない場合は、二重書き込み環境を Dataverse インスタンスにリンクしている可能性があります。 このリンクの不一致は予期しない動作の原因になる可能性があります。 ビジネス イベント、仮想テーブル、アドインで同じ接続を使用できるように、LCS 環境の詳細を二重書き込みの接続先と一致させることを推奨します。

現在の環境にリンクの不一致がある場合、LCS は、環境の詳細ページに次の例のような警告を表示します: "Microsoft は、Power Platform 統合で指定した宛先に、環境を二重書き込みを介してリンクしていることを検出しました。これは非推奨です。"

:::image type="content" source="media/powerplat_integration_mismatchLink.png" alt-text="Power Platform 統合のリンクの不一致。":::

この警告が表示される場合は、次のいずれかの解決策を試してください。

- これまで LCS 環境を Power Platform 統合に一度も設定していない場合は、この記事の手順に従って二重書き込みで設定した Dataverse インスタンスに接続できます。
- LCS 環境をすでに Power Platform 統合に設定している場合は、二重書き込みのリンクを解除し、[シナリオ: リンクのリセットまたは変更](relink-environments.md#scenario-reset-or-change-linking) によって LCS で指定した宛先に再接続する必要があります。

以前はサポート チケットの手動オプションを利用できましたが、それは上記のオプション 1 が存在する前でした。  Microsoft は現在、サポート チケットによる手動再リンク要求に対応していません。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
