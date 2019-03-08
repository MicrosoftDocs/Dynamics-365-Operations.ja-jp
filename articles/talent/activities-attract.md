---
title: プロセスの活動
description: このトピックでは、採用プロセスで使用できるさまざまなタイプの活動に関する情報を提供します。
author: ''
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c32db1f563466f05b9fef1a03578392888c0b7e6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2019
ms.locfileid: "374760"
---
# <a name="activities-in-the-hiring-processes"></a>採用プロセスの活動

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Talent: Attract の採用プロセスの一部として活動を追加することができます。 活動はプロセス テンプレートに追加することも、ジョブ内の採用プロセスに直接追加することもできます。 ジョブが定義されると、プロセス テンプレートが選択され、テンプレートに含まれている活動がジョブに適用されます。 テンプレートが選択されていない場合は、既定のテンプレートが使用されます。 採用プロセスは、テンプレートが適用された後にジョブに変更することもできます。

> [!NOTE] 
> プロセス テンプレートは、包括採用アドオンで利用できます。

## <a name="prospect-activity"></a>候補者活動

候補者活動は、見込顧客をジョブに追加できるかどうかを制御します。 既定値では、見込顧客をジョブに追加できます。 候補者活動をオフにするには、**候補者の有効化**オプションを**オフ**に設定します。 候補者活動をオンにすると、採用マネージャーは見込顧客を追加して表示することができ、**候補者**タブがジョブに表示されます。

## <a name="application-activity"></a>アプリケーションの活動

採用プロセス テンプレートにアプリケーションの活動が必要です。 申請の提出または申請のステージに追加する際に、候補者に電子メールを送信するには、**候補者に電子メールを送信**オプションを**オン**に設定します。

## <a name="interview-schedule-and-feedback-activity"></a>面接のスケジュールおよびフィードバック活動

この活動には 3 つのコンポーネントがあります: 候補者の面接可能日の要求、スケジュール、およびフィードバックです。 採用プロセスの一部として個別に使用する代わりに、プロセスの一部として、候補者の面接可能日の要求、スケジュール、およびフィードバックを対象とする場合は、職務テンプレートの面接の活動を使用します。 詳細については、[面接のスケジューリングおよびフィードバック](interview-scheduling-feedback.md) を参照してください。

## <a name="powerapps-activity"></a>PowerApps 活動

PowerApps 活動では、Microsoft PowerApps アプリを採用プロセスに埋め込むことができます。 アプリは、すべての申請者、内部申請者、外部申請者、または申請者には必要ありません。 アプリが必要とマークされている場合、ステージを進める前に完了する必要があります。 アプリが必要とマークされていない場合、活動はオプションのステップであり、アプリが完了していなくてもステージを進めることができます。

PowerApps 活動を採用プロセスに保存するには、PowerApps ID を入力する必要があります。 PowerApps ID を検索するには [PowerApps](https://web.powerapps.com) に移動して、**アプリ**を選択し、**詳細**を選択します。

**この活動の参加者の追加を許可**オプションを選択した場合は、PowerApps 活動を使用するアプリケーションの他の要因を追加することができます。 たとえば、組織では、技術上の役割に対する面接の質問のライブラリである PowerApps アプリを作成しました。 組織では、現在新しいソフトウェア開発者を採用しており、ソフトウェア開発者のロールの採用プロセスに PowerApps 活動が追加されました。 **この活動の参加者の追加を許可**オプションが選択されている場合、ソフトウェア開発者のロールの申請者を表示している採用担当者または採用マネージャーが PowerApps 活動に人を追加できます。 ユーザーは、面接の質問を記載したアプリを表示できます。

> [!NOTE]
> PowerApps 活動は、包括採用アドオンでのみ使用できます。

## <a name="youtube-activity"></a>YouTube 活動

YouTube 活動では、採用プロセスの一環として YouTube ビデオを共有できます。 YouTube 活動を採用プロセスに保存するには、YouTube ビデオの URL を指定する必要があります。 PowerApps 活動については、参加者が活動に追加するのを許可することができます。 **候補のみに表示**オプションを選択した場合、ビデオは候補者エクスペリエンスの一部としてのみ表示されます。 これは、Attract の採用プロセスには表示されません。

> [!NOTE]
> YouTube 活動は、包括採用アドオンでのみ使用できます。

## <a name="web-content-activity"></a>Web コンテンツ活動

Web コンテンツ活動では、オンライン コンテンツを採用プロセスに埋め込むことができます。 YouTube 活動を採用プロセスに保存するには、コンテンツの URL を指定する必要があります。 PowerApps および YouTube 活動については、参加者が活動に追加するのを許可することができます。 **候補のみに表示**オプションを選択する場合、コンテンツは候補者エクスペリエンスの一部としてのみ表示されます。 これは、Attract の採用プロセスには表示されません。 表示されるコンテンツのサイズを選択できます。

> [!NOTE]
> Web コンテンツ活動は、包括採用アドオンでのみ使用できます。

## <a name="microsoft-forms-activity"></a>Microsoft Forms 活動

Microsoft Forms 活動では、Microsoft Forms フォームを採用プロセスに埋め込むことができます。 Microsoft Forms では、クイズ、アンケート、およびポーリングを作成できます。 Microsoft Forms 活動を採用プロセスに保存するには、フォームの URL を指定する必要があります。 PowerApps、YouTube、および Web コンテンツ活動については、参加者が活動に追加するのを許可することができます。 **候補のみに表示**オプションを選択する場合、フォームは候補者エクスペリエンスの一部としてのみ表示されます。 これは、Attract の採用プロセスには表示されません。

Microsoft Forms では、組織外のユーザーがアンケートやクイズに応答できるように設定を変更できます。 この場合、ユーザーは応答を匿名で送信します。 アンケートやクイズに誰が記入したのかを見たい場合は、アンケートやクイズの一部として回答者に名前を入力することを要求できます。

> [!NOTE]
> Microsoft Forms 活動は、包括採用アドオンでのみ使用できます。
