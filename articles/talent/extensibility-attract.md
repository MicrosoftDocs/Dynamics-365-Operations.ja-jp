---
title: Attract での拡張性
description: このトピックでは、Microsoft Power Platform を使用して Microsoft Dynamics 365 for Talent - Attract を拡張する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichsew
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 52790fbe500d9f55bc9cc86fba5d54f30b11e559
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505867"
---
# <a name="extensibility-in-attract"></a>Attract での拡張性

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent は、Common Data Service プラットフォームの上に構築され、Microsoft Power Platform および Common Data Service が提供する機能を使用してさまざまな方法で拡張できます。 したがって、Microsoft PowerApps および Microsoft Flow を使用して、システムをコンフィギュレーションおよびカスタマイズできます。 Microsoft Power BI を使用して、人々に関する追加の分析を取得することもできます。 さらに、PowerApps および Web コンテンツ (iframe) 活動などの新しいカスタム活動は、採用プロセスをこれまで以上に適応しやすくします。 これらの活動を使用することにより、採用プロセスをビジネス ニーズとプロセスに合わせることができ、採用チームと候補者の両方にシームレスでカスタマイズされた経験があることを確認できます。

## <a name="extending-option-sets-in-attract"></a>Attract のオプション セットの拡張

**オプション セット** (候補リスト) は、エンティティに含めることができるフィールドのタイプです。 これは一連のオプションを定義します。 オプション セットがフォームに表示される場合、ドロップダウン リスト コントロールを使用します。  Attract には、オプション セットである複数のフィールドがあります。  不採用理由フィールド、雇用タイプフィールド、および勤続タイプフィールドをはじめとするオプション セットを拡張するための機能を導入します。   また、追加するオプションに対して、ローカライズされた表示ラベルを追加することができます。 詳細については、[オプション セット ラベルのカスタマイズ](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/customize-labels-support-multiple-languages)を参照してください。

> [!NOTE]
> LinkedIn 機能へのジョブ求人転記には、**ジョブの詳細**ページの**雇用タイプ**および**勤続タイプ**フィールドの使用が必要です。 これらのフィールドの既定値は LinkedIn でサポートされ、ジョブが転記されるときに表示されます。 そのため、LinkedIn にジョブ求人を転記していて、これらのフィールドの既存のオプション セット値を変更した場合、ジョブ求人は転記されますが、LinkedIn はカスタム**雇用タイプ**および**勤続タイプ**の値を表示しません。  

下の一覧は、**不採用理由**フィールドと業務に固有の値を更新する手順です。  

1. **不採用理由**オプション セットを拡張するには、[PowerApps 管理 Web サイト](https://admin.powerapps.com)に移動します。
2. アカウントにサインインするよう求められる可能性があります。 Dynamics365 や Office365 にサインインするために使用する userID およびパスワードの資格情報を指定し、**次へ**をクリックします。
3. **環境**タブで管理する環境を選択し、ダブルクリックして**詳細**タブにアクセスします。
4. **詳細**タブで **Dynamics 365 管理センター**を選択します。
5. 変更するインスタンスを選択し、**開く**を選択します。
6. **設定**、**カスタマイズ**に移動し、**システムをカスタマイズ**を選択します。
7. **エンティティ**を選択し、グループを展開して、オプション セットを拡張するエンティティを検索します。 この例では、**求人応募エンティティ**になります。
8. **フィールド** オプションを選択し、オプション セットを拡張するフィールドに移動します。 この例では、**msdyn_rejectionreason** になります。 フィールドをダブルクリックします。
9. **オプション セット** フィールドで、**編集**を選択します。
10. **+** アイコンを選択します。
11. **ラベル**を入力します。  (これは重複しない、一意の値である必要があります)。
12. **保存** を選択します。
13. ページ上部の**発行**を選択します。

## <a name="take-advantage-of-the-microsoft-power-platform"></a>Microsoft Power Platform を活用 

Attract からのすべてのデータは Common Data Service に存在するため、Microsoft Power Platform からのツールを使用して Attract に固有のビジネス ニーズを組み込むことができます。

### <a name="powerapps"></a>PowerApps

PowerApps を使用して、Attract データに接続し、Microsoft Excel の式のような式を使用してロジックを追加するアプリを簡単に構築できます。 PowerApps を使用して構築するアプリは、Web、Apple iOS、Google Android デバイスで実行できます。

たとえば、履歴書をスキャンして候補者を Attract の位置にフィードする軽量アプリを構築することで、採用者にとって大学のキャリアフェアを簡単にすることができます。 または、組織のコンプライアンスのニーズを満たすのに役立つアプリを構築できます。 PowerApps およびアプリの構築にそれを使用する方法の詳細については、[Common Data Service へのデータの統合](https://docs.microsoft.com/en-us/powerapps)を参照してください。

### <a name="microsoft-flow"></a>Microsoft Flow 

Microsoft Flow を使用して、Attract データの上で実行するワークフローを自動作成できます。 コードの書き込みなしで、数百の人気のアプリおよびサービスに簡単に接続できます。 Common Data Service Attract ジョブ、候補者、アプリケーション エンティティとやりとりするフローを構築することで、さまざまな活動を自動化できます。 たとえば、候補者がオファーを受け入れると、オンボード チームに通知を送信でき、または Twitter にニュースが発表されます。 フローの詳細については、[Microsoft Flow の開発者ドキュメント](https://docs.microsoft.com/en-us/flow/) を参照してください。

### <a name="power-bi"></a>Power BI

Power BI を使用すると、Attract データへのより深い洞察を与えるカスタム レポートおよびダッシュボードを構築し表示できます。 Power BI および対話型レポートとダッシュボードの作成方法の詳細については、[Power BI ドキュメント](https://docs.microsoft.com/en-us/power-bi/) を参照してください。

### <a name="custom-activities"></a>カスタム活動 

職務プロセス テンプレートのレベルで、または新しいジョブを作成している間に、PowerApps アプリおよび Web コンテンツ (iframe) 活動などのカスタム活動を追加できます。 これらの活動を使用すると、採用プロセスをカスタマイズしたり、組織に固有のビジネス ロジックを Attract にもたらすことができます。

#### <a name="powerapps-activity"></a>PowerApps 活動 

PowerApps 活動では、職務または職務プロセス テンプレートの作成者が採用フローを PowerApps アプリに埋め込むことができます。 アプリを作成し公開した後、活動コンフィギュレーションで、アプリ ID を入力できます。 PowerApps アプリを使用すると、Common Data Service へのデータの読み取りおよび書き込みができます。 アプリがフローするようにリンクもできます。 たとえば、採用担当者が電話面接の実施中に、フォームに入力するために使用するアプリがあります。 この場合、申請者が職務アプリ プロセスでさらに進めることができるかどうかを評価するフローにアプリをリンクできます。 このタイプの活動は、採用チームのメンバーでのみ表示できます。 PowerApps 活動をコンフィギュレーションする方法の詳細については、[Attract での活動](./activities-attract.md) を参照してください。

> [!NOTE]
> PowerApps 活動は、包括採用アドオンでのみ使用できます。

#### <a name="web-content-iframe-activity"></a>Web コンテンツ (iframe) 活動

Web コンテンツ (iframe) 活動を使用して、採用プロセスまたは候補者のポータルに構築したカスタム Web ソリューションを組み込むことができます。 Common Data Service から直接データの読み取りおよび書き込みができます。 フローをトリガーし、または Microsoft Azure 機能を利用できるように、ソリューションをカスタマイズすることもできます。 Web コンテンツ活動をコンフィギュレーションする方法の詳細については、[Attract での活動](./activities-attract.md) を参照してください。

> [!NOTE]
> Web コンテンツ活動は、包括採用アドオンでのみ使用できます。
