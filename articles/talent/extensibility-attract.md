---
title: "Attract での拡張性"
description: "このトピックでは、Microsoft Power Platform を使用して Microsoft Dynamics 365 for Talent - Attract を拡張する方法について説明します。"
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 0af60a0aea0f7a5de793631445aaebb37dbb0d74
ms.contentlocale: ja-jp
ms.lasthandoff: 10/22/2018

---

# <a name="extensibility-in-attract"></a>Attract での拡張性

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent は、アプリ プラットフォームの Common Data Service (CDS) の上に構築され、Microsoft Power Platform および Common Data Service for Apps が提供する機能を使用してさまざまな方法で拡張できます。 したがって、Microsoft PowerApps および Microsoft Flow を使用して、システムをコンフィギュレーションおよびカスタマイズできます。 Microsoft Power BI を使用して、人々に関する追加の分析を取得することもできます。 さらに、PowerApps および Web コンテンツ (iframe) 活動などの新しいカスタム活動は、採用プロセスをこれまで以上に適応しやすくします。 これらの活動を使用することにより、採用プロセスをビジネス ニーズとプロセスに合わせることができ、採用チームと候補者の両方にシームレスでカスタマイズされた経験があることを確認できます。

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platform を活用 

Attract からのすべてのデータは Common Data Service for Apps に存在するため、Microsoft Power Platform からのツールを使用して Attract に固有のビジネス ニーズを組み込むことができます。

### <a name="powerapps"></a>PowerApps

PowerApps を使用して、Attract データに接続し、Microsoft Excel の式のような式を使用してロジックを追加するアプリを簡単に構築できます。 PowerApps を使用して構築するアプリは、Web、Apple iOS、Google Android デバイスで実行できます。

たとえば、履歴書をスキャンして候補者を Attract の位置にフィードする軽量アプリを構築することで、採用者にとって大学のキャリアフェアを簡単にすることができます。 または、組織のコンプライアンスのニーズを満たすのに役立つアプリを構築できます。 PowerApps およびアプリの構築にそれを使用する方法の詳細については、[Common Data Service for Apps へデータを統合](https://docs.microsoft.com/en-us/powerapps) を参照してください。

### <a name="microsoft-flow"></a>Microsoft Flow 

Microsoft Flow を使用して、Attract データの上で実行するワークフローを自動作成できます。 コードの書き込みなしで、数百の人気のアプリおよびサービスに簡単に接続できます。 Common Data Service for Apps で Attract ジョブ、候補者、アプリケーション エンティティとやりとりするフローを構築することで、さまざまな活動を自動化できます。 たとえば、候補者がオファーを受け入れると、オンボード チームに通知を送信でき、または Twitter にニュースが発表されます。 フローの詳細については、[Microsoft Flow ドキュメント](https://docs.microsoft.com/en-us/flow/) を参照してください。

### <a name="power-bi"></a>パワー BI

Power BI を使用すると、Attract データへのより深い洞察を与えるカスタム レポートおよびダッシュボードを構築し表示できます。 Power BI および対話型レポートとダッシュボードの作成方法の詳細については、[Power BI ドキュメント](https://docs.microsoft.com/en-us/power-bi/) を参照してください。

### <a name="custom-activities"></a>カスタム活動 

職務プロセス テンプレートのレベルで、または新しいジョブを作成している間に、PowerApps アプリおよび Web コンテンツ (iframe) 活動などのカスタム活動を追加できます。 これらの活動を使用すると、採用プロセスをカスタマイズしたり、組織に固有のビジネス ロジックを Attract にもたらすことができます。

#### <a name="powerapps-activity"></a>PowerApps 活動 

PowerApps 活動では、職務または職務プロセス テンプレートの作成者が採用フローを PowerApps アプリに埋め込むことができます。 アプリを作成し公開した後、活動コンフィギュレーションで、アプリ ID を入力できます。 PowerApps アプリを使用すると、Common Data Service for Apps へのデータの読み取りおよび書き込みができます。 アプリがフローするようにリンクもできます。 たとえば、採用担当者が電話面接の実施中に、フォームに入力するために使用するアプリがあります。 この場合、申請者が職務アプリ プロセスでさらに進めることができるかどうかを評価するフローにアプリをリンクできます。 このタイプの活動は、採用チームのメンバーでのみ表示できます。 PowerApps 活動をコンフィギュレーションする方法の詳細については、[Attract での活動](./activities-attract.md) を参照してください。

> [!NOTE]
> PowerApps 活動は、包括採用アドオンでのみ使用できます。

#### <a name="web-content-iframe-activity"></a>Web コンテンツ (iframe) 活動

Web コンテンツ (iframe) 活動を使用して、採用プロセスまたは候補者のポータルに構築したカスタム Web ソリューションを組み込むことができます。 Common Data Service for Apps から直接データの読み取りおよび書き込みができます。 フローをトリガーし、または Microsoft Azure 機能を利用できるように、ソリューションをカスタマイズすることもできます。 Web コンテンツ活動をコンフィギュレーションする方法の詳細については、[Attract での活動](./activities-attract.md) を参照してください。

> [!NOTE]
> Web コンテンツ活動は、包括採用アドオンでのみ使用できます。
