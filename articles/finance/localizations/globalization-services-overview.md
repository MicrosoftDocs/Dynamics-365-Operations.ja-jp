---
title: Dynamics 365 グローバリゼーション サービス
description: この記事では、Microsoft Dynamics 365 グローバリゼーション サービスの概要を示します。
author: kfend
ms.date: 04/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
ms.openlocfilehash: eebf74ab30a544f6561cf5782148d12b58d9c4b7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278235"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 グローバリゼーション サービス

[!include [banner](../includes/banner.md)]

次のグローバリゼーション サービスは、一部の Microsoft Dynamics 365 オンライン サービスに存在する機能を拡張するように構成できます。

- **Regulatory Configuration Service (RCS)** は、さまざまなタイプの電子ドキュメントおよびレポート の構成をサポートします。 RCS はコンフィギュレーション リポジトリがスタンドアロンのサービスである、電子申告 (ER) の デザイナーの拡張バージョンを提供します。 詳細については、[Regulatory Configuration Service](rcs-overview.md) を参照してください。
- **電子請求** は、変換、デジタル署名、および認証や応答処理などの外部 Web サービスとの接続のための構成可能な統合のための構成可能な形式をまとめたものです。 詳細については、[電子請求](e-invoicing-service-overview.md) を参照してください。
- **税計算** は、複数の税 ID、税コード決定、税計算デザイナー、および世界中の複雑な税規制に準拠するランタイム エンジンをサポートすることにより、柔軟性を強化します。 詳細については、[税の計算](global-tax-calcuation-service-overview.md) を参照してください。

これらのグローバリゼーション サービスは、次の Dynamics 365 オンライン サービスと一新された統合を提供します。

| オンライン サービス | RCS | 電子請求 | 税の計算 (プレビュー) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | 有効 | 有効 | 有効 | 
| Dynamics 365 Supply Chain Management | 有効 | 有効 | 有効 | 
| Dynamics 365 Project Operations | 有効 | 有効 | 該当なし | 
| Dynamics 365 Commerce | 有効 | 該当なし | 適用できません | 

> [!NOTE]
> RCS の Azure 地理的場所 (地理) の可用性が異なるため、このサービスの構成により、該当する Dynamics 365 オンライン サービスに選択された地理的な場所の外部に顧客データが転送される可能性があります。 詳細については [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズを参照してください](https://aka.ms/rcs/D365Productavailabilityguide)。
