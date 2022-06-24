---
title: 電子請求サービスへの登録およびインストール
description: この記事では、電子請求サービスにサインアップしてインストールする方法についての情報を提供します。
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 57314058883e60599bc51d91a65b0daeae724bb7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865529"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>電子請求サービスへの登録およびインストール

[!include [banner](../includes/banner.md)]

この記事では、電子請求サービスにサインアップしてインストールする方法についての情報を提供します。 このプロセスには 4 つの手順があります。 手順1 ～ 3 が必須であり、手順 4 はオプションです。

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>手順 1: Regulatory Configuration Service にサインインする

Regulatory Configuration Service (RCS) は、電子請求書を構成するために使用される構成と設計エクスペリエンスを提供します。 環境や電子請求書機能などのリソースは、RCS で作成、維持、管理されます。 リソースの準備が整うと、電子請求サービスにリソースが公開されます。

RCS の詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md) を参照してください。

RCS にサインインするには、[Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) ページに移動します。

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>手順 2: Microsoft Dynamics Lifecycle Services でのマイクロサービス向けアドインをインストールする

電子請求サービスは、Microsoft データセンサーでホストされる一連のマイクロサービスです。 既定では、Dynamics 365 Finance および Dynamics 365 Supply Chain Management の顧客は電子請求サービスのアクセス権は持っていません。 このファイルは、Microsoft Dynamics Lifecycle Services (LCS) にアドインとしてインストールする必要があります。 アドインをインストールすると、電子請求サービスへの接続が許可されるアプリケーションのレジスターに財務または Supply Chain Management 環境が登録されます。

この手順を完了させるには、[Lifecycle Services でのマイクロサービス向けアドインのインストール](e-invoicing-install-add-in-microservices-lcs.md) を参照してください。

### <a name="step-3-set-up-rcs"></a>手順 3: RCS を設定する

RCS と電子請求サービスとの間の統合を設定する必要があります。 メイン コンポーネントも設定する必要があります。

この手順を完了するには、[Regulatory Configuration Service (RCS) の設定](e-invoicing-set-up-rcs.md) を参照してください。

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>手順 4: Microsoft Power Platform プラグイン管理リファレンス

一部のシナリオでは、Microsoft Power Platform のスコープで Dataverse との統合が必要です。

現在、この設定は、分数電子請求のシナリオで電子請求ソリューションを使用する場合は必須です。 ただし、サウジアラビアの電子請求のシナリオでは省略できます。 詳細については、[国や地域別の電子請求機能の可用性](e-invoicing-country-specific-availability.md) を参照してください。

この手順を完了するには、[Microsoft Power Platform プラグイン管理者リファレンス](e-invoicing-power-platform-plug-in.md) を参照してください。
