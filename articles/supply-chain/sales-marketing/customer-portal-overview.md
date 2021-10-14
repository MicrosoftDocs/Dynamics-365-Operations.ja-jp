---
title: Dynamics 365 Supply Chain Management の顧客ポータルの概要
description: このトピックでは、顧客ポータルの概要とその使用方法および機能について説明します。
author: Henrikan
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 79dc0527c4e65b6984ea3bf043a653961fcab14f
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572676"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Dynamics 365 Supply Chain Management の顧客ポータルの概要

[!include [banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a>顧客のポータルの概要

最新のサプライ チェーンシステムは統合と依存関係があります。 そのためには、在庫、顧客需要、販売部門を個別の格納するのではなく統合する必要があります。 顧客ポータルを使用することで、Microsoft Dynamics 365 Supply Chain Management を実行している組織がこの統合を促進し、顧客に情報をより効果的に提供することができます。

顧客ポータルは、[Power Apps ポータル](/powerapps/maker/portals/overview)のテンプレートを指し、販売注文の処理に関連するシナリオに対して、外部と接する企業間 (B2B) の Web サイトを作成することができます。 このテンプレートでは、[デュアル書き込み ](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)、Supply Chain Management、Power Apps ポータルを使用して、外部企業の顧客が Dynamics 365 環境からデータを表示および作成できるようになります。

顧客ポータル テンプレートには、Power Apps ポータル機能のすべてのカスタマイズ機能が用意されています。 テンプレートの変更は簡単に行うことができ、企業のブランドを表わす、機能の強化、ユーザー エクスペリエンスの変更をすることができます。 テンプレートが提供するすべての機能は必要に応じて変更できます。

> [!IMPORTANT]
> テンプレートそのものが、完全に機能するとは限りません。 企業の顧客が Supply Chain Management のデータにアクセスできるよう、外部向けの Web サイトを作成したいと考えている顧客のためのイネーブラーとしての役割を果たします。

> [!NOTE]
> 顧客ポータルのドキュメントは、Supply Chain Management の顧客ポータルをインストールや設定を行う管理者、カスタマイザー、システム インテグレーターに向けられています。 Supply Chain Management を運用している組織の顧客や、最終的なポータルの利用者は、_顧客_ と _ユーザー_ という用語で表わされます。

## <a name="video"></a>ビデオ

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

[Dynamics 365 Supply Chain Management の顧客ポータル テンプレート](https://youtu.be/nPrqoLuHfV8) ビデオ (上記参照) は、YouTube で利用可能な [Finance and Operations 再生リスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。

## <a name="who-should-use-it"></a>対象となるユーザー

顧客ポータルは、Supply Chain Managementを実行し、次の特性を持つ企業に向けて設計されています :

- こうした企業は、注文処理情報 (注文状況やアカウント情報など) を、Supply Chain Management システムから企業の顧客に直接連絡する、外部に向けた Webサイトの構築を目的としています。
- Dynamics AX 2012 から Supply Chain Management へと移行しており、以前は [AX 2012 Customer self-service portal](/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal) を使用していました。

次のようなタイプの組織は、顧客ポータルの実装には **向いていない** でしょう :

- エンタープライズ以外の顧客に向けて Web サイトを構築する企業。 こうした企業は、[Dynamics 365 Commerce e-コマースの Web サイト](../../commerce/create-ecommerce-site.md) 作成を検討する必要があります。
- 既存の Power Apps Web サイトを同様の目的で使用している企業。 このような企業には、顧客ポータルをしようしてもさらなる恩恵を得ることはないでしょう。 顧客ポータルは、デュアル書き込み、Supply Chain Management、Power Apps ポータル間の「点と点をつなげる」ことを希望する顧客に向けたガイドとなるテンプレートとして提供されます。 この目的を果たす Web サイトを既に設定している場合は、顧客ポータル テンプレートを使用して Web サイトの再プロビジョニングを行っても多くの恩恵を得られない場合があります。

## <a name="how-does-it-work"></a> どのような仕組みですか?

顧客 ポータルは、Power Apps ポータルのテンプレートとして提供されます。 これは、Power Apps ポータルとデュアル書き込みに対して依存関係があります。

[Power Appsポータル](/powerapps/maker/portals/overview)を使用することで、組織の外部のユーザーがログインできる外部向けの Web サイトをユーザーが作成できるようになります。 ポータルの作成には、コードの記述がほとんど必要ありません。 顧客ポータルは、Microsoft から入手可能な、多くの [Dynamics 365 ポータルテンプレート](/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) の1つです。

[デュアル書き込み](/powerapps/maker/portals/overview) は、Customer Engagement アプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する既成のインフラストラクチャ製品です。 デュアル書き込みは、Finance and Operations アプリと Microsoft Dataverse の間で密に結合された双方向の統合を可能とします。 そのため、アプリを横断して統合されたユーザー エクスペリエンスを実現します。 顧客ポータルは、デュアル書き込みと同期されているテーブルに依存関係があります。 Supply Chain Management からのデータを顧客ポータルで表示する前に、デュアル書き込みをすべての適切なテーブルに対して有効にする必要があります。

![顧客ポータルの依存関係。](media/customer-portal-elements.png "顧客ポータルの依存関係")

顧客ポータルは、 Power Apps ポータルを使用して Supply Chain Management のインストール データを使用した外部向けの Web サイトを構築したいと考えている組織にとっての出発点としての役割を果たします。 これにより、組織は、デュアル書き込み、Supply Chain Management、Power Apps ポータルを接続することができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]