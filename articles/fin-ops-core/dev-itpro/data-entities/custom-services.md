---
title: カスタム サービスの開発
description: このトピックでは、カスタム サービスの作成方法を説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ace272d940b5d30d64c76e74c34a30a0eb81048
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893345"
---
# <a name="custom-service-development"></a>顧客サービスの開発

[!include [banner](../includes/banner.md)]

Finance and Operations に対してカスタム サービスを開発できます。 開発者が 1 つのサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは次の 2 つのエンドポイントに常に配置されます。

- SOAP エンドポイント
- JSON エンドポイント

### <a name="soap-based-custom-service"></a>SOAP ベース顧客サービス

SOAP ベースのサービスは Dynamics AX 2012 のものと同じままです。

SOAP を使用したカスタム サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication)で利用できます。

#### <a name="key-changes"></a>キーの変更

- **AOTService グループ**ノードの下にあるすべてのサービス グループが自動的に配置されます。
- 配置する必要があるすべてのサービスはサービス グループの一部である必要があります。

**開発環境でのエンドポイントの例**

`https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`

**非開発環境でのエンドポイントの例**

`https://<baseurl>/soap/services/UserSessionService?wsdl`

カスタム サービスの詳細については、次を参照してください。

- [カスタム サービスを使用する \[AX 2012\] (TechNet)](https://technet.microsoft.com/library/hh509052.aspx)
- [チュートリアル: X++ クラスをデータ契約として公開する (TechNet)](https://technet.microsoft.com/library/gg844225.aspx)

### <a name="json-based-custom-service"></a>JSON ベース顧客サービス

この機能により、X++ クラスを JSON サービスとして使用できます。 つまり、返り値のデータ セットは、JSON 形式でです。 JavaScript Object Notation の略である JSON は、クライアントとサーバー間のデータ通信によく使用されるコンパクトで軽量なフォーマットです。

JSON エンドポイントが `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name` にあります。

**例**

`https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`

JSON サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication)で利用できます。
