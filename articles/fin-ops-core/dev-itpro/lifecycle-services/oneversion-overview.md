---
title: 1 つのバージョンのサービス更新の概要
description: このトピックでは、1 つのバージョンの一部として Microsoft によって開始されたサービスの更新を管理するための体験を構成する、さまざまな手順の概要を説明します。
author: angelmarshall
manager: AnnBe
ms.date: 05/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a00b7761c061a8ee31c05736c0d3f6ae6780de22
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117407"
---
# <a name="one-version-service-updates-overview"></a>1 つのバージョンのサービス更新の概要

[!include [banner](../includes/banner.md)]

次の一連のトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) 以降 のサービス更新に関連する情報を提供しています。 これはクラウド リリースにのみ適用されます。

- [サービス更新の可用性](../../fin-ops/get-started/public-preview-releases.md) – このトピックはリリース頻度およびリリース プロセスに関する情報を提供します。
- [ソフトウェアのライフサイクル ポリシーおよびクラウド リリース](../migration-upgrade/versions-update-policy.md) – このトピックはサービスの更新、可用性、およびサービス終了についての情報を提供します。
- [1 つのバージョンのサービス更新に関するよく寄せられる質問](../../fin-ops/get-started/one-version.md) – このトピックは更新プロセス、ツール、計画、および小売サービスの更新に関する質問に回答します。

サービス更新の経験は 4 つの異なるステップから構成されています: 

1. 構成
2. 通知
3. 更新
4. 検証

このトピックの残りでは各ステップについて説明し、関連トピックへのリンクを示します。

## <a name="configure"></a>構成

顧客はビジネスの制約に基づいて保守時間枠を選択できます。 Microsoft Dynamics Lifecycle Services (LCS) で、次の図に示すように **プロジェクト設定** ページの **設定の更新** タブで **実稼働環境の更新頻度** にあるフィールドを使用します。 今後の計画を立てるには次回の更新のカレンダーを利用できます。

[![プロジェクト設定ページの更新設定タブ](./media/UpdateSettings-ConfigureUpdates.JPG)](./media/UpdateSettings-ConfigureUpdates.JPG)

ユーザーは新機能をオプトインして有効にする必要があります。 すべての更新プログラムは最初にユーザー受け入れテスト (UAT) 環境に適用され、それから実稼働環境に適用されます。 したがって、顧客が必要な検証を行う時間があります。 顧客は更新される環境を選択できます。 最大で 3 か月まで更新プログラムを一時停止することもできます。

## <a name="notice"></a>通知

[リリース プラン](https://docs.microsoft.com/business-applications-release-notes/april19/dynamics365-finance-operations/) は、事前に計画を立て、変更点を理解するのに役立ちます。 最大で 3 か月前から次の新機能について学ぶことができます。 [新機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-changed) のトピックでは特定の月の更新プログラムに関する詳細を提供します。

さらに、通知電子メールが 5 日前に送信され、次の図に示すように更新の直前に通知が LCS に表示されます。

[![LCS の次回の更新プログラムの通知](./media/Notification-bar.png)](./media/Notification-bar.png)

## <a name="update"></a>更新

通知が送信された後、Microsoft は指定された保守時間枠で更新 (**自動更新**) を適用します。 この操作が完了した後、更新の状態を示す通知電子メールが送信されます。 LCS の標準的な更新エクスペリエンスを使用することで **自己更新** も可能になります。 詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md)を参照してください。 

初回リリース プログラムに参加している顧客は、サンドボックス環境およびその他の環境を早期に更新する機会があります。 初回リリース プログラムに登録するには [https://experience.dynamics.com](https://experience.dynamics.com) に移動します。

次の図に示すように、LCS の標準的な更新エクスペリエンスを使用することで **自己更新** も可能になります。

[![LCS の管理メニューで更新コマンドを適用する](./media/Self-Update-Execute.jpg)](./media/Self-Update-Execute.jpg)

## <a name="validate"></a>検証

UAT 環境で更新が完了したら、基本的なビジネス プロセス テストを実行して環境を検証できます。 次の図に示すように、この作業量をサポートするビジネス プロセス テスト用のコードなし自動化テスト ツールを利用できます。 詳細については、 [ユーザー受け入れテストの作成と自動化](using-task-guides-and-bpm-to-create-user-acceptance-tests.md) を参照してください。 

[![Regression Suite Automation Tool](./media/TestAutomation.png)](./media/TestAutomation.png)

一部の顧客は外部データ統合と内部データ統合の両方があります。 これらの顧客はテストに [データ タスクの自動化ツール](../data-entities/data-task-automation.md) を使用することをお勧めします。


