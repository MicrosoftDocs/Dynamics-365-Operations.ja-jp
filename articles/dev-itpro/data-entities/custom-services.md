---
title: カスタム サービスの開発
description: このトピックでは、カスタム サービスの作成方法を説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25caa03746424782b892a6db4825aaf072defdb1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368607"
---
# <a name="custom-service-development"></a>顧客サービスの開発

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations に対してカスタム サービスを開発できます。 開発者が 1 つのサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは次の 2 つのエンドポイントに常に配置されます。

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

`https://<env-name>soap.cloudax.dynamics.com/soap/services/UserSessionService?wsdl`

カスタム サービスの詳細については、次を参照してください。

- [カスタム サービスを使用する \[AX 2012\] (TechNet)](http://technet.microsoft.com/en-us/library/hh509052.aspx)
- [チュートリアル: X++ クラスをデータ契約として公開する (TechNet)](http://technet.microsoft.com/en-us/library/gg844225.aspx)

<!--
- [Custom services Office Mix presentation](https://mix.office.com/watch/12e4fejbgj429). -->


### <a name="json-based-custom-service"></a>JSON ベース顧客サービス

この機能により、X++ クラスを JSON サービスとして使用できます。 つまり、返り値のデータ セットは、JSON 形式でです。 JavaScript Object Notation の略である JSON は、クライアントとサーバー間のデータ通信によく使用されるコンパクトで軽量なフォーマットです。

JSON エンドポイントが `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name` にあります。

**例**

`https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`

JSON サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication)で利用できます。
