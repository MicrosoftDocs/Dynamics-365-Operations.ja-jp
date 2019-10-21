---
title: Retail のコンポーネント
description: このトピックは、Dynamics 365 Retail を構成するさまざまなコンポーネントについて説明します。
author: sericks007
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 221954
ms.assetid: 8fe1b080-00d4-41ae-b047-10da160877ab
ms.search.region: Global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a240175afe9b5eb98763e729f121b90bc9b062aa
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025138"
---
# <a name="retail-components"></a>Retail のコンポーネント

[!include [banner](includes/banner.md)]

このトピックは、Dynamics 365 Retail を構成するさまざまなコンポーネントについて説明します。

Retail は、中規模市場および大規模小売業者に、オンラインと従来型のストアのサポートを含む完全な本社および販売時点管理 (POS) ソリューションを提供します. 小売業者が財務収益を高め、サービスを向上させ、成長を管理して、顧客に到達し、効率面を合理化できます。

<table>
<thead>
<tr>
<th>コンポーネント</th>
<th>職務</th>
</tr>
</thead>
<tbody>
<tr>
<td>Retail Headquarters</td>
<td>Dynamics 365 Retail 用小売用バックオフィスを使用すると、一連の店舗を 1 つの企業として管理することができます。 これは、日々の業務を管理し、チェーンの全店舗の販売情報を追跡します。 小売用スケジューラは、Retail と店舗間の通信を調整します。 小売用バックオフィスは、POS 、または必要なデータを受信して転送できるオンライン店舗システムで使用できます。
<p><strong>重要:</strong> Retail において、カスタム POS またはオンライン ストア ソリューションの構築を行うには、広範囲にわたる計画、開発、およびテストなどの複雑な作業が必要となります。</p>
</td>
</tr>
<tr>
<td>Retail POS</td>
<td>Dynamics 365 Retail では POS エクスペリエンスの 2 種類のイベントがサポートされます。
<ul>
<li><strong>クラウド POS</strong> はブラウザベースの POS で、モバイルデバイスで使用できます。</li>
<li><strong>Retail Modern POS</strong> (MPOS) は、PC、タブレット、電話などのクライアントで、販売トランザクション、顧客注文、日常業務を処理し、在庫管理を実行するために使用できます。</li>
</ul>
</td>
</tr>
<tr>
<td>Retail サーバー</td>
<td>Retail サーバーは、従業員と顧客の両方が情報にアクセスし、Retail POS クライアントとオンライン店舗の両方を使用してタスクを実行できるようにする、OData Web API を提供します。</td>
</tr>
<tr>
<td>ハードウェア ステーション</td>
<td>Retail Hardware Station には、Retail POS クライアントと、プリンター、キャッシュ ドロワー、支払いデバイスなどの周辺基金が Retail Server と通信できるようにするサービスが用意されています。</td>
</tr>
<tr>
<td>Retail Store Scale Unit</td>
<td>Retail Store Scale Unit は、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。 Store スケール ユニットは、店舗内の工程専用に設計されており、バック オフィスに接続していない場合でもターミナル間トランザクションおよびシフト操作が可能になります。</td>
</tr>
<tr>
<td>Retail Cloud Scale Unit</td>
<td>Retail Cloud Scale Unit は、店頭または電子商取引において小売チャンネルの操作 (販売時点情報管理など) を可能にする一連のコンポーネントです。 Retail Cloud Scale Unit には小売サーバー、小売チャンネル データベース、およびクラウドPOSが含まれます。 Retail Cloud Scale Unit はMicrosoftによって提供、管理されています。 Retail Cloud Scale Unit はクラウド ホスト型小売サーバー、小売チャンネルのデータベース、およびクラウドPOSなどの旧製品の改良版です。</td>
<tr>
<td>Commerce Runtime</td>
<td>Commerce Runtime (CRT) は、さまざまなチャネル全体にビジネス ロジックをサポートするコア エンジンとして使用されます。 Commerce Runtime には、データ アクセス レイヤー、サービス レイヤー、ワークフロー レイヤーおよびアプリケーション プログラミング インターフェイス (API) レイヤーが含まれています。</td>
</tr>
<tr>
<td>チャネル データベース</td>
<td>チャンネル データベースは、オンライン ストアや従来型店舗など、1 つ以上の小売チャンネルの小売データを保持します。</td>
</tr>
<tr>
<td>E コマース プラットフォーム SDK</td>
<td>包括的な E コマース プラットフォームにより、プラットフォームのオムニチャネル サービスを利用できるフロントエンドのオンライン ストアにプラグインできます。 ソフトウェア開発キット (SDK) は、プラットフォームをいかに活用できるかを示すサンプル オンライン ストアで構成されています。</td>
</tr>
<tr>
<td>Retail SDK</td>
<td>Retail SDK には、サンプル ソース コードと、Retail システムをカスタマイズするために使用できるテンプレートが含まれています。</td>
</tr>
</tbody>
</table>

![SystemArchitecture](./media/Dynamics-365-for-Retail-System-Architecture.PNG)
