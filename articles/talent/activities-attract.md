---
title: 採用プロセスへの活動の追加
description: このトピックでは、Microsoft Dynamics 365 Talent - Attract における採用プロセスに追加可能なさまざまなタイプの活動に関する情報を提供します。
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ce8c0bd74a41b9857538b37d0875583d06e8c11d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461788"
---
# <a name="add-activities-to-a-hiring-process"></a>採用プロセスへの活動の追加

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract の採用プロセスの一部として活動を追加することができます。 活動はプロセス テンプレートに追加することも、ジョブ内の採用プロセスに直接追加することもできます。 ジョブが定義されると、プロセス テンプレートが選択され、テンプレートに含まれている活動がジョブに適用されます。 テンプレートが選択されていない場合は、既定のテンプレートが使用されます。 採用プロセスは、テンプレートが適用された後にジョブに変更することもできます。

> [!NOTE] 
> プロセス テンプレートは、包括採用アドオンで利用できます。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。

## <a name="prospect-activity"></a>候補者活動

候補者活動は、見込顧客をジョブに追加できるかどうかを制御します。 既定値では、見込顧客をジョブに追加できます。 候補者活動をオフにするには、**候補者の有効化** オプションを **オフ** に設定します。 候補者活動をオンにすると、採用マネージャーは見込顧客を追加して表示することができ、**候補者** タブがジョブに表示されます。

> [!NOTE]
> 応募者を LinkedIn からジョブに追加できるようにするには、**候補者の有効化** オプションを **オン** にする必要があります。

## <a name="application-activity"></a>アプリケーションの活動

採用プロセス テンプレートにアプリケーションの活動が必要です。 申請の提出または申請のステージに追加する際に、候補者に電子メールを送信するには、**候補者に電子メールを送信** オプションを **オン** に設定します。

## <a name="interview-schedule-and-feedback-activity"></a>面接のスケジュールおよびフィードバック活動

この活動には 3 つのコンポーネントがあります: 候補者の面接可能日の要求、スケジュール、およびフィードバックです。 採用プロセスの一部として個別に使用する代わりに、プロセスの一部として、候補者の面接可能日の要求、スケジュール、およびフィードバックを対象とする場合は、職務テンプレートの面接の活動を使用します。 詳細については、[面接のスケジューリングおよびフィードバック](interview-scheduling-feedback.md) を参照してください。

## <a name="power-apps-activity"></a>Power Apps 活動

Power Apps 活動では、Microsoft Power Apps アプリを採用プロセスに埋め込むことができます。 アプリは、すべての申請者、内部申請者、外部申請者、または申請者には必要ありません。 アプリが必要とマークされている場合、ステージを進める前に完了する必要があります。 完了とみなされると、**JobApplicationStatus** フィールドは **完了** に設定する必要があります。 このフィールドは JobApplicationActivity エンティティに位置するので、Power Apps アプリは、ステージを進める前に、フィールドを更新する必要があります。 アプリが必要とマークされていない場合、活動はオプションのステップであり、アプリが完了していなくてもステージを進めることができます。

Power Apps 活動を採用プロセスに保存するには、Power Apps ID を入力する必要があります。 Power Apps ID を検索するには [Power Apps](https://web.powerapps.com) に移動して、**アプリ** を選択し、**詳細** を選択します。

既定では、Power Apps 活動は採用担当マネージャー、採用担当者、および委任に利用可能です。 **この活動の参加者の追加を許可** オプションを選択した場合は、採用チームからの追加参加者は Power Apps 活動を使用するアプリケーションを追加することができます。 たとえば、組織では、技術上の役割に対する面接の質問のライブラリである Power Apps アプリを作成しました。 組織では、現在新しいソフトウェア開発者を採用しており、ソフトウェア開発者のロールの採用プロセスに Power Apps 活動が追加されました。 **この活動の参加者の追加を許可** オプションが選択されている場合、ソフトウェア開発者のロールの申請者を表示している採用担当者または採用マネージャーが Power Apps 活動に面接者を追加できます。 ユーザーは、面接の質問を記載したアプリを表示できます。

> [!NOTE]
> Power Apps 活動は、包括採用アドオンでのみ使用できます。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。

## <a name="youtube-activity"></a>YouTube 活動

YouTube 活動では、採用プロセスの一環として YouTube ビデオを共有できます。 YouTube 活動を採用プロセスに保存するには、YouTube ビデオの URL を指定する必要があります。 **雇用チーム**、**内部候補者のみ**、**外部の応募者**、または **すべての候補者** にコンテンツを表示することを選択できます。 Power Apps 活動のように、採用チームの参加者が活動に追加することを許可できます。 候補者へのコンテンツ表示を選択する場合、採用プロセスではなく候補者エクスペリエンスの一部としてのみビデオが表示されます。

> [!NOTE]
> YouTube 活動は、包括採用アドオンでのみ使用できます。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。

## <a name="web-content-activity"></a>Web コンテンツ活動

Web コンテンツ活動では、オンライン コンテンツを採用プロセスに埋め込むことができます。 Web コンテンツ活動を採用プロセスに保存するには、コンテンツの URL を指定する必要があります。 **雇用チーム**、**内部候補者のみ**、**外部の応募者**、または **すべての候補者** にコンテンツを表示することを選択できます。 Power Apps と YouTube 活動のように、採用チームの参加者が活動に追加するのを許可することができます。 候補者へのコンテンツ表示を選択する場合、採用プロセスではなく候補者エクスペリエンスの一部としてのみ Web コンテンツが表示されます。 表示されるコンテンツのサイズを選択できます。

> [!NOTE]
> Web コンテンツ活動は、包括採用アドオンでのみ使用できます。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。

## <a name="microsoft-forms-activity"></a>Microsoft Forms 活動

Microsoft Forms 活動では、Microsoft Forms 活動を採用プロセスに埋め込むことができます。 Microsoft Forms では、クイズ、アンケート、およびポーリングを作成できます。 Microsoft Forms 活動を採用プロセスに保存するには、フォームの URL を指定する必要があります。 **雇用チーム**、**内部候補者のみ**、**外部の応募者**、または **すべての候補者** にコンテンツを表示することを選択できます。 Power Apps、YouTube および Web コンテンツ活動のように、採用チームの参加者が活動に追加するのを許可することができます。 候補者へのコンテンツ表示を選択する場合、採用プロセスではなく候補者エクスペリエンスの一部としてのみフォームが表示されます。

Microsoft Forms では、組織外のユーザーがアンケートやクイズに応答できるように設定を変更できます。 この場合、ユーザーは応答を匿名で送信します。 アンケートやクイズに誰が記入したのかを見たい場合は、アンケートやクイズの一部として回答者に名前を入力することを要求できます。

> [!NOTE]
> Microsoft Forms 活動は、包括採用アドオンでのみ使用できます。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。

## <a name="offer-activity"></a>オファー アクティビティ

採用プロセス テンプレートには、オファー アクティビティが必要です。 統合オファー管理アプリを使用するには、**オファーの準備でオファー管理アプリを起動** を **オン** にします。 この設定がオフの場合、候補者はオファー アプリに表示されないので、手動で候補者のオファー アクティビティへの更新を追跡する必要があります。 採用マネージャーがオファー アプリで候補者のオファーを準備できるかどうかを定義するには、**採用マネージャーはオファーの準備が可能** を **オン** にします。 ジョブが関連付けられている複数の職位がある場合、同じ位置番号に対して複数のオファーを準備するかどうか選択できます。 ジョブごと、職位ごとに 1 つだけオファーを許可する場合は、**ジョブ内で再利用される職位を許可** を **オフ** にします。

> [!NOTE]
> 統合オファー管理アプリは、包括採用アドオンでのみ使用できます。 詳細については、[Microsoft Dynamics 365 Talent - Attract のバージョンは何ですか](./attract-comprehensive-hiring.md) を参照してください。


