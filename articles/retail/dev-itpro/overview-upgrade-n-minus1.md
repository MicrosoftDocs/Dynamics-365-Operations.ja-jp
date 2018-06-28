---
title: "Dynamics 365 for Retail のアップグレードと N-1 サポートの概要"
description: "Dynamics 365 for Retail のリリースで、アップグレードと N-1 サポートが有効になりました。 N-1 のサポートによって、AX 2012 R3 CU10 を実行する店舗を持つ顧客は、アップグレード後に Dynamics 365 for Retail headquarters で作業できます。"
author: athinesh99
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics-365-retail
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.custom: 44351
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 4a062ccbca8e3b4503cf5e61f838b5ec0b4358e1
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="overview-of-upgrade-and-n-1-support-for-dynamics-365-for-retail"></a>Dynamics 365 for Retail のアップグレードと N-1 サポートの概要

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 for Retail の 7 月のリリースで、アップグレードと N-1 サポートが有効になりました。 N-1 のサポートによって、Microsoft Dynamics AX 2012 R3 累積更新プログラム 10 (CU10) を実行する店舗を持つ顧客は、アップグレード後に Microsoft Dynamics 365 for Retail headquarters で作業できます。 アップグレードと N-1 サポートの主な目的は、AX 2012 R3 の顧客が Retail に移行してクラウドの利点を活用できるようにすることです。

次の機能を使用すると、顧客はシームレスにアップグレードできます。

- アップグレード プロセスを通じて、AX 2012 R3 から小売用バックオフィスへのデータベース アップグレードを実行できるようになりました。
- AX 2012 R3 CU10 のコンポーネントを使用して店舗を運営することができます。
- アップグレード前とアップグレード後のチェックリストの検証は、アップグレード プロセスに組み込まれています。
- アップグレード プロセスでは、エラー処理とメッセージングが強化されているため、顧客は問題を迅速にデバッグできます。
- ユーザーは、ツールを使用して、既存の小売用バック オフィスのカスタムの X++ コードを、そのバック オフィスのアップグレードされたバージョンに移行することができます。

アップグレード手順は、Retail を最新バージョンにアップグレードする手順とほぼ同じです。 一般にアップグレードに関する詳細については、[アップグレードの概要: AX 2012 を Dynamics 365 for Retail へ](../../dev-itpro/migration-upgrade/upgrade-overview-2012.md) を参照してください。

計画的なダウンタイムが必要です。 アップグレード分析を最初に行います。 アップグレード分析は、Microsoft Dynamics AX 2012 データベースに対して実行され、Microsoft Dynamics Lifecycle Services (LCS) 診断サービスに基づいています。 このステップでは、アップグレードをより迅速かつ低コストで行うための作業を特定します。 また、必要な SQL 構成、データ バックオフィス クリーンアップ、推奨されない機能を識別します。
  
その後、実際のデータ アップグレード プロセスが発生します。 AX 2012 データベースは、Microsoft Azure SQL データベースに移動され、データ アップグレード パッケージは runbook プロセスを通じて通常どおり実行されます。 アップグレードの検証が完了します。 検証ツールは、使用される前にアップグレードされた環境に対して実行されます。 このツールは自動スモーク テストを実行して、サービスが動作してアクセス可能なこと、行数の一致、財務と在庫の調整などを検証します。
 
小売チャネルのアップグレード後構成のほとんどにおいて、手動での手順をほぼ必要としません。 顧客はアップグレード前およびアップグレード後のチェックリストを使用して、完了する必要があるタスクについて知ることができます。 アップグレード後のタスクには、アップグレードされたデータベースから店舗への完全な同期の開始、アップグレードされたデータベースに対するチャンネル、レジスター、およびデバイスの検証、トランザクションの同期の検証、N-1サポートが実施されていることの検証が含まれます。
 
N-1 サポートで、顧客は、小売用バックオフィスで N-1 パッケージをインストールする必要があります。 店舗では設定は必要ありません。 このインストールは、N-1 関連の構成の完了後、アップグレード ウィンドウで実行する必要があります。

小売用バックオフィスをアップグレードし、N-1 セットアップを完了した後、N-1 店舗のコンポーネントは、小売用バック オフィスと通信できます。 N-1 のサポートのためにインストールが必要なチャネル側コンポーネントはありません。 ただし、小売用バックオフィスと通信する N-1店舗を有効にし、レジ担当者は初めてサインインするそのパスワードを変更する必要があります。
 
N-1 インストールする手順については、[Microsoft Dynamics 365 for Retail で使用する N-1 コンポーネントをインストールする](n-1-installation-configuration.md) を参照してください。

