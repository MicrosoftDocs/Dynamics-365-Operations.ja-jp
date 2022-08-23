---
title: Dynamics 365 Commerce サンドボックス環境のプロビジョニング
description: この記事では、組み込みのデモ データを使用するデモまたはプログラム用に Microsoft Dynamics 365 Commerce サンドボックス環境をプロビジョニングする方法について説明します。
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 1fc50f98055f1df72d255a5be6e863570564b183
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283644"
---
# <a name="provision-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce サンドボックス環境のプロビジョニング

[!include [banner](includes/banner.md)]

この記事では、組み込みのデモ データを使用するデモまたはプログラム用に Microsoft Dynamics 365 Commerce サンドボックス環境をプロビジョニングする方法について説明します。 運用環境を設定するプロセスは、デモ データには多くの前提条件が用意されているので、似ていますが、より込み入ったものになります。

開始する前に、この記事に目を通して、プロセスに必要な内容を把握することをお勧めします。

Commerce の環境を正しく提供するには、後で Commerce を準備するときに使用する環境および Commerce Scale Unit (CSU) 用のパラメータを指定する必要があります。 この記事の手順では、プロビジョニングを完了するために必要なすべての手順と、使用する必要があるパラメーターについて説明します。

Commerce 環境のプロビジョニングが正常に完了した後、いくつかのプロビジョニング後の手順を完了して、使用のために準備する必要があります。 一部の手順は、システムのどの側面を使用するかに応じて使用するオプションです。 オプションの手順は、後からいつでも完了できます。

プロビジョニング後に Commerce プレビュー環境を構成する方法については、[Commerce サンドボックスの構成](cpe-post-provisioning.md) を参照してください。 Commerce プレビュー環境のオプション機能を構成する方法については、[Commerce サンドボックス環境のオプション機能の構成](cpe-optional-features.md)を参照してください。

## <a name="prerequisites"></a>必要条件

Commerce プレビュー環境をプロビジョニングする前に、次の前提条件が整っている必要があります。

- Microsoft Dynamics Lifecycle Services (LCS) ポータルへのアクセス許可があります。
- 既存の Microsoft Dynamics 365 パートナーまたは顧客で、実装プロジェクトが既に作成され、LCS で使用できます。  
- Commerce システムの管理者グループとして使用される Azure Active Directory (Azure AD) セキュリティ グループが作成され、その ID が使用可能になりました。
- 評価とレビューのモデレーター グループとして使用される Azure AD セキュリティ グループが作成され、その ID が使用可能になりました。 (このセキュリティ グループは、Commerce のシステム管理グループと同じにすることができます。)
- LCS 内に本社のインスタンスを配置しました。 詳細については、[新規環境のデプロイ](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) を参照してください。

このリストは包括的なものではないことに注意してください。 問題が発生した場合は、Microsoft パートナーの連絡先に問い合わせてください。

## <a name="provision-your-commerce-environment"></a>Commerce 環境のプロビジョニング

次の手順は、Commerce 環境をプロビジョニングする方法を説明しています。 この手順を正常に完了すると、Commerce 環境を構成する準備が整います。 下で説明するすべての手順は、LCS ポータルで起こります。

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit (CSU) を初期化する (クラウド)

CSU を初期化するには、次の手順に従います。

1. LCS で、リストから、環境を選択します。
1. 右側の **環境** ビューで、**完全な詳細** を選択します。 環境の詳細のビューが表示されます。
1. **環境機能** の **環境の管理** セクションで、**管理** を選択します。
1. **Commerce Scale Unit** タブで、**初期化** を選択します。 **スケール単位の追加** ビューが表示されます。
1. **地域** フィールドで、環境を配置したのと同じか、またはそれに近い地域を選択します。
1. **バージョン** ボックスの一覧で、使用可能な最新バージョンを選択します。
1. **初期化** を選択します。
1. Commerce Scale Unit の初期化を確認する必要がある警告ダイアログ ボックスで、**はい** を選択します。 CSU がプロビジョニング用にキューに格納されました。
1. 続行する前に、CSU が **成功** となっていることを確認します。 初期化には約 2 ~ 5 時間かかります。

環境の詳細ビューに **管理** リンクが見つからない場合は 、Microsoft の連絡先に問い合わせてください。

### <a name="initialize-e-commerce"></a>E コマースの初期化

Commerce を初期化するためには、次の手順に従います。

1. **E コマース** タブで、**設定** を選択します。
1. **E コマース環境名** フィールドに名前を入力します。 この名前は E コマース インスタンスを指す URL の一部に表示されることに注意してください。
1. **Commerce Scale Unit の名前** フィールドで、リストから CSU を選択します。 (リストには 1 つのオプションのみが必要です。)

    **E コマースの地域** フィールドは自動的に設定されます。

1. **次へ** を選択して続行します。
1. **サポートされているホスト名** フィールドに、`www.fabrikam.com` などの有効なドメインを入力します。
1. **システム管理者の AAD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力し、虫眼鏡記号を選択して検索結果を表示します。 リストで正しいセキュリティ グループを選択します。
1.  **評価とレビュー モデレーター用 AAD セキュリティ グループ** フィールドに、使用するセキュリティ グループの名前の最初の数文字を入力し、虫眼鏡記号を選択して検索結果を表示します。 リストで正しいセキュリティ グループを選択します。
1. **評価とレビュー サービスを有効にする** オプションを、**はい** のままにします。
1. **初期化** を選択します。 **E コマース** タブが選択されているところでは、**コマースの管理** ビューが再度表示されます。 E コマースの初期化を開始しました。
1. 続行する前に、Commerce の初期化状態が **初期化成功** になるまでお待ちください。
1. 右下の **リンク** で、次のリンクの URL をメモします。

    * **E コマース サイト** – E コマース サイトのルートへのリンク。
    * **Commerce サイト ビルダー** – サイト管理ツールへのリンク。

## <a name="next-steps"></a>次のステップ

Commerce 環境のプロビジョニングと構成のプロセスを続行するには、[Commerce 環境の構成](cpe-post-provisioning.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce サンドボックス環境の構成](cpe-post-provisioning.md)

[Dynamics 365 Commerce サンドボックス環境での BOPIS の構成](cpe-bopis.md)

[Dynamics 365 Commerce サンドボックス環境のオプション機能の構成](cpe-optional-features.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (クラウド)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure ポータル](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce Web サイト](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
