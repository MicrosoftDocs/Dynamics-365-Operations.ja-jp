---
title: Lifecycle Services (LCS) ユーザー ガイド
description: この記事では、Lifecycle Services で使用できるツールと、作業段階を進めていく際に使用するツールについて説明します。
author: angelmarshall
ms.date: 07/02/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 6034
ms.assetid: 3bebecd6-a72e-48b2-9eec-8c19eafe5dad
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b584c91f49ae944f871bb0199a06d103a514a835
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103351"
---
# <a name="lifecycle-services-lcs-user-guide"></a>Lifecycle Services (LCS) ユーザー ガイド

[!include [banner](../includes/banner.md)]

Microsoft DynamicsLifecycle Services (LCS) は、定期的に更新されるサービスを提供します。 LCS の目標は、適切な情報を適切なタイミングで適切な相手に伝えることであり、実装、更新、アップグレードを毎回問題なく実行する反復性と予測可能性を実現することです。 LCS は顧客やパートナーがサポート計画の一部として使用できます。 Dynamics 365 財務と運用アプリの最新バージョンの顧客である場合は、Microsoft Azure Active Directory (Azure AD) 資格情報を使用してサインインできます。 [LCS に移動](https://lcs.dynamics.com/Logon/Index).

## <a name="tools-that-are-provided-in-lcs"></a>LCS で提供されるツール
次のテーブルでは、LCS で提供されるツールのリストと各ツールが適用されるフェーズについて説明しています。

| 工具                                     | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [プロジェクト](/dynamicsax-2012/appuser-itpro/projects-lifecycle-services-lcs)                                 | プロジェクトは、LCS でのエクスペリエンスの主な開催者です。 プロジェクトでは、共同作業するパートナーを招待し、進捗状況を追跡することもできます。                                                                                                                                                                                                                                                                                                                                                   |
| [方法](/dynamicsax-2012/appuser-itpro/methodologies-lifecycle-services-lcs)                            | 方法では、さらなる反復可能で予測可能な実装プロジェクトを保証するために使用できるツールが提供されます。 いずれかの既成の方法を使用するか、自分の方法を作成することができます。 方法を使用することで、進捗状況を容易に追跡およびレポートすることができます。                                                                                                                                                                                                                                                                  |
| [ビジネス プロセス モデラー](/dynamicsax-2012/appuser-itpro/business-process-modeler-lcs)                 | ビジネス プロセス モデラーにより標準プロセス フローを作成、表示、および変更することができます。 ビジネス プロセス モデラーを使用することにより、次の目標を達成することができます。プロセス フローを標準化します。アメリカ生産性品質センター (APQC) によって説明されているように、業務プロセスを業界標準プロセスに合わせることができます。ユーザー要件と Microsoft Dynamics 製品が提供する既定の機能との間の適合性とギャップを識別します。                                                                 |
| [クラウド ホスト環境](/dynamicsax-2012/appuser-itpro/cloud-hosted-environments-lifecycle-services-lcs)                | クラウド ホスト環境は、 Azure上に Microsoft Dynamics 環境を配置することができるツールです。 クラウドでホストされた環境を使用するとき、デモ、開発者/テスト、運用環境などの配置する環境タイプを選択する必要があります。 この選択に基づいて、クラウド ホスト環境ツールは Azure の仮想マシン (VM) の適切な番号を提供します。 これらの VM には、Microsoft Dynamics コンポーネント (およびすべての前提条件) がすでにインストールされています。                                       |
| [クラウドを利用したサポート](cloud-powered-support-lcs.md)                    | クラウドを利用したサポートでは、サポート インシデントを管理できます。 これにより、ローカル環境と同じ修正プログラムがインストールされた Azure に VM を作成できます。 VM 上でインシデントを再生成して記録し、インシデントをサポート チームに送信することができます。 サポートは調査し、可能な場合は VM 上で修正をテストし、検証のためにユーザーに修正プログラムを返送します。                                                                                                              |
| [コンフィギュレーションとデータ マネージャー (プレビュー)](configuration-manager-lcs.md) | 設定およびデータマネージャ (プレビュー) を使用すると、コンフィギュレーションをあるインスタンスから別のインスタンスにコピーできます。 以下の条件を満たす環境から、および環境に対してコピーすることができます: LCS プロジェクトの一部として管理される。データのインポート/エクスポート フレームワークを実行する。                                                                                                                                                                                                                                               |
| [カスタマイズ分析](/dynamicsax-2012/appuser-itpro/customization-analysis-lcs)                   | カスタマイズ分析は、ベスト プラクティスに対してモデル ファイルを検証し、改善の可能性のある領域のレポートを提供します。                                                                                                                                                                                                                                             |
| [問題検索](issue-search-lcs.md)                             | 問題検索で、Microsoft Dynamics 製品の既知の問題に関する既存のソリューションと回避策を検索できます。 どの問題が修正、未修正、または非対応として解決されたかを確認することができます。                                            |
| [資産ライブラリ](asset-library.md)                             | アセット ライブラリは、 LCS のテナントに関連付けられているさまざまな資産の保管場所です。                                                                                                                                                                      |
| [更新プログラムの入手](../migration-upgrade/download-hotfix-lcs.md)                            | 更新プログラムの入手とは、顧客が環境で利用可能なアップデートにアクセスするためのツールです。                            |
| [環境の監視](monitoring-diagnostics.md)                            | 環境監視は、管理対象となる環境状態の監視、診断および分析に役立つツールです。                                               |
| [Translation Service](translation-service-overview.md)                      | Microsoft Dynamics 365 Translation Service (DTS) は、 LCS にてホストされています。 パートナーおよび独立系ソフトウェア ベンダー (ISV) がソリューションを翻訳、または新たな言語を対応しているDynamics製品に追加する際の効率向上を図るために設計されています。                                                                  |
| [規制の更新](../lcs-solutions/regulatory-watch-communication.md)                      | 規制の更新は、お客様、パートナー、ISV ソリューション プロバイダがLCSを使用してアラートを設定することにより、規制の更新に関する最新情報を入手できるようにするツールです。                                        |
| [システム診断](/dynamicsax-2012/appuser-itpro/system-diagnostics-lifecycle-services-lcs)                       | システム診断は、 AX 2012環境を管理者が監視するにあったって役立つツールです。                                                                                                                                                                                                                                                                                      |
| [更新プログラム](/dynamicsax-2012/appuser-itpro/updates-for-microsoft-dynamics-ax-2012-r3-lifecycle-services-lcs)                                  | **更新** ページは、 AX 2012環境で使用可能な更新プログラムの詳細をホストします。 また、スリップストリームのインストールに使用できる更新のグループにアクセスできます。                                                                                                                                                                                                                                                                                                                               |
| [アップグレード分析](/dynamicsax-2012/appuser-itpro/upgrade-analysis-lifecycle-services-lcs)                         | アップグレード分析は、Microsoft Dynamics AX 4.0、Microsoft Dynamics AX 2009、または AX 2012 からコード アーティファクトを分析して、最新バージョンに更新する計画に役立ちます。                                                                                                                                                                                                                                                                                                    |
| [使用状況プロファイラー](/dynamicsax-2012/appuser-itpro/usage-profiler-lifecycle-services-lcs)                           | 使用状況プロファイラーは、予想される使用状況、または現在の使用状況を説明するのに役立つデータ収集ツールです。 生成された使用プロファイルは、ハードウェアのサイズ変更やサポートなど、さまざまな目的で使用できます。                                                                                                                                                                                                                                                                                                 |
| [ダウンロード可能なツール](/dynamicsax-2012/appuser-itpro/lifecycle-services-downloadable-tools-formerly-on-informationsource)                       | **ダウンロード可能なツール** ページは、 Microsoft Dynamics InformationSource にホストされていたツールを提供します。                                      |
| [ライセンス数見積もりツール](/dynamicsax-2012/appuser-itpro/license-sizing-estimator-lcs)                 | ライセンス数見積もりツールは、必要なライセンスの数を予測するのに役立ちます。 これは、既定またはカスタマイズされたロールをモデル化して、必要なクライアント アクセス ライセンス (CAL) を自動的に計算できる共有ワークスペースを提供します。

## <a name="additional-resources"></a>追加リソース

LCS チームは、 [Lifecycle Services エンジニアリング ブログ](https://cloudblogs.microsoft.com/dynamics365/?s=lcs) にも記事を執筆しています。 投稿やお知らせの最新情報を入手するため、RSS フィードを購読します。

[Lifecycle Servicesにアクセスする](https://lcs.dynamics.com/)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
