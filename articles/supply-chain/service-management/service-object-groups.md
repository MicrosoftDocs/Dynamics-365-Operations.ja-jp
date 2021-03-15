---
title: サービス対象グループ
description: 対象グループは、レポートや統計用の対象に関するデータの並べ替えやフィルタ処理を行う場合に便利です。
author: ShylaThompson
manager: tfehr
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a8e050afb44787072f78e2c971394956cb1026f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977591"
---
# <a name="service-object-groups"></a>サービス対象グループ 

[!include [banner](../includes/banner.md)]

対象グループは、レポートや統計用の対象に関するデータの並べ替えやフィルタ処理を行う場合に便利です。 たとえば、地理的な場所またはタイプ別に対象をグループ化できます。

## <a name="group-by-geographical-location"></a>地理的な場所別のグループ化

このグループ化の方法を使用すると、会社がサービスを提供しているさまざまな対象の場所を表示できます。 地理的な場所別に対象をグループ化すると、たとえば、特定の国/地域で既にサービスを提供している対象を識別する必要がある場合などにも役立ちます。

## <a name="example"></a>例

ベルギーの顧客からサービス センターに電話があり、対象 ABC のサービス合意を作成するように依頼されました。 ベルギーでサービスを提供しているすべての対象には、ベルギーという地理的な場所の対象グループを関連付けてあります。 フィルタとしてこのグループを使用して、プログラムに既に ABC のレコードがあるか、または新しい対象を設定する必要があるかどうかを確認できます。 

## <a name="group-by-type"></a>タイプ別のグループ化

このグループ化の方法を使用すると、会社でサービスを実行している対象のタイプを表示できます。 タイプ別に対象をグループ化すると、たとえば、既にプログラムに存在する同様の対象に基づいて新しい対象を作成する場合などにも役立ちます。

## <a name="example"></a>例

顧客から電話があり、空調機械 HIJ のサービス合意を設定するように依頼されました。 既にこの機械のレコードがありません。 ただし、空調装置という名前のオブジェクト グループを設定して、このグループは空調機械のすべてのオブジェクトに関連付されました。 したがって、他の空調機械すべてをすばやく検索し、これらのオブジェクトのテンプレート情報を使用してHIJ のサービス契約項目を作成できます。 この方法で対象グループを使用して、簡単に新しい対象を設定し、実行するサービス作業を決定できます。 

## <a name="create-service-object-groups"></a>サービス対象グループの作成

サービス対象を割り当てることができるグループを作成します。 サービス対象とは、サービスを実行する他の製品および在庫品目です。 サービス対象のグループ化することによって、同様のそして関連するサービス対象のレポートを作成できます。 たとえば、サービス対象グループは 2 種類のサービス対象から構成される場合があります: 1 番目のサービス対象はキット、2 番目のサービス対象はキットをインストールするサービスです。

サービス対象グループを作成するには、次の手順に従います:

1. **サービス管理 > 設定 > サービス対象 > サービス対象グループ** の順にクリックします。

2. **新規** をクリックして、新しいサービス対象グループを作成します。

3. サービス対象グループに一意の名前、および必要に応じて説明を入力します。

**サービス対象** フォームを使用すると、グループにサービス対象を割り当てることができます。 

## <a name="see-also"></a>参照

[サービス対象の作成](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]