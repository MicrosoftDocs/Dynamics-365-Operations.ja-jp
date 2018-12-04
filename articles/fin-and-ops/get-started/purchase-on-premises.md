---
title: "Finance and Operations (オンプレミス) の購入"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations (オンプレミス) を購入して展開する方法について説明します。"
author: maertenm
manager: AnnBe
ms.date: 02/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: ec1c6028f8d3d16bc5e95fc9b6be34cdf38a5d89
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="buy-finance-and-operations-on-premises"></a>Finance and Operations (オンプレミス) の購入

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations (オンプレミス) では、組織のニーズに最適な幅広いライセンスの種類を取りそろえております。  Finance and Operations (オンプレミス) のライセンス取得方法を理解するには、PartnerSource の[ライセンス ガイド](https://go.microsoft.com/fwlink/?linkid=852079)にアクセスできるパートナーと協力してください。 組織のライセンスを購入する準備ができたら、パートナーと協力して、このトピックで説明している手順に従います。

> [!IMPORTANT]
>   Azure を含む、任意のパブリック クラウド インフラストラクチャでサポートされていない、Microsoft Dynamics 365 for Finance and Operations のオンプレミス配置。 

<a name="purchase-client-access-licenses"></a>クライアント アクセス ライセンスを購入
-------------------

Finance and Operations (オンプレミス) を実行するには、ライセンス ガイドに従って組織の適切な数のクライアント アクセス ライセンス (CAL) を取得する必要があります。 個々のユーザーに購入された CAL は、ユーザーが使用する権限のある機能を決定します。 ユーザー CAL は、[マイクロソフト ボリューム ライセンス サービス センター](https://www.microsoft.com/Licensing/servicecenter/default.aspx)から購入できます。

<a name="purchase-server-licenses"></a>サーバー ライセンスを購入
--------------------------

Finance and Operations (オンプレミス) を実行しているすべてのサーバーにサーバー ライセンスが必要です。 サーバー ライセンスを購入した後、パートナーと協力して [PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/) からライセンス ファイルをダウンロードします。 このライセンス ファイルは、そこに含まれる詳細が Lifecycle Services (LCS) プロジェクトを設定するときに使用されるため扱いやすい状態にしておきます。

パートナーは、顧客の Finance and Operations (オンプレミス) ライセンス ファイルを PartnerSource ビジネス センターからこれらの手順を使用してダウンロードできます。

1.  [PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/) にログオンします。

3.  **Find A Customer** フィールドに顧客名およびアカウント番号を入力し、次に**検索**をクリックします。

4.  顧客の会社名をクリックします。 これにより、**顧客概要**ページが開きます。

5.  **登録されている製品** で **登録キー** をクリックします。

6.  **ライセンス キーのバージョンを要求して表示** フィールドで **バージョン 07** を選択します。

7.  **ライセンスキーの表示**をクリックします。

8.  **ライセンス キーの要求**ページで、**現在のライセンス/登録キーのダウンロード**を選択します。

9.  **ファイルのダウンロード**ダイアログ ボックスの**名前を付けて保存**をクリックし、**名前を付けて保存**ダイアログボックスでライセンス ファイルをダウンロードするフォルダを選択し、**保存** をクリックします。

**注記**: PartnerSource Business Center に登録キーが表示されない場合は、PartnerSource Business Center の**登録キーの表示が可能**が**はい**に設定されていることを確認する必要があります。

<a name="get-started-with-lifecycle-services-lcs"></a>Lifecycle Services (LCS) の使用を開始する
---------------------------------------

Finance and Operations (オンプレミス) を購入するには、Microsoft Online Services ID が必要です。 Microsoft Online Services ID は、Finance and Operations (設置型) のための必要なコンポーネントを含む LCS プロジェクトをプロビジョニングするために使用されます。 LCS は、オンプレミス環境が準備され、ビジネス プロセス モデルが作成/アップロードされ、修正プログラムが使用可能で、サポート ケースが入力および管理され、ライセンス キーのシリアル番号の有効化が送信されるなどのサービスです。

Microsoft Online Services ID は、Finance and Operations (設置型) をエンティティが所有するハードウェアと環境にプロビジョニングして登録するために必要です。 プロビジョニングおよび登録プロセスを完了するには、プロビジョニング ガイド (下へのリンク) を参照してください。 Microsof tオンライン サービス ID が既に存在する場合は、グローバル管理者によって、プロセスを完了する必要があります。 Microsoft オンライン サービスの ID を最初に作成する場合は、プロセスを開始する担当者がグローバル管理者になります。

既存の Microsoft オンライン サービス試用版または有料サブスクリプションがある場合は、サインアップ時に作成された Microsoft オンライン サービス ID が既にあります。 次のリンクをクリックするときは、オンプレミス配置にこの同じ Azure Active Directory (AAD) テナントを使用する場合に、このアカウントでログインを選択します。

プロビジョニング ガイドへのアクセスについては、こちらを参照してください。

- [CustomerSource のプロビジョニング ガイド](https://go.microsoft.com/fwlink/?linkid=852080)

- [PartnerSource のプロビジョニング ガイド](https://mbs.microsoft.com/partnersource/global/deployment/documentation/user-guides/D365Ops_OnPremEEProvisionGuide)

LCS にログインすると、プロジェクトが自動的にプロビジョニングします。 LCS プロジェクトでは、Finance and Operations (設置型) を配置できます。 LCS プロジェクトの使用開始の詳細については、[Lifecycle Services でのオンプレミス プロジェクトの作成](../../dev-itpro/lifecycle-services/lbd-create-lcs-on-prem-project.md) を参照してください。

