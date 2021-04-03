---
title: 証明書タイプ
description: このトピックでは、Dynamics 365 Human Resources の証明書タイプ エンティティについて説明します。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 962bccb3aaab16322d072417660ec3aac821183b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467484"
---
# <a name="certificate-type"></a>証明書タイプ

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の証明書タイプ エンティティについて説明します。

物理名 : mshr_hcmcertificatetypeentity

## <a name="description"></a>説明

このエンティティは、Human Resources で設定された職業証明書タイプの一覧を定義します。 エンティティは、法人 (会社) に固有のエンティティではありません。

## <a name="json-representation"></a>JSON 表記

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **証明書タイプ エンティティ ID**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | 読み取り専用<br>必須 
システム生成 | 証明書タイプに固有のプライマリ識別子です。 |
| **証明書タイプ**<br>mshr_certificatetype<br>*文字列* | 読み取り/書き込み<br>必須 | 証明書タイプに固有のユーザーが読取り可能な識別子です。 |
| **説明**<br>mshr_description<br>*文字列* | 読み取り/書き込み<br>必須 | 証明書タイプの説明。 |
| **更新の要求**<br>mshr_requirerenewal<br>*mshr_noyes オプション セット* | 読み取り/書き込み<br>オプション | 証明書に更新が必要かどうかを示します。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]