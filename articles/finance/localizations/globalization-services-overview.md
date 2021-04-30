---
title: Dynamics 365 グローバリゼーション サービス
description: このトピックでは、Microsoft Dynamics 365 グローバリゼーション サービスの概要を示します。
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893051"
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
| Dynamics 365 Finance | あり | あり | あり | 
| Dynamics 365 Supply Chain Management | あり | あり | あり | 
| Dynamics 365 Project Operations | あり | あり | 適用できません | 
| Dynamics 365 Commerce | あり | 適用できません | 適用できません | 

> [!NOTE]
> RCS の Azure 地理的場所 (地理) の可用性が異なるため、このサービスの構成により、該当する Dynamics 365 オンライン サービスに選択された地理的な場所の外部に顧客データが転送される可能性があります。 詳細については [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズを参照してください](https://aka.ms/rcs/D365Productavailabilityguide)。