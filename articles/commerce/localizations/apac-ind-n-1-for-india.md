---
title: インド向けアップグレードと N-1 のサポート
description: このトピックでは、インドでのコマース顧客向けの N-1 サポート概要を提供します。
author: kfend
manager: ezubov
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: India
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 28b76c7b88f6839750e48b928fd94dae32076fe4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012406"
---
# <a name="support-for-upgrade-and-n-1-for-india"></a>インド向けアップグレードと N-1 のサポート

[!include [banner](../includes/banner.md)]

このトピックでは、インドでの段階的なロールアウト (N-1) コマース コンポーネントの設定および使用に必要な手順を説明します。 N-1 のアップグレード手順およびワークフローは、基本的に一般的な Dynamics 365 Commerce 環境のものと同じです。 N-1 のインストールおよび使用の一般的な情報は、[Retail のアップグレードおよび N-1 のサポート](../dev-itpro/overview-upgrade-n-minus1.md)を参照してください。

さらに、次の手順はアップグレードのために重要です。

- コマース バックオフィス および AX 2012 Retail コンポーネントの両方が商品及びサービス税 (GST) 計算をサポートしている必要があります。 詳細については、[必要条件](#prerequisites) セクションを参照してください。
- AX 2012 チャンネル側でコマースのために準備されたコンフィギュレーションを使用するには、GST コンフィギュレーションのダウングレードが必要です。
- 配送スケジュールには、バックオフィスと AX 2012 チャンネル間で GST コンフィギュレーションおよび税計算結果を同期するために必要な、追加のアップロード ジョブおよびダウンロード ジョブが含まれます。

## <a name="prerequisites"></a>必要条件

- AX 2013 R3 小売コンポーネントを GST Update 2、[KB4058327](https://fix.lcs.dynamics.com/Issue/Details?kb=4058327&bugId=3898178&qc=acbe1a0b3f5d9240d56a94a633fa69fbfe4be0cf98587fd05a7807e082210a12)、またはそれ以降に更新します。 詳細については、[インド GST 更新 2 - リリース ノート](https://mbs.microsoft.com/Files/customer/AX/Downloads/Taxupdates/Release-Note-India-GST-Update-2.pdf)を参照してください。
- 基本的な N-1 環境を設定します。 詳細については、[Phased Rollout (N-1) のインストール、コンフィギュレーション、および切替ガイド](../dev-itpro/n-1-installation-configuration.md)を参照してください。
- [インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合](./apac-ind-cash-registers.md) ガイドに基づき、バックオフィスでインド向けコマース GST を設定します。

## <a name="periodic-procedure-to-downgrade-tax-configuration"></a>税コンフィギュレーションをダウングレードする定期処理

GST コンフィギュレーション データは AX 2012 およびコマースのバージョン間で異なります。 データを変換するには、特別な定期処理手順を実行する必要があります。 この手順を実行するには、以下の内容を実行します:

1. バックオフィスにサインインして、**Retail と Commerce \> Retail と Commerce IT \> N-1 から税構成を処理する** に移動します。
2. **OK** をクリックします。

税構成の変更が行われて確定するたび、データを AX 2012 チャネルに送信する間に上記の操作を実行する必要があります。
