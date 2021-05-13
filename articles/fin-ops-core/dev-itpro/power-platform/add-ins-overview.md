---
title: アドインの概要
description: このトピックでは、Finance and Operations アプリの機能を拡張するために使用できるアドインに関する情報を提供します。
author: ankugo
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: ankugo
ms.search.validFrom: 2021-02-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 52dcf72609d29d62c3e044277b637526ead88039
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909018"
---
# <a name="add-ins-overview"></a>アドインの概要

[!include[banner](../includes/banner.md)]

アドインを使用すると、Finance and Operations アプリの機能を拡張できます。 次のトピックでは、アドインの例を示します:

- [計画最適化の概要](../../../supply-chain/master-planning/planning-optimization/planning-optimization-overview.md)
- [在庫の視覚化アドイン](../../../supply-chain/inventory/inventory-visibility.md)
- [Azure Data Lake へのエクスポートのコンフィギュレーション](../data-entities/configure-export-data-lake.md)
- [IoT インテリジェンスのホーム ページ](../../../supply-chain/iot/iot-intelligence-home-page.md)

## <a name="prerequisites-for-setting-up-add-ins"></a>アドインを設定するための前提条件

- Microsoft Dataverse 領域の少なくとも 1 ギガバイト (GB) を使用できます。 それ以外の場合、設定は失敗です。 [Power Platform管理センター](https://admin.powerplatform.microsoft.com/resources/capacity) にて、容量を表示できます。 
- Finance and Operations 環境管理者を識別します。 **環境の詳細** セクションにて、情報を確認できます。

    ![環境の詳細タブ](media/EnvironmentDetails.png)
    
- Power Platform 環境ガバナンス ポリシーを検証します。 検証するには、**グローバル管理者** または **Power Platform 管理者** である必要があります。
    
    1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にサイン インします。
    2. Power Platform サイトの右上端にあるギア アイコンを選択します。
    
        ![Power Platform の設定](media/PowerPlatformSettings.png)
    
- 組織では、運用環境に対して **全ユーザー** を選択する必要があります。
    
    Finance and Operations 環境管理者は、次のいずれかのロールに追加する必要があります。 このアクションを実行するには、グローバル管理者が必要です。
    - Global 管理者
    - Dynamics 365 管理者
    - Power Platform 管理者
    
    詳細については、[サービス管理者ロールを使用したテナントの管理](/power-platform/admin/use-service-admin-role-manage-tenant) を参照してください。

## <a name="set-up-add-ins"></a>アドインの設定

> [!NOTE]
> インストールを計画しているアドインに「デュアル書き込みリンク」が必要ない場合は、この手順を実行する必要があります。

1. Finance and Operations 環境が LCS を通じて展開された後、LCS の **環境詳細** ページが開きます。
2. **Power Platform 統合** セクションで、**設定** を選択します。
3. **Power Platform環境の設定** ダイアログ ボックスでチェック ボックスをオンにし、ダイアログ ボックスの下部にある **設定** を選択します。

    > [!NOTE]
    > Dataverse 環境は、デュアル書き込み機能を含む方法で設定されています。 通常この設定で消費される容量は、Dataverse 領域の 約 1 GB です。

4. Microsoft Power Platform 環境が準備されているというメッセージが表示された場合は、**OK** を選択します。

    **環境詳細** ページの **Power Platform 統合** セクションに、Microsoft Power Platform 環境が準備されているというメッセージが表示されます。

5. 数分後、**環境の詳細** ページが更新されます。
6. **Power Platform 統合** セクションにおいて、**ステータス** フィールドの値が **環境設定が進行中** であることに注意してください。

    通常、設定は 60分 から 90分かかります。

    Dataverse 環境が準備された後、**新しいアドインのインストール** ボタンが **Power Platform 統合** セクションで利用できます。

    ![新しいアドイン ボタンのインストール](media/InstallANewAddIn.png)

## <a name="troubleshoot-the-setup"></a>設定のトラブルシューティング

- 次の図に示すように、セットアップ プロセスによってデュアル書き込み機能の設定が試行される場合、Dataverse 環境の準備後にデュアル書き込み設定が失敗することがあります 。 このような場合は、**新しいアドインのインストール** ボタンを使用して、アドインのインストールのブロックを解除できます。デュアル書き込み機能を継続して設定する場合は、**経歴** を選択します。

    ![デュアル書き込みの失敗](media/Error.png)

- 能力やライセンスに関する問題が発生すると、Dataverse 環境の準備に失敗することがあります。 そのような場合は、Power Platform 管理センターにログインして問題を修正します。 次に LCS の **環境詳細** ページの **Power Platform 統合** セクションで、**経歴** を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]