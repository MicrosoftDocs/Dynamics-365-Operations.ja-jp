---
title: ドキュメント回覧エージェントの更新
description: この記事では、Document Routing Agent を更新する方法について説明します。
author: RichdiMSFT
ms.date: 07/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b91ac00881b09ffbce15319bac091cc2c1cd409
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206641"
---
# <a name="update-the-document-routing-agent"></a>ドキュメント回覧エージェントの更新

[!include[banner](../includes/banner.md)]

印刷ジョブ キューを管理するソリューションは、顧客が大容量印刷の要件を満たすために Dynamics 365 財務と運用アプリを適切に拡張できるように設計されています。 印刷ジョブの管理に使用されるパブリック サービス エンドポイントは下位互換性がありますが、顧客が **すべて** の既存のドキュメント回覧エージェント (Document Routing Agent: DRA) クライアントを更新することを強くお勧めします。

DRA の既存のインストールを最新バージョンに更新しないと、次のような問題が発生する可能性があります:

- アプリケーションで監視可能なパフォーマンスの低下
- 孤立した印刷ジョブに関連する文書の消失
- カスタムの余白がある印刷ドキュメントの一貫性のない処理

IT 管理者は、DRA をホストするために使用される各ドメイン リソースに対して、次の手順を実行する必要があります。

> [!NOTE]
> DRA 更新プログラムを完了すると、IT 管理者は、ホストサーバー経由で接続しているすべてのプリンターを登録する必要があります。 ネットワーク パスによって識別されるネットワーク プリンターでは、パスが変更されていない限りは更新の必要はありません。

## <a name="get-started"></a>はじめに
DRA を Microsoft Windows サービスとして引き続き実行するには、サービスを実行するために使用されるドメイン アカウントのユーザー名とパスワードの両方が必要です。 この情報は、更新プログラム完了後に使用可能になっている必要があります。 有効なサービス アカウントの情報を検索するには、Microsoft 管理コンソール (MMC) サービス スナップインを起動し、一覧から **Microsoft Dynamics 365 ドキュメント回覧サービス** を選択します。

![マネージャー スナップイン。](media/Services_dialog.png)

## <a name="uninstall-an-existing-document-routing-agent"></a>既存のドキュメント回覧エージェントのアンインストール
**プログラムと機能** を開き、**Microsoft Dynamics 365 Finance: ドキュメント回覧** を検索し、削除します。

![プログラム ウィンドウをアンインストールまたは変更します。](media/Programs_and_Features_dialog.png)

アンインストールのプロセス中に、Microsoft Dynamics 365 ドキュメント回覧サービス アプリケーションを終了するメッセージが表示された場合は、**セットアップが完了したら、アプリケーションを自動的に閉じて再起動します。** を選択します。

![アプリケーションの終了を促すダイアログ ボックス。](media/Uninstall_DRA_services.png)

## <a name="install-the-latest-document-routing-agent"></a>最新のドキュメント回覧エージェントのインストール
サブスクリプションで使用可能な最新の DRA をインストールする方法の詳細については、[ネットワーク プリンター デバイスを有効にするためにドキュメント回覧エージェントをインストールする](install-document-routing-agent.md) を参照してください。

> [!NOTE]
> アップグレード後に DRA クライアントを開いて、ネットワーク ユーザーの資格情報を更新してください。

## <a name="best-practices"></a>ベスト プラクティス
Document Routing Agent に固有のサポート チームを作成する場合、Document Routing Agent コンピューターから問題が発生した時点のイベントを含むイベント ログをエクスポートすることを検討します。 

既定のイベント ログ サイズは1 MB だけであるため、パフォーマンスの問題などの問題が断続的な場合は、イベント ログ サイズを増やすことを検討してください。 イベント ログをエクスポートするまでしばらく待機します。

- \\Applications and Services Logs\Microsoft\Dynamics\Ax-DocumentRouting\Operational
- \\Applications and Services Logs\Microsoft\Dynamics\Ax-DocumentRouting\Admin

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
