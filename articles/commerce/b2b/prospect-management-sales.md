---
title: Dynamics 365 Sales を使った B2B e コマース Web サイトでのビジネス パートナー ユーザーを管理する
description: このトピックでは、Microsoft Dynamics 365 Sales を使用して、Dynamics 365 Commerce 企業間 (B2B) の Web サイトに対するビジネス パートナーの承認を管理する方法について説明します。
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c6ac5409de5101c91b9348de800e3eaea9895c23
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/16/2022
ms.locfileid: "8312606"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Dynamics 365 Sales を使った B2B e コマース Web サイトでのビジネス パートナー ユーザーを管理する

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Sales を使用して、Dynamics 365 Commerce 企業間 (B2B) の Web サイトに対するビジネス パートナーの承認を管理する方法について説明します。 Dynamics 365 Sales ソリューションに既に投資している組織は、B2B の e コマースのビジネス パートナー承認プロセスに対して、そのリード タイムと営業案件の概念を使用できます。

B2B ビジネス パートナーの承認プロセスのバックグラウンドの情報については、[B2B eコマースの Web サイトでのビジネス パートナー ユーザーの管理](manage-b2b-users.md) を参照してください。

潜在的なビジネス パートナーは、B2B Web サイト上のリンクを介してオンボーディング リクエストを送信することで、B2B e コマース Web サイトへのオンボーディング プロセスを開始することができます。 要求が送信された後、関連するジョブ (**P-0001** や **注文およびチャンネル要求の同期** など) がCommerce 本部で実行されると、その日に開催される要求は、Commerce 本部の **全見込顧客** ページに保存されます。 その後、販売でビジネス パートナーの見込顧客の承認プロセスを完了できます。

Sales と Commerce との間の統合が有効になると、Commerce でビジネス パートナーの見込顧客が作成され、Sales で *リード* が作成されます。

次の図は、販売のビジネス パートナー見込顧客のリード作成ページの例を示しています。

![Dynamics 365 Sales の リード 作成ページ](../media/LeadInSales.png)

この図では、**連絡先** セクションには所属する要求の送信者が示され、**会社** セクション には組織が表示されます。 **タイムライン** セクションのメモは、デュアル書き込みインフラストラクチャによってリードが生成された場合に示されます。 このリードはデュアル書き込みインフラストラクチャによって作成されたので、**自分のオープン リード** ドロップダウン リストには表示されません。 代わりに、**すべての Commerce B2B リード** という 名前の新しいビューの下に表示されます。

販売の標準のリード タイムプロセスで、ユーザーが、*営業案件* レコード、*連絡先* レコード、*アカウント* レコードを "見込みあると評価する" 場合に作成されます。 デュアル書き込みインフラストラクチャは、連絡先およびアカウント レコードを Commerce に書き込む場合に使用します。 連絡先が *個人* タイプの顧客として作成され、会社は *組織* タイプの顧客として作成されます。 ユーザーが営業案件で **受注として完了** を選択すると、その見込顧客は Commerce で承認されます。 見込顧客の承認によって、顧客階層が作成されます。

残りの業務プロセスはすべて Commerce で発生します。 このプロセスには、ビジネス パートナーへの電子メールの送信、ユーザーの与信限度額管理の定義、B2B サイトへのユーザーの追加が含まれます。 ただし、ユーザーが顧客を見込みなしと評価したり、営業案件をリードを見込みありと評価する代わりに失注としてマークを付けた場合、Commerce の見込顧客は拒否としてマークされ、承認を示すメールが要求者に送信されます。

## <a name="enable-integration-between-sales-and-commerce"></a>Sales と Commerce との間の統合を有効にする

Sales と Commerce の統合は、二重書き込みインフラストラクチャに依存しています。 したがって、あるシステムで作成された顧客がもう一方のシステムにも書き込まれるように、二重書き込みを有効にし、機能させる必要があります。 二重書き込み機能の詳細については、[二重書き込みの概要](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) を参照してください。

二重書き込み設定が完了すると、実装パートナーは [Microsoft AppSource](https://appsource.microsoft.com/) に移動して、[二重書き込み Commerce ソリューション](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview) という名前のソリューションを検索することができます。 標準のインストール ウィザードを使用してパッケージをインストールし、B2B サイトで見込顧客を作成してパッケージをテストします。 見込顧客が作成された後、**すべての見込顧客** が Commerce に表示されている要求を確認し、見込顧客が Sales のリードとして表示されている点を確認します。

## <a name="additional-resources"></a>追加リソース

[B2B eコマース Web サイトでのビジネス パートナー ユーザーの管理](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
