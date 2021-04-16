---
title: コンテンツ配信ネットワークの実装オプション
description: このトピックでは、Microsoft Dynamics 365 Commerce 環境で使用できるコンテンツ配信ネットワーク (CDN) の実装に関するさまざまなオプションを確認します。 オプションには、Azure Front Door のコマース提供のインスタンスおよび Azure Front Door の顧客所有のインスタンスであるネイティブが含まれます。
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9e98cf81f13b9181059bc96b95ac277a088311ea
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800714"
---
# <a name="content-delivery-network-implementation-options"></a>コンテンツ配信ネットワークの実装オプション

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce 環境で使用できるコンテンツ配信ネットワーク (CDN) の実装に関するさまざまなオプションを確認します。 オプションには、Azure Front Door のコマース提供のインスタンスおよび Azure Front Door の顧客所有のインスタンスであるネイティブが含まれます。

コマースの顧客は、コマース環境でどの CDN サービスを使用するか検討する際、いくつかのオプションがあります。 コマースは、基本的なホストとカスタム ドメインの要件をカバーする基本的な Azure Front Door サポートとともにリリースされます。 Web アプリケーション ファイアウォール (WAF) など、より詳細な制御機能とより具体的なセキュリティ能力を必要とする会社では、最良なオプションは Azure Front Door の顧客所有のインスタンスまたは外部の CDN サービスのいずれかを使用することです。

次の 3 つの CDN 実装オプションがコマース環境で使用できます。

- Azure Front Door のコマース提供インスタンス
- Azure Front Door の顧客所有インスタンス (制御強化と追加セキュリティ機能に向け)
- 外部 CDN サービス

3 つすべての CDN 実装オプションは、カスタム ドメインからの動的な HTML コンテンツのみを提供します。 コマースでは自動的に全ての JavaScript、Cascading Style Sheets (CSS)、画像、動画、そして Microsoft 管理の CDN を使った他の静的コンテンツを管理します。 選択するオプションによって、運用能力、制御機能、および追加のセキュリティ機能が決まります。

次の図では、コマース アーキテクチャの概要を表示します。

![コマース アーキテクチャの概要](media/Commerce_CDN-Option_ComparisonModels.png)

コマース サイトの Azure Front Door インスタンスを設定する方法については、[CDN サポートを追加](add-cdn-support.md) を参照してください。

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>コマース提供 Azure Front Door インスタンスの使用

次の表では、コンテンツ エンドポイントを管理するための Azure Fron Door のコマース提供インスタンスを使うことの長所と短所が示されています。

| プロ | 短所 |
|------|------|
| <ul><li>このインスタンスは、コマースの原価に含まれます。</li><li>このインスタンスはコマース チームによって管理されているため、メンテナンスの必要量を減らし、共有のセットアップ手順があります。</li><li>Azure でホストされたインフラストラクチャは、スケーラブル、セキュリティ、および信頼性があります。</li><li>Secure Sockets Layer (SSL) 証明書は、1 回の設定が必要で、自動的に更新されます。</li><li>このインスタンスでは、コマース チームがエラーや変更を監視します。</li></ul> | <ul><li>WAF はサポートされていません。</li><li>具体的なカスタマイズや設定調整はありません。</li><li>このインスタンスは、コマース チームによって更新や変更が異なります。</li><li>apex ドメインには別の Azure Front Door インスタンスが必要であり、Azure DNS の統合 apex ドメインには追加の作業が必要です。</li><li>顧客には、1 秒あたりの応答 (RPS) やエラー率に関する製品利用統計情報は提供されません。</li></ul> |

次の図は、コマースが提供する Azure Front Door インスタンスのアーキテクチャを示しています。

![コマース提供 Azure Front Door インスタンス](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>顧客所有 Azure Front Door インスタンスの使用

次の表では、コンテンツ エンドポイントを管理するための Azure Fron Door の顧客所有インスタンスを使うことの長所と短所が示されています。

| プロ | 短所 |
|------|------|
| <ul><li>設定はセキュリティで保護され、管理が容易です。</li><li>Azure でホストされたインフラストラクチャは、スケーラブル、セキュリティ、および信頼性があります。</li><li>このインスタンスでは、使用しているサイト向けに特別に調整されているより細かい等級のセキュリティに対して、WAF 統合およびきめ細かいルール制御が許可されます。</li><li>このインスタンスでは、SSL 証明書 (顧客所有と Azure Front Door 管理の両方) およびドメイン リンクの詳細な制御が可能です。</li><li>このインスタンスは、Azure DNS に直接使用される場合、ドメイン ソリューションを提供します。</li><li>製品利用統計情報および警告機能が用意されています。</li><li>SSL 証明書は、1 回の設定が必要で、自動的に更新されます。</li></ul> | <ul><li>インスタンスはセルフ管理されます。</li><li>初期知識のランプ アップが必要です。</li></ul> |

次の図は、顧客所有 Azure Front Door インスタンスを含むコマース インフラストラクチャを示しています。

![顧客所有 Azure Front Door インスタンスを含むコマース インフラストラクチャ](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>外部 CDN サービスの使用

次の表に、コンテンツ エンドポイントを管理するにあたり、外部 CDN サービスを使用の長所と短所を示します。

| プロ | 短所 |
|------|------|
| <ul><li>このオプションは、既存のドメインが既に外部 CDN でホストされている場合に便利です。</li><li>競合他社 CDN (たとえば、Akamai) は、WAF 機能を持つ場合があります。</li></ul> | <ul><li>別途契約を作成し、追加の原価設定を行う必要があります。</li><li>SSL は追加費用が発生する場合があります。</li><li>サービスは Azure クラウド構造とは別ので、追加のインフラストラクチャを管理する必要があります。</li><li>サービスでは、エンドポイントおよびセキュリティの設定に要する時間が長くなる場合があります。</li><li>サービスはセルフ管理されます。</li><li>サービスはセルフ監視されます。</li></ul> |

次の図は、外部の CDN サービスを含むコマース インフラストラクチャを示しています。

![外部の CDN サービスを含むコマース インフラストラクチャ](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>追加リソース

[コンテンツ配信ネットワーク (CDN) のサポートの追加](add-cdn-support.md)
