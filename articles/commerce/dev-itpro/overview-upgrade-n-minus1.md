---
title: Commerce のアップグレードおよび N-1 のサポート
description: Dynamics 365 Commerce のリリースで、アップグレードと N-1 サポートが有効になりました。
author: josaw1
ms.date: 11/14/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Retail July 2017 update
ms.custom: 44351,  ""intro-internal
ms.openlocfilehash: bc065f90a7e2c817c44fa83cc17884987b0a8eaf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276218"
---
# <a name="upgrade-and-n-1-support-for-commerce"></a>Commerce のアップグレードおよび N-1 のサポート

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Retail の 2017 年 7 月のリリースで、アップグレードと N-1 サポートが有効になりました。 N-1 のサポートによって、Microsoft Dynamics AX 2012 R3 累積更新プログラム 10 (CU10) を実行する店舗を持つ顧客は、アップグレード後にバックオフィスで作業できます。 アップグレードと N-1 サポートの主な目的は、AX 2012 R3 の顧客がクラウドの利点を活用できるようにすることです。

次の機能を使用すると、顧客はシームレスにアップグレードできます。

- アップグレード プロセスを通じて、AX 2012 R3 からバックオフィスへのデータベース アップグレードを実行できるようになりました。
- AX 2012 R3 CU10 のコンポーネントを使用して店舗を運営することができます。
- アップグレード前とアップグレード後のチェックリストの検証は、アップグレード プロセスに組み込まれています。
- アップグレード プロセスでは、エラー処理とメッセージングが強化されているため、顧客は問題を迅速にデバッグできます。
- ユーザーは、ツールを使用して、既存のバックオフィスのカスタムの X++ コードを、そのバックオフィスのアップグレードされたバージョンに移行することができます。

アップグレード手順は、Retail を最新バージョンにアップグレードする手順とほぼ同じです。 一般に、アップグレードに関する詳細については、「[AX 2012 から Dynamics 365 Retail へのアップグレードの概要](../../fin-ops-core/dev-itpro/migration-upgrade/upgrade-overview-2012.md)」を参照してください。

計画的なダウンタイムが必要です。 アップグレード分析を最初に行います。 アップグレード分析は、Microsoft Dynamics AX 2012 データベースに対して実行され、Microsoft Dynamics Lifecycle Services (LCS) 診断サービスに基づいています。 このステップでは、アップグレードをより迅速かつ低コストで行うための作業を特定します。 また、必要な SQL 構成、データ バックオフィス クリーンアップ、推奨されない機能を識別します。
  
その後、実際のデータ アップグレード プロセスが発生します。 AX 2012 データベースは、Microsoft Azure SQL データベースに移動され、データ アップグレード パッケージは runbook プロセスを通じて通常どおり実行されます。 アップグレードの検証が完了します。 検証ツールは、使用される前にアップグレードされた環境に対して実行されます。 このツールは自動スモーク テストを実行して、サービスが動作してアクセス可能なこと、行数の一致、財務と在庫の調整などを検証します。

チャネルのアップグレード後構成のほとんどにおいて、手動での手順をほぼ必要としません。 顧客はアップグレード前およびアップグレード後のチェックリストを使用して、完了する必要があるタスクについて知ることができます。 アップグレード後のタスクには、アップグレードされたデータベースから店舗への完全な同期の開始、アップグレードされたデータベースに対するチャンネル、レジスター、およびデバイスの検証、トランザクションの同期の検証、N-1サポートが実施されていることの検証が含まれます。

N-1 のサポートでは、顧客は Commerce 本部で N-1 パッケージをインストールする必要があります。 店舗では設定は必要ありません。 このインストールは、N-1 関連の構成の完了後、アップグレード ウィンドウで実行する必要があります。

Commerce 本部のアップグレードと、N-1 の設定の完了後、N-1 店舗のコンポーネントが Commerce 本部と通信できるようになります。 N-1 のサポートのためにインストールが必要なチャネル側コンポーネントはありません。 ただし、N-1 店舗が Commerce 本部と通信できるようにするためには、レジ担当者が最初にサイン インした際にパスワードを変更する必要があります。

N-1インストールの手順については、 [段階的なロールアウト (N-1) インストール、コンフィギュレーション、および切替ガイド](n-1-installation-configuration.md) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
