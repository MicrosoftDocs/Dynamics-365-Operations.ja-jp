---
title: データ統合のトラブルシューティング ガイド
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations と Common Data Service 間のデータ統合に関するトラブルシューティングの情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797278"
---
# <a name="troubleshooting-guide-for-data-integration"></a>データ統合のトラブルシューティング ガイド

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Common Data Service のプラグイン トレースを有効にし、デュアル書き込みプラグイン エラーの詳細を確認

デュアル書き込み同期で問題またはエラーが発生した場合は、トレース ログでエラーを検査できます。

1. エラーを検査する前に、[プラグインと登録](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) の指示に従い、プラグイン トレースを有効にする必要があります。 これで、エラーを検査できます。
2. Dynamics 365 for Sales にログインします。
3. 設定アイコン (ギア) をクリックし、**詳細設定**を選びます。
4. **設定**メニューで、**カスタマイズ > プラグイン トレース ログ**を選択します。
5. タイプ名 **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** をクリックして、エラー詳細を表示します。

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>Finance and Operations のデュアル書き込み同期エラーを確認

テスト中にエラーを確認するには、次の手順を実行します。

+ LifeCycle Services (LCS) にログインします。
+ デュアル書き込みテストを実行するために、選択した LCS プロジェクトを開きます。
+ クラウド ホスト環境に移動します。
+ LCS に表示されるローカル アカウントを使用して、Finance and Operations VM にデスクトップをリモートします。
+ イベント ビューアーを開きます。 
+ **アプリケーションとサービス ログ > Microsoft > Dynamics > AX-DualWriteSync > オペレーション**へ移動します。 エラーと詳細が表示されます。

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Finance and Operations から、別の Common Data Service 環境をリンクおよび解除の方法

リンクを更新する場合は、次の手順を実行します。

+ Finance and Operations 環境に移動します。
+ データ管理を開きます。
+ **アプリの CDS にリンク**をクリックします。
+ 実行中のすべてのマッピングを選択し、**停止**をクリックします。 
+ 実行中のすべてのマッピングを選択し、**削除**をクリックします。

    > [!NOTE]
    > **CustomerV3-Account** テンプレートが選択されている場合、**削除**オプションは表示されません。 必要に応じて、選択を解除します。 **CustomerV3-Account** は古いプロビジョニングされたテンプレートであり、見込み客から現金化ソリューションで動作します。 グローバルにリリースされているため、すべてのテンプレートの下に表示されます。

+ **リンク解除の環境**をクリックします。
+ **はい**をクリックし、確認します。
+ 新しい環境をリンクするには、[インストール ガイド](https://aka.ms/dualwrite-docs) の手順に従います。

