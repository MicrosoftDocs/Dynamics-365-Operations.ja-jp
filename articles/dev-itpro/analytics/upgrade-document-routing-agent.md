---
title: ドキュメント回覧エージェントのアップグレード
description: このトピックでは、ドキュメント巡回エージェントをアップグレードする方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 04/06/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96c09e7784a6e3111247466c4e933f0198936e78
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544323"
---
# <a name="upgrade-the-document-routing-agent"></a>ドキュメント回覧エージェントのアップグレード

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 12 には、ネットワーク印刷機能を提供するコンポーネントに対するいくつかの重要な拡張機能が含まれています。 たとえば、印刷ジョブ キューを管理するソリューションは、印刷ジョブの管理サービスが大量の印刷要件を満たすために調整されるよう再設計されました。 印刷ジョブの管理サービスには、市場バージョンのドキュメント回覧エージェント (DRA) クライアントと下位互換性のあるバージョンがありますが、顧客がオンプレミスでホストされている既存の DRA クライアントを**すべて**アップグレードすることを強くお勧めします。

DRA の既存のインストールをプラットフォーム更新プログラム 12 またはそれ以降のバージョンにアップグレードしない場合は、次の問題が発生する可能性があります。

- Finance and Operations アプリケーションの監視可能なパフォーマンス低下
- 孤立した印刷ジョブに関連する文書の消失
- カスタムの余白がある印刷ドキュメントの一貫性のない処理

IT 管理者は、Finance and Operations の DRA をホストするために使用される各ドメイン リソースに対して、次の手順を実行する必要があります。

## <a name="get-started"></a>使用開始
DRA を Microsoft Windows サービスとして引き続き実行するには、サービスを実行するために使用されるドメイン アカウントのユーザー名とパスワードの両方が必要です。 この情報は、アップグレード完了後に使用可能になっている必要があります。 有効なサービス アカウントの情報を検索するには、Microsoft 管理コンソール (MMC) サービス スナップインを起動し、一覧から **Microsoft Dynamics 365 ドキュメント回覧サービス**を選択します。

![マネージャー スナップイン](media/Services_dialog.png)

## <a name="uninstall-an-existing-document-routing-agent"></a>既存のドキュメント回覧エージェントのアンインストール
**プログラムと機能**を開き、**Microsoft Dynamics 365 for Finance and Operations: ドキュメント回覧**を検索し、削除します。

![プログラム ウィンドウのアンインストールまたは変更](media/Programs_and_Features_dialog.png)

アンインストールのプロセス中に、Microsoft Dynamics 365 ドキュメント回覧サービス アプリケーションを終了するメッセージが表示された場合は、**セットアップが完了したら、アプリケーションを自動的に閉じて再起動します。** を選択します。

![アプリケーションの終了を促すダイアログ ボックス](media/Uninstall_DRA_services.png)

## <a name="install-the-latest-document-routing-agent"></a>最新のドキュメント回覧エージェントのインストール
定期売買で使用可能な最新の DRA をインストールする方法の詳細については、[ネットワーク プリンター デバイスを有効にするためにドキュメント回覧エージェントをインストールする](install-document-routing-agent.md) を参照してください。
