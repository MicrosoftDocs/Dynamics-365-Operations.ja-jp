---
title: Lifecycle Services (LCS) ユーザー ガイド
description: このトピックでは、Lifecycle Services (LCS) で使用できるツールと、LCS で作業段階を進めていく際に使用するツールについて説明します。
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 6034
ms.assetid: 3bebecd6-a72e-48b2-9eec-8c19eafe5dad
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 94a95543300017a419ec328ac50e04925503a0cd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369160"
---
# <a name="lifecycle-services-lcs-user-guide"></a>Lifecycle Services (LCS) ユーザー ガイド

[!include [banner](../includes/banner.md)]

Lifecycle Services (LCS) は、定期的に更新されるサービスを提供します。 LCS の目標は、適切な情報を適切なタイミングで適切な相手に伝えることであり、実装、更新、アップグレードを毎回問題なく実行する反復性と予測可能性を実現することです。 LCS は顧客やパートナーがサポート計画の一部として使用できます。 Microsoft Dynamics AX 2012 ユーザーである場合、CustomerSource または PartnerSource の資格情報を使用してログインすることができます。 Finance and Operations の最新バージョンの顧客である場合は、Microsoft Azure Active Directory (Azure AD) 資格情報を使用してログインできます。 [LCS に移動](https://lcs.dynamics.com/Logon/Index).

## <a name="tools-that-are-provided-in-lcs"></a>LCS で提供されるツール
次のテーブルでは、LCS で提供されるツールのリストと各ツールが適用されるフェーズについて説明しています。

| 工具                                     | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [プロジェクト](ax-2012/projects-lcs.md)                                 | プロジェクトは、LCS でのエクスペリエンスの主な開催者です。 プロジェクトでは、共同作業するパートナーを招待し、進捗状況を追跡することもできます。                                                                                                                                                                                                                                                                                                                                                   |
| [方法](ax-2012/methodologies-lcs.md)                            | 方法では、さらなる反復可能で予測可能な実装プロジェクトを保証するために使用できるツールが提供されます。 いずれかの既成の方法を使用するか、自分の方法を作成することができます。 方法を使用することで、進捗状況を容易に追跡およびレポートすることができます。                                                                                                                                                                                                                                                                  |
| [ビジネス プロセス モデラー](ax-2012/business-process-modeler-lcs.md)                 | ビジネス プロセス モデラーにより標準プロセス フローを作成、表示、および変更することができます。 ビジネス プロセス モデラーを使用することにより、次の目標を達成することができます。プロセス フローを標準化します。アメリカ生産性品質センター (APQC) によって説明されているように、業務プロセスを業界標準プロセスに合わせることができます。ユーザー要件と Microsoft Dynamics 製品が提供する既定の機能との間の適合性とギャップを識別します。                                                                 |
| [クラウド ホスト環境](ax-2012/cloud-hosted-environments-lcs.md)                | クラウド ホスト環境は、Microsoft Azure 上に Microsoft Dynamics 環境を配置するツールです。 クラウドでホストされた環境を使用するとき、デモ、開発者/テスト、または実稼動環境などの、配置する環境のタイプを選択する必要があります。 この選択に基づいて、クラウド ホスト環境ツールは Azure の仮想マシン (VM) の適切な番号を提供します。 これらの VM には、Microsoft Dynamics コンポーネント (およびすべての前提条件) がすでにインストールされています。 |
| [クラウドを利用したサポート](cloud-powered-support-lcs.md)                    | クラウドを利用したサポートでは、サポート インシデントを管理できます。 これにより、ローカル環境と同じ修正プログラムがインストールされた Azure に VM を作成できます。 VM 上でインシデントを再生成して記録し、インシデントをサポート チームに送信することができます。 サポートは調査し、可能な場合は VM 上で修正をテストし、検証のためにユーザーに修正プログラムを返送します。                                                                                                              |
| [コンフィギュレーションとデータ マネージャー (プレビュー)](configuration-manager-lcs.md) | 設定およびデータマネージャ (プレビュー) を使用すると、コンフィギュレーションをあるインスタンスから別のインスタンスにコピーできます。 以下の条件を満たす環境から、および環境に対してコピーすることができます: LCS プロジェクトの一部として管理される。データのインポート/エクスポート フレームワークを実行する。                                                                                                                                                                                                                                               |
| [カスタマイズ分析](ax-2012/customization-analysis-lcs.md)                   | カスタマイズ分析は、ベスト プラクティスに対してモデル ファイルを検証し、改善の可能性のある領域のレポートを提供します。                                                                                                                                                                                                                                                                                                                                                                                     |
| [問題検索](issue-search-lcs.md)                             | 問題検索で、Microsoft Dynamics 製品の既知の問題に関する既存のソリューションと回避策を検索できます。 どの問題が修正され、どの問題が未修正で、どの問題が「修正しない」として解決されたか確認することができます。                                                                                                                                                                                                                                                                           |
| [ライセンス数見積もりツール](ax-2012/license-sizing-estimator-lcs.md)                 | ライセンス数見積もりツールは、必要なライセンスの数を予測するのに役立ちます。 これは、既定またはカスタマイズされたロールをモデル化して、必要なクライアント アクセス ライセンス (CAL) を自動的に計算できる共有ワークスペースを提供します。                                                                                                                                                                                                                                                               |
| [RFP 応答](ax-2012/rfp-responses-lcs.md)                            | RFP 応答 ページでは、パートナーが提案依頼 (RFP) に応答することができます。                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [システム診断](ax-2012/system-diagnostics-lcs.md)                       | システム診断は、Microsoft Dynamics 環境を管理者が監視するのに役立ちます。                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [更新](ax-2012/update-2012-r3-lcs.md)                                  | 更新のページは、環境で使用可能な更新プログラムの詳細をホストします。 また、スリップストリームのインストールに使用できる更新のグループにアクセスできます。                                                                                                                                                                                                                                                                                                                               |
| [アップグレード分析](ax-2012/upgrade-analysis-lcs.md)                         | アップグレード分析は、Microsoft Dynamics AX 4.0、Dynamics AX 2009、または Dynamics AX 2012 のコード アーティファクトを分析することにより、Microsoft Dynamics 365 for Finance and Operations の最新バージョンへのアップグレードを計画するのに役立ちます。                                                                                                                                                                                                                                                                                                    |
| [使用状況プロファイラー](ax-2012/usage-profiler-lcs.md)                           | 使用状況プロファイラーは、予想される使用状況、または現在の使用状況を説明するのに役立つデータ収集ツールです。 生成された使用プロファイルは、ハードウェアのサイズ変更やサポートなど、さまざまな目的で使用できます。                                                                                                                                                                                                                                                                                                 |
| [ダウンロード可能なツール](ax-2012/lcs-downloadable-tools-formerly-informationsource.md)                       | ダウンロード可能なツール ページは、Microsoft Dynamics InformationSource にホストされていた一連のツールを提供します。                                                                                                                                                                                                                                                                                                                                                                                          |

LCS チームは、[Lifecycle Services エンジニアリング ブログ](https://blogs.msdn.microsoft.com/lcs/)にも記事を執筆しています。 投稿やお知らせの最新情報を入手するため、RSS フィードを購読します。

<a name="additional-resources"></a>その他のリソース
--------

[Lifecycle Services](https://lcs.dynamics.com/)



