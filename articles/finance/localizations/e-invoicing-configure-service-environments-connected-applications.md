---
title: サービス環境と接続されたアプリケーションの構成
description: この記事では、サービス環境および接続されたアプリケーションの構成方法に関する情報について説明します。
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8ede98cfad685992bad3fb643ea46d6adcb08487
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269534"
---
# <a name="configure-service-environments-and-connected-applications"></a>サービス環境と接続されたアプリケーションの構成

[!include [banner](../includes/banner.md)]

この記事では、サービス環境および接続されたアプリケーションの構成方法に関する情報について説明します。 このプロセスには 3 つの手順があります。 手順 1 は必須で、手順 2 と 3 はオプションです。

## <a name="step-1-create-a-service-environment"></a>手順 1: サービス環境の作成

サービス環境を作成する場合、グローバリゼーション機能をサービスに展開できるユーザーの一覧を定義します。 一部のシナリオでは、必要に応じて電子請求サービスと通信できる外部アプリケーションの一覧を定義します。 それをシナリオで使用する場合は、番号順序を設定します。

この手順を完了するには、[サービス環境](e-invoicing-service-environments.md) を参照してください。

## <a name="step-2-add-certificates-and-secrets"></a>手順 2: 証明書とシークレットの追加

参照を Microsoft Azure キー コンテナーに追加して、それをシナリオで使用します。 パイプライン処理中のアクションが、証明書と、デジタル署名または外部 Web サービスを使用した通信のためのシークレットを使用する場合、この手順は必須です。

この手順を完了するには、[顧客の証明書およびシークレット](e-invoicing-customer-certificates-secrets.md) を参照してください。

## <a name="step-3-configure-connected-applications"></a>手順3: 接続されているアプリケーションの構成

Dynamics 365 Finance または Dynamics 365 Supply Chain Management アプリケーションと、電子請求間の通信を設定するには、Finance または Supply Chain Management を構成して電子請求サービスへの呼び出しを作成し、必要な電子形式に変換できる統合構造内にビジネス データを準備する必要があります。 また、アプリケーションはサービスからの応答も適切に処理する必要があります。 この構成は、Finance 環境または Supply Chain Management 環境で直接実行するか、Regulatory Configuration Service (RCS) で完了できます。 RCS で構成を完了すると、Finance または Supply Chain Management 環境に配置できます。 この手順では、接続されているアプリケーションをパラメータの展開用に登録します。

この手順を完了するには、[接続されているアプリケーション](e-invoicing-connected-applications.md) を参照してください。
