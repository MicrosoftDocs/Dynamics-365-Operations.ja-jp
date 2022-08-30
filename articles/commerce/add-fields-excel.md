---
title: 小売トランザクションを編集するために Excel ブックにフィールドを追加する
description: この記事では、Microsoft Dynamics 365 Commerce で小売トランザクションを編集できるように、Microsoft Excel ブックにフィールドを追加する方法について説明します。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: a5cf726e25364b883cfd644f064a9ed4fb6f509d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270402"
---
# <a name="add-fields-to-an-excel-workbook-to-edit-retail-transactions"></a>小売トランザクションを編集するために Excel ブックにフィールドを追加する

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で小売トランザクションを編集できるように、Microsoft Excel ブックにフィールドを追加する方法について説明します。

## <a name="overview"></a>概要

小売トランザクションを編集できるように Excel ファイルを生成するときに、ファイルの一部の既定のフィールドは入力されます。 生成された Excel ファイルに更新が必要なフィールドが既定で表示されない場合は、追加できます。

## <a name="add-fields-to-a-worksheet-in-an-excel-workbook"></a>Excel ブックのワークシートにフィールドを追加する

小売トランザクションを編集できるように、Excel ブックにフィールドを追加するには、次の手順に従います。

1. **明細書** ページ、**小売トランザクション** ページ、または **店舗の財務** ワークスペースの **トランザクションの検証エラー** タイル から Excel ファイルをダウンロードして開きます。
1. **デザイン** を選択します。
1. 目的のテーブルの鉛筆の記号を選択し、使用可能なフィールドの一覧で追加するフィールドを検索して選択します。
1. **追加** を選択してから **更新** を選択します。 フィールドの順序を変更できます。
1. 更新が完了したら、**更新** を選択して新しい列のデータをフェッチします。

これで、新しいフィールドとデータを Excel で編集できるようになります。

## <a name="additional-resources"></a>追加リソース

[現金売りトランザクションと現金管理トランザクションの編集と監査](edit-cash-trans.md)

[オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査](edit-order-trans.md)

[小売トランザクションの財務分析コードの編集](edit-financial-dim.md)

[小売トランザクションを編集するために Excel ブックを作成する](create-excel-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
