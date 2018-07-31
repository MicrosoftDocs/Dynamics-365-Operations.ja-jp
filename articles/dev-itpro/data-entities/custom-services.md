---
title: "顧客サービス"
description: "このトピックでは、カスタム サービスの作成方法を説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2475c6db57d1fa01ca914e568407b5f618ba95a1
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="custom-services-for-microsoft-dynamics-365-for-finance-and-operations"></a>Microsoft Dynamics 365 for Finance and Operations の顧客サービス

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations のカスタム サービスを展開することができます。 開発者がサービス グループに属するカスタム サービスを書き込むと、そのサービス グループは 2 つのエンドポイントに常に配置されます。
-   SOAP エンドポイント 
-   JSON エンドポイント

### <a name="soap-based-custom-service"></a>SOAP ベース顧客サービス

SOAP ベースのサービスは AX 2012 のものと同じままです。

SOAP を使用してカスタム サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/SoapConsoleApplication) です。

#### <a name="key-changes"></a>キーの変更

-   **AOTService グループ**ノードの下にあるすべてのサービス グループが自動的に配置されます。
-   配置する必要があるすべてのサービスはサービス グループの一部である必要があります。

SOAP エンドポイントが `https://host_uri/soap/services/service_group_name` にあります。 

**例:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/soap/services/UserSessionService?wsdl`

詳細については、以下を参照してください。
-   [カスタム サービスを使用する \[AX 2012\] (TechNet)](http://technet.microsoft.com/en-us/library/hh509052.aspx)
-   [チュートリアル: X++ クラスをデータ契約として公開する (TechNet)](http://technet.microsoft.com/en-us/library/gg844225.aspx)

<!--
-   [Custom services Office Mix presentation](https://mix.office.com/watch/12e4fejbgj429). -->


### <a name="json-based-custom-service"></a>JSON ベース顧客サービス

この機能により、X++ クラスを JSON サービスとして使用できます。 つまり、返り値のデータ セットは、JSON 形式でです。 JavaScript Object Notation を示す JSON は、クライアントとサーバーの間でのデータ通信によく使用されるコンパクトで軽量なフォーマットです。 

JSON エンドポイントが `https://host_uri/api/services/service_group_name/service_group_service_name/operation_name` にあります。

**例:** `https://usnconeboxax1aos.cloud.onebox.dynamics.com/en/api/services/UserSessionService/AifUserSessionService/GetUserSessionInfo`

JSON サービスを使用するためのコード例は、[Microsoft Dynamics AX 統合 GitHub リポジトリ](https://github.com/Microsoft/Dynamics-AX-Integration/tree/master/ServiceSamples/JsonConsoleApplication) です。


