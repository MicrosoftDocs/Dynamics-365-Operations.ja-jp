---
title: "Retail コンポーネント"
description: "このトピックでは、Microsoft Dynamics 365 for Retail を構成するさまざまなコンポーネントについて説明します。"
author: sericks007
manager: AnnBe
ms.date: 03/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 221954
ms.assetid: 8fe1b080-00d4-41ae-b047-10da160877ab
ms.search.region: Global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ef10f6272aaa97f5f10aa5234938d3f0b5bdd702
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="retail-components"></a>Retail コンポーネント

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Retail を構成するさまざまなコンポーネントについて説明します。

Dynamics 365 for Retail は、中規模市場および大規模小売業者に、オンラインと従来型のストアのサポートを含む完全な本社および販売時点管理 (POS) ソリューションを提供します. 小売業者が財務収益を高め、サービスを向上させ、成長を管理して、顧客に到達し、効率面を合理化できます。
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>コンポーネント</strong></td>
<td><strong>機能</strong></td>
</tr>
<tr class="even">
<td>小売用バックオフィス</td>
<td>Dynamics 365 for Retail 用小売用バックオフィスを使用すると、一連の店舗を 1 つの企業として管理することができます。 これは、日々の業務を管理し、チェーンの全店舗の販売情報を追跡します。 小売用スケジューラは、Dynamics 365 for Retail と店舗間の通信を調整します。 小売用バックオフィスは、POS 、または必要なデータを受信して転送できるオンライン店舗システムで使用できます。 <strong>重要:</strong> Dynamics 365 for Retail のカスタム POS またはオンライン ストア ソリューションの構築は、広範な計画、開発、およびテストが必要な複雑な作業です。</td>
</tr>
<tr class="odd">
<td>Retail POS</td>
<td>Dynamics 365 for Retail では、POS 経験の 2 つのタイプがサポートされます。
<ul>
<li><strong>クラウド POS</strong> はブラウザベースの POS で、モバイルデバイスで使用できます。</li>
<li><strong>Retail Modern POS</strong> (MPOS) は、PC、タブレット、電話などのクライアントで、販売トランザクション、顧客注文、日常業務を処理し、在庫管理を実行するために使用できます。</li>
</ul></td>
</tr>
<tr class="even">
<td>Retail サーバー</td>
<td>Retail サーバーは、従業員と顧客の両方が情報にアクセスし、Retail POS クライアントとオンライン店舗の両方を使用してタスクを実行できるようにする、OData Web API を提供します。</td>
</tr>
<tr class="odd">
<td>ハードウェア ステーション</td>
<td>Retail Hardware Station には、Retail POS クライアントと、プリンター、キャッシュ ドロワー、支払いデバイスなどの周辺基金が Retail Server と通信できるようにするサービスが用意されています。</td>
</tr>
<tr class="even">
<td>Retail Store スケール ユニット</td>
<td>Retail Store スケール ユニットは、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。 Store スケール ユニットは、店舗内の工程専用に設計されており、バック オフィスに接続していない場合でもターミナル間トランザクションおよびシフト操作が可能になります。</td>
</tr>
<tr class="odd">
<td>Commerce Runtime</td>
<td>Commerce Runtime (CRT) は、さまざまなチャネル全体にビジネス ロジックをサポートするコア エンジンとして使用されます。 Commerce Runtime には、データ アクセス レイヤー、サービス レイヤー、ワークフロー レイヤーおよびアプリケーション プログラミング インターフェイス (API) レイヤーが含まれています。</td>
</tr>
<tr class="even">
<td>チャネル データベース</td>
<td>チャンネル データベースは、オンライン ストアや従来型店舗など、1 つ以上の小売チャンネルの小売データを保持します。</td>
</tr>
<tr class="odd">
<td>E コマース プラットフォーム SDK</td>
<td>包括的な E コマース プラットフォームにより、プラットフォームのオムニチャネル サービスを利用できるフロントエンドのオンライン ストアにプラグインできます。 ソフトウェア開発キット (SDK) は、プラットフォームをいかに活用できるかを示すサンプル オンライン ストアで構成されています。</td>
</tr>
<tr class="even">
<td>Retail SDK</td>
<td>Retail SDK には、サンプル ソース コードと、Retail システムをカスタマイズするために使用できるテンプレートが含まれています。</td>
</tr>
</tbody>
</table>

![SystemArchitecture](./media/Dynamics-365-for-Retail-System-Architecture.PNG)





